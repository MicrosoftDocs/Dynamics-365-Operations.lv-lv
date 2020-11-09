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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 0ecc401706911f8b92146b95bb6415185df8b451
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997556"
---
# <a name="switch-between-vendor-designs"></a>Pārslēgšanās starp kreditoru noformējumiem

[!include [banner](../../includes/banner.md)]



## <a name="vendor-data-flow"></a>Kreditora datu plūsma 

Ja izvēlaties izmantot elementu **Konts** elementu, lai uzglabātu veidu **Organizācija** un elementu **Kontaktpersona** veida **Persona** tipa kreditoriem, konfigurējiet šādas darbplūsmas. Pretējā gadījumā šī konfigurācija nav obligāta.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a>Izmantot paplašināto kreditoru noformējumu Organizācijas veida kreditoriem

**Dynamics365FinanceExtended** risinājuma pakotnē ir šādas darbplūsmas procesa veidnes. Katrai veidnei tiks izveidota darbplūsma.

+ Izveidot kreditorus konta elementā
+ Izveidot kreditorus kreditoru elementā
+ Atjaunināt kreditorus konta elementā
+ Atjaunināt kreditorus kreditoru elementā

Lai izveidotu jaunus darbplūsmas procesus, izmantojot darbplūsmas procesa veidnes, veiciet šādas darbības.

1. Izveidojiet darbplūsmas procesu elementam **Kreditors** un atlasiet darbplūsmas procesa veidni **Izveidot kreditorus konta elementā**. Tad atl. **Labi**. Šī darbplūsma apstrādā kreditora izveides scenāriju elementam **Konts**.

    ![Izveidot kreditorus konta elementa darbplūsmas procesā](media/create_process.png)

2. Izveidojiet darbplūsmas procesu elementam **Kreditors** un atlasiet darbplūsmas procesa veidni **Atjaunināt kreditorus konta elementā**. Tad atl. **Labi**. Šī darbplūsma apstrādā kreditora atjaunināšanas scenāriju elementam **Konts**.
3. Izveidojiet darbplūsmas procesu elementam **Konts** un atlasiet darbplūsmas procesa veidni **Izveidot kreditorus kreditoru elementā**.
4. Izveidojiet darbplūsmas procesu elementam **Konts** un atlasiet darbplūsmas procesa veidni **Atjaunināt kreditorus kreditoru elementā**.
5. Darbplūsmas var konfigurēt vai nu kā reāllaika vai fona darbplūsmas, atkarībā no jūsu prasībām. Lai konfigurētu darbplūsmu kā fona darbplūsmu, atlasiet **Pārvērst par fona darbplūsmu.**

    ![Poga Konvertēt uz fona darbplūsmu](media/background_workflow.png)

6. Aktivizējiet darbplūsmas, ko izveidojāt elementos **Konts** un **Kreditors** , lai sāktu izmantot elementu **Konts** , lai glabātu informāciju kreditoriem no veida **Organizācija**.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a>Izmantot paplašināto kreditoru noformējumu Personas veida kreditoriem

**Dynamics365FinanceExtended** risinājuma pakotnē ir šādas darbplūsmas procesa veidnes. Katrai veidnei tiks izveidota darbplūsma.

+ Izveidot kreditorus ar veidu Persona kreditoru elementā
+ Izveidot kreditorus ar veidu Persona kontaktpersonu elementā
+ Atjaunināt kreditorus ar veidu Persona kontaktpersonu elementā
+ Atjaunināt kreditorus ar veidu Persona kreditoru elementā

Lai izveidotu jaunus darbplūsmas procesus, izmantojot darbplūsmas procesa veidnes, veiciet šādas darbības.

1. Izveidojiet darbplūsmas procesu elementam **Kreditors** un atlasiet darbplūsmas procesa veidni **Izveidot kreditorus ar veidu Persona kontaktpersonu elementā**. Tad atl. **Labi**. Šī darbplūsma apstrādā kreditora izveides scenāriju elementam **Kontaktpersona**.
2. Izveidojiet darbplūsmas procesu elementam **Kreditors** un atlasiet darbplūsmas procesa veidni **Atjaunināt kreditorus ar veidu Persona kontaktpersonu elementā**. Tad atl. **Labi**. Šī darbplūsma apstrādā kreditora atjaunināšanas scenāriju elementam **Kontaktpersona**.
3. Izveidojiet darbplūsmas procesu elementam **Kontaktpersona** un atlasiet darbplūsmas procesa veidni **Izveidot kreditorus ar veidu Persona kreditoru elementā**.
4. Izveidojiet darbplūsmas procesu elementam **Kontaktpersona** un atlasiet darbplūsmas procesa veidni **Atjaunināt kreditorus ar veidu Persona kreditoru elementā**.
5. Darbplūsmas var konfigurēt vai nu kā reāllaika vai fona darbplūsmas, atkarībā no jūsu prasībām. Lai konfigurētu darbplūsmu kā fona darbplūsmu, atlasiet **Pārvērst par fona darbplūsmu.**
6. Aktivizējiet darbplūsmas, ko izveidojāt elementos **Kontaktpersona** un **Kreditors** , lai sāktu izmantot elementu **Kontaktpersona** , lai glabātu informāciju kreditoriem no veida **Persona**.
