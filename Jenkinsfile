node {
    stage ('docker build') {
        checkout scm
        sh 'docker-compose down --rmi all' 
        sh 'docker-compose up -d' 
        sh 'docker rmi $(docker images -f "dangling=true" -q)'
    } 
}
