pipeline { 
  agent any 
  stages { 
    stage('Checkout') { steps { git 'https://github.com/atharva-0605/EXP-3.git' } }  
    stage('Install') { steps { sh 'npm install' } } 
    stage('Test') { steps { sh 'npm test' } } 
    stage('Build') { steps { sh 'npm run build' } } 
  } 
  post { 
    success { echo 'Pipeline completed successfully!' } 
    failure { echo 'Pipeline failed.' } 
  } 
}
```[cite: 1]

*(Note: If you are running Jenkins on Windows natively, replace `sh` with `bat` like `bat 'npm install'`).*

4. Save the file (`Ctrl + S`) and push it to GitHub[cite: 1]:
   ```powershell
   git add .
   git commit -m "Add Jenkinsfile"
   git push origin main