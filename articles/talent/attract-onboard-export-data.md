---
title: Datu eksportēšana no programmām Attract un Onboard
description: Datu eksportēšana no Dynamics 365 Talent — Attract un Onboard.
author: andreabichsel
manager: AnnBe
ms.date: 01/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: eb97a16c15476c2f34ec581a32a677fa6fee8739
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461821"
---
# <a name="export-data-from-attract-and-onboard"></a>Datu eksportēšana no programmām Attract un Onboard

[!include [banner](includes/banner.md)]

Kā paziņots [Programmu Dynamics 365 Talent: Attract un Dynamics 365 Talent: Onboard darbība tiek pārtraukta](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps), mēs pārtraucam Dynamics 365 Talent: Attract un Dynamics 365 Talent: Onboard darbību 2022. gada 1 februārī. Lai palīdzētu jums migrēt uz citu, abas programmas tagad nodrošina datu eksporta iespējas.

## <a name="export-data-from-attract"></a>Eksportēt datus no Attract

Jūs varat eksportēt savus datus, neierobežojot piekļuvi savai videi. Iespējams, jūs vēlēsieties to darīt testēšanas nolūkā vai, lai saprastu mūsu datu struktūru. Kad esat gatavs migrēt, ierobežojiet piekļuvi jūsu Attract videi, izmantojot norādījumus pēc šīs procedūras. Noteikti eksportējiet datus vēlreiz. 

1. Dodieties uz [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).

2. Sadaļā **Datu eksports** atlasiet **Pieprasīt datu eksportu**.

   ![[Pieprasīt datu eksportu no Attract](./media/attract-onboard-export-data-attract-request.png)](./media/attract-onboard-export-data-attract-request.png)

3. Kad tiek ziņojuma lodziņš **Jūsu pieprasījums tiek apstrādāts**, atlasiet **Labi**. Datu eksports var ilgt līdz 20 minūtēm atkarībā no jūsu eksporta apjoma.

4. Kad eksports ir pabeigts, atlasiet blakus esošo pogu **Lejupielādēt**. 

   >[!NOTE]
   >Visi datu eksporti ir pieejami septiņas dienas, un tajā brīdī saites **Lejupielādēt** termiņš beidzas.</br>
   
Lejupielāde satur .zip failu ar jūsu Attract datiem, ieskaitot tālāk norādītās mapes.

| Mapes nosaukums | Apraksts |
| --- | --- |
| Administratora iestatījumi | Attract administrēšanas centra konfigurācijas. |
| Kandidāti | Visi kandidāti, kas tika pievienoti darbiem vai talantu kopām. |
| E-pasta veidnes | Visas e-pasta veidnes, kas tika konfigurētas videi. |
| Darba piedāvājuma pakotņu veidnes | Visas izveidotās darba piedāvājumu pakotņu veidnes un ar tām saistītās konfigurācijas. |
| Darba piedāvājuma kārtulu kopas |  Visi kārtulu kopu faili, kas tika augšupielādēti piedāvājuma pārvaldībai. |
| Darba piedāvājuma veidnes | Visas darba piedāvājumu dokumentu veidnes, kas izveidotas videi. |
| Darba piedāvājumi | Visi izveidotie darbi. Dzēstie darbi netiek eksportēti. Apakšmapēs ir iekļauti kandidātu pieteikumi, ar apakšmapēm kandidātu pieteikumu pielikumiem un piedāvājuma pakotnēm, ja piemērojams. |
| Darba piedāvājumu veidnes | Visas darba procesa veidnes, kas tika konfigurētas videi. |
| Kandidātu kopas | Visas izveidotās talantu kopas, to atbalstītāju saraksti un kandidātu saraksti talantu kopām. |
| Nodarbinātie | Saraksts ar visiem darbiniekiem, kuri atrodas vidē, un viņu lomas. |
| (saknes mape) | JSON shēmas fails, kas apraksta datu struktūras laukus. |

