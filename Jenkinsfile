pipeline {
    agent { label 'master' }
    stages {
       stage('build') {
          steps {
             bat 'cd C:/altisource/software-dump/gradle-4.1-bin/practice'
             bat 'gradle hello1'
            
                echo 'Multiline'
                echo 'Example'
           
             echo 'not using shell'
          }
       }
    }
}
