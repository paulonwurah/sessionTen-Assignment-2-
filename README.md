# sessionTen-Assignment-2-

Using SPARK SHELL

Execute map, flatMap, filter, reduceByKey, collect, count, reduce RDDs with an example 


val input = sc.parallelize(List(“Acadgild is the best school of the moment”))

val flattenInput = input.flatMap(x => x.split(“  “))

val  mapInput = flattenInput.map(x => x.length)

mapInput.count()

val reduceFlattenedInput = mapInput.reduce((x,y) => (x+y))

val KeyValue= reduceFlattenedInput.map(x => x + 1)

val reduceKeyValue  = keyValue.reduceByKey((x,y) => (x+y))

reduceByKey.collect()
