---
title: E-pasta iestatījumu konfigurēšana programmā Attract
description: Šajā tēmā ir paskaidrots, kā konfigurēt iestatījumus e-pasta ziņojumiem, kas tiek nosūtīti, izmantojot Microsoft Dynamics 365 Talent - Attract.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: e641e3f0d1873d91be1a1dc9bc22eb734a2b21d5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461846"
---
# <a name="configure-email-settings-in-attract"></a>E-pasta iestatījumu konfigurēšana programmā Attract

[!include [banner](includes/banner.md)]

Jūsu zīmols nosaka uzticēšanos un palīdz veidot attiecības ar kandidātiem, pirms viņi vēl ir paspējuši pieteikties jūsu izsludinātajiem amatiem. Pozitīva zīmola uztvere piesaista labākos talantus un pastiprina esošo darbinieku lojalitāti. Microsoft Dynamics 365 Talent: Attract ļauj konfigurēt e-pasta ziņojumus tā, lai tie atspoguļotu jūsu uzņēmuma zīmolu. Tādējādi varat nodrošināt konsekventu pieredzi darba kandidātiem visa atlases procesa gaitā.

Izmantojot Attract, varat veikt tālāk norādītās darbības.

- Konfigurējiet e-pasta iestatījumus, lai tiktu izmantots jūsu uzņēmuma Microsoft Exchange e-pasta pakalpojumu konts. Šādā veidā kandidāti zinās, ka e-pasta ziņojumi nāk no jūsu uzņēmuma. Piemēram, varat konfigurēt iestatījumus tā, lai kandidāti saņemtu e-pasta ziņojumus no adreses `recruiting@contoso.com`, nevis no `contoso@microsoft.com`.
- Nodrošiniet konsekventu zīmolradi visos e-pasta ziņojumos, iestatot globālo galveni un kājeni e-pasta veidnēm. 

> [!NOTE]
> Lai konfigurētu programmu Attract tā, lai tā e-pasta ziņojumu sūtīšanai izmantotu jūsu uzņēmuma e-pasta pakalpojumu kontu, ir nepieciešams visaptverošais darbā pieņemšanas papildinājums.

## <a name="connect-an-email-service-account"></a>E-pasta pakalpojumu konta pievienošana

Pievienojot uzņēmuma e-pasta pakalpojumu kontu, varat izveidot zīmolam pielāgotus e-pasta ziņojumus sarakstei ar darba kandidātiem. Ja nepievienojat sava uzņēmuma kontu, programma Attract izmanto noklusējuma Microsoft zīmola e-pasta pakalpojumu kontu.

1. Atlasiet **Iestatījumi** (zobrata simbols augšējā labajā stūrī) un pēc tam atlasiet **Administrēšanas centrs**.
2. Cilnes **E-pasta iestatījumi** sadaļā **E-pasta pakalpojumu konti** atlasiet **Pievienot uzņēmuma kontu**.

    ![Uzņēmuma e-pasta pakalpojumu konta pievienošana programmā Attract](./media/attract-admin-email-service-accounts.png)

    Plašāku informāciju par to, kā izveidot kopīgotu e-pasta kontu, skatiet tēmā [Koplietojamās pastkastes pakalpojumā Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).

3. Microsoft pierakstīšanās logā pierakstieties, izmantojot uzņēmuma akreditācijas datus.
4. Ja vēl neesat iestatījis e-pasta pakalpojumu kontu vai vēlaties pievienot jaunu, atlasiet **Pievienot jaunu pakalpojumu kontu** un pēc tam ievadiet e-pasta informāciju. Ja esat jau iestatījis e-pasta pakalpojumu kontu, ko vēlaties izmantot, atlasiet to.

Kad jūsu e-pasta pakalpojumu konts ir veiksmīgi konfigurēts, tas tiek rādīts sadaļā **E-pasta pakalpojumu konti**.

## <a name="disconnect-an-email-service-account"></a>E-pasta pakalpojumu konta atvienošana

Ja vēlaties pārtraukt sava uzņēmuma domēna izmantošanu e-pasta sarakstē programmā Attract, varat atvienot e-pasta pakalpojumu kontu.

1. Atlasiet **Iestatījumi** (zobrata simbols augšējā labajā stūrī) un pēc tam atlasiet **Administrēšanas centrs**.
2. Cilnes **E-pasta iestatījumi** sadaļā **E-pasta pakalpojumu konti** atlasiet pogu **Vairāk** (trīs vertikālie punkti) blakus e-pasta pakalpojumu kontam, ko vēlaties atvienot.
3. Atlasiet **Atvienot e-pasta kontu**.

    ![Uzņēmuma e-pasta pakalpojumu konta atvienošana](./media/attract-admin-disconnect-email-account.png)

4. Kad tiek parādīta uzvedne ar aicinājumu apstiprināt operāciju, atlasiet **Atvienot**.

    ![Uzņēmuma e-pasta pakalpojumu konta atvienošanas apstiprināšana](./media/attract-admin-email-confirm-disconnect.png)

Ja nepievienojat citu e-pasta pakalpojumu kontu, e-pasta ziņojumu sūtīšanai no programmas Attract tiek izmantots noklusējuma Microsoft zīmola e-pasta pakalpojumu konts.

## <a name="configure-email-template-settings"></a>E-pasta veidnes iestatījumu konfigurēšana

Varat augšupielādēt sava uzņēmuma logotipa attēlu vai citu informāciju kā zīmola galveni uzņēmuma e-pasta ziņojumiem. E-pasta kājenē varat arī norādīt saites uz konfidencialitātes politiku un lietošanas nosacījumiem.

> [!NOTE]
> Jums ir jāievēro visi piemērojamie jūsu valsts vai reģiona tiesību akti, kā arī e-pasta adresātam piemērojamie valsts vai reģiona tiesību akti. Tostarp jāievēro arī surogātpasta ierobežošanas noteikumi.

1. Atlasiet **Iestatījumi** (zobrata simbols augšējā labajā stūrī) un pēc tam atlasiet **Administrēšanas centrs**.
2. Cilnes **E-pasta iestatījumi** sadaļā **E-pasta veidnes iestatījumi** ievelciet attēlu, kuru vēlaties izmantot kā e-pasta galveni, attēlu lodziņā vai noklikšķiniet uz attēlu lodziņa, lai pārlūkotu failu. Lai aizstātu jau esošu attēlu, vispirms atlasiet opciju **Noņemt** blakus attēlam. Attēlam ir jābūt JPEG, JPG, PNG vai SVG failam. Ieteicamais attēlu lielums ir no 25 līdz 800 pikseļiem platumā un no 25 līdz 150 pikseļiem augstumā. Maksimālais galvenes faila lielums ir 1 megabaits (MB).

    ![Uzņēmuma e-pasta galvenes attēla pievienošana](./media/attract-admin-email-header.png)

3. Sadaļā **Jūsu konfidencialitātes politika saziņai** norādiet saiti uz jūsu uzņēmuma konfidencialitātes politiku. Sadaļā **Jūsu noteikumi un nosacījumi komunikācijai** norādiet saiti uz jūsu uzņēmuma lietošanas nosacījumiem.

    ![Saišu pievienošana uz uzņēmuma konfidencialitātes politiku un lietošanas nosacījumiem izmantošanai e-pasta kājenē](./media/attract-admin-email-footer.png)

4. Atlasiet **Saglabāt**, lai saglabātu e-pasta veidnes iestatījumus.


[!INCLUDE[footer-include](../includes/footer-banner.md)]