pipeline{
    agent any
    stages{
        stage("Build"){
            steps{
                sh 'g++ -o PES2UG20CS192-1 PES2UG20CS192_1.cpp'
                echo 'Build successfull'
            }
        }

        stage('Test'){
            steps{
                sh './PES2UG20CS192-1'
            }
        }
        stage('Deploy'){
            steps{
                echo 'Deployment successful'
            }
        }
    post{
        always{
            echo "Pipeline completed"
        }
        failure{
            echo "Pipeline failed"
        }
    }
     }
}
