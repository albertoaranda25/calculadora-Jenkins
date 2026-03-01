pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                // Creamos el entorno virtual
                sh 'python3 -m venv venv'
                // Activamos e instalamos en la misma ejecución
                sh '. venv/bin/activate && pip install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                // Activamos y probamos en la misma ejecución
                sh '. venv/bin/activate && python3 -m pytest'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Despliegue simulado exitoso"'
            }
        }
    }
}
