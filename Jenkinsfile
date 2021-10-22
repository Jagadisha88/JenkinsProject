pipeline {
    agent any 
      stages {
        stage("build") { 
            steps {
               echo 'Building yarn'
		nodejs('NodeJS') {
			   sh 'yarn install'
			   }
            }
        }
        stage("test") { 
            steps {
               echo 'Testing Application'
			   withGradle(){
			   sh './gradlew -v'
			   }
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
