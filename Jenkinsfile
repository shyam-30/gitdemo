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
        sh ''' sudo apt-get update -y && sudo apt-get install nginx -y 
               sudo service nginx.service start '''
      }
    }
    stage('deploy'){
    steps{
      sh 'cp index.html /usr/share/nginx/html/index.html'
    }
    }
  }
    post{
      always{
        echo 'pipeline completed'
      }
    }
  
}
