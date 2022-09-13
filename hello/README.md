## Hello

Running the ANTLR tool on Hello.g4 generates an executable recognizer embodied by HelloParser.java and HelloLexer.java.
```
>> antlr4 Hello.g4
>> javac *.java
```

ANTLR provides a flexible testing tool in the runtime library called `TestRig`. It can display lots of information about how a recognizer matches input from a file or standard input. TestRig uses Java reflection to invoke compiled recognizers.
```
>> grun Hello r -tokens
hello world
^D
[@0,0:4='hello',<'hello'>,1:0]
[@1,6:10='world',<ID>,1:6]
[@2,12:11='<EOF>',<EOF>,2:0]
```

```
>> grun Hello r -tree
hello world
^D
(r hello world)
```

```
>> grun Hello r -gui
hello world
^D
```