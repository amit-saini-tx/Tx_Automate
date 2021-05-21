pipeline {
  agent any
  stages {
    stage('Git') {
      steps {
        build 'Tx_Automate_Git'
      }
    }

    stage('Automation_Pipeline') {
      parallel {
        stage('Performance_Test') {
          steps {
            build 'Tx_Automate_Performance'
          }
        }

        stage('Web_Test') {
          steps {
            build 'Tx_Automate_Web'
          }
        }

        stage('API_Test') {
          steps {
            build 'Tx_Automate_API'
          }
        }

        stage('Mobile_Test') {
          steps {
            build 'Tx_Automate_Mobile'
          }
        }

      }
    }

  }
}