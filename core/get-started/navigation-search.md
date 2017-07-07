---
title: "Navigācijas meklēšana"
description: "Šajā tēmā ir paskaidrots, kā izmantot meklēšanas funkcijas, lai pārietu uz lapām sistēmā Microsoft Dynamics 365 for Finance and Operations."
author: aneesmsft
manager: AnnBe
ms.date: 04/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 25991
ms.assetid: eef0676f-c4b1-490e-a032-e9c8580f3fea
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 431165d541c9a3b63100a93108ee770df8e88aa8
ms.contentlocale: lv-lv
ms.lasthandoff: 06/13/2017


---

# <a name="navigation-search"></a>Navigācijas meklēšana

[!include[banner](../includes/banner.md)]


Šajā tēmā ir paskaidrots, kā izmantot meklēšanas funkcijas, lai pārietu uz lapām sistēmā Microsoft Dynamics 365 for Finance and Operations.

Finance and Operations nodrošina funkcijas visdažādākajām nozarēm un vertikālēm. Lietojumprogrammā ir ietverti vairāki apgabali un lapas, kas palīdz veikt dažādus uzdevumus. Lai ātri atrastu uzdevumu veikšanai nepieciešamās lapas, izmantojiet navigācijas meklēšanas līdzekli. 

Lai izmantotu šo līdzekli, noklikšķiniet uz ikonas **Meklēšana**, lai parādītu lodziņu **Meklēšana**. Pēc tam varat ierakstīt lodziņā vienu vai vairākus vārdus. Sistēma programmā uzreiz meklē attiecīgās lapas, kuras atbilst ievadītajiem vārdiem. Piemēram, jūs varat ievadīt “kreditora rēķins”, un pēc tam sistēma parādīs rezultātus, kas atbilst ievadītajam tekstam. 

**Piezīme.** Lodziņš **Meklēšana** palīdz atrast lapas un pāriet uz tām. Tas nepalīdzēs jums atrast specifiskus datus vai darbības. 

[![search-box](media/navigation-search.png "Meklēšanas lodziņš") 

## <a name="quickly-navigate-to-a-particular-page"></a>Ātri pārvietoties uz konkrētu lapu
Navigācijas meklēšanas līdzeklis ir arī lielisks risinājums ātrai pāriešanai uz noteiktu lapu. Piemēram, ja esat kreditoriem maksājamo parādu darbinieks, kurš bieži lieto lapu **Maksājumu žurnāls**, tad lodziņā **Meklēt** varat ievadīt “maksājumu žurnāls”. Tā kā ievadītais teksts precīzi atbilst lapas nosaukumam, lapa tiek parādīta meklēšanas rezultātu saraksta augšpusē un varat ātri uz to navigēt. 

Meklēšanas rezultātu sarakstā tiek parādīts lapas nosaukums, kā arī navigācijas ceļš. Tas parāda lapas atrašanās vietu programmā. Tas arī palīdz atšķirt divas vai vairāk līdzīgas lapas rezultātos. 

Meklējot lapu, ievadītais teksts tiek salīdzināts ar lapas nosaukumu, kā arī tās navigācijas ceļu. Piemēram, lodziņā **Meklēt** ievadot vārdu “parādi”, tiks parādīti rezultāti lapām, kas jums ir pieejamas apgabalā Debitoru parādi, lai gan pašu lapu nosaukumos vārds “parādi” nav ietverts. 

## <a name="quickly-navigate-to-a-page-based-on-the-technical-form-name"></a>Ātri pārvietoties uz lapu, pamatojoties uz tehnisko formas nosaukumu
Navigācijas meklēšanas funkcionalitāte ietver arī pieprasītu līdzekli, kas paredzēts prasmīgiem lietotājiem: iespēju ātri pārvietoties uz lapu, pamatojoties uz tehnisko formas nosaukumu. Daudzi lietotāji ir tik labi pazīstami ar sistēmu, ka viņi zina precīzus to formu nosaukumus, ar kurām tie strādā. Ja esat viens no šiem lietotājiem, jūs varat ievadīt tekstu **forma:** un pēc tam norādīt meklējamās formas nosaukumu. Piemēram, ja ievadāt **forma: vendinvoice**, meklēšanas rezultāti parādīs visas lapas, kurās formas nosaukums sākas ar **vendinvoice**. 

## <a name="administration-and-security"></a>Administrēšana un drošība
No administrēšanas un drošības viedokļa navigācijas meklēšanas funkcionalitāte parāda tikai divu tālāk norādīto tipu rezultātus.

-   Lapas, kas ir iespējotas pašreizējā konfigurācijā (izmantojot konfigurācijas atslēgas).
-   Lapas, kurām lietotājam ir piekļuve, pamatojoties uz lietotāja lomu.

Meklēšanas rezultātu sarakstā tiek parādīti ne vairāk kā 10 vienumi. Ja jums neizdodas atrast meklēto rezultātos, mēģiniet precizēt vai atjaunināt ievadīto informāciju. 

## <a name="development"></a>Izstrāde 
No izstrādes viedokļa navigācijas meklēšanas funkcionalitāte ir ļoti vienkārši izmantojama, jo izvēļņu vienumus meklēšanas rezultātos ir iespējams parādīt gandrīz uzreiz pēc to izvietošanas. Ja uz izvēļņu vienumiem ir izveidota saite no navigācijas rūts vai informācijas paneļa, tie automātiski kļūst meklējami. 

