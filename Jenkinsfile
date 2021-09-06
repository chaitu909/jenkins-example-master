pipeline {
    agent any
    
    tools {
        maven 'apache-maven-3.8.1'
        jdk 'openjdk-11.0.11_9'
    }

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'apache-maven-3.8.1') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'apache-maven-3.8.1') {
                    sh 'mvn test'
                }
            }
        }


        /*stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'apache-maven-3.8.1') {
                    sh 'mvn deploy'
                }
            }
        }*/
    }
}