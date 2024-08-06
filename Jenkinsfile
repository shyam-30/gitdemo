pipeline{
  agent any 
  stages{
    stage('checkout'){
steps{
  git 'https://github.com/shyam-30/gitdemo.git'
}
    }
    stage('build'){
      steps{
        echo 'building'
      }
    }
    stage('deploy'){
    steps{
      sh 'cp index.html /var/www/html/index.html'
    }
    }
    post{
      always{
        echo 'pipeline completed'
      }
    }
  }
}
