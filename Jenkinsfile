pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
               git "https://github.com/Kaustubhqt/javaset"
            }
        }
        stage('Publish') {
            steps{
           publishHTML([
               allowmissing:true,
               alwaysLinktoLastBuild:false,
               KeepAll:false,
               reportDir:'.',
               reportFiles:'index.html',
               reportName:'My HTML Page'
               ]);
            }
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

