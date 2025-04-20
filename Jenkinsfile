pipeline {
   agent any
    tools {
        nodejs "nodejs"
    }
    stages {
        stage("NODE") {
            steps {
                script {
                    powershell "${WORKSPACE}/scanPackages.ps1 -rootDirectory "${WORKSPACE}""
                }
            }
        }
    }
}