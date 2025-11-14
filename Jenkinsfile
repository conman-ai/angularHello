pipeline {
    agent any
    tools{
      nodejs 'Nodejs Local installation'
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

            sh """"
              echo 'ready for deploy'
            """
            
            
          }
         
    }
}
