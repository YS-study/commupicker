node {
    stage ('docker build') {
        checkout scm
        sh 'docker-compose down --rmi all' 
        sh 'docker-compose up -d' 
    } 
}
