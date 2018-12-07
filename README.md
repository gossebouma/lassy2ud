# lassy2ud
Lassy Small to Universal Dependencies Conversion 

This script was used to procude the UD Dutch (as of V2.1) and UD Dutch LassySmall corpora in the Universal Dependencies repository. It takes (manually corrected) annotation as produced in the LassySmall and related projects as input.

Paper: 

* Gosse Bouma and Gertjan van Noord [Increasing Return on annotation investment: the automatic construction of a Universal Dependency treebank for Dutch](http://aclweb.org/anthology/W17-0403)

in: Proceedings of the Universal Dependencies Workshop, Gothenburg, 22 May 2017

* Gosse Bouma, Comparing Two Methods for Adding Enhanced Universal Dependencies to UD Treebanks, to appear in: Proceedings of the 17th International Workshop on Treebanks and Linguistic Theory, Oslo, 2018

## usage

For universal_dependencies.xq :

Example with [saxon](http://www.saxonica.com):

```sh
saxon DIR=collection.xml LIB=no MODE=conll ENHANCED=yes universal_dependencies_2.3.xq
```

Example with [xqilla](http://xqilla.sourceforge.net):

```sh
xqilla -v DIR collection.xml -v MODE conll -v ENHANCED yes universal_dependencies_2.3.xq
```

These examples assume you have a file `collection.xml` with the names
of the individual files you want to prosess. Example:

```xml
<collection>
<doc href="file1.xml"/>
<doc href="file2.xml"/>
</collection>
```
