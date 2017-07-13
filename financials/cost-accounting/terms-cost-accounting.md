---
title: "Izmaksu uzskaites terminoloģija"
description: "Šajā tēmā tiek definēti galvenie termini, kas tiek izmantoti Izmaksu uzskaitē."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostControlWorkspace, CAMCostControlWorkspaceConfiguration
audience: Application User
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 223114
ms.assetid: 1c798592-77d0-4a8f-beaa-9159c75957da
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 35b8e510e7e2c13aebb73f46d20b16275d097432
ms.contentlocale: lv-lv
ms.lasthandoff: 06/13/2017


---

# <a name="cost-accounting-terminology"></a>Izmaksu uzskaites terminoloģija

[!include[banner](../includes/banner.md)]


Šajā tēmā tiek definēti galvenie termini, kas tiek izmantoti Izmaksu uzskaitē.

**Izmaksu uzskaite**

Izmaksu uzskaite ļauj jums apkopot datus no dažādiem avotiem, piemēram, virsgrāmata, apakšgrāmata, budžeti un statistiska informācija. Pēc tam jūs varat analizēt, apkopot un novērtēt izmaksu datus, tādējādi vadība var pieņemt vislabākos lēmumus cenas pielāgošanai, budžetiem, izmaksu kontrolei un tā tālāk. Datu avots, kas tiek izmantots izmaksu analīzei, tiek izmantots neatkarīgi Izmaksu uzskaitē. Tāpēc atjauninājumus Izmaksu uzskaitē neietekmē datu avots. Tomēr, apkopojot izmaksu datus no dažādiem avotiem, un jo īpaši, importējot galvenos kontus no Microsoft Dynamics 365 for Finance and Operations izdevuma Enterprise virsgrāmatas kā izmaksu elementus, rodas datu dublēšana, jo tie paši dati pastāv gan Virsgrāmatā, gan Izmaksu uzskaitē. Šāda dublēšana ir nepieciešama, jo jūs izmantojat finanšu pārvaldību ārēju pārskatu veidošanai, un Izmaksu uzskaiti iekšēju pārskatu veidošanai.

**Izmaksu uzskaites virsgrāmata**

Izmaksu uzskaites virsgrāmata ir specializētas struktūra, kas nosaka kā procesi, vērtības un daudzumi tiek ievadīti un uzrādīti konkrētā apgabalā Izmaksu uzskaitē. Izmaksu uzskaites virsgrāmata nosaka procesus un noteikumus izmaksu uz objektu izmaksu novērtēšanai. Tā apstrādā izmaksu darbības un pārvalda dokumentus, kas ieraksta vērtību un daudzumu izmaiņas, ko veido izmaksu darbības.

**Izmaksu ieraksts**

Izmaksu ieraksti ir pārsūtīšanas rezultāts, izmantojot datu savienotājus no virsgrāmatas ierakstiem, izmaksu sadalījumus un grāmatotos izmaksu ierakstus izmaksu žurnālos.

**Izmaksu objekts**

Izmaksu objekti ir jebkura veida objekti, kuriem tiek piešķirtas izmaksas. Daži tipiski izmaksu objekti:

-   Preces
-   Projekti
-   Resursi
-   Nodaļas
-   Izmaksu centri
-   Ģeogrāfiskie reģioni

Vadība izmanto izmaksu objektus, lai aprēķinātu izmaksu daudzumu, kā arī veiktu ienesīguma analīzi.

**Izmaksu elements**

Izmaksu elementus izmanto kā funkciju, lai izsekotu un klasificētu, kur plūst izmaksas. Ir divu veidu izmaksu elementi: primārās izmaksas un sekundārās izmaksas. **Primārās izmaksas** Primāro izmaksu elementi pārstāv izmaksu plūsmu no finanšu uzskaites uz izmaksu uzskaiti. Izmaksu elementu struktūra atbilst peļņas un zaudējumu konta struktūrai virsgrāmatā, kur izmaksu elements var atbilst galvenajam kontam. Ne visi galvenie konti vienmēr var tikt pārstāvēti kā izmaksu elementi atkarībā no biznesa vajadzībām. Daži primāro izmaksu elementu piemēri:

