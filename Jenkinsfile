pipeline{
    agent any
    triggers{
        pollSCM('* * * * *')
    }
    stages{
        stage('SMC'){
            steps{
                git url: 'https://github.com/devops-pr-ctice/spring-petclinic.git',
                branch: 'main'
            }
        }
        stage('build'){
            steps{
                echo 'sh build code'
                echo 'sh static code analysis'
                echo 'archive package into jfrog'
                ech 'sh quality gate'
            }
        }
        stage('deploy'){
            steps{
                echo 'sh using terraform create env'
                echo 'sh using kubectl to deploy'
                echo 'sh run end to end system tests'
            }
        }
        stage('test'){
            steps{
                echo 'run end to end system tests'
                echo 'sh display test results'
            }
        }
    }
}