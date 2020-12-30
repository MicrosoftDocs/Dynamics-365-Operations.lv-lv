---
title: Izmaksu uzskaites terminoloģija
description: Šajā tēmā tiek definēti galvenie termini, kas tiek izmantoti Izmaksu uzskaitē.
author: ShylaThompson
manager: AnnBe
ms.date: 08/31/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostAccountingLedger
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 223114
ms.assetid: 1c798592-77d0-4a8f-beaa-9159c75957da
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 948beb7baa19c69530dca52b5d4c119b69f8f011
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445720"
---
# <a name="cost-accounting-terminology"></a>Izmaksu uzskaites terminoloģija

[!include [banner](../includes/banner.md)]

Šajā tēmā tiek definēti galvenie termini, kas tiek izmantoti Izmaksu uzskaitē.

**Sadalījuma pamats**

Sadalījuma pamats tiek izmantots, lai mērītu aktivitātes, piemēram, izmantotās mašīnstundas, patērētās kilovatstundas (kWh) vai aizņemto platību, un lai noteiktu šo aktivitāšu daudzumu. Tas tiek izmantots kā bāze izmaksu sadalīšanai vienam vai vairākiem izmaksu objektiem

**Izmaksu uzskaite**

Izmaksu uzskaite ļauj jums apkopot datus no dažādiem avotiem, piemēram, virsgrāmata, apakšgrāmata, budžeti un statistiska informācija. Pēc tam jūs varat analizēt, apkopot un novērtēt izmaksu datus, tādējādi vadība var pieņemt vislabākos lēmumus cenas pielāgošanai, budžetiem, izmaksu kontrolei un tā tālāk. Datu avots, kas tiek izmantots izmaksu analīzei, tiek izmantots neatkarīgi Izmaksu uzskaitē. Tāpēc atjauninājumus Izmaksu uzskaitē neietekmē datu avots. Tomēr, apkopojot izmaksu datus no dažādiem avotiem, un jo īpaši, importējot galvenos kontus no virsgrāmatas kā izmaksu elementus, rodas datu dublēšana, jo tie paši dati pastāv gan Virsgrāmatā, gan Izmaksu uzskaitē. Šāda dublēšana ir nepieciešama, jo jūs izmantojat finanšu pārvaldību ārēju pārskatu veidošanai, un Izmaksu uzskaiti iekšēju pārskatu veidošanai.

**Izmaksu uzskaites virsgrāmata**

To nosaka pēc kalendāra, valūtas un izmaksu elementa dimensijas, un tā kontrolē procesus un politikas izmaksu mērīšanai. 

**Izmaksu ieraksts**

Izmaksu ieraksti ir pārsūtīšanas rezultāts, izmantojot datu savienotājus no virsgrāmatas ierakstiem, izmaksu sadalījumus un grāmatotos izmaksu ierakstus izmaksu žurnālos.

**Izmaksu objekts**

Jebkura tipa objekts, kas ir atlasīts izmaksu kontrolei. Izmaksas vai ieņēmumi tiek grāmatoti tieši vai piešķirti izmaksu objektiem. Tālāk ir uzskaitīti daži tipiskie izmaksu objekti.

-  Preces
-  Projekti
-  Nodaļas
-  Izmaksu centri

Vadība izmanto izmaksu objektus, lai aprēķinātu izmaksu daudzumu, kā arī veiktu ienesīguma analīzi.

**Izmaksu elements**

Lietots kā funkcija izmaksu izsekošanai un kategorizēšanai. Ir divi izmaksu elementu tipi: primārais un sekundārais.

Primārie izmaksu elementi pārstāv izmaksu plūsmu no finanšu uzskaites uz izmaksu uzskaiti. Šī struktūra parasti atbilst peļņas un zaudējumu konta struktūrai virsgrāmatā, kur izmaksu elements var atbilst galvenajam kontam. Ne visi galvenie konti vienmēr var tikt pārstāvēti kā izmaksu elementi atkarībā no biznesa vajadzībām. 

Sekundārie izmaksu elementi pārstāv iekšējo izmaksu plūsmu, jo šīs izmaksas tiek izmantotas tikai izmaksu uzskaitē. Tie tiek izmantoti izmaksu apkopojumu kārtulās, lai izmaksas apkopotu saprotamos intervālos, kurus izmanto pieskaitāmo izmaksu aprēķināšanai. 

