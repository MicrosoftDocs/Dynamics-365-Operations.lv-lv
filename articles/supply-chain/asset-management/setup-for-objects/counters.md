---
title: Līdzekļu mēri
description: Tēmā ir paskaidrots, kā Līdzekļu pārvaldībā izveidot līdzekļu mēru tipus.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectCounterPart, EntAssetObjectCounterLookup, EntAssetCounterType, EntAssetObjectCounterTotals
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: adadb1df7b41488fad496f937ecbc24e0761e42d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432886"
---
# <a name="counters"></a>Skaitītāji

[!include [banner](../../includes/banner.md)]

Tēmā ir paskaidrots, kā Līdzekļu pārvaldībā izveidot līdzekļu skaitītāju veidus. Skaitītāju veidi tiek izmantoti, lai veiktu līdzekļu skaitītāju reģistrācijas, piemēram, attiecībā uz ražošanas stundu skaitu vai līdzeklim saražoto daudzumu. Līdzekļu veidi ir saistīti ar skaitītāju veidiem. Tas nozīmē, ka skaitītāju var izmantot līdzeklim tikai tad, ja skaitītājs ir iestatīts līdzekļa veidam, kas izmantots līdzeklim.

Pirms varat veikt skaitītāju reģistrācijas līdzekļiem, izveidojiet skaitītāju veidus, kurus vēlaties izmantot **Skaitītājos**. Pēc tam varat izveidot skaitītāju reģistrācijas līdzekļiem **Skaitītājos**. 

Skaitītājus var izmantot uzturēšanas plāniem. Uzturēšanas plāna rinda var būt ar tipu "Skaitītājs", piemēram, attiecībā uz ražošanas stundu skaitu vai saražoto daudzumu. 

Skaitītāju reģistrāciju var atjaunināt manuāli vai automātiski, pamatojoties uz ražošanas laiku vai saražoto daudzumu. Skaitītāju var iestatīt, lai izmantotu vienu no trim atjaunināšanas metodēm (kas atlasītas laukā **Atjaunināt** sadaļā **Skaitītāji**):
  
- Manuāli — skaitītāja vērtības ir jāreģistrē manuāli.  
- Ražošanas stundas — skaitītājs tiek automātiski atjaunināts, pamatojoties uz ražošanas stundu skaitu.  
- Ražošanas daudzums — skaitītājs tiek automātiski atjaunināts, pamatojoties uz saražoto daudzumu.  

>[!NOTE]
>Ja tiek izmantots saražotais daudzums, *visi* reģistrētie krājumi tiek iekļauti skaitītāju reģistrācijā — labais daudzums, kā arī kļūdu daudzums. Ja nepieciešams, vienmēr ir iespējams veikt manuālas skaitītāju reģistrācijas.

## <a name="create-counter-types-for-asset-counter-registrations"></a>Skaitītāju tipu izveide līdzekļu skaitītāju reģistrācijām

1. Atlasiet **Līdzekļu pārvaldība** > **Iestatīšana** > **Līdzekļu tipi** > **Skaitītāji**.
2. Atlasiet **Jauns**, lai izveidotu jaunu skaitītāja veidu.
3. Ievadiet ID laukā **Skaitītājs**, bet laukā **Nosaukums** — skaitītāja nosaukumu.
4. Kopsavilkuma cilnē **Vispārīgi** atlasiet skaitītāja vienību laukā **Vienība**.
5. Laukā **Atjaunināt** atlasiet atjaunināšanas metodi, kas jāizmanto līdzekļa skaitītājam.
6. Atlasiet "Jā" pārslēgšanas pogā **Mantotās skaitītāja vērtības**, ja pakārtotajiem līdzekļiem līdzekļu struktūrā automātiski jāmanto skaitītāja reģistrācijas, kas veiktas primārajam līdzeklim.
7. Laukā **Apkopotā kopsumma** atlasiet summēšanas metodi, kas jāizmanto skaitītājā, izmantojot šo skaitītāja veidu. "Summa" ir standarta atlase, ko izmanto, lai pastāvīgi pievienotu reģistrētās vērtības kopējai vērtībai. "Vidējo" var izmantot, ja skaitītājs ir iestatīts, lai uzraudzītu sliekšņvērtību, piemēram, attiecībā uz temperatūru, vibrāciju vai aktīva nolietojumu un nodilumu. 
8. Laukā **Novirze virs** ievadiet augšējo līmeni procentos, lai pārbaudītu, vai manuālās skaitītāja reģistrācijas ir paredzētajā diapazonā. Pārbaude ir balstīta uz esošo skaitītāju reģistrāciju lineāru pieaugumu.
9. Laukā **Novirze zem** ievadiet apakšējo līmeni procentos, lai pārbaudītu, vai manuālās skaitītāja reģistrācijas ir paredzētajā diapazonā. Pārbaude ir balstīta uz esošo skaitītāju reģistrāciju lineāru samazinājumu.
10. Laukā **Tips** atlasiet ziņojuma tipu (informācija, brīdinājums, kļūda), kas jāparāda, ja, veicot manuālas skaitītāju reģistrācijas, rodas novirzes ārpus noteiktā diapazona.
11. Kopsavilkuma cilnē **Līdzekļu tipi** pievienojiet līdzekļu tipus, kuriem būtu jāspēj izmantot skaitītāju.
12. Kopsavilkuma cilnē **Saistītie skaitītāji** pievienojiet skaitītājus, kurus vēlaties atjaunināt automātiski, kad tiek atjaunināts šis skaitītājs.


>[!NOTE]
>Saistītais skaitītājs tiek automātiski atjaunināts tikai tad, ja saistītajam skaitītājam skaitītāja iestatījumos ir līdzekļa veids, ar kuru tas ir saistīts. Piemēram: jūs iestatāt skaitītāju "Ražošanas stundām" un pievienojat līdzekļa veidu "Kravas automašīnas dzinējs". Kad šis skaitītājs tiek atjaunināts, atjaunināts tiek arī saistītais skaitītājs "Benzīns" ar tādām pašām skaitītāja vērtībām. Iestatījumi **Skaitītājos** ietver iestatījumu "Stundas". Lai nodrošinātu skaitītāju saistību, arī skaitītājā "Benzīns" līdzekļa veids "Kravas automašīnas dzinējs" ir jāpievieno kopsavilkuma cilnei **Līdzekļu veidi**. Piemēru par Stundu un Benzīna skaitītājiem skatiet ekrānuzņēmumos zemāk.

Kad līdzekļu veidi tiek pievienoti skaitītāja veidam **Skaitītājos**, šis skaitītājs tiek automātiski pievienots līdzekļu veidiem kopsavilkuma cilnē **Skaitītāji** [Līdzekļu veidi](../setup-for-objects/object-types.md).

![1. attēls](media/071-setup-for-objects.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]