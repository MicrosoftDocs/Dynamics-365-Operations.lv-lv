---
title: "Dokumentācijas vai apmācības veidošana, izmantojot uzdevumu ierakstus"
description: "Šajā tēmā ir paskaidrots, kāda uzdevuma rakstītāju un rokasgrāmatas uzdevums ir, kā izveidot uzdevumu ierakstus, un kā pielāgot Microsoft uzdevumu ceļveži un tos iekļaut jūsu palīdzību."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysHelpSetup
audience: Application User, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25391
ms.assetid: 59bf39f8-1464-441e-8b23-9a856c73471b
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: 38bce4a843f0db575c8d1ba08b7dc2ece8366663
ms.lasthandoff: 03/31/2017


---

# <a name="create-documentation-or-training-using-task-recordings"></a>Dokumentācijas vai apmācības veidošana, izmantojot uzdevumu ierakstus
Šajā tēmā ir paskaidrots, kāda uzdevuma rakstītāju un rokasgrāmatas uzdevums ir, kā izveidot uzdevumu ierakstus, un kā pielāgot Microsoft uzdevumu ceļveži un tos iekļaut jūsu palīdzību.

<a name="learn-about-task-recorder"></a>Uzdevumu ierakstītāja iepazīšana
-------------------------

Ierakstīšanas iekārtas uzdevums ir Microsoft Dynamics 365 par darbībām rīks, ko var lietot, lai ierakstītu darbības, ko izmantot produkta lietotāja interfeisa (UI). Kad izmantojat uzdevumu ierakstītāju, tiek uzņemti visi notikumi, ko veicat UI un kas tiek izpildīti attiecībā pret serveri — tostarp vērtību pievienošana, iestatījumu mainīšana, datu noņemšana. Ierakstītās darbības kopā tiek sauktas par *uzdevuma ierakstu*. Uzdevumu ierakstus var izmantot daudzos veidos:

-   **Uzdevumu ierakstus var atskaņot kā uzdevumu ceļvežus.** Rokasgrāmatas uzdevums ir neatņemama gabals Dynamics 365 operāciju palīdzību pieredzes. Uzdevuma guide ir kontrolēta, ekskursija, interaktīvo pieredzi biznesa procesa soļus. Lietotājs tiek instruēts izpildīt katru darbību, izmantojot uznirstošas uzvednes (jeb “burbuļus”), kas kā animācija tiek parādītas lietotāja interfeisā un norāda uz UI elementiem, ar kuriem lietotājam ir nepieciešams mijiedarboties. "Burbulis" sniedz arī informāciju par mijiedarbību ar elementu, piemēram, "Noklikšķiniet šeit" vai "Šajā laukā ievadīt vērtību." Uzdevuma rokasgrāmata darbojas pret pašreizējo lietotāja datu kopai un ir ievadītie dati tiek saglabāti lietotāja darba vide.
-   **Uzdevumu ierakstus var tikt skatīti kā procesuālus pasākumus palīdzības rūtī.** Palīdzības rūti var izmantot, lai meklētu un parādīt uzdevumu ierakstiem. Palīdzības rūts var piekļūt, noklikšķinot uz **?** Ikonas augšējo navigācijas joslu, vai jūs varat izmantot īsinājumtaustiņu kombinācija, **Ctrl + Shift +?**. Soļi uzdevuma reģistrēšana palīdzības rūtī varat lasīt, vai jūs varat izvēlēties, lai demonstrētu ierakstu kā uzdevumu guide, tāpēc tā vada jūs cauri UI.
-   **Uzdevumu ierakstus var saglabāt uz BPM.** Savu uzdevuma ierakstu varat saglabāt kādā Biznesa procesu modelētāja (BPM) bibliotēkas hierarhijas rindā pakalpojumos Lifecycle Services (LCS). No ieraksta tiks ģenerēts darbību saraksts un biznesa procesu plūsmas diagramma. Uzdevumu ierakstus, BPM bibliotēkā saglabātās redzami Dynamics 365 darbībās, kā palīdzēt.
-   **Uzdevumu ierakstus var saglabāt kā Word dokumentus.** Tādējādi varat ērti veidot drukājamus apmācību ceļvežus.

Var izveidot savu uzdevumu ierakstus, demonstrēt uzdevumu ierakstus, ko nodrošina Microsoft vai modificēt Microsoft nodrošinātajiem uzdevumu ieraksti atspoguļo jūsu konfigurāciju. Papildinformāciju par uzdevumu rakstītājs, skatiet [uzdevumu ierakstītājs programmā Dynamics 365 operācijām](task-recorder.md).

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
-   Katrai uzdevuma ieraksta darbībai varat izveidot anotācijas. Uzdevuma ieraksta atskaņošanas laikā anotācijas tiek rādītas“burbulī” kā piezīmes virs vai zem attiecīgās darbības teksta. Skatoties kā palīdzības rūtī teksts, anotācijas tiek parādīti kā teksts iekļauts darbībā. Saistībā ar aprakstu — savas anotācijas ir ieteicams rakstīt un saglabāt atsevišķā dokumentā. Uzdevuma ierakstīšanas laikā izgrieziet un ielīmējiet anotācijas no šī dokumenta.

