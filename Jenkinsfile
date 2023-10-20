pipeline {
    agent any
    stages {
        stage('Hello') {
            steps {
                echo "Hello world"
                    }
            }
        }
    post{
        always{
            mail to: "medalimouldi.1@gmail.com",
            subject: "Test Email",
            body: "Test"
        }
    }
}
