---
title: Datu modeļu definīciju atlase, veidojot formātus
description: Lai izpildītu šīs procedūras darbības, vispirms izpildiet procedūrau “ER Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu”.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66b9636f6d9da06f0ea65ab311dd9308ff6ae020
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184719"
---
# <a name="select-data-model-definitions-when-you-create-formats"></a>Datu modeļu definīciju atlase, veidojot formātus

[!include [task guide banner](../../includes/task-guide-banner.md)]

Lai izpildītu šīs procedūras darbības, vispirms izpildiet procedūrau “ER Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu”. 

Šajā procedūrā parādīts, kā modeļa saknes vienumu var atlasīt kā datu modeļa definīciju ievietošanai elektroniskā pārskata (ER) formāta konfigurācijā, kas paredzēta elektronisko dokumentu ģenerēšanai. Šajā procedūrā jūs pievienosit jaunu ER formāta konfigurāciju parauga uzņēmumam “Litware, Inc.”. 

Šī procedūra ir paredzēta lietotājiem, kuriem ir piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma. Darbības var veikt, izmantojot jebkuru datu kopu.

1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.
    * Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam “Litware, Inc.” ir pieejams un ir atzīmēts kā aktīvs. Ja neredzat šo konfigurācijas nodrošinātāju, jums vispirms ir jāizpilda darbības, kas aprakstītas procedūrā “Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu”.  
2. Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.

## <a name="add-a-new-er-data-model-configuration"></a>Pievienot jaunu ER datu modeļa konfigurāciju
1. Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.
    * Mēs pievienojam jaunu ER modeļa konfigurāciju, kas satur datu modeli, kurš paredzēts lietošanai kā datu avots ER pārskatu ģenerēšanai.  
2. Laukā Nosaukums ierakstiet “Maksājuma modelis (fiktīvs)”.
    * Maksājuma modelis (fiktīvs)  
3. Klikšķiniet Izveidot konfigurāciju.
4. Noklikšķiniet uz Veidotājs.
    * Atveriet ER veidotāju, lai norādītu šīs konfigurācijas datu modeļa struktūru.  
    * Pieņemsim, ka mēs noformējam datu modeli maksājumu biznesa jomai, lai atbalstītu 2 maksājumu metodes — kredīta pārskaitījumu un tiešo debetu.  
5. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
6. Laukā Nosaukums ierakstiet “Maksājumi — kredīta pārskaitījums”.
    * Maksājumi — kredīta pārskaitījums  
7. Noklikšķiniet uz Pievienot.
8. Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.
9. Laukā Jauns zars ievadiet “Modeļa sakne”.
10. Laukā Nosaukums ierakstiet “Maksājumi — tiešais debets”.
    * Maksājumi — tiešais debets  
11. Noklikšķiniet uz Pievienot.
12. Noklikšķiniet uz Saglabāt.
13. Aizvērt lapu.
14. Noklikšķiniet uz Mainīt statusu.
    * Pabeidziet modeļa melnraksta versiju, lai to padarītu pieejamu jaunā modeļa kartējumos un formātos.  
15. Noklikšķiniet uz Pabeigt.
16. Noklikšķiniet uz OK.

## <a name="start-to-enter-a-new-er-format-configuration"></a>Sākt ievadīt jaunu ER formāta konfigurāciju
1. Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.
2. Laukā Jauns ievadiet “Uz datu modeli Maksājuma modelis (fiktīvs) balstīts formāts”.
3. Ievadiet vai atlasiet kādu vērtību laukā Datu modelis.
    * Ņemiet vērā, ka visi saknes vienumi ar atlasīto datu modeli pašlaik ir pieejami atlasei kā datu modeļa definīcijas. Varat turpināt noformēt formātu, izmantojot jebkuru no nepieciešamajiem datu modeļa saknes vienumiem. Varat turpināt arī tad, ja atlasītajam saknes vienumam trūkst modeļa kartējuma.  
4. Aizvērt lapu.

## <a name="add-a-new-er-model-mapping-configuration"></a>Pievienot jaunu ER datu modeļa kartējuma konfigurāciju
1. Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.
2. Laukā Jauns ievadiet “Uz datu modeli Maksājuma modelis (fiktīvs) balstīts modeļa kartējums”.
3. Laukā Nosaukums ierakstiet “Maksājuma modeļa kartējumi (fiktīvi)”.
    * Maksājuma modeļa kartējumi (fiktīvi)  
4. Ievadiet vai atlasiet kādu vērtību laukā Datu modelis.
5. Klikšķiniet Izveidot konfigurāciju.

## <a name="design-er-model-mappings"></a>Veidot ER modeļu kartējumus
1. Noklikšķiniet uz Veidotājs.
    * Izmantojiet ER izstrādes rīku, lai norādītu nepieciešamo saknes vienumu modeļa kartējumus.  
2. Noklikšķiniet uz Veidotājs.
    * Simulējiet atlasītā modeļa kartējums iestatīšanu atlasītajam modeļa saknes vienumam.  
3. Kokā atlasiet 'Dynamics 365 for Operations\Tabulas ieraksti'.
4. Noklikšķiniet uz Pievienot sakni.
5. Laukā Nosaukums ierakstiet “Virsgrāmata”.
6. Laukā Tabula ierakstiet 'LedgerJournalTrans'.
    * LedgerJournalTrans  
7. Noklikšķiniet uz OK.
8. Noklikšķiniet uz Saglabāt.
9. Aizvērt lapu.
10. Aizvērt lapu.

## <a name="start-to-enter-another-new-er-format-configuration"></a>Sākt ievadīt citu jaunu ER formāta konfigurāciju
1. Koka struktūrā atlasiet “Maksājuma modelis (fiktīvs)”.
2. Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.
3. Laukā Jauns ievadiet “Uz datu modeli Maksājuma modelis (fiktīvs) balstīts formāts”.
4. Ievadiet vai atlasiet kādu vērtību laukā Datu modelis.
    * Ņemiet vērā, ka tagad ir pieejams tikai viens saknes vienums, lai kartētu programmas datu avotus. Kad ir ieviests vismaz viens modeļa kartējums, kā modeļa definīciju ER formāta pievienošanas laikā var atlasīt tikai modeļa saknes vienumus, kas ir kartēti programmas datu avotiem.   
5. Aizvērt lapu.

