node('<JDK8>'){
        stage ('SourceCodes'){
                 //get the code from git repo
                  git branch: 'spring1_devolop', url: 'https://github.com/johnbek1/game-of-life.git'
        }
        stage ('Build the  code '){
                 sh 'mvn clean package'
        }
        stage ('Archiving and Test Results'){
                junit '**/surefire-reports/*.xml'
                archiveArtifacts artifacts: '**/*.war', followSymlinks: false
        }
}

