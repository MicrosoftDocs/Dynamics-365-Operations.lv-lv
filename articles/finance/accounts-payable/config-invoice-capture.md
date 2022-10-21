---
title: Konfigurēt rēķina ieguves risinājumu
description: Šajā rakstā ir izskaidrots, kā konfigurēt rēķina tveršanas risinājumu.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: e297dafc930368f14f2e68213ce4153ba792ef4d
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690985"
---
# <a name="configure-the-invoice-capture-solution"></a>Konfigurēt rēķina ieguves risinājumu

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Kad rēķina ieguves risinājums ir instalēts, ir jākonfigurē vide. Šis process sastāv no šādiem pamata soļiem.

1. **Nepieciešams:** sinhronizēt juridiskās personas no Microsoft Dynamics 365 Finansēm. Šis solis tiek izmantots, lai iestatītu organizācijas struktūru Microsoft Power Platform.
2. **Nepieciešams:** konfigurējiet kanālus rēķinu attēlu importam. Risinājums atbalsta šādus kanālus:

    - Office 365 Outlook (noklusējums)
    - Outlook.com
    - OneDrive
    - SharePoint

3. **Nav obligāti:** definējiet papildu konfigurācijas grupas optiskajam rakstzīmju atpazīšanas (OCR) pakalpojumam.
4. **Nav obligāti:** definēt kartēšanas kārtulas juridiskajai personai, kreditora kontam, krājumam un sagādes tipam.

Šis raksts ir fokusēts uz diviem nepieciešamajiem procesa soļiem. Papildinformāciju par konfigurācijas grupām skatiet sadaļā Rēķinu [ieguves risinājumu konfigurācijas grupas](invoice-capture-config-group.md). Papildinformāciju par kartēšanas kārtulām skatiet sadaļā Rēķina [tveršanas risinājuma kartēšanas kārtulas](invoice-capture-mapping-rules.md).

## <a name="manage-legal-entities"></a>Pārvaldīt juridiskās personas

Finanses definē juridiskas personas kā organizācijas, kas tiek identificētas, reģistrējoties juridiskajām iestādēm. Biznesa aktivitātes tiek veiktas un reģistrētas atsevišķās juridiskajās personām. Uzņēmuma Microsoft Power Platform vienībās, drošības lomās un lietotāji ir saistīti kopā veidā, kas atbilst uz lomu balstītajam drošības modelim.

Biznesa vienības tiek lietotas kopā ar drošības lomām, lai kontrolētu piekļuvi datiem. Lietotāji redz tikai informāciju, ko tie pieprasa veikt darbus. Rēķina tveršanas risinājums nodrošina konfigurācijas vietu, kur varat ielādēt pamatinformāciju no esošajām finanšu juridiskajām personām un pārvaldīt tās entītijas, kas ir izveidotas manuāli. Juridiskās personas tiek izmantotas kreditoru rēķinos un drošības kontrolē.

Kad juridiska persona ir izveidota un parādīta sarakstu skatījumā, automātiski tiek izveidota noklusējuma biznesa vienība ar tādu pašu nosaukumu. Grupai tiek piešķirta **AP darbinieks drošības** loma. Kad juridiskās personas tiek importētas, tiek importēti pamata pamatdati no Finansēm. Neesošos krājumus identificēs juridiskā persona un pievienos tos rēķina ieguves risinājumam. Noklusējuma konfigurācijas grupa tiek piešķirta jaunām juridiskajām personām.

### <a name="sync-legal-entities"></a>Sinhronizēt juridiskās personas

Juridiskās personas nevar izveidot tieši. Tomēr juridiskās personas var sinhronizēt no Finansēm. Lai sinhronizētu juridiskās personas, sekojiet šiem soļiem.

1. Dodieties uz **iestatīšanas \> sistēmas \> iestatīšanu, lai pārvaldītu juridiskās personas**.
2. Atlasiet **Sinhronizēt juridiskās** personas un pēc tam **apstiprinājuma** dialoglodziņā atlasiet Labi.

Pēc sinhronizācijas pabeigšanas tiek parādīts jaunu juridisko personu skaits. Jaunās juridiskās personas ir parādītas saraksta skatā. Noklusējuma konfigurācijas grupa tiek piešķirta jaunajām juridiskajām personām.

## <a name="configure-invoice-import-channels"></a>Konfigurēt rēķinu importēšanas kanālus

Kreditori, izmantojot dažādus formātus (papīra vai attēlu), sūta rēķinus no dažādiem kanāliem (e-pasta adrese, faila darbvieta vai rēķinu portāls). Rēķina ieguves risinājums var apstrādāt dažādus kanālus un formātus. Ir atbalstīti šādi tipi:

- Office 365 Outlook
- Outlook.com
- SharePoint
- OneDrive

