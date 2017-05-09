---
title: "Mazumtirdzniecības perifēro ierīču simulators"
description: "Šajā tēmā ir aprakstīts kopā ar programmatūru Microsoft Dynamics 365 for Operations — Retail nodrošinātais perifēro ierīču simulēšanas rīks."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 266544
ms.assetid: 16f31e70-15fc-441e-9727-e6a31c3a48f5
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 42dc414ff2bb6359b47d89c3bd3c510e4258f816
ms.openlocfilehash: b2229466040351d8c2b9494b30b4c928651820b8
ms.lasthandoff: 03/31/2017


---

# <a name="retail-peripheral-simulator"></a>Mazumtirdzniecības perifēro ierīču simulators

[!include[banner](includes/banner.md)]


Šajā tēmā ir aprakstīts kopā ar programmatūru Microsoft Dynamics 365 for Operations — Retail nodrošinātais perifēro ierīču simulēšanas rīks.

<a name="overview"></a>Pārskats
--------

Microsoft Dynamics 365 for Operations — Retail perifēro ierīču simulators ir rīks, kas palīdz veikt mazumtirdzniecības vidēs izmantoto perifēro ierīču iestatīšanu, pārbaudi un problēmu novēršanu. Perifēro ierīču simulatoru var izmantot, lai racionalizētu mazumtirdzniecības perifēro ierīču pārbaudi un noteiktu problēmas, ko ir izraisījuši nepareizi ierīču draiveru iestatījumi vai to darbības traucējumi. Perifēro ierīču simulatorā ir ietverta datorprogramma, kas nodrošina programmatūrā Dynamics 365 for Operations — Retail atbalstīto ierīču virtuālās versijas. Katras virtuālās ierīces sadaļā ir sniegta informācija par ierīces mijiedarbību ar mazumtirdzniecības pārdošanas punktu (POS). To var izmantot arī dažādos POS scenārijos derīgu ievades datu nodrošināšanai. Perifēro ierīču simulators atbalsta POS mijiedarbību ar tālāk norādītajām virtuālajām ierīcēm.

-   **Printeris** — perifēro ierīču simulatorā var tikt parādītas POS printerim konfigurētās kvītis.
-   **Rindu displejs** — varat konfigurēt virtuālu rindu displeju, lai atainotu aktivitāti fiziskā rindu displejā.
-   **Magnētiskās joslas lasītājs (MJL)** — varat nosūtīt simulētus magnētiskās joslas notikumus no perifēro ierīču simulatora uz POS.
-   **Naudas kaste** — varat simulēt fizisku naudas kasti.
-   **2. naudas kaste** — iestatot otru naudas kasti perifēro ierīču simulatorā, varat simulēt scenārijus, kuros vienai POS kases sistēmai ir divas aktīvas darba maiņas.
-   **Skeneris** — perifēro ierīču simulatora atbalstītais virtuālais svītrkoda skeneris var izdot svītrkoda skenēšanas notikumus.
-   **Svari** — virtuāli svari sniedz iespēju simulēt svērto preču mijiedarbību ar POS.
-   **Personas identifikācijas numura (PIN) bloks** — varat simulēt PIN bloka operācijas. **Piezīme.** Ir jāievieš fiziska PIN bloka atbalsts, izmantojot maksājumu savienotāju.
-   **Paraksta ieguve** — perifēro ierīču simulatorā ir ietverta virtuāla paraksta ieguves ierīce, ko varat iestatīt, lai tiktu prasīti paraksti, kuri ir nepieciešami dažiem darījumiem, piemēram, debitora konta maksājumiem.

Varat arī izmantot perifēro ierīču simulatoru, lai simulētu svītrkoda/magnētiskās joslas nolasīšanas ierīces notikumus, kas ir saņemti no svītrkoda skenera un MJL. Virtuālo perifēro ierīču simulators tieši atbalsta objektu ieguldīšanas un saistīšanas punktā Retail POS (OPOS) ierīces.

## <a name="key-scenarios"></a>Galvenie scenāriji
### <a name="troubleshooting"></a>Problēmu novēršana

