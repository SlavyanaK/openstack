node {
	checkout scm

	stage('Read file'){
		def topologyToCreate = readYaml file: "./template-stack-creation.yml"
		echo "Topology to create: $topologyToCreate"
	}

	stage('Check infra ressource availability'){
		echo "check"
	}

	stage('Upgrade Infra'){
		withCredentials([[$class: 'UsernamePasswordMultiBinding', credentialsId: 'skokorina', usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD']]) {
			docker.image('slav/openstack-cli-heat:1.0').inside(){
				sh "./tpe-dla-cec-openrc.sh && \
        		export OS_PASSWORD=${env.PASSWORD} && \
	        	export OS_USERNAME=${env.USERNAME} && \
	        	openstack router list"
	        }
	    }
	}

	stage('Check Infra Creation'){
	}	
}