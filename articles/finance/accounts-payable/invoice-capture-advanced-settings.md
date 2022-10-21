---
title: Rēķina tveršanas risinājuma papildu iestatījumi
description: Šajā rakstā ir sniegta informācija par papildu iestatījumiem rēķina tveršanas risinājumā.
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
ms.openlocfilehash: a1e24b700d0f30fd90f2619dd6e6687736a86774
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691002"
---
# <a name="invoice-capture-solution-advanced-settings"></a>Rēķina tveršanas risinājuma papildu iestatījumi

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šajā rakstā ir sniegta informācija par papildu iestatījumiem rēķina tveršanas risinājumā.

## <a name="create-additional-connections-for-channels"></a>Izveidot papildu savienojumus kanāliem

Ir jāizveido savienojumi ar e-pasta ziņojumu vai failu krātuvi, lai iespējotu ienākošo rēķinu pārraudzību no dažādiem kanāliem. Vispirms jāreģistrē savienojumi, lai piešķirtu piekļuvi automatizētām plūsmām, ko izmanto risinājumā.

Rēķinu importam tiek izmantoti šādi savienojuma tipi:

- Office 365 Outlook
- Outlook.com
- OneDrive
- SharePoint

Kanālu rēķinu importēšanai izmantos savienojumus turpmākos konfigurācijas soļos. Pirms lietotāji var izveidot noteikta savienojuma kanālu, **tiem** jāpiešķir drošības loma Administrators un jāizveido savienojumi.

Lai izveidotu savienojumu, sekojiet Microsoft Dataverse šiem soļiem.

1. Dodieties uz **administratora sistēmas \> noklusējuma risinājumu**.
2. Atlasiet **Jauns** un pēc tam atlasiet **Savienojuma atsauce**.
3. Laukā **Parādāmais** nosaukums ievadiet nosaukumu.
4. Atlasiet **Microsoft Dataverse** kā savienotāju.
5. Ja savienojumu iestatāt pirmo reizi, atlasiet Jauns **savienojums**.
6. Dialoglodziņā, kas tiek parādīts, izveidojiet savienojumu Dataverse un pēc tam atlasiet **Izveidot**.
7. Ievadiet Dataverse kontu un paroli.
8. Kad apstiprināšana ir veiksmīga, atveriet savienojuma lapu, atlasiet **Atsvaidzināt**, atlasiet kontu un pēc tam atlasiet **Izveidot**.

Lai izveidotu e-pasta ziņojumu vai failu glabāšanas savienojumu, rīkojieties šādi.

1. **Savienojuma izveides lapas** laukā Savienojuma **tips** atlasiet **Office 365 Outlook**.
2. E-pasta savienojumam kā savienotāju **varat Outlook.com** **Office 365 vai Outlook**. Lai izveidotu failu glabāšanas savienojumu, varat atlasīt vai nu vienu no **OneDrive**, vai **SharePoint**.

Lai pārskatītu esošos savienojumus, pārejiet uz **sadaļu Noklusējuma risinājuma \> objektu \> savienojuma atsauces**. Lietotājam, kas izveido kanālus, papildus noteiktiem e-pasta Dataverse vai failu glabāšanas savienojumiem ir jābūt vismaz vienam savienojumam. Jaunā kanāla veidotājam jābūt savienojuma īpašniekam.
