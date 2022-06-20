---
title: Dokumentācijas vai apmācības izveide ar uzdevuma reģistrētāju
description: Šajā rakstā ir izskaidrots, kādi ir Uzdevumu ierakstītāja un uzdevumu ceļveži, kā izveidot ierakstus un kā pielāgot Microsoft uzdevumu ceļvežus un iekļaut tos jūsu Palīdzībā.
author: josaw1
ms.date: 03/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysHelpSetup
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.custom: 25391
ms.assetid: 59bf39f8-1464-441e-8b23-9a856c73471b
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b556003edf2fe186f6b095e538f142fcf5a0bba5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891819"
---
# <a name="create-documentation-or-training-with-task-recorder"></a>Dokumentācijas vai apmācības izveide ar uzdevuma reģistrētāju

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Šajā rakstā ir izskaidrots, kādi ir Uzdevumu ierakstītāja un uzdevumu ceļveži, kā izveidot uzdevumu ierakstus un kā pielāgot Microsoft uzdevumu ceļvežus un iekļaut tos jūsu Palīdzībā.

> [!IMPORTANT]
> Varat ierakstīt savus uzdevumu ceļvežus programmatūrai Dynamics 365 Human Resources, bet pašlaik tos nevar saglabāt Biznesa procesu modelētāja (BPM) bibliotēkā vai atvērt no palīdzības rūts. Varat tos saglabāt lokāli vai kaut kur tīklā, un pēc tam tos atvērt un vēlreiz atskaņot, izmantojot līdzekli Uzdevumu ierakstītājs. 

## <a name="learn-about-task-recorder"></a>Uzdevumu ierakstītāja iepazīšana

Uzdevuma reģistrētājs ir rīks, ko varat lietot, lai reģistrētu darbības, kuras veicat preces lietotāja interfeisā (UI). Kad izmantojat uzdevuma reģistrētāju, tiek reģistrēti visi notikumi, ko veicat lietotāja interfeisā un kas tiek izpildīti attiecībā pret serveri — tostarp vērtību pievienošana, iestatījumu mainīšana, datu noņemšana. Ierakstītās darbības kopā tiek sauktas par *uzdevuma ierakstu*. Uzdevumu ierakstus var izmantot daudzos veidos:

-   **Uzdevumu ierakstus var atskaņot kā uzdevumu ceļvežus.** Uzdevumu ceļveži ir neatņemama palīdzības funkcionalitātes sastāvdaļa. Uzdevuma ceļvedis ir kontrolēts, strukturēts, interaktīvs līdzeklis, kas palīdz veikt biznesa procesa darbības. Lietotājs tiek instruēts izpildīt katru darbību, izmantojot uznirstošas uzvednes (jeb “burbuļus”), kas kā animācija tiek parādītas lietotāja interfeisā un norāda uz UI elementiem, ar kuriem lietotājam ir nepieciešams mijiedarboties. “Burbulis” arī sniedz informāciju par to, kā mijiedarboties ar attiecīgo elementu, piemēram, “Noklikšķiniet šeit” vai “Ievadiet vērtību šajā laukā”. Uzdevuma ceļvedis darbojas ar lietotāja pašreizējo datu kopu, un ievadītie dati tiek saglabāti lietotāja vidē.
-   **Uzdevumu ierakstus var saglabāt kā Word dokumentus.** Tādējādi varat ērti veidot drukājamus apmācību ceļvežus.

Varat izveidot pats savus uzdevumu ierakstus, atskaņot Microsoft nodrošinātos uzdevumu ierakstus vai modificēt Microsoft nodrošinātos uzdevumu ierakstus, lai atspoguļotu jūsu konfigurāciju. Plašāku informāciju par uzdevuma reģistrētāju skatiet rakstā [Uzdevuma reģistrētājs](task-recorder.md).

## <a name="plan-your-task-recording"></a>Jūsu uzdevuma ieraksta plānošana
Gan veidojot jaunu uzdevumu ierakstu, gan sava ieraksta pamatā izmantojot Microsoft uzdevuma ierakstu, paturiet prātā tālāk norādīto informāciju.

