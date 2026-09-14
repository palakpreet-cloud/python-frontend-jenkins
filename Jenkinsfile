pipeline{
    agent any
    tools{
        nodejs 'mynode'
    }
    stages{
        stage('git'){
            steps{
                git url: 'https://github.com/palakpreet-cloud/python-frontend-jenkins.git', branch: 'main', credentialsId: 'pythonfrontendjenkinsfile'
            }
        }
        stage('install'){
            steps{
                sh 'npm i'
            }
        }
        stage('build'){
            steps{
                sh 'npm run build'
            }
        }
        stage('start'){
            steps{
                sh 'npm run dev'
            }
        }
    }
}
