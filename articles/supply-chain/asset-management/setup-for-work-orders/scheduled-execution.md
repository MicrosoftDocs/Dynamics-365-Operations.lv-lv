---
title: Plānotā izpilde
description: Šajā rakstā ir paskaidrota plānotā izpilde Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e9d6af5c224f683481378da57708fda3c1b7207
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848054"
---
# <a name="scheduled-execution"></a>Plānotā izpilde

[!include [banner](../../includes/banner.md)]

 

Lai iestatītu plānoto izpildi, varat izmantot darba pasūtījuma pakalpojumu līmeņus. (Plašāku informāciju par darba pasūtījumu pakalpojumu līmeņiem skatiet sadaļā [Pakalpojuma līmenis un apraksts](service-level-and-description.md).) Plānotā izpilde nodrošina elastību darba plānošanā uzturēšanas speciālistiem, jo varat iestatīt detalizētas vai mazāk detalizētas prasības intervālam, kurā darba pasūtījums ir jāpabeidz. Piemēram, uzturēšanas speciālists, kurš pabeidz uzdevumu ātrāk, nekā paredzēts ražošanā, iestāde var pāriet uz citu tuvumā esošu uzdevumu, kas tika ieplānots pašreizējai nedēļai, bet ne obligāti pašreizējai dienai. Šī pieeja ļauj optimizēt darbinieku plānošanu un darbu izpildi.

Plānotās izpildes iestatījums, kas ir saistīts ar darba pasūtījumiem, var būt vispārīgs vai konkrēts. Varat iestatīt vispārīgās rindas, kuras nav ierobežotas konkrētiem darba pasūtījuma tipiem u. tml. Vai arī varat izveidot plānotas izpildes rindas, kas attiecas uz konkrētu darba pasūtījuma tipu, līdzekļu tipu, uzturēšanas darba tipu u. tml.

1. Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Darba pasūtījumi** \> **Plānotā izpilde**.
2. Atlasiet **Jauns**, lai izveidotu plānotās izpildes rindu.
3. Laukos **Funkcionālais novietojums**, **Darba pasūtījuma tips**, **Līdzekļu tips**, **Ražotājs**, **Modelis**, **Uzturēšanas darba tipa kategorija**, **Uzturēšanas darba tips**, **Uzturēšanas darba tipa variants** un **Tirdzniecība** atlasiet nepieciešamās vērtības.
4. Laukā **Pakalpojuma līmenis** atlasiet darba pasūtījuma pakalpojuma līmeni. Ja atstāsiet šo lauku tukšu, būsiet izveidojis ieplānotās izpildes rindas vispārīgāko tipu. Vispārīgās rindas piemēru skatiet pirmajā tālāk norādītās ilustrācijas ierakstā. Šī rinda iespējo visus darba pasūtījumus, kuriem nav darba pasūtījuma pakalpojuma līmeņa, kas jāieplāno konkrētā datumā un laikā.
5. Laukā **Plānotā izpilde** atlasiet laika intervālu.
6. Atlasiet **Saglabāt**.

![Plānotā izpilde.](media/20-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]