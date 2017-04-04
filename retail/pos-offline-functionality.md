---
title: "POS bezsaistes funkcionalitāte"
description: "Šajā rakstā ir sniegta informācija par Retail Modern POS bezsaistes režīmu, kurā POS ierīces no kanāla datu bāzes automātiski pārslēdzas uz bezsaistes datu bāzi, ja mazumtirdzniecības serveris nav pieejams. Šajā rakstā ir ietverta arī vispārīga iestatīšanas informācija bezsaistes režīmam un skaidrota datu sinhronizēšana, kas notiek starp bezsaistes datu bāzi un kanāla datu bāzi."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27041
ms.assetid: 20b51874-8912-40cf-9296-864df707315a
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ef4d20b3302e4a420c7013b77a57ebdfa99fe6a3
ms.lasthandoff: 03/31/2017


---

# <a name="pos-offline-functionality"></a>POS bezsaistes funkcionalitāte

Šajā rakstā ir sniegta informācija par Retail Modern POS bezsaistes režīmu, kurā POS ierīces no kanāla datu bāzes automātiski pārslēdzas uz bezsaistes datu bāzi, ja mazumtirdzniecības serveris nav pieejams. Šajā rakstā ir ietverta arī vispārīga iestatīšanas informācija bezsaistes režīmam un skaidrota datu sinhronizēšana, kas notiek starp bezsaistes datu bāzi un kanāla datu bāzi.

<a name="overview"></a>Pārskats
--------

Mazumtirdzniecība modernas POS, sale (POS) ierīces punktā tērēta bezsaistes režīmā ikreiz, kad mazumtirdzniecības serveris nav pieejams. Tādēļ, ja ir zaudēts savienojums ar serveri, mazumtirdzniecības, mazumtirdzniecības mūsdienu POS automātiski pārslēdzas uz bezsaistes datu bāzi. Pārdošanas transakcijas laikā, ja datu pieprasījums netiek sekmīgi izpildīts bezsaistes profilā konfigurētajā taimauta intervālā, tad Retail Modern POS automātiski pārslēdzas uz bezsaistes datu bāzi un turpina pārdošanas transakciju. Kamēr POS ierīce atrodas bezsaistes režīmā, Retail Modern POS mēģina atjaunot savienojumu ar mazumtirdzniecības serveri pēc bezsaistes profilā konfigurētā atkārtotas pievienošanās mēģinājuma intervāla. Šāds atkārtotas pievienošanās mēģinājums notiek tikai transakcijas sākumā.

### <a name="determining-the-connection-mode-of-retail-modern-pos"></a>Retail Modern POS savienojuma režīma noteikšana

Retail Modern POS statusa virsraksts norāda pašreizējo savienojuma statusu, un logā **Savienojuma statuss** tiek rādīts statuss pēdējam mēģinājumam sinhronizēties ar bezsaistes datu bāzi. [![Connection status](./media/status.png)](./media/status.png)

### <a name="creating-a-button-to-manually-switch-between-online-and-offline-modes"></a>Pogas izveidošana, lai manuāli pārslēgtos starp tiešsaistes un bezsaistes režīmiem

Retail Modern POS varat pievienot pogu, lai manuāli pārslēgtos starp tiešsaistes un bezsaistes režīmiem. Izveidojiet pogu POS operācijai **917 — Datu bāzes savienojuma statuss**. Šīs pogas nosaukums ir **Atvienot**, kad Retail Modern POS ir izveidots savienojums ar mazumtirdzniecības serveri, un nosaukums ir **Savienot**, kad tas ir atvienots. Šo pogu varat izmantot, lai skatītu savienojumu, un lai atvienotos no mazumtirdzniecības servera vai izveidotu savienojumu ar to. [![Atvienot pogu mazumtirdzniecības mūsdienu POS](./media/details-1024x537.png)](./media/details.png)

## <a name="setup"></a>Iestatīšana
Iespējot bezsaistes atbalstu POS ierīces (reģistrs), kas **bezsaistes atbalstu** iespēju **Jā** par **reģistrēties** lapā. Jaunā kanāla datu bāzes uzņēmuma ir izveidota un pievienota veikala kanāla datu grupas. Pēc tam izpildiet visus nepieciešamos sadales grafikus, lai ģenerētu datu pakotnes bezsaistes datu bāzei. Pēc tam instalējiet mazumtirdzniecības mūsdienu POS bezsaistes versiju. Instalācijas process izveido bezsaistes datu bāzi. Turklāt jāinstalē Microsoft SQL Server 2014 Express, ja tas ir nepieciešams. Bezsaistes datu sinhronizēšana sākas pēc pirmās pierakstīšanās sistēmā Retail Modern POS.

## <a name="data-synchronization"></a>Datu sinhronizācija
Lai pamatdatus sūtītu uz bezsaistes datu bāzi, tiek izmantots mazumtirdzniecības plānotājs. Pēc noklusējuma, kad palaižat sadales grafiku, datu izmaiņas tiek sūtītas gan uz kanāla datu bāzi, gan uz bezsaistes datu bāzi. Retail Modern POS ietver asinhronas sinhronizēšanas bibliotēku, kas lejupielādē visas pieejamās datus pakotnes un ievieto tās bezsaistes datu bāzē. Ja kādas transakcijas tiek izveidotas bezsaistē, Retail Modern POS tās augšupielādē uz mazumtirdzniecības serveri, lai tās varētu ievietot kanāla datu bāzē. Bezsaistes datu sinhronizēšana var notikt tikai tad, ja darbojas Retail Modern POS. [![Offline synchronization](./media/offline-sync-1024x521.png)](./media/offline-sync.png)


