pipeline {
  agent any
  stages {
    stage('dev') {
      steps {
        build 'dev'
      }
    }

    stage('Deploy QA') {
      steps {
        echo 'QA'
      }
    }

    stage('UI Testing') {
      parallel {
        stage('UI Testing') {
          steps {
            echo 'UI Testing'
          }
        }

        stage('API Testing') {
          steps {
            echo 'api testing'
          }
        }

        stage('DB Testing') {
          steps {
            echo 'Db testing'
          }
        }

      }
    }

    stage('Deploy UAT') {
      steps {
        echo 'uat'
      }
    }

    stage('Certify UAT') {
      steps {
        echo 'UAT'
      }
    }

    stage('ProdDeploy') {
      steps {
        echo 'Prod'
      }
    }

  }
}