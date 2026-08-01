pipeline { 
    agent any 
    stages { 
        stage('Checkout') { 
            steps { 
                checkout scm 
            } 
        }  
        stage('Install') { 
            steps { 
                bat 'npm install' 
            } 
        } 
        stage('Test') { 
            steps { 
                bat 'npm test' 
            } 
        } 
    } 
    post { 
        success { 
            echo 'Pipeline completed successfully!' 
        } 
        failure { 
            echo 'Pipeline failed.' 
        } 
    } 
}