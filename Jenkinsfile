
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

stage('Docker login to Docker hub'){
sh "docker login -u 'mmureithi' -p 'Mureithi5' "
}
stage('Tag image'){
sh "docker tag maureen:latest mmureithi/maureenexam:latest"
}
stage('Push image'){
sh "docker push mmureithi/test:latest"
}

stage('Apply changes to the environment') {
sh "ls -l"
}


}

