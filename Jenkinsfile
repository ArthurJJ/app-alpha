pipeline {
    agent any

    options {
        timestamps()
        timeout(time: 10, unit: 'MINUTES')
    }

    stages {
        stage('Build') {
            steps { sh 'sh scripts/build.sh' }
        }
        stage('Tests') {
            steps { sh 'sh scripts/test.sh' }
        }
        stage('Déploiement') {
            steps { echo 'Déploiement simulé de alpha' }
        }
    }

    post {
        success { echo 'NOTIF : alpha OK' }
        failure { echo 'NOTIF : alpha KO' }
    }
}
