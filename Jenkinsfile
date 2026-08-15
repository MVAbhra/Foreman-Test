pipeline {

    agent any

    tools {

        maven 'Maven-3'
    }

    environment {

        SPRING_DATASOURCE_URL = credentials('RAILWAY_DB_URL')

        SPRING_DATASOURCE_USERNAME = credentials('RAILWAY_DB_USERNAME')

        SPRING_DATASOURCE_PASSWORD = credentials('RAILWAY_DB_PASSWORD')
    }

    stages {

        stage('Build') {

            steps {

                sh 'mvn clean install'
            }
        }
    }
}