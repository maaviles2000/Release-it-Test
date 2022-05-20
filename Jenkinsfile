def targetBranch = ghprbTargetBranch;
def packageJSONVersion = readJSON(file: 'package.json').version;
pipeline {
    agent {
        docker { image 'node:14' }
    }
    stages{
        stage('DEVELOP') {
            when {
                expression {
                    return targetBranch == 'develop';
                }
            }
            steps {
                echo "DEVELOP :)"
                sh "npm run release -- minor --ci"
                echo "${packageJSONVersion}"
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
                sh "npm run release -- major --ci"
                echo "${packageJSONVersion}"
            }
        }
    }
}
