---
title: Instalējiet programmu Microservices pievienojumprogrammu pakalpojumam Lifecycle Services
description: Šajā tēmā skaidrots, kā instalēt elektronisko rēķinu izrakstīšanas pievienojumprogrammu lifecycle Microsoft Dynamics Services (LCS).
author: dkalyuzh
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: a575f3e26489607dc2143ba05c941240969a0feb
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371971"
---
# <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>Instalējiet programmu Microservices pievienojumprogrammu pakalpojumam Lifecycle Services

[!include [banner](../includes/banner.md)]

Lai varētu veikt autentifikāciju elektronisko rēķinu izrakstīšanas pakalpojumā, pakalpojumu platformā ir jāreģistrē korporācija Microsoft Dynamics 365 Finance Dynamics 365 Supply Chain ManagementMicrosoft Dynamics vai vide, instalējot pievienojumprogrammu jūsu videi pakalpojumā Lifecycle Services (LCS).

Lai reģistrētu vidi, veiciet šādus soļus.

1. Piesakieties savā LCS kontā.
2. Projekta informācijas panelī atlasiet LCS projektu.
2. Projekta informācijas panelī **Vides** atlasiet izvietoto vidi. atlasītājai videi jābūt palaistai.
3. **Power Platform Cilnes Integrācija** sadaļā **Vides pievienojumprogrammas** atlasiet Instalēt **jaunu pievienojumprogrammu**.
4. Atlasiet **Elektronisko rēķinu izrakstīšana**.
5. Laukā **AAD pieteikuma ID** ievadiet **091c98b0-a1c9-4b02-b62c-7753395ccabe**. Šī vērtība ir fiksēta vērtība. Pārliecinieties, vai tiek ievadīts tikai globāli unikāls identifikators (GUID). Neietveriet citus simbolus, piemēram, atstarpes, komatus, punktus vai pēdiņas.
6. Laukā **AAD nomnieka ID** ievadiet jūsu Azure abonementa konta nomnieka ID. Azure Active Directory(Azure AD) Jūsu norādītam nomniekam jābūt tam pašam nomniekam, kas tiek izmantots regulēšanas konfigurācijas pakalpojumam (RCS).
7. Pārskatiet noteikumus un nosacījumus un pēc tam atzīmējiet izvēles rūtiņu.
8. Atlasiet **Instalēt**. Pēc dažām minūtēm statusam jāmainās no **Instalē** uz **Instalēts**. Lai skatītu šīs izmaiņas, iespējams, būs jāatsvaidzina lapa.

Elektronisko rēķinu izrakstīšana tagad ir gatava lietošanai.

> [!NOTE]
> Uzņēmumiem parasti ir vairākas finanšu vai piegādes ķēžu pārvaldības vides. Šīs vides ietver ražošanas vides, lietotāju pieņemšanas testa (UAT) vides un izstrādes (kaska) vides. Iepriekšējā procedūra jāveic visām vidēm, kuras vēlaties savienot ar elektronisko rēķinu izrakstīšanu.
