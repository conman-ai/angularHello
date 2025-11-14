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
                npx ng build
              """  
            }
        }
        stage("deploy"){
          when {
            branch 'main'
          }
          steps{

            sh '''
              echo 'ready for deploy'
            '''
           }
         
      }
  }
}
