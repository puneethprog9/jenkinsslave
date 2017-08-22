pipeline {
    agent none
    stages {
        stage('Build') {
         agent {node{label 'redhat'}}
            steps {
                checkout scm
		    
            }
        }
        stage('test') {
          agent {node{label 'test'}}
            steps {
                echo 'Testing..'
		sh 'uname -n'    
            }
        }
        stage('prod') {
        agent {node{label 'redhat'}}
            steps {
                echo 'production....'
		sh 'uname -n'
            }
        }
    }
}
