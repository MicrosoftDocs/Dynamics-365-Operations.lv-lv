---
title: Bieži uzdotie jautājumi par Dynamics 365 Commerce novērtējuma vidi
description: Šajā tēmā sniegtas atbildes uz bieži uzdotiem jautājumiem par Microsoft Dynamics 365 Commerce novērtēšanas vidi.
author: v-chgri
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a0c6f82432a4786f23f12122f3806c3b96a05c8f
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193598"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a>Dynamics 365 Commerce novērtēšanas vides BUJ

[!include [banner](includes/banner.md)]

Šajā tēmā sniegtas atbildes uz bieži uzdotiem jautājumiem par Microsoft Dynamics 365 Commerce novērtēšanas vidi.

**Vai mēs varam izmantot Commerce novērtējuma vidi kā e-komercijas vitrīnu klientiem, kas pašlaik ievieš mazumtirdzniecību?**

Nr.p.k. Commerce novērtējuma vide ir paredzēta tikai novērtēšanai. Ja jums ir nepieciešama vide, kurā tiek ieviesta mazumtirdzniecība, sazinieties ar Microsoft.

**Vai Commerce novērtējuma vidi var izmantot, lai nodrošinātu e-komercijas funkcijas papildu esošajam pieteikumam/videi, kas ievieš mazumtirdzniecību?**

Nē (galvenokārt). Commerce novērtēšanas komponenti ir pieejami tikai vidēm, kas atbilst konfigurācijām, kas norādītas priekšnosacījumos un nodrošināšanas ceļvedī. Turklāt nepieciešamie bāzes demonstrācijas dati nebūs pieejami vidēs, kas tika izvietotas ar sākotnējo laidienu, kas ir agrāks par 10.0.8. 

**Kādas izmaksas ir saistītas ar Commerce novērtējuma vides izvietošanu pakalpojumā Microsoft Azure, izmantojot Microsoft Dynamics Lifecycle Services (LCS)?**

Tradicionālā Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce Headquarters demonstrācijas vide (virtuālā mašīna \[VM\]) tiks viesota jūsu Azure abonementā. Lai novērtētu šīs izmaksas, varat izmantot [Azure cenu kalkulatoru](https://azure.microsoft.com/pricing/calculator/).

Citi komponenti, piemēram, Commerce Scale Unit, Commerce vietņu veidotājs un jūsu e-komercijas vietne būs pieejama kā programmatūras pakalpojums (SaaS) un tiks viesoti Microsoft.

**Kuras Azure ģeogrāfiskās īpašības pašlaik tiek atbalstītas Commerce novērtējuma videi?**

Commerce novērtējuma vidi var izvietot tikai Ziemeļamerikā.

**Vai ir lejupielādējams virtuāls cietais disks (VHD), kurā ir pilnīga OneBox virtuālās mašīnas (VM) opcija?**

Dynamics 365 Commerce un Commerce Scale Unit ir pilnīgi programmatūras pakalpojumi (SaaS), un tiem ir jābūt viesotiem mākonī.

**Cik ilgi var izmantot Commerce novērtējuma vidi?**

Commerce novērtējuma videi ir 30 dienu laika ierobežojums no datuma, kad tiek nodrošināti SaaS komponenti, piemēram, Commerce Scale Unit, Commerce vietņu veidotājs un jūsu e-komercijas vietne.

**Vai es varu pagarināt laika ierobežojumu savai Commerce novērtējuma videi?**

Laika ierobežojuma pagarināšana ir normas izņēmums un tiek apsvērti katrā gadījumā atsevišķi. Lai saņemtu palīdzību, sazinieties ar Microsoft partnera kontaktpersonu.

## <a name="additional-resources"></a>Papildu resursi

[Dynamics 365 Commerce novērtējuma vides pārskats](cpe-overview.md)

[Nodrošināt Dynamics 365 Commerce novērtējuma vidi](provisioning-guide.md)

[Konfigurēt Dynamics 365 Commerce novērtējuma vidi](cpe-post-provisioning.md)

[BOPIS konfigurācija Dynamics 365 Commerce novērtējuma videi](cpe-bopis.md)

[Izvēles funkciju konfigurācija Dynamics 365 Commerce novērtējuma videi](cpe-optional-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]