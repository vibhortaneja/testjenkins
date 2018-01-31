node {

	agent any
    tools { 
        maven 'mvn352' 
        jdk 'jdk8' 
        git 'mygit'
    }

    stages {

	    stage('Checkout') {
	    	steps {
                echo 'In checkout'
		        git url: 'https://github.com/vibhortaneja/testjenkins'
            }
	    }

	    stage('Build') {
	    	steps {
                echo 'In Build'
                sh 'mvn -DskipTests install' 
			}
	    }

	    stage('Deploy') {
	    	steps {
                echo 'In Deploy'
                sh 'mvn publish' 
			}
	    }
    }
}