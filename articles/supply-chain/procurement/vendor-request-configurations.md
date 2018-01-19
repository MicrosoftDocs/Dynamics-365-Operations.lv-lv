---
title: "Piegādātāja pieprasījuma konfigurācijas"
description: "Šajā tēmā ir aprakstīti lauki, kuri jaunā piegādātāja pieprasījumā ir jāaizpilda obligāti."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 0ca19ab9ed7a52328c5dd5252c418bb9343bdc2b
ms.openlocfilehash: e45f8698e69a2a870c7c00f91622216deb4cb38a
ms.contentlocale: lv-lv
ms.lasthandoff: 12/14/2017

---

# <a name="vendor-request-configurations"></a>Piegādātāja pieprasījuma konfigurācijas
[!include[banner](../includes/banner.md)]

Lai izpildītu piegādātāja pieprasījumu, piegādātāja kontaktpersonai ir jāizpilda potenciālā piegādātāja reģistrēšanas vednis.

Formā **Piegādātāja pieprasījuma konfigurācijas** varat izveidot profilus, kas potenciālā piegādātāja reģistrācijas vednī norāda obligātos laukus un redzamos laukus.

Kreditora reģistrācijas vednis sākas, jautājot potenciālā piegādātāja lietotājam par valsti/reģionu, kurā piegādātājs darbojas. Šī informācija nosaka piemērojamo konfigurāciju. Ja kādai valstij/reģionam nav definēta īpaša konfigurācija, tiek izmantota noklusējuma konfigurācija.

### <a name="set-up-a-vendor-request-configuration"></a>Piegādātāja pieprasījuma konfigurācijas iestatīšana

Kreditora konfigurācija pēc noklusējuma ir pieejama formā “Kreditora pieprasījuma konfigurācija”.

Noklusējuma konfigurācijai nav iespējams atlasīt valsti/reģionus, tādēļ sadaļu **Valstis/reģioni** nevar mainīt.

1.  Noklikšķiniet uz **Sagāde un avoti** > **Iestatīšana** > **Kreditori** un pēc tam noklikšķiniet uz **Piegādātāja pieprasījuma konfigurācijas**.
2.  Noklikšķiniet uz cilnes **Lauki**, lai iestatītu uzskaitīto lauku statusu.
-   Slēpts (nav redzams)
-   Parādīts (redzams, bet nav obligāts)
-   Obligāts (redzams un obligāts)
3.  Noklikšķiniet uz cilnes **Saturs**, lai norādītu, vai teksts būs redzams vednī un vai ir nepieciešams apliecinājums, ka potenciālā piegādātāja lietotājam ir jāsniedz piekrišana par šo, pirms notiek pāriešana uz nākamo vedņa posmu. Apstiprinājums tiks pieprasīts par visiem noteikumiem un nosacījumiem, kas lietotājam ir jāpieņem, lai varētu turpināt.

Varat arī ievadīt apstiprinājuma ziņojumu, kas tiek parādīts, kad vednis ir pabeigts, un varat pievienot vienu vai vairākas anketas.

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a>Piegādātāja konfigurācijas izveidošana noteiktai valstij/reģionam
1.  Noklikšķiniet uz **Sagāde un avoti** > **Iestatīšana** > **Kreditori** un pēc tam noklikšķiniet uz **Piegādātāja pieprasījuma konfigurācijas**.
2.  Noklikšķiniet uz **Jauns**, lai izveidotu jaunu konfigurāciju, un norādiet šīs konfigurācijas nosaukumu.
3.  Noklikšķiniet uz **Saglabāt**.
4.  Atveriet cilni **Valsts/reģioni**, lai atlasītu valsti/reģionu, kuriem šī konfigurācija ir jāizmanto.
5.  Pabeidziet konfigurēšanu, ievērojot vadlīnijas par noklusējuma konfigurāciju.


