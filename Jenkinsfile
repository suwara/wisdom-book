pipeline {
     agent any
     stages {
          stage('Source') {
               steps {
                    git branch: 'main',
                        url: 'https://github.com/suwara/wisdom-book'
               }
          }
          stage('Build') {
               steps {
                    bat 'C:/Users/User/apache-maven-3.9.4-bin/apache-maven-3.9.4/bin/mvn package -DskipTests'
               }
          }
          stage('Test') {
               steps {
                    echo 'testing...'
               }
          }
          stage('Deploy') {
               steps {
                    bat 'java -jar ./target/book-1.0.jar'
               }
          }
     }
}
