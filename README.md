### 1.
```buildoutcfg
HTTP/1.1 301 Moved Permanently
```
>Означает что запрошенная страница была перемещена и доступна по адресу
```buildoutcfg
location: https://stackoverflow.com/questions
```

### 2.
```buildoutcfg
Request URL: http://stackoverflow.com/
Request Method: GET
Status Code: 307 Internal Redirect
Referrer Policy: strict-origin-when-cross-origin
```
> Полностью страница загрузидась за 8.65 сек.

> Дольше всего загружалась страница https://stackoverflow.com/ 1.01 сек
 
![скриншот](https://github.com/Vladislav-Pugachev/netology-DevOps-dz_-11/blob/main/consol.JPG)

### 3.
```buildoutcfg
root@vagrant:~# curl ifconfig.me.
213.87.195.56
```

### 4.
```buildoutcfg
route:          213.87.192.0/21
descr:          Mobile TeleSystems, OJSC, Ufa
origin:         AS42115
```

### 5.
```buildoutcfg
traceroute -IAn 8.8.8.8
traceroute to 8.8.8.8 (8.8.8.8), 30 hops max, 60 byte packets
 1  10.0.2.2 [*]  1.393 ms  2.429 ms  0.768 ms
 2  192.168.0.1 [*]  14.107 ms  15.952 ms  21.317 ms
 3  100.88.0.1 [*]  18.628 ms  16.750 ms  22.511 ms
 4  212.188.61.77 [AS8359]  20.483 ms  21.544 ms  26.547 ms
 5  212.188.61.76 [AS8359]  27.028 ms  29.341 ms  28.382 ms
 6  195.34.59.161 [AS8359]  23.260 ms  77.468 ms  79.856 ms
 7  195.34.50.161 [AS8359]  91.926 ms  90.875 ms  91.755 ms
 8  212.188.29.82 [AS8359]  90.527 ms  89.806 ms  89.493 ms
 9  108.170.250.99 [AS15169]  37.726 ms  42.735 ms  43.816 ms
10  142.251.49.24 [AS15169]  45.941 ms  46.518 ms  45.585 ms
11  108.170.235.64 [AS15169]  38.370 ms  39.262 ms  43.965 ms
12  142.250.236.77 [AS15169]  42.501 ms  44.309 ms  45.605 ms
13  * * *
14  * * *
15  * * *
16  * * *
17  * * *
18  * * *
19  * * *
20  * * *
21  8.8.8.8 [AS15169]  46.359 ms * *
```


### 6.
>сымые большие задержки возникают между 9 и 12 хопами
```buildoutcfg
vagrant (10.0.2.15)                                                                            2021-11-16T17:44:22+0000
Keys:  Help   Display mode   Restart statistics   Order of fields   quit
                                                                               Packets               Pings
 Host                                                                        Loss%   Snt   Last   Avg  Best  Wrst StDev
 1. AS???    10.0.2.2                                                         0.0%    29    2.8   4.7   1.2  16.1   4.1
 2. AS???    192.168.0.1                                                      0.0%    29    5.0  17.0   3.1  93.7  18.5
 3. AS???    100.88.0.1                                                       0.0%    28   59.3  20.8   3.8  85.7  22.9
 4. AS8359   212.188.61.77                                                    0.0%    28   90.5  18.4   4.8  90.5  17.9
 5. AS8359   212.188.61.76                                                    0.0%    28   39.7  22.8   4.9  90.4  25.6
 6. AS8359   195.34.59.161                                                    0.0%    28   92.4  24.0  12.3  92.4  17.4
 7. AS8359   195.34.50.161                                                    0.0%    28   55.1  41.6  24.7  90.0  21.3
 8. AS8359   212.188.29.82                                                    0.0%    28   75.4  38.3  24.7  94.2  19.5
 9. AS15169  108.170.250.99                                                   0.0%    28  135.5  42.0  25.6 135.5  24.2
10. AS15169  142.251.49.24                                                    7.1%    28  122.0  58.8  40.2 122.0  24.4
11. AS15169  108.170.235.64                                                   0.0%    28   51.2  54.7  37.3 105.1  18.0
12. AS15169  142.250.236.77                                                   0.0%    28  185.1  54.7  37.6 185.1  32.0
13. (waiting for reply)
14. (waiting for reply)
15. (waiting for reply)
16. (waiting for reply)
17. (waiting for reply)
18. (waiting for reply)
19. AS15169  8.8.8.8                                                         63.0%    28   71.6  50.9  39.9  82.3  15.4
```

### 7.


```buildoutcfg
dns.google.             10800   IN      NS      ns1.zdns.google.
dns.google.             10800   IN      NS      ns3.zdns.google.
dns.google.             10800   IN      NS      ns2.zdns.google.
dns.google.             10800   IN      NS      ns4.zdns.google.
```

```buildoutcfg
dns.google.             900     IN      A       8.8.8.8
dns.google.             900     IN      A       8.8.4.4
```

### 8.

```buildoutcfg
root@vagrant:~# dig -x 8.8.8.8 +short
dns.google.
root@vagrant:~# dig -x 8.8.4.4 +short
dns.google.
```
