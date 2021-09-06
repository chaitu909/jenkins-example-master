pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                maven(maven : 'apache-maven-3.8.1') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                maven(maven : 'apache-maven-3.8.1') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                maven(maven : 'apache-maven-3.8.1') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}