pipeline {
  agent none
  stages {
    stage('input') {
      agent any
      input {
        message "What is your first name?"
        ok "Submit"
        parameters {
          string(defaultValue: 'Dave', name: 'FIRST_NAME', trim: true) 
        }
      }
      steps {
        echo "Good Morning, $FIRST_NAME"
        sh '''
          hostname
          cat /etc/redhat-release
        '''
      }
    }
  }
}
