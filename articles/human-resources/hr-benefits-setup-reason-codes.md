---
title: Iestatiet cēloņa kodus
description: Dynamics 365 Human Resources izmanto pamatojuma kodus, lai izskaidrotu, kāpēc nodarbinātā atvieglojumi mainās.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c799a81f38a5dbd5996afbda9529fa83d7fe5cf9
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468399"
---
# <a name="set-up-reason-codes"></a>Iestatiet cēloņa kodus

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources izmanto pamatojuma kodus, lai izskaidrotu, kāpēc nodarbinātā atvieglojumi mainās.

> [!NOTE]
> No 2021. gada janvāra iemeslu kodi tiek migrēti uz darbvietu **Personāla vadība**, nevis uz darbvietu **Atvieglojumu pārvaldība**. Papildinformāciju skatiet sadaļā [Iemesla kodu manuāla migrēšana uz Personāla pārvaldību](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).

## <a name="create-reason-codes"></a>Iemeslu kodu izveide

1. Darbvietā **Personāla pārvaldība** (vai darbvietā **Atvieglojumu pārvaldība**, ja iemeslu kodi vēl nav migrēti), atlasiet **Saites** un pēc tam atlasiet **Iemeslu kodi**.

2. Atlasiet **Jauns**.

3. Norādiet vērtības tālāk minētajos laukos.

   | Lauks | Apraksts |
   | --- | --- |
   | **Pamatojuma kods** | Unikālais nosaukums, lai identificētu iemeslu, kāpēc nodarbinātais varētu mainīt atvieglojumu plāna reģistrāciju. |
   | **Apraksts** | Pamatojuma koda apraksts. |

4. Sadaļā **Piemērojamie scenāriji** iestatiet **Atvieglojumu pārvaldība** uz **Jā**. (Nav piemērojams, ja iemeslu kodi vēl nav migrēti uz darbvietu **Personāla pārvaldība**.)

5. Atlasiet **Saglabāt**.

## <a name="manually-migrate-reason-codes-to-personnel-management"></a>Iemesla kodu manuāla migrēšana uz Personāla pārvaldību

2021. gada janvārī iemeslu kodi tiek migrēti uz darbvietu **Personāla vadība**, nevis uz darbvietu **Atvieglojumu pārvaldība**. Vairums iemesla koda datu tiks automātiski migrēti jūsu vidē. Daži iemesla koda dati, iespējams, netiks migrēti. Piemēram, iemeslu kodiem tagad ir maksimālais 15 rakstzīmju skaits, tāpēc visi iemeslu kodi, kas pārsniedz 15 rakstzīmes, netiks migrēti automātiski.

Jūs redzēsit reklāmkarogu darbvietas **Atvieglojumu pārvaldība** lapā **Saites**, kurā būs sniegta informācija par migrāciju un to, vai kādi iemeslu kodi netika migrēti.

1. Atlasiet **Iemeslu kodi**, lai skatītu detalizētu informāciju par migrācijas statusu.

   [![Iemeslu kodi](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)

2. Atlasiet iemeslu kodu, kas netika migrēts.

   [![Iemesla koda migrācijas statuss](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)

3. Atlasiet **Migrēt iemesla kodu**.

   [![Migrēt iemesla kodu](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)

4. Rūtī **Atvieglojuma iemesla koda migrācija** jums ir divas opcijas kartēšanai uz Personāla pārvaldības iemesla kodu:

   - Lai Personāla pārvaldībā izmantotu esošu iemesla kodu, izvēlieties vienu kodu nolaižamajā sarakstā **Izmantot esošo iemesla kodu**.
     > [!NOTE]
     > Personāla pārvaldībā varat izmantot esošu iemesla kodu tikai tad, ja cits Atvieglojumu pārvaldības iemesla kods vēl nav migrēts uz to.
   - Lai Personāla pārvaldībā izveidotu jaunu iemesla kodu, ievadiet jaunu iemesla kodu sadaļā **Jauns iemesla kods** un tam ievadiet aprakstu sadaļā **Jauns apraksts**.

   [![Kartēt uz Personāla pārvaldības iemesla kodu](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)

Kad iemeslu kodi ir migrēti uz Personāla pārvaldību, opcija tos izmantot Atvieglojumu pārvaldībā tiek automātiski iestatīta uz **Jā**.

[![Izmantot iemesla kodu Atvieglojumu pārvaldībā](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]