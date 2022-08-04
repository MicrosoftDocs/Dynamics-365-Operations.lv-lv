---
title: Konfigurēt Palīdzības pieredzi finanšu un operāciju programmām
description: Šajā rakstā ir sniegta informācija par Palīdzības sistēmas komponentiem dažām Microsoft Dynamics 365 programmām.
author: margoc
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 35f5d73075d118079ccb0616fbd1c5e1a8e00424
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2022
ms.locfileid: "9123630"
---
# <a name="configure-the-help-experience-for-finance-and-operations-apps"></a>Konfigurēt Palīdzības pieredzi finanšu un operāciju programmām

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Šajā rakstā jūs atradīsiet pārskatu par Palīdzības sistēmas komponentiem finanšu un operāciju programmām, piemēram, Microsoft Dynamics 365 Finanses, Dynamics 365 Supply Chain Management Dynamics 365 Commerce un Dynamics 365 Human Resources. Šajā rakstā ir izskaidrots arī, kā izveidot savienojumu ar šiem komponentiem un sniegts procesa kopsavilkums par pielāgotas palīdzības izveidei.

## <a name="help-architecture"></a>Palīdzības arhitektūra

Finanšu un operāciju programmas ietver konceptuālus apskatu un citas tēmas, kas tiek publicētas [Microsoft Dynamics 365. dokumentācijas](/dynamics365/) vietnē. Šim saturam var piekļūt no preces **Palīdzības** rūts. Nākamajā attēlā ir parādītas daļas no palīdzības sistēmas.

[![Palīdzības sistēmas arhitektūra.](./media/help-architecture.png)](./media/help-architecture.png)

Preces palīdzības sistēma izvelk rakstus no docs.microsoft.com un citām saistītām vietnēm. Tas arī velk uzdevumu ceļvežus, kas tiek uzglabāti Biznesa procesu modelētājā (BPM) Microsoft Dynamics Lifecycle Services (LCS).

## <a name="adding-task-guides"></a>Uzdevumu ceļvežu pievienošana

> [!NOTE]
> Cilne **Uzdevumu ceļveži** pašlaik nav pieejami Personāla vadībā vai Commerce. <!--We are currently working to enable this functionality in a future release.--> Tomēr uzdevumu ceļveži Darba sākšanas pieredzē Personāla vadībā ir pieejami pamata funkcionalitātes segšanai. Procesuālā palīdzība ir pieejama arī vietnē [Microsoft Dynamics 365 documentation](/dynamics365/) gan Human Resources, gan Commerce programmām.

Lapā **Sistēmas parametri** sistēmas administratori var konfigurēt piekļuvi attiecīgajām uzdevumu ceļveža bibliotēkām ieviešanai.

> [!NOTE]
> - Lai konfigurētu palīdzību, jums ir jāpierakstās ar kontu tajā pašā nomniekā, kurā ir izvietota programma.
> - Savienojumu ar LCS bibliotēku nav iespējams izveidot no programmas instances, kas darbojas lokālā virtuālajā cietajā diskā (VHD).

