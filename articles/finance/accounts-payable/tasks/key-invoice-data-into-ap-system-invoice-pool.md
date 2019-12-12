---
title: Rēķinu datu ievade kreditoru sistēmā, izmantojot rēķinu kopu
description: Šajā tēmā aprakstīts, kā lietot rēķinu reģistru, lai izveidotu rēķinus.
author: abruer
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f7d72c1d98100d1313109e8b5e55df02e2163174
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189365"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a>Rēķinu datu ievade kreditoru sistēmā, izmantojot rēķinu kopu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā tēmā aprakstīts, kā lietot rēķinu reģistru, lai izveidotu rēķinus. Pēc tam izmantojiet rēķinu kopu, lai saskaņotu rēķinu ar pirkšanas pasūtījumu un pabeigtu izdevumu kreditora rēķina lapā.


## <a name="create-a-purchase-order"></a>Pirkšanas pasūtījuma izveide
1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Kreditori > Pirkuma pasūtījumi > Pirkuma pasūtījumi**.
2. Atlasiet **Jauns**, lai izveidotu pirkuma pasūtījumu.
3. Laukā **Piegādātāja konts** nolaižamajā izvēlnē atlasiet piegādātāju. Piemēram, atlasiet piegādātāju **1001**.
4. Atlasiet **Labi**.
5. Laukā **Vienuma numurs** atlasiet pakalpojumu vienuma numuru no nolaižamās izvēlnes. Piemēram, atlasiet **S0001**. Neto summa ir 75,00.  Tā ir summa, kuru sagaidām rēķinā.  
6. Darbību rūtī atlasiet **Iegādāties**.
7. Atlasiet **Apstiprināt**.

## <a name="create-and-post-and-invoice"></a>Izveidot un grāmatot rēķinu
1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Kreditori > Rēķini > Rēķinu reģistrs**.
2. Atlasiet **Jauns**.
3. Lai atlasītu nosaukumu rēķinu reģistram, kuru vēlaties izmantot, atveriet uzmeklēšanu.
4. Atlasiet nosaukumu tam rēķinu reģistram, kuru vēlaties lietot.
5. Atlasiet **Rindas**, lai atvērtu reģistru un ievadītu izmaksu rindas. 
6. Uzmeklēšanas skatā atlasiet kreditoru. Piemēram, atlasiet piegādātāju **1001**.
7. Laukā **Rēķins** ievadiet rēķina numuru
8. Laukā **Apraksts** ierakstiet kādu vērtību.
9. Laukā **Kredīts** ievadiet kādu skaitli.
10. Laukā **Pirkuma pasūtījums** atveriet nolaižamo izvēlni, lai atlasītu pirkuma pasūtījumu, kuru pirms tam izveidojāt.
11. Laukā **Apstiprināja** nolaižamajā sarakstā iezīmējiet apstiprinātāju un noklikšķiniet uz **Atlasīt**, lai atlasītu šo apstiprinātāju.
12. Atlasiet **Grāmatot**.

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a>Lai pabeigtu rēķina izveides procesu, atveriet rēķinu no kopas un salīdziniet to ar pirkšanas pasūtījumu.
1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Kreditori > Rēķini > Rēķinu kopa**.
2. Atlasiet **Pirkuma pasūtījums**, lai izveidotu piegādātāja rēķinu no kopas rēķina.
3. Atlasiet rēķinu, kuru vēlaties pārskatīt.
4. Atlasiet **Atjaunināt salīdzinājuma statusu**, lai pabeigtu salīdzināšanu.
5. Darbību rūtī atlasiet **Opcijas**.
6. Atlasiet **Mainīt skatu**.
7. Atlasiet **Režģa skats**.
8. Atlasiet **Grāmatot**.
9. Aizveriet formu.
10. Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Kreditori > Piegādātāji > Piegādātāji**.
11. Atlasiet kreditoru, kuram tika sastādīts pirkšanas pasūtījums. Piemēram, atlasiet piegādātāju **1001**.
12. Darbību rūtī atlasiet **Piegādātājs**.
13. Atlasiet **Darbības**.
14. Atlasiet izveidoto rēķinu. Rēķinu reģistra uzkrāšana tika atsaukta un iegrāmatota atbilstošajā izdevumu kontā.  
