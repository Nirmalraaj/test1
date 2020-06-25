  
node{
   stage('SCM Checkout'){
     git 'https://github.com/bhavanimahalingam/testjob'
   }
   stage('Deploy to Tomcat'){
    sshagent(['jenkins_tom']) {
    sh 'scp -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/automated_deploy/target/*.war  ec2-user@54.173.79.163:/home/ec2-user/tomcat7/webapps/'
     }
    
    }
}   
