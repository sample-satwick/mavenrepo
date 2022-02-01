pipeline{
agent any
triggers{
	pollSCM('* * * * *')
}
stages{
stage('SCM'){
steps{
checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: '869d3c6d-f7e9-4191-b36d-c7a701363394', url: 'https://github.com/sample-satwick/mavenrepo.git']]])

}
}

stage('build'){
steps{
sh 'mvn package'
}
}


}
}
