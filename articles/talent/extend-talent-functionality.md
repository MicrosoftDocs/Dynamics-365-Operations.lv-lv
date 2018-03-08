---
title: "Microsoft Dynamics 365 for Talent funkcionalitātes paplašināšana"
description: "Ja esat izveidojis kādas Microsoft PowerApps programmas, šīs programmas varat palaist no saitēm programmatūrā Microsoft Dynamics 365 for Talent."
author: rschloma
manager: AnnBe
ms.date: 11/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-28
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: cfd3b475b113fdab4ceeb3e636fea6c9134ab982
ms.openlocfilehash: 0ab829803634871c9060daa381bd02d7d2bbdf42
ms.contentlocale: lv-lv
ms.lasthandoff: 12/01/2017

---
# <a name="extend-the-functionality-of-microsoft-dynamics-365-for-talent"></a>Microsoft Dynamics 365 for Talent funkcionalitātes paplašināšana

[!include[banner](includes/banner.md)]

Ja esat izveidojis kādas Microsoft PowerApps programmas, šīs programmas varat palaist no saitēm programmatūrā Microsoft Dynamics 365 for Talent. Lai iestatītu piekļuvi savām programmām, ir jāiestata noteikta informācija sadaļā Talent, kas atrodas konfigurācijas lapā, kuru varat atvērt no darbvietas **Sistēmas administrēšana**.

## <a name="configuring-embedded-powerapps-within-talent"></a>Iegulto PowerApps programmu konfigurēšana Talent ietvaros
Lai Talent lapas konfigurētu PowerApps programmu palaišanai, izmantojiet lapu **Iestatīt iegultas Microsoft PowerApps programmas**. Lai atvērtu lapu **Iestatīt iegultas Microsoft PowerApps programmas**, atveriet darbvietu **Sistēmas administrēšana** un pēc tam atveriet cilni **Saites**. Grupā **Iestatīšana** atlasiet **Microsoft PowerApps**. 

Šajā lapā tiek ievadīta vai iestatīta tālāk norādītā informācija. 

> - Katras PowerApps programmas aprakstošs nosaukums vai identifikators.
> - Unikāls identifikators (GUID) katrai programmai, kuru pievienojat lapai Talent. Šis programmas ID ir pieejams PowerApps vietnē [powerapps.com](http://powerapps.com/). 
> - Lapa, no kuras lietotāji var atvērt kādu programmu vai pārskatu. Ne visas Talent lapas atbalsta iegultās PowerApps programmas un Power BI pārskatus. 

 > [!NOTE]
 >  Ievadiet lapas iekšējo nosaukumu, nevis parādāmo nosaukumu, kurš ir redzams lapas augšdaļā. Lai atrastu iekšējo nosaukumu, atveriet lapu, kuras iekšējais nosaukums jums ir nepieciešams, un ar peles labo pogu noklikšķiniet jebkurā šīs lapas vietā. Kad tiek atvērta izvēlne, virziet peles rādītāju virs vienuma **Formas informācija**. Iekšējais formas nosaukums izvēlnē tiek rādīts blakus vienumam **Formas informācija**.
 
> - Norādiet formas vadīklu, no kuras programma var izgūt konteksta datus. Piemēram, programma varētu izmantot datus par kādu nodarbināto. Ja laukā **Konteksts** ievadāt lapu **Nodarbinātais**, startējot programmu, tiek atvērta lapa **Nodarbinātais**. Ieraksts laukā **Konteksts** nav obligāts. 
> - Iestatiet lielumu dialoglodziņam, kurā darbosies PowerApps programmas. Dialoglodziņa rūtiņas ir norādītas kā “mazs” vai “liels”, lai optimizētu lietotāja interfeisu, kad jūsu programma attiecīgi darbojas tālruni vai lielākā ierīcē. 

Varat arī norādīt, kurām juridiskajām personām programma būs pieejama, vai varat to padarīt pieejamu visām savām juridiskajām personām. Pēc noklusējuma jūsu PowerApps programmas ir pieejamas visām juridiskajām personām.

## <a name="opening-an-application"></a>Programmas atvēršana
Kad esat konfigurējis iegultās PowerApps programmas, Talent lapās tiek pievienotas saites uz jūsu norādītajām programmām. Noklikšķiniet uz saites, lai atvērtu programmu. 



