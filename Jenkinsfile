pipeline{
    agent any
    stages{
        stage('PULL'){
            steps{
                //pulling github repo 
                git branch: 'main', url: 'https://github.com/Unnati18-uk/jenkins-terra.git'
                echo 'pull success'
            }
        }
        stage('INITIALIZE TERRAFORM'){
            steps{
                //it will initialize terraform
                sh 'terraform init'
                echo 'initializing terraform is success'
            }
        }
        stage('PLAN TERRAFORM'){
            steps{
                //it will show an overview that terraform does after running terraform apply
                sh 'terraform plan'
                echo 'plan success'
            }
        }
        stage('EXECUTE TERRAFORM'){
            steps{
                //it will execute all configuration
                sh 'terraform apply --auto-approve'
                echo 'apply successful'
            }
        }
    }
}
