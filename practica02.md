## Exercici 1
Tecleja un arxiu amb nano com el següena però els “·” substitueix-los per espais.

_Ajuda:_ Pots copiar i apaegar en un editor de text creant un fitxer "fitxer" i després executar :
```bash
 tr "·" " " <fitxer>fitxer1
```
> linux······unix···windows·······ms-dos···dr-dos····mac-os···cotxas   
hal·········klatu·····robot···········barada····matrix····arbusto··terminator   
carme····usto······pere·············maria·····josep······anna·······susanna······montse
camio····cotxe····carreto·········bicicleta·moto······susto·······helicopter
cotxes···avions···biccccicletessss
Almeuordinadoralgunacosalifalla

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

## Execici 2
Crea un fitxer anomenat agenda amb aquesta informació:


> Josep Garcia  
+34 678 456 545   
jgarcia234@gmail.com   
C/Perú, 23   
València, València   
Carme Velázquez   
+46 567 456 342  
carmen@hotmail.com  
C/ Sin nombre  
Gandia, València  
Aina Cohen  
+34 675 545 343  
ainamallorca@mallorca.org  
C/ Menorca  
Palam, Mallorca  


1. Fes una cerca per un número de telèfon qualsevol amb l’ajuda de la comanda grep. Fes que es vegin tant la línia anterior (opció -B, busca a l’ajuda) com les tres línies posteriors.

```bash
grep "+[0-9]\{2,2\} [0-9]\{3,3\} [0-9]\{3,3\} [0-9]\{3,3\}" text1 
```
```bash
grep -B 1 -A 3 "+[0-9]\{2,2\} [0-9]\{3,3\} [0-9]\{3,3\} [0-9]\{3,3\}" text1
```
2. Fes el mateix però ara cercant per correu electrònic. Crea un àlies a dins de .bashrc
(anomena’l email) que ens permeti fer aquesta cerca de forma més còmoda.
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
Eliminem-lo
```bash
unalias buscaemail
```
Afegim la línia al fitxer bashrc del nostre directori de treball
```bash
sudo nano ~/.bashrc
```
3. Busca recursivament al directori /etc totes les línies de tots els fitxers que continguin la paraula hostname. A l’executar l’ordre com a usuaris normals és possible que ens apareguin molts errors per pantalla. Com ho faríem per evitar que surtin aquests errors per
pantalla? (sense emprar sudo o executar-ho com a root).
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

4. Per a l’anterior ordre, afegeix amb “|” l’ordre necessària per a comptar el nombre de
trobades de la paraula “hostname”.
```bash
grep -r "\<hostname\>" /etc 2>/dev/null|wc -l
```

5. Compta el nombre de processos amb nom bash que hi hagi en execució al teu ordinador.
```bash
ps -aux|grep "\<bash\>"
```


