---
title: Rindu definīciju šūnu modificēšana
description: Šajā tēmā ir izskaidrota informācija, kas ir nepieciešama katrai šūnai finanšu atskaites rindas definīcijā, un paskaidrots, kā šo informāciju ievadīt.
author: ShylaThompson
manager: AnnBe
ms.date: 02/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 58881
ms.assetid: 0af492df-a84e-450c-8045-78ef1211abaf
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 92d03f08fc5e34402f10068ed770b1f724cfd3a8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685863"
---
# <a name="modify-row-definition-cells"></a>Rindu definīciju šūnu modificēšana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir izskaidrota informācija, kas ir nepieciešama katrai šūnai finanšu atskaites rindas definīcijā, un paskaidrots, kā šo informāciju ievadīt.

## <a name="specify-a-row-code-in-a-row-definition"></a>Rindas koda norādīšana rindas definīcijā

Rindas definīcijā numuri vai etiķetes šūnā **Rindas kods** identificē rindas definīcijas katru rindu. Rindas kodu var norādīt, lai izveidotu atsauci uz datiem aprēķinos vai kopsummās.

### <a name="row-code-requirements"></a>Rindas koda prasības

Rindas kods ir jānorāda visās rindās. Rindas definīcijā varat kombinēt ciparu, burtciparu un neiestatītus (tukšu) rindu kodus. Rindas kods var būt pozitīvs vesels skaitlis (mazāks par 100 000 000) vai aprakstoša etiķete ar rindas identifikāciju. Aprakstošajai etiķetei jāievēro tālāk minētie nosacījumi.

- Etiķetei jāsākas ar alfabēta rakstzīmi (no a līdz z vai no A līdz Z), un tā var būt jebkura ciparu un burtu kombinācija līdz 16 rakstzīmēm.

    > [!NOTE]
    > Etiķete var ietvert pasvītrojuma rakstzīmi (\_), bet nav atļautas citas īpašās rakstzīmes.

- Etiķetē aizliegts izmantot rezervētos vārdus: AND, OR, IF, THEN, ELSE, PERIODS, TO, BASEROW, UNIT, NULL, CPO vai RPO.

Šeit norādīti daži derīgu rindu kodu piemēri:

- 320
- TL\_NET\_INCOME
- TL\_NET\_94

### <a name="change-a-row-code-in-a-row-definition"></a>Rindas definīcijas rindas koda maiņa

1. Atskaišu veidotājā noklikšķiniet uz **Rindas definīcijas** un atveriet modificējamo rindas definīciju.
2. Atbilstošajā rindā ievadiet jaunu vērtību kolonnas **Rindas kods** šūnā.

### <a name="reset-numeric-row-codes"></a>Skaitlisko rindu kodu atiestate

1. Pārskatu veidotājā noklikšķiniet uz **Rindu definīcijas** un atveriet modificējamo rindas definīciju.
2. Izvēlnē **Rediģēt** noklikšķiniet uz **Pārnumurēt rindas**.
3. Dialoglodziņā **Pārnumurēt rindas** norādiet jaunās vērtības sākuma rindas kodam un rindu kodu pieauguma solim. Varat atiestatīt ciparu rindu kodus uz vienādi izvietotām vērtībām. Taču atskaišu veidotājs pārnumurē tikai tos rindu kodus, kas sākas ar skaitļiem (piemēram, 130 vai 246). Tas nepārnumurē rindu kodus, kas sākas ar burtiem (piemēram, INCOME\_93 vai TP0693).

> [!NOTE]
> Kad pārnumurējat rindu kodus, pārskatu veidotājs automātiski atjaunina **TOT** un **CAL** atsauces. Piemēram, ja **TOT** rinda atsaucas uz diapazonu, kas sākas ar rindas kodu 100, un jūs pārnumurējat rindas, sākot ar 90, sākuma **TOT** atsauce tiek mainīta no 100 uz 90.

## <a name="add-a-description"></a>Apraksta pievienošana
Apraksta šūna sniedz aprakstu par pārskata rindā esošajiem finanšu datiem, piemēram, Ieņēmumi vai Tīrā peļņa. Teksts šūnā **Apraksts** tiek parādīts pārskatā tieši tā, kā to ievadāt rindas definīcijā.

> [!NOTE]
> Apraksta kolonnas platums pārskatā ir iestatīts kolonnas definīcijā. Ja teksts rindas definīcijā kolonnā **Apraksts** ir garš, pārbaudiet kolonnas **DESC** platumu. Izmantojot dialoglodziņu **Ievietot rindas no** vērtības kolonnā **Apraksts** ir finanšu datu segmentu vērtības vai dimensiju vērtības. Varat ievietot rindas, lai pievienotu aprakstošu tekstu, piemēram, sadaļas virsrakstu vai sadaļas kopsummu, un pievienotu formatējumu, piemēram, līniju virs kopsummas rindas. Ja pārskatā ietilpst pārskatu koks, varat ietvert papildu tekstu, kas pārskatu kokā ir definēts pārskatu vienībām. Varat arī ierobežot papildu teksta lietošanu, izmantojot konkrētu pārskatu vienību.

### <a name="add-the-description-for-a-line-on-a-report"></a>Apraksta pievienošana pārskata rindai

1. Pārskatu veidotājā noklikšķiniet uz **Rindu definīcijas** un atveriet modificējamo rindas definīciju.
2. Atlasiet šūnu **Apraksts** un tad ievadiet pārskata rindas nosaukumu.
3. Lietot formatējumu.

### <a name="add-additional-text-from-a-reporting-tree-in-the-description"></a>Papildu teksta pievienošana aprakstam no pārskatu koka

1. Pārskatu veidotājā noklikšķiniet uz **Rindu definīcijas** un atveriet modificējamo rindas definīciju.
2. Ievadiet papildu teksta kodu un pārējo tekstu atbilstošajā šūnā **Apraksts**.
3. Lietot formatējumu.

### <a name="limit-the-additional-text-to-a-specific-reporting-unit"></a>Papildu teksta ierobežošana, izmantojot konkrētu pārskatu vienību

1. Pārskatu veidotājā noklikšķiniet uz **Rindu definīcijas** un atveriet modificējamo rindas definīciju.
2. Atrodiet rindu, kurā jāizveido papildu teksts, un tad veiciet dubultklikšķi uz šūnas kolonnā **Saistītās formulas/Rindas/Vienības**.
3. Atlasiet pārskata koku dialoglodziņa **Pārskata vienību atlase** laukā **Pārskata koks**.
4. Laukā **Atlasiet ierobežojuma pārskata vienību** izvērsiet vai sakļaujiet pārskata koku un tad atlasiet pārskata vienību.

## <a name="add-a-format-code"></a>Formāta koda pievienošana
Šūnā **Formāta kods** iespējams izvēlēties iepriekš formatētu rindas satura izvēli. Ja šūna **Formāta kods** ir tukša, rinda tiek interpretēta kā rinda informācijai par finanšu datiem.

> [!NOTE]
> Ja pārskats ietver formatēšanas rindas, kas nav paredzētas summām, bet kas ir saistītas ar summas rindām, kuras ir likvidētas (piemēram, sakarā ar nulles bilanci), tad varat izmantot kolonnu **Saistītās formulas/rindas/vienības**, lai nepieļautu virsraksta un formāta rindu drukāšanu.

### <a name="add-a-format-code-to-a-report-row"></a>Formāta koda pievienošana pārskata rindai

