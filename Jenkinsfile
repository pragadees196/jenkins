pipeline{
    agent any
    environment{
        name = "Pragadees"
        age = 22
    }
    stages{
        stage("First"){
            steps{
                echo "My name is {name}"
            }
        }
        stage("Second"){
            steps{
                echo "age: {age}"
            }
        }
        stage("Third"){
            steps{
                echo "python3 test.py"
            }
        }
    }
}
