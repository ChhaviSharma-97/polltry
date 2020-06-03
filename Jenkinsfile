pipeline {
    agent any
    triggers {
    pollSCM('* * * * *')
    }
    environment {
        GIT_CRED_ID = 'git'
        REPO_URL = 'https://github.com/ChhaviSharma-97/polltry.git'
        REPO_URL_2 = 'https://github.com/ChhaviSharma-97/JSL_helloword.git'
    }
    stages {
        
        stage('Git Checkout') {
            steps {
                checkout([
	                $class: 'GitSCM', 
	                branches: [[name: '*/master']],  
	                userRemoteConfigs: [[credentialsId: GIT_CRED_ID, url: REPO_URL]]
	                ])
	           sh "ls -l"
            }
        }
        stage('Start') {
            steps {
                echo 'Running build automation'
                sh 'echo "Start Successful!"'
                
            }
        }
        
        
        stage('Git Checkout 2') {
            steps {
                checkout([
	                $class: 'GitSCM', 
	                branches: [[name: '*/master']],  
	                userRemoteConfigs: [[credentialsId: GIT_CRED_ID, url: REPO_URL_2]]
	                ])
	           sh "ls -l"
            }
        }
        
        stage('Done') {
            steps {
                echo 'Running build automation'
                sh 'echo "End Successful!"'
                
            }
        }
        
    }
}
