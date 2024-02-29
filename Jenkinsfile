pipeline {
  agent any
  stages {
    stage('check out') {
      steps {
        git(url: 'https://github.com/yli202/JacocoExample', branch: 'master')
      }
    }

    stage('Build ') {
      steps {
        sh 'mvn clean compile'
      }
    }

    stage('Test ') {
      steps {
        sh 'mvn test'
      }
    }

    stage('Code Coverage ') {
      steps {
        jacoco()
      }
    }
#  stage("sonarqube") {
 #           steps {
  #            withSonarQubeEnv('Sonarqube_server') {
   #             sh 'mvn clean package sonar:sonar'
    #          }
     #       }
      #    }
  }
}
