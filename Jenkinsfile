pipeline {
    agent any
    environment {
        PIP_HOME = 'C:\\env'
        PYTHON_HOME = 'C:\\env\\python-3.12.4-embed-amd64'
        PATH = "${env.PATH};${PIP_HOME};${PYTHON_HOME};${PYTHON_HOME}\\Scripts;${PYTHON_HOME}\\Lib\\site-packages"
    }
    stages {
        stage('Checkout') {
            steps {
               git branch: 'main', url: 'https://github.com/awoune/jenkins-data-pipeline.git'
            }
        }
        stage('Build') {
            steps {
                script {
                    if (isUnix()) {
                        sh 'echo "Running on Unix"'
                        // Add your Unix-specific build commands here
                    } else {
                        bat 'echo "Running on Windows"'
                        bat 'python --version' // Vérifier la version python
                        bat 'pip.pyz --version' // Vérifier la version pip
                        //bat 'pip.pyz install pandas' // Installer les dÃ©pendances
                        //bat 'python data_analysis.py' // ExÃ©cuter le script Python
                        // Add your Windows-specific build commands here
                    }
                }
            }
        }
    }
}
