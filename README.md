# Project Overview

This Jenkins Pipeline Project automates the process of handling eBay orders, including fetching orders, generating postage CSV files, creating postage labels, and dispatching orders. The project is structured to facilitate easy integration with Jenkins and includes logging for tracking the execution of each step.

## Project Structure

```
jenkins-pipeline-project
├── scripts
│   ├── fetch_orders.groovy
│   ├── generate_postage_csv.groovy
│   ├── create_postage.groovy
│   └── dispatch_orders.groovy
├── Jenkinsfile
├── pom.xml
└── README.md
```

### Scripts

- **fetch_orders.groovy**: Placeholder script for fetching all undispatched eBay orders. Logs its steps in Jenkins and saves the logs as artifacts.

- **generate_postage_csv.groovy**: Placeholder script for generating a CSV file from the fetched orders. Logs its steps in Jenkins and saves the logs as artifacts.

- **create_postage.groovy**: Placeholder script for creating postage labels and saving the tracking numbers in a CSV format. Logs its steps in Jenkins and saves the logs as artifacts.

- **dispatch_orders.groovy**: Placeholder script for the final step of dispatching the orders. Logs its steps in Jenkins and saves the logs as artifacts.

### Jenkinsfile

The `Jenkinsfile` defines the Jenkins pipeline, including stages for executing the Groovy scripts, logging the steps, and archiving the logs as artifacts.

### pom.xml

The `pom.xml` file is the Maven configuration file that specifies the project dependencies, build settings, and plugins required for building and testing the project with Spock.

## Setup Instructions

1. Clone the repository to your local machine.
2. Ensure you have Jenkins installed and configured.
3. Create a new Jenkins pipeline project and point it to the cloned repository.
4. Configure the necessary credentials for accessing eBay and Royal Mail APIs.
5. Run the pipeline to automate the order processing.

## Functionality Overview

This pipeline automates the following processes:
- Fetching undispatched eBay orders.
- Generating a CSV file for postage.
- Creating postage labels and tracking numbers.
- Dispatching orders and logging each step for traceability.

For further details on each script, please refer to the respective Groovy files in the `scripts` directory.