pipeline {
      agent none
      environment {
  DB_URL = "35.154.149.129"
}
      stages{
        stage ('BUILD'){
              agent {label 'master'}
        steps{
            sh ''' 
            sleep 5
            echo "this is build stage"
            '''
            }
         }
          stage ('DEPLOY'){
                agent{label'maven'}
        steps{
            sh '''
            sleep 5
             echo "this is beploy stage"
            '''
            }
         }
          stage ('TESTING'){
                agent {label 'maven'}
        steps{
            sh '''
            sleep 5
             echo "this is TESTING stage"
            '''
            }
         }
      }
}
