pipeline {
    agent any
    stages {
        stage('Build Application') {
            steps {
                script {
                    
                        bat 'mvn clean install'
                    
                }
            }
        }
        stage('Deploy CloudHubs') {
            
            steps {
                echo 'Deploying mule project due to the latest code commit...'
                echo 'Deploying to the configured environment....'
                script {
                   
                        bat "mvn clean deploy -DmuleDeploy"
                    
                }
            }
        }
    }
}
