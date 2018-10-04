pipeline {
    agent any
    tools {nodejs "node"}
    environment {
        JENKINS_GITHUB_TOKEN = credentials('git_token')
    }
    stages {
      stage('Cloning Git') {
         steps {
            git 'https://github.com/g4gulshan/node-js-sample.git'
      }
    }       
      stage('Install dependencies') {
         steps {
            bat 'npm install '   
      }
    }
    stage('Start Server') {
      steps {
         bat 'npm start'
      }
    }    
    }      
  }
