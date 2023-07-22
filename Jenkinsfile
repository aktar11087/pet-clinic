pipeline {
    agent any
    
    tools {
        jdk "Jdk11"
        maven "Maven3"
    }

    stages {
        stage('Git Checkout') {
            steps {
             git branch: 'feature2', url: 'https://github.com/aktar11087/pet-clinic.git'
            }
        }
        stage('Compile') {
            steps {
             sh "mvn clean compile"
            }
        }
        stage('Build') {
            steps {
             sh "mvn clean package -DskipTests=true"
            }
        }
    }
}
