pipeline {
agent any
stages {
stage('gitpull') {
git "https://github.com/nazu216/stable.git"
}
stage('build') {
  steps { 
    sh "mvn clean package"
  }
}
}
}
