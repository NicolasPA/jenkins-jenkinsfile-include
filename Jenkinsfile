#!groovy

pipeline {
    stage('Shared') {
        steps(
            echo 'Shared stage'

            checkout scm
        )
    }
    stage('Run specific job') {
        steps {
            script{
                if (env.JOB_NAME == 'Project 1') {
                    load 'Project1/Jenkinsfile'
                } else if (env.JOB_NAME == 'Project 2') {
                    load 'Project2/Jenkinsfile'
                }
            }
        }
}
