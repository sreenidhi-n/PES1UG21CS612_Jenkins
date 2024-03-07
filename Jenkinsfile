pipeline{
  agent any
  stages{
    stage('Clone repository'){
      steps{
        checkout([$class:'GitSCM', branches:[[name: '*/main']], userRemoteConfigs: [[url:'https://github.com/sreenidhi-n/PES1UG21CS612_Jenkins.git']]])
      }
    }
    stage('Build'){
      steps{
        build 'PES1UG21CS612-1'
        sh 'g++ main.cp -o output'
      }
    }
    stage('Test'){
      steps{
        sh './output'
      }
    }
    stage('Deploy'){
      steps{
        echo 'deploy
      }
    }
  }
  post{
    failure{
      error 'Pipeline failed'
    }
  }
}
