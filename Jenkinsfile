pipeline {
  agent{
    docker { image 'maven:3.6.3-jdk-11-slim' }
  }
  stages{
      stage("Build"){
          steps{
              echo "This is Build Stage"
              sh "mvn compile"
          }
      }
    stage("Random Stage"){
          steps{
            echo "Random Stage-feature"
          }
      }
      stage("Package"){
          steps{
              sh "mvn package -DskipTests"
          }
      }
  }

  post{
    always{
        echo 'This pipeline is completed..'
        echo "You are Awesome"
    }
  }
}
