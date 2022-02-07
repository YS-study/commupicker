node {
    stage ('git clone') {
        checkout scm
        sh 'ls'
        sh 'docker --version'
    }
    stage ('docker build') {
        sh 'docker-compose down --rmi all' 
        sh 'docker-compose up -d --build' 
    } 
}
