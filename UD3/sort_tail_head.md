# Exemples usos tail, head i sort
```bash
tomas@portatil:~/Documents/textos$ ls -l |sort -nr
total 12
-rw-rw-r-- 1 tomas tomas 63 de des.   5 10:56 fitxer.txt
-rw-rw-r-- 1 tomas tomas 30 de des.   5 11:07 f13
-rw-rw-r-- 1 tomas tomas  6 de des.   5 11:07 f1
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f12
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f11
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f10
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f09
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f08
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f07
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f06
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f05
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f04
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f03
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f02
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f01
```
Per eliminar lnies de resum o totalitzadores a l'inici..

tomas@portatil:~/Documents/textos$ ls -l |sort -nr|tail -n +2
-rw-rw-r-- 1 tomas tomas 63 de des.   5 10:56 fitxer.txt
-rw-rw-r-- 1 tomas tomas 30 de des.   5 11:07 f13
-rw-rw-r-- 1 tomas tomas  6 de des.   5 11:07 f1
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f12
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f11
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f10
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f09
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f08
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f07
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f06
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f05
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f04
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f03
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f02
-rw-rw-r-- 1 tomas tomas  0 de des.   5 10:01 f01
tomas@portatil:~/Documents/textos$ ls -l |sort -nr|tail -n +2|head -n 3
-rw-rw-r-- 1 tomas tomas 63 de des.   5 10:56 fitxer.txt
-rw-rw-r-- 1 tomas tomas 30 de des.   5 11:07 f13
-rw-rw-r-- 1 tomas tomas  6 de des.   5 11:07 f1
tomas@portatil:~/Documents/textos$ 
