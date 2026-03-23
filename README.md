core cases :
| TC | Popis | Dáta | Očakávanie |
|----|-------|------|------------|
| TC01 | 2x nula, ≥100 dní | 1.1:0, 15.5:0 | nevierohodné |
| TC02 | 2x nula, <100 dní | 1.1:0, 1.3:0 | vierohodné |
| TC03 | viac ako 2 nuly, ≥100 dní | 1.1:0, 15.5:0, 1.9:0 | nevierohodné |
| TC04 | prerušená sekvencia | 0 → 10 → 0 → 0 | vierohodné |
| TC05 | presne 100 dní | rozdiel = 100 | nevierohodné |
| TC06 | 99 dní | rozdiel = 99 | vierohodné |
| TC07 | typ 02 (výnimka) | 0,0 typ 02 | vierohodné |
| TC08 | typ 03 (výnimka) | 0,0 typ 03 | vierohodné |
| TC09 | dôvod 06 (výnimka) | 0,0 dôvod 06 | vierohodné |
| TC10 | kombinácia výnimka + normálny | 0(normálny), 0(typ02) | vierohodné |
| TC11 | zmena parametra x=3 | 2 nuly | vierohodné |
| TC12 | zmena parametra y=50 | 60 dní | nevierohodné |
| TC13 | vypnutá validácia | ľubovoľné | vierohodné |
| TC14 | hromadné vs postupné nahratie | rovnaké dáta | rovnaký výsledok |

edge cases :
| TC | Popis | Dáta | Očakávanie |
|----|-------|------|------------|
| TC15 | x = 1 (každá nula) | 1.1:0 | nevierohodné |
| TC16 | x = 0 (neplatná hodnota) | param x=0 | chyba / nevalidné nastavenie |
| TC17 | y = 0 | 1.1:0, 2.1:0 | nevierohodné |
| TC18 | y < 0 (neplatná hodnota) | param y=-10 | chyba / nevalidné nastavenie |
| TC19 | prerušenie nenulovou hodnotou (čas splnený) | 1.1:0, 1.2:5, 1.6:0 | vierohodné |
| TC20 | viac odpočtov medzi nulami | 1.1:0, 1.2:5, 1.3:7, 1.6:0 | vierohodné |
| TC21 | kombinácia výnimka uprostred | 0(normálny), 0(typ02), 0(normálny) | vierohodné |
| TC22 | kombinácia viac výnimiek | 0(typ02), 0(typ03), 0(normálny) | vierohodné |
