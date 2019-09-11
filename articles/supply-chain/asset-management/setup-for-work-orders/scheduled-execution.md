---
title: Plānotā izpilde
description: Šajā tēmā ir aprakstīta plānotā izpilde Līdzekļu pārvaldībā.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8d9c8afc139c96e32efb3161d35fde685b8abcc5
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874674"
---
# <a name="scheduled-execution"></a>Plānotā izpilde

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Lai iestatītu plānoto izpildi, varat izmantot darba pasūtījuma pakalpojumu līmeņus. (Plašāku informāciju par darba pasūtījumu pakalpojumu līmeņiem skatiet sadaļā [Pakalpojuma līmenis un apraksts](service-level-and-description.md).) Plānotā izpilde nodrošina elastību darba plānošanā uzturēšanas speciālistiem, jo varat iestatīt detalizētas vai mazāk detalizētas prasības intervālam, kurā darba pasūtījums ir jāpabeidz. Piemēram, uzturēšanas speciālists, kurš pabeidz uzdevumu ātrāk, nekā paredzēts ražošanā, iestāde var pāriet uz citu tuvumā esošu uzdevumu, kas tika ieplānots pašreizējai nedēļai, bet ne obligāti pašreizējai dienai. Šī pieeja ļauj optimizēt darbinieku plānošanu un darbu izpildi.

Plānotās izpildes iestatījums, kas ir saistīts ar darba pasūtījumiem, var būt vispārīgs vai konkrēts. Varat iestatīt vispārīgās rindas, kuras nav ierobežotas konkrētiem darba pasūtījuma tipiem u. tml. Vai arī varat izveidot plānotas izpildes rindas, kas attiecas uz konkrētu darba pasūtījuma tipu, līdzekļu tipu, uzturēšanas darba tipu u. tml.

1. Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Darba pasūtījumi** \> **Plānotā izpilde**.
2. Atlasiet **Jauns**, lai izveidotu plānotās izpildes rindu.
3. Laukos **Funkcionālais novietojums**, **Darba pasūtījuma tips**, **Līdzekļu tips**, **Ražotājs**, **Modelis**, **Uzturēšanas darba tipa kategorija**, **Uzturēšanas darba tips**, **Uzturēšanas darba tipa variants** un **Tirdzniecība** atlasiet nepieciešamās vērtības.
4. Laukā **Pakalpojuma līmenis** atlasiet darba pasūtījuma pakalpojuma līmeni. Ja atstāsiet šo lauku tukšu, būsiet izveidojis ieplānotās izpildes rindas vispārīgāko tipu. Vispārīgās rindas piemēru skatiet pirmajā tālāk norādītās ilustrācijas ierakstā. Šī rinda iespējo visus darba pasūtījumus, kuriem nav darba pasūtījuma pakalpojuma līmeņa, kas jāieplāno konkrētā datumā un laikā.
5. Laukā **Plānotā izpilde** atlasiet laika intervālu.
6. Atlasiet **Saglabāt**.

![1. attēls](media/20-setup-for-work-orders.png)
