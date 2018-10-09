pipeline {
  agent any
  stages {
    stage('') {
      steps {
        sh '''#!/bin/sh
              : ' INPUT_STRING=hello
              while [ "$INPUT_STRING" != "bye" ]
              do
                echo "Please type something in (bye to quit)"
                read INPUT_STRING
                echo "You typed: $INPUT_STRING"
              done

              while read f
              do
                case $f in
                  hello) echo English ;;
                  howdy) echo American ;;
                  *) echo unknown ;;
                esac
              done < myfile'
              i=0
              while :
              do
                echo $i
                if [ $i -eq "5" ] ; then
                  break
                fi
                i=`expr $i + 1 `
              done '''
      }
    }
  }
}