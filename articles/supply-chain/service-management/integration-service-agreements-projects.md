---
title: Integrācija pakalpojumu līgumiem un projektiem
description: Kad jūs strādājat ar pakalpojumu līgumiem un pakalpojumu līgumu rindām, jūs lietojat datus, kas ir iestatīti sadaļas Projektu pārvaldība un uzskaite apgabalos.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9a19a138cceb7db08216e1151eb92442691bc58d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202334"
---
# <a name="integration-for-service-agreements-and-projects"></a>Integrācija pakalpojumu līgumiem un projektiem 

[!include [banner](../includes/banner.md)]


Kad jūs strādājat ar pakalpojumu līgumiem un pakalpojumu līgumu rindām, jūs lietojat datus, kas ir iestatīti sadaļas **Projektu pārvaldība un uzskaite** apgabalos.

## <a name="project-prices"></a>Projekta cenas

Pakalpojuma līguma darbības izmaksas un pārdošanas cena izriet no izmaksu cenu iestatījumiem, kas attiecas uz pakalpojuma līgumam pievienoto projektu. Izmaksu un pārdošanas cenas var tikt iestatītas projektam, darbiniekam un kategorijai. 

## <a name="project-validation"></a>Projekta pārbaude

Pakalpojuma līguma rindā atlasei pieejamie projekti, darbinieki un kategorijas var tikt ierobežoti ar apstiprināšanas iestatījumu palīdzību sadaļā **Projektu pārvaldība un uzskaite**. Izmantojot apstiprināšanas iestatījumus, varat kombinēt darbiniekus, projektus un kategorijas piekļuves kontrolei. 

## <a name="project-line-properties"></a>Projekta rindas statuss

Pakalpojuma līguma rindai rindas statuss tiek ievadīts automātiski.

Rindas rekvizīti tiek izveidoti veidlapā **Rindas rekvizīti**, sadaļā **Projektu pārvaldība un uzskaite**. Rindas rekvizīts, kas ir ievadīts pakalpojumu līgumā, ir pievienots pakalpojumu līgumam atlasītajam projektam, un to manto pakalpojumu līguma rinda. 

## <a name="default-offset-accounts"></a>Noklusētie korespondējošie konti

Ja jūs ievadīsit izmaksu darbību, attiecīgajai darbībai automātiski tiek atlasīts noklusētais korespondējošais konts. Noklusētais izdevumu konts tiek iestatīts projektam, kas piesaistīts pašreizējam pakalpojumu līgumam.

## <a name="project-categories"></a>Projektu kategorijas

Pakalpojumu līgumu rindām pieejamās kategorijas ir iestatītas veidlapā **Projektu kategorijas**, kas atrodas sadaļā **Projektu pārvaldība un uzskaite**. 

> [!NOTE]
> <P>Kategorijas, kurām ir atzīmēta izvēles rūtiņa <STRONG>Aktīvs žurnālos</STRONG> veidlapas <STRONG>Projektu kategorijas</STRONG> cilnē <STRONG>Projekts</STRONG>, ir pieejamas atlasei. Tomēr, ja ir atlasīta izvēles rūtiņa <STRONG>Neaktīvās kategorijas</STRONG> veidlapas <STRONG>Projektu vadības un uzskaites parametri</STRONG> cilnē <STRONG>Žurnāli</STRONG>, visas kategorijas ir pieejamas atlasei.</P>

## <a name="project-parameters"></a>Projektu parametri

Ja ir atlasīts lauks **Nodarbinātie, ar kuriem ir pārtrauktas darba attiecības** veidlapas **Projektu vadības un uzskaites parametri** cilnē **Žurnāli**, jūs varat atlasīt neaktīvos darbiniekus papildus aktīvajiem darbiniekiem veidlapās **Pakalpojumu līgumi** un **Pakalpojumu pasūtījumi**.

Jūs varat arī iespējot laukus **Sākuma laiks** un **Beigu laiks** veidlapas **Pakalpojumu pasūtījumi** cilnē **Projekts**, lai ievadītu sākuma un beigu laikus pakalpojumu pasūtījumu rindās.

## <a name="enable-the-starting-and-ending-time-feature-for-service-orders"></a>Sākuma un beigu laika iespējas iespējošana pakalpojumu pasūtījumiem

1.  Noklikšķiniet uz **Projektu vadība un uzskaite** \> **Iestatīšana** \> **Projektu vadības un uzskaites parametri**.

2.  Noklikšķiniet uz cilnes **Žurnāli** un pēc tam atzīmējiet izvēles rūtiņu **Parādīt sākuma/beigu laikus**.

3.  Noklikšķiniet uz **Projektu pārvaldība un uzskaite** \> **Iestatījumi** \> **Žurnāli** \> **Žurnālu nosaukumi**.

4.  Atlasiet pakalpojuma pasūtījumam pievienotā žurnāla nosaukumu.

5.  Noklikšķiniet uz cilnes **Vispārīgi** un pēc tam atzīmējiet izvēles rūtiņu **Parādīt sākuma/beigu laikus**.


> [!NOTE]
> <P>Atlasiet žurnāla nosaukumu pakalpojumu pasūtījumam laukā <STRONG>Stunda</STRONG> veidlapas <STRONG>Pakalpojumu pārvaldības parametri</STRONG> cilnē <STRONG>Žurnāli</STRONG>.</P>





