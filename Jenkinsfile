// Jenkinsfile (Declarative Pipeline)
pipeline {
    // 1. runs in any agent, otherwise specify a slave node
    agent any
    parameters {
    // 2.variables for the parametrized execution of the test: Text and options
        choice(choices: 'yes\nno', description: 'Are you sure you want to execute this test?', name: 'run_test_only')
        choice(choices: 'yes\nno', description: 'Archived war?', name: 'archive_war')
        string(defaultValue: "your.email@gmail.com", description: 'email for notifications', name: 'notification_email')
    }
    //3. Environment variablesÎ
    environment {
        firstEnvVar= 'FIRST_VAR'
        secondEnvVar= 'SECOND_VAR'
        thirdEnvVar= 'THIRD_VAR'
    }
    //4. Stages
    stages {
        stage('SVN') {
            steps {
                echo 'Check out ..'
                checkout([
                    $class: 'SubversionSCM', 
                    additionalCredentials: [], 
                    excludedCommitMessages: '', 
                    excludedRegions: '', 
                    excludedRevprop: '', 
                    excludedUsers: '', 
                    filterChangelog: false, 
                    ignoreDirPropChanges: false, 
                    includedRegions: '', 
                    locations: [[
                        cancelProcessOnExternalsFail: true, 
                        credentialsId: '608ff627-0cc7-4cf0-9db4-83ab4521d410', 
                        depthOption: 'infinity', 
                        ignoreExternalsOption: false, 
                        local: 'trunk_android', 
                        remote: 'http://192.168.50.86/svn/slg/xfiles/trunk/client/project/Shell']], 
                    quietOperation: true, 
                    workspaceUpdater: [$class: 'UpdateUpdater']])
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }

            
        }
    }
}