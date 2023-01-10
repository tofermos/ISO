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

tr "·" " "<fitxer1









```
