node {
	
	def mapTopology = [:]
	stage ('Checkout Source Code'){
		checkout scm
	}

	stage('Read file'){
		def topologyToCreate = readYaml file: "./template-stack-creation.yml"
		println topologyToCreate['ressources']['os-network-1']['type']
	}
	
}