[![Veidlapa Sistēmas parametri, kurā ir atvērti palīdzības iestatījumi.](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)

Lai konfigurētu risinājuma uzdevumu ceļvežus, veiciet šīs darbības lapā **Sistēmas parametri**.

> [!IMPORTANT]
> Kad cilni **Palīdzība** atverat pirmo reizi, ir jāizveido savienojums ar Lifecycle Services. Noteikti atlasiet saiti formas vidū, uzgaidiet, līdz tiek izveidots savienojums, aizveriet dialoglodziņu un pēc tam atlasiet **Labi**, lai piekļūtu lapai **Sistēmas parametri**.
>
> [![Izveidot savienojumu ar LCS](./media/connect-to-lcs-crop-1024x365.png "Izveidot savienojumu ar LCS.")](./media/connect-to-lcs-crop.png)

1. Atlasiet Lifecycle Services projektu, ar kuru izveidot savienojumu.
2. Atlasiet BPM bibliotēkas (atlasītajā projektā), no kurām izgūt uzdevumu ierakstus.
3. Iestatiet BPM bibliotēku attēlošanas secību. Displejs nosaka secību, kādā uzdevumu ieraksti no bibliotēkām tiks rādīti rūtī **Palīdzība**.

Kad šīs darbības pabeigtas **, varat atvērt palīdzības** rūti **un atlasīt cilni** Uzdevumu ceļveži. Tagad redzēsiet uzdevumu ceļvežus, kas attiecas uz lapu, kuru pašlaik izmantojat finanšu un operāciju programmās. Ja netiek atrasts neviens uzdevuma ceļvedis, varat ievadīt atslēgvārdus, lai precizētu meklēšanu.

### <a name="showing-translated-task-guides"></a>Tulkotu uzdevumu ceļvežu parādīšana

Tulkotie uzdevumu ceļveži pirmo reizi tika izlaisti 2016. gada maijā izlaistajā APQC vienotajā bibliotēkā un darba sākšanas bibliotēkā. Lai redzētu lokalizēto uzdevumu ceļvežu palīdzību, pārliecinieties, ka jūsu Dynamics 365 risinājums ir savienots ar 2016. gada maija bibliotēku. Lietotāji var mainīt uzdevuma ceļveža rādīšanas valodu, izmantojot valodas iestatījumus sadaļā **Opcijas** &gt; **Preferences**.

> [!NOTE]
> Lai gan daudzi uzdevumu ceļveži ir iztulkoti, klients šobrīd nerāda tulkoto uzdevumu ceļvežu nosaukumus. Turklāt 2016. gada maija bibliotēkā tulkojumi ir pieejami tikai tiem uzdevumu ceļvežiem, kas tika izlaisti 2016. gada februārī. Microsoft izdosim atjauninātu bibliotēku, kas iekļauj papildu tulkojumus.
>
> - Ja kāds uzdevumu ceļvedis ir iztulkots, kad atverat šo uzdevumu ceļvedi, viss uzdevuma ceļveža teksts jums tiek rādīts jūsu izvēlētajā valodā.
> - Ja kāds uzdevumu ceļvedis vēl nav iztulkots, kad to atverat, jūsu izvēlētajā valodā jums tiek rādīta tikai daļa teksta (vadīklu teksts).

## <a name="adding-custom-help"></a>Pielāgotās palīdzības pievienošana

Var izmantot uzdevumu ceļvežus, lai izveidotu palīdzību, vai jūs varat savienot pielāgotās palīdzības vietni rūtī **Palīdzība**.

### <a name="create-custom-help-by-using-task-guides"></a>Pielāgotās palīdzības izveide, izmantojot uzdevumu ceļvežus

Atbalstītajām programmām varat izveidot pielāgotu palīdzību, izveidojot uzdevumu ierakstus, kas atspoguļo jūsu implementāciju, un tad tos saglabājot LCS biznesa procesu bibliotēkā. Personāla vadībai nav iespējams izveidot pielāgotus uzdevumu ceļvežus.

Ja esat partneris un pārveidojat bibliotēku par korporatīvo bibliotēku, un iekļaujat to kādā risinājumā, tā ir pieejama jūsu klientiem. Varat arī izveidot APQC vienotās bibliotēkas kopiju, pēc tam atvērt uzdevumu reģistrēšanu kopijā, rediģēt un saglabāt tos ar savām veiktajām izmaiņām. Papildinformāciju skatiet tēmā [Uzdevuma reģistrētāja resursi](../../dev-itpro/user-interface/task-recorder.md).

### <a name="connect-a-custom-help-site"></a>Savienojuma izveide ar pielāgotu palīdzības vietni

Finanšu un operāciju programmas tiek reti izmantotas viņu izvēles formā. Tā vietā risinājums ir pielāgots un paplašināts, lai atbilstu organizācijas vajadzībām. Varat arī pielāgot un paplašināt palīdzības pieredzi. Piemēram, varat pievienot pielāgotu palīdzību preces **Palīdzības** rūtij.

Korporācija Microsoft ir nodrošinājusi rīku komplektu, lai palīdzētu jums izvietot un savienot pielāgotu palīdzību **Palīdzības** rūtī. Lai iegūtu informāciju par to, kā varat iestatīt pielāgotu palīdzības risinājumu, kas ir saistīts ar **Palīdzības** rūti, skatiet [Pielāgotās palīdzības pārskatu](../../dev-itpro/help/custom-help-overview.md).

Ja vēlaties sadarboties ar Microsoft, strādājot ar rīkiem un procesiem palīdzības pielāgošanai, aizpildiet veidlapu [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).

## <a name="see-also"></a>Skatiet arī

[Palīdzības sistēma](help-overview.md)  
[Pielāgotās palīdzības pārskats](../../dev-itpro/help/custom-help-overview.md)  
[Uzdevuma reģistrētāja resursi](../../dev-itpro/user-interface/task-recorder.md)  
[Dokumentācijas vai apmācības izveide, izmantojot uzdevuma reģistrētāju](../../dev-itpro/user-interface/task-recorder-training-docs.md)  
[Pielāgotās palīdzības GitHub repozitorijs](https://github.com/microsoft/dynamics356f-o-custom-help)  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

