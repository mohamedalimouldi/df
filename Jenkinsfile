pipeline{
    agent any
    stages{
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/mohamedalimouldi/github-jenkins.git'
            }
        }
        stage('Email Notification'){
            steps{
                script {
                    def readmeContent = readFile('README.md')
                }
                emailext(
                    subject: 'commit changes',
                    body: "un nodsfdf",
                    to: 'medalimouldi.1@gmail.com'
                    )
            }
        }
    }
}
