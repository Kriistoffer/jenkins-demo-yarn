pipeline {
   agent any
    tools {
        nodejs "nodejs"
    }
    stages {
        stage("NODE") {
            steps {
                script {
                    sh "grep 'auditSummary' ${WORKSPACE}/test.json" > realoutput.json
                    def output = readJSON(file: "${WORKSPACE}/realoutput.json")

                    echo "Totaldependencies: ${output}"


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