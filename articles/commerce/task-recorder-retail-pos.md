---
title: Retail Modern POS (MPOS) un Cloud POS uzdevumu ierakstītājs un palīdzība
description: Šajā rakstā ir aprakstīts, kā izmantot uzdevumu ierakstītāju mākonī Retail Modern POS POS un tajā.
author: josaw1
ms.date: 06/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 1205393
ms.assetid: 2f13e9cf-55b5-458b-8c32-3f8cd98c9ecf
ms.search.industry: Retail
ms.search.form: RetailTerminalTable, SystemParameters
ms.openlocfilehash: 32d5c959c044a628a6ed1044b6e30f3363680293
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267463"
---
# <a name="task-recorder-and-help-for-retail-modern-pos-mpos-and-cloud-pos"></a>Retail Modern POS (MPOS) un Cloud POS uzdevumu ierakstītājs un palīdzība

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā izmantot uzdevumu ierakstītāju mākonī Retail Modern POS POS un tajā.

## <a name="overview"></a>Pārskats

Programmās Retail Modern POS vai Cloud POS ietvertais uzdevuma reģistrētājs ir jauns risinājums, kas ir izstrādāts tā, lai nodrošinātu augstu reaģētspēju. Tas nodrošina pielāgojamu lietojumprogrammu programmēšanas saskarni (API), kura nodrošina paplašināšanas iespējas un vienkāršu integrāciju ar biznesa procesu ierakstus izmantojošajām sistēmām. Turklāt ir progresējusi Uzdevumu ierakstītāja integrācija portāla Microsoft Dynamics Lifecycle Services rīkā Biznesa procesu modelētājs (BPM) ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)). Tāpēc lietotāji joprojām var no ierakstiem veidot ar datiem piesātinātas biznesa procesu diagrammas, lai analizētu un izstrādātu lietojumprogrammas.

## <a name="architecture"></a>Arhitektūra

Uzdevuma reģistrētājs var nodrošināt klientā veikto lietotāja darbību precīzu reģistrāciju. Katra vadīkla ir konfigurēta tām, lai uz uzdevuma reģistrētāju tiktu sūtīta informācija par lietotāja darbību izpildi. No vadīklas uz uzdevuma reģistrētāju tiek reāllaikā nosūtīta informācija par notikuma norisi, kā arī visa vajadzīgā informācija par attiecīgo lietotāja darbību. No šīs informācijas uzdevuma reģistrētajā tiek izgūts lietotāja darbības veids (piemēram, pogas klikšķis, vērtības ievade vai navigācija) un visi ar lietotāja darbību saistītie dati (piemēram, ievadīto datu vērtība un veids, veidlapas konteksts vai ieraksta konteksts). Uzdevuma reģistrētājā informācija tiek reģistrēta pietiekami detalizēti, lai nodrošinātu, ka ieraksta demonstrēšanas laikā reģistrētās darbības var veikt tieši tā, kā to darīja lietotājs. (Demonstrēšanas līdzeklis vēl nav ieviests programmās Retail Modern POS un Cloud POS.)

## <a name="basic-configuration"></a>Pamata konfigurācija

Lai POS iespējotu uzdevuma reģistrēšanu, veiciet tālāk norādītas darbības.

1. Noklikšķiniet uz **Retail un Commerce** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **Reģistri**.
2. Noklikšķiniet uz kases sistēmas, kurā vēlaties iespējot uzdevuma reģistrēšanu.
3. Cilnes **Reģistrs** kopsavilkuma cilnē **Vispārīgi** iestatiet opcijas **Iespējot uzdevumu ierakstīšanu** vērtību **Jā**.
4. Noklikšķiniet uz **Saglabāt**.
5. Pārejiet uz **Retail un Commerce** &gt; **Retail un Commerce IT** &gt; **Sadales grafiks**.
6. Atlasiet uzdevumu **Reģistri (1090)** un pēc tam noklikšķiniet uz **Izpildīt tūlīt**.

## <a name="create-a-recording"></a>Ieraksta izveide

Lai izveidotu jaunu ierakstu, izmantojot uzdevuma reģistrētāju, veiciet tālāk norādītās darbības.