Varat izmantot perifēro ierīču simulatoru, lai novērstu ar ierīces iestatīšanu saistītas problēmas. Ja jums nav perifēro ierīču simulatora vai otras tādas pašas klases ierīces, var būt grūti noteikt problēmas cēloni. Taču, ja jums ir perifēro ierīču simulators, varat iestatīt virtuālas ierīces un palaist tos pašus koda ceļus un biznesa loģiku, kas tiek izmantoti fiziskajās ierīcēs. Perifēro ierīču simulatorā galvenā atšķirība starp virtuālām un fiziskām ierīcēm ir pakalpojumu objekts jeb ierīces draiveris. Fizisko ierīču pakalpojumu objektu nodrošina ierīces ražotājs. Taču perifēro ierīču simulatorā pakalpojumu objekti tiek nodrošināti programmatūras ietvaros. Ja perifēro ierīču simulators darbojas pareizi un pēc tam, kad aparatūras profilā ierīces nosaukums ir nomainīts uz fiziskās ierīces nosaukumu, ierīce nedarbojas pareizi, varat pieņemt, ka ir radusies ar ražotāja nodrošināto pakalpojumu objektu saistīta problēma.

### <a name="training"></a>Apmācība

Varat izmantot perifēro ierīču simulatoru, lai padarītu kasieru apmācību praktiskāku gadījumā, ja nav pieejama fiziskā aparatūra. Ja perifēro ierīču simulators tiek izmantots apmācības scenārijos, kasieris var efektīvāk mijiedarboties ar POS, veicot tādas ievades darbības kā preces svītrkoda skenēšana un dāvanu kartes nolasīšana un novērojot to, kuras kvītis tiek drukātas noteiktai transakcijai.

### <a name="testing"></a>Testēšana

Varat izmantot perifēro ierīču simulatoru, lai virtuālā vidē pārbaudītu preču svītrkodus, kvīšu formātus un ne tikai, neieviešot fizisku aparatūru. Tā kā nav nepieciešama fiziska aparatūra un aparatūras stacijā vai fiziskā datorā nav jāizvieto POS klients, varat ātrāk pārbaudīt operāciju uzskaites daļā veiktās izmaiņas.

## <a name="set-up-the-peripheral-simulator"></a>Perifēro ierīču simulatora iestatīšana
### <a name="set-up-a-hardware-profile"></a>Aparatūras profila iestatīšana

1.  Lai iestatītu perifēro ierīču simulatoru, pārejiet uz sadaļu **Mazumtirdzniecība un komercija** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **POS profili** &gt; **Aparatūras profili**.
2.  Lai izveidotu jaunu profilu, noklikšķiniet uz **Jauns**.
3.  Ievadiet vērtības laukos **Profila numurs** un **Apraksts**.
4.  Izmantojiet tālāk esošo tabulu, lai iestatītu pārbaudāmās virtuālās ierīces. Tālāk ir sniegts tabulas kolonnu paskaidrojums.
    -   **Ierīce** — šajā kolonnā ir norādīts tās kopsavilkuma cilnes nosaukums, kas ir jāizvērš, lai iestatītu ierīci.
    -   **Ierīces veids** — šajā kolonnā ir norādīta vērtība, kas ir jāatlasa laukā, kura apzīmējumā ir ietverts ierīces nosaukums.
    -   **Ierīces nosaukums** — šajā kolonnā ir norādīta precīza vērtība, kas ir jāievada kā ierīces nosaukums. **Svarīgi!** Šeit norādītie ierīču nosaukumi ir obligāti jāizmanto, jo šie konkrētie nosaukumi tiek izmantoti ierīču adresēšanai aparatūras stacijā. Ja neizmantojat šos konkrētos nosaukumus, ierīci nevar lietot.

    | Ierīce            | Ierīces veids | Ierīces nosaukums              |
    |-------------------|-------------|--------------------------|
    | Printeris           | OPOS        | MockOPOSPrinter          |
    | Rindu displejs      | OPOS        | MockOPOSLineDisplay      |
    | MJL (magnētiskās joslas lasītājs)               | OPOS        | MockOPOSMSR              |
    | Dokumenta sastādītājs            | OPOS        | MockOPOSDrawer1          |
    | 2. naudas kaste           | OPOS        | MockOPOSDrawers          |
    | Skeneris           | OPOS        | MockOPOSScanner          |
    | Mērogs             | OPOS        | MockOPOSScale            |
    | PIN bloks           | OPOS        | MockOPOSPinPad           |
    | Paraksta ieguve | OPOS        | MockOPOSSignatureCapture |

**Piezīme.** Lai simulētu svītrkoda skenera notikumus, kas ir saņemti no svītrkoda/magnētiskās joslas nolasīšanas ierīce un MJL, aparatūras profilā nav jāveic īpaši iestatījumi.

### <a name="assign-the-hardware-profile-to-a-register"></a>Aparatūras profila piešķiršana kases sistēmai

