---
title: Preču kvalitātes pārbaude
description: Šajā tēmā ir paskaidrots, kā apstrādāt kvalitātes pārbaudes pasūtījumu.
author: perlynne
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 75fbfbb7b993b528e96d247dafa2bdfe20837987
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145621"
---
# <a name="inspect-the-quality-of-goods"></a>Preču kvalitātes pārbaude

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā apstrādāt kvalitātes pārbaudes pasūtījumu. Šo ceļvedi varat izpildīt demonstrācijas datu uzņēmumā USMF. Pirms sākat šo piemēra procedūru, jums ir jāapstiprina pirkšanas pasūtījums "000016" un jāiegrāmato produktu ieejas plūsma. Šādi automātiski tiks izveidots kvalitātes pārbaudes pasūtījums. Kvalitātes pārbaudes parasti veic kvalitātes darbinieks.


## <a name="select-a-quality-order"></a>Atlasiet kvalitātes pārbaudes pasūtījumu.
1. Navigācijas rūtī dodieties uz **Moduļi > Krājumu vadība > Periodiskie uzdevumi > Kvalitātes vadība > Kvalitātes pārbaudes pasūtījumi**.
2. Atlasiet kvalitātes pārbaudes pasūtījumu, kas tika izveidots pirms šīs procedūras uzsākšanas.  

## <a name="record-test-results"></a>Testa rezultātu reģistrēšana
1. Atlasiet **Rezultāti**.
2. Atlasiet **Rediģēt**.
3. Laukā **Rezultātu daudzums** ierakstiet skaitli.
4. Laukā **Iznākums** nolaižamamajā izvēlnē atlasiet vēlamo ierakstu.  
- Šajā piemērā rezultāta pamatā ir iepriekš definēts iznākums. Parasti tiek ierakstīts specifiskāks testa rezultāts, piemēram, izmērs vai cita dimensija.  
5. Atlasiet **Saglabāt**.
6. Aizvērt lapu.

## <a name="validate-the-quality-order"></a>Pārbaudīt kvalitātes pasūtījumu
1. Atlasiet **Validēt**.
2. Laukā **Validējis** atlasiet lietotāju, kurš veic pārbaudi no nolaižamās izvēlnes.  
3. Noklikšķiniet uz **Atlasīt**.
4. Atlasiet **Labi**.
5. Aizvērt lapu.

