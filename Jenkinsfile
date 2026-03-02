pipeline {
    agent any

    stages {
        stage('Fetching File..') {
            steps {
               git "https://github.com/Kaustubhqt/javaset"
            }
        }
        stage('Build') {
            steps {
                echo 'Building Project....'
                bat "javac Hello.java"
            }
        }
        stage('Executing..') {
            steps {
                echo 'Executing Program'
                bat "java Hello"
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying Project..'
            }
        }
    }
    post{
        success{
            echo "Pipeline executed successfully!"
        }
        failure{
             echo "Pipeline failed"
        }
    }
}
