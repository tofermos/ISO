# Exemples usos tail, head i sort
```bash
tomas@portatil:~/Documents/textos$ ls -l 
total 12
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f01
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f02
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f03
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f04
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f05
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f06
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f07
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f08
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f09
-rw-rw-r-- 1 tomas tomas  6 de des.   5 11:07 f1
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f10
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f11
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f12
-rw-rw-r-- 1 tomas tomas 30 de des.   5 11:07 f13
-rw-rw-r-- 1 tomas tomas 63 de des.   5 10:56 fitxer.txt
```
## Eliminació de títols i totalitzadors.
Un dels usos más habituals del *head* i del *tail* seria per eliminar línies de resum o totalitzadores a l'inici o final d'un text.

A l'exemple següent llevem la línia primera "Total 12", filtrant la cua fins la +2ª línia
```bash
tomas@portatil:~/Documents/textos$ ls -l |tail -n +2
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f01
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f02
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f03
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f04
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f05
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f06
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f07
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f08
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f09
-rw-rw-r-- 1 tomas tomas  6 de des.   5 11:07 f1
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f10
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f11
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f12
-rw-rw-r-- 1 tomas tomas 30 de des.   5 11:07 f13
-rw-rw-r-- 1 tomas tomas 63 de des.   5 10:56 fitxer.txt
```
## LListat ordrenat. N-primeres o N-darreres.
El següent exemple ordrenem per tamany i seleccionem els 3 fitxers més grans.
```bash
tomas@portatil:~/Documents/textos$ ls -l |tail -n +2|sort -n|tail -n 3
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f12
-rw-rw-r-- 1 tomas tomas 30 de des.   5 11:07 f13
-rw-rw-r-- 1 tomas tomas 63 de des.   5 10:56 fitxer.txt
```
Depenent de l'ordrenació ens interessen les primeres o les últimes línies.
```bash
tomas@portatil:~/Documents/textos$ ls -l |tail -n +2|sort -nr|head -n 3
-rw-rw-r-- 1 tomas tomas 63 de des.   5 10:56 fitxer.txt
-rw-rw-r-- 1 tomas tomas 30 de des.   5 11:07 f13
-rw-rw-r-- 1 tomas tomas  6 de des.   5 11:07 f1
```
