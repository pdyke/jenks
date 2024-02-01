pipeline{
    agent any
    stages{
        stage("Test"){
            steps{
                sh """
                        echo "Welcome to Jenkins Seun"
                   """
            }
        }
    
        stage("Deploy"){
            steps{
                sh """
                        echo "Welcome to the Deployment. Added Jenkins"
                        ssh -o StrictHostKeyChecking=no -T -i /var/lib/jenkins/all_computers.pem ec2-16-171-162-26.eu-north-1.compute.amazonaws.com
                        sudo apt update -y
                        cd /var/www
                        sudo rm -rf html
                        git clone https://github.com/pdyke/jenks.git html
                   """
            }
        }
    
    }
}