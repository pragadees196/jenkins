pipeline{
    agent any
    parameters{
        string(name: "Name",default: "")
        choice(name: "Age",choices:[20,21,22,23])
    }
    stages{
        stage("First"){
            steps{
                echo "My name is ${name}"
            }
        }
        stage("Second"){
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
