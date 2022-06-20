---
title: (ER) Konfigurāciju importēšana no RCS
description: Šajā rakstā ir sniegta informācija par to, kā lietotājs var importēt jaunu ER konfigurācijas versiju no RCS.
author: NickSelin
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5317b1f7c8c0af6cd5c839e065c590c4474c84de
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850148"
---
# <a name="er-import-configurations-from-rcs"></a>(ER) Konfigurāciju importēšana no RCS

[!include [banner](../../includes/banner.md)]

Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko atskaišu izstrādātājs var importēt jaunu elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurācijas versiju no Microsoft Regulatory Configuration Services (RCS). Šajā piemērā ir jāatlasa RCS instancē konfigurētā ER konfigurācijas versija un jāimportē tā parauga uzņēmuma Litware, Inc. pašreizējā instancē. Šīs darbības var izpildīt jebkurā uzņēmumā, jo ER konfigurācijas tiek koplietotas starp uzņēmumiem. Lai veiktu šīs darbības, vispirms ir jāveic soļi rakstā, izveidojiet konfigurācijas nodrošinātājus [un atzīmējiet tos kā aktīvus](er-configuration-provider-mark-it-active-2016-11.md). Lai veiktu šīs darbības, ir nepieciešama piekļuve arī RCS instancei, kas satur vismaz vienu ER konfigurāciju ar statusu **Pabeigts** vai **Koplietots**.

1. Dodieties uz **Organizācijas administrēšana** > **Darbvietas** > **Elektronisko pārskatu veidošana**. 
2. Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam Litware, Inc. ir pieejams un ir atzīmēts kā **Aktīvs**. Ja šī konfigurācijas nodrošinātājs nav redzams, izpildiet rakstu norādītās darbības, [izveidojiet konfigurācijas nodrošinātājus un atzīmējiet tos kā aktīvus](er-configuration-provider-mark-it-active-2016-11.md). 
3. Ja jūsu uzņēmuma nav nodrošināta neviena RCS vide, atlasiet ārējo saiti **Regulatory services — konfigurācija** un izpildiet norādījumus, lai nodrošinātu RCS vidi. 
4. Atlasiet **Elektronisko pārskatu veidošanas parametri**. 
5. Atlasiet cilni **RCS**. 
6. Ja RCS vide jūsu uzņēmumam jau ir nodrošināta, izmantojiet lapās norādītos URL, lai piekļūtu tai. 
7. Aizvērt lapu. 

## <a name="register-a-new-er-repository"></a>Reģistrējiet jaunu ER repozitoriju. 
1. Sarakstā atzīmējiet atlasīto rindu. 
2. Atlasiet pakalpojumu sniedzēju Litware, Inc. 
3. Atlasiet Repozitoriji. 
4. Atlasiet Pievienot, lai atvērtu nolaižamo dialoglodziņu. 
5. Laukā Konfigurācijas repozitorija veids ievadiet "RCS". 
6. Atlasiet Izveidot repozitoriju. 
7. RCS vides parādāmā nosaukuma laukā ievadiet vai atlasiet vērtību. 
8. Atlasiet vēlamo RCS instanci. Tās var būt vairākas. 
9. Atlasiet Labi. 

## <a name="import-er-configurations-from-rcs-based-repository"></a>ER konfigurāciju importēšana no RCS repozitorija
1. Atlasiet **Rādīt filtrus**. 
2. Laukā **Nosaukums** ievadiet “RCS” filtra vērtību, izmantojot filtra operatoru **sākas ar**. 
3. Atverot atlasīto repozitoriju, lapā **Izveidot savienojumu ar Regulatory Configuration Services** atlasiet saiti **Atlasiet šeit, lai izveidotu savienojumu ar Regulatory Configuration Services**. 
4. Atlasiet **Atvērt**. 
5. Atlasiet **Aizvērt**. 
6. Atlasiet nepieciešamo ER konfigurācijas versiju un atlasiet **Importēt**, lai ievietotu to pašreizējā instancē.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]