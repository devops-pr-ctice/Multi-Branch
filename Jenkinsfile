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
                echo 'sh quality gate'
            }
        }
        stage('deploy-prod'){
            steps{
                echo 'sh deploy into production'
            }
        }
    }
}