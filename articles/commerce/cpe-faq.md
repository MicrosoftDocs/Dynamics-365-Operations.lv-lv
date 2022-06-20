---
title: Dynamics 365 Commerce novērtēšanas vides BUJ
description: Šajā rakstā ir sniegtas atbildes uz bieži uzdotiem jautājumiem par Microsoft Dynamics 365 Commerce novērtēšanas vidi.
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
ms.openlocfilehash: 94717c1b9ff4ec05ee9734e1471a137cef55edfe
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861944"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a>Dynamics 365 Commerce novērtēšanas vides BUJ

[!include [banner](includes/banner.md)]

Šajā rakstā ir sniegtas atbildes uz bieži uzdotiem jautājumiem par Microsoft Dynamics 365 Commerce novērtēšanas vidi.

## <a name="can-we-use-the-commerce-evaluation-environment-as-an-e-commerce-storefront-for-customers-that-currently-implement-retail"></a>Vai mēs varam izmantot Commerce novērtējuma vidi kā e-komercijas vitrīnu klientiem, kas pašlaik ievieš mazumtirdzniecību?

Nr.p.k. Commerce novērtējuma vide ir paredzēta tikai novērtēšanai. Ja jums ir nepieciešama vide, kurā tiek ieviesta mazumtirdzniecība, sazinieties ar Microsoft.

## <a name="can-the-commerce-evaluation-environment-be-used-to-provision-the-e-commerce-features-on-top-of-an-existing-applicationenvironment-that-implements-retail"></a>Vai Commerce novērtējuma vidi var izmantot, lai nodrošinātu e-komercijas funkcijas papildu esošajam pieteikumam/videi, kas ievieš mazumtirdzniecību?

Nē (galvenokārt). Commerce novērtēšanas komponenti ir pieejami tikai vidēm, kas atbilst konfigurācijām, kas norādītas priekšnosacījumos un nodrošināšanas ceļvedī. Turklāt nepieciešamie bāzes demonstrācijas dati nebūs pieejami vidēs, kas tika izvietotas ar sākotnējo laidienu, kas ir agrāks par 10.0.8. 

## <a name="what-costs-are-involved-in-deploying-the-commerce-evaluation-environment-on-microsoft-azure-via-microsoft-dynamics-lifecycle-services-lcs"></a>Kādas izmaksas ir saistītas ar Commerce novērtējuma vides izvietošanu pakalpojumā Microsoft Azure, izmantojot Microsoft Dynamics Lifecycle Services (LCS)?

Tradicionāla Dynamics 365 Finanšu//Dynamics 365 Supply Chain Management Dynamics 365 Commerce galveno pārvaldes demonstrācijas vide (virtuālā \[mašīna VM\]) tiks viesota Jūsu Azure abonementā. Lai novērtētu šīs izmaksas, varat izmantot [Azure cenu kalkulatoru](https://azure.microsoft.com/pricing/calculator/).

Citi komponenti, piemēram, Commerce Scale Unit, Commerce vietņu veidotājs un jūsu e-komercijas vietne būs pieejama kā programmatūras pakalpojums (SaaS) un tiks viesoti Microsoft.

## <a name="which-azure-geographies-are-currently-supported-for-the-commerce-evaluation-environment"></a>Kuras Azure ģeogrāfiskās īpašības pašlaik tiek atbalstītas Commerce novērtējuma videi?

Commerce novērtējuma vidi var izvietot tikai Ziemeļamerikā.

## <a name="is-there-a-downloadable-virtual-hard-disk-vhd-that-has-the-complete-onebox-virtual-machine-vm-option"></a>Vai ir lejupielādējams virtuāls cietais disks (VHD), kurā ir pilnīga OneBox virtuālās mašīnas (VM) opcija?

Dynamics 365 Commerce un Commerce Scale Unit ir pilnīgi programmatūras pakalpojumi (SaaS), un tiem ir jābūt viesotiem mākonī.

## <a name="how-long-can-the-commerce-evaluation-environment-be-used"></a>Cik ilgi var izmantot Commerce novērtējuma vidi?

Commerce novērtējuma videi ir 30 dienu laika ierobežojums no datuma, kad tiek nodrošināti SaaS komponenti, piemēram, Commerce Scale Unit, Commerce vietņu veidotājs un jūsu e-komercijas vietne.

## <a name="can-i-extend-the-time-limit-for-my-commerce-evaluation-environment"></a>Vai es varu pagarināt laika ierobežojumu savai Commerce novērtējuma videi?

Laika ierobežojuma pagarināšana ir normas izņēmums un tiek apsvērti katrā gadījumā atsevišķi. Lai saņemtu palīdzību, sazinieties ar Microsoft partnera kontaktpersonu.

## <a name="additional-resources"></a>Papildu resursi

[Dynamics 365 Commerce novērtējuma vides pārskats](cpe-overview.md)

[Nodrošināt Dynamics 365 Commerce novērtējuma vidi](provisioning-guide.md)

[Konfigurēt Dynamics 365 Commerce novērtējuma vidi](cpe-post-provisioning.md)

[BOPIS konfigurācija Dynamics 365 Commerce novērtējuma videi](cpe-bopis.md)

[Izvēles funkciju konfigurācija Dynamics 365 Commerce novērtējuma videi](cpe-optional-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
