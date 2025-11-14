pipeline {

  agent any

  options {

    buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5')

    }
  stages{
    stage("build"){
            steps{
              sh """ 
                npm install
                ng build
              """  
            }
        }
        stage("deploy"){
          when {
            branch 'main'
          }
          steps{
            sh """
            echo 'ready to deploy'
           """
          }
          
        }
    }
  
}
