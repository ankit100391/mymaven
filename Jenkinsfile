pipeline {
      agent none

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
                agent{label'slave3'}
        steps{
            sh '''
            sleep 5
             echo "this is beploy stage"
             git pull https://github.com/ankit100391/pipetemp.git
             sudo kubectl apply -f pod.yml
            '''
            }
         }
          stage ('TESTING'){
                agent {label 'slave1'}
        steps{
            sh '''
            sleep 5
             echo "this is TESTING stage"
            '''
            }
         }
      }
}
