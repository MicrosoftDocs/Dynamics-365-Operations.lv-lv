---
title: Teksta bloka modulis
description: Šajā tēmā aplūkoti Text block moduļi un aprakstīta to pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 9068c35eaeee68f97d81d168983d7281da09491cb0afd70cb8196010ce771b0d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723315"
---
# <a name="text-block-module"></a>Teksta bloka modulis

[!include [banner](includes/banner.md)]

Šajā tēmā aplūkoti Text block moduļi un aprakstīta to pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.

Teksta bloka modulis ir modulis, kas tiek izmantots teksta satura pievienošanai. Tas var būt gan informatīvs, gan reklāmas saturs.

Teksta bloka moduļus vada dati no Satura pārvaldības sistēmas (CMS), un tos var ievietot jebkurā lapā. Tas ir savrups moduļi, kas nav atkarīgi no lapas konteksta vai jebkādiem citiem moduļiem.

## <a name="examples-of-text-block-modules-in-e-commerce"></a>Teksta bloka moduļu piemēri pakalpojumā e-Commerce

Teksta bloka moduļus var izmantot šādi.

* Lai preces informācijas lapā rādītu preces līdzekļus.
* Informācijas nolūkiem jebkurā lapā. Piemēram, tie var izskaidrot lojalitātes programmu priekšrocības, aprakstīt nosūtīšanas un atgriešanas politiku, atbildēt uz bieži uzdotajiem jautājumiem vai nodrošināt saturu "par mums".
* Pievienot pielāgotus ziņojumus preces informācijas lapā. (piemēram, “brīva piegāde pasūtījumiem virs 50 $”).
* Atrunām un kontaktinformācijai par preču detalizētas informācijas lapām, groza lapām, izrakstīšanās lapām un citām lapām (piemēram, “Piegāde un atgriešana saskaņā ar veikala politikām”).

Attēlā zemāk redzams piemērs teksta bloka modulim, kas tiek izmantots sākumlapā.

![Teksta bloka moduļa piemērs.](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a>Teksta bloka moduļa rekvizīti

| Rekvizīta nosaukums     | Vērtība                                            | Apraksts |
|-------------------|--------------------------------------------------|-------------|
| Bagātināts teksts         | Bagātināts teksts                                        | Rindkopas teksts. Tiek atbalstītas dažas pamata bagātināta teksta iespējas, piemēram, treknraksts, pasvītrots un slīpraksta teksts. |
| Pielāgotās klases nosaukums | Kaskadētās stila lapas (CSS) klases nosaukums        | Tās pielāgotās CSS klases nosaukums, ko izstrādātājs sniedz, lai formatētu šo moduli. Klases nosaukumam ir jābūt definētam dizaina pakotnē. |
| Fontu lielums         | **Mazs**, **Vidējs**, **Liels** vai **X-liels** | Satura fonta lielums. |

## <a name="add-a-text-block-module-to-a-page"></a>Teksta bloka moduļa pievienošana lapā

Lai pievienotu teksta bloka moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.

1. Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu jaunu veidni.
1. Dialoglodziņā **Jauna veidne** zem **Veidnes nosaukums** ievadiet **Satura veidne**.
1. Slotā **Pamatteksts** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Noklusējuma lapa** un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Dodieties uz **Lapas** un atlasiet **Jauns**, lai izveidotu jaunu lapu.
1. Dialoglodziņā **Izvēlēties veidni** atlasiet **Satura veidne**. Sadaļā **Lapas nosaukums** ievadiet **Satura lapa** pēc tam atlasiet **Labi**.
1. Jaunās lapas slotā **Galvenais** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Konteiners** un pēc tam atlasiet **Labi**.
1. Konteinera moduļa rekvizītu rūtī iestatiet rekvizītu **Platums** uz **Aizpildīt konteineru**.
1. Slotā **Konteiners** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Teksta bloks** un pēc tam atlasiet **Labi**. 
1. Teksta bloka moduļa rekvizītu rūtī pievienojiet tekstu laukā **Bagātinātais teksts**.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Akcijas reklāmkaroga modulis](add-alert.md)

[Karuseļa modulis](add-carousel.md)

[Satura bloka modulis](add-hero-module.md)

[Video atskaņotāja modulis](add-video-player.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]