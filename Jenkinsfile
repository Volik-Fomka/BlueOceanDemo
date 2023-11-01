pipeline {
  agent any
  stages {
    stage('CheckoutGit') {
      steps {
        git(url: 'https://github.com/Volik-Fomka/BlueOceanDemo.git', branch: 'main')
      }
    }

    stage('Build') {
      steps {
        echo 'This is build'
      }
    }

    stage('Deploy to Dev 1') {
      parallel {
        stage('Deploy') {
          steps {
            sleep 30
            echo 'finish dev1'
          }
        }

        stage('Deploy to Dev 2') {
          steps {
            sleep 50
            echo 'finish dev2'
          }
        }

      }
    }

    stage('test') {
      steps {
        echo 'TEST'
      }
    }

  }
}