node {
	
	def mapTopology = [:]
	stage ('Checkout Source Code'){
		checkout scm
	}

	stage('Read file'){
		def newTopologyCreation = readJSON file: './infraTopology.json'
		println ("Topology to create: $newTopologyCreation")
		mapTopology = ['networkName': "${newTopologyCreation["Network"]["name"]}", 
						'subnetName': "${newTopologyCreation["Subnet"]["name"]}",
						'subnetRange': "${newTopologyCreation["Subnet"]["subnet-range"]}",
						'routerName': "${newTopologyCreation["Router"]["name"]}",
						'routerExternalGateway': "${newTopologyCreation["Router"]["external-gateway"]}",
						'serverName': "${newTopologyCreation["Server"]["name"]}",
						'serverImage': "${newTopologyCreation["Server"]["image"]}",
						'serverFlavor': "${newTopologyCreation["Server"]["flavor"]}",
						'serverSecurityGroup': "${newTopologyCreation["Server"]["security-group"]}",
						'serverKeyName': "${newTopologyCreation["Server"]["key-name"]}",
						'serverAvailabilityZone': "${newTopologyCreation["Server"]["availability-zone"]}"]
		mapTopology.each { name, value ->
			println "Topology: $name - $value"
		}
	}
	
}