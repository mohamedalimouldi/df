pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                script {
                    git branch: 'main', url: 'https://github.com/mohamedalimouldi/df.git'
                }
            }
        }
        stage('Send Email') {
            steps {
                script {
                    def readmeContent = readFile('README.md')
                    emailext(
                        subject: 'Nouveau commit',
                        body: "Un nouveau commit a été effectué dans le référentiel.\n\nContenu du README.md:\n\n${readmeContent}",
                        to: 'medalimouldi.1@gmail.com'
                    )
                }
            }
        }
    }
}
