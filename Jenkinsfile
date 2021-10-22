pipeline {
    agent any 
      stages {
        stage("build") { 
            steps {
               echo 'Building yarn'
			   nodejs('NodeJS17.0.1'){
			   batch 'yarn install'
			   batch 'yarn build'
			   }
            }
        }
        stage("test") { 
            steps {
               echo 'Testing Application'
			   withGradle(){
			   batch './gradlew -v'
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
