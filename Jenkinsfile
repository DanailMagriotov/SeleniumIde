pipeline{
    agent any
    stages{
        stage("Checkout the code"){
            bat "actions/checkout@v4"
        }
        stage("Setup .NET 8.0"){
            bat "actions/setup-dotnet@v4"
        }
        stage("Restore dependencies"){
            bat "dotnet restore"
        }
        stage("Build the app"){
            bat "dotnet build --no-restore"
        }
        stage("Run UI tests"){
            bat "dotnet test --no-build --no-restore"
        }
    }
}