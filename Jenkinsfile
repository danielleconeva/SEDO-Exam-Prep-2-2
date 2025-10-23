pipeline{
    agent any

    stages{
        stage('Restore .NET dependencies'){
            steps{
                sh 'dotnet restore'
            }
        }

        stage('Build .NET project'){
            steps{
                sh 'dotnet build --no-restore'
            }
        }

        stage('Run Unit and Integration tests'){
            steps{
                sh 'dotnet test --no-build --verbosity normal'
            }
        } 
    }
}