pipeline {
    agent any
    environment {
        NAME = 'NARENDRA'
    }
    parameters{
        choice(name:'chacolete',choices:['dairy milk','5star','much'],description:'')
        booleanParam(defaultValue: true, description: '', name: 'BOOLEAN')
    }
    stages{
        stage('build') {
            when{
                expression {
                    params.BOOLEAN
                }
            }
            steps {
                script {
                    echo "i am $NAME and i am building the the application"
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    echo "i am $NAME testing the applicattion"
                }
            }
        }
        stage('deploy') {
            steps {
                script {
                    echo "i want this ${params.chacolete} chocolete"
                }
            }
        }
        
    }
}
