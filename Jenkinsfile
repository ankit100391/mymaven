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
            cd pipetemp
             sudo kubectl apply -f pod.yml
            '''
            }
         
         
         }
      }
}