1.  Pēc aparatūras profila izveides pārejiet uz sadaļu **Mazumtirdzniecība un komercija** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **Reģistri**.
2.  Saraksta **POS kases sistēmas** laukā **Kases sistēmas numurs** noklikšķiniet uz saites, kas atbilst kases sistēmai, kurai ir jāizmanto perifēro ierīču simulators.
3.  Noklikšķiniet uz **Rediģēt**.
4.  Sadaļas **Profili** laukā **Aparatūras profils** atlasiet aparatūras profilu, ko izveidojāt virtuālajām perifērajām ierīcēm.
5.  Noklikšķiniet uz **Saglabāt**.

### <a name="synchronize-changes-to-the-channel-database"></a>Izmaiņu sinhronizēšana ar kanālu datu bāzi

1.  Pārejiet uz sadaļu **Mazumtirdzniecība un komercija** &gt; **Mazumtirdzniecības IT** &gt; **Sadales grafiks**.
2.  Atlasiet sadales grafiku **1090**.
3.  Noklikšķiniet uz **Izpildīt tūlīt**, lai sinhronizētu izmaiņas ar POS.

Kad dati ir sinhronizēti, kases sistēmas jaunais aparatūras profils un izmaiņas ir pieejamas kanālu datu bāzē.

## <a name="install-the-peripheral-simulator"></a>Perifēro ierīču simulatora instalēšana
1.  Pārejiet uz sadaļu **Mazumtirdzniecība un komercija** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **POS profili** &gt; **Aparatūras profili**.
2.  Noklikšķiniet uz **Lejupielādēt** un pēc tam noklikšķiniet uz **PeripheralSimulator**. **Piezīme.** Lai varētu lejupielādēt perifēro ierīču simulatoru, vispirms ir jāizslēdz uznirstošo elementu bloķētāji.
3.  Kad lejupielāde ir pabeigta, atveriet mapi **Lejupielādes** un veiciet dubultklikšķi uz faila **VirtualPeripherals.msi**, lai palaistu instalēšanas programmu.
4.  Instalējiet perifēro ierīču simulatoru, izmantojot noklusējuma iestatījumus.

Papildus perifēro ierīču simulatoram ir jāinstalē Monroe Consulting Services vispārīgie vadības objekti. Pretējā gadījumā perifēro ierīču simulators nedarbosies pareizi. Lai lejupielādētu vispārīgos vadības objektus, apmeklējiet vietni <http://monroecs.com/oposccos_current.htm>.

## <a name="using-the-peripheral-simulator"></a>Perifēro ierīču simulatora lietošana
Lai palaistu perifēro ierīču simulatoru, datorā noklikšķiniet uz **Sākt**, ievadiet **Mazumtirdzniecības perifēro ierīču simulators** un atlasiet programmu, kad tā tiek parādīta meklēšanas rezultātos. Pēc perifēro ierīču simulatora palaišanas noklikšķiniet uz ierīces nosaukuma, lai skatītu atbalstītās ierīces. Šīs ierīces tiek norādītas kā cilnes loga kreisajā pusē. Lai skatītu konkrētu ierīci, noklikšķiniet uz šīs ierīces cilnes.

### <a name="line-display-capabilities"></a>Rindu displeja iespējas

Rindu displejs ir pirmā ierīce, kas ir norādīta perifēro ierīču simulatorā. Ja ir konfigurēts virtuālais rindu displejs, tajā tiek rādīti POS transakciju ietvaros skenētie rindas elementi. Kad POS tiek atlasīti norēķini, papildus rindas elementiem displejā tiek parādīta apmaksājamā kopsumma. Tajā tiek parādīta arī nenomaksātā bilance, ja ir ievadīti norēķini, taču transakcijai joprojām ir nenomaksāta bilance. Kad POS netiek lietots, var tikt parādīts ziņojums par to, ka kases aparāts ir aizvērts. Šis ziņojums ir jākonfigurē aparatūras profila kopsavilkuma cilnē **Rindas displejs**.

### <a name="cash-drawer-capabilities"></a>Naudas kastes iespējas

