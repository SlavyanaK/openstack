node {
	checkout scm
	

	stage('Read file'){
		sh "ls -l"
		sh "cat logs.txt >> output"
		def read = readFile 'output'
		println read
	}
}