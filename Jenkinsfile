  
node{
   stage('SCM Checkout'){
     git 'https://github.com/bhavanimahalingam/testjob'
   }
   stage('Deploy to Tomcat'){
    sshagent(['jenkins_tom']) {
    sh 'scp -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/automated_deploy/target/*.war  ec2-user@34.202.233.126:/home/ec2-user/apache-tomcat-7.0.104/webapps/'
     }
    
    }
}   
