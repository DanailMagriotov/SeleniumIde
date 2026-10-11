pipeline{
    agent any

    stages{
        stage("Restore dependencies"){
            steps{
                bat "dotnet restore"
            }  
        }
        stage("Build the app"){
            steps{
                bat "dotnet build --no-restore"
            }
        }
        stage("Run UI tests"){
            steps{
                bat "dotnet test --no-build --no-restore"
            }
        }
    }
}