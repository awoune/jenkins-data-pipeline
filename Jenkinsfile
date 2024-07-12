pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    // Choisissez la commande en fonction de votre script
                    bat 'echo "Running on Windows"'
                    bat 'pip install pandas' // Installer les dépendances
                    bat 'python data_analysis.py' // Exécuter le script Python
                }
            }
        }
    }
}