**Izprotiet dažādos anotāciju tipus** Visas anotācijas ir neobligātas. Pievienojiet tās tikai tad, ja tās lietotājam sniedz noderīgu informāciju.

-   **Nosaukums**: virsrakstu anotācija parādīsies pirms darbības teksts, kas uzdevumu ierakstīšanas iekārta automātiski ģenerē. Ceļvedī uzdevumu anotācijas virsraksts parādās virs automātiski izveidotu tekstu. Šī tipa anotāciju varat lietot, lai skaidrotu, kāpēc lietotājs izpilda attiecīgo darbību, vai lai sniegt papildu kontekstu.

Šī ir rediģēšanas rūts, kuru redzat, kad ieraksta veidošanas laikā pievienojat anotācijas. Ievadiet virsraksta anotāciju lodziņā **Virsraksts**. 

[![screen1](./media/screen1.png)](./media/screen1.png) 

Šādi virsraksta anotācija izskatās uzdevuma ceļveža “burbulī”. 

[![screen2](./media/screen2.png)](./media/screen2.png)

-   **Piezīmes.** Piezīmju anotācija ir redzama pēc darbības teksta, ko uzdevumu ierakstītājs ģenerē automātiski. Uzdevuma ceļvedī tā ir redzama tikai tad, ja uzdevuma ceļveža burbulī lietotājs noklikšķina uz saites **Rādīt vairāk**. Šī tipa anotāciju varat lietot, lai aprakstītu jebko, kas lietotājam būtu jāzina, izpildot attiecīgo darbību.

Šī ir rediģēšanas rūts, kuru redzat, kad ieraksta veidošanas laikā pievienojat anotācijas. Ievadiet piezīmju anotāciju lodziņā **Piezīmes**. 

[![screen3](./media/screen3.png)](./media/screen3.png) 

Tas ir kā piezīmes anotācija izskatās "burbulis" uzdevumu rokasgrāmatā.

[![screen4](./media/screen4.png)](./media/screen4.png)

-   **Info soli**: šīs anotācijas tiek veidotas tiesības noklikšķinot uz vadīklas vai jebkurā formā &lt;**uzdevumu rakstītāju**&lt; * * Add info soli. * * Info darbības parādās kā numurētu soli jebkurā brīdī to ievietot, kaut arī nekāda darbība tika ierakstīts UI. Varat pievienot formas līmeņa informācijas darbību vai ar vadīklu saistītu informācijas darbību. Ja informācijas darbība ir saistīta ar kādu formu, uzdevumu ceļveža atskaņošanas laikā uzdevumu ceļveža “burbulis” kļūst redzams kaut kur šajā formā, bez rādītāja. Ja info pasākums ir saistīts ar vadīklu, uzdevumu rokasgrāmata "burbulis" norādīs vadības atskaņojot uzdevumu rokasgrāmata. Rūtī palīdzība info solis anotācijas parādīsies kā numurētās soli ar tekstu, ko esat ievadījis. Lietojiet informācijas pasākumus, lai sagatavotu lietotājam par nākamajiem soļiem, apraksta pasākumus, kas jāveic ārpus Dynamics 365 operācijām, vai atsaukties uz citiem ierakstiem (lai gan nevar izveidot hyperinks anotācijas.).

**Nosakiet, cik ilgu ierakstu veidot**

-   Parasti lietotājs ierakstu lasīs vai atskaņos no sākuma līdz beigām, tāpēc nekombinējiet darbības vai uzdevumus, kurus labāk veikt atsevišķi.
-   Mēģiniet neierakstīt ilgu scenāriju, kurā ir iesaistīti vairāki pakārtotie procesi. Piemēram, ieraksta tēma “Klientu informācijas nodaļas darbība veikalā” ir pārāk plaša; sadaliet to īsākos uzdevumos, piemēram, “Pieņemt atgriešanas darbības” un “Pievienot dāvanu kartei”.
-   Ja kādu uzdevumu var izpildīt kā daļu no vairākiem atsevišķiem biznesa procesiem, izveidojiet tam atsevišķu ierakstu, un pēc tam uz to varat atsaukties citos ierakstos.
-   Ja process ietver vairākus uzdevumus, kurus persona, visticamāk, izpilda visus uzreiz, šos uzdevumus varat saglabāt vienā ierakstā, piemēram, “Iestatīt un piešķirt funkcionalitātes profilus”.
-   Ja ir jāieraksta kaut kas, ko persona izpilda vienreiz (piemēram, konfigurēšana), un pēc tam vēl viens uzdevums, ko var darīt uzreiz pēc tam, bet ko var darīt atkārtoti un vienu pašu, sadaliet tos divos uzdevumu ierakstos.

