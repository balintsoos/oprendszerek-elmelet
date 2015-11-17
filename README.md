#Oprendszerek elmélet

#####Mi az operációs rendszer kernel módja és felhasználói módja közti különbség?
   - Különböző védelmi szintek, kernel mód -> felügyelt mód, felhasználói mód -> oprendszer feladatok

#####Milyen kommunikációs típust ismerünk a perifériákkal?
   - Lekérdezés átvitel (polling), megszakítás (interrupt), közvetlen memória elérés (DMA)

#####Mi a "virtuális gép" operációs rendszer struktúra lényege, honnan ered ez az elv?
   - Az IBM-től származik az elv. Pl. nem érdekel, hogyan teszi át akarok másolni egy képet.

#####Mi a CHS címzés?
   - Cilinder-Head-Selecor, mágneslemeznél adatok címzésére használjuk

#####Írja le az SSTF ütemezés lényegét és jellemzőit!
   - Shortest Seek Time First-leghamarabb elérhetőt először. A legkisebb fejmozgatást részesíti előnyben, átlagos várakozás kicsi,
   tviteli sávszélesség nagy. Kiéheztetés veszélye

#####Mi az i-node tábla?
   - UNIX rendszeren minden fájlt egy i-node ír le. 15 rekeszből áll 12 fájl blokkra mutat. 13., 14. új i-node-ra mutat.

#####Az operációs rendszerek folyamatainak milyen állapotait, állapotátmeneteit ismerjük?
   - Futó
   - Futásra kész, ideiglenesen leállították, CPU időre vár.
   - Blokkolt, ha logikailag nem lehet folytatni, pl. másik folyamat eredményére vár.
   - Állapot átmenetek: futó -> blokkolt, futó -> futásra kész, -> blokkolt -> futásra kész

#####A kölcsönös kizárás Peterson féle megoldásának mi a lényege? (algoritmus)
#####Mi a szemafor?
   - Dijkstra javasolja, egy változótípus. A szemafor tilosat mutat(0) akkor a folyamat elalszik, ha a szemafor>0, akkor be szabad lépni a kritikus szakaszra. Két művelete van: Belépéskor csökkentjük a szemafor értékét, kilépéskor növeljük. Ezek elemi műveletek.

#####Mi a különbség a szemafor és a mutex között?
   - A mutex bináris szemafor, csak 0 és 1 lehet az értéke, pl. vasutas helyzet.
   
#####Mit értünk folyamatok ütemezésén?
#####Mi a "sorsjáték ütemezés" lényege, hol használják?
#####Mit jelent a holtpont gráfmodellje?
   - Holtpont feltételek ábrázolása gráfokkal. Az erőforrásokat és a folyamatokat tartalmazza. Ha az erőforrások, folyamatok gráfjában kör van, az holtpontot jelent.

#####Ismertesse a bankár algoritmust! Lényege!
   - Minden kérés esetén megnézi, hogy a teljesítése biztonságos-e. Úgy osztja el az erőforrásokat, hogy legalább egy kérés biztosan be tudjon fejeződni, így amikor vissza adja az általa használt erőforrásokat akkor a többi kérésnek több jut.

#####Mi a POSIX?
   - Portable Operating System Interface for uniX - szabványos minimális rendszerhívás készlet, egy API

#####Mik a(z) (1., 2., 3., 4.) generációs operációs rendszerek jellemzői?
#####Mi a RAID(1..5), mi a működésének a lényege?
   - RAID1: Két független lemezből készít egy logikai egységet, egyszerre menti mindkettőre. Tároló kapacitás felére csökken
   - RAID2: Adatbitek mellett hibajavító biteket tartalmaz. ECC pl. 4 diszkhez 3 javító diszk.
   - RAID3: Elég egy plusz paritásdiszk n+1 diszk, szum n a kapacitás
   - RAID4: RAID0 + paritásdiszk
   - RAID5: Nincs paritás diszk, el van osztva a tömb összes elemére. Adatok elosztva kerülnek tárolásra. A paritásbitből meg a többiből egy eltűnt kiszámítható.

#####Mi a kölcsönös kizárás, mik a megvalósítás feltételei?
   - Módszer ami biztosítja, hogy a közös adatokat egyszerre csak egy folyamat tudja használni. Feltételei: Nincs két folyamat egyszerre a kritikus szekcióban, nincs sebesség CPU, paraméter függőség, egyetlen kritikus szekción kívül lévő folyamat sem blokkolhat msik folyamatot. Egy folyamat sem vár örökké, hogy a kritikus szekcióba tudjon lépni.

#####Ismertesse a kölcsönös kizárás megvalósítását TSL utasítással!
   - Atomi művelet, a belépéskor TSL lock kerül a regiszterbe, a kilépésig zárolja a memóriasínt.

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
   - Master Boot Record,a 0.szektor. 2 particíója van az elsőről töltődik be az operációs rendszer

