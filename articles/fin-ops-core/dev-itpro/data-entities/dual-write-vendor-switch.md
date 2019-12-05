---
title: Pārslēgties starp kreditora modeļiem
description: ''
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 4e97ff0b0e6195b5e3703e15a0bb0de7644ef8d1
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772368"
---
# <a name="switch-between-vendor-designs"></a>Pārslēgties starp kreditora modeļiem

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a>Kreditora datu plūsma 

Ja izmantojat citas Dynamics 365 programmas kreditora pamatdatu apgūšanai un vēlaties nošķirt kreditora informāciju no debitoriem, izmantojiet šo pamata kreditora modeli.  

![Pamata kreditora plūsma](media/dual-write-switch-1.png)
 
Ja izmantojat citas Dynamics 365 programmas kreditora pamatdatu apgūšanai un vēlaties arī turpmāk izmantot elementu **Konts** kreditora informācijas glabāšanai, izmantojiet šo paplašināto kreditora modeli. Šajā modelī paplašināta kreditora informācija, piemēram, kreditora aizturēšanas statuss un kreditora profils, tiek glabāts elementā **kreditori** pakalpojumā Common Data Service. 

![Kreditora paplašinātā plūsma](media/dual-write-switch-2.png)
 
Izpildiet tālāk norādītās darbības, lai izmantotu paplašināto kreditora modeli. 
 
1. **SupplyChainCommon** risinājuma pakotnē ir iekļautas darbplūsmas procesa veidnes, kā redzams nākamajā attēlā.
    > [!div class="mx-imgBorder"]
    > ![Darbplūsmas procesa veidnes](media/dual-write-switch-3.png)
2. Izveidojiet jaunus darbplūsmas procesus, izmantojot darbplūsmas procesa veidnes: 
    1. Izveidojiet jaunu darbplūsmas procesu elementā **Kreditors**, izmantojot darbplūsmas procesa veidni **Izveidot kreditorus konta elementā** un noklikšķiniet uz **Labi**. Šī darbplūsma apstrādā kreditora izveides scenāriju elementam **Konts**.
        > [!div class="mx-imgBorder"]
        > ![Izveidot kreditorus konta elementā](media/dual-write-switch-4.png)
    2. Izveidojiet jaunu darbplūsmas procesu elementā **Kreditors**, izmantojot darbplūsmas procesa veidni **Atjaunināt kontu elementu** un noklikšķiniet uz **Labi**. Šī darbplūsma apstrādā kreditora atjaunināšanas scenāriju elementam **Konts**. 
        > [!div class="mx-imgBorder"]
        > ![Atjaunināt kontu elementu](media/dual-write-switch-5.png)
    3. Izveidojiet jaunus darbplūsmas procesus no veidnēm, kas izveidotas elementā **Konti**. 
        > [!div class="mx-imgBorder"]
        > ![Izveidot kreditorus kreditoru elementā](media/dual-write-switch-6.png)
        > [!div class="mx-imgBorder"]
        > ![Atjaunināt kreditoru elementu](media/dual-write-switch-7.png)
    4. Darbplūsmas var konfigurēt kā reāllaika vai fona darbplūsmas, pamatojoties uz jūsu prasībām. 
        > [!div class="mx-imgBorder"]
        > ![Konvertēt uz fona darbplūsmu](media/dual-write-switch-8.png)
    5. Aktivizējiet darbplūsmas, ko izveidojāt elementos **Konts** un **Kreditors**, lai sāktu izmantot Customer Engagement elementu **Konts** kreditora informācijas glabāšanai. 
 
