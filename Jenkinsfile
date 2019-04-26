pipeline {
    agent none 
    environment{
        PATH = "C:\\Program Files\\Git\\usr\\bin;C:\\Program Files\\Git\\bin;${env.PATH}"        
        stages {
            stage('Build') { 
                agent {
                    docker {
                        image 'python:2-alpine' 
                    }
                }
                steps {
                    sh 'python -m py_compile sources/add2vals.py sources/calc.py' 
                }
            }
        }
    }
}