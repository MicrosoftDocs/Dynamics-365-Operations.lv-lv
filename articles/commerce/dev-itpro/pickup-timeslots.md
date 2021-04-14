---
title: Klienta preču saņemšanas laika nišu izveidošana un atjaunināšana
description: Šajā tēmā ir aprakstīts, kā izveidot, konfigurēt un atjaunināt klientu preču saņemšanas laika nišas programmā Commerce Headquarters.
author: anupamar-ms
ms.date: 01/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-09-20
ms.dyn365.ops.version: Retail 10.0.15 update
ms.openlocfilehash: c3da7474f9a61e97ee11688a18cb91a5ad1ccb5c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791169"
---
# <a name="create-and-update-time-slots-for-customer-pickup"></a>Klienta preču saņemšanas laika nišu izveidošana un atjaunināšana

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā izveidot, konfigurēt un atjaunināt klientu preču saņemšanas laika nišas programmā Commerce Headquarters.

Laika nišas funkcija sniedz mazumtirgotājiem veidu, kā definēt laika nišu krājumiem, kam ir ieslēgts klientu saņemšanas piegādes veids. Laika nišas ļauj mazumtirgotājiem noteikt dienas un laikus, kad pasūtījumi var tikt saņemti veikalā. Mazumtirgotāji var arī definēt pasūtījumu skaitu, ko var saņemt noteiktā periodā. Šādā veidā tirgotāji var ierobežot pasūtījumu skaitu, ko var saņemt noteiktā dienā un noteiktā laikā. Rezultāts ir labākas kvalitātes pieredze saviem klientiem.

> [!NOTE]
> Laika nišas līdzeklis ir pieejams Microsoft Dynamics 365 Commerce versijā 10.0.15 un jaunākās versijās.

Sekojošajā attēlā parādīts laika nišas atlases piemērs e-tirdzniecības norēķināšanās laikā.

