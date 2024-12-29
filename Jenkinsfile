pipeline {
    agent any
    stages {
        stage('Pull Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/mahmoudelbrolosy/20216092'
            }
        }
        stage('Set Permissions') {
            steps {
                sh 'chmod +x run_ls.sh'
            }
        }
        stage('Execute Script') {
            steps {
                script {
                    if (isUnix()) {
                        sh './run_ls.sh'
                    } else {
                        bat 'run_ls.bat'
                    }
                }
            }
        }
    }
}
