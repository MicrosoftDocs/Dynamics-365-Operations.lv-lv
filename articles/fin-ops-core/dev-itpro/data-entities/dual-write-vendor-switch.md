---
title: Pārslēgšanās starp kreditoru noformējumiem
description: Šajā tēmā ir aprakstīts, kā pārslēgties starp kreditora datu integrāciju starp Finance and Operations programmām un Common Data Service.
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
ms.openlocfilehash: 204d788e72e79e7acf744d24cbeacb0f9b47da7d
ms.sourcegitcommit: 3306e451f04df01c51d8d332306b135d8ae1e254
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/09/2019
ms.locfileid: "2902729"
---
# <a name="switch-between-vendor-designs"></a>Pārslēgšanās starp kreditoru noformējumiem

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a>Kreditora datu plūsma 

Ja izmantojat citas Dynamics 365 programmas kreditora pamatdatu apgūšanai un vēlaties nošķirt kreditora informāciju no debitoriem, izmantojiet šo pamata kreditora modeli.  

![Pamata kreditora plūsma](media/dual-write-vendor-data-flow.png)
 
Ja izmantojat citas Dynamics 365 programmas kreditora pamatdatu apgūšanai un vēlaties arī turpmāk izmantot elementu **Konts** kreditora informācijas glabāšanai, izmantojiet šo paplašināto kreditora modeli. Šajā modelī paplašināta kreditora informācija, piemēram, kreditora aizturēšanas statuss un kreditora profils, tiek glabāts elementā **kreditori** pakalpojumā Common Data Service. 

![Kreditora paplašinātā plūsma](media/dual-write-vendor-detail.jpg)
 
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
    5. Aktivizējiet darbplūsmas, ko izveidojāt elementos **Konts** un **Kreditors**, lai sāktu izmantot elementu **Konts** kreditora informācijas glabāšanai. 
 
