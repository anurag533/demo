pipeline {

 
 

 
agent any

 
tools {

 
maven 'MavenDefault'

 
}

 
 

 
 

 
stages{

 
 

 
 

 
stage('Build') {

 
steps{

 
 

 
bat 'mvn package'

 
 

 
}

 
}

 
 

 
 

 
stage('SonarQube analysis') {

 
steps{

 
withSonarQubeEnv('SonarQuabedefault') { // If you have configured more than one global server connection, you can specify its name

 
 

 
bat 'mvn sonar:sonar'

 
}

 
}

 
}
