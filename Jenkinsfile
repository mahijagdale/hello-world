node{
   stage('SCM checkout')
    {
      
    git 'https://github.com/mahijagdale/hello-world.git'
     }
     
     stage ('compile package')
     {
        def mvnhome = tool name: 'Maven', type: 'maven'
        sh "${mvnhome}/bin/mvn package"      }
      
   }
