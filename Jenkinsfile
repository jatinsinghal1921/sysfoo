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
