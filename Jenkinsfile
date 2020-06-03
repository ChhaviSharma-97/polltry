pipeline {
    agent any
    triggers {
    pollSCM(H/5 * * * *')
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
