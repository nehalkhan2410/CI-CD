# Jenkins Pipeline

## 1. Checkout from GitHub 

The below code snippet gives an idea on how to Checkout Code from GitHub.


```groovy

    checkout([
        $class: 'GitSCM', 
        branches: [[name: 'branch_name']], 
        doGenerateSubmoduleConfigurations: false, 
        extensions: [], submoduleCfg: [], 
        userRemoteConfigs: [
            [credentialsId: 'jenkins_credential_id', url: 'git_url']
        ]
    ])

```

`GitSCM` is the class to be used for Checkout.

`branch_name` is the name of the branch to be checkout out.

`jenkins_credential_id` is the ID of the credential that is configured in Jenkins.

`git_url` is the URL for the git repository.

