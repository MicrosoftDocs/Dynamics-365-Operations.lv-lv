---
title: Kvalitātes pārvaldības testi
description: Šajā tēmā ir aprakstīts, kā izveidot testus, ko var izmantot kvalitātes pārbaudes pasūtījumiem Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62e5aca8c41aa324802e83e53f52ea39b623a65882962413e743e6dd2671a901
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781042"
---
# <a name="quality-management-tests"></a>Kvalitātes pārvaldības testi

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā izveidot testus, ko var izmantot kvalitātes pārbaudes pasūtījumiem Microsoft Dynamics 365 Supply Chain Management.

Lapu **Testi** izmantojiet, lai definētu un skatītu atsevišķus testus, kas nosaka, vai produkti atbilst kvalitātes specifikācijām. Vienu vai vairākus atsevišķus testus varat piešķirt testu grupai. Šajā gadījumā jums ir jānorāda arī testa specifiskā informācija, piemēram, pieņemamās mērījumu vērtības. Mērījuma vērtības tiek izmantotas kvantitatīvajiem testiem. Kvalitatīvajiem testiem tiek izmantoti testa mainīgie.

- Kvantitatīviem testiem lauks **Veids** ir iestatīts uz *Vesels skaitlis* vai *Daļskaitlis*. Ir norādīta arī mērvienība. Kvalitātes specifikācijas un testa rezultāti tiek izteikti kā skaitļi.
- Kvalitatīvajiem testiem lauks **Veids** ir iestatīts uz *Opcija*. Kvalitatīvajiem testiem ir nepieciešama papildinformācija par testa mainīgo, kas tiek mērīts, un tā uzskaitīšanas iespējam. Kvalitātes specifikācijas un testa rezultāti tiek izteikti atbilstoši rezultātam.

Testam var piešķirt arī pārbaudes instrumentu. Tomēr, testa instrumenti nav nepieciešami, lai izveidotu un izmantotu testus ar kvalitātes pasūtījumiem. Papildinformāciju skatiet [Kvalitātes pārvaldības testa instrumenti](quality-test-instruments.md).

Pēc izvēles var arī norādīt testa vienību, lai norādītu mērvienību, kādā tiek ierakstīti testa rezultāti. Piemēram, temperatūras tests var ietvert Fahrenheita vai Celsija grādu vienību.

## <a name="example-of-a-test"></a>Testa piemērs

Ražošanas uzņēmums iepirktajam materiālam veic divus testus: kvantitatīvo testu materiāla kvalitātei un kvalitatīvo testu iepakojuma bojājumam. Uzņēmums norāda papildu informāciju par kvalitātes testu, lai definētu testa mainīgo (piemēram, bojāto iepakojumu) un tā rezultātus. Uzņēmums izmanto lapu **Testu grupas**, lai abus testus piešķirtu testu grupai un norādītu testa specifisko informāciju. Kvalitātes pasūtījumam tiek piešķirta testa grupā, tādējādi uzņēmums var ziņot testa rezultātus par diviem testiem.

## <a name="create-a-test"></a>Testa izveide

Lai izveidotu testu, rīkojieties šādi.

1. Dodieties uz **Krājumu pārvaldība \> Iestatīšana \> Kvalitātes kontrole \> Testi**.
1. Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**. Jaunajā rindā iestatiet šādus laukus:

    - **Tests** – ievadiet unikālu ID vai nosaukumu testam.
    - **Apraksts** — ievadiet testa detālizēto aprakstu.
    - **Veids** – atlasiet testa rezultātu veidu. Kvantitatīviem testiem atlasiet *Daļskaitlis* vai *Vesels skaitlis*. Kvalitatīvajiem testiem atlasiet *Opciju*.
    - **Testa instruments** – atlasiet [testa instrumentu](quality-test-instruments.md), kas jāizmanto testam.
    - **Vienība** – ja jūs atlasījāt *Daļskaitlis* vai *Vesels skaitlis* laukā **Veids** (t.i., ja tests ir kvantitātes tests), atlasiet mērvienību, kurā jāieraksta testa rezultāti.

1. Aizvērt lapu.

> [!NOTE]
> Pēc testa saglabāšanas režģī vairs nevar rediģēt lauku **Veids**. Ja jāmaina testa rezultātu veids, kas tiks ierakstīts testam, darbību rūtī atlasiet **Mainīt kvalitātes testa veidu**. Dialoglodziņā iestatiet lauku Jauns tips **Mainīt kvalitātes testa veidu** iestatiet lauku **Jauns veids** uz vajadzīgo veidu un pēc tam atlasiet **Labi**, lai aizvērtu dialoglodziņu.

## <a name="additional-resources"></a>Papildu resursi

- [Kvalitātes pārvaldības testa instrumenti](quality-test-instruments.md)
- [Kvalitātes pārvaldības testa grupas](quality-test-groups.md)
- [Kvalitātes pārvaldības testa mainīgie](quality-test-variables.md)
- [Kvalitātes piesaistes](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
