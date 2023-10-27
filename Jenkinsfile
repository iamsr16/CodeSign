pipeline {
    agent any
    
    environment {
        dotnet = 'C:/Program Files/dotnet/dotnet.exe'
         }
  stages{
        
      stage('checkout') {
           steps {
             git branch: 'master',url:'https://github.com/iamsr16/CodeSign.git'
             
          }
        }
      stage('Restore packages'){
            steps { 
                bat "dotnet restore "
               }
            }
            
     stage('Clean'){
           steps {
                  bat "dotnet clean"
                }
           }
   
   stage('Build'){
        steps{
          bat "dotnet build --configuration Release"
         }
     } 
 stage('Publish'){
     steps{
       bat "dotnet publish "
     }
   }
  }
}
