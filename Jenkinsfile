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
            steps {
                sh 'pip install -r requirements.txt' 
            }
        }
  }
}
