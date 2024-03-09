pipeline {
    agent any
    stages {
//         stage('Clone repository') {
//             steps {
//                 checkout([$class: 'GitSCM', 
//                 branches: [[name: '*/main']], 
//                 userRemoteConfigs: [[url: 'https://github.com/shreyas-m-n/PES1UG21CS582_Jenkins.git']]])
//             }
//         }
        stage('Build') {
            steps {
                build 'PES1UG21CS582-1'
                sh 'g++ main/he856llo.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    post{
        failure{
            error 'Pipeline failed'
        }
    }
}
