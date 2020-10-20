pipeline {
    agent any
     
    stages{
        stage('git') {
            steps {
             git "https://github.com/nazu216/stable.git"  
            }
        }
        stage ('build') {
            steps {
                
        sh "mvn clean install"
        echo "code is building"
        echo "Build number is ${currentBuild.number}"
         
            }
        }
        stage('Build') {
            steps {
                script {
                   VERSION_NUMBER = VersionNumber(versionNumberString: '1.2.1.${BUILDS_ALL_TIME}')
                   currentBuild.displayName = "${VERSION_NUMBER}"
                   sh "mvn -Dversion=${VERSION_NUMBER} build"
                }
            }
        }
        
    }
}
