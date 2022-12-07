---
title: Personīgās saziņas piemērotības opciju konfigurēšana
description: Šajā rakstā ir izskaidrots, kā konfigurēt piemērotības opcijas personiskajiem kontaktiem programmā Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e3e393002901f31c035a54bd8036ed20ecdf9e00
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/23/2022
ms.locfileid: "9803889"
---
# <a name="configure-personal-contact-eligibility-options"></a>Personīgās saziņas piemērotības opciju konfigurēšana


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā rakstā ir izskaidrots, kā konfigurēt personisko kontaktpersonu tipus, ko var izmantot Microsoft atvieglojumiem Dynamics 365 Human Resources. Personiskās kontaktpersonas ir personas, kas tiks iekļautas jūsu plānos (apgādājamie) vai kuras saņems jūsu plānus (saņēmēji). Parasti apgādājamie ir dzīvesbiedri vai bērni. Saņēmēji var būt laulātie, bērni, tresti vai vecāki.

1. Darbvietā **Atvieglojumu pārvaldība** sadaļā **Iestatīt** atlasiet **Personisko kontaktpersonu piemērotības opcijas**.

2. Atlasiet **Jauns**.

3. Norādiet vērtības tālāk minētajos laukos.

   | Lauks | Apraksts |
   | --- | --- |
   | **Piemērojamības opcija** | Unikāls piemērotības opcijas nosaukums vai kods, lai identificētu piemērotības opciju. |
   | **Apraksts** | Īss piemērotības opcijas apraksts. |
   | **Kontaktpersonas piemērojamības kods** | Sistēmas kods, kas vislabāk raksturo personiskās piemērojamības opciju. Var izvēlēties kādu no zemāk minētajiem. <ul><li>Attiecības</li><li>Students</li><li>Pārsnieguma pakārtotais</li><li>Gados vecs pakārtotais ar invaliditāti</li></ul> |
   | **Statuss** | Piemērotības opcijas statuss. Ja piemērotības opcijas statuss ir iestatīts kā neaktīvs, nevar atlasīt personisko kontaktpersonu piemērotības opciju. |
   | **Attiecības** | Norāda attiecības starp personisko kontaktpersonu un darbinieku. Šis lauks ir aktīvs tikai tad, ja kontaktpersonas piemērotības kods ir iestatīts uz Attiecības. |
   | **Vecums** |Norāda atvieglojumu plānam atbilstīgās personiskās kontaktpersonas maksimālo vecumu. Šis lauks ir aktīvs tikai tad, ja atlasāt attiecības. Šis vecums tiek salīdzināts ar personiskās kontaktpersonas aprēķināto vecumu. Aprēķinātais vecums ir: (seguma datums — personiskās kontaktpersonas dzimšanas datums / 365). Tas vienmēr ir vesels skaitlis.
No **pārkaru atkarīgām** personas kontaktinformācijas iespējām, šajā laukā vecums ir minimālais vecums. Piemēram, ja pēc vecuma opcijas Pārmakums ir iestatīts uz **18**, tad apgādājamajiem, kas atzīmēti kā apgādājami par pārkaru un ir 18 vai vecāki, piemērotības opcija tiks segta.  |

4. Atlasiet **Saglabāt**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
