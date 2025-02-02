pipeline {
    agent any

    stages {
        stage('Fetch Orders') {
            steps {
                script {
                    def entrypoints = load 'scripts/entrypoints.groovy'
                    entrypoints.fetchOrders()
                }
            }
        }
        stage('Generate Postage CSV') {
            steps {
                script {
                    def entrypoints = load 'scripts/entrypoints.groovy'
                    entrypoints.generatePostageCSV()
                }
            }
        }
        stage('Create Postage') {
            steps {
                script {
                    def entrypoints = load 'scripts/entrypoints.groovy'
                    entrypoints.createPostage()
                }
            }
        }
        stage('Dispatch Orders') {
            steps {
                script {
                    def entrypoints = load 'scripts/entrypoints.groovy'
                    entrypoints.dispatchOrders()
                }
            }
        }
    }

    post {
        always {
            archiveArtifacts artifacts: 'logs/*.log', allowEmptyArchive: true
        }
    }
}