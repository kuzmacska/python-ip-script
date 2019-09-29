podTemplate(containers: [
  containerTemplate(name: 'python', image: 'python:3.6', ttyEnabled: true, command: 'cat')
  ]) {

  node(POD_LABEL) {
    stage('Build a Python project') {
      git 'https://github.com/kuzmacska/python-ip-script.git'
      container('python') {
          sh 'python main.py'
      }
    }
  }
}