Naudas kaste ir otrā ierīce, kas ir norādīta perifēro ierīču simulatorā. Ja aparatūras profils ir konfigurēts virtuālu naudas kastu lietošanai, POS atver aktīvās darba maiņas naudas kasti, reaģējot uz tādām naudas kastes operācijām kā norēķinu deklarācijas, kā arī lai kasieris varētu izdot vai ielikt kastē skaidru naudu, veicot standarta skaidras naudas transakcijas bez piegādes. Virtuālajām naudas kastēm tiek lietoti apzīmējumi **Galvenā naudas kaste** un **Sekundārā naudas kaste**. Šie apzīmējumi atbilst attiecīgi naudas kastei un 2. naudas kastei aparatūras profilā. Kad naudas kaste ir aizvērta, tiek rādīts aizvērtas naudas kastes attēls un aizvērtās naudas kastes pogas apzīmējums ir **Atvērt naudas kasti**. Ja noklikšķināt uz šīs pogas, attēls tiek aizstāts ar atvērtas naudas kastes attēlu, norādot, ka tagad naudas kaste ir atvērta. Atvērtās naudas kastes pogas apzīmējums ir **Aizvērt naudas kasti**. Vairākas POS operācijas var izraisīt naudas kastes atvēršanu. Vairumu operāciju nevar veikt, ja naudas kaste ir atvērta. Izņēmums ir dažas dienas beigās veicamās procedūras. Ja POS lietotājs saņem kļūdas ziņojumu par to, ka operāciju nevar veikt, kamēr ir atvērta naudas kaste, tad, lai turpinātu, lietotājam ir jāaizver virtuālā vai fiziskā naudas kaste. Ja naudas kaste aparatūras profilā ir atzīmēta kā **Koplietota**, sistēmā pirms operācijas veikšanas netiek pārbaudīts, vai naudas kaste ir aizvērta. Operācija tiek veikta kā parasti pat tad, ja naudas kaste ir atvērta. Šī darbība ir piemērota scenārijiem, kuros naudas kastes lieto vairāki pārdevēji un viens pārdevējs lieto naudas kasti, kamēr cits pārdevējs veic nesaistītus uzdevumus savā POS ierīcē. Naudas kastes izmaiņas nestājas spēkā, līdz tiek slēgta pašreizējā maiņa un atvērta jauna maiņa.

### <a name="msr-capabilities"></a>MJL iespējas

Perifēro ierīču simulators nodrošina visaptverošu MJL operāciju atbalstu darbam OPOS režīmā vai svītrkoda/magnētiskās joslas nolasīšanas ierīces režīmā. OPOS režīmā ir nepieciešams, lai MJL aparatūras profilā būtu konfigurēts kā OPOS ierīce. Svītrkoda/magnētiskās joslas nolasīšanas ierīces režīmā uz operētājsistēmu Microsoft Windows tiek vienkārši sūtīti svītrkoda/magnētiskās joslas nolasīšanas ierīces datu notikumi. Papildus iestatījumu atšķirībām OPOS režīms un svītrkoda/magnētiskās joslas nolasīšanas ierīces režīms atšķiras tālāk norādītajos veidos.

-   POS klientā tiek iespējota OPOS MJL ierīču lietošana dažādos scenārijos, piemēram, kad lojalitātes programmas vai dāvanu kartes ierakstam var izmantot magnētiskās joslas datus.
-   Svītrkoda/magnētiskās joslas nolasīšanas ierīces režīmā perifēro ierīču simulators nodrošina svītrkoda/magnētiskās joslas nolasīšanas ierīces datu sūtīšanu uz lauku, kas ir aktīvs datu nosūtīšanas laikā. Šī darbība līdzinās tai, kas notiek, ievadot datus ar tastatūru. Lai MJL izmantotu kā svītrkoda/magnētiskās joslas nolasīšanas ierīci, lietotājam ir jāpāriet uz programmu Retail Modern POS (MPOS), lai pārliecinātos, ka dati tiek saņemti pareizajā laukā. Tāpēc varat konfigurēt aizkavi, lai lietotājam pietiktu laika pārliecināties, ka dati tiks nosūtīti uz pareizo lauku.

#### <a name="testing-gift-and-payment-card-swipes"></a>Dāvanu karšu un maksājumu karšu nolasīšanas pārbaude

