pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
               // withMaven(maven : 'maven3.3.9') {
                    bat 'mvn clean compile'
              //  }
            }
        }

        stage ('Testing Stage') {

            steps {
              //  withMaven(maven : 'maven3.3.9') {
                    bat 'mvn test'
               // }
            }
        }


        stage ('Deployment Stage') {
            steps {
              //  withMaven(maven : 'maven3.3.9') {
                    bat 'mvn install'
               // }
            }
        }
    }
}