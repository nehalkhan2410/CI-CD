# Jenkins Pipeline

## 1. Checkout from GitHub 

The Checkout step has a large variety of Software Configuration Managements (SCMs) available.

All the options and parameters in the checkout step vary depending on the chosen SCM.

<span style="color:orange">*Code Snippet to Checkout Code from **GitHub** and use it as part of a pipeline.*</span>


```groovy

    checkout([
        $class: 'GitSCM or <scm_name>', 
        branches: [[name: '<branch_name>']], 
        doGenerateSubmoduleConfigurations: false, 
        extensions: [], submoduleCfg: [], 
        userRemoteConfigs: [
            [credentialsId: '<jenkins_credential_id>', url: '<git_url>']
        ]
    ])

```

### Brief explanation of the options and parameters used.

### *Predefined paramters used above*

`$class` option is used to provide name of a specific SCM you can want to use in the whole checkout step. Since, we are using Git as version control system we pass `GitSCM` as parameter, more details on all available SCMs [here](https://jenkins.io/doc/pipeline/steps/workflow-scm-step/)

**All the below paramters are related to `GitSCM` and will vary depending upon the SCM we choose.**

`branches: array` accepts one paramter as follows:

- `name: string` name of the specific branch to be used.

- All branches if **no parameter** is passed.

`doGenerateSubmoduleConfigurations: boolean`

`extensions: array` here we pass **no parameter** but we can pass various extensions that are available for `GitSCM` 

`submoduleCfg: array` here we pass **no parameter** but accepts two parameters as follows:

- `submoduleName: string`

- `branches: array`

`userRemoteConfigs: array` Specify the repository to track. This can be a URL or a local file path. Accepts four paramters as follows:

- `credentialsId: string` takes ID of the credential that is configured in Jenkins as paramter. 

- `url: string` takes url to the git reposirtory.

- `name: string` takes ID of the repository, such as origin, to uniquely identify this repository among other remote repositories.

- `refspec: string` takes refspec controls the remote refs to be retrieved and how they map to local refs.

### *User provided parameters used above*

`scm_name:`*string* takes name of SCM to be used here we used **`GitSCM`** as SCM.

`branch_name:`*string* takes name of the branch to be used.

`jenkins_credential_id:`*string* takes ID of the credentials that are setup as part of Jenkins Configurations. The Jenkins Credentials Setup can be refered [here](./markdowns/JenkinsCredentials.md). 

`git_url:`*string* takes url of the git repository to be used. 

