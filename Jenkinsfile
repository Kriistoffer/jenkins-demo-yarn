pipeline {
   agent any
    tools {
        nodejs "nodejs"
    }
    stages {
        stage("NODE") {
            steps {
                dir("src") {
                    echo pwd
                    sh "yarn install"
                }
            }
        }
    }
}