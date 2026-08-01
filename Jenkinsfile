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
        stage('Build') { 
            steps { 
                bat 'npm run build' 
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
```[cite: 1]

---

#### 3. Push & Build
1. Save `Jenkinsfile` and push it from VS Code terminal[cite: 1]:
   ```powershell
   git add .
   git commit -m "Use checkout scm"
   git push origin main