**Izlemt, kur UI, lai startētu ierakstīšanu** lapu, kurā atrodaties, kad jūs sāktu ierakstīšanu uzdevuma ierakstu ietekmē kurā lappusē tiek rādīts uzdevuma rokasgrāmata. Piemēram, ja vēlaties, lai jūsu uzdevuma reģistrēšana minētas palīdzības rūts, kad lietotājs noklikšķina uz palīdzības lapā Virsgrāmatas parametri, jums jāsāk jūsu reģistrācijas lapā Virsgrāmatas parametri. **Saglabājiet ierakstus kā .axtr failus** Kad esat pabeidzis veidot vai rediģēt uzdevumu ierakstu, jums tiek sniegtas vairākas opcijas veidam, kā šo ierakstu vēlaties lejupielādēt vai saglabāt. Failu varat lejupielādēt kā uzdevuma ieraksta pakotni (.axtr), to lejupielādēt kā neapstrādātu ieraksta failu (.xml), to lejupielādēt kā Word dokumentu vai failu saglabāt LCS bibliotēkā. Vienmēr ieteicams savu uzdevuma ierakstu saglabāt kā uzdevuma ieraksta pakotnes failu (.axtr). Šādi tiek vienkāršota faila uzturēšana, ja vēlāk nepieciešams mainīt procedūras vai anotācijas. Ja failu vēlaties lejupielādēt kā Word dokumentu, saglabājiet to arī kā uzdevumu ieraksta pakotnes failu.

## <a name="create-your-task-recording"></a>Sava uzdevuma ieraksta izveidošana
Arkveida detalizētu pakāpieni, skatiet [ģKā izveidot uzdevuma ierakstu,](task-recorder.md).

## <a name="copy-and-customize-microsofts-task-recordings"></a>Microsoft uzdevumu ierakstu kopēšana un pielāgošana
Jūs varat lejupielādēt un rediģēt Microsoft uzdevumu ierakstus vai tos izmanto savu palīdzības dokumentācijā vai mācību materiāli. Lai lejupielādētu Microsoft uzdevumu ierakstu, rīkojieties šādi:

1.  Dynamics 365 operācijām, atveriet uzdevumu rakstītāju. Uzdevumu ierakstītājs atrodas izvēlnē **Iestatījumi**.
2.  Uzdevumu ierakstītāja rūtī noklikšķiniet uz **Uzturēt ierakstu.**
3.  Sadaļā **Kur ir šis ieraksts?** noklikšķiniet uz **Tas ir LCS bibliotēkā**.
4.  Noklikšķiniet uz **Atlasīt LCS bibliotēku**.
5.  Atlasiet Microsoft global bibliotēka.
6.  Koka skatā atlasiet biznesa procesu bibliotēkas zaru, ar kuru ir saistīts šis uzdevuma ieraksts.
7.  Noklikšķiniet uz **OK**.
8.  Noklikšķiniet uz **Sākt**.
9.  Šajā brīdī, ierakstīšana, maiņa nekādas darbības, kā jums iet ierakstiet to vēlreiz pārskatītu. **Piezīme**: ja vēlaties mainīt ierakstu teksta, jūs varat atvērt ierakstu **labot ierakstu anotāciju** režīmā, un pēc tam saglabājiet to.
10. Kad ierakstu esat atskaņojis līdz galam, uzdevumu ierakstītāja joslā ekrāna augšpusē noklikšķiniet uz **Apturēt**.
11. Izvēlieties, kā vēlaties saglabāt šo uzdevuma ierakstu.

## <a name="include-your-task-recordings-in-the-help-pane"></a>Palīdzības rūts iekļaut uzdevumu ierakstiem
Parādīt palīdzības rūts pielāgotajām uzdevumu ierakstus, tā, ka viņi var atskaņots kā uzdevumu rokasgrāmatas vai skatīt kā tekstu, BPM bibliotēkā saglabāt uzdevumu ierakstus un pēc tam atjauniniet palīdzības sistēmas parametriem, norādīt uz bibliotēkā BPM. Lai iegūtu papildinformāciju, skatiet [savienojumu ir palīdzības sistēma.](../get-started/help-connect.md)

<a name="see-also"></a>Skatiet arī
--------

[Dynamics 365 operācijām palīdzēt](..\get-started\help-overview.md)

[Izveidot savienojumu ar palīdzības](..\get-started\help-connect.md)

[Uzdevuma ierakstītājs programmā Dynamics 365 operācijām](task-recorder.md)

[Nesen pievienotās uzdevums ierakstīšanas iekārtas funkcijas](\core\get-started\recently-added-editing-features-in-task-recorder)

[Izveidojot jaunu apmācību bibliotēkās Dynamics AX Lifecycle dienestos, izmantojot uzdevuma ierakstītāju (ārējā saite)](https://docs.com/mufife/163372c6-f366-4c5a-94fa-93e2c25f878a/creating-new-training-libraries-for-dynamics-ax)

[Izveidotu Rich palīdzības tēmas ar uzdevumu rakstītāju (ārējā saite)](https://mbspartner.microsoft.com/AX/Videos/970)


