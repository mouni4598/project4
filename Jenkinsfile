pipeline {
    agent any


    
    environment {
        AWS_ACCESS_KEY_ID     = credentials('AWS_ACCESS_KEY_ID')
        AWS_SECRET_ACCESS_KEY = credentials('AWS_SECRET_ACCESS_KEY')
        TF_IN_AUTOMATION      = '1'
    }

    stages {
        stage('Init and Apply') {
            steps {
              
                sh 'terraform init -input=false'
                    
                sh 'terraform apply -auto-approve'
            }
        }

       
    }


}
