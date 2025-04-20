pipeline {
   agent any
    tools {
        nodejs "nodejs"
    }
    stages {
        stage("NODE") {
            steps {
                script {
                    echo "Workspace dir: ${WORKSPACE}"
                    powershell "scanPackages.ps1"
                }
            }
        }
    }
}