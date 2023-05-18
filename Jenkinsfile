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
                agent{label'master'}
        steps{
            sh '''
            sleep 5
             echo "this is beploy stage"
            sudo git clone git@github.com:ankit100391/pipetemp.git
            cd pipetemp
             sudo kubectl apply -f pod.yml
            '''
            }
         
         
         }
      }
}
