pipeline {
agent {docker(maven:3.3.9)}
node {
  git url: 'https://github.com/sameer-world/2nd-project.git'
  def mvnHome = tool 'M3'
  sh "${mvnHome} /usr/share/maven"
}
     stages  {
           stage ("compile stage"){
           steps{
                 
                 sh 'mvn clean compile'
                 
               }
               
           stage ("Testing stage"){
               
                 sh 'mvn test '
                 
               }
           
            stage ("Deployment stage"){
              
                 sh 'mvn deploy '
                 
               }
             }
          }
}
