#!/usr/bin/env groovy

//parameters {
//    string(name: 'Greeting', defaultValue: 'Hello', description: 'How should I greet the world?')
//}
//stages {
//    stage('Example') {
//        steps {
//            echo "${params.Greeting} World!"
//        }
//    }
//}

properties([
    pipelineTriggers([
        cron(env.BRANCH_NAME != 'master' ? 'H * * * *': '')
    ]),

])
parameters {
    string(name: 'Greeting', defaultValue: 'Hello', description: 'How should I greet the world?')
}

node {
    stage('Example') {
        steps {
            echo "${params.Greeting} World!"
        }
    }
}
