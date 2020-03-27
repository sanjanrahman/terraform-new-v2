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
     dir ('/terraform-new-v2/projects/A')
     //dir ('terraform-new-v2/projects/A') {
     sh 'terraform init'
    }
     echo "done init"
        }
     }
    }
}
