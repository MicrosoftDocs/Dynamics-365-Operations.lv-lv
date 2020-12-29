---
title: Izveidot un atjaunināt laika periodus klientu preču saņemšanai
description: Šajā tēmā ir aprakstīts, kā izveidot, konfigurēt un atjaunināt klientu preču saņemšanas laika periodus programmā Commerce Headquarters.
author: anupamar-ms
manager: AnnBe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-09-20
ms.dyn365.ops.version: Retail 10.0.15 update
ms.openlocfilehash: f86eb47ec64dff230223ed0ecbe792373aca649f
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681546"
---
# <a name="create-and-update-time-slots-for-customer-pickup"></a>Izveidot un atjaunināt laika periodus klientu preču saņemšanai

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā izveidot, konfigurēt un atjaunināt klientu preču saņemšanas laika periodus programmā Commerce Headquarters.

Laika periodu funkcija sniedz mazumtirgotājiem veidu, kā definēt laika periodu krājumiem, kam ir ieslēgts klientu saņemšanas piegādes veids. Laika periodi ļauj mazumtirgotājiem noteikt dienas un laikus, kad pasūtījumi var tikt saņemti veikalā. Mazumtirgotāji var arī definēt pasūtījumu skaitu, ko var saņemt noteiktā periodā. Šādā veidā tirgotāji var ierobežot pasūtījumu skaitu, ko var saņemt noteiktā dienā un noteiktā laikā. Rezultāts ir labākas kvalitātes pieredze saviem klientiem.

> [!NOTE]
> Laika periodu līdzeklis ir pieejams Microsoft Dynamics 365 Commerce versijā 10.0.15 un jaunākās versijās.

Sekojošajā attēlā parādīts laika periodu atlases piemērs e-tirdzniecības norēķināšanās laikā.

