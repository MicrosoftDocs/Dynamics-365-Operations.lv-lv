---
title: Uzlabot ER risinājumu veiktspēju, samazinot izpildlaikā ienesto tabulas lauku skaitu
description: Šajā rakstā skaidrots, kā jūs varat palīdzēt uzlabot veiktspēju, samazinot tabulas lauku skaitu, kas tiek ienests izpildlaikā.
author: kfend
ms.date: 05/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.28
ms.custom: ''
ms.assetid: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
ms.openlocfilehash: 5c9481f1021a5dba6e1d4020bbf85a10bd551ac0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278832"
---
# <a name="improve-performance-of-er-solutions-by-reducing-the-number-of-table-fields-that-are-fetched-at-runtime"></a>Uzlabot ER risinājumu veiktspēju, samazinot izpildlaikā ienesto tabulas lauku skaitu

[!include[banner](../includes/banner.md)]

Varat projektēt elektronisko [pārskatu (](general-electronic-reporting.md) ER) formātus [...](er-overview-components.md#format-components-for-outgoing-electronic-documents), kas ģenerē izejošos dokumentus dažādos formātos. Kad dokuments ir ģenerēts, ER formāts izsauc datu avotus, kas tika konfigurēti atbilstošā ER modeļa [kartēšanā](er-overview-components.md#model-mapping-component). Lai konfigurētu piekļuvi programmas tabulām, vaicājumiem vai entītijām ierakstu izgūšanai, varat izmantot tabulas ierakstu tipa ER *datu avotus*. Pēc noklusējuma tabulas ierakstu tipa *datu avots* izgūst visu lauku vērtības pieprasītajā ierakstos. Tomēr šī tipa datu avotu var konfigurēt tā, lai inesekotu tikai lauka vērtības, kas nepieciešamas palaistam ER formātam. Šī konfigurācija palīdz samazināt atmiņas patēriņu programmas serverim, kas veic datu izgūšanu un turpmāku ierakstīšanas kešdarbi.

Lai uzzinātu vairāk par to, kā *ierobežot datu avotu ieneses lauku sarakstu tabulas ierakstu tipam*, izpildiet šajā rakstā minēto piemēru.

## <a name="example-reduce-the-number-of-table-fields-that-are-fetched-at-runtime"></a>Piemērs: samazināt izpildlaikā ienesto tabulas lauku skaitu

Šīs procedūras parāda, kā lietotājs sistēmas administratora vai elektronisko pārskatu izstrādātāja lomā var konfigurēt ER modeļa kartējumu, lai tas iedietu tikai tos laukus, kas nepieciešami ER formāta palaišanai, lai palīdzētu samazināt programmas servera atmiņas patēriņu.

Šīs procedūras var veikt **USMF uzņēmumā** Microsoft Dynamics 365 Finansēs. Kodēšana nav nepieciešama.

Lai pabeigtu šo piemēru, ir nepieciešama piekļuve USMF **uzņēmumam** vienai no šīm lomām:

- Elektronisko pārskatu veidošanas funkcionālais konsultants
- Sistēmas administrators

Šajā piemērā izmantosiet ER konfigurācijas [, kas](general-electronic-reporting.md#Configuration) ir paredzētas **uzņēmumam Litware, Inc.** sample. Pārliecinieties, vai **Litware, Inc.** (`http://www.litware.com`) parauga uzņēmuma konfigurācijas nodrošinātājs ir norādīts ER struktūrā un vai tas ir atzīmēts kā **aktīvs**. Ja šī konfigurācijas nodrošinātāja nav **uzskaitīts** vai arī tas nav atzīmēts kā aktīvs, [izpildiet darbības, kas norādītas Sadaļā Konfigurācijas nodrošinātāja izveide un atzīmējiet to kā aktīvu](tasks/er-configuration-provider-mark-it-active-2016-11.md).

### <a name="configure-the-er-framework"></a>ER struktūras konfigurēšana

Izpildiet sadaļā [ER struktūras konfigurēšana](er-quick-start2-customize-report.md#ConfigureFramework) norādītās darbības, lai iestatītu ER parametru minimālo kopu. Šis iestatījums jāpabeidz, pirms sākat lietot ER struktūru, lai modificētu nodrošinātā ER risinājuma datu avotus.

### <a name="import-the-sample-er-configurations"></a>Parauga ER konfigurācijas failu importēšana

Ja neesat [izpildījis piemērus jaunā ER risinājuma izstrādāšanā, lai izdrukātu pielāgotu pārskata rakstu, lejupielādējiet un lokāli saglabājiet XML failus šādām ER](er-quick-start1-new-solution.md) risinājuma konfigurācijām.

| Satura apraksts            | Faila nosaukums |
|--------------------------------|-----------|
| ER datu modeļa konfigurācija    | [Anketas model.version.1.xml](https://download.microsoft.com/download/b/6/3/b633bd34-d200-4422-96d9-8f62eb5218f8/Questionnaires_model.version.1.xml) |
| ER modeļa kartējuma konfigurācija | [Anketu kartēšana.versija.1.1.xml](https://download.microsoft.com/download/7/b/2/7b258e4e-4bd5-46a4-8114-27419ae4acd8/Questionnaires_mapping.version.1.1.xml) |
| ER formāta konfigurācija        | [Anketas format.version.1.1.xml](https://download.microsoft.com/download/1/b/a/1ba39ec2-257a-44d8-972f-25bf7d18fb41/Questionnaires_format.version.1.1.xml) |

Pēc tam veiciet šos soļus, lai augšupielādētu finanšu instancei paredzētā ER risinājuma konfigurācijas.

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Atlasiet **Pārskatu konfigurācijas**.
3. Konfigurāciju lapā **importējiet** ER datu modeļa konfigurāciju.

    1. Atlasiet **Apmaiņa**, un pēc tam atlasiet **Ielādēt no XML faila**.
    2. Atlasiet **Pārlūkot**, atrast un atlasīt **anketu modeļa.versijas.1.xml** failu un pēc tam atlasiet **Labi**.

4. Importēt ER modeļa kartēšanas konfigurāciju.

    1. Atlasiet **Apmaiņa**, un pēc tam atlasiet **Ielādēt no XML faila**.
    2. Atlasiet **Pārlūkot**, atrast un atlasīt **anketu kartēšanu.1.1.xml** un pēc tam atlasiet **Labi**.

5. Importēt ER formāta konfigurāciju.

    1. Atlasiet **Apmaiņa**, un pēc tam atlasiet **Ielādēt no XML faila**.
    2. Atlasiet **Pārlūkot**, atrast un atlasīt **anketu formātu.1.1.xml** un pēc tam atlasiet **Labi**.

6. Konfigurācijas kokā izvērsiet **anketu modeli**.
7. Konfigurāciju kokā pārskatiet importējamo ER konfigurāciju sarakstu.

    ![Pārskatīt importēto ER konfigurāciju sarakstu konfigurāciju lapā Konfigurācijas.](./media/er-reduce-fetched-fields-number-configurations.png)

### <a name="review-the-provided-er-model-mapping"></a>Pārskatīt sniegto ER modeļa kartējumu

1. Lapā Konfigurācijas **atlasiet** Anketu **kartēšana**.
2. Darbību rūtī atlasiet **Noformētājs**.
3. Lapā Modelis **uz datu avota kartēšanu** atlasiet **Veidotājs**.
4. Modeļu kartēšanas **veidotāja** lapā Darbību rūtī atlasiet Grupas skats, **lai** ieslēgtu **grupas** skatu.
5. Datu modeļa **rūtī izvērsiet** **Anketu.**

    Ievērojiet, ka **anketas** datu avots ir konfigurēts, lai piekļūtu pieteikumu `KMCollection` tabulai.

6. Datu avotu **rūtī izvērsiet** tabulas ierakstus **anketas** \> **laukos** \> **·**.

    Ņemiet vērā, cik laukus `KMCollection` no programmas tabulas atklāj tabulas **ierakstu** tipa anketas *datu* avots.

    ![Pārskatiet sniegto modeļa kartējumu modeļu kartēšanas veidotāja lapā, kad grupas skats ir ieslēgts.](./media/er-reduce-fetched-fields-number-mapping1.png)

7. Darbību rūtī vēlreiz atlasiet Grupas skats **, lai** izslēgtu grupas **skatu**, un pēc tam atlasiet Rādīt **visu tikai** \> **kartēto**.

    Ievērojiet, ka daži pieteikuma tabulas `KMCollection` lauki tiek izmantoti, lai aizpildītu **anketas** ierakstu sarakstu ER datu modelī:

    - `Active`
    - `Description`
    - `questionMode`
    - `kmCollectionId`

    ![Pārskatiet sniegto modeļa kartējumu modeļu kartēšanas veidotāja lapā, kad grupas skats ir izslēgts.](./media/er-reduce-fetched-fields-number-mapping2.png)

### <a name="turn-on-the-er-performance-trace"></a>ER veiktspējas izsekošanas ieslēgšana

Lai iestatītu [ER](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) lietotāja parametrus, kas iespējo ER komponentu izpildes izsekošanu, rīkojieties saskaņā ar soļiem.

### <a name="run-the-provided-er-format-by-using-the-provided-model-mapping"></a>Palaist sniegto ER formātu, izmantojot sniegto modeļa kartēšanu

Izpildiet darbības, [kas izpildiet sadaļā Palaist noformētu formātu no ER](er-quick-start1-new-solution.md#RunFormatFromER), lai palaistu sniegto ER formātu atsevišķai anketai no **konfigurāciju** lapas.

### <a name="review-the-execution-trace-of-the-first-run"></a>Pārskatīt pirmās izpildes izpildes izsekošanu

1. Doties uz **organizācijas administrēšanas** \> **elektronisko pārskatu \> konfigurācijām.**
2. Lapā Konfigurācijas **izvērsiet** anketu **modeli un atlasiet** Anketu **kartēšanu**.

    > [!NOTE]
    > Detalizēta informācija kopsavilkuma cilnē **Versijas** norāda, ka atlasījāt anketu kartēšanas **konfigurācijas melnraksta** versiju. Tāpēc jūs varat modificēt šī modeļa kartēšanas saturu.

3. Darbību rūtī atlasiet **Noformētājs**.
4. Lapā Modelis **uz datu avota kartēšanu** atlasiet **Veidotājs**.
5. Lapā **Modeļa kartējuma noformētājs**, darbību rūtī atlasiet **Veiktspējas izsekošana**.
6. **Dialoglodziņā Veiktspējas izsekošanas rezultātu** iestatījumi atlasiet izsekošanu, kas tika ģenerēta pēdējā formāta izpildes laikā.

    ![Izsekošanas atlasīšana veiktspējas izsekošanas rezultātu iestatījumu dialoglodziņā.](./media/er-reduce-fetched-fields-number-select-trace-1.png)

7. Atlasiet **Labi**. 
8. Kopsavilkuma cilnē **Detalizēta** informācija filtrējiet anketas **ceļu**, kas norāda uz anketas **datu** avotu.
9. Pārskatiet tās datu bāzes vaicājuma detaļas, kas tika ģenerētas, izsaucot **anketas** datu avotu.

    Ņemiet vērā, ka visi programmas `KMCollection` tabulas lauki tika ienesti izpildlaikā, kad tika **izsaukts** anketas datu avots.

    ![Pārskatiet datu bāzes vaicājuma detaļas modeļu kartēšanas veidotāja lapā.](./media/er-reduce-fetched-fields-number-query1.png)

### <a name="modify-the-provided-er-model-mapping"></a>Modificēt sniegto ER modeļa kartējumu

1. Modeļu kartēšanas **veidotāja** lapā datu **avotu** rūtī atlasiet anketas **datu** avotu.
2. **Datu avotu rūtī** atlasiet **Rediģēt**.
3. Datu avota rekvizītu dialoglodziņā atlasiet laukus, lai norādītu to **lauku sarakstu programmas tabulā, uz kuru ir atsauce, kura tiks izgūta izpildlaikā,** **kad tiks izsaukts rediģējamais**`KMCollection` anketas datu avots.**·**

    ![Atlasot Opciju Atlasīt laukus datu avota rekvizītu dialoglodziņā, lai sāktu to lauku saraksta konfigurēšanu, kas tiks ienesti no programmas tabulas, izmantojot rediģējamo datu avotu.](./media/er-reduce-fetched-fields-number-select-fields1.png)

4. Lapā Atlasīt **laukus** atlasiet Automātiskā **uzpildīšana**.

    Atlasītais **lauku** saraksts tiek aizpildīts automātiski, pamatojoties uz iepriekš konfigurētiem modeļa kartēšanas artefaktiem. Sarakstam tiek pievienoti visi atsauču tabulas lauki un saites, kas ir minētas jebkurā saistīšanā, formulā vai modeļu kartēšanas datu avotā.

    ![Notiek to lauku saraksta konfigurēšana, kas tiks ienesti no programmas tabulas lapā Atlasīt laukus.](./media/er-reduce-fetched-fields-number-select-fields2.png)

5. Atlasiet **Saglabāt** un aizvērt lapu Atlasīt **laukus**.
6. Atlasiet **Labi**, lai saglabātu izmaiņas, ko veicāt datu avota iestatījumos.
7. Darbību rūtī atlasiet Rādīt **visu**.

    Ņemiet vērā, **ka** anketas datu avots tagad rāda tekstu **\<Fields are filtered\>**. Šis teksts norāda, ka datu avots ir konfigurēts, lai ienestu ierobežotu lauku skaitu no programmas, uz kuru ir atsauces.

    ![Pārskatīt atjaunināto modeļu kartējumu modeļu kartēšanas veidotāja lapā.](./media/er-reduce-fetched-fields-number-mapping3.png)

8. Atlasiet **Saglabāt**, lai saglabātu izmaiņas, ko veicāt rediģējamā modeļa kartēšanā.

    > [!NOTE]
    > Izpildlaikā ER analizē pievienotās relācijas un pievieno visus laukus, kas tiek izmantoti tos datu bāzes vaicājumam, pat ja šie lauki nav skaidri pievienoti ienesto lauku sarakstam noformēšanas laikā.

### <a name="run-the-provided-er-format-by-using-the-updated-model-mapping"></a>Palaist sniegto ER formātu, izmantojot atjaunināto modeļu kartēšanu

Izpildiet darbības, [kas izpildiet sadaļā Palaist noformētu formātu no ER](er-quick-start1-new-solution.md#RunFormatFromER), lai palaistu sniegto ER formātu atsevišķai anketai no **konfigurāciju** lapas.

### <a name="review-the-execution-trace-of-the-second-run"></a>Pārskatīt otrās izpildes izpildes izsekošanu

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā Konfigurācijas **izvērsiet** anketu **modeli un atlasiet** Anketu **kartēšanu**.
3. Darbību rūtī atlasiet **Noformētājs**.
4. Lapā Modelis **uz datu avota kartēšanu** atlasiet **Veidotājs**.
5. Lapā **Modeļa kartējuma noformētājs**, darbību rūtī atlasiet **Veiktspējas izsekošana**.
6. **Dialoglodziņā Veiktspējas izsekošanas rezultātu** iestatījumi atlasiet izsekošanu, kas tika ģenerēta pēdējā formāta izpildes laikā.
7. Atlasiet **Labi**.
8. Kopsavilkuma cilnē **Detalizēta** informācija filtrējiet anketas **ceļu**, kas norāda uz anketas **datu** avotu.
9. Pārskatiet tās datu bāzes vaicājuma detaļas, kas tika ģenerētas, izsaucot **anketas** datu avotu.

    Ievērojiet, ka izpildlaikā `KMCollection`**no** programmas tabulas tika ienesti tikai tie lauki, kas nepieciešami datu avota aizpildīšanai, kad tika izsaukts anketas datu avots.

    > [!NOTE]
    > Daļa lauku, piemēram, nodalījuma ID lauku, datu apgabala ID un ieraksta ID, automātiski tiek pievienoti, izmantojot Finanšu programmas datu pārvaldības struktūru.

    ![Pārskata datu bāzes vaicājuma detaļas par atjaunināto modeļa kartēšanu modeļu kartēšanas veidotāja lapā.](./media/er-reduce-fetched-fields-number-query2.png)

Šo tehniku varat izmantot, lai samazinātu ienesto ierakstu skaitu, ja jāsamazina atmiņas patēriņš, palaižot ER modeļa kartēšanu un ER formātu.

## <a name="limitations"></a>Ierobežojumi

*Ierobežojot* ienesto lauku skaitu tabulas ierakstu tipa datu avotam, nevar izmantot tās programmas tabulas metodes, uz kuru attiecas datu avots, jo programmas metadati nesniedz informāciju par tabulas laukiem, kas ir nepieciešami šo metožu izsaukšanai.

## <a name="usage-notes"></a>Lietošanas piezīmes

Lai arī **automātiskās uzpildes** komanda automātiski pievieno laukus, iepriekš pievienotie lauki netiek automātiski dzēsti, pat ja tie vairs netiek izmantoti saistīšanā, formulās un rediģējamo modeļu kartēšanas datu avotos.

Atlasot **Uzpildīšanu**, ER analizē saistījumus, formulas un datu avotus, kas bija rediģējamā modeļa kartēšanai, kad to atvērāt rediģēšanai. Ja maināt rediģējama modeļa kartēšanas saistījumus, formulas un datu avotus un vēlaties izmantot komandu Automātiskā piepildīšana, aizveriet modeļu kartēšanas veidotāju un pēc tam vēlreiz atveriet **to**, lai rediģētu modeļa kartēšanu. 

## <a name="additional-resources"></a>Papildu resursi

- [Elektronisko atskaišu veidošanas (ER) formāta failu izpildes uzraudzīšana, lai novērstu veiktspējas problēmas](trace-execution-er-troubleshoot-perf.md)
- [Veiktspējas problēmu novēršana ER konfigurācijās](er-troubleshoot-perf-issues-in-configurations.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
