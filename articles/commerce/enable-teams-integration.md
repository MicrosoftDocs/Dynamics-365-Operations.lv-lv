---
title: Iespējot Dynamics 365 Commerce un Microsoft Teams integrāciju
description: Šajā tēmā ir aprakstīts, kā aktivizēt Microsoft Dynamics 365 Commerce un Microsoft Teams integrāciju.
author: gvrmohanreddy
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dfada577ab97fdb9912c22d2399529f934b25d54
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8695738"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a>Iespējot Dynamics 365 Commerce un Microsoft Teams integrāciju

[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīts, kā aktivizēt Microsoft Dynamics 365 Commerce un Microsoft Teams integrāciju.

Lai nodrošinātu Teams ar informāciju no Dynamics 365 Commerce un sinhronizētu uzdevumu pārvaldības līdzekļus starp Teams un pārdošanas punkta (POS) programmu, ir jāiespējo integrācijas līdzekļi programmā Commerce Headquarters.

> [!NOTE]
> Iespējojot Teams integrāciju, jūs atļaujat koplietot datus ar brigādes grupām. Dati, kas tiek koplietoti ar Teams, var atrasties citā valstī, nevis jūsu Commerce datos, un uz tiem var būt attiecas atšķirīgi saskaņotības standarti. Papildinformāciju par šīm izmaiņām skatiet sadaļā [Microsoft drošības kontroles centrs](https://www.microsoft.com/trust-center). Papildinformāciju par Microsoft konfidencialitātes politikām skatiet [Microsoft Konfidencialitātes paziņojums](https://aka.ms/privacy).

## <a name="enable-teams-integration"></a>Iespējot Teams integrāciju

Lai iespējotu Microsoft Teams integrāciju ar commerce, jums Azure portālā ir jāreģistrē programma Teams ar savu nomnieku.

Lai reģistrētu programmu Teams savam nomniekam Azure portālā, veiciet tālāk norādītās darbības.

1. Veiciet norādītās darbības sadaļā [Ātrais starts: reģistrējiet programmu Microsoft identitātes platformā](/azure/active-directory/develop/quickstart-register-app), lai reģistrētu programmu Teams kopā ar nomnieku Azure portālā.
1. **Cilnē Programmas reģistrācija** atlasiet programmu, kuru izveidojāt iepriekšējā darbībā. Pēc tam cilnē **Autentifikācija** atlasiet Pievienot **platformu**.
1. Dialoglodziņā atlasiet **Web**. Pēc tam laukā **Novirzīšanas** URL ievadiet VIETRĀDI URL formātā **\<HQUrl\>/oauth**. Aizstāt **\<HQUrl\>** ar commerce headquarters url (piemēram, `https://hxennugbjtweufmdeo385f47fadb6aa9a0aos.cloudax.int.dynamics.com/oauth`).
1. **Reģistrētās programmas** pārskata lapā kopējiet Programmas **(klienta) ID** vērtību. Šī vērtība būs jānodrošina, lai nākamajā sadaļā iespējotu Teams integrāciju commerce headquarters.
1. Lai pievienotu klienta noslēpumu [, sekojiet instrukcijām](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret) sadaļā Klienta noslēpums. Pēc tam kopējiet **klienta** slepeno vērtību. Šī vērtība būs jānodrošina, lai nākamajā sadaļā iespējotu Teams integrāciju commerce headquarters.
1. Atlasiet **API atļaujas** un pēc tam **atlasiet Pievienot atļauju**.
1. Dialoglodziņā Pieprasīt **API atļaujas** atlasiet Microsoft grafiks **,** atlasiet Deleģētās atļaujas, **izvērsiet** Grupa, **·** **atlasiet Group.ReadWrite.All** un pēc tam atlasiet **Pievienot atļaujas**.
1. Dialoglodziņā Pieprasīt **API atļaujas** atlasiet Pievienot atļauju, **atlasiet** Microsoft Graph **,** atlasiet Programmu atļaujas, **izvērsiet** Grupa, **·** **atlasiet Group.ReadWrite.All** **un pēc tam atlasiet Pievienot atļaujas.**
1. **Dialoglodziņā Pieprasīt API** atļaujas atlasiet **Pievienot atļauju**. Cilnē API **mans uzņēmums izmanto,** meklējiet mazumtirdzniecības **Microsoft Teams pakalpojumu** un atlasiet to.
1. Atlasiet **Deleģētās atļaujas**, izvērsiet **Uzdevumu publicēšana**, atlasiet **TaskPublising.ReadWrite.All** un pēc tam atlasiet **Pievienot atļaujas**. Papildinformāciju skatiet klienta [programmas konfigurēšana tīmekļa API piekļuvei](/azure/active-directory/develop/quickstart-configure-app-access-web-apis).

Lai iespējotu Teams integrāciju Commerce Headquarters, veiciet tālāk norādītās darbības.

1. Dodieties uz **Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Microsoft Teams integrācijas konfigurēšana**.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Iestatiet opciju **Iespējot Microsoft Teams integrāciju** uz **Jā**.
1. Laukā **Programmas ID** ievadiet lietojumprogrammas **(klienta) ID** vērtību, ko ieguvāt, kad Azure portālā reģistrēāt programmu Brigādes.
1. Laukā **Programmas atslēga ievadiet** slepeno **vērtību,** ko ieguvāt, azure portālā pievienojiet klienta noslēpumu.
1. Darbību rūtī atlasiet **Saglabāt**.

Šajā attēlā parādīts Teams integration konfigurācijas piemērs Commerce Headquarters.

![Grupu integrācijas konfigurācija programmā Commerce Headquarters.](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a>Atspējot Teams integrāciju

Lai atspējotu Microsoft Teams integrāciju Commerce Headquarters, veiciet tālāk norādītās darbības.

1. Dodieties uz **Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Microsoft Teams integrācijas konfigurēšana**.
1. Darbību rūtī atlasiet **Rediģēt**.
3. Iestatiet opciju **Iespējot Microsoft Teams integrāciju** uz **Nē**.
4. Notīriet vērtības no laukiem **Programmas ID** un **Programmas atslēga**.
1. Darbību rūtī atlasiet **Saglabāt**.

> [!NOTE]
> Pēc brigādes integrācijas programmas Commerce deaktivizēšanas POS termināļi vairs nerādīs uzdevumus, kas publicēti no programmas Teams.

## <a name="additional-resources"></a>Papildu resursi

[Dynamics 365 Commerce un Microsoft Teams integrācijas pārskats](commerce-teams-integration.md)

[Nodrošināt Microsoft Teams no Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Sinhronizēt uzdevumu pārvaldību starp Microsoft Teams un Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[Lietotāju lomu pārvaldība Microsoft Teams](manage-user-roles-teams.md)

[Kartējiet veikalus un grupas, ja programmā ir iepriekšējas darba grupas Microsoft Teams](map-stores-existing-teams.md)

[Dynamics 365 Commerce un Microsoft Teams integrācijas BUJ](teams-integration-faq.md)
