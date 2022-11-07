---
title: Pasūtījumu operācijas atsaukšana punktā POS
description: Šajā rakstā ir paskaidrotas līdzekļu iespējas, kas ir pieejamas uzlabotām pasūtījumu atsaukšanas lapām POS.
author: hhainesms
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 0624c251646110644a8a72658a6dd6f8d319c57f
ms.sourcegitcommit: e25fe4228add88dd37f4f38ece86979e1c621f6a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/01/2022
ms.locfileid: "9734299"
---
# <a name="recall-order-operation-in-pos"></a>Pasūtījuma operāciju atsaukšana punktā POS

[!include [banner](includes/banner.md)]

Darbība **Pasūtījuma atsaukšana** Commerce pārdošanas punktā (POS) nodrošina atjauninātus pasūtījuma meklēšanas un filtrēšanas līdzekļus un ar pasūtījumu saistītu informāciju. Šis līdzeklis ir pieejams Commerce versijās 10.0.15 un jaunākās.

Lai iespējotu šo funkcionalitāti ieslēdziet līdzekli **Uzlabota pasūtījuma operāciju atsaukšana punktā POS**, kas atrodas **Līdzekļu pārvaldība** darbvietā, programmā Commerce Headquarters. Pēc līdzekļa iespējošanas, apsveriet iespēju atjaunināt [ekrāna izkārtojumus](pos-screen-layouts.md) punktā POS, lai izmantotu dažas no mainītajām iespējām.

Operāciju pogas **Atsaukt pasūtījumu** konfigurēšana ļauj organizācijām izvietot operāciju ar iepriekš definētu displeju.

![Pogu rindas konfigurēšana.](media/recallorderbuttongrid.png)

Displeja opcijas ir aprakstītas šeit.
- **Nav** – šī opcija izvieto operāciju bez noteikta displeja. Kad lietotājs atver operāciju ar šo konfigurāciju, viņam tiks piedāvāts meklēt un atrast pasūtījumus vai izvēlēties no iepriekš definēta pasūtījumu filtra.
- **Izpildāmie pasūtījumi** – lietotājam uzsākot operāciju, vaicājums tiks izpildīts automātiski, lai meklētu un parādītu lietotāja pašreizējā veikalā izpildāmo pasūtījumu sarakstu. Šie pasūtījumi ir konfigurēti saņemšanai veikalā vai veikala sūtījumiem, un šo pasūtījumu rindas vēl nav izdotas vai iepakotas.
- **Izdodamie pasūtījumi** – lietotājam uzsākot operāciju, vaicājums tiks izpildīts automātiski, lai meklētu un parādītu sarakstu ar pasūtījumiem, kuri ir konfigurēti saņemšanai lietotāja pašreizējā veikalā.
- **Nosūtāmie pasūtījumi** – lietotājam uzsākot operāciju, vaicājums tiks izpildīts automātiski, lai meklētu un parādītu sarakstu ar pasūtījumiem, kuri ir konfigurēti nosūtīšanai no lietotāja pašreizējā veikala.

Uzsākot **Atsaukt pasūtījumu** operāciju no punkta POS, ja displejs ir konfigurēts uz **Nav**, lietotājs varēs meklēt un izgūt pasūtījumus vienā no tālāk norādītajiem veidiem.
- Skenēt pasūtījumu svītrkodus. Šādā veidā tiks meklētas atbilstības pasūtījuma numura, kanāla atsauces un saņemšanas ID laukos.
- Lai izmantotu filtrēšanas mehānismu un atrastu pasūtījumus, kas atbilst filtrēšanas kritērijiem, atlasiet **Meklēt pasūtījumus** vai **Meklēt un filtrēt** ikonu, kas atrodas AppBar.
- Nolaižamajā izvēlnē **Rādīt pasūtījumus** izvēlieties kādu no iepriekš definētajiem filtriem (izpildāmie pasūtījumi, izdodamie pasūtījumi vai nosūtāmie pasūtījumi).

![RecallOrderMainMenu.](media/recallordermain.png)

Pēc meklēšanas kritēriju piemērošanas programmā tiks parādīts atbilstošo pārdošanas pasūtījumu saraksts. Ir svarīgi ņemt vērā, ka, izmantojot meklēšanas/filtra opcijas, izgūtajiem pasūtījumiem nav jābūt pasūtījumiem, kas saistīti ar lietotāja pašreizējo veikalu. Šis meklēšanas process izgūs un parādīs jebkuru debitora pasūtījumu, kas atbilst meklēšanas kritērijiem, pat ja pasūtījums tika izveidots vai iestatīts izpildei citā veikala/kanāla vai noliktavas vietā.

![RecallOrderDetail.](media/orderrecalldetail.png)

Lietotājs sarakstā var atlasīt pasūtījumu, lai skatītu papildu informāciju. Informācijas panelī ekrāna labajā pusē tiek parādīta atlasītā pasūtījuma specifika, ieskaitot pasūtījuma rindas informāciju, piegādes informāciju un izpildes informāciju.

Lietotājs var atlasīt operāciju no AppBar. Atkarībā no pasūtījuma statusa, atsevišķas operācijas var nebūt iespējotas.

- **Atgriešana** — uzsāk atgriešanas procesu jebkuram no atlasītā debitora pasūtījumā iekļautajiem produktiem, par kuru ir izrakstīts rēķins.

- **Atcelt** – izpilda atlasītā pārdošanas pasūtījuma pilnīgu atcelšanu. Šī opcija nav pieejama pasūtījumiem, kas ir sākti, izmantojot zvanu centra kanālu, un to nevar izmantot, lai daļēji atceltu pasūtījumu.

- **Izpildīt** – pārsūta lietotāju uz pasūtījuma izpildes lapu, kas tiks iepriekš filtrēta atlasītajam pasūtījumam. Tiks parādītas tikai tās pasūtījuma rindas, kas ir atvērtas, lai lietotāja veikals varētu izpildīt atlasīto pasūtījumu.

- **Rediģēt** – ļauj lietotājiem veikt izmaiņas atlasītajā debitora pasūtījumā. Pasūtījumus var rediģēt tikai [noteiktos scenārijos](customer-orders-overview.md#edit-an-existing-customer-order).

- **Savākšana** — šī opcija ir pieejama, ja pasūtījumam ir viena vai vairākas rindas, kas ir iestatītas savākšanai lietotāja pašreizējā veikalā. Šī darbība palaiž izdošanas plūsmu, kas ļauj lietotājam izvēlēties saņemamās preces un izveido izdošanas pārdošanas transakciju.

## <a name="add-notifications-to-the-recall-order-operation"></a>Pievienot paziņojumus pasūtījuma atsaukšanas operācijai

Versijā 10.0.18 un jaunākā versijā varat konfigurēt POS paziņojumus un tiešsaistes elementu brīdinājumus par operāciju **Pasūtījuma atsaukšana**, ja tas ir vēlams. Papildinformāciju skatiet sadaļā [Pasūtījumu paziņojumu rādīšana pārdošanas punktā (POS)](notifications-pos.md).  

> [!NOTE]
> Lai iespējotu pasūtījuma uzmeklēšanas līdzekli, nodrošiniet, lai **licences konfigurācijas atslēgās** atslēga Piedāvājums **būtu** > **iespējota**.
>
> ![Jāaktivizē piedāvājumu licences atslēgas konfigurācija.](./media/Quotations_License_Key_Configuration.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
