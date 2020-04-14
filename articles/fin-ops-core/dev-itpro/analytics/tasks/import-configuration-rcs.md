---
title: (ER) Konfigurāciju importēšana no RCS
description: Šajā tēmā ir sniegta informācija par to, kā lietotājs var importēt jaunu ER konfigurācijas versiju no RCS.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea2bfd2514be666d05165410ca27041a86464715
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143227"
---
# <a name="er-import-configurations-from-rcs"></a>(ER) Konfigurāciju importēšana no RCS

[!include [banner](../../includes/banner.md)]

Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko atskaišu izstrādātājs var importēt jaunu elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurācijas versiju no Microsoft Regulatory Configuration Services (RCS). Šajā piemērā ir jāatlasa RCS instancē konfigurētā ER konfigurācijas versija un jāimportē tā parauga uzņēmuma Litware, Inc. pašreizējā instancē. Šīs darbības var izpildīt jebkurā uzņēmumā, jo ER konfigurācijas tiek koplietotas starp uzņēmumiem. Lai izpildītu tālāk norādītās darbības, vispirms izpildiet darbības, kas ir aprakstītas tēmā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](er-configuration-provider-mark-it-active-2016-11.md). Lai veiktu šīs darbības, ir nepieciešama piekļuve arī RCS instancei, kas satur vismaz vienu ER konfigurāciju ar statusu **Pabeigts** vai **Koplietots**.

1. Dodieties uz **Organizācijas administrēšana** > **Darbvietas** > **Elektronisko pārskatu veidošana**. 
2. Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam Litware, Inc. ir pieejams un ir atzīmēts kā **Aktīvs**. Ja neredzat šo konfigurācijas nodrošinātāju, izpildiet darbības tēmā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](er-configuration-provider-mark-it-active-2016-11.md). 
3. Ja jūsu uzņēmuma nav nodrošināta neviena RCS vide, noklikšķiniet uz ārējās saites **Regulatory services — konfigurācija** un izpildiet norādījumus, lai nodrošinātu RCS vidi. 
4. Noklikšķiniet uz **Elektronisko pārskatu veidošanas parametri**. 
5. Noklikšķiniet uz cilnes **RCS**. 
6. Ja RCS vide jūsu uzņēmumam jau ir nodrošināta, izmantojiet lapās norādītos URL, lai piekļūtu tai. 
7. Aizvērt lapu. 

## <a name="register-a-new-er-repository"></a>Reģistrējiet jaunu ER repozitoriju. 
1. Sarakstā atzīmējiet atlasīto rindu. 
2. Atlasiet pakalpojumu sniedzēju Litware, Inc. 
3. Noklikšķiniet uz Repozitoriji. 
4. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu. 
5. Laukā Konfigurācijas repozitorija veids ievadiet "RCS". 
6. Noklikšķiniet uz Izveidot repozitoriju. 
7. RCS vides parādāmā nosaukuma laukā ievadiet vai atlasiet vērtību. 
8. Atlasiet vēlamo RCS instanci. Ņemiet vērā, ka tās var būt vairākas. 
9. Noklikšķiniet uz Labi. 

## <a name="import-er-configurations-from-rcs-based-repository"></a>ER konfigurāciju importēšana no RCS repozitorija
1. Noklikšķiniet uz **Rādīt filtrus**. 
2. Laukā **Nosaukums** ievadiet “RCS” filtra vērtību, izmantojot filtra operatoru **sākas ar**. 
3. Atverot atlasīto repozitoriju, lapā **Izveidot savienojumu ar Regulatory Configuration Services** noklikšķiniet uz saites **Noklikšķiniet šeit, lai izveidotu savienojumu ar Regulatory Configuration Services**. 
4. Noklikšķiniet uz **Atvērt**. 
5. Noklikšķiniet uz **Aizvērt**. 
6. Atlasiet nepieciešamo ER konfigurācijas versiju un noklikšķiniet uz **Importēt**, lai ievietotu to pašreizējā instancē.

