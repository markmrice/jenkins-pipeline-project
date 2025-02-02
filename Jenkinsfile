pipeline {
    agent any

    stages {
        stage('Fetch Orders') {
            steps {
                script {
                    load 'scripts/entrypoints.groovy'
                    fetchOrders()
                }
            }
        }
        stage('Generate Postage CSV') {
            steps {
                script {
                    load 'scripts/entrypoints.groovy'
                    generatePostageCSV()
                }
            }
        }
        stage('Create Postage') {
            steps {
                script {
                    load 'scripts/entrypoints.groovy'
                    createPostage()
                }
            }
        }
        stage('Dispatch Orders') {
            steps {
                script {
                    load 'scripts/entrypoints.groovy'
                    dispatchOrders()
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