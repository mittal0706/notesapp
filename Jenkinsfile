pipeline{
agent any
  stages{
    stage('Git checkout'){
      steps{
        script{
          withCredentials([gitUsernamePassword(credentialsId: 'github', gitToolName: 'Default')]) {
          }
        }
      }
    }
    stage('Install dependencies') {
      agent {
        docker { 
          image 'python:3.8-alpine'
        }
      }
        
            steps {
                sh 'pip3 install -r requirements.txt' 
            }
        }
  }
}
