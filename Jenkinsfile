pipeline {
    agent any 
      stages {
        stage("build") { 
            steps {
               echo 'Building application'
            }
        }
        stage("test") { 
            steps {
               echo 'Testing Application'
                java Hello
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
