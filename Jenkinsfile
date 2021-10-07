pipeline {
    agent any 
    BranchName=env.BRANCH_NAME
    stages {
        stage("build") { 
            steps {
               echo 'Building application'
               echo "Branch name is ${BranchName}"
            }
        }
        stage("test") { 
            steps {
               echo 'Testing Application'
                echo "Branch name is ${BranchName}"
            }
        }
        stage("deploy") { 
            steps {
                echo 'Deploying Application'
                echo "Branch name is ${BranchName}"
            }
        }
    }
}
