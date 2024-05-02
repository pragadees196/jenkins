pipeline{
    agent any
    stages{
        stage("first"){
            steps{
                sh 'python3 test.py'
            }
        }
        stage("second"){
            steps{
                echo 'second'
            }
        }
        stage("Third"){
            steps{
                echo "Third"
            }
        }
    }
}
