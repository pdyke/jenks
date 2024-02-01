pipeline{
    agent any
    stages{
        stage("Test"){
            steps{
                sh """
                        echo "Welcome to Jenkins Ebuka"
                   """
            }
        }
    
        stage("Deploy"){
            steps{
                sh """
                        echo "Welcome to the Deployment. Added Jenkins"
                        ssh -o StrictHostKeyChecking=no -T -i /var/lib/jenkins/tester2.pem ubuntu@ec2-54-242-151-111.compute-1.amazonaws.com
                        sudo apt update -y
                        cd /var/www
                        sudo rm -rf html
                        git clone https://github.com/monyslim/jenk.git html
                   """
            }
        }
    
    }
}