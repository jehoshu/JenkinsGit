pipeline {
    agent any
    stages{
        stage ("cloning ..."){
            steps{
                sh 'git clone https://github.com/jehoshu/JenkinsGit.git'
                checkout checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/jehoshu/JenkinsGit']]])
            }
        } 
        stage ("building ..."){
            steps{
                echo "exec"
            }
        }       
        stage ("testing ..."){
            steps{
                echo "exec"
            }
        }       
    }
}
