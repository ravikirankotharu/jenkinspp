node('ubuntu') {
    stage('git') {
    git 'https://github.com/wakaleo/game-of-life.git'
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
}