### <a name="restrict-access-to-attract"></a>Ierobežot piekļuvi programmai Attract

Kad esat gatavs migrēt, ierobežojiet piekļuvi lietotājiem, kas nav administratori, video Attract un eksportējiet savus datus.

>[!IMPORTANT]
>Piekļuves ierobežošana jūsu Attract videi ir pastāvīga, un to nevar atsaukt. Ja vēlaties, lai lietotāji, kas nav administratori, varētu turpināt piekļūt jūsu videi, izlaidiet šo darbību.

1. Dodieties uz [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).

2. Lai ierobežotu lietotāju, kas nav administratori, piekļuvi jūsu Attract videi, sadaļā **Ierobežot piekļuvi šai programmai** atlasiet **Ierobežot piekļuvi tagad**. Piekļuves ierobežošana arī atgrāmato visus aktīvos darbus, kas ir grāmatoti.

   ![[Ierobežot lietotāju, kas nav administratori, piekļuvi programmai Attract](./media/attract-onboard-export-data-attract-restrict-access.png)](./media/attract-onboard-export-data-attract-restrict-access.png)

3. Kad redzat brīdinājumu, **Šīs izmaiņas ir paliekošas**, atlasiet **Ierobežot piekļuvi**, lai pastāvīgi ierobežotu lietotājus, kas nav administratori, no šīs vides. Ja neesat gatavs pabeigt šo darbību, atlasiet **Atcelt**.

   ![[Brīdinājums, ka piekļuves ierobežošana ir neatgriezeniskas izmaiņas](./media/attract-onboard-export-data-attract-warning.png)](./media/attract-onboard-export-data-attract-warning.png)

   >[!NOTE]
   >Administratori var turpināt piekļūt datu eksporta un personas pārskata lapām pēc tam, kad jūs ierobežojat piekļuvi Attract videi.

## <a name="export-data-from-onboard"></a>Eksportēt datus no Onboard

Kad esat gatavs, varat lejupielādēt veidnes, ceļvežus un kandidātu datus no Onboard.

1. Dodieties uz [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).

2. Sadaļā **Datu eksports** atlasiet **Pieprasīt datu eksportu**. 

   ![[Pieprasīt datu eksportu no Onboard](./media/attract-onboard-export-data-onboard-request.png)](./media/attract-onboard-export-data-onboard-request.png)

3. Kad tiek ziņojuma lodziņš **Jūsu pieprasījums tiek apstrādāts**, atlasiet **Labi**. Datu eksports var ilgt līdz 20 minūtēm atkarībā no jūsu eksporta apjoma.

4. Kad eksports ir pabeigts, atlasiet blakus esošo pogu **Lejupielādēt**. 

   ![[Lejupielādēt datu eksportu no Onboard](./media/attract-onboard-export-data-onboard-download.png)](./media/attract-onboard-export-data-onboard-download.png)

   >[!NOTE]
   >Jūsu datu eksports ir pieejams septiņas dienas. Pēc septiņām dienām saites **Lejupielādēt** termiņš beidzas, un jums ir jāpieprasa jauns eksports, ja nepieciešams atkārtoti lejupielādēt datus. Kad sākat jaunu datu eksportu, visām esošajām lejupielādēm derīguma termiņš beigsies pēc jaunās eksportēšanas veiksmīgas darbības.

Lejupielāde ir.zip fails, kas satur tālāk norādīto.

- **Veidņu** mape, kas ietver jūsu Onboard veidnes Word dokumenta formātā.

- **Ceļvežu** mape, kas ietver jūsu Onboard ceļvežus Word dokumenta formātā.

## <a name="see-also"></a>Skatiet arī

[Programmu Dynamics 365 Talent: Attract un Dynamics 365 Talent: Onboard darbības pārtraukšana](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)

[!INCLUDE[footer-include](../includes/footer-banner.md)]