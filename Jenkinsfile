pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                        withEnv([
                            "PYTHON_HOME=C:\\env\\python-3.12.4-embed-amd64",
                            "PIP_HOME=C:\\Users\\cdied\\AppData\\Local\\Packages\\PythonSoftwareFoundation.Python.3.12_qbz5n2kfra8p0\\LocalCache\\local-packages\\Python312\\Scripts",
                            "PATH=${env.PATH};${PYTHON_HOME};${PIP_HOME}"
                        ]) {
                            // Choisissez la commande en fonction de votre script
                            bat 'echo "Running on Windows"'
                            bat 'pip install pandas' // Installer les dÃ©pendances
                            bat 'python data_analysis.py' // ExÃ©cuter le script Python
                        }
                }
            }
        }
    }
}
