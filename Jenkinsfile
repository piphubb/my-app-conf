pipeline {
    agent any

    stages {
        stage('Run Script') {
            steps {
               sh """
                    sed -i 's+piphubb/reactjs-argo:.*+piphubb/reactjs-argo:${params.VERSION}+g' deploy/reactjs-argo.yaml
                    git config user.name 'piphubb'
                    git config user.email 'piphub.p16@gmail.com'
                    git add .
                    git commit -m 'change the file ${params.VERSION}'
                    git push https://piphubb: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@github.com/piphubb/my-app-conf.git HEAD:main
               """
            }
        }
    }
}