**Izmaksu klasifikācija**

Izmaksu klasifikācijas grupu izmaksas atbilstoši to koplietojamajām iezīmēm. Piemēram, izmaksas var grupēt pēc elementiem, izsekojamības un uzvedības.

-   **Pēc elementiem** – materiāli, darbaspēks un izdevumi.
-   **Pēc izsekojamības** – tiešās un netiešās izmaksas. Tiešās izmaksas tiek piešķirtas tieši izmaksu objektiem. Netiešās izmaksas nav tieši izsekojamas izmaksu objektiem. Netiešās izmaksas ir sadalītas izmaksu objektiem.
-   **Pēc uzvedības** – fiksēts, mainīgs un daļēji mainīgs.

**Izmaksu izturēšanās**

Izmaksu darbību klasificē izmaksas atbilstoši to uzvedībai saistībā ar galvenajām biznesa aktivitāšu izmaiņām. Lai efektīvi kontrolētu izmaksas, vadībai jāsaprot izmaksu uzvedību. Pastāv trīs veidu izmaksu uzvedības modeļi: fiksēts, mainīgs un daļēji mainīgs.

- **Fiksētās izmaksas** — fiksētās izmaksas ir izmaksas, kas neatšķiras īstermiņā neatkarīgi no izmaiņām aktivitātes līmenī. Fiksētas izmaksas var būt, piemēram, biznesa pamata saimnieciskās darbības izdevumi, piemēram, noma, ka netiks ietekmēta pat tad, ja aktivitātes līmenis palielinās vai samazinās.

- **Mainīgās izmaksas** — mainīgās izmaksas mainās atbilstoši aktivitātes līmeņa izmaiņām. Piemēram, noteiktu tiešo materiālu izmaksas ir saistītas ar katru pārdoto preci. Jo vairāk preču tiek pārdots, jo vairāk ir tiešo materiālu izmaksu.

- **Daļēji mainīgās izmaksas** — daļēji mainīgās izmaksas ir daļēji fiksētas un daļēji mainīgas izmaksas. Piemēram, interneta piekļuves maksa ietver standarta mēneša piekļuves maksu un platjoslas lietošanas maksu. Standarta mēneša piekļuves maksa ir fiksēta izmaksa, bet platjoslas lietošanas maksa ir mainīga izmaksa.

**Izmaksu vadības ierīce**

Izmaksu vadības ierīce atspoguļo izmaksu struktūru. Šī struktūra nosaka, kā izmaksas hierarhiskā secībā plūst starp izmaksu objektu dimensijām un to attiecīgajiem izmaksu objektiem. 

**Izmaksu sadale**

Tiek izmantota, lai izmaksas no viena izmaksu objekta sadalītu uz vienu vai vairākiem citiem izmaksu objektiem, lietojot atbilstošu sadalījuma pamatu. Izmaksu sadale no izmaksu sadalījuma atšķiras ar to, ka izmaksu sadale vienmēr notiek sākotnējo izmaksu primārā izmaksu elementa līmenī, bez savstarpējās apstrādes.

**Izmaksu sadalījums**

Tiek izmantots, lai izmaksu objekta bilanci piešķirtu citiem izmaksu objektiem, lietojot sadalījuma pamatu. Finance atbalsta savstarpējā sadalījuma metodi. Savstarpējā sadalījuma metodē tiek pilnīgi atpazīti savstarpējie pakalpojumi, ar kuriem izmaksu objekti apmainās. Sistēma automātiski nosaka secību, kādā veikt sadalījumus un veikt tās iterāciju. Izmaksu objekta bilance tiek sadalīta pēc viena sadalījuma pamata. Tiek atbalstīti sadalījumi dažādās izmaksu objektu dimensijās un to attiecīgajos elementos. Sadalījuma secību kontrolē izmaksu kontroles vienība.

**Izmaksu sadalījuma politika**

