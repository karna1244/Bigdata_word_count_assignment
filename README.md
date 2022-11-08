# Bigdata_word_count_assignment

1. For the maven file creation I used the following command
```
mvn archetype:generate `
  -D archetypeGroupId=org.apache.beam `
  -D archetypeArtifactId=beam-sdks-java-maven-archetypes-examples `
  -D archetypeVersion=2.42.0 `
  -D groupId=org.example `
  -D artifactId=word-count-beam `
  -D version="0.1" `
  -D package=org.apache.beam.examples `
  -D interactiveMode=false
```
2. I changed to word-count-beam directory
```
cd .\word-count-beam
```

3. Getting the list of example pipelines  
```
dir .\src\main\java\org\apache\beam\examples
```

4. Creating a file for sample.txt
```
New-item -Path . -Name "sample.txt" -ItemType "file"
```

5. Running the WordCount pipeline using the following command
```
mvn compile exec:java -D exec.mainClass=org.apache.beam.examples.WordCount `
 -D exec.args="--inputFile=sample.txt --output=counts" -P direct-runner
```
6. View the output coutext using the following command
```
more counts*
```

Reference link
[beam](https://beam.apache.org/get-started/quickstart-java/)


   