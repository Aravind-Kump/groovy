// execute echo command
properties([parameters([<object of type com.cwctravel.hudson.plugins.extended_choice_parameter.ExtendedChoiceParameterDefinition>, <object of type com.cwctravel.hudson.plugins.extended_choice_parameter.ExtendedChoiceParameterDefinition>])])
agent {
   node {
       label 'slave1'
       steps {
       println(echo Hello World! ${type})
   }
   }
}


node {
  echo 'Hello World'
  properties([parameters([<object of type com.cwctravel.hudson.plugins.extended_choice_parameter.ExtendedChoiceParameterDefinition>])])
  println ("${<object of type com.cwctravel.hudson.plugins.extended_choice_parameter.ExtendedChoiceParameterDefinition>}")

}


node {
   stage ("testing") {
       def list = ["abc", "def"]
       listIterator(list)
       listIterator2(list)
       println "done."
   }
}

@NonCPS
def listIterator(List<String> list) {
   list.each { item -> println "item[${item}]" }
}

@NonCPS
def listIterator2(List<String> list) {
   list.each { item -> echo "item[${item}]" }




///node {
///    stage ("testing") {
///        def list = ["${Date}", "${Start-Time}", "${End-Time}"]
///        listIterator(list)
///        listIterator2(list)
///        listIterator3(list)
///        println "done."
///    }
///}

echo "${Date}"
println "${Start-Time}"
println "${End-Time}"
@NonCPS
def listIterator(List<String> list) {
   list.each { item -> echo "${Date}" }
}

@NonCPS
def listIterator2(List<String> list) {
   list.each { item -> println "${Start-Time}" }
}

def listIterator3(List<String> list) {
   list.each { item -> println "${End-Time}" }
}



properties([parameters([<object of type com.cwctravel.hudson.plugins.extended_choice_parameter.ExtendedChoiceParameterDefinition>, <object of type com.cwctravel.hudson.plugins.extended_choice_parameter.ExtendedChoiceParameterDefinition>, <object of type com.cwctravel.hudson.plugins.extended_choice_parameter.ExtendedChoiceParameterDefinition>])])


node ('slave'){
   stage ("testing") {
       sh 'echo ${Start_Time} ${End_Time} ${Date}'
       def sout = new StringBuilder(), serr = new StringBuilder()
       def proc = 'ls /var/lib/jenkins/workspace/sample001'.execute()
       proc.consumeProcessOutput(sout, serr)
       proc.waitForOrKill(1000)
       println "out> $sout err> $serr"
   }
}
