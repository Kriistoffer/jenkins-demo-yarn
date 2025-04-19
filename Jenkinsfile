pipeline {
   agent any
    tools {
        nodejs "nodejs"
    }
    stages {
        stage("NODE") {
            steps {
                script {
                    def list = readJSON(file: "${WORKSPACE}/test.json")
                    // echo "list: ${list}"
                    echo "Size: ${list.size()}"
                    // def list = readFile("${WORKSPACE}/test.txt").readLines()
                    // def lastLine

                    // for (item in list) {
                    //     lastLine = item
                    // }
                    
                    // new File("${WORKSPACE}/output.json").write(lastLine)
                    // def output = readJSON(file: "output.json")

                    // echo "Printing high vuln: ${output.data.vulnerabilities.high}"

                    // def myFile = readJSON(file: "output.json")
                    // myFile.write(lastLine)
                    // def myFile = new File("output.json")
                    // myFile.append(lastLine)
                }
            }
        }
    }
}