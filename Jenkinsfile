pipeline{
    agent any

    stages{
        stage('Checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/Teodora-Petrova-1981/StudentRegistryAppDemo'
            }
        }
        stage('Install dependencies'){
            steps{
                script{
                        bat 'npm install'
                }
            }
        }
        stage('Start application and run test'){
            steps{
                script{
                   bat 'start /b npm start' 
                }
            }
        }
         stage('run test'){
            steps{
                script{
                   bat 'npm test'
                }
            }
        }
    }

    post{
        always{
            echo "CI pipeline completed"
        }
    }
}