1. Pārskatu veidotājā noklikšķiniet uz **Rindu definīcijas** un atlasiet modificējamo rindas definīciju.
2. Veiciet dubultklikšķi uz **Formāta kods** šūnas.
3. Sarakstā atlasiet formāta kodu. Tālāk sniegtajā tabulā ir aprakstīti formātu kodi un to darbības.

    | Formāta kods                   | Formāta koda interpretācija | Darbība |
    |-------------------------------|-----------------------------------|--------|
    | (nav)                        |                                   | Notīra šūnu **Formāta kods**. |
    | KOP                           | Kopsumma                             | Identificē rindu, kas izmanto matemātiskās operācijas kolonnā **Saistītās Formulas/Rindas/Vienības**. Kopsummās tiek lietoti vienkārši operatori, piemēram, **+** vai **-**. |
    | CAL                           | Aprēķins                       | Identificē rindu, kas izmanto matemātiskās operācijas kolonnā **Saistītās Formulas/Rindas/Vienības**. Aprēķinos tiek lietoti sarežģīti operatori, piemēram, **+**, **-**, **\**_, _*/** un priekšraksti **IF/THEN/ELSE**. |
    | APR                           | Apraksts                       | Identificē pārskatā virsraksta rindas vai tukšu rindu. |
    | LFT RGT CEN                   | Pa kreisi Pa labi Pa vidu                 | Izlīdzina rindas apraksta tekstu pārskata lapā neatkarīgi no teksta izvietojuma kolonnas definīcijā. |
    | MBR                           | Pamata rindas maiņa                   | Norāda rindu, kas kolonnu aprēķiniem iestata pamata rindu. |
    | KOLONNA                        | Kolonnu pārtraukumi                      | Sāk jaunu pārskata kolonnu. |
    | PAGE                          | Lappuses pārtraukums                        | Sāk jaunu pārskata lapu. |
    | \---                          | Vienkāršs pasvītrojums                  | Izvieto vienu līniju zem visām pārskata summas kolonnām. |
    | ===                           | Dubults pasvītrojums                  | Izvieto divas līnijas zem visām pārskata summas kolonnām. |
    | LĪNIJA1                         | Šaura līnija                         | Pāri lapai uzvelk vienkāršu šauru līniju. |
    | LĪNIJA2                         | Bieza līnija                        | Pāri lapai uzvelk vienkāršu biezu līniju. |
    | LĪNIJA3                         | Punktēta līnija                       | Pāri lapai uzvelk vienkāršu punktētu līniju. |
    | LĪNIJA4                         | Bieza līnija un šaura līnija          | Pāri lapai uzvelk dubultu līniju. Augšējā līnija ir bieza, un apakšējā līnija ir šaura. |
    | LĪNIJA5                         | Šaura līnija un bieza līnija          | Pāri lapai uzvelk dubultu līniju. Augšējā līnija ir šaura, un apakšējā līnija ir bieza. |
    | BXB BXC                       | Ierāmēta rinda                         | Zīmē rāmi ap pārskata rindām, kas sākas ar **BXB** rindu un beidzas ar **BXC** rindu. |
    | PIEZ                           | Piezīme                            | Norāda rindu, kas ir komentāru rinda un kas nav jādrukā pārskatā. Piemēram, piezīmju rinda var skaidrot jūsu formatēšanas metodes. |
    | SORT ASORT SORTDESC ASORTDESC | Kārtot                              | Kārto izdevumus vai ienākumus, kārto faktiskās vai budžeta novirzes pārskatu pēc lielākās novirzes vai kārto rindu aprakstus pēc alfabēta. |

## <a name="specify-related-formulasrowsunits"></a>Saistītās formulas/rindas/vienības norādīšana
Šūnai **Saistītās formulas/Rindas/Vienības** ir vairāki pielietojumi. Atkarībā no rindas tipa šūna **Saistītās formulas/Rindas/Vienības** var veikt vienu no šādām funkcijām:

- Definēt rindas, kas jāpievieno aprēķinā, kad lietojat **TOT** formāta kodu vai **CAL** formāta kodu;
- formāta rindas saistīšana ar summas rindu, lai formatējumu tiktu drukāts tikai gadījumā, kad tiek drukāta saistītā summa
- rindas ierobežošana, izmantojot konkrētu pārskatu vienību
- Definēt pamata rindu aprēķiniem, kad izmantojat **BASEROW** formāta kodu;
- kārtojamo rindu definēšana, izmantojot jebkuru kārtošanas formāta kodu

### <a name="use-a-row-total-in-a-row-definition"></a>Rindas kopsummas izmantošana rindas definīcijā

Izmantojiet rindas kopsummas formulu, lai pievienotu summas vai atskaitītu tās no citu rindu vērtībām. Rindas kopsummas izveides formulā var ietvert operatorus + un -, lai apvienotu atsevišķu rindu kodus un diapazonus. Diapazoni tiek apzīmēti ar kolu (:). Formula var ietvert līdz 1024 rakstzīmēm. Šis ir standarta summēšanas formulas piemērs: 400+420+430+450+460LIABILITIES + EQUITY520:546520:546-LIABILITIES

### <a name="components-of-a-row-total-formula"></a>Rindas kopsummas formulas komponenti

Izveidojot rindas kopsummas formulu, ir jāizmanto rindu kodi, lai norādītu rindas, kas ir jāpievieno vai jāatskaita pašreizējā rindas definīcijā. Turklāt ir jāizmanto operatori, lai norādītu, kā rindas ir jāapvieno. Kopsummu rindas un summu rindas var apvienot jebkādā kombinācijā.

> [!NOTE]
> Diapazonā esošās kopsummu rindas tiek izslēgtas. Lai aprēķinātu visu kopsummu vērtību, varat norādīt rindu diapazonu. Ja diapazona pirmā rinda ir kopsummas rinda, šī rinda tiek ietverta jaunajā kopsummā. Tabulā ir aprakstīts, kā operatori tiek izmantoti rindu kopsummu formulās.

| Operators | Parauga formula | Apraksts                                                 |
|----------|-----------------|-------------------------------------------------------------|
| +        | 100+330         | Pievieno summu 100. rindā summai 330. rindā.        |
| :        | 100:330         | Pievieno kopsummas no visām rindām starp 100. rindu un 330. rindu.    |
| -        | 100-330         | Atņem summu 100. rindā no summas 330. rindā. |

### <a name="create-a-row-total"></a>Rindas kopsummas izveide

1. Pārskatu veidotājā noklikšķiniet uz **Rindas definīcijas** un pēc tam atveriet modificējamo rindas definīciju.
2. Veiciet dubultklikšķi uz šūnas **Formāta kods** rindas definīcijā un atlasiet **TOT**.
3. Šūnā **Saistītās formulas/Rindas/Vienības** ievadiet kopsummas formulu.

### <a name="relate-a-format-row-to-an-amount-row"></a>Formāta rindas saistīšana ar summas rindu

Rindas definīcijas kolonnā **Formāta kods** formātu kodi **DES**, **LFT**, **RGT**, **CEN**, **---** un **===** nodrošina formatējuma lietošanu rindām, kas nav summas rindas. Lai novērstu formatējuma drukāšanu, kad saistītās summas rindas ir likvidētas (piemēram, ja summas rindās ir nulles vērtības vai nav perioda aktivitātes), formāta rindas ir jāsaista ar atbilstošām summu rindām. Šī funkcionalitāte ir noderīga, ja nevēlaties drukāt galvenes vai formatējumu, kas ir saistīts ar starpsummām, kad periodā nav informācijas.

> [!NOTE]
> Varat neļaut arī detalizēto summu rindu drukāšanu, noņemot atzīmi opcijai, kas rāda rindas bez summām. Šī opcija atrodas pārskata definīcijas cilnē **Iestatījumi**. Pārskatā pēc noklusējuma tiek izlaista darījumu detalizēta informācija par kontiem, kuros ir nulles bilance vai kuros attiecīgā periodā netika veiktas darbības. Lai parādītu šos transakciju detalizētās informācijas kontus, atzīmējiet izvēles rūtiņu **Parādīt rindas bez summām** pārskata definīcijas cilnē **Iestatījumi**.

### <a name="relate-a-format-row-to-an-amount-row"></a>Formāta rindas sasaistīšana ar summas rindu

1. Pārskatu veidotājā noklikšķiniet uz **Rindu definīcijas** un atlasiet modificējamo rindas definīciju.
2. Formatējuma rindas šūnā **Saistītās formulas/Rindas/Vienības** ievadiet likvidējamās summas rindas kodu.

    > [!NOTE]
    > Lai izlaistu summas rindu, rindas bilancei ir jābūt 0 (nulle). Summas rinda ar bilanci netiek izlaista.

3. Izvēlnē **Fails** noklikšķiniet uz **Saglabāt**.

### <a name="example-of-preventing-printing-of-rows"></a>Rindu drukāšanas izlaišanas piemērs

Šajā piemērā lietotājs vēlas novērst virsrakstu un pasvītrojuma zīmju drukāšanu sava pārskata rindai **Kopsumma kasē**, jo nevienā no kases kontiem nebija aktivitātes. Tāpēc 220. rindas (kas saskaņā ar formāta kodu **---** ir formatēšanas rinda) šūnā **Saistītās formulas/rindas/vienības** lietotājs ievada **250**, kas ir tās summas rindas kods, kuru lietotājs vēlas likvidēt.

[![RelatedRowsRowDefinition](./media/relatedrowsrowdefinition-1024x144.png)](./media/relatedrowsrowdefinition.png)

## <a name="select-the-base-row-for-a-column-calculation"></a>Pamata rindas atlase kolonnas aprēķinam
Relāciju pārskatā rindas definīcijai piešķiriet vienu vai vairākas pamata rindas, izmantojot formāta kodu **CBR** (pamata rindas maiņa). Pēc tam ar aprēķinu kolonnas definīcijā tiek izmantota atsauce uz pamata rindu. Tālāk minēti daži tipiski CBR aprēķinu piemēri.

- Kopējo ieņēmumu procenti attiecībā pret atsevišķiem ieņēmumu vienumiem.
- Kopējo izdevumu procentuālais daudzums attiecībā pret atsevišķiem izdevumu vienumiem.
- Bruto peļņas procenti attiecībā pret dalījuma vai nodaļas informāciju.

Rindas definīcijā tiek definēta viena vai vairākas pamata rindas, un pēc tam kolonnas definīcija nosaka relāciju, kādā par šo pamata rindu tiek ziņots. Kods, kas tiek izmantots kolonnas formulā ir **BASEROW**. Ar **BASEROW** tiek izmantotas šādas pamata matemātiskās darbības: dalīt, reizināt, pieskaitīt vai atņemt. Operācija, kas tiek izmantota visbiežāk, ir dalīt ar **BASEROW**, kur rezultāts tiek parādīts procentos. Kolonnas aprēķini, kas formulā izmanto **BASEROW**, izmanto saistīto pamata rindu kodu rindas definīciju. **CBR** rindām ir šādi rekvizīti:

- **CBR** rindas pabeigtajā pārskatā netiek drukātas,
- **CBR** formāta kods un tā saistītās rindas kods ir novietoti virs rindas vai sadaļas, kas parāda saistītos aprēķinus.

Kolonnas definīcijā kolonnas tips **APRĒK** norāda kolonnu, kas nosaka formulu rindā **Formula**. Šī formula darbojas ar šīs pārskata kolonnas datiem un izmanto Baserow atslēgvārdu, lai balstītu aprēķinus uz rindas formātu kodiem **CBR**. Rindas definīcijā formāta kods **CBR** nosaka pamata rindu kolonnām, kas veic uz pamata rindu balstītus procentu aprēķinus vai reizina katru pārskata rindu ar pamata rindu. Rindas formātā var būt vairāki **CBR** formātu kodi, piemēram, viens neto pārdošanai, viens bruto pārdošanai un viens kopējiem izdevumiem. Parasti **CBR** formāta kodu izmanto, lai aprēķinātu kontu procentuālās daļas, kas tiek salīdzinātas ar rindas kopsummu. Pamata rinda tiek izmantota visiem aprēķiniem, līdz tiek definēta cita pamata rinda. Ir jādefinē sākuma **CBR** formāta kods un beigu **CBR** formāta kods. Lai izdevumus noteiktu, piemēram, kā procentuālu daudzumu no neto pārdošanas daudzuma, vērtību katrā izdevumu rindā varat dalīt ar vērtību neto pārdošanas rindā. Šajā gadījumā neto pārdošanas rinda ir pamata rinda. Varat definēt kolonnas definīciju, kas ziņo par pašreizējiem un līdzšinējā gada rezultātiem kopā ar pamata procentuālo daudzumu katram rezultātam (skatīt tālāk sniegto piemēru). Sāciet ar detalizētu peļņas un zaudējumu pārskatu.

### <a name="select-the-base-row-in-a-row-definition-for-a-column-calculation"></a>Pamata rindas atlase rindas definīcijā kolonnas aprēķinam

1. Pārskatu veidotājā noklikšķiniet uz **Kolonnu definīcijas** un atveriet peļņas un zaudējumu pārskata kolonnas definīciju.
2. Kolonnu definīcijai pievienojiet jaunu kolonnu, un iestatiet kolonnas tipu **CALC**.
3. Jaunās kolonnas šūnā **Formula** ievadiet formulu **X/BASEROW**, kur **X** ir **FD** kolonnas tips, kurš jāizsaka procentos.
4. Veiciet dubultklikšķi uz šūnas **Formāts/Valūtas ignorēšana**.
5. Dialoglodziņā **Formāta ignorēšana**, kas atrodas sarakstā **Formāta kategorija**, atlasiet **Procenti** un noklikšķiniet uz **Labi**.
6. Lai saglabātu kolonnas definīciju ar jaunu nosaukumu, izvēlnē **Fails** noklikšķiniet uz **Saglabāt kā**. Pašreizējam faila nosaukumam pievienojiet **CBR** (piemēram, **CUR\_YTD\_CBR**). Šī kolonnas definīcija ir jūsu pamata rindas kolonnas definīcija.
7. Pārskatu veidotājā noklikšķiniet uz **Rindu definīcijas** un atveriet modificējamo rindas definīciju, izmantojot pamata rindas aprēķinus.
8. Ievietojiet jaunu rindu virs rindas, kurā jāsākas pamata rindas aprēķinam.
9. Veiciet dubultklikšķi uz šūnas **Formāta kods** rindas definīcijā un atlasiet **CBR**.
10. Šūnā **Saistītās formulas/Rindas/Vienības** ievadiet bāzes rindas koda numuru.

### <a name="example-of-base-row-calculation"></a>Pamata rindas aprēķina piemērs

Šajā rindas definīcijas piemērā 100. rindā ir parādīts, ka aprēķinu pamata rinda ir 280. rinda.

[![Pamata rindas aprēķina piemērs.](./media/cbrrowdefinition.png)](./media/cbrrowdefinition.png)

Šajā kolonnas definīcijas piemērā aprēķiniem tiek izmantots formāta kods **CBR**. Aprēķins kolonnā C šī pārskata kolonnas B vērtību dala ar vērtību kolonnas B rindā 280. Formāta ignorēšana kolonnā B šī aprēķina rezultātu izdrukā kā procentuālu vērtību. Līdzīgi katra summa kolonnā E ir kolonnā D esošais daudzums, kas izteikts kā procenti no neto pārdošanas daudzuma.

[![Kolonnas definīcijas piemērs.](./media/cbrcolumndefinition2.png)](./media/cbrcolumndefinition2.png)

Tālāk minētajā piemērā ir parādīts pārskats, kuru var izveidot, balstoties uz iepriekšējiem aprēķiniem.

[![Atskaites piemērs, kurā ir izmantoti iepriekš sniegtie aprēķinu piemēri.](./media/cbrreport-1024x272.png)](./media/cbrreport.png)

## <a name="select-a-sorting-code-for-a-row-definition"></a>Rindas definīcijai paredzēta kārtošanas koda atlase
Izmantojot kārtošanas kodus, var kārtot kontus un vērtības, kārtot faktisko vai budžeta noviržu pārskatu pēc lielākās novirzes, kā arī kārtot rindu aprakstus pēc alfabēta. Ir pieejami šādi kārtošanas kodi:

- **SORT** — sakārto atskaiti augošā secībā, pamatojoties uz vērtībām norādītajā kolonnā.
- **ASORT** — sakārto atskaiti augošā secībā, pamatojoties uz norādītajā kolonnā esošo vērtību absolūtajām vērtībām. Citiem vārdiem sakot, kārtojot vērtības, tiek ignorēta katras vērtības zīme. Izmantojot šo formāta kodu, vērtības tiek kārtotas pēc novirzes lieluma neatkarīgi no tā, vai vērtība ir pozitīva vai negatīva.
- **SORTDESC** — sakārto atskaiti dilstošā secībā, pamatojoties uz vērtībām norādītajā kolonnā.
- **ASORTDESC** — sakārto atskaiti dilstošā secībā, pamatojoties uz norādītajā kolonnā esošo vērtību absolūtajām vērtībām.

### <a name="select-a-sorting-code"></a>Kārtošanas koda atlasīšana

1. Pārskatu veidotājā noklikšķiniet uz **Rindu definīcijas** un atveriet modificējamo rindas definīciju.
2. Veiciet dubultklikšķi uz šūnas **Formāta kods** un atlasiet kārtošanas kodu.
3. Šūnā **Saistītās formulas/Rindas/Vienības** norādiet kārtojamo rindu kodu diapazonu. Lai norādītu diapazonu, ievadiet pirmās rindas kodu, kolu (:) un pēc tam pēdējās rindas kodu. Piemēram, ievadiet **160:490** lai norādītu, ka diapazons ir no 160. rindas līdz 490. rindai.
4. Šūnā **Kolonnu ierobežojums** ievadiet tās pārskata kolonnas burtu, kas jāizmanto kārtošanai.

    > [!NOTE]
    > Kārtošanas aprēķinā iekļaujiet tikai summu rindas.

### <a name="examples-of-ascending-and-descending-column-values"></a>Augošu un dilstošu kolonnu vērtību piemēri

Tālāk sniegtā piemēra ietvaros pārskata D kolonnas 160.–490. rindas vērtības tiek sakārtotas augošā secībā. Turklāt G kolonnas 610.–940. rindas absolūtās vērtības tiek kārtotas dilstošā secībā.

| Rindas kods | Apraksts                                         | Formāta kods | Saistītās formulas/rindas/vienības | Parasta bilance | Kolonnas ierobežojums | Saite uz finanšu dimensijām |
|----------|-----------------------------------------------------|-------------|-----------------------------|----------------|--------------------|------------------------------|
| 100      | Kārtots augošā secībā pēc mēneša novirzes       | APR         |                             |                |                    |                              |
| 130      |                                                     | KĀRT        | 160:490                     |                | D                  |                              |
| 160      | Pārdošana                                               |             |                             | C              |                    | 4100                         |
| 190      | Atgrieztās pārdotās preces                                       |             |                             |                |                    | 4110                         |
|          | ...                                                 |             |                             |                |                    |                              |
| 490      | Procentu ieņēmumi                                     |             |                             | C              |                    | 7000                         |
| 520      |                                                     | APR         |                             |                |                    |                              |
| 550      | Kārtots dilstošā secībā pēc YTD absolūtās novirzes | APR         |                             |                |                    |                              |
| 580      |                                                     | AKĀRTDILST   | 610:940                     |                | P                  |                              |
| 610      | Pārdošana                                               |             |                             | U              |                    | 4100                         |
| 640      | Atgrieztās pārdotās preces                                       |             |                             |                |                    | 4110                         |
|          | ...                                                 |             |                             |                |                    |                              |
| 940      | Procentu ieņēmumi                                     |             |                             | U              |                    | 7000                         |


## <a name="specify-a-format-override-cell"></a>Formāta ignorēšanas šūnu norādīšana
Šūna **Formāta ignorēšana** norāda formatējumu, kas rindai tiek izmantots pārskata drukāšanai. Šis formatējums aizstāj formatējumu, kas ir norādīts kolonnas definīcijā un pārskata definīcijā. Pēc noklusējuma šajās definīcijās norādītais formatējums ir valūta. Ja kādā pārskata rindā ir norādīts līdzekļu skaits, piemēram, ēku skaits, un citā rindā — šo līdzekļu monetārā vērtība, valūtas formātu var pārrakstīt, ievadot skaitlisko formātu rindās, kurās ir norādīts ēku skaits. Šī informācija jānorāda dialoglodziņā **Formātā ignorēšana**. Opciju pieejamība ir atkarīga no atlasītās formāta kategorijas. Dialoglodziņa apgabalā **Paraugs** tiek parādīti formātu piemēri. Ir pieejamas šādas formāta kategorijas.

- Valūtas formatēšana
- Skaitliskā formatēšana
- Procentuālā formatēšana
- Pielāgotā formatēšana

### <a name="override-cell-formatting"></a>Šūnas formāta ignorēšana

1. Pārskatu veidotājā atveriet modificējamo rindas definīciju.
2. Rindā, kurā vēlaties ignorēt formātu, veiciet dubultklikšķi uz šūnas kolonnā **Formāta ignorēšana**.
3. Dialoglodziņā **Formāta ignorēšana** atlasiet formatēšanas opcijas, kuras šai rindai vēlaties izmantot pārskatā.
4. Noklikšķiniet uz **Labi**.

### <a name="currency-formatting"></a>Valūtas formatēšana

Valūtas formatēšana attiecas naudas līdzekļu daudzumu un ietver valūtas simbolu. Ir pieejamas tālāk minētās opcijas.

- **Valūtas simbols** — valūtas simbols, kas ir ietverams pārskatā. Šī vērtība ignorē uzņēmuma informācijas **Reģionālās opcijas** iestatījumu.
- **Negatīvi skaitļi** — negatīvie skaitļi var būt atzīmēti ar mīnusa zīmi (-), tie var parādīties iekavās vai tie var būt atzīmēti ar trīsstūri (∆).
- **Decimāldaļas vietas** — ciparu skaits, ko rādīt pēc komata.
- **Nulles vērtības ignorēšanas teksts** — teksts, kas jāiekļauj pārskatā, ja summa ir 0 (nulle). Šis teksts tiek rādīts apgabala **Paraugs** pēdējā rindā.

    > [!NOTE]
    > Ja nulles vērtībām vai neesošai perioda aktivitātei drukāšana tiek atcelta, tad šis teksts tiek atcelts.

### <a name="numeric-formatting"></a>Skaitliskā formatēšana

Skaitlisko formatēšanu var lietot jebkādā summā, un formatēšana neietver valūtas simbolu. Ir pieejamas tālāk minētās opcijas.

- **Negatīvi skaitļi** — negatīvie skaitļi var būt atzīmēti ar mīnusa zīmi (-), tie var parādīties iekavās vai tie var būt atzīmēti ar trīsstūri (∆).
- **Decimāldaļas vietas** — ciparu skaits, ko rādīt pēc komata.
- **Nulles vērtības ignorēšanas teksts** — teksts, kas jāiekļauj pārskatā, ja summa ir 0 (nulle). Šis teksts tiek rādīts apgabala **Paraugs** pēdējā rindā.

    > [!NOTE]
    > Ja nulles vērtībām vai neesošai perioda aktivitātei drukāšana tiek atcelta, tad šis teksts tiek atcelts.

### <a name="percentage-formatting"></a>Procentuālā formatēšana

Procentuālā formatēšana ietver procenta simbolu (%). Ir pieejamas tālāk minētās opcijas.

- **Negatīvi skaitļi** — negatīvie skaitļi var būt atzīmēti ar mīnusa zīmi (-), tie var parādīties iekavās vai tie var būt atzīmēti ar trīsstūri (∆).
- **Decimāldaļas vietas** — ciparu skaits, ko parādīt pēc komata.
- **Nulles vērtības ignorēšanas teksts** — teksts, kas jāiekļauj pārskatā, ja summa ir 0 (nulle). Šis teksts tiek rādīts apgabala **Paraugs** pēdējā rindā.

    > [!NOTE]
    > Ja nulles vērtībām vai neesošai perioda aktivitātei drukāšana tiek atcelta, tad šis teksts tiek atcelts.

### <a name="custom-formatting"></a>Pielāgotā formatēšana

Izmantojiet pielāgotu formatēšanas kategoriju, lai izveidotu pielāgoto formātu, kas aizstās esošo. Ir pieejamas tālāk minētās opcijas.

- **Tips** — pielāgotais formāts.
- **Nulles vērtības ignorēšanas teksts** — teksts, kas jāiekļauj pārskatā, ja summa ir 0 (nulle). Šis teksts tiek rādīts apgabala **Paraugs** pēdējā rindā.

    > [!NOTE]
    > Ja nulles vērtībām vai neesošai perioda aktivitātei drukāšana tiek atcelta, tad šis teksts tiek atcelts.

Tipam jāattēlo pozitīvā vērtība un pēc tam arī negatīvā vērtība. Parasti tiek ievadīts līdzīgs formāts, kas atšķir pozitīvās un negatīvās vērtības. Piemēram, lai norādītu, ka gan pozitīvām, gan negatīvām vērtībām ir divi cipari aiz komata, bet negatīvas vērtības tiek rādītas iekavās, ievadiet **0.00;(0.00)**. Tabulā tālāk ir redzami pielāgotie formāti, ko varat izmantot, lai pārvaldītu vērtību formātu. Visi piemēri sākas ar vērtību 1234,56.

| Formāts                         | Pozitīvā vērtība   | Negatīvs     | Nulle    |
|--------------------------------|------------|--------------|---------|
| 0                              | 1235       | -1235        | 0       |
| 0;0                            | 1235       | 1235         | 0       |
| 0;(0);-                        | 1235       | 1235         | -       |
| \#,\#\#\#;(\#,\#\#\#);""       | 1235      | (1235)      | (Tukšs) |
| \#,\#\#0.00;(\#,\#\#0.00);nulle | 1234,56   | (1234,56)   | nulle    |
| 0.00%;(0.00%)                  | 123456.00% | (123 456,00%) | 0,00%   |

## <a name="specify-a-normal-balance-cell"></a>Šūnas Parasta bilance norādīšana
Rindas definīcijas šūna **Parastā bilance** kontrolē rindas summu zīmi. Lai mainītu rindas zīmi vai ja parastā konta bilance ir kredīts, šīs rindas šūnā **Parastā bilance** ievadiet **C**. Pārskatu noformētājs maina zīmi uz pretējo visiem kredīta bilances kontiem šajā rindā. Kad atskaišu veidotājs pārveido šos kontus, tas noņem debeta/kredīta raksturlielumu no visām summām un tādējādi vienkāršo summēšanu. Piemēram, lai aprēķinātu tīro peļņu, no ienākumiem ir jāatskaita izdevumi. Parasti uz summēšanas un aprēķinu rindām **C** kodam nav ietekmes. Tomēr **XCR** drukas vadība kolonnas definīcijā maina zīmi jebkurā rindā, kas kolonnā **Parastā bilance** satur kodu **C**. Šis formatējums ir jo īpaši svarīgs, kad visas nevēlamās novirzes ir jāparāda kā negatīvās summas. Ja summētajam vai aprēķinātajam skaitlim ir nepareiza zīme, rindas šūnā **Parastā bilance** ievadiet **C**, kas mainīs zīmi uz pretējo.

## <a name="specify-a-row-modifier-cell"></a>Rindas modifikatora šūnas norādīšana
Rindas definīcijas šūnas **Rindas modifikators** saturs ignorē finanšu gadus, periodus un citu informāciju, kas ir norādīta šīs rindas kolonnas definīcijā. Atlasītais modifikators attiecas uz ikvienu kontu šajā rindā. Katru rindu varat modificēt, izmantojot vienu vai vairākus tālāk uzskaitīto tipu modifikatorus.

- Konta modifikatori
- Uzskaites koda modifikatori
- Konta un darījuma atribūti

### <a name="override-a-column-definition"></a>Kolonnas definīcijas ignorēšana

1. Pārskatu veidotājā atveriet modificējamo rindas definīciju.
2. Rindā, kurā vēlaties ignorēt kolonnas definīciju, veiciet dubultklikšķi uz šūnas **Rindas modifikators**.
3. Dialoglodziņā **Rindas modifikators** atlasiet opciju laukā **Konta modifikators**. Opciju aprakstu skatiet sadaļā Kontu modifikatori.
4. Laukā **Grāmatas koda modifikators** atlasiet rindai izmantojamās grāmatas kodu.
5. Sadaļā **Atribūti** veiciet tālāk minētās darbības, lai pievienotu ierakstu katram atribūtam, kas jāiekļauj rindas kodā.

    1. Veiciet dubultklikšķi uz šūnas **Atribūts** un atlasiet atribūta nosaukumu.

        > [!IMPORTANT]
        > Nomainiet numura zīmi (\#) pret skaitlisku vērtību.

    2. Veiciet dubultklikšķi uz šūnas **No** un ievadiet pirmo diapazona vērtību.
    3. Veiciet dubultklikšķi uz šūnas **Līdz** un ievadiet pēdējo diapazona vērtību.

6. Noklikšķiniet uz **Labi**.

### <a name="account-modifiers"></a>konta modifikatori,

Kad atlasāt noteiktu kontu, atskaišu veidotājs parasti kombinē kontu un finanšu gadus, periodus un citu informāciju, ko norādāt kolonnas definīcijā. Konkrētām rindām varat izmantot citu informāciju, piemēram, citus finanšu periodus. Šajā tabulā parādīti pieejamie kontu modifikatori. Aizstājiet restītes simbolu (\#) ar vērtību, kas ir vienāda ar vai mazāka par periodu skaitu finanšu gadā.

| Konta modifikators | Kas tiek izdrukāts                                                                           |
|------------------|-------------------------------------------------------------------------------------------|
| /BB              | Konta sākuma bilance.                                                     |
| /\#              | Bilance norādītajam periodam.                                                     |
| /-\#             | Bilance periodam, kas ir \# periodus pirms pašreizējā perioda.                  |
| /+\#             | Bilance periodam, kas ir \# periodus pēc pašreizējā perioda.                   |
| /C               | Bilance pašreizējam periodam.                                                       |
| /C-\#            | Bilance periodam, kas ir \# periodus pirms pašreizējā perioda.                  |
| /C+\#            | Bilance periodam, kas ir \# periodus pēc pašreizējā perioda.                   |
| /Y               | Līdzšinējā gada bilance līdz pašreizējam periodam.                                      |
| /Y-\#            | Līdzšinējā gada bilance līdz periodam, kas ir \# periodus pirms pašreizējā perioda. |
| /Y+\#            | Līdzšinējā gada bilance līdz periodam, kas ir \# periodus pēc pašreizējā perioda.  |

### <a name="book-code-modifiers"></a>Grāmatas koda modifikatori

Varat ierobežot rindu ar esošu grāmatas kodu. Kolonnas definīcijā jāiekļauj vismaz viena **FD** kolonna, kurā ir grāmatas kods.

> [!NOTE]
> Rindas grāmatas koda ierobežojums ignorē grāmatas koda ierobežojumus, kas norādīti šīs rindas kolonnas definīcijā.

### <a name="account-and-transaction-attributes"></a>Konta un darījuma atribūti

Noteiktas grāmatvedības sistēmas finanšu datos atbalsta kontu atribūtus un darījumu atribūtus. Šie atribūti darbojas kā virtuāli kontu segmenti, un tie var ietvert papildu informāciju par kontu vai darījumu. Šī papildu informācija var būt konta ID, partijas ID, pasta indeksi un citi atribūti. Ja jūsu grāmatvedības sistēmā tiek atbalstīti atribūti, rindas definīcijā kā rindu modifikatorus varat izmantot kontu atribūtus vai darījumu atribūtus. Papildinformāciju par rindas informācijas ignorēšanu skatiet šajā rakstā iepriekš aprakstītajā tēmā Kolonnas definīcijas ignorēšana.

## <a name="specify-a-link-to-financial-dimensions-cell"></a>Šūnas Saite uz finanšu dimensijām norādīšana
Šūna **Saite uz finanšu dimensijām** satur saites uz finanšu datiem, kas ir jāiekļauj katrā pārskata rindā. Šī šūnā ietver dimensiju vērtības. Lai atvērtu dialoglodziņu **Dimensijas**, veiciet dubultklikšķi uz šūnas **Saite uz finanšu dimensijām**.

> [!NOTE]
> Pārskatu veidotājs nevar atlasīt Microsoft Dynamics ERP sistēmā esošos kontus, dimensijas vai laukus, kuros ir ietverta jebkura no šīm rezervētajām rakstzīmēm: &, \*, \[, \], { vai }. Lai norādītu informāciju rindai, kas jau ir ietverta rindas definīcijā, pievienojiet šo informāciju šūnā **Saite uz finanšu dimensijām**. Lai pievienotu jaunas rindas, kurās ir saite uz finanšu datiem, un izveidotu jaunas pārskata definīcijas rindas, izmantojiet dialoglodziņu **Ievietot rindas no**. Kolonnas nosaukums tiek mainīts atkarībā no kolonnas konfigurācijas (skatiet tālāk redzamo tabulu).

| Atlasītais saites tips       | Kolonnas Saite apraksts tiek mainīts šādi |
|----------------------------------|----------------------------------------------------|
| Finanšu dimensijas             | Saite uz finanšu dimensijām                       |
| Sniegt pārskatu par darblapu                 | Finanšu pārskata izveide                         |

### <a name="specify-a-dimension-or-range"></a>Dimensijas vai diapazona norādīšana

1. Pārskatu veidotājā atveriet modificējamo rindas definīciju.
2. Veiciet dubultklikšķi uz kolonnas **Saite uz finanšu dimensijām** šūnas.
3. Dialoglodziņā **Dimensijas**, veiciet dubultklikšķi uz šūnas, kas redzama zem dimensijas nosaukuma.
4. Dimensijas dialoglodziņā atlasiet **Individuāli vai diapazona**.
5. Laukā **No** ievadiet sākuma dimensiju vai noklikšķiniet uz ![Pārlūkot](media/browse.gif "Pārlūkot"), lai meklētu pieejamās dimensijas. Lai ievadītu dimensiju diapazonu, ievadiet beigu dimensiju laukā **Uz**.
6. Lai aizvērtu dimensijas dialoglodziņu, noklikšķiniet uz **Labi**. Dialoglodziņā **Dimensijas** attēlota atjauninātā dimensija vai diapazons.
7. Lai aizvērtu dialoglodziņu **Dimensijas**, noklikšķiniet uz **Labi**.

## <a name="display-zero-balance-accounts-in-a-row-definition"></a>Nulles bilances kontu attēlošana rindas definīcijā
Pēc noklusējuma atskaišu veidotājs nedrukā rindas, kurās finanšu datos nav atbilstošas bilances. Tāpēc varat izveidot vienu rindas definīciju, kurā tiks ietvertas visu galveno segmentu vērtības vai visu dimensiju vērtības, un pēc tam izmantot šo rindas definīciju visās datu grupās.

### <a name="modify-zero-balance-settings"></a>Nulles bilances iestatījumu modificēšana

1. Pārskatu veidotājā atveriet modificējamo pārskata definīciju.
2. Cilnes **Iestatījumi** sadaļā **Citi formatējumi** atlasiet opcijas rindas definīcijai, kas tiek izmantota pārskata definīcijā.
3. Lai saglabātu izmaiņas, izvēlnē **Fails** noklikšķiniet uz **Saglabāt**.

## <a name="use-wildcard-characters-and-ranges-in-a-row-definition"></a>Aizstājējzīmju un diapazonu izmantošana rindas definīcijā
Kad dialoglodziņā **Dimensijas** ievadāt galvenā segmenta vērtību, varat ievadīt aizstājējzīmi (? vai \*) jebkurā segmenta pozīcijā. Pārskatu noformētājs izgūst visas definēto pozīciju vērtības, neņemot vērā aizstājējzīmes. Piemēram, rindas definīcija satur tikai fizisko segmentu vērtības un fiziskajiem segmentiem ir četras rakstzīmes. Ievadot **6???** kādā rindā, pārskatu noformētājam tiek dota komanda ietvert visus kontus, kuriem ir galvenā segmenta vērtība, kas sākas ar 6. Ja ievadāt **6\**_, tiek atgriezti tādi paši rezultāti, taču tajos ir ietvertas arī dažāda garuma vērtības, piemēram, _* 60** un **600000**. Atskaišu veidotājs katru aizstājējzīmi (?) aizstāj ar pilnu iespējamo vērtību klāstu, kas ietver burtus un īpašās rakstzīmes. Piemēram, diapazonā no **12?0** līdz **12?4**, aizstājējzīme virknē **12?0** tiek aizstāta ar zemāko rakstzīmju kopas vērtību un aizstājējzīme virknē **12?4** tiek aizstāta ar augstāko rakstzīmju kopas vērtību.

> [!NOTE]
> Ir jāizvairās no aizstājējzīmju izmantošanas diapazona sākuma un beigu kontos. Ja izmantojat aizstājējzīmes, norādot sākuma kontu vai beigu kontu, vaicājuma rezultāti var būt neparedzēti.

### <a name="single-segment-or-single-dimension-ranges"></a>Viena segmenta vai vienas dimensijas diapazoni

Jūs varat norādīt segmentu vērtību vai dimensiju vērtību diapazonu. Norādot diapazonu, priekšrocība ir tas, ka nav nepieciešams atjaunināt rindas definīciju katru reizi, kad finanšu datiem tiek pievienota jauna segmenta vērtība vai dimensijas vērtība. Piemēram, izmantojot diapazonu **+Konts=\[6100:6900\]**, rindas summas aprēķinam tiek izgūtas vērtības no 6100.–6900. konta. Kad diapazons ietver aizstājējzīmi (?), atskaišu veidotājs nevērtē diapazonu katrai rakstzīmei. Tā vietā tiek noteikti diapazona zemākā un augstākā vērtība, un tad tiek iekļautas robežvērtības un visas vērtības starp tām.

> [!NOTE]
> Pārskatu veidotājs nevar atlasīt Microsoft Dynamics ERP sistēmā esošos kontus, dimensijas vai laukus, kuros ir ietverta jebkura no šīm rezervētajām rakstzīmēm: &, \*, \[, \], { vai }. Varat pievienot & zīmi tikai tad, kad automātiski veidojat rindu definīcijas, izmantojot dialoglodziņu **Ievietot rindas no dimensijām**.

### <a name="multiple-segment-or-multiple-dimension-ranges"></a>Vairāku segmentu vai vairāku dimensiju diapazoni

Ja ievadāt diapazonu, izmantojot vairāku dimensiju vērtību kombinācijas, diapazona salīdzināšana tiek veikta katrai dimensijai atsevišķi ..\\financial-dimensions\\dimension-by-dimension basis. Diapazona salīdzināšanu nevar veikt rakstzīmi pēc rakstzīmes vai daļēji balstoties uz segmentu. Piemēram, diapazons **+Konts=\[5000:6000\], Nodaļa=\[1000:2000\], Izmaksu centrs=\[00\]** ietver tikai tos kontus, kas atbilst katram segmentam. Šī scenārija ietvaros pirmajai dimensijai ir jābūt diapazonā no 5000 līdz 6000, otrajai dimensijai ir jābūt diapazonā no 1000 līdz 2000 un pēdējai dimensijai ir jābūt 00. Piemēram, diapazons **+Konts=\[5100\], Nodaļa=\[1100\], Izmaksu centrs=\[01\]** netiek ietverts pārskatā, jo pēdējais segments ir ārpus norādītā diapazona. Ja segmenta vērtībā ir atstarpes, iekļaujiet šo vērtību kvadrātiekavās (\[ \]). Četrzīmju segmentam ir derīgas šādas vērtības: **\[ 234\], \[123 \], \[1 34\]**. Dimensiju vērtības ir jāietver kvadrātiekavās (\[ \]), un pārskatu noformētājs šīs iekavas pievieno jūsu vietā. Ja vairāku segmentu vai vairāku dimensiju diapazonā ir ietvertas aizstājējzīmes (? vai \*), tiek noteikta visa vairāku segmentu vai vairāku dimensiju diapazona lielākā un mazākā robežvērtība un pēc tam tiek iekļautas šīs robežvērtības un visas starp tām esošās vērtības. Ja jums ir liels diapazons, piemēram, viss kontu diapazons no 40000 līdz 99999, vajadzētu norādīt derīgu sākuma kontu un beigu kontu, ja vien iespējams.

> [!NOTE] 
> Pārskatu veidotājs nevar atlasīt Microsoft Dynamics ERP sistēmā esošos kontus, dimensijas vai laukus, kuros ir ietverta jebkura no šīm rezervētajām rakstzīmēm: &, \*, \[, \], { vai }. Varat pievienot & zīmi tikai tad, kad automātiski veidojat rindu definīcijas, izmantojot dialoglodziņu **Ievietot rindas no dimensijām**.

## <a name="add-or-subtract-from-other-accounts-in-a-row-definition"></a>Pievienošana citiem kontiem vai atskaitīšana no tiem rindas definīcijā
Lai saskaitītu vai atņemtu naudas summas vienā kontā no cita konta naudas summas, šūnā **Saite uz finanšu dimensijām** varat izmantot plus zīmi (+) un mīnus zīmi (-). Tālāk tabulā ir redzami formāti, kas tiek atbalstīti finanšu datu saitēs, lai saskaitītu vai atņemtu esošo summu vērtības.

| Operācija                                                                               | Izmantojiet šo formātu                                                                                              |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Saskaitiet divus pilnībā derīgus kontus.                                                       | +Reģions=\[000\], Konts=\[1205\], Nodaļa=\[00\]+Reģions=\[100\], Konts=\[1205\], Nodaļa=\[00\] |
| Saskaitiet divas segmenta vērtības.                                                                 | +Konts=\[1205\]+Konts=\[1210\]                                                                           |
| Saskaitiet segmenta vērtības, kas satur aizstājējzīmes.                                    | +Konts=\[120?+Konts=\[11??\]                                                                             |
| Sasummējiet pilnībā derīgu kontu diapazonu.                                                | +Reģions=\[000:100\], Konts=\[1205\], Nodaļa=\[00\]                                                   |
| Summējiet segmenta vērtību diapazonu.                                                          | +Konts=\[1200:1205\]                                                                                       |
| Sasummējiet segmenta vērtību diapazonu, kas satur aizstājējzīmes.                         | +Konts=\[120?:130?\]                                                                                       |
| Atņemiet vienu pilnībā derīgu kontu no cita pilnībā derīga konta.              | +Reģions=\[000\], Konts=\[1205\], Nodaļa=\[00\]-Reģions=\[100\], Konts=\[1205\], Nodaļa=\[00\] |
| Atņemiet viena segmenta vērtību no citas segmenta vērtības.                                  | +Konts=\[1205\]-Konts=\[1210\]                                                                           |
| Atņemiet segmenta vērtību, kas ietver aizstājējzīmi, no citas segmenta vērtības. | +Konts=\[1200\]-Konts=\[11??\]                                                                           |
| Atņemiet pilnībā derīgu kontu diapazonu.                                           | -Reģions=\[000:100\], Konts=\[1200:1205\], Nodaļa=\[00:01\]                                           |
| Atņemiet segmenta vērtību diapazonu.                                                     | -Konts=\[1200:1205\]                                                                                       |
| Atņemiet segmenta vērtību diapazonu, kas satur aizstājējzīmes.                    | -Konts=\[120?:130?\]                                                                                       |

Lai gan kontus varat modificēt nepastarpināti, varat izmantot arī dialoglodziņu **Dimensijas**, lai jūsu finanšu datu saitēm lietotu pareizo formatējumu. Jebkurā vērtībā var ietvert aizstājējzīmes (? vai \*). Taču pārskatu veidotājs nevar atlasīt Microsoft Dynamics ERP sistēmā esošos kontus, dimensijas vai laukus, kuros ir ietverta jebkura no šīm rezervētajām rakstzīmēm: &, \*, \[, \], { vai }.

> [!NOTE]
> Lai vērtības atņemtu, tās jāieraksta iekavās. Piemēram, ja ievadāt diapazonu **450?-(4509)**, tas tiek parādīts kā **+Konts=\[4509\]-Konts=\[450?\]** un pārskatu noformētajam tiek dota komanda 4509. konta segmenta summu atņemt no summas jebkurā konta segmentā, kura numurs sākas ar 450.

### <a name="add-or-subtract-accounts-from-other-accounts"></a>Pieskaitiet vai atņemiet kontus no citiem kontiem

1. Pārskatu veidotājā atveriet modificējamo rindas definīciju.
2. Atbilstošajā rindā veiciet dubultklikšķi uz šūnas kolonnā **Saite uz finanšu dimensijām**.
3. Dialoglodziņa **Dimensijas** pirmajā rindā veiciet tālāk minētās darbības.

    1. Pirmajā laukā atlasiet visas dimensijas (noklusētās) vai noklikšķiniet, lai atvērtu **Dimensiju kopu pārvaldība** dialoglodziņu, kur varat izveidot, modificēt, kopēt vai dzēst kopu.
    2. Veiciet dubultklikšķi uz šūnas **Operators +/-** un atlasiet plusa (**+**) vai mīnusa (**-**) operatoru, kas attiecas uz vienu vai vairākām dimensiju vērtībām vai kopām rindā.
    3. Atbilstošajā dimensijas vērtību kolonnā veiciet dubultklikšķi uz šūnas, lai atvērtu dialoglodziņu **Dimensijas**, un atlasiet, vai šī dimensijas vērtība ir atsevišķa vai diapazons, dimensijas vērtību kopa vai summēšanas konti. Dialoglodziņa **Dimensijas** lauku aprakstus skatiet sadaļā "Dialoglodziņa Dimensijas apraksts".
    4. Ievadiet segmenta vērtības kolonnā **No** un kolonnā **Līdz**.

4. Atkārtojiet 2. līdz 3. soli, lai pievienotu vairāk operāciju.

> [!NOTE]
> Šis operators attiecas uz visām rindas dimensijām.

## <a name="description-of-the-dimensions-dialog-box"></a>Dialoglodziņa Dimensijas apraksts
Tabulā ir aprakstīti dialoglodziņa **Dimensijas** lauki.

| Vienums                | Apraksts |
|---------------------|-------------|
| Atsevišķi vai diapazons | Laukā **No** ievadiet konta nosaukumu vai noklikšķiniet uz pogas **Pārlūkot** ![Pārlūkot](media/browse.gif "Pārlūkot"), lai pārlūkotu līdz kontam. Lai atlasītu diapazonu, ievadiet vai uzmeklējiet vērtību laukā **Līdz**. |
| Dimensijas vērtību kopa | Laukā **Nosaukums** ievadiet dimensijas vērtību kopas nosaukumu. Lai kopu izveidotu, modificētu, kopētu vai dzēstu, noklikšķiniet uz **Pārvaldīt dimensiju vērtību kopas**. Lauks **Formula** tiek aizpildīts ar formulu no šūnas **Saite uz finanšu dimensijām** šai dimensiju vērtību kopai rindas definīcijā. |
| Kontu summēšana   | Laukā **Nosaukums** ievadiet vai uzmeklējiet dimensiju summēšanas kontiem. Lauks **Formula** šim summēšanas kontam pārskata definīcijā tiek aizpildīts ar formulu no šūnas **Saite uz finanšu dimensijām**. |

## <a name="add-dimension-value-sets-in-a-row-definition"></a>Pievienojiet rindas definīcijai dimensijas vērtību kopu
Dimensiju vērtību kopa ir dimensiju vērtību grupa, kurai piešķirts nosaukums. Dimensiju vērtību kopa var saturēt tikai vienas dimensijas vērtības, bet varat izmantot dimensiju vērtību kopu vairākās rindu definīcijās, kolonnu definīcijās, pārskatu veidošanas koku definīcijās un pārskatu definīcijās. Pārskata definīcijā varat arī kombinēt vairākas dimensiju vērtību kopas. Ja maināt finanšu datus, un tādēļ nepieciešams veikt izmaiņas dimensiju vērtību kopā, varat atjaunināt dimensiju vērtību kopas definīciju. Šī atjaunināšanas darbība tiek veikta visiem tiem apgabaliem, kuriem tiek izmantota dimensiju vērtību kopa. Piemēram, ja bieži norādāt vērtību diapazonu, kas jāsaista ar finanšu datiem, piemēram, vērtības no 5100 līdz 5600, šo diapazonu var piešķirt kontu kopai ar nosaukumu Pārdošana. Pēc dimensiju vērtību kopas izveides, šo kopu varat atlasīt kā finanšu datu saiti. Vēl viens piemērs — ja kontu kopai Pārdošana ir piešķirtas vērtības no 5100 līdz 5600, bet kopai Atlaides — 4175, pārdošanas kopsummu varat noteikt, atņemot kopas Atlaides summu no kopas Pārdošana summas. Šī operācija tiek norādīta šādā veidā: **(5100:5600)-4175**.

### <a name="create-a-set-of-dimension-values"></a>Dimensiju vērtību kopas izveide

1. Pārskatu veidotājā atveriet modificējamo rindas, kolonnas vai koka definīciju.
2. Izvēlnē **Rediģēt** noklikšķiniet uz **Pārvaldīt dimensiju vērtību kopas**.
3. Dialoglodziņa **Pārvaldīt dimensiju vērtību kopas** laukā **Dimensija** atlasiet izveidojamās dimensiju vērtību kopas tipu un tad noklikšķiniet uz **Jauns**.
4. Dialoglodziņā **Jauns** ievadiet kopas nosaukumu un aprakstu.
5. Kolonnā **No** veiciet dubultklikšķi šūnā.
6. Dialoglodziņā **Konts** sarakstā atlasiet konta nosaukumu vai meklējiet ierakstu laukā **Meklēt**. Tad noklikšķiniet uz **Labi**.
7. Atkārtojiet soļus 5.-6. kolonnā **Līdz**, lai šim operatoram izveidotu formulu.
8. Kad formula ir pabeigta, noklikšķiniet uz **Labi**.
9. Dialoglodziņā **Dimensiju kopu pārvaldība** noklikšķiniet uz **Aizvērt**.

### <a name="update-a-set-of-dimension-values"></a>Dimensiju vērtību kopas atjaunināšana

1. Pārskatu veidotājā atveriet modificējamo rindas, kolonnas vai pārskatu koka definīciju.
2. Izvēlnē **Rediģēt** noklikšķiniet uz **Pārvaldīt dimensiju vērtību kopas**.
3. Dialoglodziņa **Pārvaldīt dimensiju vērtību kopas** laukā **Dimensija** atlasiet dimensijas tipu.
4. Sarakstā atlasiet atjaunināmo dimensiju vērtību kopu un tad noklikšķiniet uz **Modificēt**.
5. Dialoglodziņā **Modificēt** modificējiet formulu vērtības, kuras vēlaties iekļaut kopā.

    > [!NOTE]
    > Ja pievienojat jaunus kontus vai dimensijas, noteikti modificējiet pastāvošo dimensiju vērtību kopu, lai ieviestu šīs izmaiņas.

6. Veiciet dubultklikšķi uz šūnas un atlasiet atbilstošo operatoru, **No** kontu un **Līdz** kontu.
7. Noklikšķiniet uz **Labi**, lai aizvērtu dialoglodziņu **Modificēt** un saglabātu izmaiņas.

### <a name="copy-a-dimension-set"></a>Dimensiju kopas kopēšana

1. Pārskatu veidotājā atveriet modificējamo rindas, kolonnas vai pārskatu koka definīciju.
2. Izvēlnē **Rediģēt** noklikšķiniet uz **Pārvaldīt dimensiju vērtību kopas**.
3. Dialoglodziņa **Pārvaldīt dimensiju vērtību kopas** laukā **Dimensija** atlasiet dimensijas tipu.
4. Sarakstā atlasiet kopējamo kopu un tad noklikšķiniet uz **Saglabāt kā**.
5. Ievadiet kopētās kopas jauno nosaukumu un tad noklikšķiniet uz **Labi**.

### <a name="delete-a-dimension-set"></a>Dimensiju kopas dzēšana

1. Pārskatu veidotājā atveriet modificējamo rindas, kolonnas vai pārskatu koka definīciju.
2. Izvēlnē **Rediģēt** noklikšķiniet uz **Pārvaldīt dimensiju vērtību kopas**.
3. Dialoglodziņa **Pārvaldīt dimensiju vērtību kopas** laukā **Dimensija** atlasiet dimensijas tipu.
4. Atlasiet dzēšamo kopu un pēc tam noklikšķiniet uz **Dzēst**. Noklikšķiniet uz **Jā**, lai neatgriezeniski dzēstu dimensiju vērtību kopu.

## <a name="additional-resources"></a>Papildu resursi

[Finanšu pārskatu veidošana](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]