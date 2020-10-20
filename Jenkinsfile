pipeline {
agent any
tools "jdk" "mvn"
stages {
stage('gitpull') {
  steps {
git "https://github.com/nazu216/stable.git"
}
}
stage('build') {
  steps { 
    sh "mvn clean package"
  }
}
}
}
