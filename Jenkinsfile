node {
	checkout scm

	stage('Read file'){
		def readTopology = readYaml file: "./template-stack-creation.yml"
		//echo "Topology to create: $readTopology"
		println readTopology.resources[0]
		/**readTopology.resources.each{
			println "PRINT $it"
		}**/

	}
}