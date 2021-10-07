pipeline {
    agent any 
    parameters{
        choice(name: 'VERSION', choices: ['1.1.0', '1.2.0'], description: '')
        booleanParam(name: 'executeTests', defaultValue: true, description: '')
    }
    stages {
        stage("build") { 
            steps {
               echo 'Building application'
            }
        }
        stage("test") { 
            when{
                expression{
                    parameters.executeTests
                }
            }
            steps {
               echo 'Testing Application'
            }
        }
        stage("deploy") { 
            steps {
                echo 'Deploying Application'
                echo "Deploying version ${params.VERSION}"
            }
        }
    }
}
