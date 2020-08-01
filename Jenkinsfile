node {
    def mvnHome
    stage('Checkout') {
        git 'https://github.com/nayaralopes/lab-bootcamp-devops.git'
    }
    stage('Docker Build') {
        sh 'sudo docker build -t myapp .'
    }
    stage('Stop App') {
        sh label: '', script: 'sudo docker run hello-world; sudo docker stop $(sudo docker ps -a -q); sudo docker container prune -f'
    }
    stage('Deploy') {
        sh 'sudo docker run --name website -p 8082:80 -d myapp'
    }
}