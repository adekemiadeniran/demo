pipeline {
    agent any

    stages {

        stage('Start') {
            steps {
                echo 'Pipeline Started'
            }
        }

        stage('Show Files') {
            steps {
                sh 'ls'
            }
        }

        stage('Backup File') {
            steps {
                sh 'cp notes.txt backup'
            }
        }

        stage('Check Backup') {
            steps {
                sh 'cat backup'
            }
        }

        stage('Finish') {
            steps {
                echo 'Backup Completed'
            }
        }
    }
    
post {

   success {

       mail to: 'oyejope@gmail.com',
       subject: 'Build Success',
       body: 'Pipeline Success'

   }

  }
}
    
