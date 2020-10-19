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

properties[
        pipelineTriggers([
                cron(env.BRANCH_NAME != 'master' ? 'H * * * *' : '')
        ]),
        parameters {
            string(name: 'Order IDs', defaultValue: '', description: '')
            choice(name: 'Test scenario',
                    choices: ['run_sanity_stg.sh',
                              'run_confirmed_shipment_tracking_number_stg.sh',
                              'run_item_cancellation_stg.sh',
                              'run_item_return_stg.sh'],
                    defaultValue: 'run_sanity_stg.sh',
                    description: '')
        }
]


node {
    stage('WIP') {
        echo "${params.Greeting} World!"
    }
}
