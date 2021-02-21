pipeline {
    agent any
    parameters {
      string(defaultValue: 'All_TestData.py', description: 'This is used to replace testdata file name', name: 'testDataFile', trim: true)
      choice(choices: ['5268AC', 'NVG599', 'BGW210-700'], description: '', name: 'deviceModel')
    }
    stages {
        stage('Run ECOManageGUI on '${params.choices[0]}) {
            steps{
                echo 'Run ECOManageGUI testsuite on '${params.choices[0]}
                build 'Robot Framework - ECOManageGUI'
            }
        }
    }
}
