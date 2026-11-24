# Improved Siegeengines

**Verzió**: 1.0.29

Az alapjátékban az MI ostromgépei elpazarolják magukat: a katapultok egészen a falig gurulnak ahelyett, hogy távolról lőnék, hosszú játékokban az ostromsátrak egyre messzebb kerülnek, míg a hajítógépek már semmit nem érnek el, az ostromtornyok megfelelő falra várva ácsorognak, a pajzsok pedig szarvasokat kergetnek. Ez a modul mindegyiket kijavítja.

Minden alábbi elem külön ki- és bekapcsolható. Az MI ostromgépeit módosítja, kivéve az ostromtornyok kikötését és utasait, valamint az olajos mérnököket, amelyek a játékosnak is segítenek.

## Mit tud a modul

**A katapultok és hajítógépek maguk választanak célpontot.** Az MI katapultja vagy hajítógépe teljes lőtávján belül körülnéz a legközelebbi ellenséges fal, torony vagy kapuház után, és helyből lövi. Polgári épületekre csak akkor lő, ha nincs erődítmény lőtávon belül, és csak akkor gurul közelebb, ha semmi sincs lőtávon belül. (A játék saját keresése egyszerre csak egy irányt nézett és figyelmen kívül hagyta a sérült falakat.)

**Megállás lövéshez útközben.** A játék csak álló helyzetben keres célpontot, így a mozgó MI-katapultok elgurultak minden célpont mellett. Mostantól a mozgó katapult vagy hajítógép időnként körülnéz, és amint ellenséges fal, torony, kapuház vagy épület lőtávba kerül, megáll lőni.

**Tovább a következő ellenfélre.** A katapult vagy hajítógép csak az ostromlott játékosra céloz. Ha az elesett (a lordja meghalt), tétlen állás helyett bármely más lőtávon belüli ellenségre lő.

**Más lőtávon belüli ellenségek.** Ha az ostromlott játékosnak semmije sincs lőtávon belül, más ellenségek falaira és épületeire lő elhaladás helyett. Az ostromlott játékos célpontjai elsőbbséget élveznek, lerombolt épületre pedig sosem céloz.

**Nincs többé romok lövése.** Egy épületre célzó ostromgép (tűzballiszta vagy katapult) az épület megsemmisülése után is lőtte az üres helyet, mert a játék csak az épület számát nézte. Mostantól elengedi a lerombolt célpontot és újat választ, a tűzballiszták is.

**Pontosabb célzás.** Az alapjátékban az MI katapult köve akár 12 mezővel rövidebbre és 6-tal oldalra is csapódhatott. A szórás most feleződik és a célra központosul (beállítható; 100% az eredeti pontosság). A saját gépeid változatlanok.

**Sátorhelyek újrafelhasználása.** Ha az ott építő csapat eltűnt, a hely üres és nincs elég közel ellenséges katona, az MI újra építhet oda sátrat. Az alapjátékban egy hely a meccs végéig foglalt maradt.

**Távolsági sátrak lőtáv alapján.** A katapultok, hajítógépek és tűzballiszták sátrai az ellenséges falaktól, tornyoktól és kapuházaktól 0–10 mezővel (beállítható) a lőtávon belülre kerülnek, így a vár belsejét is elérik.

**A mérnökök mindig bejutnak a sátorba.** Az elzárt sátorbejárat szabad oldalra költözik, és a feladó vagy elakadt mérnököket újra elküldi, közeli tétlen mérnökökkel kiegészítve. A körbefalazott sátor azonnal megkapja a mérnökeit, amint út nyílik.

**Több falhoz kikötő ostromtornyok.** Ha a játék nem talál helyet, a torony sarkával átlós falhoz is kiköt, vagy legfeljebb három mezővel arrébb ugyanazon a falon.

**Az MI ostromtornyai maguk keresnek falat.** Egy tétlen MI-torony a legközelebbi kiköthető ellenséges falhoz megy (100 mezőn belül). Ha nincs ilyen vagy elakad, hatalmas pajzsként kíséri a sereget — járőrök, ostromvédelem, fősereg, véletlen távolsági csoport, végül tartalékok mellett.

**Gyalogosok utaznak ostromtornyokon.** Jelölj ki gyalogosokat és kattints egy saját ostromtornyodra: legfeljebb 9 felmászik, és az íjászok menet közben is lőnek, kikötött torony szintű védelemmel. Útközben nem jelölhetők ki; a toronnyal együtt pusztulnak vagy kikötés után azon maradnak. A toronyra kattintva először az utasok, másodszor a mérnökök szállnak ki. Az MI tornyai 3 mezőn belülről veszik fel saját távolsági egységeiket.

**A pajzsok saját csapataikkal mennek.** Az MI pajzsai egyenletesen oszlanak meg az árokbetemetők, a támadó sereg távolsági ostromgépei (sosem az otthoniak) és a távolsági egységek között. A tartalékok csak utánuk kapnak; ha senki sincs, a pajzs helyben vár.

**Az olajos mérnökök talajra öntenek.** A mérnökök — a tiéid is — csak nyílt talajra öntenek, ahol az olaj égni tud, sosem falra, lépcsőre vagy toronyra. Önállóan csak ilyen talajon álló ellenségre öntenek; alkalmatlan pontra küldve 45 fokon belül a legközelebbi talajra öntenek, vagy „lehetetlen hely” jelzéssel megtartják az olajat.

**Az olaj a mennyisége szerint terül szét.** Egy kondér olaja adott számú mezőt (alapértelmezés szerint 41) fed le a célponttól indulva. Nyílt terepen ez megegyezik az alapjátékkal; szűk átjáróban több egymás utáni kondérként hat. Az éghető épületek (kunyhótól a fegyvertárig, templomig, katedrálisig) akár életerejük egyharmadát elvesztik; a falak, tornyok, kapuházak és vártornyok sértetlenek maradnak.

## Jó tudni

* Többjátékos módban mindenkinek azonos beállításokkal kell használnia ezt a modult.
* A mentésekbe semmi nem kerül.
