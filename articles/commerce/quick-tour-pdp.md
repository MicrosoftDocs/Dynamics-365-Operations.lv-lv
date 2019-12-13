---
title: Preču detalizētas informācijas lapu apskats
description: Šajā tēmā sniegts pārskats par preču detalizētas informācijas (PDP) lapām Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3b02d50adbfcda27d590bcb87fd9669d67d4a01c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697869"
---
# <a name="overview-of-product-details-pages"></a>Preču detalizētas informācijas lapu apskats

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā sniegts pārskats par preču detalizētas informācijas (PDP) lapām Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

PDP sniedz detalizētu informāciju par preci, un ļaujiet klientiem izvēlēties preces opcijas, piemēram, izmēru, stilu un krāsu. PDP ir jāparāda visa preces informācija, kas klientam nepieciešama, lai pieņemtu lēmumu par pirkšanu.

Tālāk redzamajā attēlā parādīts PDP piemērs.

![Preces detalizētas informācijas lapas piemērs](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a>Galvenes un kājenes moduļi

PDP augšpusē ir virsraksts, kas parāda visas preču kategorijas un citas lapas, kuras mazumtirgotājs vēlas, lai klienti pārlūkotu. Lapas apakšpusē ir kājene, kas ietver ātras saites uz dažādām tēmām, kas varētu interesēt pircējus.

## <a name="buy-box-module"></a>Iegādes lodziņa modulis

Vissvarīgākais modulis PDP ir iegādes lodziņa modulis. Tāpēc tas ir pirmais vienums lapas galvenajā sadaļā. Iegādes lodziņa modulis ir konteinera modulis, un tas vieso vairākus moduļus, kas satur svarīgāko informāciju par preci. Šī informācija ietver preces nosaukumu, preces attēlus, aprakstu, cenu un preces vērtējumus.

Iegādes lodziņa modulis ļauj klientam izvēlēties preces opcijas (piemēram, izmēru, stilu un krāsu) un pievienot preci grozam. Tas arī ļauj klientam nopirkt preci tiešsaistē un saņemt to veikalā. Modulis pirkšanai tiešsaistē un saņemšanai veikalā izmanto integrāciju ar Bing Maps programmas programmēšanas interfeisiem (API), lai atrastu tuvumā esošos veikalus vai veikalus citā vietā, ko norāda klients.

Iegādes lodziņa modulim ir nepieciešams preces ID. Šis ID tiek iegūts no lapas konteksta. Ja iegādes lodziņa modulis ir pievienots lapai, kur lapas konteksts neietver preces ID, tas šo informāciju neatveidos pareizi.

## <a name="product-specifications-module"></a>Preces specifikāciju modulis

Preces specifikāciju modulis var tikt izmantots, lai parādītu papildu informāciju par preci. Šī detalizētā informācija tiek ņemta no preces īpašībām Dynamics 365 Retail. Preces specifikāciju modulis parāda katru īpašību, kur **redzams** rekvizīts ir iestatīts kā **patiess**. Lai izgūtu preces īpašības, ir nepieciešams preces ID.

## <a name="recommendations-module"></a>Ieteikumu modulis

Ieteikumu modulis ir svarīgs modulis PDP. Kamēr klienti meklē preces, tiem jāsniedz vairāk preču opciju, lai klienti varētu atrast pareizo preci un veikt pirkumu. Ieteikumi palīdz klientiem viegli atklāt saistīto saturu un turpināt iepirkties.

Ir pieejami dažādi ieteikumu sarakstu veidi.

- Saraksts **Pircējiem patīk arī** ir balstīts uz mašīnmācību. Lai sniegtu ieteikumus, tas izmanto citu klientu transakciju vēsturi. Šo sarakstu ģenerē ieteikumu pakalpojums un tas līdzinās sarakstiem "Klientiem, kas iegādājušies šo, nopirka arī...". Lai ģenerētu šo sarakstu, ir nepieciešams preces ID.
- Sarakstu **Saistīts** precei ir iespējams konfigurēt Retail. Piemēram, brūnai rokas ceļasomai no ādas saistītajā sarakstā var konfigurēt vairāk rokassomu, kas izgatavotas no ādas, vai paredzētas ceļošanai. Citus saistīto sarakstu veidus, piemēram, **Piederumi** un **Vairāk kā šis** arī var konfigurēt Retail. Lai ģenerētu šo sarakstu, ir nepieciešams preces ID. Tāpēc, ja tas ir pievienots sākumlapai, kur lapas konteksts neietver preces ID, saraksts būs tukšs.
- Algoritmiski ģenerētie ieteikumu saraksti, piemēram, **Populārs**, **Vispirktākais** un **Jauns** var tikt izmantoti PDP. Lai gan šie saraksti var nebūt tieši saistīti ar preci PDP, tas ir cits veids, kā palīdzēt klientiem atrast preces, kas varētu to interesēt. Šiem sarakstu veidiem nav nepieciešams preces ID. Tie ir vispārēji saraksti, kas tiek ģenerēti, balstoties uz iepirkšanās paradumiem visā vietnē.
- Redakcionālie saraksti ir manuāli pārraudzīti saraksti. Piemēram, mazumtirgotājs var nolemt manuāli pārraudzīt to preču sarakstus, ko tas vēlas parādīt.

## <a name="ratings-and-reviews-module"></a>Vērtējumu un apskatu modulis

Vērtējumu un apskatu modulis parāda vērtējumus un apskatus, ko snieguši citi klienti. Tas arī ļauj klientam uzrakstīt pašam savu preces apskatu. Turklāt tajā ir ietverta histogramma, kas parāda preces vērtējumu tendenci. Papildinformāciju skatiet [Pārskats par vērtējumiem un apskatiem](ratings-reviews-overview.md).

## <a name="marketing-modules"></a>Mārketinga moduļi

Ja mārketinga saturs ir unikāls konkrētai precei, PDP var pievienot jebkuru mārketinga moduli. Varat pievienot mārketinga moduļus PDP, izmantojot lapas "papildināšanu". 

## <a name="additional-resources"></a>Papildu resursi

[Sākumlapas pārskats](quick-tour-home-page.md)

[Noklusējuma kategorijas ielādes lapas un meklēšanas rezultātu lapas apskats](category-search-page-overview.md)

[Pārskats par grozu un norēķināšanās lapām](quick-tour-cart-checkout.md)

[Pārskats par konta pārvaldības lapām](quick-tour-account-management.md)
