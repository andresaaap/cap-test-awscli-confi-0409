pipeline {
	agent any
	stages {


		stage('Domain redirect blue') {
			steps {
				withAWS(region:'us-east-1', credentials:'aws-static') {
					sh '''
						aws route53 change-resource-record-sets --hosted-zone-id ZKCU19G790VD6 --change-batch file://alias-record.json
					'''
				}
			}
		}
	}
}