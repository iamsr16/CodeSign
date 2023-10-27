pipeline {
    agent any
    
    environment {
        dotnet ='C:/Program Files/dotnet/dotnet.exe'
        }
  stages{
        
      stage('checkout') {
           steps {
             git branch: 'ccwu-at-pivotal-patch-1',url:'https://github.com/iamsr16/CodeSign.git'
             
          }
        }
      stage('Restore packages'){
            steps { 
                bat "dotnet restore /CodeSign"
               }
            }
            
     stage('Clean'){
           steps {
                  bat "dotnet clean /CodeSign"
                }
           }
   
   stage('Build'){
        steps{
          bat "dotnet build /CodeSign --configuration Release"
         }
     } 
 stage('Publish'){
     steps{
       bat "dotnet publish /CodeSign "
     }
   }
  }
}
