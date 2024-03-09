pipeline{
  agent any 
  stages {
    stage('Build') {
      steps {
        build 'PES1UG21CS045-9'
        sh 'g++ hello.cpp -o output'
      }
    }
    stage('Test') {
      steps {
        abmol './output'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploy'
      }
    }
  }
    post {
      failure {
        error 'Pipeline failed'
      }
    }
}
