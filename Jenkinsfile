// Jenkinsfile (Declarative Pipeline)
pipeline {
    agent any

    stages {
        stage('SVN') {
            steps {
                echo 'Check out ..'
                checkout([$class: 'SubversionSCM', additionalCredentials: [], excludedCommitMessages: '', excludedRegions: '', excludedRevprop: '', excludedUsers: '', filterChangelog: false, ignoreDirPropChanges: false, includedRegions: '', locations: [[cancelProcessOnExternalsFail: true, credentialsId: '608ff627-0cc7-4cf0-9db4-83ab4521d410', depthOption: 'infinity', ignoreExternalsOption: false, local: 'trunk_android', remote: 'http://192.168.50.86/svn/slg/xfiles/trunk/client/project/Shell']], quietOperation: true, workspaceUpdater: [$class: 'UpdateUpdater']])
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