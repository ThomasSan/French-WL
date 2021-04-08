# Wordlist traduites en Francais

Lors des pentest j'ai toujours du mal a trouver des wordlist clean en Francais. Celles-ci sont extraites des ressources telles que les WL de Wfuzz, SecLists et DirBuster.
Je les ai clean des accents et j'ai retire les caracteres speciaux.


```bash
cat file.txt tr '[:upper:]' '[:lower:]' | sed 's/[ëèé]/e/g' | sed 's/[äâ]/a/g' | cut -d \' -f 2 | grep -v '[[:punct:]]' | grep -v '[[:digit:]]' | sort -u 
```
