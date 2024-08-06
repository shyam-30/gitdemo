pipeline{
  agent any 
  stages{
    stage('checkout'){
steps{
  git branch: 'main', url: 'https://github.com/shyam-30/gitdemo.git'
}
    }
    stage('install'){
      steps{
        sh 'echo this is installation '
      }
    }
    stage('deploy'){
    steps{
      sh 'echo jao or so jao gn '
    }
    }
  }
    post{
      always{
        echo 'pipeline completed'
      }
    }
  
}