-   Plānojiet savu ierakstu tāpat, kā plānotu videoierakstu. Visus lēmumus pieņemiet jau iepriekš.
-   Izpildiet biznesa procesu vienu vai divas reizes, to neierakstot, lai izprastu visas darbības.
-   Kad veicat biznesa procesu pirms ierakstīšanas, ievērojiet, kur jūs izmantojat īsinājumtaustiņus vai taustiņu **Enter**, lai faktiskās ierakstīšanas laikā varētu izvairīties no to lietošanas.
-   Nosakiet tālāk minēto.
    -   Vai darbības vēlaties grupēt apakšuzdevumos? Apakšuzdevumi vizuāli atdala procesa sadaļas. Piemēram, ja veidojat ierakstu procesam “Preces izveidošana un izlaišana”, iespējams, vēlaties grupēt darbības, kas ir nepieciešamas preces izveidošanai, un pēc tam grupēt darbības, kas ir nepieciešamas preces izlaišanai. Apakšuzdevumi arī atvieglo garāku procesus lasīšanu.
    -   Vai vēlaties pievienot anotācijas; ja tā — kur? Papildinformāciju skatiet tālāk sadaļā “Izprotiet dažādos anotāciju tipus”.
    -   Kādas vērtības jūs pievienosiet dažādajos laukos, izpildot biznesa procesa darbības? Ieteicams zināt, ko jūs atlasīsiet vai ievadīsiet procesa izpildes laikā, lai ierakstīšanas laikā nevajadzētu atgriezties un meklēt vai labot kļūdas.

**Apraksts un anotācijas ir jāieraksta jau iepriekš**

-   Katra uzdevuma ierakstīšanas sākumā ir apraksta lauks, kurā varat ievadīt ieraksta ievadu. Aprakstu ieteicams jau iepriekš uzrakstīt un saglabāt atsevišķā dokumentā, lai to varētu kopēt un ielīmēt uzdevuma ierakstā, kad veicat ierakstīšanu. Tādējādi varat veltīt laiku teksta uzlabošanai, kad nenotiek ierakstīšanas process. Teksta izgriešana un ielīmēšana ierakstīšanas procesu padara ātrāku un mazina aizķeršanās.
-   Katrai uzdevuma ieraksta darbībai varat izveidot anotācijas. Uzdevuma ieraksta atskaņošanas laikā anotācijas tiek rādītas“burbulī” kā piezīmes virs vai zem attiecīgās darbības teksta. Skatot kā tekstu palīdzības rūtī, anotācijas tiek rādītas kā darbībā iekļauts teksts. Saistībā ar aprakstu — savas anotācijas ir ieteicams rakstīt un saglabāt atsevišķā dokumentā. Uzdevuma ierakstīšanas laikā izgrieziet un ielīmējiet anotācijas no šī dokumenta.

**Izprotiet dažādos anotāciju tipus** Visas anotācijas ir neobligātas. Pievienojiet tās tikai tad, ja tās lietotājam sniedz noderīgu informāciju.

-   **Virsraksts.** Virsraksta anotācija ir redzama pirms darbības teksta, ko uzdevumu reģistrētājs ģenerē automātiski. Uzdevuma ceļvedī virsraksta anotācija ir redzama virs automātiski ģenerētā teksta. Šī tipa anotāciju varat lietot, lai skaidrotu, kāpēc lietotājs izpilda attiecīgo darbību, vai lai sniegt papildu kontekstu.

Šī ir rediģēšanas rūts, kuru redzat, kad ieraksta veidošanas laikā pievienojat anotācijas. Ievadiet virsraksta anotāciju lodziņā **Virsraksts**. 

[![Rediģēšanas rūts ar virsraksta anotāciju.](./media/screen1.png)](./media/screen1.png) 

Šādi virsraksta anotācija izskatās uzdevuma ceļveža “burbulī”. 

