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
        echo "code is building"
        echo "Build number is ${currentBuild.number}"
         
            }
        }
        
    }
}
