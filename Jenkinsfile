pipeline {
    agent any
    tools{
      nodejs 'Nodejs Local installation'
    }
    stages{
        stage("build"){
            steps{
              sh """ 
                npm --version
              """  
            }
        }
    }
}