-   Pārdoto preču pašizmaksa
-   Netiešās materiālu izmaksas
-   Personāla izmaksas
-   Enerģijas izmaksas

**Sekundāro izmaksu elements** 

Sekundāro izmaksu elementi, kas pārstāv plūsmas izmaksas iekšēji, jo šīs izmaksas tiek izveidotas un izmantotas tikai Izmaksu uzskaitē. Sekundārās izmaksas elementi palīdz garantēt, ka izmaksu avotu var izsekot. Šos izmaksu elementus izmanto izmaksu sadalījumos un pieskaitāmo izmaksu aprēķinos. Daži sekundāro izmaksu elementu piemēri:

-   Ražošanas izmaksas
-   Ražošanas, materiālu un mārketinga pieskaitāmās izmaksas

**Izmaksu vadības ierīce**

Izmaksu kontroles vienība atspoguļo izmaksu struktūru. Tai jābūt saistītai ar izmaksu objektu dimensijām izmaksu uzskaitē virsgrāmatā.

**Versija**

Versijas tiek izmantotas, lai simulētu, skatītu un salīdzinātu dažādus rezultātus. Pēc noklusējuma visas faktiskās izmaksas tiek skatītas vienu bāzes versijā, kas ir pazīstama kā *faktiskā*. Budžetiem un aprēķiniem jūs varat strādāt ar tik versijām, cik nepieciešams. Piemēram, budžeta datus var importēt sākotnējā versijā, un pēc tam pārskatīt budžetu pārskatītajā versijā. Aprēķiniem jūs varat izveidot vairākas versijas. Šajās dažādajās versijās, pēc tam var izveidot aprēķinus, izmantojot dažādus aprēķina noteikumus, kas tiks izmantoti izmaksu sadalījumam.

**Izraksts**

Izraksti ir skati vadītājiem, kas atbild par izmaksu kontroli. Izrakstus definē izmaksu kontrolieris, un tie sniedz ātru pārskatu par faktiskajām un budžeta izmaksām, un pat novirzes un aprēķinu versijas. Lai palīdzētu nodrošināt vadītājiem skatīt tikai tos datus, par kuriem tie atskaitās, dati, kas parādās izrakstos tiek pakļauti piekļuves noteikumiem.

**Datu savienotājs**

Datus var importēt Izmaksu uzskaitē no ārējām sistēmām, izmantojot datu savienotājus. Piemēram, jūs varat importēt kontu struktūras, dimensijas, virsgrāmatas ierakstus un budžeta ierakstus. Jūs varat izmantot iepriekš konfigurētus datu savienotājus vai pielāgotus savienotājus, lai importētu datus un veidotu datu savienojumus.

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

**Pieskaitāmās izmaksas**

Pieskaitāmās izmaksas attiecas uz esošajiem saimnieciskās darbības izdevumiem. Tās ir izmaksas, kuras nevar tieši saistīt ar konkrētu biznesa aktivitāti. Šeit norādītas dažas pieskaitāmās izmaksas:

-   Uzskaites maksas
-   Nolietojums
-   Apdrošināšana
-   Intereses
-   Juridisko pakalpojumu izdevumi
-   Nodokļi
-   Komunālo pakalpojumu izmaksas

**Izmaksu sadalījums**

Izmaksu sadalījums ir izmaksu piešķiršanas un sadales process, pamatojoties uz kopējo izmaksu cēloņiem. Jūs piešķirat izmaksu summas un daudzumus no viena izmaksu objekta, vienam vai vairākiem citiem izmaksu objektiem. Piemēram, visas iestādes pakalpojumu izmaksas tiek sadalītas dažādās nodaļās, kas izmanto kopējo biroja ēku.

**Izmaksu sadalījuma politika**

