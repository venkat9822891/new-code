node 
{
    stage('Continuous Download') 
	{
    git 'https://github.com/venkat9822891/new-code.git'
	}
    stage('Continuous Build') 
	{
    sh 'mvn package'
	}
    stage('Continuous Deployment')
        {
    sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/Multi-Branch-Job_dev/webapp/target/webapp.war   ubuntu@172.31.42.115:/var/lib/tomcat8/webapps/devenv.war'
        }
	
   
}
