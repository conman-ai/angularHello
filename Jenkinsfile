pipeline {

  agent any

  tools{
	nodejs 'Nodejs Local installation'

  }

  options {

    buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5')

    }
  stages{
    stage("build"){
	when{
	   branch 'develop'
	}
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

            sh """"
              echo 'ready for deploy'
            """
           }
         
      }
  }
}
