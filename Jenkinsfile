node {
    stage('git') {
    git 'https://github.com/ravikirankotharu/jenkinspp.git'
    }
    stage('maven') {
    sh label: '', script: 'mvn package'
