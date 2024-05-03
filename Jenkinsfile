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
                 params.Age > 22
               }
            }
            steps{
                echo "age: ${age}"
            }
        }
        stage("Third"){
            steps{
                sh "python3 test.py"
            }
        }
    }
}
