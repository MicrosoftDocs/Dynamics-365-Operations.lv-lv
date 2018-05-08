---
title: "Microsoft Project klienta integrācija"
description: "Projekta grafika plānošana un uzturēšana var būt sarežģīta, tādēļ projektu vadītājiem jāizmanto rīki, kas palīdz pārvaldīt šo uzdevumu. Integrācija ar Microsoft Project klientu nodrošina atbalstu projekta darba sadalījuma struktūras atvēršanai un pārvaldībai."
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 4a3445417d5ae88e2ff3676962a82921a7ab475d
ms.contentlocale: lv-lv
ms.lasthandoff: 03/26/2018

---

# <a name="microsoft-project-client-integration"></a>Microsoft Project klienta integrācija

[!include [banner](../includes/banner.md)]

Projekta grafika plānošana un uzturēšana var būt sarežģīta, tādēļ projektu vadītājiem jāizmanto rīki, kas palīdz pārvaldīt šo uzdevumu. Integrācija ar Microsoft Project klientu nodrošina atbalstu projekta darba sadalījuma struktūras atvēršanai un pārvaldībai. Projektu vadītājs var publicēt visas izmaiņas Finance and Operations projekta darba sadalījuma struktūrā.

> [!NOTE]
> Ja izmantojat Microsoft Dynamics 365 for Finance and Operations jūlija atjauninājumu, jums ir jāinstalē KB 4054797 un 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>Microsoft Project klienta pievienojumprogrammas konfigurēšana
Lai iespējotu integrāciju ar Microsoft Project klientu, lietotāja klienta Microsoft Project programmā ir jāinstalē Microsoft Dynamics 365 pievienojumprogramma. To var izdarīt, atverot darbvietu **Projektu pārvaldība**.

•   Darbvietas sadaļā **Saites** > **Iestatīšana** noklikšķiniet uz **Konfigurēt projekta klienta pievienojumprogrammu**.

•   Noklikšķiniet uz **Atvērt**, un, kad tiek parādīta attiecīgā uzvedne, noklikšķiniet uz **Palaist**.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Esošas melnraksta darba sadalījuma struktūras atvēršana un rediģēšana Microsoft Project klientā
Ja projektam programmā Finance and Operations jau ir izveidota darba sadalījuma struktūra, šo darba sadalījuma struktūru var atvērt Microsoft Project klienta lietojumprogrammā, ja darba sadalījuma struktūrai ir melnraksta statuss. Lai atvērtu no lapas **Projekts**, cilnē **Plāns** noklikšķiniet uz saites **Atvērt programmā Microsoft Project**. Šo lapu var arī atvērt no Microsoft Project klienta lietojumprogrammas, cilnē **Microsoft Dynamics 365** noklikšķinot uz **Atvērt**. Sarakstā atlasiet vienumus **Juridiska persona** un **Projekts**.

> [!NOTE]
> Ja izmantojat pārlūkprogrammu Internet Explorer, jums jānoklikšķina uz **Saglabāt**, lai manuāli atvērtu no vietas, kurā fails ir lejupielādēts. Vai arī noklikšķiniet uz **Saglabāt un atvērt**, lai failu atvērtu Microsoft Project klientā. Saglabājot failu, nepārdēvējiet to.

Pirms veicat jebkādu rediģēšanu failā, izmantojot Microsoft Project klientu, jums tas ir jāpaņem. Cilnē **Microsoft Dynamics 365** noklikšķiniet uz **Paņemt**. Tādējādi citi lietotāji nevarēs vienlaikus rediģēt darba sadalījuma struktūru no programmas Finance and Operations. Lai darba sadalījuma struktūru publicētu pēc rediģēšanas pabeigšanas, cilnē **Microsoft Dynamics 365** noklikšķiniet uz **Atdot**.

Ja projekta grupa jau ir pievienota projektam programmā Finance and Operations, resursu saraksts tiks aizpildīts ar grupas dalībniekiem. Ja projekta grupa vēl nav pievienota projektam, varat atlasīt resursus un izveidot grupu Microsoft Project klientā, cilnē **Microsoft Dynamics 365** noklikšķinot uz pogas **Resursi**. 

Ar programmu Finance and Operations kā daļa no atdošanas procesa tiks sinhronizēti tālāk norādītie dati.

•   Uzdevuma nosaukums

•   Sākuma datums

•   Beigu datums

•   Pirmstecīgas aktivitātes

•   Resursu nosaukumi

•   Kategorija

•   Resursu kategorija

•   Darba stundas

•   Piezīmes

•   Prioritāte

> [!NOTE]
> Ja savam Microsoft Project klienta failam pievienosit jebkuras citas kolonnas, tās netiks saglabātas failā un netiks parādītas pēc atkārtotas faila atvēršanas.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Darba sadalījuma struktūras izveide esošam projektam, izmantojot Microsoft Project klientu
Lai izveidotu jaunu darba sadalījuma struktūru, izmantojot Microsoft Project klientu, veiciet tālāk norādītās darbības.


1.  Atveriet Microsoft Project klientu.

2.  Cilnē **Microsoft Dynamics 365** noklikšķiniet uz **Atvērt**.

3.  Projektam atlasiet vienumu **Juridiska persona**.

4.  Atlasiet vienumu **Projekts**.

5.  Cilnē **Microsoft Dynamics 365** noklikšķiniet uz **Paņemt**.

6.  Kad fails ir gatavs publicēšanai programmā Finance and Operations, cilnē **Microsoft Dynamics 365** noklikšķiniet uz **Atdot**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Esošas darba sadalījuma struktūras aizstāšana esošam projektam, izmantojot Microsoft Project klientu
Lai izveidotu jaunu darba sadalījuma struktūru, izmantojot Microsoft Project klientu, un aizstātu esošu darba sadalījuma struktūru esošam projektam, veiciet tālāk norādītās darbības.

1.  Atveriet Microsoft Project klientu.

2.  Izveidojiet grafiku Microsoft Project klientā.

3.  Cilnē **Microsoft Dynamics 365** noklikšķiniet uz vienumiem **Saglabāt izmaiņas** > **Aizstāt esošu projektu**.

4.  Projektam atlasiet vienumu **Juridiska persona**.

5.  Atlasiet vienumu **Projekts**.

6.  Noklikšķiniet uz **Labi**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Jauna projekta izveide no Microsoft Project klienta


1.  Atveriet Microsoft Project klientu.

2.  Izveidojiet grafiku Microsoft Project klientā.

3.  Cilnē **Microsoft Dynamics 365** noklikšķiniet uz vienumiem **Saglabāt izmaiņas** > **Saglabāt jaunā projektā**.

4.  Projektam atlasiet vienumu **Juridiska persona**.

5.  Ievadiet **Projekta ID**, ja nepieciešams.

6.  Ievadiet vienumu **Projekta nosaukums**.

7.  Atlasiet vienumus **Projekta tips**, **Projektu grupa** un **Projekta līguma ID**. Vai arī varat izveidot jaunu projekta līgumu, noklikšķinot uz **Jauns**.

8.  Atlasiet vienumu **Kalendārs**, ko izmantot resursiem.

11. Noklikšķiniet uz **Labi**.

