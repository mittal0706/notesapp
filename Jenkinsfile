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
