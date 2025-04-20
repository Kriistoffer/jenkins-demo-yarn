pipeline {
   agent any
    tools {
        nodejs "nodejs"
    }
    stages {
        stage("NODE") {
            steps {
                script {
                    sh "grep 'auditSummary' ${WORKSPACE}/test.json > realoutput.json"
                    def output = readJSON(file: "${WORKSPACE}/realoutput.json")

                    echo "Totaldependencies: ${output.data.totalDependencies}"

                    powershell """
                    $SOLUTIONROOT = "${WORKSPACE}"
                    Function ListAllPackages ($BaseDirectory)

                    {

                        Write-Host "Starting Package List - This may take a few minutes ..."

                        $PACKAGECONFIGS = Get-ChildItem -Recurse -Force $BaseDirectory -ErrorAction SilentlyContinue |

                            Where-Object { ($_.PSIsContainer -eq $false) -and  ( $_.Name -eq "packages.config")}

                        ForEach($PACKAGECONFIG in $PACKAGECONFIGS)

                        {

                            $path = $PACKAGECONFIG.FullName

                            $xml = [xml]$packages = Get-Content $path

                            foreach($package in $packages.packages.package)

                            {

                                Write-Host "$($package.id) - $($package.version)"

                            }

                        }

                    }
                    ListAllPackages $SOLUTIONROOT
                    """
                }
            }
        }
    }
}