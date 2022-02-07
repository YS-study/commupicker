node {
    stage ('git clone') {
        checkout scm
    }
    stage ('docker build') {
        sh 'docker-compose down --rmi all' 
        sh 'docker-compose up -d' 
    } 
}
