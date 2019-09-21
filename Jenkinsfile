node('ansible') {
    stage('git') {
    git 'https://github.com/ravikirankotharu/jenkinspp.git'
    }
    stage('maven') {
    sh label: '', script: 'mvn package'
    }
    stage('artifacts') {
    archiveArtifacts 'gameoflife-web/target/*.war'
    }
    stage('junitresults'){
    junit 'gameoflife-web/target/surefire-reports/*.xml'
    }
    stage('ansible deployment') {
    sh label: '', script: 'ansible-playbook gof.yml'
    }
}