Perifēro ierīču simulatora nodrošinātais virtuālais MJL sniedz iespēju konfigurēt arī konkrētus MJL datus, lai izmēģinātu dāvanu kartes un maksājumu kartes nolasīšanas scenārijus. Lai izveidotu karti, noklikšķiniet uz pluszīmes (**+**) pogas un atlasiet kartes veidu. Pēc tam norādiet kartes numuru vai izsekošanas datus, kas ir jāsūta uz POS, kā arī definētās kartes derīguma termiņa beigu mēnesi un gadu. Laukā **Kartes veids** atlasītā vērtība ir tikai apzīmējums, ko var piesaistīt kartei. Šis apzīmējums atvieglo karšu identificēšanu, kad tās tiek nolasītas perifēro ierīču simulatorā. Varat atlasīt perifēro ierīču simulatorā konfigurētās kartes, izmantojot pa kreisi vērstās bultiņas (**&lt;**) un pa labi vērstās bultiņas (**&gt;**) pogas, kas atrodas virs kartes attēla. Varat rediģēt un dzēst kartes, izmantojot pogas **Rediģēt** un **Dzēst**, kas atrodas blakus pluszīmes (**+**) pogai.

### <a name="pin-pad"></a>PIN bloks

Varat konfigurēt PIN bloka simulatoru, lai simulētu OPOS PIN bloku. Kad POS tiek veikta elektronisko līdzekļu pārskaitījuma (EFT) transakcija un ir nepieciešama PIN ievade, no aparatūras stacijas uz PIN ierīci tiek sūtīts PIN ievades pieprasījums. Lai tas varētu darboties, PIN blokam perifēro ierīču simulatorā ir nepieciešams EFT maksājumu savienotāja atbalsts.

### <a name="printer"></a>Printeris

Virtuālais perifērais printeris nodrošina tikai POS drukāto kvīšu parādīšanu. Ja ar drukāšanas operāciju tiek drukātas vairākas kvītis, varat tās ritināt.

#### <a name="configure-receipt-printing"></a>Kvīts drukāšanas konfigurēšana

1.  Pārejiet uz sadaļu **Mazumtirdzniecība un komercija** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **POS profili** &gt; **Aparatūras profili**.
2.  Atlasiet aparatūras profilu, ko izveidojāt virtuālajām perifērajām ierīcēm.
3.  Kopsavilkuma cilnē **Printeris** noklikšķiniet uz **Rediģēt**.
4.  Laukā **Kvīts profila ID** atlasiet kvīts profilu.
5.  Noklikšķiniet uz **Saglabāt**.

### <a name="scale"></a>Mērogs

Ja POS transakcijai tiek pievienota sverama prece un ir konfigurēti svari, POS izgūst svara datus no svariem. Neatkarīgi no tā, vai lietojat virtuālus vai fiziskus svarus, pirms preces pievienošanas transakcijai ir jānorāda prece vai svars. Pirms sveramas preces pievienošanas transakcijai, pārejiet uz svariem perifēro ierīču simulatorā un izmantojiet pluszīmes (**+**) un mīnuszīmes (**–**) pogas, lai koriģētu svaru, kas ir jāuzrāda svariem. Varat arī tieši ievadīt vajadzīgo svaru laukā **Pašreizējā vērtība**. Varat koriģēt svariem lietotās svara mērvienības, izmantojot pluszīmes (**+**) pogu un pogas **Rediģēt** un **Dzēst**. Tādējādi var norādīt mērvienības, pamatojoties uz svērtajām precēm vai atrašanās vietu, kur tiek lietoti svari.

#### <a name="configure-a-scale-product"></a>Sveramas preces konfigurēšana

1.  Pārejiet uz sadaļu **Mazumtirdzniecība un** **komercija** &gt; **Preces un kategorijas** &gt; **Izpildei nodotās preces pēc kategorijas**.
2.  Atveriet preces ierakstu.
3.  Atlasiet sveramo preci.
4.  Kopsavilkuma cilnē **Mazumtirdzniecība** mainiet opcijas **Mēroga prece** vērtību no **Nē** uz **Jā**.

#### <a name="synchronize-changes-to-the-channel-database"></a>Izmaiņu sinhronizēšana ar kanālu datu bāzi

1.  Pārejiet uz sadaļu **Mazumtirdzniecība un komercija** &gt; **Mazumtirdzniecības IT** &gt; **Sadales grafiks**.
2.  Atlasiet sadales grafiku **1040**.
3.  Noklikšķiniet uz **Izpildīt tūlīt**, lai sinhronizētu izmaiņas ar POS.

Pēc datu sinhronizācijas, kad POS transakcijai tiek pievienota sverama prece, POS tiek saņemti svara dati no svariem.

### <a name="signature-capture"></a>Paraksta ieguve

