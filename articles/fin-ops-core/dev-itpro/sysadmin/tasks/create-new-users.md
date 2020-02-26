---
title: Jaunu lietotāju izveide
description: Lietotāji ir jūsu organizācijas iekšējie darbinieki vai ārējie debitori un kreditori, kuriem nepieciešama piekļuve sistēmai sava darba veikšanai.
author: maertenm
manager: AnnBe
ms.date: 02/06/2020
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
ms.openlocfilehash: 6d884dfe30be5684a90925d4d2d9ab7eebca5b44
ms.sourcegitcommit: 13c4a6f98ccce243d6befde90992aefcf562bdab
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029813"
---
# <a name="create-new-users"></a>Jaunu lietotāju izveide

[!include [task guide banner](../../includes/task-guide-banner.md)]

Lietotāji ir jūsu organizācijas iekšējie darbinieki vai ārējie debitori un kreditori, kuriem nepieciešama piekļuve sistēmai sava darba veikšanai.

## <a name="associate-a-user-with-a-license-new-license-types-only"></a>Saistīt lietotāju ar licenci (tikai jauni licences veidi)
Attiecībā uz debitoriem, kuriem ir viens no jaunajiem licences tipiem, kas tika pievienoti 2019. oktobrī, lietotājiem jābūt saistītiem ar licenci. Lietotāji, kas ir saistīti ar licenci, tiek automātiski pievienoti kā sistēmas lietotāji, kuriem nav lomas, pirmo reizi pierakstoties sistēmā.

Sistēmas administratori var [piešķirt licences lietotājiem](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) [Microsoft 365 administrēšanas centrā](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).

## <a name="associate-an-external-user-with-a-license-new-license-types-only"></a>Saistīt ārējo lietotāju ar licenci (tikai jauni licences veidi)
Lietotāji, kas ir ārēji nomniekam, kurā tika izvietota vide, jānorāda resursdatora nomnieka direktorijā (Azure Active Directory (Azure AD)), lai tiem varētu piešķirt licences. Šie ārējie lietotāji jāpievieno nomniekam Azure AD kā vieslietotāji un pēc tam jāpiešķir atbilstošās licences. Papildinformāciju skatiet [Azure Active Directory B2B sadarbības lietotāju pievienošana Azure portālā](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).

## <a name="add-a-new-user"></a>Pievienot jaunu lietotāju
1. Dodieties uz **Sistēmas administrēšana \> Lietotāji \> Lietotāji**.
2. Darbību rūtī atlasiet **Jauns**.
3. Laukā **Lietotāja ID** ievadiet lietotāja unikālu identifikatoru. Jānorāda lietotāja ID.  
4. Laukā **Lietotāja vārds** ievadiet lietotāja vārdu.  
5. Laukā **Domēns** ievadiet lietotāja domēnu.  
6. Laukā **Aizstājvārds** ievadiet lietotāja aizstājvārdu.  
7. Laukā **Uzņēmums** atlasiet vēlamo uzņēmumu. 
8. Kopsavilkuma cilnē **Lietotāja lomas** atlasiet **Piešķirt lomas**, lai pieškirtu lietotājus drošības lomām. Plašāku informāciju skatiet [Lietotāju piešķiršana drošības lomām](assign-users-security-roles.md).
9. Atlasiet **Labi**.
10. Atlasiet **Saglabāt**.

## <a name="import-users"></a>Importēt lietotājus
1. Darbību rūtī atlasiet **Importēt lietotājus**.
2. Sarakstā atzīmējiet atlasīto rindu.
3. Atlasiet **Importēt lietotājus**.
4. Atlasiet **Aizvērt**.

