---
title: "Rindu definīciju šūnu modificēšana"
description: "Šajā rakstā ir paskaidrota informācija, kas ir nepieciešama katrai šūnai finanšu atskaites rindas definīcijā, un paskaidrots, kā šo informāciju ievadīt."
author: RobinARH
manager: AnnBe
ms.date: 2016-03-07 16 - 09 - 06
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: Management Reporter, Core
ms.custom: 58881
ms.assetid: 0af492df-a84e-450c-8045-78ef1211abaf
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 
ms.dyn365.ops.version: 
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: b61364c9055e5c5a63592c7f05551d0c145924b9
ms.lasthandoff: 03/29/2017


---

# <a name="modify-row-definition-cells"></a>Rindu definīciju šūnu modificēšana

Šajā rakstā ir paskaidrota informācija, kas ir nepieciešama katrai šūnai finanšu atskaites rindas definīcijā, un paskaidrots, kā šo informāciju ievadīt. 

# <a name="specify-a-row-code-in-a-row-definition"></a>Rindas koda norādīšana rindas definīcijā

Rindas definīcijā numuri vai etiķetes šūnā **Rindas kods** identificē rindas definīcijas katru rindu. Varat norādīt rindas kodu, lai atsauktos uz datiem aprēķinos un kopsummās.

### <a name="row-code-requirements"></a>Rindas koda prasības

Rindas kods ir nepieciešams visām rindām. Rindas definīcijā varat kombinēt ciparu, burtciparu un neiestatītus (tukšu) rindu kodus. Rindas kods var būt pozitīvs vesels skaitlis (zem 100 000 000) vai aprakstošā etiķete, kas identificē šo rindu. Aprakstošajai etiķetei ir jāatbilst tālāk norādītajām prasībām.

-   Etiķetei jāsākas ar alfabēta rakstzīmi (no a līdz z vai no A līdz Z), un tā var būt jebkura ciparu un burtu kombinācija līdz 16 rakstzīmēm. **Piezīme:** etiķeti var ietvert pasvītrojuma rakstzīmi (\_), bet citas īpašas rakstzīmes nav atļautas.
-   Etiķetē aizliegts izmantot rezervētos vārdus: AND, OR, IF, THEN, ELSE, PERIODS, TO, BASEROW, UNIT, NULL, CPO vai RPO.

Šeit norādīti daži derīgu rindu kodu piemēri:

-   320
-   TL\_NET\_INCOME
-   TL\_NET\_94

### <a name="change-a-row-code-in-a-row-definition"></a>Rindas definīcijas rindas koda maiņa

1.  Atskaišu veidotājā noklikšķiniet uz **Rindas definīcijas** un atveriet modificējamo rindas definīciju.
2.  Atbilstošajā rindā ievadiet jaunu vērtību kolonnas **Rindas kods** šūnā.

### <a name="reset-numeric-row-codes"></a>Ciparu rindu kodu atiestatīšana

1.  Pārskatu veidotājā noklikšķiniet uz **Rindu definīcijas** un atveriet modificējamo rindas definīciju.
2.  Izvēlnē **Rediģēt** noklikšķiniet uz **Pārnumurēt rindas**.
3.  Dialoglodziņā **Pārnumurēt rindas** norādiet jaunās vērtības sākuma rindas kodam un rindu kodu pieauguma solim. Varat atiestatīt ciparu rindu kodus uz vienādi izvietotām vērtībām. Taču atskaišu veidotājs pārnumurē tikai tos rindu kodus, kas sākas ar skaitļiem (piemēram, 130 vai 246). Tas nav Pārnumurēt rindas kodi, kas sākas ar burtiem (piemēram, ienākumu\_93 vai TP0693). **Piezīme.** Kad pārnumurējat rindu kodus, atskaišu veidotājs automātiski atjaunina **TOT** un **CAL** atsauces. Piemēram, ja **TOT** rinda atsaucas uz diapazonu, kas sākas ar rindas kodu 100, un jūs pārnumurējat rindas, sākot ar 90, sākuma **TOT** atsauce tiek mainīta no 100 uz 90.

## <a name="add-a-description"></a>Apraksta pievienošana
Apraksta šūna sniedz pārskata rindas finanšu datu aprakstu, piemēram, "Ieņēmumi" vai "Neto ieņēmumi". Teksts šūnā **Apraksts** tiek parādīts pārskatā tieši tā, kā to ievadāt rindas definīcijā. **Piezīme:** apraksta kolonnas platums pārskatā ir iestatīts kolonnas definīcijā. Ja teksts rindas definīcijā kolonnā **Apraksts** ir garš, pārbaudiet kolonnas **DESC** platumu. Izmantojot dialoglodziņu **Ievietot rindas no** vērtības kolonnā **Apraksts** ir finanšu datu segmentu vērtības vai dimensiju vērtības. Varat ievietot rindas aprakstoša teksta pievienošanai, piemēram, sadaļas virsrakstu vai sadaļas kopsummu, un formatējuma pievienošanai, piemēram, līniju virs kopsummas rindas. Ja pārskatā tiks iekļauts pārskata koks, varat iekļaut papildu tekstu, kas ir definēts pārskata koka pārskatu veidošanas vienībām. Varat arī ierobežot papildu tekstu, lai noteiktu pārskata mērvienību.

### <a name="add-the-description-for-a-line-on-a-report"></a>Pārskata rindas apraksta pievienošana

1.  Pārskatu veidotājā noklikšķiniet uz **Rindu definīcijas** un atveriet modificējamo rindas definīciju.
2.  Atlasiet šūnu **Apraksts** un tad ievadiet pārskata rindas nosaukumu.
3.  Lietojiet formatējumu.

### <a name="add-additional-text-from-a-reporting-tree-in-the-description"></a>Papildu teksta pievienošana aprakstam no pārskata koka

1.  Pārskatu veidotājā noklikšķiniet uz **Rindu definīcijas** un atveriet modificējamo rindas definīciju.
2.  Ievadiet papildu teksta kodu un pārējo tekstu atbilstošajā šūnā **Apraksts**.
3.  Lietojiet formatējumu.

### <a name="limit-the-additional-text-to-a-specific-reporting-unit"></a>Papildu teksta ierobežošana, lai noteiktu pārskata mērvienību

1.  Pārskatu veidotājā noklikšķiniet uz **Rindu definīcijas** un atveriet modificējamo rindas definīciju.
2.  Atrodiet rindu, kurā jāizveido papildu teksts, un tad veiciet dubultklikšķi uz šūnas kolonnā **Saistītās formulas/Rindas/Vienības**.
3.  Atlasiet pārskata koku dialoglodziņa **Pārskata vienību atlase** laukā **Pārskata koks**.
4.  Laukā **Atlasiet ierobežojuma pārskata vienību** izvērsiet vai sakļaujiet pārskata koku un tad atlasiet pārskata vienību.

## <a name="add-a-format-code"></a>Formāta koda pievienošana
Šūnā **Formāta kods** iespējams izvēlēties iepriekš formatētu rindas satura izvēli. Ja šūna **Formāta kods** ir tukša, rinda tiek interpretēta kā rinda informācijai par finanšu datiem. **Piezīme:** ja pārskats satur formatēšanas rindas, kas nav paredzētas summām, bet kas ir saistītas ar summas rindām, kas ir likvidētas (piemēram, sakarā ar nulles bilanci), varat izmantot kolonnu **Saistītās Formulas/Rindas/Vienības**, lai nepieļautu virsraksta un formāta rindu drukāšanu.

### <a name="add-a-format-code-to-a-report-row"></a>Formāta koda pievienošana pārskata rindai

