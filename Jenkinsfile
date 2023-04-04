pipeline{
agent any
  stages{
    stage('Git checkout'){
      steps{
        script{
          git branch: 'main', url: 'https://github.com/mittal0706/notesapp.git'
          }
        }
    }
    stage('Install dependencies') {
           agent {
              docker {
                image 'python:3'
                }
            steps {
                sh 'pip install -r requirements.txt'
            }
           }   
  }
 }
}