Izmaksu sadalījuma politika definē summas un daudzumus, kas tiek sadalīti. Sadalījuma noteikumi ietver sadalījuma avota noteikumus, kas nosaka izmaksas, kas tiek sadalītas, kā arī sadalījuma mērķu kārtulas, kas nosaka, kur tiek sadalītas izmaksas. Piemēram, visas izmaksas iestādes pakalpojumiem ir sadalījuma avots, kas var tikt sadalīts dažādās nodaļās organizācijā (t.i., sadalījuma mērķiem).

**Izmaksu apkopojums**

Izmaksu apkopojuma kārtulu mērķis ir izmaksas apkopot saprotamos intervālos. Apkopojuma līmeni definē lietotājs, un tas ietver sekundāra izmaksu elementa piešķiršanu. Ja izmaksu apkopojums netiek lietots, katrs izmaksu elements tiek piešķirts no viena izmaksu objekta citam

**Izmaksu likmju politika**

Izmaksu likme tiek izmantota, lai aprēķinātu cenu katram izmaksu objektam. Lai izprastu cenu elementus, nepieciešams definēt izmaksu likmes nosacījumus. Ir divu veidu izmaksu likme: vēsturiskā izmaksu likme un plānotā izmaksu likme. Vēsturiskā izmaksu likme ir aprēķinātā likme, kas tiek izmantota kā sadalījuma pamata reizinātājs izmaksu objektam. Likme tiek aprēķināta, pamatojoties uz izmaksu sadalījumiem iepriekšējā periodā. Plānotā likme ir lietotāja definēta likme.

**Dimensiju hierarhija**

Ir divu veidu dimensiju hierarhijas: kategorizēšanas hierarhija un klasifikācijas hierarhija. Dimensiju kategorizācijas hierarhijas tips tiek izmantots pārskatu veidošanai. Tas atbalsta tikai izmaksu elementu dimensijas. Dimensiju klasifikācijas hierarhijas tips tiek izmantots politiku definēšanai un pārskatu veidošanai. Tas atbalsta visas dimensijas, piemēram, izmaksu objektu, izmaksu elementu un statistiskās dimensijas. 

**Datu savienotājs**

Izmaksu uzskaite atbalsta datu integrēšanu no avota sistēmām, izmantojot datu savienotāju komplektu. Ir pieejami tālāk norādītie datu savienotāji.

-  Importētās transakcijas (iepriekš konfigurētas)
-  Dynamics 365 Finance (iepriekš konfigurētas)
-  Dynamics AX (nepieciešams konfigurēt)

**Piezīme.** Datu savienotājs Importētās transakcijas ir balstīts uz datu elementiem.

**Datu sniedzējs**

Vairums avota sistēmu var sniegt datus, kas atbilst vienam vai vairākiem datu avotiem izmaksu uzskaitē. Lai datus no avota sistēmām saskaņotu ar datu avotu izmaksu uzskaitē, datu sniedzējs ir jākonfigurē. Nākamajā tabulā ir uzskaitīta datu sniedzēju pieejamība atkarībā no datu savienotāja un datu avota.

|  **Datu avoti** |  **Importēto transakciju datu savienotājs** | **Dynamics 365 Finance datu savienotājs**  | **Dynamics AX datu savienotājs**  |
|---|---|---|---|
| Izmaksu elementu dimensiju elementi  |  Jā | Jā  | Jā  |
|  Izmaksu objekta dimensiju elementi |  Jā | Jā  | Jā  |
|  Statiski dimensiju elementi | Jā  | Nav  | Nav  |
|  Virsgrāmata | Jā  | Jā  | Jā  |
|  Budžeta ieraksti  | Jā  | Jā  | Jā  |
|  Statistiskie mēri | Jā  | Jā  | Jā  |

**Formula**

Formulas sadalījuma pamati sniedz iespēju definēt uzlabotas formulas, lai iegūtu vajadzīgos sadalījuma pamatus. Formulas sadalījuma pamatus varat izveidot manuāli. Lai definētu formulu, varat izmantot tālāk norādītos operatorus.

|  **Simboli** | **Teksts**  |
|---|---|
|  ( ) | Iekavas  |
|  < |  Mazāks nekā |
|  > |  Lielāks nekā |
|  + |  Saskaitīšana |
|  – |  Atņemšana |
| *  | Reizināšana  |

Parastie IF priekšraksti netiek atbalstīti. Taču varat izveidot priekšrakstus un pārbaudīt, vai tie ir patiesi.

