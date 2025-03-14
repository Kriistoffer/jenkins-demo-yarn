pipeline {
   agent any
    tools {
        nodejs "nodejs"
    }
    stages {
        stage("NODE") {
            steps {
                script {
                    def list = readFile("${WORKSPACE}/test.txt").readLines()
                    def lastLine

                    for (item in list) {
                        lastLine = item
                    }
                    
                    new File("${WORKSPACE}/output.json").write(lastLine)
                    echo "Printing the last line: ${lastLine.data}"

                    // def myFile = readJSON(file: "output.json")
                    // myFile.write(lastLine)
                    // def myFile = new File("output.json")
                    // myFile.append(lastLine)
                }
            }
        }
    }
}