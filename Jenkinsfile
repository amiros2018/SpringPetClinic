pipeline{
    agent{label 'main'}
    tools{maven 'M3'}
    stages{
        stage('Checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/amiros2018/SpringPetClinic.git'
            }
        }
        stage('Build'){
            steps{
                sh 'mvn compile'
            }
        }
        stage('Test'){
            steps{
                sh 'mvn test'
            }
        }
        stage('Package'){
            steps{
                sh 'mvn package'
            }
        }
        stage('Deployment'){
            steps{
                sh 'java -jar /var/lib/jenkins/workspace/PetClinicDeclarativepipeline/target/*.jar'
            }
        }
    }
}
