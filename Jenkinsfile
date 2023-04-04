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
    stage('Install dependencies'){
      steps{
        script{
          sh 'sudo apt install python3-pip'
          sh 'sudo pip install -r requirements.txt'
        }
      }
    
    }
  }
}