Izmaksu sadalījuma politika definē summas un daudzumus, kas tiek sadalīti. Sadalījuma noteikumi ietver sadalījuma avota noteikumus, kas nosaka izmaksas, kas tiek sadalītas, kā arī sadalījuma mērķu kārtulas, kas nosaka, kur tiek sadalītas izmaksas. Piemēram, visas izmaksas iestādes pakalpojumiem ir sadalījuma avots, kas var tikt sadalīts dažādās nodaļās organizācijā (t.i., sadalījuma mērķiem).

**Sadalījuma pamats**

Sadalījuma pamats ir bāze, ko var izmantot, lai mērītu un noteiktu darbību daudzumu, piemēram, mašīnstundas, kas tiek izmantotas, kilovatstundas, kas tiek patērētas, tiešā darba stundas, kas tiek patērētas vai kvadrātpēdas, kas tiek aizņemtas. Tas tiek izmantots, lai sadalītu izmaksas vienam vai vairākiem izmaksu objektiem.

**Sadalījuma princips**

Viens no sadalījuma principiem ir sadalīt izmaksas pēc izmaksu likmes. Jūs varat sadalīt izmaksas, izmantojot faktisko perioda vai vēsturisko likmi. Sadalījums, kas izmanto savstarpēju metodi palīdz nodrošināt, ka sadalījuma pamats tiek noteikts ar vienlaicīgu vienādojumu sēriju pirms tiek veikts sadalījums, izmantojot faktisko perioda likmi.

**Izmaksu apkopojums**

Izmaksu apkopojuma mērķis ir iekļaut visas izmaksas noteiktā izmaksu objektā. Apkopojuma līmenis ir lietotāja definēts. Lietojot izmaksu apkopojumu, jūs varat apkopot izmaksas, kas jāpiešķir no viena izmaksu objekta citam. Ja netiek izmantots izmaksu apkopojums, katrs izmaksu elements tiek piešķirts no viena izmaksu objekta uz citu.

**Izmaksu likmju politika**

Izmaksu likme tiek izmantota, lai aprēķinātu cenu katram izmaksu objektam. Lai izprastu cenu elementus, nepieciešams definēt izmaksu likmes nosacījumus. Ir divu veidu izmaksu likme: vēsturiskā izmaksu likme un plānotā izmaksu likme. Vēsturiskā izmaksu likme ir aprēķinātā likme, kas tiek izmantota kā sadalījuma pamata reizinātājs izmaksu objektam. Likme tiek aprēķināta, pamatojoties uz izmaksu sadalījumiem iepriekšējā periodā. Plānotā likme ir lietotāja definēta likme.

**Dimensiju hierarhija**

Dimensiju hierarhijas tiek izmantotas kā pārskata struktūras, definējot kārtulas sadalījumam, izmaksu likmei un izmaksu apkopojumam, skatot izrakstus vai datus programmā Microsoft Excel, definējot piekļuves tiesības apkopotajiem datiem. Ir divu veidu dimensiju hierarhijas: kategorizēšanas hierarhija un klasifikācijas hierarhija. Kategorizēšanas hierarhija tiek definēta, balstoties uz izmaksu elementiem, bet klasifikācijas hierarhija tiek definēta, balstoties uz izmaksu objektiem.

**Statistiskā dimensija**

Statistikas dimensija ir objekta skaita vai summas izteiksme, ko var izmantot kā pamatu sadalījumiem vai izmaksu likmes aprēķiniem. Tas tiek izveidota manuāli vai importēta no avota sistēmām. Statistikas dimensiju piemēri ir darbinieku skaits, licencētas programmatūras skaits katrā ierīcē, katras ierīces enerģijas patēriņš vai kvadrātmetri izmaksu centram.

**Statistikas ieraksts**

Statistikas ieraksti aiztur ierakstīto summu vai skaitu noteiktai statistikas dimensijas vērtībai. Ierakstītā summa vai skaita vērtība tiek dēvēta arī par lielumu.




