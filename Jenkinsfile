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
                echo "Age: ${Age}"
            }
        }
        stage("Docker ps"){
            steps{
                sh "/usr/local/bin/docker ps"
            }
        }
        stage("Third"){
            steps{
                sh "python3 test.py"
            }
        }
    }
}
