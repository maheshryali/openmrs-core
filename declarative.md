pipeline {
    agent any {
        stages{
            stage('openmrs') {
                step {
                    git branch: 'master'
                    url: 'https://github.com/maheshryali/openmrs-core.git'
                    sh 'mvn package'
                }
            }
        }
    }
}