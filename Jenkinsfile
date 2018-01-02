node {
	checkout scm

	stage('Read file'){
		def topologyToCreate = readYaml file: "./template-stack-creation.yml"
		echo "Topology to create: $topologyToCreate"
	}
}