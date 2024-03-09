pipeline{
  agent any 
  stages {
    stage('Build') {
      steps {
        build 'PES1UG21CS045-1'
        sh 'g++ random.cpp -o output'
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
