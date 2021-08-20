---
title: Darījumu e-pasta ziņojumu pielāgošana pēc piegādes veida
description: Šajā tēmā aprakstīts, kā iestatīt pielāgotas e-pasta veidnes konkrētiem paziņojumu veidiem un piegādes veidiem risinājumā Microsoft Dynamics 365 Commerce.
author: stuharg
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: d15e7c5c7050ad373cb45da72de59416e85a5f2034f7a11b007d497b2e2b98bd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6749911"
---
# <a name="customize-transactional-emails-by-mode-of-delivery"></a>Darbību e-pasta ziņojumu pielāgošana pēc piegādes veida

[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīts, kā iestatīt pielāgotas e-pasta veidnes konkrētiem paziņojumu veidiem un piegādes veidiem risinājumā Microsoft Dynamics 365 Commerce.

Transakciju e-pasta vēstules tagad var tikt pielāgotas kombinācijai no paziņojuma veida (piemēram, **Pasūtījums izveidots**, **Pasūtījums iepakots** vai **Pasūtījumam ir izrakstīts rēķins**) un piegādes veida (piemēram, pa nakti, savākšana no veikala vai savākšana ietves malā). Pielāgoti transakciju e-pasta ziņojumi ļauj mazumtirgotājiem nodrošināt saviem klientiem pasūtījumu izpildi, kas ir pielāgota pasūtījuma piegādes veidam. Piemēram, "pasūtījums iepakots" notikums var tikt pielāgots, lai tas nodrošinātu saņemšanas ietves malā instrukcijas debitoriem, kuri izvēlas savākšanu ietves malā. Tā var arī sniegt informāciju par pārvadājumu pārvadātāju un piegādi klientiem, kuri izvēlas nosūtīt pasūtījumu.

> [!NOTE]
> Lai izmantotu funkcionalitāti pielāgotajiem transakciju e-pastiem, vispirms ir jāieslēdz līdzeklis **Transakciju e-pasta veidņu pielāgošana pēc piegādes veida**, dodoties uz **Darbvietas \> Līdzekļu pārvaldība** programmā Commerce Headquarters.

E-pasta ziņojumus var pielāgot pēc piegādes veida šādos paziņojuma tipos:

- **Pasūtījuma atcelšana** — Šis e-pasta paziņojuma tips ir jauns.
- **Pasūtījums izveidots**
- **Pasūtījums apstiprināts**
- **Pasūtījumam ir izrakstīts rēķins** — Šis e-pasta paziņojuma tips ir jauns. To var izmantot, paziņojuma tipa **Pasūtījuma nosūtīts** vietā, kas nosūtīs paziņojumu jebkuram rēķina notikumam, kuram ir nosūtīšanas piegādes veids (nevis saņemšanas, izpildes vai elektroniskais piegādes veids).
- **Pasūtījums saņemts**
- **Pasūtījums iepakots**
- **Pasūtījums sagatavots savākšanai** – šo paziņojuma tipu var pielāgot piegādes veidam tikai tad, ja ir ieslēgts līdzeklis **Vairāku saņemšanas piegādes režīmu atbalsts**. Šādā gadījumā šis paziņojuma tips ir funkcionāli līdzvērtīgs paziņojuma tipam **Pasūtījuma iepakots**.
- **Maksājums neizdevās**
- **Izveidots aizstāšanas pasūtījums**

## <a name="configure-email-templates-for-specific-modes-of-delivery"></a>Konfigurēt e-pasta veidnes noteiktiem piegādes veidiem

Šai procedūrai pieņēmums ir tāds, ka jūs jau esat izveidojis jaunas, pielāgotas e-pasta veidnes un pievienojis tās lapai **Organizācijas e-pasta veidnes**. Informāciju par e-pasta veidņu izveidi un augšupielādi skatiet [E-pasta veidņu izveide transakciju notikumiem](email-templates-transactions.md).

Lai konfigurētu e-pasta veidnes noteiktiem piegādes veidiem programmā Commerce Headquarters, veiciet tālāk norādītās darbības.

1. Dodieties uz **Komercijas e-pasta paziņojumu profils**.
1. Sadaļā **Mazumtirdzniecības notikumu paziņojumu iestatījumi** atlasiet esošu paziņojuma tipu.
1. Kamēr paziņojuma tips joprojām ir atlasīts, izvēlieties **Konfigurēt piegādes veidus**.
1. Dialoglodziņā **Piegādes veidi** atlasiet **Jauns**.
1. Jaunajā rindā, laukā **Piegādes veids** atlasiet piegādes veidu.
1. Laukā **E-pasta ID** atlasiet e-pasta veidni, ko kartēt uz piegādes veidu.
1. Atzīmējiet izvēles rūtiņu **Aktivizēt**.
1. Atkārtojiet 4. un 7. soli, lai pievienotu citus piegādes veidus.
1. Pēc pabeigšanas atlasiet **Labi**.

> [!NOTE]
> - Kad pārdošanas pasūtījuma rindās ir vairāk nekā viens piegādes veids, tiks izmantota noklusējuma veidne. Noklusējuma veidne ir veidne, kas ir kartēta paziņojuma veidam lapā **Komercijas e-pasta paziņojuma profils**.
> - Ja pārdošanas pasūtījumam ir piegādes veids, kas nav konfigurēts pielāgotai e-pasta veidnei, tiks izmantota noklusējuma e-pasta veidne.

## <a name="additional-resources"></a>Papildu resursi

[Zvanu centra pasūtījumu izveide](tasks/create-call-center-orders.md)

[Piegādes veida mainīšana programmā POS](pos-change-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]