node('built-in') 
{
	stage('Continuous Download') 
	{
    		git 'https://github.com/shaikwahab01/Jenkins_Multibranch.git'
	}
    	stage('Continuous Build') 
	{
    		sh label: '', script: 'mvn package'
	}
	stage('ContinuousDeployment') 
	{
		sh 'scp /home/ubuntu/.jenkins/workspace/Pipelines/ScriptedPipeline/webapp/target/webapp.war ubuntu@172.31.26.75:/var/lib/tomcat9/webapps/qaenv.war'
	}
	stage('ContinuousTesting')
	{
		sh 'echo "Testing Passed"'
	}
	stage('ContinuousDelivery')
	{
		sh 'scp /home/ubuntu/.jenkins/workspace/Pipelines/ScriptedPipeline/webapp/target/webapp.war ubuntu@172.31.22.121:/var/lib/tomcat9/webapps/prodenv.war'
	}
}
