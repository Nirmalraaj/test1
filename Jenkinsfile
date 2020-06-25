  
node{
   stage('SCM Checkout'){
     git 'https://github.com/bhavanimahalingam/testjob'
   }
   stage('Deploy to Tomcat'){
    sshagent(['jenkins_tom']) {
    sh 'scp -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/automated_deploy/target/*.war  ec2-user@3.88.59.170:/home/ec2-user/tomcat7/webapps/'
     }
    
    }
}   
