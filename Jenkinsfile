pipeline {
    agent any
    parameters{
        string (name: 'node-repo', defaultValue : 'https://github.com/contentful/the-example-app.nodejs.git', description: '')

    }
    stages{
        stage ("cloning") {
            steps{
                echo "clonage"
               sh "git clone ${node-repo}"
            }
        }
        stage ("Install dependenciess"){
            steps{
                echo "installation des dependences"
                sh "cd the-example-app.nodejs && npm install "
            }
        }
        stage ("Deploy"){
            steps{
                echo "start project"
                sh "cd the-example-app.nodejs && npm start"
            }
        }

    }
}