![Laika periodu atlases piemērs e-tirdzniecības norēķināšanās laikā](../dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="time-slot-properties"></a>Laika periodu rekvizīti

Laika periods ir noteikts intervāls, kad klients var izvēlēties saņemt pasūtījumu no noteikta veikala vai atrašanās vietas. Laika periodu pārvaldības līdzeklis ir pieejams tikai tad, ja ir konfigurēts klienta saņemšanas piegādes veids risinājumā Dynamics 365 Commerce.

Laika periods tiek definēts, izmantojot šādus rekvizītus:

- **Piegādes veids** - norādiet piegādes saņemšanas veidu, uz kuru attiecas laika periods.
- **Minimālo dienu skaits** un **Maksimālo dienu skaits** - norādiet agrākos un vēlākos datumus, ko var atlasīt preču izsniegšanai attiecībā pret datumu, kad tiek veikts pasūtījums. 

    **Minimālo dienu skaits** rekvizīts nodrošina, ka ir pietiekami daudz laika, lai mazumtirgotājs varētu apstrādāt pasūtījumu, pirms tas ir gatavs saņemšanai. **Maksimālo dienu skaits** rekvizīts nodrošina, ka lietotājs nevar atlasīt datumu, kas ir pārāk tālu nākotnē. Piemēram, ja minimālā vērtība ir iestatīta uz **1** un pasūtījums tiek veikts 20. septembrī, agrākā diena, kad pasūtījums būs pieejams savākšanai, ir nākamā piemērotā diena (21. septembris). Līdzīgi, iestatot maksimālo vērtību, varat definēt maksimālo dienu skaitu, kad var saņemt pasūtījumu. Kad minimālās un maksimālās vērtības ir definētas, vietnes lietotāji var redzēt un atlasīt tikai noteiktu dienu kopu norēķināšanās laikā.

    Minimālo vērtību var iestatīt uz decimālu vērtību, kas ir mazāka par 1. Piemēram, ja paņemšana ir pieejama četras stundas pēc pasūtījuma veikšanas, iestatiet minimālo vērtību uz **0,17** (= 4 ÷ 24, noapaļojot līdz divām decimāldaļām). Tomēr, ja iestatāt minimālo vērtību uz decimālu vērtību, kas ir lielāka par 1, tā vienmēr tiek noapaļota līdz tuvākajam veselajam skaitlim (uz augšu vai uz leju).

    Ja maksimālā vērtība tiek iestatīta decimālskaitļa vērtība, tā vienmēr tiek noapaļota. Piemēram, vērtība **1,2** tiks noapaļota uz **2**.

- **Sākuma datums** un **Beigu datums** - norādiet laika perioda sākuma un beigu datumus. Katram laika perioda ierakstam ir sākuma datums un beigu datums. Tāpēc varat brīvi pievienot dažādus laika periodus visu gadu (piemēram, saņemšanu svētku laikā). Ja laika perioda sākuma un beigu datumi tiek mainīti pēc tam, kad pasūtījums ir ticis veikts, izmaiņas netiek piemērotas šim pasūtījumam. Definējot sākuma un beigu datumus, ir jāņem vērā veikala slēgšanas datumi (piemēram, Ziemassvētku diena) un jānodrošina, ka laika periodi nav definēti šīm dienām.
- **Aktīvās piegādes stundas** - norādiet periodu, kad ir atļauta saņemšana. Piemēram, saņemšanas laiki varētu būt no plkst. 14.00 līdz 17.00 katru dienu. Šis rekvizīts ļauj saņemšanas laikiem būt neatkarīgiem no veikala darba laika. Tāpēc mazumtirgotājs var konfigurēt saņemšanas laikus, kas atbilst tā īpašajām biznesa prasībām. Definējot aktīvās preču saņemšanas stundas, ir jāapsver veikala darba laiks un jānodrošina, ka saņemšanas laiki nav definēti laikos, kad veikals ir slēgts.

    > [!NOTE]
    > Veikala preču saņemšanas darba laiks ir jādefinē attiecīgā veikala darba laikā..

- **Laika periodu intervāls**- norādiet ilgumu, ko var piešķirt katram laika periodam. Piemēram, katra laika perioda ilgums var būt par 15 minūtes, 30 minūtes vai vienu stundu.
- **Laika periodi pa intervāliem** - norādiet klienta vai pasūtījumu skaitu, kurus var apkalpot saņemšanai katrā laika intervālā. Piemēram, ievadiet **1**, **2**, **3** vai jebkuru citu veselu skaitli.
- **Aktīvās dienas** - norādiet nedēļas dienas, kad saņemšanas laika periodi ir aktīvi. Šis rekvizīts ļauj mazumtirgotājam noteikt dienas, kad tas vēlas atbalstīt saņemšanas pasūtījumus.
- **Mazumtirdzniecības kanāli** - norādiet mazumtirdzniecības kanālus. Katru laika periodu var saistīt ar vienu vai vairākiem mazumtirdzniecības veikaliem. Atkarībā no katra veikala darbības laika, var izveidot vienu vai vairākus laika periodu ierakstus un saistīt tos ar kanālu. 

<!-- ![HQ Timeslot overview](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

Katram kanālam var konfigurēt tikai vienu laika perioda veidni. Šie kanāli ietver fiziskus veikalus, zvanu centrus, mobilās ierīces un e-komercijas vietnes.

## <a name="configure-the-time-slot-feature-in-commerce-headquarters"></a>Konfigurējiet laika periodu līdzekli risinājumā Commerce Headquarters

Laika periodi ir jādefinē katram saņemšanas veidam risinājumā Commerce Headquarters, tādējādi pārdošanas punkts (POS) un e-tirdzniecības kanāli var atsaukties uz tiem.

- Ar katru veikalu vai kanālu var saistīt tikai vienu laika perioda veidni.
- Katram izveidotajam laika periodam veidnē ir jābūt unikālam piegādes veidam.
- Pēc laika perioda funkcijas konfigurēšanas laika periodu kalendārs būs pieejams atlasītajiem veikaliem vai veikalu grupām. Atsaucei tas būs redzams arī POS sistēmā.

Lai konfigurētu laika periodu līdzekli risinājumā Commerce Headquarters, veiciet sekojošās darbības.

1. Doties uz **Commerce** \> **Kanāla uzstādīšana** \> **Veikala preču saņemšanas laika periods**.
1. Atlasiet **Jauns**, lai izveidotu jaunu laika periodu veidni. Lai izmantotu esošu veidni, atlasiet veidni kreisajā rūtī.
1. Ievadiet vērtības laukos **Laika perioda ID** un **Apraksts**.
1. Kopsavilkuma cilnē **Pasūtījuma saņemšana - Laika iestatījumi** atlasiet **Pievienot**.
1. Dialoglodziņā **Pasūtījuma saņemšana - laika iestatījumi** definējiet datumu diapazonu, piegādes veidu, aktīvās piegādes stundas, aktīvās dienas, laika perioda intervālu, laika periodus pa intervāliem un citus iestatījumus.

    Ja laika periodi tuvākajā nākotnē būs statiski, atstājiet lauku **Beigu datums** tukšu.

    > [!NOTE]
    > Varat izveidot vairākas veidnes, bet tikai vienu veidni var saistīt ar vienu kanālu vai veikalu.

    ![Pasūtījuma saņemšana - laika iestatījumu dialoglodziņš](../dev-itpro/media/Curbside_timeslot_Settings_Page.PNG)

1. Pēc pabeigšanas atlasiet **Labi**.
1. Ja laika periodi dienā atšķirsies, izveidojiet papildu ierakstus kopsavilkuma cilnē **Pasūtījuma saņemšana - laika iestatījumi**, lai nodrošinātu, ka datumi un laiki nepārklājas.
1. Kopsavilkuma cilnē **Mazumtirdzniecības kanāli** atlasiet **Pievienot**, lai saistītu laika periodu veidni ar veikaliem vai kanāliem, kuros tas tiks izmantots.
1. Dialoglodziņā **Izvēlēties organizācijas mezglus**, izmantojiet bultiņu pogas, lai atlasītu (vai notīrītu izvēli) veikalus, reģionus un organizācijas, ar kurām veidne jāsaista.

    <!-- ![HQ Timeslot overview](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

1. Pēc pabeigšanas atlasiet **Labi**.
1. Lapā **Sadales grafiks** palaidiet darbus **1070** un **1135**, lai sinhronizētu datus ar kanāliem.

## <a name="time-slot-selection-for-pos-orders"></a>Laika periodu atlase POS pasūtījumiem

Kad pasūtījuma vai pasūtījuma rinda ir identificēta izsniegšanai POS sistēmā, kasieris var izvēlēties saņemšanas veikalu vai vietu un datumu un laika periodu. Ja klientam ir paņemšanas pasūtījums citam veikalam, kasieris var izvēlēties datumus, kad paņemšana būs pieejama šajā veikalā. Veikala uzmeklēšanā tiks sniegta atsauce uz datumiem un veikalu laikiem.

Sekojošajā attēlā parādīts laika periodu atlases piemērs POS pasūtījumam.

![Laika periodu atlases piemērs POS pasūtījumam](../dev-itpro/media/Curbside_timeslot_POS.png)

## <a name="time-slot-selection-for-e-commerce-orders"></a>Laika periodu atlase e-tirdzniecības pasūtījumiem

Informāciju par to, kā veikt laika periodu atlasi e-tirdzniecības pasūtījumiem, skatiet [Saņemšanas informācijas modulis](../pickup-info-module.md).

> [!NOTE]
> Lietotāji var skatīt vai rediģēt saņemšanas laika periodus Commerce vietnes izrakstīšanās lapā tikai tad, ja saņemšanas informācijas modulis ir pievienots šai lapai. Ja izrakstīšanās lapā nav ietverts saņemšanas informācijas modulis, pasūtījumi tiks izveidoti, neļaujot lietotājiem norādīt vai skatīt laika perioda informāciju.

Sekojošajā attēlā redzams e-tirdzniecības pasūtījuma piemērs, kurā ir izvēlēts saņemšanas laika periods.

![E-tirdzniecības pasūtījuma piemērs, kurā ir izvēlēts saņemšanas laika periods](../dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a>Papildu resursi

[Saņemšanas informācijas modulis](../pickup-info-module.md)
