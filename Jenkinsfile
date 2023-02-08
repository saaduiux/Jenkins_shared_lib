pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
              sh """
              ls -lha /usr/bin/
              python --version
              python3 -m venv changelog-jenkins
              . ./changelog-jenkins/bin/activate
              pip3 install -r requirements.txt
              python3 gitlog.py
              """
            }
        }
    }
}
