pipeline {
    agent any

    stages {

        stage('Run Build'){
            agent {
                docker {
                    image 'node:18-alpine'
                }
            }

            steps {
                sh '''
                  echo "Building Node App"
                  npm run build
                '''
            }
    }

    stage('Run Test') {
        agent {
            docker {
                image 'node:18-alpine'
            }
        }

        steps {
            sh '''
                echo "Running Test"
                npm run test
            '''
        }
    }

    stage('Deploy'){

        steps {
            sh '''
                echo "Deploying APP in AWS EC2 Instances
            '''
        }

    }

}

}