---
title: Līdzekļu mēri
description: Tēmā ir paskaidrots, kā Līdzekļu pārvaldībā izveidot līdzekļu mēru tipus.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9c445832a649c4f6a6642036ecab325e8aa2079
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783441"
---
# <a name="asset-measures"></a>Līdzekļu mēri

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Tēmā ir paskaidrots, kā Līdzekļu pārvaldībā izveidot līdzekļu mēru tipus. Līdzekļu mēru tipi tiek izmantoti, lai veiktu līdzekļu mērījumu reģistrācijas, piemēram, attiecībā uz ražošanas stundu skaitu vai līdzeklim saražoto daudzumu. Līdzekļu tipi ir saistīti ar līdzekļu mēru tipiem. Tas nozīmē, ka līdzekļa mēru var izmantot līdzeklim tikai tad, ja līdzekļa mērs ir iestatīts līdzekļa tipam, kas izmantots līdzeklim.

Pirms varat veikt mērījumu reģistrācijas līdzekļiem, izveidojiet līdzekļu mēru tipus, kurus vēlaties izmantot **Skaitītājos**. Pēc tam varat izveidot mērījumu reģistrācijas līdzekļiem **Līdzekļu mēros**. 

Līdzekļu mērus var izmantot uzturēšanas plāniem. Uzturēšanas plāna rinda var būt ar tipu "Skaitītājs", piemēram, attiecībā uz ražošanas stundu skaitu vai saražoto daudzumu. 

Līdzekļu mērījumu reģistrāciju var atjaunināt manuāli vai automātiski, pamatojoties uz ražošanas laiku vai saražoto daudzumu. Līdzekļa mēru var iestatīt, lai izmantotu vienu no trim atjaunināšanas metodēm (kas atlasītas laukā **Atjaunināt** sadaļā **Skaitītāji**):
  
- Manuāli — līdzekļu mērījumu vērtības ir jāreģistrē manuāli.  
- Ražošanas stundas — skaitītājs tiek automātiski atjaunināts, pamatojoties uz ražošanas stundu skaitu.  
- Ražošanas daudzums — skaitītājs tiek automātiski atjaunināts, pamatojoties uz saražoto daudzumu.  

>[!NOTE]
>Ja tiek izmantots saražotais daudzums, *visi* reģistrētie krājumi tiek iekļauti mērījumu reģistrācijā — labais daudzums, kā arī kļūdu daudzums. Ja nepieciešams, vienmēr ir iespējams veikt manuālas līdzekļu mērījumu reģistrācijas.

## <a name="create-counter-types-for-asset-counter-registrations"></a>Skaitītāju tipu izveide līdzekļu skaitītāju reģistrācijām

1. Atlasiet **Līdzekļu pārvaldība** > **Iestatīšana** > **Līdzekļu tipi** > **Skaitītāji**.
2. Atlasiet **Jauns**, lai izveidotu jaunu līdzekļa mēra tipu.
3. Ievadiet ID laukā **Skaitītājs**, bet laukā **Nosaukums** — skaitītāja nosaukumu.
4. Kopsavilkuma cilnē **Vispārīgi** atlasiet mērvienību laukā **Vienība**.
5. Laukā **Atjaunināt** atlasiet atjaunināšanas metodi, kas jāizmanto līdzekļa mēram.
6. Atlasiet "Jā" pārslēgšanas pogā **Mantotās skaitītāja vērtības**, ja pakārtotajiem līdzekļiem līdzekļu struktūrā automātiski jāmanto līdzekļa mēra reģistrācijas, kas veiktas primārajam līdzeklim.
7. Laukā **Apkopotā kopsumma** atlasiet summēšanas metodi, kas jāizmanto līdzekļa mērā, izmantojot šo līdzekļa mēra tipu. "Summa" ir standarta atlase, ko izmanto, lai pastāvīgi pievienotu reģistrētās vērtības kopējai vērtībai. "Vidējo" var izmantot, ja līdzekļa mērs ir iestatīts, lai uzraudzītu sliekšņvērtību, piemēram, attiecībā uz temperatūru, vibrāciju vai aktīva nolietojumu un nodilumu. 
8. Laukā **Novirze virs** ievadiet augšējo līmeni procentos, lai pārbaudītu, vai manuālās līdzekļu mēru reģistrācijas ir paredzētajā diapazonā. Pārbaude ir balstīta uz esošo līdzekļu mēru reģistrāciju lineāru pieaugumu.
9. Laukā **Novirze zem** ievadiet apakšējo līmeni procentos, lai pārbaudītu, vai manuālās līdzekļu mēru reģistrācijas ir paredzētajā diapazonā. Pārbaude ir balstīta uz esošo līdzekļu mēru reģistrāciju lineāru samazinājumu.
10. Laukā **Tips** atlasiet ziņojuma tipu (informācija, brīdinājums, kļūda), kas jāparāda, ja, veicot manuālas līdzekļu mēru reģistrācijas, rodas novirzes ārpus noteiktā diapazona.
11. Kopsavilkuma cilnē **Līdzekļu tipi** pievienojiet līdzekļu tipus, kuriem būtu jāspēj izmantot līdzekļa mēru.
12. Kopsavilkuma cilnē **Saistītie līdzekļa mēri** pievienojiet līdzekļa mērus, kurus vēlaties atjaunināt automātiski, kad tiek atjaunināts šis līdzekļa mērs.


>[!NOTE]
>Saistītais līdzekļa mērs tiek automātiski atjaunināts tikai tad, ja saistītajam līdzekļa mēram līdzekļa mēra iestatījumos ir līdzekļa tips, ar kuru tas ir saistīts. Piemēram: jūs iestatāt līdzekļa mēru "Ražošanas stundām" un pievienojat līdzekļa tipu "Kravas automašīnas dzinējs". Kad šis līdzeklis tiek atjaunināts, atjaunināts tiek arī saistītais skaitītājs "Benzīns" ar tādām pašām aktīva mēra vērtībām. Iestatījumi **Skaitītājos** ietver iestatījumu "Stundas". Lai nodrošinātu līdzekļa mēru saistību, arī līdzekļa mērā "Benzīns" līdzekļa tips "Kravas automašīnas dzinējs" ir jāpievieno kopsavilkuma cilnei **Līdzekļu tipi**. Piemēru par Stundu un Benzīna līdzekļu mēriem skatiet ekrānuzņēmumos zemāk.

Kad līdzekļu tipi tiek pievienoti līdzekļa mēra tipam **Skaitītājos**, šī līdzekļa mērs tiek automātiski pievienots līdzekļu tipiem kopsavilkuma cilnē **Skaitītāji**[Aktīvu tipos](../setup-for-objects/object-types.md).

![1. attēls](media/071-setup-for-objects.png)


