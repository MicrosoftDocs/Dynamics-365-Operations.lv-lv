---
title: Preču papildinformācijas lapu pārskats
description: Šajā tēmā sniegts pārskats par preču detalizētas informācijas (PDP) lapām Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b0f50b4e7b78f4a5b9fe674a101476879923e10d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979832"
---
# <a name="product-details-pages-overview"></a>Preču papildinformācijas lapu pārskats

[!include [banner](includes/banner.md)]

Šajā tēmā sniegts pārskats par preču detalizētas informācijas (PDP) lapām Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

PDP sniedz detalizētu informāciju par preci, un ļaujiet klientiem izvēlēties preces opcijas, piemēram, izmēru, stilu un krāsu. PDP ir jāparāda visa preces informācija, kas klientam nepieciešama, lai pieņemtu lēmumu par pirkšanu.

Tālāk redzamajā attēlā parādīts PDP piemērs.

![Preces detalizētas informācijas lapas piemērs](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a>Galvenes un kājenes moduļi

PDP augšpusē ir virsraksts, kas parāda visas preču kategorijas un citas lapas, kuras mazumtirgotājs vēlas, lai klienti pārlūkotu. Lapas apakšpusē ir kājene, kas ietver ātras saites uz dažādām tēmām, kas varētu interesēt pircējus.

## <a name="buy-box-module"></a>Pirkšanas lodziņa modulis

Nozīmīgākais modulis PDP ir pirkšanas loga modulis, kas tiek parādīts kā pirmais vienums lapas galvenajā sadaļā. Pirkšanas loga modulis parāda svarīgu informāciju par preci, piemēram, preces nosaukumu, preces aprakstu, preces cenu, preces attēlus un preces vērtējumu.

Iegādes lodziņa modulis ļauj klientam izvēlēties preces opcijas (piemēram, izmēru, stilu un krāsu) un pievienot preci grozam. Tas arī ļauj klientam nopirkt preci tiešsaistē un saņemt to veikalā. Modulis pirkšanai tiešsaistē un saņemšanai veikalā izmanto integrāciju ar Bing Maps programmas programmēšanas interfeisiem (API), lai atrastu tuvumā esošos veikalus vai veikalus citā vietā, ko norāda klients.

Iegādes lodziņa modulim ir nepieciešams preces ID. Šis ID tiek iegūts no lapas konteksta. Ja iegādes lodziņa modulis ir pievienots lapai, kur lapas konteksts neietver preces ID, tas šo informāciju neatveidos pareizi.

## <a name="product-specifications-module"></a>Preces specifikāciju modulis

Preces specifikāciju modulis var tikt izmantots, lai parādītu papildu informāciju par preci. Šī detalizētā informācija tiek ņemta no preces īpašībām programmā Commerce. Preces specifikāciju modulis parāda katru īpašību, kur **redzams** rekvizīts ir iestatīts kā **patiess**. Lai izgūtu preces īpašības, ir nepieciešams preces ID.

## <a name="recommendations-module"></a>Ieteikumu modulis

Ieteikumu modulis ir svarīgs modulis PDP. Kamēr klienti meklē preces, tiem jāsniedz vairāk preču opciju, lai klienti varētu atrast pareizo preci un veikt pirkumu. Ieteikumi palīdz klientiem viegli atklāt saistīto saturu un turpināt iepirkties.

Ir pieejami dažādi ieteikumu sarakstu veidi.

- Saraksts **Pircējiem patīk arī** ir balstīts uz mašīnmācību. Lai sniegtu ieteikumus, tas izmanto citu klientu darījumu vēsturi. Šo sarakstu ģenerē ieteikumu pakalpojums un tas līdzinās sarakstiem "Klientiem, kas iegādājušies šo, nopirka arī...". Lai ģenerētu šo sarakstu, ir nepieciešams preces ID.
- Sarakstu **Saistīts** precei ir iespējams konfigurēt programmā Commerce. Piemēram, brūnai rokas ceļasomai no ādas saistītajā sarakstā var konfigurēt vairāk rokassomu, kas izgatavotas no ādas, vai paredzētas ceļošanai. Citus saistīto sarakstu veidus, piemēram, **Piederumi** un **Vairāk līdzīgu preču** arī var konfigurēt programmā Commerce. Lai ģenerētu šo sarakstu, ir nepieciešams preces ID. Tāpēc, ja tas ir pievienots mājas lapai, kur lapas konteksts neietver preces ID, saraksts būs tukšs.
- Algoritmiski ģenerētie ieteikumu saraksti, piemēram, **Populārs**, **Vispirktākais** un **Jauns** var tikt izmantoti PDP. Lai gan šie saraksti var nebūt tieši saistīti ar preci PDP, tas ir cits veids, kā palīdzēt klientiem atrast preces, kas varētu to interesēt. Šiem sarakstu veidiem nav nepieciešams preces ID. Tie ir vispārēji saraksti, kas tiek ģenerēti, balstoties uz iepirkšanās paradumiem visā vietnē.
- Rediģējamie saraksti ir manuāli pārraudzīti saraksti. Piemēram, mazumtirgotājs var nolemt manuāli pārraudzīt to preču sarakstus, ko tas vēlas parādīt.

## <a name="ratings-and-reviews-modules"></a>Vērtējumu un apskatu moduļi

Var izmantot trīs moduļus, lai parādītu un pievienotu pārskatus:

- **Apskati** – Šis modulis parāda vērtējumus un apskatus, ko snieguši citi klienti. Debitori var šķirot un filtrēt pārskatus. Šis modulis ļauj arī klientiem atzinīgi vai negatīvi novērtēt apskatus, kā arī ziņot par problēmām.
- **Rakstīt apskati** – Šis modulis ļauj klientiem rakstīt savus apskatus par preci.
- **Vērtējumu histogramma** – šis modulis ietver histogrammu, kas parāda preces reitingu tendenci.

Papildinformāciju skatiet [Pārskats par vērtējumiem un apskatiem](ratings-reviews-overview.md).

## <a name="marketing-modules"></a>Mārketinga moduļi

Ja mārketinga saturs ir unikāls konkrētai precei, PDP var pievienot jebkuru mārketinga moduli. Varat pievienot mārketinga moduļus PDP, izmantojot lapas "papildināšanu". Plašāku informāciju skatiet [Preces lapas bagātināšana](enrich-product-page.md).

## <a name="additional-resources"></a>Papildu resursi

[Mājas lapas pārskats](quick-tour-home-page.md)

[Pārskats par grozu un norēķināšanās lapām](quick-tour-cart-checkout.md)

[Konta pārvaldības lapu pārskats](quick-tour-account-management.md)

[Preces informācijas bagātināšanas lapa](enrich-product-page.md)
