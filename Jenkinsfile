pipeline{
    agent any
    
    stages{
        stage("Checkout the code"){
            steps{
                bat "actions/checkout@v4"
            }
        }
        stage("Setup .NET 8.0"){
            steps{
                bat "actions/setup-dotnet@v4"
            }
        }
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