---
title: Iframe modulis
description: Šajā tēmā tiek stāstīts par iframe moduli un aprakstīts, kā to pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: bce6a50e8c145f8961bd0c839fe16c1f4d69e811
ms.sourcegitcommit: 408786b164b44bee4e16ae7c3d956034d54c3f80
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/05/2021
ms.locfileid: "7754018"
---
# <a name="iframe-module"></a>Iframe modulis

[!include [banner](includes/banner.md)]

Šajā tēmā tiek stāstīts par iframe moduli un aprakstīts, kā to pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.

Iframe modulis nodrošina iframe (iekļauts kadrs), kas vieso ārējo saturu vietnē. Piemēram, to var izmantot, lai viesotu YouTube video vai PDF failu skatītāju jebkurā vietnes lapā. 

Iframe modulim nepieciešams mērķa URL. Tad tas vieso mērķa lapas saturu, kas atrodas HTML **iframe** elementā. Ārējiem URL jābūt atļautajā sarakstā katras vietnes satura drošības politikas (CSP) direktīvām. Iframe saturam ir jāatļauj vietrāžus URL, izmantojot **frame-ancestor** direktīvu. Papildinformāciju skatiet [Pārvaldīt satura drošības politiku (CSP)](manage-csp.md).

> [!NOTE]
> Iframe modulis ir pieejams Dynamics 365 Commerce 10.0.13 laidienā.

Sekojošajā attēlā ir parādīti iframe moduļu piemēri, kas parāda ārējos videoklipus vietnes lapās.

![Piemērs iframe moduļiem, kas izrāda ārējos video.](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a>Iframe moduļa rekvizīti

| Rekvizīta nosaukums             | Vērtība                 | Apraksts |
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

> [!NOTE]
> Tā kā iframe modulis vieso ārēju saturu, vietas autoriem ir jānodrošina, ka iframe modulī viesotais saturs nepārkāpj satura ierobežojumu politiku attiecīgajā tirgū. Ja lapā, kas izmanto iframe moduli, ir satura pārkāpums, vietas autors var noņemt iframe moduli, atverot lapu vietas veidotājā, atlasot Noņemt moduli iframe moduļa slotā un pēc tam saglabājot un atkārtoti publicējot **·** lapu.

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Satura drošības politikas (CSP) pārvaldība](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