1.  Pārskatu veidotājā noklikšķiniet uz **Rindu definīcijas** un atlasiet modificējamo rindas definīciju.
2.  Veiciet dubultklikšķi uz **Formāta kods** šūnas.
3.  Atlasiet formāta kodu sarakstā. Tabulā ir aprakstīti formātu kodi un to darbība.
    | Formāta kods                   | Formāta koda interpretācija | Darbība|
    |---|---|---|
    | (Nav)                        |                                    | Notīra šūnu **Formāta kods**.                                                                                                                                                                               |
    | TOT                           | KOPĀ                              | Identificē rindu, kas izmanto matemātiskās operācijas kolonnā **Saistītās Formulas/Rindas/Vienības**. Kopsummu satur vienkāršu operatorus, piemēram, **+**vai**-**.                                                      |
    | CAL                           | Aprēķins                        | Identificē rindu, kas izmanto matemātiskās operācijas kolonnā **Saistītās Formulas/Rindas/Vienības**. Aprēķini ietver kompleksu operatoriem, piemēram, **+**, **-**, **\***, **/**, un **tam/ja/cits** apgalvojumiem. |
    | DES                           | apraksts                        | Identificē pārskatā virsraksta rindas vai tukšu rindu.                                                                                                                                                        |
    | LFT RGT CEN                   | Pa kreisi, pa labi, centrā                  | Izlīdzina rindas apraksta tekstu pārskata lapā neatkarīgi no teksta novietojuma kolonnas definīcijā.                                                                                               |
    | CBR                           | Pamata rindas maiņa                    | Identificē rindu, kas iestata kolonnas aprēķinu pamata rindu.                                                                                                                                               |
    | COLUMN                        | Kolonnas atkāpe                       | Sāk jaunu pārskata kolonnu.                                                                                                                                                                             |
    | PAGE                          | Lappuses pārtraukums                         | Sāk jaunu pārskata lapu.                                                                                                                                                                               |
    | ---                           | Vienkāršs pasvītrojums                   | Izvieto vienu līniju zem visām pārskata summas kolonnām.                                                                                                                                                     |
    | ===                           | Dubults pasvītrojums                   | Izvieto divas līnijas zem visām pārskata summas kolonnām.                                                                                                                                                     |
    | LINE1                         | Šaura līnija                          | Izveido vienu šauru līniju pāri lapai.                                                                                                                                                                      |
    | LINE2                         | Bieza līnija                         | Izveido vienu biezu līniju pāri lapai.                                                                                                                                                                     |
    | LINE3                         | Punktēta līnija                        | Izveido vienu punktotu līniju pāri lapai.                                                                                                                                                                    |
    | LINE4                         | Bieza līnija un plāna līnija           | Izveido dubultu līniju pāri lapai. Augšējā līnija ir bieza un apakšējā līnija ir plāna.                                                                                                                       |
    | LINE5                         | Plāna līnija un bieza līnija           | Izveido dubultu līniju pāri lapai. Augšējā līnija ir plāna un apakšējā līnija ir bieza.                                                                                                                       |
    | BXB BXC                       | Ierāmēta rinda                          | Zīmē rāmi ap pārskata rindām, kas sākas ar **BXB** rindu un beidzas ar **BXC** rindu.                                                                                                               |
    | REM                           | Piezīme                             | Identificē rindu, kas ir komentāru rinda un nav jādrukā pārskatā. Piemēram, piezīmju rinda varētu paskaidrot jūsu formatēšanas metodes.                                                            |
    | SORT ASORT SORTDESC ASORTDESC | Kārtot                               | Kārto izdevumus vai ieņēmumus, kārto faktisko vai budžeta novirzes pārskatu pēc lielākās novirzes vai rindu aprakstus kārto alfabētiskā secībā.                                                                   |

## <a name="specify-related-formulasrowsunits"></a>Saistīto formulu/rindu/vienību norādīšana
Šūnai **Saistītās formulas/Rindas/Vienības** ir vairāki pielietojumi. Atkarībā no rindas tipa šūna **Saistītās formulas/Rindas/Vienības** var veikt vienu no šādām funkcijām:

-   Definēt rindas, kas jāpievieno aprēķinā, kad lietojat **TOT** formāta kodu vai **CAL** formāta kodu;
-   Saistīt formatēšanas rindu ar summas rindu, lai formatējums tiek drukāts tikai tad, kad tiek drukāta saistītā summa;
-   Ierobežot rindu, lai noteiktu pārskata mērvienību;
-   Definēt pamata rindu aprēķiniem, kad izmantojat **BASEROW** formāta kodu;
-   Definēt kārtojamās rindas, kad tiek izmantots jebkurš no kārtošanas formātu kodiem.

### <a name="use-a-row-total-in-a-row-definition"></a>Rindu kopsummu izmantošana rindu definīcijās

Izmantojiet rindas kopsummas formulu, lai pieskaitītu vai atņemtu summas, kas norādītas citās rindās. Formula rindas kopsummas izveidošanai var ietvert + un - operatorus, lai kombinētu atsevišķu rindu kodus un diapazonus. Diapazonus apzīmē ar kolu (:). Formula var ietvert ne vairāk kā 1024 rakstzīmes. Šis ir standarta summēšanas formulas piemērs: 400+420+430+450+460LIABILITIES + EQUITY520:546520:546-LIABILITIES

### <a name="components-of-a-row-total-formula"></a>Rindas kopsummas formulas komponenti

Veidojot rindas kopsummas formulu, jāizmanto rindu kodi, lai norādītu, kuras rindas pieskaitīt vai atņemt pašreizējā rindas definīcijā, un jāizmanto operatori, lai norādītu, kā rindas tiek kombinētas. Kopsummu rindas un summu rindas var tikt izmantotas jebkurās kombinācijās. **Piezīme:** visas kopsummu rindas, kas ir diapazonā, tiek izslēgtas. Lai izveidotu gala summu, varat norādīt rindu diapazonu. Ja diapazona pirmā rinda ir kopsummas rinda, šī rinda tiek iekļauta jaunajā kopsummā. Tabulā ir aprakstīts, kā operatori tiek izmantoti rindu kopsummu formulās.

| Operators | Parauga formula | apraksts                                                 |
|----------|-----------------|-------------------------------------------------------------|
| +        | 100+330         | Pievieno summu 100. rindā summai 330. rindā.        |
| :        | 100:330         | Pievieno kopsummas no visām rindām starp 100. rindu un 330. rindu.    |
| -        | 100-330         | Atņem summu 100. rindā no summas 330. rindā. |

### <a name="create-a-row-total"></a>Rindas kopsummas izveide

1.  Pārskatu veidotājā noklikšķiniet uz **Rindu definīcijas** un atveriet modificējamo rindas definīciju.
2.  Veiciet dubultklikšķi uz šūnas **Formāta kods** rindas definīcijā un atlasiet **TOT**.
3.  Šūnā **Saistītās formulas/Rindas/Vienības** ievadiet kopsummas formulu.

### <a name="relate-a-format-row-to-an-amount-row"></a>Formāta rindas sasaistīšana ar summas rindu

Šajā **formāta koda** kolonnu rindu definīcijā, **DES**, **LFT**, **RGT**, **CEN**, **---**, un **===**formātu kodi pielāgotu formatējumu-summa rindu. Lai novērstu formatējuma drukāšanu, kad saistītās summas rindas ir likvidētas (piemēram, ja summas rindās ir nulles vērtības vai nav perioda aktivitātes), formāta rindas ir jāsaista ar atbilstošām summu rindām. Šī funkcionalitāte ir noderīga, ja nevēlaties drukāt galvenes vai formatējumu, kas ir saistīts ar starpsummām, kad periodā nav informācijas. **Piezīme:** varat arī novērst detalizētu summu rindu drukāšanu, noņemot atzīmi no opcijas parādīt rindas bez summām. Šī opcija atrodas pārskata definīcijas cilnē **Iestatījumi**. Pēc noklusējuma transakcijas detalizētās informācijas konti, kuriem ir nulles bilance vai periodā nav aktivitātes, pārskatos tiek likvidēti. Lai parādītu šos transakciju detalizētās informācijas kontus, atzīmējiet izvēles rūtiņu **Parādīt rindas bez summām** pārskata definīcijas cilnē **Iestatījumi**.

### <a name="relate-a-format-row-to-an-amount-row"></a>Formāta rindas sasaistīšana ar summas rindu

1.  Pārskatu veidotājā noklikšķiniet uz **Rindu definīcijas** un atlasiet modificējamo rindas definīciju.
2.  Formatējuma rindas šūnā **Saistītās formulas/Rindas/Vienības** ievadiet likvidējamās summas rindas kodu. **Piezīme:** lai nerādītu summas rindu, rindas bilancei jābūt 0 (nulle). Summas rinda, kurai ir bilance, netiek likvidēta.
3.  Izvēlnē **Fails** noklikšķiniet uz **Saglabāt**.

### <a name="example-of-preventing-printing-of-rows"></a>Rindu drukāšanas aizliegšanas piemērs

Šajā piemērā Māra vēlas novērst virsrakstu un pasvītrojuma zīmju drukāšanu sava pārskata rindai **Kopsumma kasē**, jo nevienā no kases kontiem nebija aktivitātes. Tādēļ rindā 220 (, kā **---**formāta kodu norāda, ir formatēšanas rinda), **saistītās Formulas/rindas/vienības** kamerā, viņa nonāk **250**, kas ir rindas kods summa rindai, kurā viņa grib apspiest. [![RelatedRowsRowDefinition](./media/relatedrowsrowdefinition-1024x144.png)](./media/relatedrowsrowdefinition.png)

## <a name="select-the-base-row-for-a-column-calculation"></a>Pamata rindas atlase kolonnas aprēķinam
Relāciju pārskatā rindas definīcijai piešķiriet vienu vai vairākas pamata rindas, izmantojot formāta kodu **CBR** (pamata rindas maiņa). Tad uz pamata rindu atsaucas, izmantojot kolonnas definīcijas aprēķinu. Šeit norādīti daži tipiski CBR aprēķinu piemēri:

-   procentuālā daļa no kopējiem ieņēmumiem, saistībā ar atsevišķiem ieņēmumu posteņiem,
-   procentuālā daļa no kopējiem izdevumiem, saistībā ar atsevišķiem izdevumu posteņiem,
-   procentuālā daļa no bruto peļņas, saistībā ar nodaļas vai departamenta informāciju.

Rindas definīcijā definēta viena vai vairākas pamata rindas, un tad kolonnas definīcijā tiek noteikta pamata rindas attiecība, kuru iekļaut pārskatā. Kods, kas tiek izmantots kolonnas formulā ir **BASEROW**. Ar **BASEROW** tiek izmantotas šādas pamata matemātiskās darbības: dalīt, reizināt, pieskaitīt vai atņemt. Operācija, kas tiek izmantota visbiežāk, ir dalīt ar **BASEROW**, kur rezultāts tiek parādīts procentos. Kolonnas aprēķini, kas formulā izmanto **BASEROW**, izmanto saistīto pamata rindu kodu rindas definīciju. **CBR** rindām ir šādi rekvizīti:

-   **CBR** rindas pabeigtajā pārskatā netiek drukātas,
-   **CBR** formāta kods un tā saistītās rindas kods ir novietoti virs rindas vai sadaļas, kas parāda saistītos aprēķinus.

Kolonnas definīcijā kolonnas tips **CALC** apzīmē kolonnu, kas norāda uz formulu rindā **Formula**. Šī formula darbojas ar šīs pārskata kolonnas datiem un izmanto Baserow atslēgvārdu, lai balstītu aprēķinus uz rindas formātu kodiem **CBR**. Rindas definīcijā formāta kods **CBR** nosaka pamata rindu kolonnām, kas veic uz pamata rindu balstītus procentu aprēķinus vai reizina katru pārskata rindu ar pamata rindu. Rindas formātā var būt vairāki **CBR** formātu kodi, piemēram, viens neto pārdošanai, viens bruto pārdošanai un viens kopējiem izdevumiem. Parasti **CBR** formāta kodu izmanto, lai aprēķinātu kontu procentuālās daļas, kas tiek salīdzinātas ar rindas kopsummu. Pamata rinda tiek izmantota visos aprēķinus, līdz tiek definēta cita pamata rinda. Ir jādefinē sākuma **CBR** formāta kods un beigu **CBR **formāta kods. Piemēram, lai noteiktu izdevumus procentos no neto pārdošanas apjoma, varat sadalīt katras izdevumu rindas vērtību ar neto pārdošanas rindas vērtību. Šajā gadījumā neto pārdošanas rinda ir pamata rinda. Varat definēt kolonnas definīciju, kas ziņo par pašreizējos un līdzšinējos gada rezultātus, kā arī katra rezultāta procentuālo daļu no pamata vērtības, kā redzams tālākajā piemērā. Sāciet ar detalizētu ienākumu aprēķinu.

### <a name="select-the-base-row-in-a-row-definition-for-a-column-calculation"></a>Pamata rindas atlase kolonnas aprēķinu rindas definīcijā

1.  Pārskatu veidotājā noklikšķiniet uz **Kolonnu definīcijas** un atveriet peļņas un zaudējumu pārskata kolonnas definīciju.
2.  Kolonnu definīcijai pievienojiet jaunu kolonnu, un iestatiet kolonnas tipu **CALC**.
3.  Jaunās kolonnas šūnā **Formula** ievadiet formulu **X/BASEROW**, kur **X** ir **FD** kolonnas tips, kurš jāizsaka procentos.
4.  Veiciet dubultklikšķi uz šūnas **Formāts/Valūtas ignorēšana**.
5.  Dialoglodziņā **Formāta ignorēšana**, kas atrodas sarakstā **Formāta kategorija**, atlasiet **Procenti** un noklikšķiniet uz **Labi**.
6.  Lai saglabātu kolonnas definīciju ar jaunu nosaukumu, izvēlnē **Fails** noklikšķiniet uz **Saglabāt kā**. Pievienot **CBR** uz pašreizējo faila nosaukumu (piemēram, **CUR\_YTD\_CBR**). Šī kolonnas definīcija ir jūsu pamata rindas kolonnas definīcija.
7.  Pārskatu veidotājā noklikšķiniet uz **Rindu definīcijas** un atveriet modificējamo rindas definīciju, izmantojot pamata rindas aprēķinus.
8.  Ievietojiet jaunu rindu virs rindas, kur būtu jāsākas pamata rindas aprēķiniem.
9.  Veiciet dubultklikšķi uz šūnas **Formāta kods** rindas definīcijā un atlasiet **CBR**.
10. Šūnā **Saistītās formulas/Rindas/Vienības** ievadiet bāzes rindas koda numuru.

### <a name="example-of-base-row-calculation"></a>Pamata rindu aprēķina piemērs

Šajā rindas definīcijas piemērā 100. rindā ir parādīts, ka aprēķinu pamata rinda ir 280. rinda. [![Base rindu aprēķina piemērs.](./media/cbrrowdefinition.png)](./media/cbrrowdefinition.png) Šajā kolonnas definīcijas piemērā aprēķiniem tiek izmantots formāta kods **CBR**. Aprēķini kolonnā C dala vērtību pārskata kolonnā B ar vērtību B kolonnas 280. rindā. Formāta ignorēšana kolonnā B drukā aprēķina rezultātu procentos. Līdzīgi, katra kolonnā E norādītā summa, ir D kolonnā norādītā summa, kas izteikta procentos no neto pārdošanas. [![Kolonna definīcijas piemērs.](./media/cbrcolumndefinition2.png)](./media/cbrcolumndefinition2.png) Šajā piemērā ir parādīts pārskats, kuru iespējams ģenerēt, pamatojoties uz iepriekšējiem aprēķiniem. [![Piemērā atskaiti, kas balstīta uz iepriekšējo piemēru aprēķinu.](./media/cbrreport-1024x272.png)](./media/cbrreport.png)

## <a name="select-a-sorting-code-for-a-row-definition"></a>Rindas definīcijas kārtošanas koda atlase
Kārtošanas kodi sakārto kontus vai vērtības, sakārto faktisko vai budžeta novirzes pārskatu pēc lielākās novirzes vai kārto rindu aprakstus alfabētiskā secībā. Pieejami šādi kārtošanas kodi:

-   **SORT** — sakārto atskaiti augošā secībā, pamatojoties uz vērtībām norādītajā kolonnā.
-   **ASORT** — sakārto atskaiti augošā secībā, pamatojoties uz norādītajā kolonnā esošo vērtību absolūtajām vērtībām. Citiem vārdiem sakot, kārtošanas laikā katras vērtības zīme tiek ignorēta. Šis formāta kods sarindo vērtības atbilstoši novirzes lielumam, neatkarīgi no tā, vai novirze ir pozitīva vai negatīva.
-   **SORTDESC** — sakārto atskaiti dilstošā secībā, pamatojoties uz vērtībām norādītajā kolonnā.
-   **ASORTDESC** — sakārto atskaiti dilstošā secībā, pamatojoties uz norādītajā kolonnā esošo vērtību absolūtajām vērtībām.

### <a name="select-a-sorting-code"></a>Kārtošanas koda atlase

1.  Pārskatu veidotājā noklikšķiniet uz **Rindu definīcijas** un atveriet modificējamo rindas definīciju.
2.  Veiciet dubultklikšķi uz šūnas **Formāta kods** un atlasiet kārtošanas kodu.
3.  Šūnā **Saistītās formulas/Rindas/Vienības** norādiet kārtojamo rindu kodu diapazonu. Lai norādītu diapazonu, ievadiet pirmo rindas kodu, kolu (:) un pēdējās rindas kodu. Piemēram, ievadiet **160:490** lai norādītu, ka diapazons ir no 160. rindas līdz 490. rindai.
4.  Šūnā **Kolonnu ierobežojums** ievadiet tās pārskata kolonnas burtu, kas jāizmanto kārtošanai. **Piezīme:** kārtošanas aprēķinā iekļaujiet tikai summu rindas.

### <a name="examples-of-ascending-and-descending-column-values"></a>Augošu un dilstošu kolonnu vērtību piemēri

Šajā piemērā vērtības kolonnā D atskaites tiks sakārtoti augošā secībā 160 490 caur rindām. Turklāt, absolūtās vērtības kolonnā G atskaites būs jākārto dilstošā kārtībā rindām 610 caur 940.

| Rindas kods | Apraksts                                         | Formāta kods | Saistītās formulas/Rindas/Vienības | Parastā bilance | Kolonnas ierobežojumi | Saite uz finanšu dimensijām |
|----------|-----------------------------------------------------|-------------|-----------------------------|----------------|--------------------|------------------------------|
| 100      | Sakārtots pēc mēneša novirzes augošā secībā       | DES         |                             |                |                    |                              |
| 130      |                                                     | SORT        | 160:490                     |                | D                  |                              |
| 160      | Pārdošana                                               |             |                             | K              |                    | 4100                         |
| 190      | Pārdošanas ieņēmumi                                       |             |                             |                |                    | 4110                         |
|          | ...                                                 |             |                             |                |                    |                              |
| 490      | Procentu ienākumi                                     |             |                             | K              |                    | 7000                         |
| 520      |                                                     | DES         |                             |                |                    |                              |
| 550      | Sakārtots līdzšinējās gada absolūtās novirzes dilstošā secībā | DES         |                             |                |                    |                              |
| 580      |                                                     | ASORTDESC   | 610:940                     |                | G                  |                              |
| 610      | Pārdošana                                               |             |                             | K              |                    | 4100                         |
| 640      | Pārdošanas ieņēmumi                                       |             |                             |                |                    | 4110                         |
|          | ...                                                 |             |                             |                |                    |                              |
| 940      | Procentu ienākumi                                     |             |                             | K              |                    | 7000                         |

Šis ir uzģenerētā pārskata piemērs.

**Novirzes analīze (sakārtots pēc novirzes)**

**Pekinas un Atlantas reģioni**

**Septiņi mēneši līdz 2013. gada 31. jūlijam**

**Jūlijā**

**YTD**

**Faktiskais**

**Budžets**

**Novirze**

**Faktiskais**

**Budžets**

**Novirze**

**Sakārtots pēc mēneša novirzes augošā secībā**

PPPI

873,872

236,144

(637,728)

4,864,274

1,590,315

(3,273,959)

Algas

97,624

65,573

(32,051)

653,884

441,664

(212,220)

Pārdošanas atlaides

36,383

24,152

(12,231)

241,562

162,670

(78,892)

Pārdošanas ieņēmumi

10,917

7,246

(3,671)

62,809

48,803

(14,006)

Nomas izdevumi

12,052

9,019

(3,033)

80,444

60,748

(19,696)

Ofisa izdevumi

5,023

3,291

(1,732)

33,420

22,098

(11,322)

Ceļojumu izdevumi

7,656

7,641

(15)

51,062

51,469

407

Pārdošana

1,240,119

410,389

829,730

7,139,288

2,764,549

4,374,739

**Sakārtots līdzšinējās gada absolūtās novirzes dilstošā secībā**

Pārdošana

1,240,119

410,389

829,730

7,139,288

2,764,549

4,374,739

Ceļojumu izdevumi

7,656

7,641

(15)

51,062

51,469

407

Ofisa izdevumi

5,023

3,291

(1,732)

33,420

22,098

(11,322)

Pārdošanas ieņēmumi

10,917

7,246

(3,671)

62,809

48,803

(14,006)

Nomas izdevumi

12,052

9,019

(3,033)

80,444

60,748

(19,696)

Pārdošanas atlaides

36,383

24,152

(12,231)

241,562

162,670

(78,892)

Algas

97,624

65,573

(32,051)

653,884

441,664

(212,220)

PPPI

873,872

236,144

(637,728)

4,864,274

1,590,315

(3,273,959)

## <a name="specify-a-format-override-cell"></a>Formāta ignorēšanas šūnu norādīšana
Šūna **Formāta ignorēšana** norāda formatējumu, kas rindai tiek izmantots pārskata drukāšanai. Šis formatējums ignorē formatējumu, kas norādīts kolonnas definīcijā un pārskata definīcijā. Pēc noklusējuma formatējums, kas tiek norādīts šajās definīcijās, ir valūta. Ja viena pārskata rinda norāda pamatlīdzekļu skaitu, piemēram, ēku skaitu, bet cita rinda norāda šo pamatlīdzekļu vērtību, varat ignorēt valūtas formatējumu un ievadīt skaitlisko formatējumu rindai, kas norāda ēku skaitu. Šī informācija jānorāda dialoglodziņā **Formātā ignorēšana**. Pieejamās opcijas ir atkarīgas no izvēlētās formāta kategorijas. Dialoglodziņa apgabalā **Paraugs** tiek parādīti formātu piemēri. Pieejamas šādas formātu kategorijas:

-   valūtas formatēšana,
-   skaitļu formatēšana,
-   procentu formatēšana,
-   pielāgotā formatēšana.

### <a name="override-cell-formatting"></a>Šūnas formatējuma ignorēšana

1.  Pārskatu veidotājā atveriet modificējamo rindas definīciju.
2.  Rindā, kurā vēlaties ignorēt formātu, veiciet dubultklikšķi uz šūnas kolonnā **Formāta ignorēšana**.
3.  Dialoglodziņā **Formāta ignorēšana** atlasiet formatēšanas opcijas, kuras šai rindai vēlaties izmantot pārskatā.
4.  Noklikšķiniet uz **OK**.

### <a name="currency-formatting"></a>Valūtas formatēšana

Valūtas formatēšana attiecas naudas līdzekļu daudzumu un ietver valūtas simbolu. Pieejamas šādas opcijas

-   **Valūtas simbols** — valūtas simbols pārskatam. Šī vērtība ignorē uzņēmuma informācijas **Reģionālās opcijas** iestatījumu.
-   **Negatīvi skaitļi** — negatīvie skaitļi var būt atzīmēti ar mīnusa zīmi (-), tie var parādīties iekavās vai tie var būt atzīmēti ar trīsstūri (∆).
-   **Decimāldaļas vietas** — ciparu skaits, ko rādīt pēc komata.
-   **Nulles vērtības ignorēšanas teksts** — teksts, kas jāiekļauj pārskatā, ja summa ir 0 (nulle). Šis teksts tiek rādīts apgabala **Paraugs** pēdējā rindā. **Piezīme:** ja drukāšanai nulles vērtības vai neesoša perioda aktivitāte ir likvidēta, šis teksts tiek izlaists.

### <a name="numeric-formatting"></a>Skaitļu formatēšana

Skaitļa formatēšana attiecas jebkuru summu un neietver valūtas simbolu. Pieejamas šādas opcijas

-   **Negatīvi skaitļi** — negatīvie skaitļi var būt atzīmēti ar mīnusa zīmi (-), tie var parādīties iekavās vai tie var būt atzīmēti ar trīsstūri (∆).
-   **Decimāldaļas vietas** — ciparu skaits, ko rādīt pēc komata.
-   **Nulles vērtības ignorēšanas teksts** — teksts, kas jāiekļauj pārskatā, ja summa ir 0 (nulle). Šis teksts tiek rādīts apgabala **Paraugs** pēdējā rindā. **Piezīme:** ja drukāšanai nulles vērtības vai neesoša perioda aktivitāte ir likvidēta, šis teksts tiek izlaists.

### <a name="percentage-formatting"></a>Procentu formatēšana

Procentu formatējums ietver procentu zīmi (%). Pieejamas šādas opcijas

-   **Negatīvi skaitļi** — negatīvie skaitļi var būt atzīmēti ar mīnusa zīmi (-), tie var parādīties iekavās vai tie var būt atzīmēti ar trīsstūri (∆).
-   **Decimāldaļas vietas** — ciparu skaits, ko parādīt pēc komata.
-   **Nulles vērtības ignorēšanas teksts** — teksts, kas jāiekļauj pārskatā, ja summa ir 0 (nulle). Šis teksts tiek rādīts apgabala **Paraugs** pēdējā rindā. **Piezīme:** ja drukāšanai nulles vērtības vai neesoša perioda aktivitāte ir likvidēta, šis teksts tiek izlaists.

### <a name="custom-formatting"></a>Pielāgota formatēšana

Lietojiet pielāgoto formatēšanas kategoriju, lai izveidotu pielāgotu formāta ignorēšanu. Pieejamas šādas opcijas

-   **Tips** — pielāgotais formāts.
-   **Nulles vērtības ignorēšanas teksts** — teksts, kas jāiekļauj pārskatā, ja summa ir 0 (nulle). Šis teksts tiek rādīts apgabala **Paraugs** pēdējā rindā. **Piezīme:** ja drukāšanai nulles vērtības vai neesoša perioda aktivitāte ir likvidēta, šis teksts tiek izlaists.

Tipam jāatspoguļo pozitīva vērtība, un tad negatīva vērtība. Parasti tiek ievadīts līdzīgs formāts, kas atšķir pozitīvas un negatīvas vērtības. Piemēram, lai norādītu, ka gan pozitīvās, gan negatīvās vērtības divām decimāldaļas vietām, bet negatīvās vērtības parādās iekavās, ievadiet **0.00;(0.00)**. Šajā tabulā ir parādīti pielāgotie formāti, kurus varat izmantot, lai kontrolētu savu vērtību formātu. Visi piemēri sākas no vērtības 1234.56.

| Formāts                         | Pozitīvs   | Negatīvs     | Nulle    |
|--------------------------------|------------|--------------|---------|
| 0                              | 1235       | -1235        | 0       |
| 0;0                            | 1235       | 1235         | 0       |
| 0;(0);-                        | 1235       | 1235         | -       |
| \#,\#\#\#;(\#,\#\#\#);“”       | 1,235      | (1,235)      | (Tukšs) |
| \#,\#\#0.00;(\#,\#\#0.00);zero | 1,234.56   | (1,234.56)   | nulle    |
| 0.00%;(0.00%)                  | 123456.00% | (123456.00%) | 0.00%   |

## <a name="specify-a-normal-balance-cell"></a>Parastās bilances šūnas norādīšana
Rindas definīcijas šūna **Parastā bilance** kontrolē rindas summu zīmi. Lai mainītu rindas zīmi vai ja parastā konta bilance ir kredīts, šīs rindas šūnā **Parastā bilance** ievadiet **C**. Atskaišu izstrādes rīks apvērš zīmi visiem kredīta bilances kontiem šajā rindā. Kad atskaišu veidotājs pārveido šos kontus, tas noņem debeta/kredīta raksturlielumu no visām summām un tādējādi vienkāršo summēšanu. Piemēram, lai aprēķinātu neto ienākumus, atņemiet izdevumus no ienākumiem. Parasti uz summēšanas un aprēķinu rindām **C** kodam nav ietekmes. Tomēr **XCR** drukas vadība kolonnas definīcijā maina zīmi jebkurā rindā, kas kolonnā **Parastā bilance** satur kodu **C**. Šis formatējums ir īpaši svarīgs, ja vēlaties parādīt visas nelabvēlīgās novirzes kā negatīvas summas. Ja summētajam vai aprēķinātajam skaitlim ir nepareiza zīme, rindas šūnā **Parastā bilance** ievadiet **C**, kas mainīs zīmi uz pretējo.

## <a name="specify-a-row-modifier-cell"></a>Rindas modifikatora šūnas norādīšana
Rindas definīcijas šūnas **Rindas modifikators** saturs ignorē finanšu gadus, periodus un citu informāciju, kas ir norādīta šīs rindas kolonnas definīcijā. Atlasītais modifikators attiecas uz katru rindas kontu. Varat modificēt katru rindu, izmantojot vienu vai vairākus no šiem modifikatoru veidiem:

-   konta modifikatori,
-   grāmatas koda modifikatori,
-   konta un transakcijas atribūti.

### <a name="override-a-column-definition"></a>Kolonnas definīcijas ignorēšana

1.  Pārskatu veidotājā atveriet modificējamo rindas definīciju.
2.  Rindā, kurā vēlaties ignorēt kolonnas definīciju, veiciet dubultklikšķi uz šūnas **Rindas modifikators**.
3.  Dialoglodziņā **Rindas modifikators** atlasiet opciju laukā **Konta modifikators**. Opciju aprakstu skatiet sadaļā "Konta modifikatori".
4.  Laukā **Grāmatas koda modifikators** atlasiet rindai izmantojamās grāmatas kodu.
5.  Sadaļā **Atribūti** veiciet tālāk minētās darbības, lai pievienotu ierakstu katram atribūtam, kas jāiekļauj rindas kodā.
    1.  Veiciet dubultklikšķi uz šūnas **Atribūts** un atlasiet atribūta nosaukumu. **Brīdinājums:** aizstāt numura zīme (\#) ar skaitlisku vērtību.
    2.  Veiciet dubultklikšķi uz šūnas **No** un ievadiet pirmo diapazona vērtību.
    3.  Veiciet dubultklikšķi uz šūnas **Līdz** un ievadiet pēdējo diapazona vērtību.

6.  Noklikšķiniet uz **OK**.

### <a name="account-modifiers"></a>konta modifikatori,

Kad atlasāt noteiktu kontu, atskaišu veidotājs parasti kombinē kontu un finanšu gadus, periodus un citu informāciju, ko norādāt kolonnas definīcijā. Varat izmantot citu informāciju, piemēram, dažādus finanšu periodus noteiktām rindām. Šajā tabulā parādīti pieejamie kontu modifikatori. Aizstāt numura zīme (\#) ar vērtību, kas ir vienāda ar vai mazāka par periodu skaitu finanšu gadā.

| Konta modifikators | Kas tiek izdrukāts                                                                           |
|------------------|-------------------------------------------------------------------------------------------|
| /BB              | Konta sākuma bilance.                                                     |
| /\#              | Bilance norādītajam periodam.                                                     |
| /-\#             | Bilance par periodu, kas ir \#periodiem pirms pašreizējā periodā.                  |
| /+\#             | Bilance par periodu, kas ir \#periodu pēc perioda.                   |
| /C               | Bilance pašreizējam periodam.                                                       |
| /C-\#            | Bilance par periodu, kas ir \#periodiem pirms pašreizējā periodā.                  |
| /C+\#            | Bilance par periodu, kas ir \#periodu pēc perioda.                   |
| /Y               | Līdzšinējā gada bilance līdz pašreizējam periodam.                                      |
| /Y-\#            | Atlikums gada sākuma līdz konkrētajam datumam cauri periodam, kas ir \#periodiem pirms pašreizējā periodā. |
| /Y+\#            | Atlikums gada sākuma līdz konkrētajam datumam cauri periodam, kas ir \#periodu pēc perioda.  |

### <a name="book-code-modifiers"></a>grāmatas koda modifikatori,

Varat ierobežot rindu ar esošu grāmatas kodu. Kolonnas definīcijā jāiekļauj vismaz viena **FD** kolonna, kurā ir grāmatas kods. **Piezīme:** rindas grāmatas koda ierobežojums ignorē grāmatas koda ierobežojumus, kas norādīti šīs rindas kolonnas definīcijā.

### <a name="account-and-transaction-attributes"></a>konta un transakcijas atribūti.

Dažas grāmatvedības sistēmas atbalsta kontu atribūtus un transakciju atribūtus finanšu datos. Šie atribūti darbojas kā virtuāli kontu segmenti un tie var saturēt papildu informāciju par kontu vai transakciju. Šī papildu informācija var būt konta ID, partijas ID, pasta indeksi vai citi atribūti. Ja jūsu grāmatvedības sistēma atbalsta atribūtus, varat izmantot kontu atribūtus vai transakciju atribūtus par rindu modifikatoriem rindu definīcijās. Informāciju par rindas informācijas ignorēšanu skatiet sadaļā "Kolonnas definīcijas ignorēšana" iepriekš šajā rakstā.

## <a name="specify-a-link-to-financial-dimensions-cell"></a>Saites izveide uz finanšu dimensiju šūnu
Šūna **Saite uz finanšu dimensijām** satur saites uz finanšu datiem, kas ir jāiekļauj katrā pārskata rindā. Šī šūna satur dimensiju vērtības, bet to vietā vai papildus tām jūs varat norādīt šūnas Microsoft Excel darblapā, segmentu vērtības vai dimensiju vērtības. Lai atvērtu dialoglodziņu **Dimensijas**, veiciet dubultklikšķi uz šūnas **Saite uz finanšu dimensijām**. **Piezīme:** atskaišu izstrādes rīks nevar atlasīt kontu, dimensijas vai lauki Microsoft Dynamics ERP sistēma, kas ietver šādas rezervēto rakstzīmes: &, \*, \[, \], {, vai}. Lai norādītu informāciju rindai, kas jau ir rindas definīcijā, pievienojiet informāciju šūnā **Saite uz finanšu dimensijām**. Lai pievienotu jaunas rindas, kurās ir saite uz finanšu datiem, un izveidotu jaunas pārskata definīcijas rindas, izmantojiet dialoglodziņu **Ievietot rindas no**. Kolonnas virsraksts mainās atkarībā no kolonnas konfigurācijas, kā tas parādīts šajā tabulā.

| Atlasītais saites tips       | Saites kolonnas apraksts mainās uz šo |
|----------------------------------|----------------------------------------------------|
| Finanšu dimensijas             | Saite uz finanšu dimensijām                       |
| Ārēja darblapa               | Saite uz darblapu                                  |
| Finanšu dimensijas + darblapa | Saite uz finanšu dimensijām + darblapa           |
| Management Reporter pārskats       | Management Reporter pārskats                         |

### <a name="specify-a-dimension-or-range"></a>Diapazona dimensiju norādīšana

1.  Pārskatu veidotājā atveriet modificējamo rindas definīciju.
2.  Veiciet dubultklikšķi uz šūnas kolonnā **Saite uz finanšu dimensijām**.
3.  Dialoglodziņā **Dimensijas** veiciet dubultklikšķi uz šūnas zem dimensijas nosaukuma.
4.  Dimensijas dialoglodziņā atlasiet **Individuāli vai diapazona**.
5.  Ar **no** lauku, ievadiet sākuma dimensiju, vai noklikšķiniet uz ![pārlūkot](https://i-technet.sec.s-msft.com/dynimg/IC679490.gif "pārlūkot") lai meklētu pieejamās dimensijas. Lai ievadītu dimensiju diapazonu, ievadiet beigu dimensiju laukā **Uz**.
6.  Lai aizvērtu dimensijas dialoglodziņu, noklikšķiniet uz **Labi**. Dialoglodziņā **Dimensijas** attēlota atjauninātā dimensija vai diapazons.
7.  Lai aizvērtu dialoglodziņu **Dimensijas**, noklikšķiniet uz **Labi**.

## <a name="display-zero-balance-accounts-in-a-row-definition"></a>Nulles bilances kontu attēlošana rindas definīcijā
Pēc noklusējuma atskaišu veidotājs nedrukā rindas, kurās finanšu datos nav atbilstošas bilances. Tāpēc varat izveidot vienu rindas definīciju, kas ietver visas fizisko segmentu vērtības vai visas dimensiju vērtības, un tad izmantot to rindas definīcijai jebkurai nodaļai.

### <a name="modify-zero-balance-settings"></a>Nulles bilances iestatījumu modificēšana

1.  Pārskatu veidotājā atveriet modificējamo pārskata definīciju.
2.  Cilnes **Iestatījumi** sadaļā **Citi formatējumi** atlasiet opcijas rindas definīcijai, kas tiek izmantota pārskata definīcijā.
3.  Lai saglabātu izmaiņas, izvēlnē **Fails** noklikšķiniet uz **Saglabāt**.

## <a name="use-wildcard-characters-and-ranges-in-a-row-definition"></a>Aizstājējzīmju un diapazonu izmantošana rindas definīcijā
Ievadot vērtību dabas segmenta **dimensijas** dialoglodziņā varat ievietot aizstājējzīmes rakstzīmi (? Vai \*) kādā stāvoklī segments. Atskaišu izstrādes rīks iegūst visas vērtības, kas definētas pozīcijas, neapsverot aizstājējzīmes. Piemēram, rindas definīcija satur tikai fizisko segmentu vērtības un fiziskajiem segmentiem ir četras rakstzīmes. Ievadot **6?** Pēc kārtas, dot norādījumus atskaišu izstrādes rīks, lai iekļautu visus kontus, kuriem ir dabas segmenta vērtība, kas sākas ar 6. Ja ievadāt **6\***, tādi paši rezultāti tiek atgriezti, bet rezultāti arī ietver mainīgo platumu vērtības, piemēram, **60** un **600000**. Atskaišu veidotājs katru aizstājējzīmi (?) aizstāj ar pilnu iespējamo vērtību klāstu, kas ietver burtus un īpašās rakstzīmes. Piemēram, diapazonā no **12?0** līdz **12?4**, aizstājējzīme virknē **12?0** tiek aizstāta ar zemāko rakstzīmju kopas vērtību un aizstājējzīme virknē **12?4** tiek aizstāta ar augstāko rakstzīmju kopas vērtību. **Piezīme:** jāizvairās no aizstājējzīmju izmantošanas diapazona sākuma un beigu kontos. Ja izmantojat aizstājējzīmes sākuma kontā vai beigu kontā, varat saņemt negaidītus rezultātus.

### <a name="single-segment-or-single-dimension-ranges"></a>Viena segmenta vai vienas dimensijas diapazoni

Varat norādīt segmenta vērtību vai dimensijas vērtību diapazonu. Norādot diapazonu, priekšrocība ir tas, ka nav nepieciešams atjaunināt rindas definīciju katru reizi, kad finanšu datiem tiek pievienota jauna segmenta vērtība vai dimensijas vērtība. Piemēram, diapazonā **+ konta =\[6100:6900\]** iebrauc rindas summa vērtību no kontiem 6100 caur 6900. Kad diapazons ietver aizstājējzīmi (?), atskaišu veidotājs nevērtē diapazonu katrai rakstzīmei. Tā vietā tiek noteikti diapazona zemākā un augstākā vērtība, un tad tiek iekļautas robežvērtības un visas vērtības starp tām. **Piezīme:** atskaišu izstrādes rīks nevar atlasīt kontu, dimensijas vai lauki Microsoft Dynamics ERP sistēma, kas ietver šādas rezervēto rakstzīmes: &, \*, \[, \], {, vai}. Varat pievienot & zīmi tikai tad, kad automātiski veidojat rindu definīcijas, izmantojot dialoglodziņu **Ievietot rindas no dimensijām**.

### <a name="multiple-segment-or-multiple-dimension-ranges"></a>Vairāku segmentu vai vairāku dimensiju diapazoni

Ievadot diapazonu, izmantojot vairāku dimensiju vērtību kombinācijas, diapazons salīdzināšana tiek veikta uz... \financial-dimensions\dimension-by-Dimension pamats. Diapazona salīdzināšanu nevar veikt rakstzīmi pēc rakstzīmes vai daļēji balstoties uz segmentu. Piemēram, diapazonā **+ konta =\[5000:6000\], Department =\[1000:2000\], izmaksu centrs =\[00\]** ietver tikai uzņēmumus, kas atbilst katra segmenta. Šādā gadījumā pirmajai dimensijai jābūt diapazonā no 5000 līdz 6000, otrā dimensija jābūt robežās no 1000 līdz 2000 un pēdējo dimensija jābūt 00. Piemēram, **+ konta =\[5100\], Department =\[1100\], izmaksu centrs =\[01\]** nav iekļauta ziņojumā, jo pēdējais segments ir ārpus norādītā diapazona. Ja segmenta vērtība ir atstarpes, iekļaujiet šo vērtību kvadrātiekavās (\[\]). Šīm vērtībām ir derīgas četrzīmju segments: **\[234\], \[123 \], \[1 34\]**. Dimensiju vērtības ir jāiekļauj kvadrātiekavās (\[\]), un ziņojuma izstrādātājs pievieno šīs iekavas jums. Ja vairāku segmentu vai vairāku dimensiju diapazons ietver aizstājējzīmju rakstzīmes (? Vai \*), kopumā vairāku segmentu vai vairāku dimensiju diapazona zemas un augstas gali tiek noteiktas un tad beigās un visas vērtības starp tām ir iekļauti. Ja jums ir liels diapazons, piemēram, viss kontu diapazons no 40000 līdz 99999, vajadzētu norādīt derīgu sākuma kontu un beigu kontu, ja vien iespējams. **Piezīme:** atskaišu izstrādes rīks nevar atlasīt kontu, dimensijas vai lauki Microsoft Dynamics ERP sistēma, kas ietver šādas rezervēto rakstzīmes: &, \*, \[, \], {, vai}. Varat pievienot & zīmi tikai tad, kad automātiski veidojat rindu definīcijas, izmantojot dialoglodziņu **Ievietot rindas no dimensijām**.

## <a name="add-or-subtract-from-other-accounts-in-a-row-definition"></a>Pieskaitīšana vai atņemšana no citiem kontiem rindas definīcijā
Lai saskaitītu vai atņemtu naudas summas vienā kontā no cita konta naudas summas, šūnā **Saite uz finanšu dimensijām** varat izmantot plus zīmi (+) un mīnus zīmi (-). Šajā tabulā ir parādīti pieņemami formāti finanšu datu saišu pieskaitīšanai un atņemšanai.

| Operācija                                                                               | Izmantojiet šo formātu                                                                                              |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Saskaitiet divus pilnībā derīgus kontus.                                                       | + Rajons =\[000\], konts =\[1205\], departaments =\[00\]+ Division =\[100\], konts =\[1205\], departaments =\[00\] |
| Saskaitiet divas segmenta vērtības.                                                                 | + Konta =\[1205\]+ konta =\[1210\]                                                                           |
| Saskaitiet segmenta vērtības, kas satur aizstājējzīmes.                                    | + Konta =\[120? + konta =\[11?\]                                                                             |
| Sasummējiet pilnībā derīgu kontu diapazonu.                                                | + Rajons =\[000:100\], konts =\[1205\], Department =\[00\]                                                   |
| Summējiet segmenta vērtību diapazonu.                                                          | + Konta =\[1200:1205\]                                                                                       |
| Sasummējiet segmenta vērtību diapazonu, kas satur aizstājējzīmes.                         | + Konta =\[120?: 130?\]                                                                                       |
| Atņemiet vienu pilnībā derīgu kontu no cita pilnībā derīga konta.              | + Rajons =\[000\], konts =\[1205\], departaments =\[00\]-Division =\[100\], konts =\[1205\], departaments =\[00\] |
| Atņemiet viena segmenta vērtību no citas segmenta vērtības.                                  | + Konta =\[1205\]-konta =\[1210\]                                                                           |
| Atņemiet segmenta vērtību, kas ietver aizstājējzīmi, no citas segmenta vērtības. | + Konta =\[1200\]-konta =\[11?\]                                                                           |
| Atņemiet pilnībā derīgu kontu diapazonu.                                           | -Rajons =\[000:100\], konts =\[1200:1205\], Department =\[00:01\]                                           |
| Atņemiet segmenta vērtību diapazonu.                                                     | -Konta =\[1200:1205\]                                                                                       |
| Atņemiet segmenta vērtību diapazonu, kas satur aizstājējzīmes.                    | -Konta =\[120?: 130?\]                                                                                       |

Lai gan kontus varat modificēt nepastarpināti, varat izmantot arī dialoglodziņu **Dimensijas**, lai jūsu finanšu datu saitēm lietotu pareizo formatējumu. Kāda no vērtībām var iekļaut aizstājējzīmes rakstzīmes (? Or \*). Tomēr, atskaišu izstrādes rīks nevar atlasīt kontu, dimensijas vai lauki Microsoft Dynamics ERP sistēma, kas ietver šādas rezervēto rakstzīmes: &, \*, \[, \], {, vai}. **Piezīme:** lai atņemtu vērtības, šīs vērtības ir jāliek iekavās. Piemēram, ja ievadāt **450?-(4509)**, tas tiek parādīts kā **+ konta =\[4509\]-konta =\[450? \]**, un tu esi instruēt atskaišu izstrādes rīks jāatņem summa kontā segmentam 4509 no jebkura konta segmentu, kas sākas ar 450 summa.

### <a name="add-or-subtract-accounts-from-other-accounts"></a>Pieskaitiet vai atņemiet kontus no citiem kontiem

1.  Pārskatu veidotājā atveriet modificējamo rindas definīciju.
2.  Atbilstošajā rindā veiciet dubultklikšķi uz šūnas kolonnā **Saite uz finanšu dimensijām**.
3.  Dialoglodziņa **Dimensijas** pirmajā rindā veiciet tālāk minētās darbības.
    1.  Pirmajā laukā atlasiet visas dimensijas (noklusētās) vai noklikšķiniet, lai atvērtu **Dimensiju kopu pārvaldība** dialoglodziņu, kur varat izveidot, modificēt, kopēt vai dzēst kopu.
    2.  Veiciet dubultklikšķi uz **operators + /-** šūnas un atlasiet plus (**+**) vai mīnusa (**-**) operators, ko lieto vienu vai vairākas dimensijas vērtībām vai iestata rindas.
    3.  Atbilstošajā dimensijas vērtību kolonnā veiciet dubultklikšķi uz šūnas, lai atvērtu dialoglodziņu **Dimensijas**, un atlasiet, vai šī dimensijas vērtība ir atsevišķa vai diapazons, dimensijas vērtību kopa vai summēšanas konti. Dialoglodziņa **Dimensijas** lauku aprakstus skatiet sadaļā "Dialoglodziņa Dimensijas apraksts".
    4.  Ievadiet segmenta vērtības kolonnā **No** un kolonnā **Līdz**.

4.  Atkārtojiet 2. līdz 3. soli, lai pievienotu vairāk operāciju.

**Piezīme:** operators attiecas uz visām rindas dimensijām.

## <a name="description-of-the-dimensions-dialog-box"></a>Dialoglodziņa Dimensijas apraksts
Tabulā ir aprakstīti dialoglodziņa **Dimensijas** lauki.

| Krājums                | Apraksts                                                                                                                                                                                                                                                                                             |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Individuāls vai diapazons | Ar **no** lauku, ievadiet konta nosaukumu, vai noklikšķiniet uz **pārlūkot** pogu ![pārlūkot](https://i-technet.sec.s-msft.com/dynimg/IC679490.gif "pārlūkot") pārlūkot konta. Lai atlasītu diapazonu, ievadiet vai uzmeklējiet vērtību laukā **Līdz**.                                             |
| Dimensijas vērtību kopa | Laukā **Nosaukums** ievadiet dimensijas vērtību kopas nosaukumu. Lai kopu izveidotu, modificētu, kopētu vai dzēstu, noklikšķiniet uz **Pārvaldīt dimensiju vērtību kopas**. **Formula** lauks tiek aizpildīts ar formulu no **saite uz finanšu dimensijas** šūnu šo dimensijas vērtību noteikt rindu definīcijā. |
| Summēšanas konti   | Laukā **Nosaukums** ievadiet vai uzmeklējiet dimensiju summēšanas kontiem. Lauks **Formula** šim summēšanas kontam pārskata definīcijā tiek aizpildīts ar formulu no šūnas **Saite uz finanšu dimensijām**.                                                                       |

## <a name="add-dimension-value-sets-in-a-row-definition"></a>Pievienojiet rindas definīcijai dimensijas vērtību kopu
Dimensiju vērtību kopa ir dimensiju vērtību grupa, kurai piešķirts nosaukums. Dimensiju vērtību kopa var saturēt tikai vienas dimensijas vērtības, bet varat izmantot dimensiju vērtību kopu vairākās rindu definīcijās, kolonnu definīcijās, pārskatu veidošanas koku definīcijās un pārskatu definīcijās. Pārskata definīcijā varat arī kombinēt vairākas dimensiju vērtību kopas. Kad finanšu datu izmaiņas pieprasa mainīt dimensiju vērtību kopu, varat atjaunināt dimensijas vērtību kopas definīciju un šī atjaunināšana attieksies uz visiem apgabaliem, kuros dimensiju vērtību kopa ir izmantota. Piemēram, ja bieži norādāt vērtību diapazonu, lai veidotu saiti uz finanšu datiem, piemēram, vērtības no 5100 līdz 5600, varat piešķirt šo diapazonu konta kopai ar nosaukumu Pārdošana. Pēc dimensiju vērtību kopu izveides varat atlasīt vai iestatīta kā finanšu datu saiti. Cits piemērs, ja 5100 caur 5600 vērtību diapazons tiek piešķirts pārdošanas un 4175 piešķirt atlaides, var noteikt pārdošanas kopsummas atņemot atlaides no pārdošanas. Šī darbība ir norādīta kā **(5100:5600)-4175**.

### <a name="create-a-set-of-dimension-values"></a>Dimensiju vērtību kopas izveide

1.  Pārskatu veidotājā atveriet modificējamo rindas, kolonnas vai koka definīciju.
2.  Izvēlnē **Rediģēt** noklikšķiniet uz **Pārvaldīt dimensiju vērtību kopas**.
3.  Dialoglodziņa **Pārvaldīt dimensiju vērtību kopas** laukā **Dimensija** atlasiet izveidojamās dimensiju vērtību kopas tipu un tad noklikšķiniet uz **Jauns**.
4.  Dialoglodziņā **Jauns** ievadiet kopas nosaukumu un aprakstu.
5.  Kolonnā **No** veiciet dubultklikšķi šūnā.
6.  Dialoglodziņā **Konts** sarakstā atlasiet konta nosaukumu vai meklējiet ierakstu laukā **Meklēt**. Tad noklikšķiniet uz **Labi**.
7.  Atkārtojiet soļus 5.-6. kolonnā **Līdz**, lai šim operatoram izveidotu formulu.
8.  Kad formula ir pabeigta, noklikšķiniet uz **Labi**.
9.  Dialoglodziņā **Pārvaldīt dimensiju kopas** noklikšķiniet uz **Aizvērt**.

### <a name="update-a-set-of-dimension-values"></a>Dimensiju vērtību kopas atjaunināšana

1.  Pārskatu veidotājā atveriet modificējamo rindas, kolonnas vai koka definīciju.
2.  Izvēlnē **Rediģēt** noklikšķiniet uz **Pārvaldīt dimensiju vērtību kopas**.
3.  Dialoglodziņa **Pārvaldīt dimensiju vērtību kopas** laukā **Dimensija** atlasiet dimensijas tipu.
4.  Sarakstā atlasiet atjaunināmo dimensiju vērtību kopu un tad noklikšķiniet uz **Modificēt**.
5.  Dialoglodziņā **Modificēt** modificējiet formulu vērtības, kuras vēlaties iekļaut kopā. **Piezīme:** ja pievienojat jaunus kontus vai dimensijas, pārliecinieties, ka modificējat pastāvošu dimensiju vērtību kopu, kurā vēlaties iekļaut izmaiņas.
6.  Veiciet dubultklikšķi uz šūnas un atlasiet atbilstošo operatoru, **No** kontu un **Līdz** kontu.
7.  Noklikšķiniet uz **Labi**, lai aizvērtu dialoglodziņu **Modificēt** un saglabātu izmaiņas.

### <a name="copy-a-dimension-set"></a>Dimensiju kopas kopēšana

1.  Pārskatu veidotājā atveriet modificējamo rindas, kolonnas vai koka definīciju.
2.  Izvēlnē **Rediģēt** noklikšķiniet uz **Pārvaldīt dimensiju vērtību kopas**.
3.  Dialoglodziņa **Pārvaldīt dimensiju vērtību kopas** laukā **Dimensija** atlasiet dimensijas tipu.
4.  Sarakstā atlasiet kopējamo kopu un tad noklikšķiniet uz **Saglabāt kā**.
5.  Ievadiet kopētās kopas jauno nosaukumu un tad noklikšķiniet uz **Labi**.

### <a name="delete-a-dimension-set"></a>Dimensiju kopas dzēšana

1.  Pārskatu veidotājā atveriet modificējamo rindas, kolonnas vai koka definīciju.
2.  Izvēlnē **Rediģēt** noklikšķiniet uz **Pārvaldīt dimensiju vērtību kopas**.
3.  Dialoglodziņa **Pārvaldīt dimensiju vērtību kopas** laukā **Dimensija** atlasiet dimensijas tipu.
4.  Atlasiet dzēšamo kopu un tad noklikšķiniet uz **Dzēst**. Noklikšķiniet uz **Jā**, lai neatgriezeniski izdzēstu šo dimensijas vērtību kopu.


<a name="see-also"></a>Skatiet arī
--------

[Finanšu pārskatu Microsoft Dynamics 365 operācijām](financial-reporting-intro.md)


