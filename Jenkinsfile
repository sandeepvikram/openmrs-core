node('SPC') {
    Stage('scm') {
        git "https://github.com/sandeepvikram/openmrs-core.git"
    }
    stage('build') {
        sh 'mvn package'
    }
    stage('postbuild') {
        junit '**/TEST-*.xml'
        archive '**/*.war'
    }
}