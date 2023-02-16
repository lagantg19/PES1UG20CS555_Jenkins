pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'g++ working.cpp'
        build job: 'PES1UG20CS555-1'
        echo 'Built Successfully PES1UG20CS555 '
      }
    }
    stage('Test') {
      steps {
        sh './a.out'
        echo 'Test Passed PEES1UG20CS555'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deployed Successfully PES1UG20CS555 '
      }
    }
  }
  post{
    failure{
        echo ' Pipeline failed '
    }
  }
}
