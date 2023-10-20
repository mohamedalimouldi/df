pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                script {
                    // Checkout the Git repository
                    def gitRepo = checkout([
                        $class: 'GitSCM',
                        branches: [[name: 'main']],
                        userRemoteConfigs: [[url: 'https://github.com/mohamedalimouldi/df.git']]
                    ])
                }
            }
        }
        stage('Send Email') {
            steps {
                script {
                    // Read the README.md file from the repository
                    // Send an email notification
                    emailext body: "Un nouveau commit a été effectué dans le référentiel.\n\nContenu du README.md",
                        subject: 'Nouveau commit',
                        to: 'medalimouldi.1@gmail.com',
                        mimeType: 'text/plain'
                }
            }
        }
    }
}
