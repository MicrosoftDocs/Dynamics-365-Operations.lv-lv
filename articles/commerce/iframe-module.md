---
title: Iframe modulis
description: Šajā tēmā tiek stāstīts par iframe moduli un aprakstīts, kā to pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 58446289c9a53af30d4d6d331a1a609ae0d2a0ad
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818202"
---
# <a name="iframe-module"></a>Iframe modulis

[!include [banner](includes/banner.md)]

Šajā tēmā tiek stāstīts par iframe moduli un aprakstīts, kā to pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Iframe modulis nodrošina iframe (iekļauts kadrs), kas vieso ārējo saturu vietnē. Piemēram, to var izmantot, lai viesotu YouTube video vai PDF failu skatītāju jebkurā vietnes lapā. 

Iframe modulim nepieciešams mērķa URL. Tad tas vieso mērķa lapas saturu, kas atrodas HTML **iframe** elementā. Ārējiem URL jābūt atļautajā sarakstā (to sauc arī par "balto sarakstu") katras vietnes satura drošības politikas (CSP) direktīvām. Iframe saturam ir jāatļauj vietrāžus URL, izmantojot **frame-ancestor** direktīvu. Papildinformāciju skatiet [Pārvaldīt satura drošības politiku (CSP)](manage-csp.md).

> [!NOTE]
> Iframe modulis ir pieejams Dynamics 365 Commerce 10.0.13 laidienā.

Sekojošajā attēlā ir parādīti iframe moduļu piemēri, kas parāda ārējos videoklipus vietnes lapās.

![Piemērs iframe moduļiem, kas izrāda ārējos video](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a>Iframe moduļa rekvizīti

| Rekvizīta nosaukums             | Vērtība                 | apraksts |
|---------------------------|-----------------------|-------------|
| Virsraksts | Teksts | Moduļa virsraksts. |
| Mērķa URL | Vietrādis URL | Modulī viesotais vietrādis URL. |
| Augstums | Skaitlis vai procenti | Moduļa augstums, pikseļos vai procentos. Piemēram, vērtība **100** tiks apstrādāta kā pikseļu skaits, un vērtība **100%** tiks apstrādāta kā procenti. |
| Aria etiķete | Teksts | Pieejamības nolūkiem var definēt Pieejamo bagātinātā interneta lietojumprogrammu (ARIA) etiķeti. |

## <a name="add-an-iframe-module-to-a-page"></a>Iframe moduļa pievienošana lapā

Lai lappusei pievienotu iframe moduli, lai parādītu ārējo videoklipu, rīkojieties šādi.

1. Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu jaunu veidni.
1. Dialoglodziņā **Jauna veidne** zem **Veidnes nosaukums** ievadiet **Mārketinga veidne** un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Dodieties uz **Lapas** un atlasiet **Jauns**, lai izveidotu jaunu lapu.
1. Dialoglodziņā **Izvēlēties veidni** atlasiet veidni **Mārketinga veidne**. Sadaļā **Lapas nosaukums** ievadiet **Mārketinga lapa** pēc tam atlasiet **Labi**.
1. Jaunās lapas slotā **Galvenais** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Konteiners** un pēc tam atlasiet **Labi**.
1. Moduļa rekvizītu rūtī iestatiet **Platuma** vērtību, lai **Aizpildītu konteineru**.
1. Slotā **Konteiners** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **iframe** un pēc tam atlasiet **Labi**.
1. Moduļa rekvizītu rūtī iestatiet **Mērķa URL** vērtību video ārējam vietrādim URL.
1. Pēc nepieciešamības iestatiet citus rekvizītus, kā **Virsraksts** un **Augstums**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Dodieties uz vietnes mārketinga lapu. Jums vajadzētu redzēt, ka video tiek atveidots iframe modulī.
 
## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Satura drošības politikas (CSP) pārvaldība](manage-csp.md)
