pipeline{
agent any
  stages{
    stage('Git checkout'){
      steps{
        script{
          git branch: 'main', credentialsId: 'github', url: 'https://github.com/mittal0706/notesapp.git'
        }
      }
    }
  }
}
