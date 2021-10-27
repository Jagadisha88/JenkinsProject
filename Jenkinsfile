pipeline {
    agent any 
      stages {
        stage("build") { 
            steps {
               echo 'Building application'
			   javac *.java
			   sleep 5
            }
        }
        stage("test") { 
            steps {
               echo 'Testing Application'
			   java Hello
			   sleep 5
			   java Demo
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
