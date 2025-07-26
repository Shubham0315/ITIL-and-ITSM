pipeline {
  agent any 

  environment {
    SONARQUBE_ENV = 'SQServer'
    CHANGE_ID = "CHG-${env.BUILD_NUMBER}"
  }

  stages {
    stage('Checkout') {
      steps {
        echo "Fetching code for the change : ${env.CHANGE_ID}"
        checkout scm
      }
    }

    stage('Build') {
      steps {
        echo "Building the application"
        sh './build.sh'
      }
    }

    stage('Static code analysis') {
      steps {
        echo "Running sonarqube analysis"
        withSonarQubeEnv("${SONARQUBE_ENV}") {
          sh 'sonar-scanner'
        }
      }
    }

    stage('Change Approval CAB') {
      when {
        expression {
          return params.REQUIRES_APPROVAL == true
        }
      }
      steps {
        timeout(time: 2, unit: 'HOURS') {
          input message: "Approve change deployment (Change ID: ${env.CHANGE_ID})?", ok: "Approve"
        }
      }
    }
  }


  post {
    success {
      echo "Change ${env.CHANGE_ID} is deployed"
      mail to: "ops-team@shubham.com",
        subject: "Deployment success"
        body: "Change ${env.CHANGE_ID} deployed to prod successfully"
    }
  }
}

    
