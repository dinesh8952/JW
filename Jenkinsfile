def gv
pipeline {
    agent any
    environment {
        NAME = 'NARENDRA'
    }
    parameters{
        choice(name:'chacolete',choices:['dairy milk','5star','much'],description:'')
        booleanParam(defaultValue: true, description: '', name: 'BOOLEAN')
    }

    stages {
        stage('init'){
            steps {
                script { 
                    gv = load "script.groovy"
                }
            }
            
        }
        stage('build') {
            when{
                expression {
                    params.BOOLEAN
                }
            }
            steps {
                script {
                    gv.Buildapp()
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    gv.Testapp()
                }
            }
        }
        stage('deploy') {
            steps {
                script {
                    gv.Deployapp()
                }
            }
        }
        
    }
}
