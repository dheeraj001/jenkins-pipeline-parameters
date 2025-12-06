pipeline {
    agent any
    parameters {
     string defaultValue: '0', name: 'num1'
     string defaultValue: '0', name: 'num2'
    }


    stages {
        stage('Build') {
            steps {
                echo 'Setting up Python environment...'
                // Set up Python environment (optional)
                sh 'python3 -m venv venv'
                sh '. venv/bin/activate'     
            }
        }
        stage('Deploy'){
            steps {
                echo 'Running Python Script ....'
                // Run the python script with parameter
                sh 'python3 sum.py ${params.num1} ${params.num2} '
            }
        }
    }
}