[![Virsraksta anotācijas izskats uzdevumu rokasgrāmatā.](./media/screen2.png)](./media/screen2.png)

-   **Piezīmes.** Piezīmju anotācija ir redzama pēc darbības teksta, ko uzdevumu ierakstītājs ģenerē automātiski. Uzdevuma ceļvedī tā ir redzama tikai tad, ja uzdevuma ceļveža burbulī lietotājs noklikšķina uz saites **Rādīt vairāk**. Šī tipa anotāciju varat lietot, lai aprakstītu jebko, kas lietotājam būtu jāzina, izpildot attiecīgo darbību.

Šī ir rediģēšanas rūts, kuru redzat, kad ieraksta veidošanas laikā pievienojat anotācijas. Ievadiet piezīmju anotāciju lodziņā **Piezīmes**. 

[![Rediģēšanas rūts ar anotāciju piezīmju lodziņā.](./media/screen3.png)](./media/screen3.png) 

Šādi piezīmju anotācija izskatās uzdevuma ceļveža “burbulī”.

[![Piezīmju anotācijas izskats uzdevumu rokasgrāmatā.](./media/screen4.png)](./media/screen4.png)

-   **Informācijas darbība**: Šāda tipa anotācijas tiek izveidotas, ar peles labo pogu noklikšķinot uz vadīklas vai jebkurā vietā formā &lt; **Uzdevumu reģistrētājs** &lt; **Pievienot informācijas darbību.** Informācijas darbības tiek parādītas kā numurētas darbības jebkurā vietā, kur tās ievietojat, pat ja UI netika ierakstīta nekāda darbība. Varat pievienot formas līmeņa informācijas darbību vai ar vadīklu saistītu informācijas darbību. Ja informācijas darbība ir saistīta ar kādu formu, uzdevumu ceļveža atskaņošanas laikā uzdevumu ceļveža “burbulis” kļūst redzams kaut kur šajā formā, bez rādītāja. Ja informācijas darbība ir saistīta ar kādu vadīklu, uzdevuma ceļveža atskaņošanas laikā uzdevuma ceļveža “burbulis” norāda uz attiecīgo vadīklu. Palīdzības rūtī informācijas darbības anotācija tiek rādīta kā numurēta darbība ar jebkādu jūsu ievadīto tekstu. Informācijas darbības varat izmantot, lai lietotāju sagatavotu nākamajām darbībām, lai aprakstītu darbības, ko nepieciešams izpildīt ārpus programmas, vai lai atsauktos uz citiem ierakstiem (lai gan anotācijās nevar izveidot hipersaites).

**Nosakiet, cik ilgu ierakstu veidot**

-   Parasti lietotājs ierakstu lasīs vai atskaņos no sākuma līdz beigām, tāpēc nekombinējiet darbības vai uzdevumus, kurus labāk veikt atsevišķi.
-   Mēģiniet neierakstīt ilgu scenāriju, kurā ir iesaistīti vairāki pakārtotie procesi. Piemēram, ieraksta tēma “Klientu informācijas nodaļas darbība veikalā” ir pārāk plaša; sadaliet to īsākos uzdevumos, piemēram, “Pieņemt atgriešanas darbības” un “Pievienot dāvanu kartei”.
-   Ja kādu uzdevumu var izpildīt kā daļu no vairākiem atsevišķiem biznesa procesiem, izveidojiet tam atsevišķu ierakstu, un pēc tam uz to varat atsaukties citos ierakstos.
-   Ja process ietver vairākus uzdevumus, kurus persona, visticamāk, izpilda visus uzreiz, šos uzdevumus varat saglabāt vienā ierakstā, piemēram, “Iestatīt un piešķirt funkcionalitātes profilus”.
-   Ja ir jāieraksta kaut kas, ko persona izpilda vienreiz (piemēram, konfigurēšana), un pēc tam vēl viens uzdevums, ko var darīt uzreiz pēc tam, bet ko var darīt atkārtoti un vienu pašu, sadaliet tos divos uzdevumu ierakstos.