#####Mi a memóriakezelő feladata?
#####Mit értünk tevékeny várakozás alatt?
   - A kölcsönös kizárásnál a CPU-t üres ciklusban járatjuk a várakozás során, így a CPU időt pazaroljuk pl. TSL, Peterson

#####Mit értünk folyamatok erőforrás görbélyén, mire használható?
#####Mit értünk virtuális memóriakezelésen, mi a lényege? Mi a lapozás?
#####Mi a szoftveres és a hardveres megszakítás közti különbség? Van egyáltalán?
#####Mi az SSTF ütemezés lényege?
   - Shortest Seek Time First, leghamarabb elérhetőt dolgozzuk fel először

#####Mit nevezünk fájlrendszernek, mi köze van az FCFS ütemezéshez?
   - First Come - First Service ahogy jönnek a kérések úgy szolgáljuk ki őket.

#####Milyen periféria kommunikációs módot ismer?
#####Mi az Ext2FS, van-e MBR-je?-je.
   - Linux fájlrendszer és van MBR.

#####Mi a TLB, mi a szerepe?
   - Translation Lookaside Buffer egy cache, amit a memória kezelő hardver használ, hogy gyorsítson a virtuális címfordítás sebességén.

#####RAID-ek közti különbségek.
#####Honnan származik, és mi a lényege a virtuális gépek(szerver) használatának?
#####Ismertesse a folytonos tárkiosztás(lemez) stratégiáit!
#####Mi a szemafor, mikor nem használható?
#####Mi a Robin-Robin ütemezés lényege?
#####Milyen partíciónak nincs i-node táblája?
   - Csak a UNIX rendszereknek van i-node táblája.

#####Mi a RAID0+1 illetve RAID1+0 lemezek közti különbség?
   - RAID 1+0: Tükrös diszkekből vonunk össze többet
   - RAID 0+1: Raid 0 összevont lemezcsoportból veszünk kettőt.

#####Honnan származik az op.rendszer virtualizáció, mik a jellemzői, mi köze a virtuális memóriakezeléshez?
#####Mit nevezünk szegmentált memóriakezelésnek?
#####Mi a valós idejű ütemezés lényege?
#####Milyen processzor védelmi szinteket ismer, hol használjuk ezeket?
   - 4 szintet különböztetünk meg, ebből 2-t használunk: kernel mód, felhasználói mód.
   - Kernel mód: felügyelt mód
   - Felhasználói mód: oprendszer, feladatok
#####Ismertesse a "probléma figyelmen kívül hagyása" módszert! Hol alkalmazzák?
#####Mi az MFT?
   - Master File Table, ezzel kezdődik az NTFS partició, 16 attribútum ad egy fájl bejegyzést, minden attribútum max 1kb. Ha ez nem elég, akkor egy attribútum mutat a folytatásra. Nincs fájlméret maximum.

#####Mi a probléma a kölcsönös kizárás szigorú váltogatásos megvalósítással?
   - Egy folyamat blokkolhatja saját magát.
#####Mit jelent az "interleave" fogalma?
#####Mit nevezünk valós idejű operációs rendszernek?
#####Milyen fájlrendszer specifikus fájlokat ismer? Hol találhatók átalában?
   - Karakter,blokk fájlok, /dev könyvtár

#####Mik a program-folyamat-szál közti különbségek?
#####Mit nevezünk fájlrendszernek, mi köze van az FCFS ütemezéshez?
   - A számítógépes fájlok tárolásának és rendszerezésének a módszere.A sorrendi ütemezéssel olvashatunk és írhatunk a lemezre, aminek a rendszerét a fájlrendszer adja

#####I/O szoftver modellje, milyen eszközkategóriákat ismer?
#####Mit nevezünk kritikus tevékenységnek?
#####Mire szolgálnak a lapozási algoritmusok?
#####Mi a különbség folyamatok és szálak között? Van egyáltalán?
   - A szál egy folyamaton belüli utasítás sor. Lehet több is egy folyamaton belül
   - csak a folyamatoknak van: címtartománya, globális változója, megnyitott fájl leírója, gyermek folyamata, szignálkezelője, ébresztője

#####Ismertesse a laptáblák szerepét! Vam köze a TLB-Hez?
#####Miért hasznos a kölcsönös kizárás üzenetküldéses megvalósítása?
#####Mire használható a monitor?
#####Mire jó a "Dirty-bit", hol használják?
#####Mi a CHS-LBA címzés közti különbség? Van egyáltalán?
   - CHS korlát 504MB, LBA minden szektor egyedi számot kap. A BIOS a megszakítások paramétereit az átalakított geometriából lemez geometriává alakítja CHS-nél, míg szektor számmá LBA-nál.

#####Mi a Round-Robin címzés lényege?

### Források:
   - előadás diák
   - iNfeRuS4 innen: elte.sharq.hu
