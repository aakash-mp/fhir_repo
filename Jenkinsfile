pipeline
{
agent any
stages{
stage('Build Application'){
steps{
bat 'mvn clean install'
}
}

stage('SonarQube Testing'){
steps{
bat 'mvn sonar:sonar -Dsonar.sources=src/ -Dsonar.host.url=http://localhost:9000 -Dsonar.login=8901658402554b97ff907da1015477bb36e60baf'
}
}



stage('Deploy Application to Mulesoft Cloudhub'){
steps{
bat 'mvn package deploy -DmuleDeploy'
}
}
}
}