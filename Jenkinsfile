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
}
