pipeline {
 agent {label'master'}
 stages{stage('checkout'){
  steps{
   script{
    echo"TARGET_ENVIRONMENT: ${params.TARGET_ENVIRONMENT}"
    git(branch: 'master',credentialsId: '6b4562bd-e947-4f59-ab5e-4b3f96d1f519',url: 'https://github.com/sanjanrahman/terraform-new-v2',changelog: true)
    }
  }
}
 stage('build') {
  steps {
    echo "...Building. terraform"
     sh 'cd $WORKSPACE'
      //sh 'cd 
     //sh 'sudo chmod 755 terraform-new-v'
     //sh 'sudo chmod 755 projects'
     dir ('sudo /projects/A') {
         sh 'sudo terraform init'}
     sh 'sudo terraform plan -out testmy_plan'
     echo "=========================================================================="
      
     //sh 'chmod 700 *.tf'
     sh 'pwd'
     //dir ('terraform-new-v2/projects/A') {
     //sh 'cd /var/lib/jenkins/workspace/terraform-new-v2/projects/A/'
     //sh 'sudo terraform init
     //sh 'sudo terraform plan'
    }
        }
     }
}
