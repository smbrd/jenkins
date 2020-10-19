pipeline {
  agent any
  stages {
    stage('WIP') {
      steps {
        echo "${params.TEST_SCENARIO} ${params.ORDER_IDS}"
      }
    }

  }
  parameters {
    string(name: 'ORDER_IDS', defaultValue: '', description: 'Order IDs')
    choice(name: 'TEST_SCENARIO', choices: ['run_sanity_stg.sh',
                             'run_confirmed_shipment_tracking_number_stg.sh',
                             'run_item_cancellation_stg.sh',
                             'run_item_return_stg.sh'], description: 'Test scenario')
  }
  triggers {
    cron(env.BRANCH_NAME != 'master' ? 'H * * * *' : '')
  }
}