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
                 params.Age.toInt() > 22
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
