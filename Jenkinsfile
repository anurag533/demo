pipeline {

 
 

 
agent any

 
tools {

 
maven 'maven'

 
}

 
 

 
 

 
stages{

 
 

 
 

 
stage('Build') {

 
steps{

 
 

 
bat 'mvn package'

 
 

 
}

 
}

 
 

 
 

 
stage('SonarQube analysis') {

 
steps{

 
withSonarQubeEnv('sonarqube') { // If you have configured more than one global server connection, you can specify its name

 
 

 
bat 'mvn sonar:sonar'

 
}

 
}

 
}

 
}

 
 

 
}
