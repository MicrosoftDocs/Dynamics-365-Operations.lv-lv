---
title: Pārslēgšanās starp kreditoru noformējumiem
description: Šajā tēmā ir aprakstīts, kā pārslēgties starp kreditora datu integrāciju starp Finance and Operations programmām un Dataverse.
author: RamaKrishnamoorthy
ms.date: 09/20/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 21f48574d34b810c8ca554a55f1c063893a34b4d
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416813"
---
# <a name="switch-between-vendor-designs"></a>Pārslēgšanās starp kreditoru noformējumiem

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a>Kreditora datu plūsma 

Ja izvēlaties izmantot elementu **Konts** elementu, lai uzglabātu veidu **Organizācija** un tabulu **Kontaktpersona** veida **Persona** tipa kreditoriem, konfigurējiet šādas darbplūsmas. Pretējā gadījumā šī konfigurācija nav obligāta.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a>Izmantot paplašināto kreditoru noformējumu Organizācijas veida kreditoriem

**Dynamics365FinanceExtended** risinājuma pakotnē ir šādas darbplūsmas procesa veidnes. Katrai veidnei tiks izveidota darbplūsma.

+ Kreditoru izveide kontu tabulā
+ Kreditoru izveide kreditoru tabulā
+ Kreditoru atjaunināšana kontu tabulā
+ Kreditoru atjaunināšana kreditoru tabulā

Lai izveidotu jaunus darbplūsmas procesus, izmantojot darbplūsmas procesa veidnes, veiciet šādas darbības.

1. Izveidojiet darbplūsmas procesu elementam **Kreditors** un atlasiet darbplūsmas procesa veidni **Izveidot kreditorus konta tabulā**. Pēc tam atlasiet **Labi**. Šī darbplūsma apstrādā kreditora izveides scenāriju tabulai **Konts**.

    ![Izveidot kreditorus konta tabulas darbplūsmas procesā.](media/create_process.png)

2. Izveidojiet darbplūsmas procesu elementam **Kreditors** un atlasiet darbplūsmas procesa veidni **Izveidot kreditorus konta tabulā**. Pēc tam atlasiet **Labi**. Šī darbplūsma apstrādā kreditora atjaunināšanas scenāriju tabulai **Konts**.
3. Izveidojiet darbplūsmas procesu elementam **Kreditors** un atlasiet darbplūsmas procesa veidni **Izveidot kreditorus konta tabulā**.
4. Izveidojiet darbplūsmas procesu elementam **Kreditors** un atlasiet darbplūsmas procesa veidni **Izveidot kreditorus konta tabulā**.
5. Darbplūsmas var konfigurēt vai nu kā reāllaika vai fona darbplūsmas, atkarībā no jūsu prasībām. Lai konfigurētu darbplūsmu kā fona darbplūsmu, atlasiet **Pārvērst par fona darbplūsmu.**

    ![Poga Konvertēt uz fona darbplūsmu.](media/background_workflow.png)

6. Aktivizējiet darbplūsmas, ko izveidojāt tabulās **Konts** un **Kreditors**, lai sāktu izmantot elementu **Konts**, lai glabātu informāciju kreditoriem no veida **Organizācija**.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a>Izmantot paplašināto kreditoru noformējumu Personas veida kreditoriem

**Dynamics365FinanceExtended** risinājuma pakotnē ir šādas darbplūsmas procesa veidnes. Katrai veidnei tiks izveidota darbplūsma.

+ Izveidot kreditorus ar veidu Persona kreditoru tabulā
+ Izveidot kreditorus ar veidu Persona kontaktpersonu tabulā
+ Atjaunināt kreditorus ar veidu Persona kontaktpersonu tabulā
+ Atjaunināt kreditorus ar veidu Persona kreditoru tabulā

Lai izveidotu jaunus darbplūsmas procesus, izmantojot darbplūsmas procesa veidnes, veiciet šādas darbības.

1. Izveidojiet darbplūsmas procesu tabulai **Kreditors** un atlasiet darbplūsmas procesa veidni **Izveidot kreditorus ar veidu Persona Kontaktpersonu tabulā** darbplūsmas procesa veidnē. Pēc tam atlasiet **Labi**. Šī darbplūsma apstrādā kreditora izveides scenāriju tabulai **Kontaktpersona**.
2. Izveidojiet darbplūsmas procesu tabulai **Kreditors** un atlasiet darbplūsmas procesa veidni **Izveidot kreditorus ar veidu Persona Kontaktpersonu tabulā** darbplūsmas procesa veidnē. Pēc tam atlasiet **Labi**. Šī darbplūsma apstrādā kreditora atjaunināšanas scenāriju tabulai **Kontaktpersona**.
3. Izveidojiet darbplūsmas procesu tabulai **Kontaktpersona** un atlasiet darbplūsmas procesa veidni **Izveidot kreditorus ar veidu Persona kreditoru tabulā**.
4. Izveidojiet darbplūsmas procesu tabulai **Kontaktpersona** un atlasiet darbplūsmas procesa veidni **Izveidot kreditorus ar veidu Persona kreditoru tabulā**.
5. Darbplūsmas var konfigurēt vai nu kā reāllaika vai fona darbplūsmas, atkarībā no jūsu prasībām. Lai konfigurētu darbplūsmu kā fona darbplūsmu, atlasiet **Pārvērst par fona darbplūsmu.**
6. Aktivizējiet darbplūsmas, ko izveidojāt tabulās **Kontaktpersona** un **Kreditors**, lai sāktu izmantot elementu **Kontaktpersona**, lai glabātu informāciju kreditoriem no veida **Persona**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]