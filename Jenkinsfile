pipeline {
  agent any {

    stages
        stage("git checkout")
    {
      git branch: 'main', url: 'https://github.com/pragjnaa/handtime.git'
    }
    stage("deploy to container")
    {
    sh 'docker build -t pragjna/handtime .'
    sh  'docker run -d -p 81:80 pragjna/handtime'
      
      
    }
  }
}

    
  
