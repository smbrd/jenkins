#!/usr/bin/env groovy

parameters {
    string(name: 'Greeting', defaultValue: 'Hello', description: 'How should I greet the world?')
}
stages {
    stage('Example') {
        steps {
            echo "${params.Greeting} World!"
        }
    }
}
//
//properties {
//    [
//            pipelineTriggers([
//                    cron(env.BRANCH_NAME != 'master' ? 'H * * * *' : '')
//            ]),
//            parameters {
//                string(name: 'ORDER_IDS', defaultValue: '', description: 'Order IDs')
//                choice(name: 'TEST_SCENARIO',
//                        choices: ['run_sanity_stg.sh',
//                                  'run_confirmed_shipment_tracking_number_stg.sh',
//                                  'run_item_cancellation_stg.sh',
//                                  'run_item_return_stg.sh'],
//                        defaultValue: 'run_sanity_stg.sh',
//                        description: 'Test scenario')
//            }
//    ]
//}
//
//
//node {
//    stage('WIP') {
//        echo "${params.TEST_SCENARIO} ${params.ORDER_IDS}"
//    }
//}
