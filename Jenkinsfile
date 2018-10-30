pipeline {
    agent any
    tools { 
        maven 'local_maven' 
        jdk 'local_java' 
    }
    stages {
        stage ('Initialize') {
            steps {
                bat '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                ''' 
            }
        }

        stage ('Git Checkout') {
            steps {
                git 'https://github.com/bananaman47/gbs-materialbatch-edh-sub-exp-api.git'
            }
        }
		stage ('compile-package')
		{
		bat mvn package
		}
    }
}
