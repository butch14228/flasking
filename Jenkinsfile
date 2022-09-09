pipeline {
  agent any
  stages {
    stage('git ') {
      steps {
        git(branch: 'main', url: 'https://github.com/butch14228/flasking')
      }
    }

    stage('build') {
      steps {
        sh 'docker build -t butch14228/flask_app .'
      }
    }

    stage('docker login') {
      steps {
        sh 'docker login -u butch14228 -p dckr_pat_II9M67fJ-Uz7qShph7LrB9Uc1ig'
      }
    }

    stage('docker push') {
      steps {
        sh 'docker push butch14228/flask_app'
      }
    }

  }
}