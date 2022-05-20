pipeline {
    agent any
    stages{
        stage('DEVELOP') {
            when {
                expression {
                    return CHANGE_TARGET == 'develop';
                }
            }
            steps {
                echo "DEVELOP :)"
            }
        }
        stage('MAIN') {
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
