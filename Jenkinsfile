pipeline {
  agent any
  tools{
     maven "Maven 3.6.3"
  }
  stages{
      stage("Build"){
          steps{
              echo "This is Build Stage"
              sh "mvn compile"
          }
      }
      stage("Package"){
          steps{
              echo "This is package stage - 2"
              sh "mvn package -DskipTests"
          }
      }
  }

  post{
    always{
        echo 'This pipeline is completed..'
    }
  }
}
