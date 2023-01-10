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
grep x fitxer1 
```
```bash
grep - fitxer1 
```
```bash
grep ^c fitxer1 
```
```bash
grep r$ fitxer1 
```
```bash
grep [xd] fitxer1 
```
```bash
grep cotxes* fitxer1 
```
```bash
grep "\<cotxe\>" fitxer1
```
```bash
grep "\<ca" fitxer1
```
```bash
grep "dos\> fitxer1
```
```bash
grep "\<ca" fitxer1
```
```bash
grep "n\{2,2\}" fitxer1
```
```bash
grep "n\{2,\}" fitxer1
```
```bash
ls -l ~|grep ^d
```
```bash
chmod u+x,g+x,o+x ~/f?
```
```bash
ls -l ~|grep ^-..x..x..x
```
```bash
chmod u+x,g+x,o+x ~/f?
```
```bash
ls -l ~|grep ^-..x..x..x
```

Execici 2
```bash
grep "+[0-9]\{3,5\} [0-9]\{3,5\}" text1 
```
grep -B 1 -A 3 "+[0-9]\{3,5\} [0-9]\{3,5\}" text1 
```

```bash
grep ".*@.*\.\(org\|com\|net\)" text1 
```
Creem el alias
```bash
alias buscaemail='grep ".*@.*\.\(org\|com\|net\)"'
```
El provem
```bash
buscaemail text1 
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
ps -aux|grep bash
```


