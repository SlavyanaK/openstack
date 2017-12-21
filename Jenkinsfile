node {
	stage ('Checkout Source Code'){
		checkout scm
	}

	stage('Read file'){
		def newTopologyCreation = readJSON file: './infraTopology.json'
		println newTopologyCreation
	}
	
}