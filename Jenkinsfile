pipeline
{
    agent
    {
        label 'linux_node'
    }
    tools
    {
        maven 'mymaven'
    }
    stages
    {
        stage('clone repo')
        {
            steps
            {
                git 'https://github.com/Bhupi-Test/simple-java-maven-app.git'
            }
        }
        stage('compile code')
        {
            steps
            {
                sh 'mvn compile'
            }
        }
        stage('code review')
        {
            steps
            {
                sh 'mvn pmd:pmd'
            }
        }
    }
}
