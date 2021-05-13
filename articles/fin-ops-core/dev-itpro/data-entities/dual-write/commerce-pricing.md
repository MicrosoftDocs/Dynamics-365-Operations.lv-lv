---
title: Dynamics 365 Commerce cenu noteikšanas programmas izmantošana ar Dynamics 365 Sales
description: Šajā tēmā aprakstīts, kā lietot Microsoft Dynamics 365 Commerce cenu noteikšanas programmu, lai izveidotu pārdošanas piedāvājumus programmā Dynamics 365 Sales.
author: ShalabhjainMSFT
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: shajain
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-11-03
ms.openlocfilehash: fa93b1262049d80148ff23b3d7223ec0f6c2fe68
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941170"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a>Dynamics 365 Commerce cenu noteikšanas programmas izmantošana ar Dynamics 365 Sales

[!include [banner](../../includes/banner.md)]

Šajā tēmā aprakstīts, kā lietot Microsoft Dynamics 365 Commerce cenu noteikšanas programmu, lai izveidotu pārdošanas piedāvājumus programmā Dynamics 365 Sales.

Dynamics 365 Commerce cenu noteikšanas programma atbalsta lielāko daļu no uzņēmuma līdz patērētājam (B2C) cenu noteikšanas scenāriju, piemēram, veikala līmeņa cenu noteikšanu, uz piederību un lojalitāti balstītu cenu noteikšanu, atlaides dažādām vienas kolekcijas precēm, apjoma atlaides un atlaides par iztērētu noteiktu summu. Cenu noteikšanas programma izmanto kompleksas kārtulas, lai noteiktu labāko cenu dotajam piedāvājumam vai pasūtījumam.

Izmantojot [duālo rakstīšanu](./dual-write-overview.md), cenu noteikšanas vajadzībām ir pieejamas trīs opcijas. Varat izmantot statisko cenu noteikšanu, kas tiek iegūta no cenrāža Dynamics 365 Sales, cenu noteikšanas programmu Dynamics 365 Supply Chain Management vai cenu noteikšanas programmu Dynamics 365 Commerce. No šīm opcijām Commerce cenu noteikšanas programma ir vislabāk piemērota B2C scenārijiem.

## <a name="use-the-commerce-pricing-engine-in-sales"></a>Commerce cenu noteikšanas programmas izmantošana Sales

> [!NOTE]
> Pašlaik Commerce cenu noteikšanas programmu var izmantot tikai piedāvājuma izveidei Sales. Pārdošanas pasūtījuma integrācija ar Commerce cenu noteikšanas programmu vēl nav pieejama.

Kad lietotāji uzsāk piedāvājumu Sales, duālās rakstīšanas struktūra kopē detalizētu informāciju par piedāvājumu uz Commerce. Visas izmaiņas esošajās piedāvājuma rindās vai jebkādas nesen pievienotās piedāvājuma rindas Sales tiek kopētas uz Commerce. Kad lietotāji vēlas izmantot Commerce cenu noteikšanas programmu, lai noteiktu cenu piedāvājumam, tie var atlasīt **Cenas piedāvājums**, lai atjauninātu piedāvājuma cenas, pamatojoties uz Commerce cenu noteikšanas programmu. Šajā gadījumā cenas automātiski tiek atjauninātas gan Sales, gan Commerce.

## <a name="prerequisites"></a>Priekšnosacījumi

- Pirms varat izmantot Commerce cenu noteikšanas programmu Sales, jāseko darbībām, kas norādītas [Potenciālais klients līdz naudai duālajā rakstīšanā](./dual-write-prospect-to-cash.md).
- Lai veiktu manuālu ievadi, jāizslēdz tirdzniecības līgumu novērtēšana, veicot tālāk norādītās darbības.

    1. Savā Commerce vidē dodieties uz **Debitoru parādi \> Iestatīšana \> Debitoru parādu parametri**.
    1. Cilnē **Cenas**, kas atrodas kopsavilkuma cilnē **Tirdzniecības līguma novērtēšana**, nodzēsiet izvēles rūtiņu **Manuālā ievade**.

## <a name="additional-resources"></a>Papildu resursi

[Potenciālā klienta-naudas duālais ieraksts](./dual-write-prospect-to-cash.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]