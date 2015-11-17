#Oprendszerek elmélet

#####Mi az operációs rendszer kernel módja és felhasználói módja közti különbség?
   -Különböző védelmi szintek, kernel mód -> felügyelt mód, felhasználói mód -> oprendszer feladatok
#####Milyen kommunikációs típust ismerünk a perifériákkal?
   -Lekérdezés átvitel (polling), megszakítás (interrupt), közvetlen memória elérés (DMA)
#####Mi a "virtuális gép" operációs rendszer struktúra lényege, honnan ered ez az elv?
   -Az IBM-től származik az elv, nem érdekel, hogyan teszi,át akarok másolni egy képet.
#####Mi a CHS címzés?
   -Cilinder-Head-Selecor, mágneslemeznél adatok címzésére használjuk
#####Írja le az SSTF ütemezés lényegét és jellemzőit!
   -
#####Mi az i-node tábla?
   -UNIX rendszeren minden fájlt egy i-node ír le.
#####Az operációs rendszerek folyamatainak milyen állapotait, állapotátmeneteit ismerjük?
#####A kölcsönös kizárás Peterson féle megoldásának mi a lényege? (algoritmus)
#####Mi a szemafor?
#####Mi a különbség a szemafor és a mutex között?
#####Mit értünk folyamatok ütemezésén?
#####Mi a "sorsjáték ütemezés" lényege, hol használják?
#####Mit jelent a holtpont gráfmodellje?
#####Ismertesse a bankár algoritmust! Lényege!
#####Mi a POSIX?
#####Mik a(z) (1., 2., 3., 4.) generációs operációs rendszerek jellemzői?
#####Mi a RAID(1..5), mi a működésének a lényege?
   -RAID1: Két független lemezből készít egy logikai egységet, egyszerre menti mindkettőre. Tároló kapacitás felére csökken
   -RAID2: Adatbitek mellett hibajavító biteket tartalmaz. ECC pl. 4 diszkhez 3 javító diszk.
   -RAID3: Elég egy plusz paritásdiszk n+1 diszk, szum n a kapacitás
   -RAID4: RAID0 + paritásdiszk
   -RAID5: Nincs paritás diszk, el van osztva a tömb összes elemére. Adatok elosztva kerülnek tárolásra. A paritásbitből meg a többiből egy eltűnt kiszámítható.
#####Mi a kölcsönös kizárás, mik a megvalósítás feltételei?
#####Ismertesse a kölcsönös kizárás megvalósítását TSL utasítással!
#####Ismertesse a folytonos tárkiosztás(lemez) stratégiáit, jellemzőit!
#####Mi a randevú stratégia?
#####Mi a monitor?
#####Mi a mutex?
#####Mi a különbség a monitor és a mutex között?
#####Mi a soft real time rendszer?
#####Mit jelent a monitor "condition" típusa?
#####Mi az arányos ütemezés lényege?
#####Milyen I/O eszközkategóriákat ismer? Mi a kivétel?
#####Mi az MBR?
   -Master Boot Record,a 0.szektor. 2 particíója van az elsőről töltődik be az operációs rendszer
#####Mi a memóriakezelő feladata?
#####Mit értünk tevékeny várakozás alatt?
#####Mit értünk folyamatok erőforrás görbélyén, mire használható?
#####Mit értünk virtuális memóriakezelésen, mi a lényege? Mi a lapozás?
#####Mi a szoftveres és a hardveres megszakítás közti különbség? Van egyáltalán?
#####Mi az SSTF ütemezés lényege?
   -Shortest Seek Time First, leghamarabb elérhetőt először
#####Mit nevezünk fájlrendszernek, mi köze van az FCFS ütemezéshez?
   -First Come - First Service ahogy jönnek a kérések úgy szolgáljuk ki őket.
#####Milyen periféria kommunikációs módot ismer?
#####Mi az Ext2FS, van-e MBR-je?-je.   
   -Linux partíció és van MBR
#####Mi a TLB, mi a szerepe?
#####RAID-ek közti különbségek.
#####Honnan származik, és mi a lényege a virtuális gépek(szerver) használatának?
#####Ismertesse a folytonos tárkiosztás(lemez) stratégiáit!
#####Mi a szemafor, mikor nem használható?
#####Mi a Robin-Robin ütemezés lényege?
#####Milyen partíciónak nincs i-node táblája?
#####Mi a RAID0+1 illetve RAID1+0 lemezek közti különbség?
#####Honnan származik az op.rendszer virtualizáció, mik a jellemzői, mi köze a virtuális memóriakezeléshez?
#####Mit nevezünk szegmentált memóriakezelésnek?
#####Mi a valós idejű ütemezés lényege?
#####Milyen processzor védelmi szinteket ismer, hol használjuk ezeket?
#####Ismertesse a "probléma figyelmen kívül hagyása" módszert! Hol alkalmazzák?
#####Mi az MFT?
#####Mi a probléma a kölcsönös kizárás szigorú váltogatásos megvalósítással?
#####Mit jelent az "interleave" fogalma?
#####Mit nevezünk valós idejű operációs rendszernek?
#####Milyen fájlrendszer specifikus fájlokat ismer? Hol találhatók átalában?
   -Karakter,blokk fájlok, /dev könyvtár
#####Mik a program-folyamat-szál közti különbségek?
#####Mit nevezünk fájlrendszernek, mi köze van az FCFS ütemezéshez?
#####I/O szoftver modellje, milyen eszközkategóriákat ismer?
#####Mit nevezünk kritikus tevékenységnek?
#####Mire szolgálnak a lapozási algoritmusok?
#####Mi a különbség folyamatok és szálak között? Van egyáltalán?
#####Ismertesse a laptáblák szerepét! Vam köze a TLB-Hez?
#####Miért hasznos a kölcsönös kizárás üzenetküldéses megvalósítása?
#####Mire használható a monitor?
#####Mire jó a "Dirty-bit", hol használják?
#####Mi a CHS-LBA címzés közti különbség? Van egyáltalán?
   -CHS korlát 504MB, LBA minden szektor egyedi számot kap. A BIOS a megszakítások paramétereit az átalakított geometriából lemez geometriává alakítja CHS-nél, míg szektor számmá LBA-nál.
#####Mi a Round-Robin címzés lényege?
