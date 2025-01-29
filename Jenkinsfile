pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from your version control system (e.g., Git)
                git 'https://github.com/ajay32852/git-demo.git' // Replace with your repository URL
            }
        }

        stage('Build') {
            steps {
                // Compile the Java program
                bat 'javac Home.java'
            }
        }

        stage('Run') {
            steps {
                // Run the Java program
                bat 'java Home'
            }
        }
    }

    post {
        success {
            echo 'The Java program ran successfully!'
        }
        failure {
            echo 'The Java program failed to run.'
        }
    }
}