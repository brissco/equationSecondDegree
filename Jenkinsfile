pipeline {
    agent any

    tools {
        // Assurez-vous que Maven est disponible
        maven 'Maven 3.9.5'
    }

    stages {
        stage('Clean and Compile') {
            steps {
                // Nettoie et compile le projet
                bat 'mvn clean compile'
            }
        }

        stage('Run Unit Tests') {
            steps {
                // Exécute les tests unitaires
                bat 'mvn test'
            }
        }

        stage('Package Application') {
            steps {
                // Package l'application en .jar ou .war
                bat 'mvn package'
            }
        }

        // Si votre projet a besoin d'autres étapes, ajoutez-les ici

    }

    post {
        always {
            // Actions à réaliser après les étapes, comme le nettoyage
            echo 'Le pipeline Jenkins est terminé'
        }
    }
}
