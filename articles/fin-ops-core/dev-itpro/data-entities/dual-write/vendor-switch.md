---
title: Pārslēgšanās starp kreditoru noformējumiem
description: Šajā tēmā ir aprakstīts, kā pārslēgties starp kreditora datu integrāciju starp Finance and Operations programmām un Dataverse.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 731efd3ae841960f3a2c0b9be210c5c68ac835f5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685513"
---
# <a name="switch-between-vendor-designs"></a>Pārslēgšanās starp kreditoru noformējumiem

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a>Kreditora datu plūsma 

Ja izvēlaties izmantot elementu **Konts** elementu, lai uzglabātu veidu **Organizācija** un elementu **Kontaktpersona** veida **Persona** tipa kreditoriem, konfigurējiet šādas darbplūsmas. Pretējā gadījumā šī konfigurācija nav obligāta.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a>Izmantot paplašināto kreditoru noformējumu Organizācijas veida kreditoriem

**Dynamics365FinanceExtended** risinājuma pakotnē ir šādas darbplūsmas procesa veidnes. Katrai veidnei tiks izveidota darbplūsma.

+ Kreditoru izveide kontu tabulā
+ Kreditoru izveide kreditoru tabulā
+ Kreditoru atjaunināšana kontu tabulā
+ Kreditoru atjaunināšana kreditoru tabulā

Lai izveidotu jaunus darbplūsmas procesus, izmantojot darbplūsmas procesa veidnes, veiciet šādas darbības.

1. Izveidojiet darbplūsmas procesu elementam **Kreditors** un atlasiet darbplūsmas procesa veidni **Izveidot kreditorus konta tabulā**. Pēc tam atlasiet **Labi**. Šī darbplūsma apstrādā kreditora izveides scenāriju elementam **Konts**.

    ![Izveidot kreditorus konta tabulas darbplūsmas procesā](media/create_process.png)

2. Izveidojiet darbplūsmas procesu elementam **Kreditors** un atlasiet darbplūsmas procesa veidni **Atjaunināt kreditorus konta tabulā**. Pēc tam atlasiet **Labi**. Šī darbplūsma apstrādā kreditora atjaunināšanas scenāriju elementam **Konts**.
3. Izveidojiet darbplūsmas procesu elementam **Konts** un atlasiet darbplūsmas procesa veidni **Izveidot kreditorus kreditoru tabulā**.
4. Izveidojiet darbplūsmas procesu elementam **Konts** un atlasiet darbplūsmas procesa veidni **Atjaunināt kreditorus kreditoru tabulā**.
5. Darbplūsmas var konfigurēt vai nu kā reāllaika vai fona darbplūsmas, atkarībā no jūsu prasībām. Lai konfigurētu darbplūsmu kā fona darbplūsmu, atlasiet **Pārvērst par fona darbplūsmu.**

    ![Poga Konvertēt uz fona darbplūsmu](media/background_workflow.png)

6. Aktivizējiet darbplūsmas, ko izveidojāt tabulās **Konts** un **Kreditors**, lai sāktu izmantot elementu **Konts**, lai glabātu informāciju kreditoriem no veida **Organizācija**.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a>Izmantot paplašināto kreditoru noformējumu Personas veida kreditoriem

**Dynamics365FinanceExtended** risinājuma pakotnē ir šādas darbplūsmas procesa veidnes. Katrai veidnei tiks izveidota darbplūsma.

+ Izveidot kreditorus ar veidu Persona kreditoru tabulā
+ Izveidot kreditorus ar veidu Persona kontaktpersonu tabulā
+ Atjaunināt kreditorus ar veidu Persona kontaktpersonu tabulā
+ Atjaunināt kreditorus ar veidu Persona kreditoru tabulā

Lai izveidotu jaunus darbplūsmas procesus, izmantojot darbplūsmas procesa veidnes, veiciet šādas darbības.

1. Izveidojiet darbplūsmas procesu elementam **Kreditors** un atlasiet darbplūsmas procesa veidni **Izveidot kreditorus ar veidu Persona kontaktpersonu tabulā**. Pēc tam atlasiet **Labi**. Šī darbplūsma apstrādā kreditora izveides scenāriju elementam **Kontaktpersona**.
2. Izveidojiet darbplūsmas procesu elementam **Kreditors** un atlasiet darbplūsmas procesa veidni **Atjaunināt kreditorus ar veidu Persona kontaktpersonu tabulā**. Pēc tam atlasiet **Labi**. Šī darbplūsma apstrādā kreditora atjaunināšanas scenāriju elementam **Kontaktpersona**.
3. Izveidojiet darbplūsmas procesu elementam **Kontaktpersona** un atlasiet darbplūsmas procesa veidni **Izveidot kreditorus ar veidu Persona kreditoru tabulā**.
4. Izveidojiet darbplūsmas procesu elementam **Kontaktpersona** un atlasiet darbplūsmas procesa veidni **Atjaunināt kreditorus ar veidu Persona kreditoru tabulā**.
5. Darbplūsmas var konfigurēt vai nu kā reāllaika vai fona darbplūsmas, atkarībā no jūsu prasībām. Lai konfigurētu darbplūsmu kā fona darbplūsmu, atlasiet **Pārvērst par fona darbplūsmu.**
6. Aktivizējiet darbplūsmas, ko izveidojāt tabulās **Kontaktpersona** un **Kreditors**, lai sāktu izmantot elementu **Kontaktpersona**, lai glabātu informāciju kreditoriem no veida **Persona**.
