---
title: Nav ģenerēts TaxTrans ieraksts
description: Šajā tēmā ir sniegta traucējummeklēšanas informācija, kas var palīdzēt, kad nav ģenerēts TaxTrans ieraksts.
author: qire
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 969d086c77b40b59495ae0d9e631579abf5e0ec6
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686412"
---
# <a name="taxtrans-record-isnt-generated"></a>Nav ģenerēts TaxTrans ieraksts

[!include [banner](../includes/banner.md)]

Ja transakcijai atlasāt **Grāmatots PVN**, bet lapa **Grāmatots PVN** vai nu nerāda nodokļu rindas, vai arī tai trūkst nodokļu rindas, iespējams, netiks ģenerēts **TaxTrans** ieraksts.

[![Grāmatota PVN lapa, kurā nav rindas krājumu.](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)

Lai novērstu šo problēmu, ja nepieciešams, veiciet tālāk norādītās darbības.

## <a name="check-the-sales-tax-before-you-post-the-transaction"></a>Pārbaudīt PVN pirms transakcijas grāmatošanas

1. Pirms transakcijas grāmatošanas lapā **Rēķina grāmatošana** atlasiet **PVN**, lai pārbaudītu aprēķinu.

    [![PVN poga rēķina grāmatošanas lapā.](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)

2. Lapā **Pagaidu PVN transakcijas** pārskatiet aprēķina rezultātus. Ja nodoklis netiek aprēķināts, skatiet [Nodoklis nav aprēķināts vai nodokļa summa ir nulle](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).

## <a name="find-the-taxtrans-record-in-all-posted-sales-tax"></a>Atrast TaxTrans ierakstu visos grāmatotos PVN

1. Dodieties uz **Nodokļi** \> **Pieprasījumi un pārskati** \> **PVN pieprasījumi** > **Grāmatotais PVN**.
2. Kolonnas **Dokuments** virsrakstā atlasiet filtra simbolu, lai atrastu **TaxTrans** ierakstu.
3. Ja meklējat PVN ierakstus, pārbaudiet datumu. Ja datums atšķiras no žurnāla virsraksta datuma, izveidojiet Microsoft pakalpojuma pieprasījumu papildu atbalstam.

    [![Grāmatota PVN lapa.](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)

## <a name="debug-to-check-details"></a>Atkļūdot, lai pārbaudītu detaļas

1. Informāciju par to, kā atkļūdot un noteikt, vai **TmpTaxWorkTrans** un **TaxUncommitted** ir pareizi ģenerētas, skatiet [Lauku vērtība TaxTrans ir nepareiza](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).
2. Ja **TaxTmpWorkTrans** vai **TaxUncommitted** ir pareizi ģenerēts, pievienojiet pārtraukumpunktu pie **TaxPost::SaveAndPost()** un **Tax::SaveAndPost**, lai atkļūdotu iemeslu, kāpēc **TaxTrans** nav ievietots.

    [![Kodā pievienoti pārtraukumpunkti.](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)

    [![Pievienoto pārtraukumpunktu rezultāti.](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)

## <a name="determine-whether-customization-exists"></a>Noteikt, vai pielāgojums pastāv

Ja esat pabeidzis iepriekšējās sadaļās norādītās darbības, bet nav atraduši nekādu problēmu, nosakiet, vai pielāgošana eksistē. Ja pielāgošana nepastāv, izveidojiet Microsoft pakalpojuma pieprasījumu turpmākam atbalstam.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