**Izlemiet, kurā UI vietā sākt ierakstīšanu** Uzdevuma ieraksta veidošanas sākumā atvērtā lapa ietekmē to, kurai lapai šis uzdevuma ceļvedis tiek rādīts. Piemēram, ja vēlaties, lai jūsu uzdevuma ieraksts tiktu rādīts palīdzības rūtī, kad lietotājs noklikšķina uz palīdzības lapā Virsgrāmatas parametri, ierakstīšana ir jāsāk lapā Virsgrāmatas parametri. **Saglabājiet ierakstus kā .axtr failus** Kad esat pabeidzis veidot vai rediģēt uzdevumu ierakstu, jums tiek sniegtas vairākas opcijas veidam, kā šo ierakstu vēlaties lejupielādēt vai saglabāt. Failu varat lejupielādēt kā uzdevuma ieraksta pakotni (.axtr), to lejupielādēt kā neapstrādātu ieraksta failu (.xml), to lejupielādēt kā Word dokumentu vai failu saglabāt LCS bibliotēkā. Vienmēr ieteicams savu uzdevuma ierakstu saglabāt kā uzdevuma ieraksta pakotnes failu (.axtr). Šādi tiek vienkāršota faila uzturēšana, ja vēlāk nepieciešams mainīt procedūras vai anotācijas. Ja failu vēlaties lejupielādēt kā Word dokumentu, saglabājiet to arī kā uzdevumu ieraksta pakotnes failu.

## <a name="create-your-task-recording"></a>Sava uzdevuma ieraksta izveidošana
Detalizētus norādījumus par izpildīšanu skatiet rakstā [Uzdevuma ierakstu resursi](task-recorder.md).

## <a name="copy-and-customize-microsofts-task-recordings"></a>Microsoft uzdevumu ierakstu kopēšana un pielāgošana
Varat lejupielādēt un rediģēt Microsoft uzdevumu ierakstus, lai tos izmantotu savai palīdzības dokumentācijai vai apmācību materiāliem. Lai lejupielādētu Microsoft uzdevumu ierakstu, rīkojieties šādi:

1.  Atveriet uzdevumu reģistrētāju. Uzdevumu ierakstītājs atrodas izvēlnē **Iestatījumi**.
2.  Uzdevumu ierakstītāja rūtī noklikšķiniet uz **Uzturēt ierakstu.**
3.  Sadaļā **Kur ir šis ieraksts?** noklikšķiniet uz **Tas ir LCS bibliotēkā**.
4.  Noklikšķiniet uz **Atlasīt LCS bibliotēku**.
5.  Atlasiet Microsoft globālo bibliotēku.
6.  Koka skatā atlasiet biznesa procesu bibliotēkas zaru, ar kuru ir saistīts šis uzdevuma ieraksts.
7.  Noklikšķiniet uz **Labi**.
8.  Noklikšķiniet uz **Sākt**.
9.  Šajā brīdī izpētiet ierakstu, mainot visas darbības, kuras grasāties ierakstīt vēlreiz. **Piezīme**. Ja nepieciešams mainīt tikai ierakstu tekstu, ierakstu varat atvērt režīmā **Rediģēt ieraksta anotācijas**, un pēc tam saglabājiet to.
10. Kad ierakstu esat atskaņojis līdz galam, uzdevumu ierakstītāja joslā ekrāna augšpusē noklikšķiniet uz **Apturēt**.
11. Izvēlieties, kā vēlaties saglabāt šo uzdevuma ierakstu.



## <a name="additional-resources"></a>Papildu resursi

[Palīdzības sistēma](../../fin-ops/get-started/help-overview.md)

[Savienojuma izveide ar palīdzības sistēmu](../../fin-ops/get-started/help-connect.md)

[Uzdevuma reģistrētājs](task-recorder.md)

[Bagātinātu palīdzības tēmu izveide ar uzdevumu reģistrētāju (ārējās saite)](https://mbspartner.microsoft.com/AX/Videos/970)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]