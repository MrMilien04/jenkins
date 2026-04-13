pipeline {
    agent {
        docker {
            image 'maven:3.9.5-amazoncorretto-17'
        }
    }


    stages {
        stage('clone') {
            steps {
                git branch: 'main', changelog: false, poll: false, url: 'https://github.com/MrMilien04/jenkins'
            }
        }
        stage('build') {
            steps {
                sh 'mvn clean'
                sh 'mvn test'
            }
        }
    }
}
