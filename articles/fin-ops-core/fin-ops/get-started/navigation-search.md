---
title: Navigācijas meklēšana
description: Šajā rakstā ir izskaidrots, kā izmantot meklēšanas funkcionalitāti, lai naviģētu uz lapām.
author: jasongre
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 25991
ms.assetid: eef0676f-c4b1-490e-a032-e9c8580f3fea
ms.openlocfilehash: 4c362e4cd83f926e7e21d775abd24ae6ddfcbbed
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292343"
---
# <a name="navigation-search"></a>Navigācijas meklēšana

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Šajā rakstā ir izskaidrots, kā izmantot meklēšanas funkcionalitāti, lai naviģētu uz lapām.

Lietojumprogrammā ir ietverti vairāki apgabali un lapas, kas palīdz veikt dažādus uzdevumus. Lai ātri atrastu uzdevumu veikšanai nepieciešamās lapas, izmantojiet navigācijas meklēšanas līdzekli.

Lai izmantotu šo līdzekli, noklikšķiniet uz ikonas **Meklēšana**, lai parādītu lodziņu **Meklēšana**. Pēc tam varat ierakstīt lodziņā vienu vai vairākus vārdus. Sistēma programmā uzreiz meklē attiecīgās lapas, kuras atbilst ievadītajiem vārdiem. Piemēram, jūs varat ievadīt “kreditora rēķins”, un pēc tam sistēma parādīs rezultātus, kas atbilst ievadītajam tekstam.

> [!NOTE]
> Lodziņš **Meklēšana** palīdz atrast lapas un pāriet uz tām. Tas nepalīdzēs jums atrast specifiskus datus vai darbības.

![meklēšanas lodziņš.](media/navigation-search.png "Meklēšanas lodziņš")

## <a name="quickly-navigate-to-a-particular-page"></a>Ātri pārvietoties uz konkrētu lapu

Navigācijas meklēšanas līdzeklis ir arī lielisks risinājums ātrai pāriešanai uz noteiktu lapu. Piemēram, ja esat kreditoriem maksājamo parādu darbinieks, kurš bieži lieto lapu **Maksājumu žurnāls**, tad lodziņā **Meklēt** varat ievadīt “maksājumu žurnāls”. Tā kā ievadītais teksts precīzi atbilst lapas nosaukumam, lapa tiek parādīta meklēšanas rezultātu saraksta augšpusē un varat ātri uz to navigēt.

Meklēšanas rezultātu sarakstā tiek parādīts lapas nosaukums, kā arī navigācijas ceļš. Tas parāda lapas atrašanās vietu programmā. Tas arī palīdz atšķirt divas vai vairāk līdzīgas lapas rezultātos.

Meklējot lapu, ievadītais teksts tiek salīdzināts ar lapas nosaukumu, kā arī tās navigācijas ceļu. Piemēram, ievadot vārdu “parādi” lodziņā **Meklēšana**, tiks parādīti rezultāti ar lapām, kas jums pieejamas apgabalā Debitoru parādi, lai arī lapu nosaukumā vārds “parādi” nav ietverts.

## <a name="quickly-navigate-to-a-page-based-on-the-technical-form-name"></a>Ātri pārvietoties uz lapu, pamatojoties uz tehnisko formas nosaukumu

Navigācijas meklēšanas funkcionalitāte ietver arī pieprasītu līdzekli, kas paredzēts prasmīgiem lietotājiem: iespēju ātri pārvietoties uz lapu, pamatojoties uz tehnisko formas nosaukumu. Daudzi lietotāji ir tik labi pazīstami ar sistēmu, ka viņi zina precīzus to formu nosaukumus, ar kurām tie strādā. Ja esat viens no šiem lietotājiem, jūs varat ievadīt tekstu **forma:** un pēc tam norādīt meklējamās formas nosaukumu. Piemēram, ja ievadāt **forma: vendinvoice**, meklēšanas rezultāti parādīs visas lapas, kurās formas nosaukums sākas ar **vendinvoice**.

## <a name="administration-and-security"></a>Administrēšana un drošība

No administrēšanas un drošības viedokļa navigācijas meklēšanas funkcionalitāte parāda tikai divu tālāk norādīto tipu rezultātus.

- Lapas, kas ir iespējotas pašreizējā konfigurācijā (izmantojot konfigurācijas atslēgas).
- Lapas, kurām lietotājam ir piekļuve, pamatojoties uz lietotāja lomu.

Meklēšanas rezultātu sarakstā tiek parādīti ne vairāk kā 10 vienumi. Ja jums neizdodas atrast meklēto rezultātos, mēģiniet precizēt vai atjaunināt ievadīto informāciju.

## <a name="development"></a>Izstrāde

No izstrādes viedokļa navigācijas meklēšanas funkcionalitāte ir ļoti vienkārši izmantojama, jo izvēļņu vienumus meklēšanas rezultātos ir iespējams parādīt gandrīz uzreiz pēc to izvietošanas. Ja uz izvēļņu vienumiem ir izveidota saite no navigācijas rūts vai informācijas paneļa, tie automātiski kļūst meklējami.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