![Laika nišas atlases piemērs e-tirdzniecības norēķināšanās laikā](../dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="time-slot-properties"></a>Laika nišas rekvizīti

Laika niša ir noteikts intervāls, kad klients var izvēlēties saņemt pasūtījumu no noteikta veikala vai atrašanās vietas. Laika nišu pārvaldības līdzeklis ir pieejams tikai tad, ja ir konfigurēts klienta saņemšanas piegādes veids risinājumā Dynamics 365 Commerce.

Laika niša tiek definēta, izmantojot šādus rekvizītus:

- **Piegādes veids** - norādiet piegādes saņemšanas veidu, uz kuru attiecas laika niša.
- **Minimālo dienu skaits** un **Maksimālo dienu skaits** - norādiet agrākos un vēlākos datumus, ko var atlasīt preču izsniegšanai attiecībā pret datumu, kad tiek veikts pasūtījums. 

    **Minimālo dienu skaits** rekvizīts nodrošina, ka ir pietiekami daudz laika, lai mazumtirgotājs varētu apstrādāt pasūtījumu, pirms tas ir gatavs saņemšanai. **Maksimālo dienu skaits** rekvizīts nodrošina, ka lietotājs nevar atlasīt datumu, kas ir pārāk tālu nākotnē. Piemēram, ja minimālā vērtība ir iestatīta uz **1** un pasūtījums tiek veikts 20. septembrī, agrākā diena, kad pasūtījums būs pieejams savākšanai, ir nākamā piemērotā diena (21. septembris). Līdzīgi, iestatot maksimālo vērtību, varat definēt maksimālo dienu skaitu, kad var saņemt pasūtījumu. Kad minimālās un maksimālās vērtības ir definētas, vietnes lietotāji var redzēt un atlasīt tikai noteiktu dienu kopu norēķināšanās laikā.

    Minimālo vērtību var iestatīt uz decimālu vērtību, kas ir mazāka par 1. Piemēram, ja paņemšana ir pieejama četras stundas pēc pasūtījuma veikšanas, iestatiet minimālo vērtību uz **0,17** (= 4 ÷ 24, noapaļojot līdz divām decimāldaļām). Tomēr, ja iestatāt minimālo vērtību uz decimālu vērtību, kas ir lielāka par 1, tā vienmēr tiek noapaļota uz tuvāko veselo skaitli. Piemēram, vērtība **1,2** tiks noapaļota uz **2**. Līdzīgi, ja iestatāt maksimālo vērtību uz decimālu vērtību, tā vienmēr tiek noapaļota uz tuvāko veselo skaitli. 

- **Sākuma datums** un **Beigu datums** - norādiet laika nišas sākuma un beigu datumus. Katram laika nišas ierakstam ir sākuma datums un beigu datums. Tāpēc varat brīvi pievienot dažādas laika nišas visu gadu (piemēram, saņemšanu svētku laikā). Ja laika nišas sākuma un beigu datumi tiek mainīti pēc tam, kad pasūtījums ir ticis veikts, izmaiņas netiek piemērotas šim pasūtījumam. Definējot sākuma un beigu datumus, ir jāņem vērā veikala slēgšanas datumi (piemēram, Ziemassvētku diena) un jānodrošina, ka laika nišas nav definētas šīm dienām.
- **Aktīvās saņemšanas stundas** - norādiet periodu, kad ir atļauta saņemšana. Piemēram, saņemšanas laiki varētu būt no plkst. 14.00 līdz 17.00 katru dienu. Šis rekvizīts ļauj saņemšanas laikiem būt neatkarīgiem no veikala darba laika. Tāpēc mazumtirgotājs var konfigurēt saņemšanas laikus, kas atbilst tā īpašajām biznesa prasībām. Definējot aktīvās preču saņemšanas stundas, ir jāapsver veikala darba laiks un jānodrošina, ka saņemšanas laiki nav definēti laikos, kad veikals ir slēgts.

    > [!NOTE]
    > Veikala preču saņemšanas darba laiks ir jādefinē attiecīgā veikala darba laikā..

- **Laika nišas intervāls**- norādiet ilgumu, ko var piešķirt katrai laika nišai. Piemēram, katras laika nišas ilgums var būt 15 minūtes, 30 minūtes vai viena stunda. Ja laika nišas vērtība ir 0, laika niša ir pieejama visam laikam starp sākuma un beigu laiku.
- **Laika nišas pa intervāliem** - norādiet klientu vai pasūtījumu skaitu, kurus var apkalpot saņemšanai katrā laika nišā. Piemēram, ievadiet **1**, **2**, **3** vai jebkuru citu veselu skaitli.
- **Aktīvās dienas** - norādiet nedēļas dienas, kad saņemšanas laika nišas ir aktīvas. Šis rekvizīts ļauj mazumtirgotājam noteikt dienas, kad tas vēlas atbalstīt saņemšanas pasūtījumus.
- **Mazumtirdzniecības kanāli** - norādiet mazumtirdzniecības kanālus. Katru laika nišu var saistīt ar vienu vai vairākiem mazumtirdzniecības veikaliem. Atkarībā no katra veikala darbības laika, var izveidot vienu vai vairākus laika nišas ierakstus un saistīt tos ar kanālu. 

<!-- ![HQ Timeslot overview](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

Katram kanālam var konfigurēt tikai vienu laika nišas veidni. Šie kanāli ietver fiziskus veikalus, zvanu centrus, mobilās ierīces un e-komercijas vietnes.

## <a name="configure-the-time-slot-feature-in-commerce-headquarters"></a>Laika nišas līdzekļa konfigurēšana Commerce Headquarters

Laika nišas ir jādefinē katram saņemšanas veidam Commerce Headquarters, tādējādi pārdošanas punkts (POS) un e-tirdzniecības kanāli var atsaukties uz tiem.

- Ar katru veikalu vai kanālu var saistīt tikai vienu laika nišas veidni.
- Katrai izveidotajai laika nišai veidnē ir jābūt unikālam piegādes veidam.
- Pēc laika nišas līdzekļa konfigurēšanas laika nišu kalendārs būs pieejams atlasītajiem veikaliem vai veikalu grupām. Atsaucei tas būs redzams arī POS sistēmā.

Lai konfigurētu laika nišu līdzekli Commerce Headquarters, veiciet tālāk norādītās darbības.

1. Doties uz **Commerce** \> **Kanāla uzstādīšana** \> **Veikala preču saņemšanas laika niša**.
1. Atlasiet **Jauns**, lai izveidotu jaunu laika nišas veidni. Lai izmantotu esošu veidni, atlasiet veidni kreisajā rūtī.
1. Ievadiet vērtības laukos **Laika nišas ID** un **Apraksts**.
1. Kopsavilkuma cilnē **Pasūtījuma saņemšana - Laika iestatījumi** atlasiet **Pievienot**.
1. Dialoglodziņā **Pasūtījuma saņemšana - laika iestatījumi** definējiet datumu diapazonu, piegādes veidu, aktīvās piegādes stundas, aktīvās dienas, laika nišas intervālu, laika nišas pa intervāliem un citus iestatījumus.

    Ja laika nišas tuvākajā nākotnē būs statiskas, iestatiet lauku **Beigu datums** uz **Nekad**.

    > [!NOTE]
    > Varat izveidot vairākas veidnes, bet tikai vienu veidni var saistīt ar vienu kanālu vai veikalu.

    ![Pasūtījuma saņemšana - laika iestatījumu dialoglodziņš](../dev-itpro/media/Curbside_timeslot_Settings_Page.PNG)

1. Pēc pabeigšanas atlasiet **Labi**.
1. Ja laika nišas dienā atšķirsies, izveidojiet papildu ierakstus kopsavilkuma cilnē **Pasūtījuma saņemšana - laika iestatījumi**, lai nodrošinātu, ka datumi un laiki nepārklājas.
1. Kopsavilkuma cilnē **Mazumtirdzniecības kanāli** atlasiet **Pievienot**, lai saistītu laika nišas veidni ar veikaliem vai kanāliem, kuros tas tiks izmantots.
1. Dialoglodziņā **Izvēlēties organizācijas mezglus**, izmantojiet bultiņu pogas, lai atlasītu (vai notīrītu izvēli) veikalus, reģionus un organizācijas, ar kurām veidne jāsaista.

    <!-- ![HQ Timeslot overview](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

1. Pēc pabeigšanas atlasiet **Labi**.
1. Lapā **Sadales grafiks** palaidiet darbus **1070** un **1135**, lai sinhronizētu datus ar kanāliem.

## <a name="time-slot-selection-for-pos-orders"></a>Laika nišas atlase POS pasūtījumiem

Kad pasūtījuma vai pasūtījuma rinda ir identificēta izsniegšanai POS sistēmā, kasieris var izvēlēties saņemšanas veikalu vai vietu un datumu un laika nišu. Ja klientam ir paņemšanas pasūtījums citam veikalam, kasieris var izvēlēties datumus, kad paņemšana būs pieejama šajā veikalā. Veikala uzmeklēšanā tiks sniegta atsauce uz datumiem un veikalu laikiem.

Sekojošajā attēlā parādīts laika nišu atlases piemērs POS pasūtījumam.

![Laika nišu atlases piemērs POS pasūtījumam](../dev-itpro/media/Curbside_timeslot_POS.png)

## <a name="time-slot-selection-for-e-commerce-orders"></a>Laika nišu atlase e-tirdzniecības pasūtījumiem

Informāciju par to, kā veikt laika nišu atlasi e-tirdzniecības pasūtījumiem, skatiet [Saņemšanas informācijas modulis](../pickup-info-module.md).

> [!NOTE]
> Lietotāji var skatīt vai rediģēt saņemšanas laika nišas Commerce vietnes izrakstīšanās lapā tikai tad, ja saņemšanas informācijas modulis ir pievienots šai lapai. Ja izrakstīšanās lapā nav ietverts saņemšanas informācijas modulis, pasūtījumi tiks izveidoti, neļaujot lietotājiem norādīt vai skatīt laika nišas informāciju.

Sekojošajā attēlā redzams e-tirdzniecības pasūtījuma piemērs, kurā ir izvēlēta saņemšanas laika niša.

![E-tirdzniecības pasūtījuma piemērs, kurā ir izvēlēta saņemšanas laika niša](../dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="time-slot-selection-for-call-center-orders"></a>Laika nišu atlase zvanu centra pasūtījumiem

Zvanu centra programmā zvanu centra aģenti var atlasīt saņemšanas veikalu vai atrašanās vietu, kā arī datuma un laika nišu, kā parādīts šajā ilustrācijā.

![Zvanu centra pasūtījuma piemērs, kurā ir izvēlēta saņemšanas laika niša](../dev-itpro/media/Curbside_timeslot_callcenter.png)

## <a name="additional-resources"></a>Papildu resursi

[Saņemšanas informācijas modulis](../pickup-info-module.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]