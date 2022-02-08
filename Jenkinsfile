node {
    stage ('git clone') {
        checkout scm
    }
    stage ('docker build') {
        sh 'docker-compose down --rmi all' 
        sh 'docker-compose up -d --build' 
        sh 'docker rmi $(docker images -f "dangling=true" -q)'
    } 
}
