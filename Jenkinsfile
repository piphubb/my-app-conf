pipeline {
    agent any

    stages {
        stage('Run Script') {
            steps {
               sh """
                    sed -i 's+piphubb/reactjs-argo:.*+piphubb/reactjs-argo:${params.VERSION}+g' deploy/reatjs-argo.yaml
                    git config user.name 'piphubb'
                    git config user.email 'piphub.p16@gmail.com'
                    git add .
                    git commit -m 'change file ${params.VERSION}'
                    git push https://piphubb:glpat-AZgb8N_DnCqKLeJvqY1a@gitlab.com/piphubb/my-app-conf.git HEAD:main
               """
            }
        }
    }
}
