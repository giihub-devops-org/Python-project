pipeline{
    agent any
    stages
    {
        stage("SCM Checkout")
        {
            steps
            {
                git branch: 'main', url: 'https://github.com/giihub-devops-org/Python-project.git'
            }
        }
        stage("Execute Build")
        {
            steps
            {
            withMaven(globalMavenSettingsConfig: '0c14f41b-b79f-4c1b-8225-4be63d44fc5f', jdk: 'Local_jdk', maven: 'Local_mvn', mavenSettingsConfig: 'cc9697ed-e30f-494d-856d-45f5b31b8bd3', traceability: true)
            {
                sh "mvn package"
            }

            }
        }
