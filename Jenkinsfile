pipeline{
    agent any
    stages{
        stage('Verify Tooling'){
            steps{
                sh '''
                    docker version
                    docker info
                    docker compose version
                    curl --version
                '''
            }
        }
        stage('Start Container'){
            steps{
                sh "docker -H ssh://devops@44.202.101.86 run hello-world"
//                 sh "docker -H ssh://devops@44.202.101.86 compose up -d"
//                 sh 'docker -H ssh://devops@44.202.101.86 compose ps'
            }
        }
    }
}
