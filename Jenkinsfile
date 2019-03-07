node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}
node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image'){

sh "docker build -t maureen:latest ."
}

stage('Docker login to hub and push the image'){
sh "docker login -u 'mmureithi' -p 'Mureithi5' "
}
stage('1'){
sh "docker tag maureen:latest mmureithi/maureenexam:latest"
}
stage('2'){
sh "docker push mmureithi/test:latest"
}

stage('Apply changes to the environment') {
sh "ls -l"
}


}

