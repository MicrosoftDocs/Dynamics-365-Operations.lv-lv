---
title: "Sagādes un avotu darbplūsmas"
description: "Dažas organizācijas pieprasa, lai pirkšanas pieprasījumus un pirkšanas pasūtījumus apstiprinātu cits lietotājs nekā persona, kura ievadīja darījumu. Lai iestatītu apstiprināšanas procesu, varat izveidot darbplūsmu."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 75daeed0d0e979165d3669e83e98cf278d7fb736
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---

# <a name="procurement-and-sourcing-workflows"></a>Sagādes un avotu darbplūsmas

[!include [banner](../includes/banner.md)]

Dažas organizācijas pieprasa, lai pirkšanas pieprasījumus un pirkšanas pasūtījumus apstiprinātu cits lietotājs nekā persona, kura ievadīja darījumu. Lai iestatītu apstiprināšanas procesu, varat izveidot darbplūsmu.

Darbplūsma attēlo biznesa procesu. Izmantojot darbplūsmu, tiek noteikta dokumenta plūsma caur sistēmu un norādīts, kuram ir jāpabeidz uzdevums vai jāapstiprina dokuments. Darbplūsmas sistēmas lietošanai organizācijā ir vairākas priekšrocības.
-   **Saskaņoti procesi** — varat definēt noteiktu dokumentiem, piemēram, pirkšanas pieprasījumu un izdevumu pārskatu, apstiprināšanas procesu. Izmantojot darbplūsmas sistēmu, varat nodrošināt saskaņotu un efektīvu dokumentu apstrādes un apstiprināšanas procesu.
-   **Procesa pārskatāmība** — varat sekot līdzi noteiktas darbplūsmas instances statusa, vēsturiskajiem un veiktspējas rādītājiem. Tādējādi varat noteikt, vai ir jāveic darbplūsmas izmaiņas, lai uzlabotu efektivitāti.
-   **Centralizēts darbu saraksts** — lietotāji var skatīt centralizētu darbu sarakstu, lai skatītu darbplūsmas uzdevumus un apstiprinājumus, kas viņiem ir piešķirti visās darbplūsmās, kurās viņi piedalās. Šī funkcija ir pieejama lapā Darba vienumi.

## <a name="the-types-of-workflows-that-you-can-create"></a>Izveidojamo darbplūsmu veidi
Sagādei un avotiem ir pieejami šādi darbplūsmu veidi.

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| **Tips**                         | **Šī tipa lietošanas nolūks**                                          |
| Pirkšanas pieprasījuma pārskats      | Izveidot pārskatīšanas un apstiprināšanas darbplūsmas pirkšanas pieprasījumiem.            |
| Pirkšanas pieprasījuma rindas pārskats | Izveidot pārskatīšanas un apstiprināšanas darbplūsmas pirkšanas pieprasījumu rindām.       |
| Pirkšanas pasūtījuma darbplūsma          | Izveidojiet pārskatīšanas un apstiprināšanas darbplūsmas pirkšanas pasūtījumiem.     |
| Pirkšanas pasūtījuma rindas darbplūsma     | Izveidojiet pārskatīšanas un apstiprināšanas darbplūsmas pirkšanas rindas pasūtījumiem. |
| Kreditoru pievienošanas pieteikumu darbplūsma  | Izveidot pārskatīšanas un apstiprināšanas darbplūsmas jaunu piegādātāju pievienošanai, izmantojot piegādātāju pieprasījumus. |

## <a name="creating-a-workflow"></a>Darbplūsmas izveide
Lai izveidotu darbplūsmu, pārejiet uz sadaļu Sagāde un avoti &gt; Iestatījumi &gt; Sagādes un avotu darbplūsmas un izveidojiet jaunu darbplūsmu, atlasot izveidojamās darbplūsmas veidu.  

Darbplūsmas audeklā varat vilkt darbplūsmas elementus uz veidotāju un saistīt elementus plūsmā. Darbplūsmas elementi ir jākonfigurē. Apstiprinājumam un uzdevuma darbplūsmas elementiem var konfigurēt to, kuram dalībniekam jāveic darbība.
Dalībnieku tipi
----------------------

Apstiprināšanas darbību varat piešķirt šādām dalībnieku grupām.

| Lietotāju grupa    | Apraksts                                                               |
|---------------|---------------------------------------------------------------------------|
| Dalībnieks   | Piešķiriet apstiprināšanas darbību kādas grupas vai lomas dalībniekiem.                   |
| Hierarhija     | Piešķiriet apstiprināšanas darbību lietotājiem noteiktā organizācijas hierarhijā. |
| Darbplūsmas lietotājs | Piešķiriet apstiprināšanas darbību šīs darbplūsmas lietotājiem.                       |
| Rinda         | Piešķiriet apstiprinājuma darbību darba vienumu rindai.                            |
| Lietotājs          | Piešķiriet apstiprināšanas darbību konkrētiem lietotājiem.                               |



<a name="additional-resources"></a>Papildu resursi
--------

[Biznesa procesu darbplūsmu definēšana pirkšanas pieprasījumiem](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

[Pirkšanas pieprasījuma darbplūsma](purchase-requisitions-workflow.md)

[Kreditoru pievienošana](vendor-onboarding.md)


