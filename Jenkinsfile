pipeline {
agent any
tools {
        maven 'mvn'
        jdk 'jdk'
    }
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
