podTemplate(containers: [
	containerTemplate(name: 'jekyll', image: 'jekyll/jekyll:3.8'),
]) {
	node(POD_LABEL) {
        stage('Run shell') {
            git 'https://github.com/serendeepia/serendeepia.github.io.git'
            container('jekyll') {
                sh '/srv/jekyll build'
            }
        }
    }
}

// pipeline {
//     agent {
//         docker {
//             image 'jekyll/jekyll:3.8'
//             args '-u root:root -v "${WORKSPACE}:/srv/jekyll"'
//         }
//     }
//     stages {
//         stage('Test & Build') {
//             steps {
//                 sh '/srv/jekyll build'
//             }
//         }
//     }
// }
