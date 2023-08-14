pipeline {
      agent any
      stages {
            stage('Init') {
                  steps {
                        echo 'Hi, this Kobbara nshul from Home :D '
                        echo 'We are Starting the Testing'
                  }
            }
            stage('Build') {
                  steps {
                        echo 'Building Sample Maven Project'
                  }
            }
            stage('Deploy') {
                  steps {
                        echo "Deploying in Staging Area"
                  }
            }
            stage('Deploy to PROD') {
                  steps {
                        echo "Deploying in PROD Area"
                  }
            }
      }
}