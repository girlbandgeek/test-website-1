pipeline {
	agent any
	environment {
		FTP_CREDS = credentials('doxen_ftp')
	}
	stages {
		stage('Deploy') {
			steps {
				sh('ncftpput -R -v -u ${FTP_CREDS_USR} -p ${FTP_CREDS_PSW} ftp.danieloxenhandler.com /public_html/danox/test-website-1 content/*')
			}
		}
	}
}