Kad kanāls ir izveidots noteiktam kontam, automatizēta plūsma, kam ir iepriekš noteikta veidne, tiek izveidota, lai pārraudzītu ienākošos e-pasta ziņojumus vai failus iesūtnē vai atstarpē. Jebkuru failu, kam ir derīgs rēķins, var atpazīt un nosūtīt uz rēķina apgabalu, lai gaidītu kreditoru (AP) klienta apstrādi. Pielikumam jābūt PDF vai attēla formātā. Atbilstoši kanāla konfigurācijai rēķinus var ielādēt rēķina tveršanas risinājumā.

### <a name="create-a-channel"></a>Kanāla izveide

Ja esat importējis papildu risinājumu pakotni (Dynamics 365 rēķina tveršanu — instalēšanas rīkus), Office 365 noklusējuma savienojums programmai Outlook ir gatavs lietošanai. Ja vēlaties izveidot vairāk savienojumu dažādiem e-pasta kontiem vai citiem kanālu tipiem, skatiet sadaļu [Papildu savienojumu izveide kanāliem](invoice-capture-advanced-settings.md#create-additional-connections-for-channels).

Lai izveidotu kanālu, veiciet šādas darbības.

1. Dodieties uz **Iestatīšanas \> sistēmas iestatīšanas \> konfigurācijas kanāliem**.
2. Atlasiet **Jauna**.
3. Iestatiet tālāk norādītos laukus.

    - Kanāla nosaukums
    - Apraksts
    - Veids
    - Savienojums

Risinājumā var importēt tikai tos e-pasta ziņojumus vai failus, kas atbilst tālāk norādītajiem kritērijiem.

| Veids               | Konfigurācija  | Papildinformācija |
|--------------------|----------------|------------------|
| Office 365 Outlook | Mape         | E-pasta mapei ir jāatrodas saknes direktorijā. Pēc noklusējuma tiek izmantota iesūtnes mape. Apakšmape netiek atbalstīta. |
|                    | Tēmu filtrs | (Izvēles iespēja) Apakšvirsra rindiņa, kas jāietver šajā temata. |
|                    | No           | (Izvēles iespēja) Sūtītāja vai sūtītāja e-pasta adrese. Ja norādāt vairākas adreses, lietojiet semikolu (;) kā atdalītāju. |
| SharePoint         | Atrašanās vietas adrese   | Vietnes adreses URL. |
|                    | Mape         | Mape atrašanās vietas adresē. |

### <a name="activate-the-channel"></a>Aktivizēt kanālu

Kad plūsma ir saglabāta, lauki rāda kanāla statusu un laiku, kad tā tika izveidota. Sākotnēji, lauka **statuss** iestatījums ir **Neaktīvs**. Statusa **iemesla lauks** norāda, ka kanāls ir inicializēts un ir gatavs aktivizēšanai.

Lai aktivizētu kanālu, atlasiet **Aktivizēt**. Statusa **un** statusa **iemesla lauki** ir atjaunināti.

Ja kanāls nav nepieciešams, to var deaktivizēt. Lai deaktivizētu kanālu, atlasiet **Deaktivizēt**. Statusa **un** statusa **iemesla lauki** ir atjaunināti.

### <a name="manage-flows-in-flow-management"></a>Pārvaldīt plūsmas plūsmas pārvaldību

Kanālu var skatīt kanālu konfigurēšanas **lapā** vai plūsmas pārvaldībā.

Lai skatītu papildinformāciju, atveriet administrēšanas **sistēmas \> noklusējuma risinājumu mākoņa \>** plūsmas un atlasiet mērķa plūsmu. Redzamas detaļas ietver saistītos savienojumus, īpašniekus un palaist histories.

Lai sinhronizētu statusu, **atlasiet Pārbaudīt**, lai apstiprinātu, ka kanāla statuss atbilst plūsmas statusam.

Daži izņēmuma apstrādes gadījumi ir parādīti laukā **Statusa iemesls**:

- **Trūkst Dataverse savienojuma** — pašreizējais lietotājs nav izveidojis vismaz vienu **Microsoft Dataverse** savienojuma atsauci.
- **Nav atrasta** — plūsma, kas ir saistīta ar kanālu, ir dzēsta plūsmas pārvaldībā. Lai izveidotu jaunu kanālu, kanāls ir jāsaglabā vēlreiz.
- **Deaktivizēts plūsmas pārvaldībā** – plūsma plūsmas pārvaldībā ir dezaktivēta, un kanāla statuss atšķiras no plūsmas statusa.
- **Aktivizēta plūsmas pārvaldībā** – plūsma ir aktivizēta plūsmas pārvaldībā, un kanāla statuss atšķiras no plūsmas statusa.
- **Radusies negaidīta** kļūda — lietotājam jāapstiprina, ka vietne ir "Sakaru vietne", un ka mape ir "Dokumentu bibliotēka".