1. Palaidiet programmu Retail Modern POS vai Cloud POS un pierakstieties.
2. Lapas **Iestatījumi** sadaļā **Uzdevuma reģistrētājs** noklikšķiniet uz **Atvērt uzdevuma reģistrētāju**. Tiek parādīta rūts **Uzdevuma reģistrētājs**. Varat noklikšķināt uz pogas **Aizvērt** (**X**) augšējā labajā stūrī, lai aizvērtu rūti **Uzdevuma reģistrētājs** pirms jaunas reģistrēšanas sesijas sākšanas. Lai atkārtoti atvērtu rūti, atkārtojiet 2. darbību.

    [![Rūts Uzdevuma reģistrētājs.](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)

3. Ievadiet ieraksta nosaukumu un aprakstu un pēc tam noklikšķiniet uz **Sākt**. Reģistrēšanas sesija sākas, tiklīdz noklikšķināt uz **Sākt**.

    > [!NOTE]
    > Ja ierakstīšanas laikā noklikšķināt uz pogas **Aizvērt** (**X**) augšējā labajā stūrī, tiek aizvērta rūts **Uzdevuma reģistrētājs**, taču reģistrēšanas sesija netiek beigta. Lai atkāroti atvērtu uzdevuma reģistrētāju, noklikšķiniet uz pogas **Palīdzība** (jautājuma zīmes ikonas) ekrāna augšpusē.
    >
    > [![Jautājuma zīme.](./media/help.jpg)](./media/help.jpg)

4. Pēc noklikšķināšanas uz **Sākt** uzdevuma reģistrētājs tiek pārslēgts reģistrēšanas režīmā. Rūtī **Uzdevuma reģistrētājs** tiek rādīta ar reģistrēšanas procesu saistītā informācija un vadīklas.
5. Veiciet vajadzīgās darbības programmas Retail Modern POS vai Cloud POS lietotāja interfeisā (UI).
6. Lai beigtu reģistrēšanas sesiju, noklikšķiniet uz **Apturēt**.

## <a name="download-options"></a>Lejupielādes opcijas

Kad beidzat reģistrēšanas sesiju, tiek parādītas vairākas ierakstu lejupielādes opcijas.

[![Lejupielādes opcijas.](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)

### <a name="save-to-this-pc"></a>Saglabāt šajā datorā

Varat izmantot ieraksta pakotni, lai demonstrētu uzdevuma ceļvedi, uzturētu ierakstu vai rediģētu ierakstā esošās anotācijas. (Šis līdzeklis vēl nav ieviests programmās Retail Modern POS un Cloud POS.)

### <a name="export-as-word-document"></a>Eksportēt kā Word dokumentu

Varat saglabāt ierakstu Microsoft Word dokumenta formātā. Dokumentā ir ietvertas reģistrētās darbības un iegūtie ekrānuzņēmumi.

### <a name="save-as-developer-recording"></a>Saglabāt kā izstrādātāja ierakstu

Neapstrādātais ieraksta fails ir noderīgs izstrādātājiem, piemēram, testa koda ģenerēšanai. (Šis līdzeklis vēl nav ieviests.)

## <a name="recording-controls"></a>Ierakstīšanas vadīklas

[![Reģistrēšanas vadīklas.](./media/controls.jpg)](./media/controls.jpg)

### <a name="stop"></a>Apturēt

Noklikšķiniet uz **Apturēt**, lai beigtu reģistrēšanas sesiju. Ņemiet vērā, ka pēc sesijas beigšanas to vairs nevar atsākt. Tāpēc pirms reģistrēšanas sesijas beigšanas pārliecinieties, ka reģistrēšana ir pabeigta.

### <a name="pause"></a>Pauze

Noklikšķiniet uz **Pauze**, lai īslaicīgi apturētu (pārtrauktu) reģistrēšanas sesiju un turpinātu darbību. Darbības, ko veicat pēc noklikšķināšanas uz **Pauze**, netiek reģistrētas.

### <a name="continue"></a>Turpināt

Lai atsāktu reģistrēšanas sesiju pēc tās pārtraukšanas noklikšķiniet uz **Turpināt**.

### <a name="capture-screenshots"></a>Veikt ekrānuzņēmumus

Uzdevuma reģistrētājs var nodrošināt Retail Modern POS lietotāja interfeisa ekrānuzņēmumu veikšanu biznesa procesa reģistrēšanas laikā. Lai ieslēgtu ekrānuzņēmumu veikšanas līdzekli, opcijai **Veikt ekrānuzņēmumu** iestatiet vērtību **Jā** un pēc tam uzņemiet ierakstu. Kad ierakstīšana ir pabeigta, noklikšķiniet uz **Apturēt** un lejupielādējiet Word dokumentu. Dokumentā būs ietvertas darbības ar attiecīgajiem ekrānuzņēmumiem.

> [!NOTE]
> Capture ekrānuzņēmuma funkcionalitāte netiek atbalstīta komponentā Store Commerce, Commerce Modern POS un Cloud POS.

### <a name="start-task-and-end-task"></a>Uzdevuma sākšana un beigšana

Varat norādīt grupētu darbību kopas sākumu un beigas, izmantojot pogas **Sākt uzdevumu** un **Beigt** **uzdevumu**. Noklikšķiniet uz **Sākt uzdevumu**, lai pievienotu darbību "Sākt uzdevumu", un pēc tam veiciet darbības, kas ir jāietver grupā. Kad esat pabeidzis grupā ietveramo darbību izpildi, noklikšķiniet uz **Beigt uzdevumu**. Uzdevumi palīdz strukturēt procedūras. Uzdevumus var ligzdot citos uzdevumos. Šādā veidā varat labāk strukturēt ļoti garus un sarežģītu biznesa procesus.

## <a name="adding-annotations"></a>Anotāciju pievienošana

Piezīme ir papildu teksts, ko pievienojat ieraksta darbībai. Piemēram, varat izmantot piezīmes, lai sniegtu lietotājam papildu informāciju vai kontekstu. Anotācijas var pievienot pirms vai pēc darbības. Varat pievienot anotāciju jebkurai darbībai, noklikšķinot uz pogas **Rediģēt** (zīmuļa simbola) pa labi no darbības.

[![Darbības rediģēšanas poga.](./media/annotate.jpg)](./media/annotate.jpg)

### <a name="texts-and-notes"></a>Teksts un piezīmes

Varat izmantot laukus **Teksts** un **Piezīmes**, lai pievienotu tekstu, kas ir jāsaista ar darbību uzdevuma reģistrētājā.

[![Lauki Teksts un Piezīmes.](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)

#### <a name="text"></a>Teksts

Laukā **Teksts** ievadītais teksts tiek rādīts *virs* darbības teksta uzdevuma reģistrētājā. Šī atrašanās vieta ir piemērota tekstam, kas lietotājam ir jāizlasa pirms darbības veikšanas.

#### <a name="notes"></a>Piezīmes

Laukā **Piezīmes** ievadītais teksts tiek rādīts *zem* darbības teksta uzdevuma reģistrētājā. Lai izlasītu piezīmes tekstu, lietotājam ir jāizvērš darbības teksts uznirstošajā logā. Šī atrašanās vieta ir piemērota papildinformācijai vai citai informācijai, kas lietotājam var noderēt lietotājam, taču nav nepieciešama, lai veiktu darbību.

## <a name="help-in-retail-modern-pos-and-cloud-pos"></a>Palīdzība programmās Retail Modern POS un Cloud POS

Lai jūsu pielāgotie uzdevumu ieraksti tiktu rādīti programmu Retail Modern POS un Cloud POS rūtī Palīdzība teksta formātā, jums ir jāsaglabā ieraksti savā BPM bibliotēkā un pēc tam ir jāatjaunina palīdzības sistēmas parametri tā, lai tie norādītu uz jūsu BPM bibliotēku. Plašāku informāciju skatiet rakstā [Savienojuma izveidošana ar palīdzības sistēmu](../fin-ops-core/fin-ops/get-started/help-connect.md). Retail Modern POS un Cloud POS palīdzības sistēma nodrošina reāllaika meklēšanu pakalpojumā LCS. Sistēma nodrošina meklēšanu visās BPM bibliotēkās, kas ir atlasītas Commerce palīdzības sistēmas parametros, un atbilstošo rezultātu parādīšanu. Lai piekļūtu izvēlnei **Palīdzība**, noklikšķiniet uz pogas **Palīdzīga** (jautājuma zīme) ekrāna augšdaļā, meklēšanas lodziņā ievadiet procesa nosaukumu un nospiediet meklēšanas pogu.

[![Poga Palīdzība.](./media/help.jpg)](./media/help.jpg)

Meklēšanas rezultātos noklikšķinot uz Uzdevumu ceļveža, varat aplūkot soļus kā palīdzības rakstu vai eksportēt soļus uz Word dokumentu.

> [!NOTE]
> Palīdzība programmās Retail Modern POS un Cloud POS nevar parādīt uzdevumu ceļvežus, ņemot vērā, kuru veidlapu pašlaik atvērāt vai kuru darbību izpildāt. Meklēšanas lodziņā ierakstiet procesa nosaukumu un pēc tam noklikšķiniet uz **Meklēt**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
