node{
    stage('vcs') {
        git 'https://github.com/wakaleo/game-of-life.git'
    }
    stage('build'){
        sh 'mvn package'
    }
    stage('post build'){
        archiveArtifacts 'gameoflife-web/target/gameoflife.war'
        junit 'gameoflife-web/target/surefire-reports/*.xml'
    }
    
}