Virtuālā paraksta ieguves ierīce pieprasa lietotājam parakstīties uz virtuālā paraksta ieguves bloka, ja izmantotajiem norēķiniem ir nepieciešams paraksts. Lietotājs var pieņemt parakstu, lai tas tiktu parādīts POS. Pēc tam kasieris var pieņemt parakstu. Pēc tam paraksts tiek saglabāts kopā ar norēķiniem un kopā ar citiem darbību datiem tiek sinhronizēts ar operāciju uzskaites daļas sistēmu.

#### <a name="set-up-a-tender-to-require-a-signature"></a>Tādu norēķinu iestatīšana, kam ir nepieciešams paraksts

1.  Pārejiet uz sadaļu **Mazumtirdzniecība un komercija** &gt; **Kanāli** &gt; **Mazumtirdzniecības veikali** &gt; **Visi mazumtirdzniecības veikali**.
2.  Atlasiet mazumtirdzniecības veikalu.
3.  Noklikšķiniet uz **Rediģēt**.
4.  Noklikšķiniet uz **Iestatīt** un pēc tam sadaļā **Iestatīt** noklikšķiniet uz **Maksājumu metodes**.
5.  Noklikšķiniet uz **Rediģēt**.
6.  Atlasiet maksājumu metodi, kurai ir nepieciešams paraksts.
7.  Sadaļas **Vispārīgi** apgabalā **Paraksta ieguve** iestatiet opcijas **Lietot paraksta ieguves ierīci** vērtību **Jā**.
8.  Laukā **Paraksta ieguves minimālā summa** ievadiet minimālo summu, kam ir jāaktivizē paraksta ieguve.

#### <a name="synchronize-changes-to-the-channel-database"></a>Izmaiņu sinhronizēšana ar kanālu datu bāzi

1.  Pārejiet uz sadaļu **Mazumtirdzniecība un komercija** &gt; **Mazumtirdzniecības IT** &gt; **Sadales grafiks**.
2.  Atlasiet sadales grafiku **1070**.
3.  Noklikšķiniet uz **Izpildīt tūlīt**, lai sinhronizētu izmaiņas ar POS.

Pēc datu sinhronizācijas, ja tiek lietoti norēķini, kam ir nepieciešams paraksts un summa atbilst paraksta sliekšņvērtībai, POS tiek pieprasīta parakstīšanās uz virtuālās paraksta ieguves ierīces.

## <a name="additional-configuration"></a>Papildu konfigurācija
Varat rediģēt perifēro ierīču simulatora konfigurācijas failu, lai to padarītu piemērotāku scenārijiem, kurus izmēģināt. Konfigurācijas fails ir pieejams šeit: C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Konfigurācijas failā ir definētas mērvienības, kas ir pieejamas pārbaudēm ar svariem, pārbaudēm pieejamie karšu veidi, kā arī svītrkodu veidi. Piemēram, modificējot teksta vērtības konfigurācijas failā, varat pievienot jaunu kartes veidu vai mērvienību, ko var atlasīt izpildes laikā. Jaunās vērtības tiek parādītas pēc programmas restartēšanas.

## <a name="troubleshooting"></a>Problēmu novēršana
Perifēro ierīču simulatorā tiek reģistrētas perifēro ierīču simulatora aktivitātes. Žurnāls ir pieejams šeit: C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Perifēro ierīču simulators nodrošina arī problēmu reģistrēšanu Windows notikumu žurnālā, kam var piekļūt sadaļā **Lietojumprogrammu un pakalpojumu žurnāli** &gt; **Microsoft** &gt; **DynamicsAX**. Ja veiktās aparatūras profila izmaiņa nav redzamas, kad lietojat MPOS vai perifēro ierīču simulatoru, pārbaudiet sadales plānotāja darbus, ko izmantojāt datu sinhronizācijai ar kanālu datu bāzi. Ja izmaiņas ir sinhronizētas, taču joprojām nav redzamas POS, restartējiet POS klientu. Konfigurēto naudas kastu izmaiņas nestājas spēkā, līdz tiek izveidota jauna darba maiņa. Tāpēc, ja veicat naudas kastu izmaiņas, vienmēr slēdziet pašreizējo darba maiņu, lai pārbaudītu jaunos naudas kastes iestatījumus. Dažreiz, ja ražotāja draiveris tiek instalēts pēc Monroe Consulting Services vispārīgie vadības objektiem, draiveris var izraisīt vispārīgo vadības objektu darbības traucējumus. Šādā gadījumā ir atkāroti jāinstalē vispārīgie vadības objekti.

<a name="see-also"></a>Skatiet arī
--------

[Pārskats par mazumtirdzniecības perifērajām ierīcēm](retail-peripherals-overview.md)




