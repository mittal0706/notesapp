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
          image 'python'
        }
      }
        
            steps {
                sh 'pip3 install -r requirements.txt' 
            }
        }
  }
}
