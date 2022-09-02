pipeline {
  agent any
  stages {
    stage ("build"){
      steps {
        echo "running build......."
        nodejs('myNodejs') {
          sh 'yarn install'
        }
      }
    }
      stage ("test"){
      steps {
        echo "testing build time interval one......"
        withGradle() {
          sh './gradlew -v'
        }
      }
    }
      stage ("depoyj"){
      steps {
        echo "deploying build......"
      }
    }
  }
  
}  
