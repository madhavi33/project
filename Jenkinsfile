@Library('my-shared-library') _

pipeline{
  
  agent any

   
  stages{
   
    stage('Git Checkout'){

       steps{
         script{

            gitCheckout(
             branch: "main",
             url: "https://github.com/madhavi33/project.git"
 
             )
         }
        }
      }


    stage('Unit Test Mvn'){
      
    // when { expression { params.action == 'create' } }

      steps{
        script{
           
             mvnTest()
         }
      }
    }
   
    stage('mvn integartion test'){
      
     // when { expression { params.action == 'create' } }
      
      steps{
        script{

            mvnIntegrationTest()

          }
        }
    }


  }
}