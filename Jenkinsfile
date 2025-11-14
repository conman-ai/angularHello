pipeline {

  agent any

  options {

    buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5')

  }

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
          sh """
            echo 'ready to deploy'
           """
        }
    }
}
