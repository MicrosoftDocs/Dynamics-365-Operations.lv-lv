---
title: Jaunu lietotāju izveide
description: Lietotāji ir jūsu organizācijas iekšējie darbinieki vai ārējie debitori un kreditori, kuriem nepieciešama piekļuve sistēmai sava darba veikšanai.
author: maertenm
manager: AnnBe
ms.date: 08/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a5635f96132b2e52227b569e7e480fa55e82d61
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180948"
---
# <a name="create-new-users"></a>Jaunu lietotāju izveide

[!include [task guide banner](../../includes/task-guide-banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Lietotāji ir jūsu organizācijas iekšējie darbinieki vai ārējie debitori un kreditori, kuriem nepieciešama piekļuve sistēmai sava darba veikšanai.

## <a name="associate-a-user-with-a-license-new-license-types-only"></a>Saistīt lietotāju ar licenci (tikai jauni licences veidi)
Attiecībā uz debitoriem, kuriem ir viens no jaunajiem licences tipiem, kas tika pievienoti 2019. oktobrī, lietotājiem jābūt saistītiem ar licenci. Lietotāji, kas ir saistīti ar licenci, tiek automātiski pievienoti kā sistēmas lietotāji, kuriem nav lomas, pirmo reizi pierakstoties sistēmā. Lietotāji, kuri nav saistīti ar licenci, saņem brīdinājuma ziņojumu.

Sistēmas administratori var [piešķirt licences lietotājiem](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) [Microsoft 365 administrēšanas centrā](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).

## <a name="add-a-new-user"></a>Pievienot jaunu lietotāju
1. Dodieties uz **Sistēmas administrēšana \> Lietotāji \> Lietotāji**.
2. Darbību rūtī atlasiet **Jauns**.
3. Laukā **Lietotāja ID** ievadiet lietotāja unikālu identifikatoru. Jānorāda lietotāja ID.  
4. Laukā **Lietotāja vārds** ievadiet lietotāja vārdu.  
5. Laukā **Domēns** ievadiet lietotāja domēnu.  
6. Laukā **Aizstājvārds** ievadiet lietotāja aizstājvārdu.  
7. Laukā **Uzņēmums** atlasiet vēlamo uzņēmumu. 
8. Kopsavilkuma cilnē **Lietotāja lomas** atlasiet **Piešķirt lomas** [piešķirtu lietotājus drošības lomām](assign-users-security-roles.md)
9. Atlasiet **Labi**.
10. Atlasiet **Saglabāt**.

## <a name="import-users"></a>Importēt lietotājus
1. Darbību rūtī atlasiet **Importēt lietotājus**.
2. Sarakstā atzīmējiet atlasīto rindu.
3. Atlasiet **Importēt lietotājus**.
4. Atlasiet **Aizvērt**.

