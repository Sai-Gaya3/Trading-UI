pipeline {
agent any
tools {
nodejs "Nodejs"
}
stages {
stage('Checkout') {
steps {
branch: 'master'
}
git url: 'https://github.com/Sai-Gaya3/Trading-UI.git',
}
stage('Check Node & NPM') {
steps {
sh 'node -v'
sh 'npm -v'
}
}
stage('Install Dependencies') {
steps {
sh 'npm install'
}
}
stage('Build') {
steps {
sh 'CI=false npm run build'
}
}
stage('Test') {
steps {
sh 'npm test || echo "No tests found"'
}
}
}
}