|  **Izraksta validēšana** | **Rezultāts**  |
|---|---|
|  a > b| Patiess  |
|  a > b |  Aplams |

**Pieskaitāmās izmaksas**

Pieskaitāmās izmaksas attiecas uz esošajiem saimnieciskās darbības izdevumiem. Tās ir izmaksas, kuras nevar tieši saistīt ar konkrētu biznesa aktivitāti. Šeit norādītas dažas pieskaitāmās izmaksas:

-   Uzskaites maksas
-   Nolietojums
-   Apdrošināšana
-   Intereses
-   Juridisko pakalpojumu izdevumi
-   Nodokļi
-   Komunālo pakalpojumu izmaksas

**Pieskaitāmo izmaksu likme**

Likmes tiek definētas pēc izmaksu objekta un izmaksu elementa. Pastāv divu tipu likmes: finanšu perioda un lietotāja norādītas. Finanšu perioda likmes tiek aprēķinātas ar pieskaitāmo izmaksu aprēķinu. Lietotāja norādīto likmi nosaka lietotājs, un to var izmantot, lai pieskaitāmo izmaksu aprēķinā izmaksas starp izmaksu objektiem sadalītu ar iepriekš noteiktu likmi.

**Publicēts**

Ja šī lauka vērtību iestatāt uz Jā, tad pārskatu darbvietā Izmaksu kontrole var skatīt lietotājs, kuram ir piešķirta kāda no tālāk norādītajām lomām.

-  Izmaksu uzskaites pārvaldnieks
-  Izmaksu grāmatvedis
-  Izmaksu grāmatvedības darbinieks
-  Izmaksu objekta kontrolieris

Ja šī lauka vērtība ir iestatīta uz Nē, tad pārskatu darbvietā Izmaksu kontrole var skatīt tikai tie lietotāji, kuriem ir piešķirta kāda no tālāk norādītajām lomām.

-  Izmaksu uzskaites pārvaldnieks
-  Izmaksu grāmatvedis
-  Izmaksu grāmatvedības darbinieks

**Statiskā dimensija**

Statistiskās dimensijas un tās elementus izmanto, lai izmaksu uzskaitē reģistrētu un kontrolētu ierakstus beznaudas vērtībām. Statistiskās dimensijas elementus var izmantot divējādi:

-  Kā sadalījuma pamatu politikās, piemēram, izmaksu sadalē vai izmaksu sadalījumā.
-  Beznaudas patēriņa pārskatu izveidē.

Statistikas dimensija ir aktivitātes skaita vai summas izteiksme, ko var izmantot kā pamatu sadalījumiem vai likmes aprēķiniem. Tas tiek izveidota manuāli vai importēta no avota sistēmām. Statistikas dimensiju piemēri ir darbinieku skaits, licencētas programmatūras skaits katrā ierīcē, katras ierīces enerģijas patēriņš vai kvadrātmetri izmaksu centram.

**Pārskats**

Izraksti ir skati vadītājiem, kas atbild par izmaksu kontroli. Izrakstus definē izmaksu kontrolieris, un tie sniedz ātru apskatu par faktiskajām izmaksām, budžetā paredzētajām izmaksām un novirzēm. Ja nepieciešams, vadītājs var skatīt detalizētāku informāciju. Lai palīdzētu nodrošināt, ka vadītāji redz tikai tos datus, par kuriem viņi atskaitās, dati, kas ir redzami izrakstos, tiek pakļauti piekļuves kārtulām.

**Versija**

Versijas tiek izmantotas, lai simulētu, skatītu un salīdzinātu dažādus rezultātus. Pēc noklusējuma visas faktiskās izmaksas tiek skatītas vienu bāzes versijā, kas ir pazīstama kā *faktiskā*. Budžetiem un aprēķiniem jūs varat strādāt ar tik versijām, cik nepieciešams. Piemēram, budžeta datus var importēt sākotnējā versijā, un pēc tam pārskatīt budžetu pārskatītajā versijā. Aprēķiniem jūs varat izveidot vairākas versijas. Šajās dažādajās versijās, pēc tam var izveidot aprēķinus, izmantojot dažādus aprēķina noteikumus, kas tiks izmantoti izmaksu sadalījumam.


