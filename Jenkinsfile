node {
	checkout scm

	stage('Read file'){
		def readTopology = readYaml file: "./template-stack-creation.yml"
		echo "Topology to create: $readTopology"

		readTopology.resources.each{
			println it
		}

	}
}