pipeline {
    agent {
        label 'linux'
    }
    stages {
        stage('install molecule') {
            steps { 
               sh 'pip install molecule'
            }
        }
        stage ('clone project'){
            steps {
                sh 'git clone https://github.com/p1ckle-r1ck/ci-cd_4'
            }
        }
            
        stage ('molecule test') { 
            steps { 
                sh 'cd ci-cd_4/infrastructure && molecule test'
            }
        }
    }
}