---
title: Rēķina ieguves risinājumu konfigurācijas grupas
description: Šajā rakstā ir sniegta vispārīga informācija par konfigurācijas grupām rēķina ieguves risinājumā.
author: sunfzam
ms.date: 09/28/2022
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
ms.openlocfilehash: cfe5ae35b4f87a350d944b30a49251081766ad27
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691006"
---
# <a name="invoice-capture-solution-configuration-groups"></a>Rēķina ieguves risinājumu konfigurācijas grupas

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Lietotāji var pārvaldīt rēķina lauku sarakstu un manuālo pārskata iestatījumu juridiskām personām, izmantojot konfigurācijas grupas. Lietotāji var iestatīt rēķinu konfigurācijas dažādām juridiskajām personām grupās. Visas juridiskās personas vienā konfigurācijas grupā izmanto vienus un tos pašus rēķina laukus un manuālās pārskatīšanas iestatījumus.

## <a name="manage-configuration-groups"></a>Pārvaldīt konfigurācijas grupas

Lai pārvaldītu konfigurācijas grupas, izmantojot programmu, atveriet sadaļu **Iestatījumi un** pēc tam atlasiet Sistēmas iestatīšanas **konfigurācijas \> grupu komponents**.

**Lapā Konfigurācijas grupu definēšana** galvenā cilne rāda definēto konfigurācijas grupu sarakstu. Rāda arī noklusēto konfigurācijas grupu. Katrai konfigurācijas grupai ir pieejamas šādas darbības:

- **Konfigurācijas grupas kopēšana** – Jaunu konfigurācijas grupu var izveidot, izveidojot jau pastāvošu grupu. Jaunajai grupai ir tādas pašas vērtības kā sākotnējai grupai visiem laukiem, izņemot Grupas **nosaukumu** un **Grupas aprakstu**. Kad konfigurācijas grupa ir dublēta, atlasiet **Labi**.
- **Konfigurācijas grupu dzēšana** - lai dzēstu konfigurācijas grupu, atlasiet to un pēc tam atlasiet **Dzēst**.

    > [!NOTE]
    > Nevar dzēst noklusējuma konfigurācijas grupu.

- **Rediģēt konfigurācijas grupas ID** — lai rediģētu konfigurācijas grupas ID, atlasiet grupas **ID** lauku un atjauniniet vērtību. Grupas ID nedrīkst saturēt atstarpes vai īpašas rakstzīmes, un tas nedrīkst pārsniegt 20 rakstzīmes.

    > [!NOTE]
    > Grupas ID lauka **vērtību** var atjaunināt tikai vienu reizi.

- **Rediģēt konfigurācijas grupas aprakstu – lai** rediģētu konfigurācijas grupas aprakstu, atlasiet **lauku Apraksts** un atjauniniet vērtību.
- **Mainīt manuālo pārskata iestatījumu** - Lietotāji var izlemt, vai rēķins ir jāpārskata manuāli. Lai mainītu manuālās pārskatīšanas iestatījumu, atlasiet opciju **Nepieciešama manuāla pārskatīšana**. Pieejamas šādas opcijas:

    - **Vienmēr veikt manuālu** pārskatīšanu - atlasiet šo opciju, ja rēķiniem konfigurācijas grupā vienmēr nepieciešams veikt manuālu pārskatīšanu.
    - **Kļūdu un brīdinājumu gadījumā atlasiet** šo opciju, ja rēķiniem, kuros ir kļūdu ziņojumi vai brīdinājuma ziņojumi, ir jāveic manuāla pārskatīšana.
    - **Kļūdas -** atlasiet šo opciju, ja rēķiniem, kas satur kļūdu ziņojumus, nepieciešams veikt manuālu pārskatīšanu.

- **Mainīt uzticamības punktu skaitu iestatījumu** – uzticamības rezultāts ir metadati, ko rēķina ieguves risinājums nodrošina, lai ziņotu par atpazīto rēķina datu precizitāti. Jo lielāks rezultāts ir, jo precīzāki varētu būt atpazītie dati. Konfigurācija ļauj lietotājiem definēt, kad nepieciešama manuāla pārskatīšana, pamatojoties uzticamības rezultātu. Lietotāji var mainīt pārliecību rezultātu slieksni rēķiniem. Lai atjauninātu pārliecību punktu skaitu, atlasiet lauku **Drošības rezultāts** un atjauniniet vērtību.

    Ir divi brīdinājumu tipi, kas ir brīdinājumu rādītājus:

    - **Brīdinājums** – rēķina lauki, kuriem ir uzticamības rādītāji virs brīdinājuma sliekšņa, tiek uzskatīti par pareiziem. Brīdinājuma slieksnim jābūt lielākam par kļūdas slieksni un mazākam par 100.
    - **Kļūda** – rēķina lauki, kuriem ir uzticamības rādītāji zem kļūdu sliekšņa, tiek uzskatīti par neizdevušiem. Kļūdas ziņojumi tiks rādīti lietotājam. Kļūdas slieksnim jābūt lielākam par 0 (nulli) un mazākam par brīdinājuma slieksni. Brīdinājuma ziņojumi tiks rādīti rēķina laukiem, kuriem ir uzticamības rezultāts starp brīdinājuma slieksni un kļūdu slieksni.

- **Pārvaldīt rēķinu laukus** — lietotāji var pārvaldīt līdzāsparādīšanas skatītājā rādīto rēķina lauku sarakstu. Cilnē Rēķinu **lauku pārvaldība atlasiet** ātrumkārbas simbolu, atlasiet pievienojamos rēķina laukus un pēc tam atlasiet **Saglabāt**. Atlasītie lauki tiks pievienoti sarakstam. Lai izņemtu rēķina lauku no saraksta, atlasiet **Noņemt** šo lauku.

### <a name="manage-file-filters-optional"></a>Pārvaldīt failu filtrus (neobligāti)

Pārvaldīt failu filtrus, lai lietotāji varētu definēt papildu filtrus ienākošajiem rēķinu failiem. Faili, kas neatbilst filtra kritērijiem, tiks **saņemti un tiks parādīti sarakstā Saņemtie faili**, taču tajos tiks rādītas faila validācijas kļūdas. Šī uzvedība atšķiras no kanālā definēto filtru funkcionalitātes. Šiem filtriem faili, kas neatbilst kritērijiem, netiks saņemti vispār. Lietotāji var pārskatīt ienākošos failus un izlemt, vai katrs fails nav derīgs rēķins, un tie var novecojuši failu vai manuāli iekļaut to atpazīšanai un iekļaušanai saglabātos rēķinos.

Kad rēķina ieguves risinājums ir instalēts, tiek definēts noklusējuma faila filtrs. Šis faila filtrs ir globāls. Ja vēlaties citus filtra iestatījumus, jūs varat atjaunināt noklusējuma filtru. Ja lauks ir obligāts, atlasiet **Obligāts**. 

### <a name="accepted-file-size"></a>Pieņemtais faila lielums

Var izvēlēties akceptēto faila lielumu.

> [!NOTE]
> Faili, kas pārsniedz 20 480 kilobaitus (KB), netiek atbalstīti.

### <a name="supported-file-types"></a>Atbalstītie failu tipi

Šobrīd tiek atbalstīti šādi failu tipi:

- PDF
- PNG
- JPG
- JPEG
- Tif
- TIFF
