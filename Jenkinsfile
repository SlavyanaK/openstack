node {
	stage ('Checkout Source Code'){
		checkout scm
	}

	stage('Read file'){
		def newTopologyCreation = readJSON file: './infraTopology.json'
		println ("Topology to create: $newTopologyCreation")
		def networkName = newTopologyCreation["Network"]["name"]
		println ("Network name: $networkName")
	}
	
}