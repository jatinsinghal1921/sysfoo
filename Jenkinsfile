pipeline {
  agent any
  tools{
     maven "Maven 3.6.3"
  }
  stages{
      stage("Build"){
          steps{
              sh "mvn compile"
          }
      }
    stage("Random Stage"){
          steps{
            echo "Random Stage - 4"
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
