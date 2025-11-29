pipeline{
  agent any
  stages{
    stage('Checkout'){
      steps{
        git branch: 'master', url: 'https://github.com/likhitha050/pyitem2'
      }
    }
    stage('compile'){
      steps{
        echo 'compilng java file...'
        sh 'javac J1.java'
      }
    }
    stage('Run'){
      steps{
        echo 'Running java file...'
        sh 'java J1'
      }
    }
  }
      post{
      success{
        echo 'Build and execution successful...'
      }
      failure{
        echo 'Build failed!'
      }
    }
}
