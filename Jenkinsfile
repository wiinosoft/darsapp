pipeline {
  agent {
    node {
      label 'Refactor'
    }

  }
  stages {
    stage('VM-Creation') {
      steps {
        echo 'Vm-ready'
      }
    }

    stage('Back-Start') {
      parallel {
        stage('Back-Start') {
          steps {
            echo 'Install Django'
            timeout(time: 2, activity: true)
          }
        }

        stage('Front-Start') {
          steps {
            echo 'Install React'
            timeout(time: 2, activity: true, unit: 'DAYS')
          }
        }

      }
    }

    stage('Stage0-begin') {
      steps {
        echo 'start-stage0'
      }
    }

    stage('Endpoints') {
      steps {
        echo 'EndPoints-Examine'
      }
    }

    stage('R/D') {
      steps {
        echo 'endpoint R/D- Estimate Refactor Time'
      }
    }

    stage('Code-Refactor') {
      parallel {
        stage('Code-Refactor') {
          steps {
            echo 'Ruhollah-code-refactor-start'
          }
        }

        stage('UI/UX-Refactor') {
          steps {
            echo 'Rezaei-hosseini-redesign'
          }
        }

        stage('Openvidu-video') {
          steps {
            echo 'Video-Connect'
          }
        }

      }
    }

    stage('Testing') {
      steps {
        echo 'Test-Refactored-Code'
      }
    }

  }
}