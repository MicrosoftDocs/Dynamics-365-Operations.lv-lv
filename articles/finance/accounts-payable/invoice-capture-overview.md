---
title: Rēķina tveršanas risinājuma apskats
description: Šajā rakstā ir sniegta informācija par rēķina ieguves risinājumu.
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
ms.openlocfilehash: 76441220b93744527f412110db536601a2fa1dd9
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691003"
---
# <a name="invoice-capture-solution"></a>Rēķina tveršanas risinājums

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šajā rakstā ir sniegta informācija par rēķina tveršanas risinājumu, kas automātiski izveido kreditora rēķinus no digitālu rēķinu attēliem.

Nodaļa Parādi kreditoriem (Ap) pārvalda un apstrādā rēķinus par saņemtajām precēm un pakalpojumiem. Kreditora grāmatvedis pārbauda datus kreditora rēķinos šādu iemeslu dēļ:

- Lai izvairītos no papildu darba, ja perioda slēgšanas laikā nepieciešamas korekcijas vai labojumi
- Lai laikus apmaksātu kreditoru rēķinus un nepieļautu finanšu zaudējumus kļūdas vai pārkāpumu dēļ

Optiskā rakstzīmju atpazīšana (OCR) ir kļuvusi plaši izmantota dažādās nozarēm iepriekšējos gados. Tagad tas ir izplatīts drukātiem tekstiem, kas jāparakstās pa ciparu veidā, lai tos varētu elektroniski rediģēt, meklēt, glabāt vairāk saglabājot un rādīt tiešsaistē. Digitālais teksts var tikt izmantots mašīnu procesos, piemēram, vienojošai skaitļošanai, mašīnu transformācijasm, teksta pārveidošanai, atslēgas datiem un datu iegūšanai.

Jūsu pētīšanas sistēmas (AI) tehnoloģija ir aktivizējusi modernos OCR risinājumus, lai nolasītu dažādus rēķinu formātus no dažādiem kreditoriem, neprasot lielu cilvēkresursu iejaukšanos. Vairāki uzņēmumi ir atpazīstami, ka tie var saglabāt darbu un uzlabot precizitāti, apstrādājot rēķinus ar automatizācijas palīdzību, nevis veikt manuālu apstrādi.

## <a name="system-landscape"></a>Sistēmas ainavorientācija

Šajā attēlā redzami rēķina ieguves risinājuma galvenie komponenti un darbības.

[![Rēķina ieguves risinājumā komponenti un darbības.](./media/Invoice-capture2.png)](./media/Invoice-capture2.png)

## <a name="required-roles"></a>Nepieciešamās lomas

Tabulā ir parādītas lomas, kas ir nepieciešamas rēķina ieguves risinājuma iestatīšanai un lietošanai.

| Loma          | Darbības | Sistēmas | Lomu nosaukumi |
|---------------|---------|---------|-----------|
| Administrators | <ul><li>Iestatiet vides programmā Microsoft Power Platform.</li><li>Izvietojiet risinājumus Microsoft Power Platform.</li><li>Iestatīt savienojumus starp Dynamics 365 un AI Builder.</li><li>Iestatiet atrašanās Azure Data Lake Storage vietas;</li></ul> | <ul><li>Dynamics 365</li><li>Microsoft Power Platform</li><li>Azure Data Lake Storage</li></ul> | <ul><li>Dynamics 365 administrators</li><li>Power Platform administrators</li><li>Krātuves BLOB datu īpašnieks</li></ul> |
| AI veidotājs      | <ul><li>Uzturēt plūsmas.</li><li>Izveidojiet pielāgotus AI modeļus.</li></ul> | <ul><li>Microsoft Power Platform</li></ul> | <ul><li>Pa pieņēmēji</li></ul> |
| Kreditoru darbinieks      | <ul><li>Pārskatīt un veikt darbības kreditora rēķina sagatavošanas apgabalā.</li><ul> | <ul><li>Microsoft Power Platform</li></ul> | <ul><li>Jauna kreditoru darbinieks loma programmā Power Platform</li></ul> |
| Kreditoru darbinieks      | <ul><li>Veiciet ikdienas operācijas kā AP darbinieks.</li><li>Pāriet uz kreditora rēķina sagatavošanas vietu.</li></ul> | <ul><li>Dynamics 365</li></ul> | <ul><li>Kreditoriem maksājamo parādu darbinieks</li></ul> |
  
Papildinformāciju par rēķina tveršanas instalēšanu skatiet sadaļā Rēķina [tveršanas instalēšana](../accounts-payable/install-invoice-capture.md).  
