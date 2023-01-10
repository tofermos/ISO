1. Fes que ens escrigui per pantalla totes les línies que tinguin una ‘x’ almenys
2. Totes les línies amb guions
3. Totes les línies que comencen amb ‘c’
4. Totes les línies que acabin amb ‘r’
5. Les línies que continguin ‘x’ o ‘d’
6. Les línies que continguin ”cotxe” o ”cotxes”
7. Les línies que contingui la paraula “cotxe”. No val ”cotxes”.
8. Les línies que continguin qualsevol, paraula que comenci per “ca”
9. Les línies que continguin qualsevol paraula que acabi en “dos”
10. Les línies que continguin dues “n” seguides.
11. Llista només els directoris del teu directori de treball.
12. Crea tres arxius dins el teu directori personal amb touch i amb chmod fes-los
executables. Després fes amb ls i grep que es llistin només els executables del teu
directori personal o de treball.
13. Les línies amb almenys 8 espais seguits.
```bash
tomas@portatil:~/Documents/proves$ grep x fitxer1 

camio····cotxe····carreto·········bicicleta·moto······susto·······helicopter
tomas@portatil:~/Documents/proves$ grep - fitxer1 

tomas@portatil:~/Documents/proves$ grep ^c fitxer1 

tomas@portatil:~/Documents/proves$ grep r$ fitxer1 
tomas@portatil:~/Documents/proves$ grep [xd] fitxer1 
tomas@portatil:~/Documents/proves$ grep cotxes* fitxer1 
tomas@portatil:~/Documents/proves$ grep "\<cotxe\>" fitxer1
tomas@portatil:~/Documents/proves$ grep "\<ca" fitxer1
tomas@portatil:~/Documents/proves$ grep "dos\> fitxer1tomas@portatil:~/Documents/proves$ grep "\<ca" fitxer1
tomas@portatil:~/Documents/proves$ grep "n\{2,2\}" fitxer1
tomas@portatil:~/Documents/proves$ grep "n\{2,\}" fitxer1
tomas@portatil:~/Documents/proves$ ls -l ~|grep ^d
tomas@portatil:~/Documents/proves$ chmod u+x,g+x,o+x ~/f?
tomas@portatil:~/Documents/proves$ ls -l ~|grep ^-..x..x..x
tomas@portatil:~/Documents/proves$ chmod u+x,g+x,o+x ~/f?
tomas@portatil:~/Documents/proves$ ls -l ~|grep ^-..x..x..x
```
Execici 2
```bash
tomas@portatil:~/Documents/proves$ grep "+[0-9]\{3,5\} [0-9]\{3,5\}" text1 
+12345 678
+2345 6789
+345 67890
tomas@portatil:~/Documents/proves$ grep -B 1 -A 3 "+[0-9]\{3,5\} [0-9]\{3,5\}" text1 
Charly Pingüí
+12345 678
tux@linux.org
C/ del Pol Sud
Vilatux, Antàrtica
Pepito uno
+2345 6789
pepito@linux.org
C/ uno
Gandia, València
Jaimito dos
+345 67890
jaimito@linux.org
C/ dos
Benidorm, Alacant
```

```bash
tomas@portatil:~/Documents/proves$ grep ".*@.*\.\(org\|com\|net\)" text1 
tux@linux.org
pepito@linux.org
jaimito@linux.org
```
Creem el alias
```bash
tomas@portatil:~/Documents/proves$ alias buscaemail='grep ".*@.*\.\(org\|com\|net\)"'
tomas@portatil:~/Documents/proves$ buscaemail text1 
tux@linux.org
pepito@linux.org
jaimito@linux.org
```
Afegim la línia
```bash
sudo nano ~/.bashrc
```
```bash
grep -r "\<hostname\>" /etc
```
Omitir errors en pantalla ( 2 solucions possibles)
```bash
grep -r "\<hostname\>" /etc 2>/dev/null
```
```bash
grep -r -s "\<hostname\>" /etc
```
Comptar amb |
```bash
grep -r "\<hostname\>" /etc 2>/dev/null|wc -l
```
Procesos amb bash
```bash
tomas@portatil:~$ ps -aux|grep bash
tomas       4881  0.0  0.0  19556  5684 pts/0    Ss+  15:23   0:00 bash
tomas       6292  0.0  0.0  20272  6556 pts/1    Ss+  15:44   0:00 bash
tomas       8468  0.0  0.0  19436  5536 pts/2    Ss   17:00   0:00 bash
tomas       8845  0.0  0.0  17248  2224 pts/2    S+   17:13   0:00 grep --color=auto bash
```


