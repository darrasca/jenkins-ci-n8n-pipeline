pipeline {
  agent any

  environment {
    IMAGE_NAME = "n8n-ci"
    TAG = "build-${BUILD_NUMBER}"
  }

  stages {
    stage('Clonar repo') {
      steps {
        git branch: 'main',
            url: 'https://github.com/darrasca/jenkins-ci-n8n-pipeline.git'
      }
    }

    stage('Construir imagen Docker') {
      steps {
        script {
          docker.build("${IMAGE_NAME}:${TAG}")
        }
      }
    }

    stage('Verificar imagen') {
      steps {
        sh "docker images | grep ${IMAGE_NAME}"
      }
    }
  }

  post {
    success {
      echo "✅ Build completado: ${IMAGE_NAME}:${TAG}"
    }
    failure {
      echo "❌ Build fallido"
    }
  }
}
