pipeline{
    agent any
    parameters{
        string(name: "Name")
        choice(name: "Age",choices:[20,21,22,23])
    }
    stages{
        stage("First"){
            steps{
                echo "My name is ${name}"
            }
        }
        stage("Second"){
            when{
               expression{
                 def age = params.Age ?: 0 // Default to 0 if Age parameter is null or empty
                 age.toInteger() > 22
               }
            }
            steps{
                echo "Age: ${params.Age}"
            }
        }
        stage("Third"){
            steps{
                sh "python3 test.py"
            }
        }
    }
}
