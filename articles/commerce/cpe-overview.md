---
title: Commerce priekšskatījuma vides pārskats
description: Šajā tēmā ir sniegts pārskats par programmas Microsoft Dynamics 365 Commerce priekšskatījuma vidi.
author: v-chgri
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 901583afde4739be5313fa129ff0e52f11326881
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906074"
---
# <a name="commerce-preview-environment-overview"></a>Commerce priekšskatījuma vides pārskats

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā ir sniegts pārskats par programmas Microsoft Dynamics 365 Commerce priekšskatījuma vidi.

## <a name="overview"></a>Pārskats

Commerce priekšskatījuma vide ir vispārīga Dynamics 365 Commerce vide pēc izvēles, kas ļauj potenciālajiem klientiem izmēģināt Commerce preci pirms tās vispārējās laišanas publiskā tirdzniecībā.

Neņemot vērā dažus nelielus ierobežojumus, kas neietekmē līdzekļus vai funkcionalitāti, Commerce priekšskatījuma vide nodrošina pilnīgu Commerce pieredzi, un to var izmantot klienti un ieviešanas partneri, lai novērtētu preci, sniegtu atsauksmes un veiktu atbilstību analīzi.

## <a name="limitations-of-the-commerce-preview-environment"></a>Commerce priekšskatījuma vides ierobežojumi

Lai gan Commerce priekšskatījuma vide nodrošina pilnu Commerce līdzekļu un funkcionalitātes komplektu, ir daži nelieli ierobežojumi.

- Lai gan pašai Commerce priekšskatījuma videi nav ģeogrāfisku ierobežojumu, vides komponenti, piemēram, Retail Cloud Scale Unit (RSCU) un e-Commerce lietojumprogrammas, var tikt nodrošināti tikai Amerikas Savienotajās valstīs.
- Commerce priekšskatījuma vides izmantošana ir ierobežota līdz 30 dienām no dienas, kad tiek nodrošināta e-Commerce.
- Commerce priekšskatījuma vidi var veiksmīgi izvietot un inicializēt tikai vidē, kas izmanto izmēģinājuma topoloģiju, kur visi vides komponenti tiek izvietoti vienā virtuālajā mašīnā (VM). Galvenais ierobežojums šajā OneBox VM topoloģijā ir to vienlaicīgo lietotāju skaits, kuru priekšskatījuma vide var atbalstīt.
- Commerce priekšskatījuma vidi var novērtēt tikai līdz Commerce preces vispārējai pieejamībai (GA). Jaunas izmēģinājuma vides būs pieejamas pēc GA.

## <a name="get-started"></a>Sākt darbu

Lai varētu nodrošināt Commerce priekšskatījuma vidi, skatiet sadaļu [Commerce priekšskatījuma vides nodrošināšana ](provisioning-guide.md).

## <a name="additional-resources"></a>Papildu resursi

[Commerce priekšskatījuma vides nodrošināšana](provisioning-guide.md)

[Commerce priekšskatījuma vides konfigurēšana](cpe-post-provisioning.md)

[Neobligāto līdzekļu konfigurēšana Commerce priekšskatījuma videi](cpe-optional-features.md)

[Commerce priekšskatījuma vides BUJ](cpe-faq.md)
