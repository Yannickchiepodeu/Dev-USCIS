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
}
