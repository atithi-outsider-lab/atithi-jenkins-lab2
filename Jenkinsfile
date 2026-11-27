pipeline {
  agent any
  options { timeout(time: 10, unit: 'MINUTES') }
  stages {
    stage('Test') {
      steps {
        sh 'echo "MARKER: this is the BASE (main) Jenkinsfile"'
        sh 'python3 -m venv .venv && . .venv/bin/activate && pip install -q -r requirements.txt && pytest -q'
      }
    }
  }
}
