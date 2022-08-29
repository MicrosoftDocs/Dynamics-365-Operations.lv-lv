---
title: E-pasta paziņojumu profila iestatīšana
description: Šajā rakstā ir aprakstīts, kā izveidot e-pasta paziņojuma profilu Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: db6c46d471e3b54982132df3e4819236833cf4a8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292140"
---
# <a name="set-up-an-email-notification-profile"></a>E-pasta paziņojumu profila iestatīšana

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā izveidot e-pasta paziņojuma profilu Microsoft Dynamics 365 Commerce.

Veidojot kanālus, varat iestatīt e-pasta paziņojuma profilu. E-pasta paziņojuma profils nosaka pārdošanas darbības notikumus (piemēram, izveidotais pasūtījums, iepakotais pasūtījums un pasūtījuma rēķinos iekļautais notikums), par kuru jums tiks sūtīti paziņojumi saviem debitoriem. 

Papildinformāciju par e-pasta ziņojumu konfigurēšanu skatiet rakstā [E-pasta ziņojumu konfigurēšana un sūtīšana](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).



## <a name="create-an-email-template"></a>E-pasta veidnes izveidošana

Lai iespējotu e-pasta paziņojuma veidu, programmā Commerce headquarters ir jāizveido organizācijas e-pasta veidne katram paziņojuma veidam, kuru vēlaties atbalstīt. Šī veidne definē e-pasta tēmu, sūtītāju, noklusējuma valodu un e-pasta pamattekstu katrai atbalstītajā valodā.

Lai izveidotu e-pasta veidni, izpildiet tālāk norādītās darbības.

1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi \> Mazumtirdzniecība un komercija \> Headquarters iestatīšana \> Parametri \> Organizāciju e-pasta veidnes**.
1. Darbību rūtī atlasiet **Jauns**.
1. Laukā **E-pasta ID** ievadiet ID, lai palīdzētu identificēt šo veidni.
1. Laukā **Sūtītāja nosaukums** ievadiet sūtītāja nosaukumu.
1. Ievadiet jēgpilnu aprakstu laukā **Epasta apraksts**.
1. Laukā **Sūtītāja e-pasta adrese** ievadiet sūtītāju e-pasta adresi.
1. Sadaļā **Vispārīgi** atlasiet noklusējuma valodu e-pasta veidnei. Noklusējuma valoda tiks lietota, ja norādītajai valodai nav lokalizētas veidnes.
1. Paplašiniet sadaļu **E-pasta ziņojuma saturs** un atlasiet **Jauns**, lai izveidotu veidnes saturu. Katram satura vienumam atlasiet valodu un norādiet e-pasta tēmas rindu. Ja e-pasta ziņojumā būs pamatteksts, pārliecinieties, ir atzīmēta izvēles rūtiņa **Ir pamatteksts**.
1. Darbības rūtī atlasiet **E-pasta ziņojums**, lai nodrošinātu e-pasta pamatteksta veidni.

Tālāk redzamajā attēlā parādīti daži e-pasta veidnes iestatījumi.

![E-pasta veidņu iestatījumi.](media/email-template.png)

Papildinformāciju par e-pasta veidņu izveidi skatiet sadaļā [E-pasta veidņu izveide darbību notikumiem](email-templates-transactions.md). 

## <a name="create-an-email-notification-profile"></a>E-pasta paziņojumu profila izveide

Lai programmā programmā izveidotu e-pasta paziņojuma profilu, izpildiet šīs darbības.

1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi \> Mazumtirdzniecība un komercija \> Headquarters iestatīšana \> Komercijas e-pasta paziņojumu profils**.
1. Darbību rūtī atlasiet **Jauns**.
1. Lai identificētu profilu, ievadiet nosaukumu laukā **E-pasta paziņojumu profils**.
1. Ievadiet atbilstošu aprakstu laukā **Apraksts**.
1. Iestatiet slēdzi **Aktīvs** uz **Jā**.

## <a name="add-a-notification-type"></a>Pievienot paziņojuma veidu

Lai izveidotu e-pasta notikumu, izpildiet tālāk norādītās darbības.

1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi \> Mazumtirdzniecība un komercija \> Headquarters iestatīšana \> Komercijas e-pasta paziņojumu profils**.
1. Sadaļā **Mazumtirdzniecības e-pasta paziņojumu** iestatījumi atlasiet **Jauns**.
1. Nolaižamajā sarakstā atlasiet atbilstošu **E-pasta paziņojumu veidu**.
1. Atlasiet e-pasta ziņojuma veidni, kuru izveidojāt augstāk no nolaižamā **saraksta E-pasta ID**.
1. Atzīmējiet **izvēles rūtiņu** Aktīvs.
1. Darbību rūtī atlasiet **Saglabāt**.

Tālāk redzamajā attēlā parādīti daži notikuma paziņojumu iestatījumi.

![Notikuma paziņojuma iestatījumi.](media/email-notification-profile.png)


## <a name="schedule-a-recurring-email-notification-process-job"></a>Plānot periodisku e-pasta paziņojumu apstrādes darbu

Lai sūtītu e-pasta paziņojumus, ir jādarbojas mazumtirdzniecības **pasūtījuma e-pasta paziņojumu procesa** darbam.

Lai programmā iestatītu pakešuzdevumu darbību e-pasta ziņojumu sūtīšanai, izpildiet šīs darbības.

1. E-pasta ziņojumu un paziņojumu sūtīšana uz e-pasta ziņojumu sūtīt e-pasta **ziņojumu, pārejiet \> uz Retail un Commerce \> Retail un Commerce IT \>**.
1. **Procesa mazumtirdzniecības pasūtījuma e-pasta** paziņojuma dialoglodziņā atlasiet **Periodiskums**.
1. Dialoglodziņā Definēt **atkārtošanos** atlasiet Bez **beigu datuma**.
1. Sadaļā **Periodiskuma** modelis atlasiet **Minūtes** un pēc tam lauku Skaits **iestatiet** uz **1**. Šie iestatījumi nodrošina to, ka e-pasta paziņojumi tiek apstrādāti pēc iespējas ātrāk.
1. Atlasiet Labi **,** lai atgrieztos mazumtirdzniecības **pasūtījuma e-pasta paziņojuma dialoglodziņā** Apstrādāt.
1. Atlasiet **Labi,** lai pabeigtu darba iestatīšanu.

## <a name="next-steps"></a>Turpmākās darbības

Pirms e-pasta ziņojumu nosūtīšanas jums ir jākonfigurē izejošo pasta pakalpojumu. Papildinformāciju skatiet [E-pasta konfigurēšana un sūtīšana](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).

## <a name="additional-resources"></a>Papildu resursi

[E-pasta konfigurēšana un sūtīšana](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[Kanālu apskats](channels-overview.md)

[Kanālu iestatīšanas priekšnosacījumi](channels-prerequisites.md)

[Organizācijas un organizāciju hierarhiju pārskats](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
