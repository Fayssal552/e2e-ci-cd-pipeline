pipeline{
    agent{
        label "jenkins-slave"
    }
    tools {
        jdk 'Java11'
        maven 'Maven3'
    }
    
    stages{
        stage("Cleanup Workspace"){
            steps {
                cleanWs()
            }

        }
        
        stage("Checkout from SCM"){
            steps {
                git branch: 'main', credentialsId: 'github', url: 'https://github.com/Fayssal552/end-to-end-ci-cd.git'
            }

        }

        stage("Build Application"){
            steps {
                sh "mvn clean package"
            }

        }

        stage("Test Application"){
            steps {
                sh "mvn test"
            }

        }

        stage("Sonarqube Analysis") {
            steps {
                script {
                    withSonarQubeEnv(credentialsId: 'SonarToken') {
                        sh "mvn sonar:sonar"
                    }
                }
            }

        }
        
    }
        
}
