pipeline{
  agent any
  stages{
    stage("Frontend"){
      steps{
        echo "Building the application.."
        echo "Application Built"
        nodejs("Node-20.2"){
          sh 'yarn install'
        }
      }
    }
    stage("Backend"){
      steps{
        echo "Testing the application.."
        withGradle(){
          sh './gradlew -v'
        }
      }
    }
    stage("deploy"){
      steps{
        echo "Deploying the application.."
      }
    }
  }
}
