pipeline {
    agent any
    stages{
        stage('Branch name') {
            when {
                expression {
                    return CHANGE_TARGET == 'develop';
                }
            }
            steps {
                echo "DEVELOP :)"
            }
        }
        stage('Branch name') {
            when {
                expression {
                    return CHANGE_TARGET == 'main';
                }
            }
            steps {
                echo "MAIN"
            }
        }
    }
}
