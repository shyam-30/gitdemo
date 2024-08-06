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
        sh ''' sudo apt install httpd -y 
               sudo service httpd.service start '''
      }
    }
    stage('deploy'){
    steps{
      sh 'cp index.html /var/www/html/index.html'
    }
    }
  }
    post{
      always{
        echo 'pipeline completed'
      }
    }
  
}
