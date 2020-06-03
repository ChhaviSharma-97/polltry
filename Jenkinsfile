pipeline {
    agent any
    triggers {
    pollSCM('* * * * *')
    }
    stages {
        
        stage('Start') {
            steps {
                echo 'Running build automation'
                sh 'echo "Start Successful"'
                
            }
        }
    }
}
