node{
   stage('SCM checkout')
    {
      
    git 'https://github.com/mahijagdale/hello-world.git'
     }
     
     stage ('compile package')
     {
        def mvnhome = tool name: 'Maven', type: 'maven'
        sh "${mvnhome}/bin/mvn package"      }
   
   stage ('Deploy to tomcat'){
      sshagent(['tomcat-dev']) {
          sh'scp -o StrictHostKeyChecking=no target/*.war ec2-user@172.31.37.0:/opt/apache-tomcat-8.5.50/webapps/'
         }
   }
      
   }
