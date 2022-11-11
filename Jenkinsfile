pipeline {
    agent any
    stages{
        stage ("cloning ..."){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/jehoshu/JenkinsGit']]])
            }
        } 
        stage ("building ..."){
            steps{
                sh 'python http_e.py'
            }
        }       
        stage ("testing ..."){
            steps{
                sh 'pytest TestRest.py'
            }
        }       
    }
}
