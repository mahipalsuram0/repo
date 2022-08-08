pipeline {
  agent any
  environment {
    myenv1="dev"
  }
  parameters {
  string defaultValue: 'dev', description: 'dev environment', name: 'Environment', trim: false
  choice choices: ['linux', 'hp-ux', 'solaris'], description: '', name: 'ostype'
}

  stages {
    stage('working with variables') {
      steps {
        script {
          def myval1=20
          println "myval1 value is ${myval1}"
          println "myenv1 environment is ${env.myenv1}"
          //printing global variables
          println "Printing build id ${env.BUILD_ID}"
          // printing parameters values
          println "my environment parameter is ${params.Environment}"
          println "my selected ostype is ${params.ostype}"
        }
      }
    }
  }
}
