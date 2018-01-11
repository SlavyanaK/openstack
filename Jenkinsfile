node {
	checkout scm
	def test = ""

	stage('Read file'){
		sh "ls -l"
		sh "cat logs.txt" >> $test
		println test
	}
}