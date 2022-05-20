def targetBranch = ghprbTargetBranch;
pipeline {
    agent any
    stages{
        stage('DEVELOP') {
            when {
                expression {
                    return targetBranch == 'develop';
                }
            }
            steps {
                echo "DEVELOP :)"
            }
        }
        stage('MAIN') {
            when {
                expression {
                    return targetBranch == 'main';
                }
            }
            steps {
                echo "MAIN"
            }
        }
    }
}
