pipeline {
  agent any
  stages {
    stage('Initialize') {
      steps {
        echo 'Moj prvi pipeline'
      }
    }

    stage('Build') {
      steps {
        sh '''cd mysite
python manage.py runserver & pid=$!
sleep 60
kill -INT $pid'''
      }
    }

  }
}