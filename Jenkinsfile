pipeline {
    agent any
    stages {
        stage('Restore') {
            steps {
                sh '/opt/homebrew/bin/dotnet restore HouseRentingSystem.sln'
            }
        }
        stage('Build') {
            steps {
                sh '/opt/homebrew/bin/dotnet build HouseRentingSystem.sln --configuration Release'
            }
        }
        stage('Test') {
            steps {
                sh '/opt/homebrew/bin/dotnet test HouseRentingSystem.Tests/HouseRentingSystem.Tests.csproj'
            }
        }
    }
}