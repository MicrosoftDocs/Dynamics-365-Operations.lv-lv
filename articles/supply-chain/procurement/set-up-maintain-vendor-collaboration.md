---
title: Kreditoru sadarbības iestatīšana un uzturēšana
description: Šajā tēmā ir izskaidrots, kā iestatīt piegādātāju sadarbību Dynamics 365 Supply Chain Management. Tajā skaidrots arī, kā nodrošināt jaunus piegādātāju sadarbības lietotājus un pārvaldīt šo lietotāju drošības lomas.
author: Henrikan
ms.date: 12/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DirExternalRole, SysUserRequestListPage, VendVendorPortalUsers, WorkflowTableListPageRnr
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: 220774
ms.assetid: 69d05e8b-7dc2-48ea-bc24-bea9ac963579
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b635255fffa6fd3c6612cd248dc692df204aa76d
ms.sourcegitcommit: 614d79cba238e466d445767a7d0a012e785a9861
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/19/2021
ms.locfileid: "7652041"
---
# <a name="set-up-and-maintain-vendor-collaboration"></a>Kreditoru sadarbības iestatīšana un uzturēšana

[!include [banner](../includes/banner.md)]

Kreditoru sadarbības interfeiss sniedz ierobežotu informācijas kopumu par ārējo piegādātāja lietotāju pirkšanas pasūtījumiem, rēķiniem un sūtījumu krājumiem. No šī interfeisa piegādātājs var arī atbildēt uz piedāvājuma pieprasījumiem (PP) un skatīt un rediģēt pamata uzņēmuma informāciju.

Šajā tēmā ir izskaidrots, kā iestatīt piegādātāju sadarbību Dynamics 365 Supply Chain Management. Tajā skaidrots arī, kā iestatīt darbplūsmu tā, lai tā nodrošinātu jaunus piegādātāja sadarbības lietotājus un kā pārvaldīt šo lietotāju drošības lomas.

> [!NOTE]
> Informācija par drošības lomu iestatījumiem piegādātāju sadarbībai attiecas tikai uz pašreizējo sistēmas Finance and Operations versiju. Programmā Microsoft Dynamics AX 7.0 (2016. gada februāris) un Microsoft Dynamics AX programmas versijā 7.0.1 (2016. gada maijs) jūs ar kreditoriem sadarbojaties, izmantojot moduli **Kreditoru portāls**. Papildinformāciju par lietotāju atļaujām Piegādātāju portālam Microsoft Dynamics AX skatiet sadaļā [Piegādātāju portāla lietotāja drošība](configure-security-vendor-portal-users.md).

## <a name="set-up-vendor-collaboration-security-roles"></a>Piegādātāju sadarbības drošības lomu iestatīšana

Sagādes profesionālis vai piegādātājs, kam ir pietiekamas atļaujas, var pieprasīt, lai kontaktpersona tiktu nodrošināta kā lietotājs, iespējojot **Nodrošināt piegādātāja lietotāju** kontaktpersonas ierakstā. Nodrošinājuma procesa laikā lietotāja atļaujas tiek atlasītas jaunajam ārējam lietotājam, un tiek iesniegts jaunā piegādātāja lietotāja pieprasījums. Ir svarīgi pareizi iestatīt lietotāja atļaujas, kas ir pieejamas atlasei piegādātāja lietotāja pieprasījumā. Pretējā gadījumā piegādātājiem var piešķirt piekļuvi informācijai, kas tiem nedrīkst būt pieejama Supply Chain Management.

### <a name="set-up-the-security-roles-that-are-available-for-selection-when-a-new-user-request-is-used-for-a-contact-person"></a>Iestatīt drošības lomas, kas ir pieejamas atlasei, ja kontaktpersonai tiek izmantots jauna lietotāja pieprasījums

1. Atlasiet **Sistēmas administrēšana** &gt; **Drošība** &gt; **Ārējās lomas**.
2. Atlasiet **Jauns**, tad atlasiet drošības lomu un puses lomu **Piegādātājs**.

Iespējams, vēlēsieties pievienot Supply Chain Management sniegtās **Piegādātāja administrators (ārējā)** un **Piegādātājs (ārējā)** lomas. Alternatīvi jūs varat izmantot jūsu uzņēmuma izveidotās drošības lomas.

Loma **Piegādātāja administrators (ārējā)** ir jāpadara pieejama tikai tad, ja piegādātājam vajadzētu būt iespējai izveidot jaunas kontaktpersonas, iesniegt kreditoru sadarbības lietotāju pieprasījumus jauniem lietotājiem un izmaiņas lietotāja informācijā un apstrādāt šos pieprasījumus, izmantojot darbplūsmu.

Ja plānojat manuāli iestatīt piegādātāju kontaktpersonas un lietotājus, varat padarīt pieejamu tikai **Piegādātāja (ārējo) lomu**. Tad šī loma ir vienīgā loma, ko var pieprasīt ar piegādātāja lietotāja pieprasījumu.

> [!NOTE]
> Kad manuāli izveidojat jaunu lietotāja kontu, tiek automātiski piešķirta loma **SystemUser**. Tāpēc jums ir jānoņem šī loma un jāpiešķir **SystemExternalUser** loma. Ja jauni lietotāju konti tiek izveidoti, izmantojot darbplūsmu, ko inicializē piegādātāja lietotāja pieprasījums nodrošināt jaunu lietotāju, tiks piešķirta viena vai vairākas lomas, kas iestatītas piegādātāju sadarbībai, un loma **SystemExternalUser**.

#### <a name="vendor-admin-external-security-role"></a>Piegādātāja administratora (ārēja) drošības loma

Lomu **Piegādātāja administrators (ārējā)** var lietot ārējiem piegādātājiem, kas uztur piegādātāja kontaktinformāciju un pieprasa nodrošināt jaunus piegādātāju sadarbības lietotājus. Ārējie lietotāji ar šo drošības lomu var veikt šādus uzdevumus:

- Skatīt un modificēt kontaktpersonas informāciju, piemēram, personas nosaukumu, e-pasta adresi un tālruņa numuru.
- Pievienot jaunu vai esošu kontaktpersonu piegādātāju kontiem, kam viņi ir kontaktpersona.
- Dzēst jebkuru kontaktpersonu, ko viņi izveidojuši.
- Aktivizēt vai deaktivizēt saistību starp kontaktpersonu un piegādātāja kontu. Pēc saistības starp kontaktpersonu un piegādātāja kontu deaktivizēšanas, kontaktpersonu nevar izmantot jauniem pirkšanas pasūtījumiem vai citiem dokumentiem.
- Liegt vai atļaut kontaktpersonas piekļuvi dokumentiem piegādātāja sadarbības interfeisā, kas ir specifiski piegādātāja kontam. Kad saistība starp kontaktpersonu un piegādātāja kontu ir deaktivizēta, piekļuve piegādātāja kontam raksturīgajiem dokumentiem vienmēr tiek liegta.
- Pieprasīt jaunu lietotāja kontu kontaktpersonai, izmantojot darbību **Uzkrājumu lietotājs**.
- Pieprasīt, lai kontaktpersonas lietotāja konts tiktu deaktivizēts.
- Pieprasīt, lai kontaktpersonas lietotāja konts tiktu modificēts, lai pievienotu vai noņemtu drošības lomas.
- Apskatīt PP.

#### <a name="vendor-external-security-role"></a>Piegādātājs (ārēja) drošības loma

Lomu **Piegādātājs (ārējā)** var izmantot ārējiem piegādātājiem, kas darbosies ar pirkšanas pasūtījumiem. Ārējie lietotāji ar šo drošības lomu var veikt šādus uzdevumus:

- Atbildēt uz un skatīt informāciju par pirkšanas pasūtījumiem.
- Uzturēt kreditora sadarbības rēķinus.
- Skatīt sūtījuma krājumus.
- Skatiet un atbildiet uz PP.
- Apskatīt informāciju par piegādātāju.

## <a name="set-up-security-roles-that-are-used-when-prospective-vendors-are-onboarded"></a>Iestatīt drošības lomas, kas tiek izmantotas, kad tiek izmantoti potenciālie piegādātāji

Uzņēmuma piegādātājiem, kas tiek uzsākti ar potenciālā piegādātāja reģistrācijas pieprasījuma starpniecību, jums ir jāiestata ārējas drošības loma. Šī loma tiks piešķirta jauniem lietotājiem nodrošinājuma procesa laikā, ko kontrolē darbplūsma ar **Lietotāja pieprasījuma darbplūsma (platforma)** tipu. Papildinformāciju skatiet tālāk šīs tēmas sadaļā [Iestatīt darbplūsmas, lai apstrādātu piegādātāju sadarbības lietotāju pieprasījumus](#set-up-workflows-to-process-vendor-collaboration-user-requests).

Informāciju par to, kā pievienot potenciālos piegādātājus, skatiet sadaļā [Pievienot piegādātājus](vendor-onboarding.md).

### <a name="set-up-a-security-role-that-is-used-when-a-new-prospective-vendor-user-request-is-submitted"></a>Iestatīt drošības lomu, kas tiek izmantota, kad tiek iesniegts jauns potenciālā piegādātāja lietotāja pieprasījums

1. Atlasiet **Sistēmas administrēšana** > **Drošība** > **Ārējās lomas**.
2. Atlasiet **Jauns**, tad atlasiet drošības lomu un puses lomu **Potenciālais piegādātājs**.

Jums jāpievieno **Piegādātāja potenciālā klienta (ārēja)** loma, kas tiek nodrošināta Supply Chain Management.

Drošības loma piešķirs piekļuvi tikai jaunā piegādātāja reģistrācijas ceļvedim.

## <a name="set-up-workflows-to-process-vendor-collaboration-user-requests"></a>Iestatīt darbplūsmas, lai apstrādātu piegādātāju sadarbības lietotāju pieprasījumus

Lai palīdzētu nodrošināt, ka visi atbilstošie uzdevumi ir pabeigti un ka tiek sniegti atbilstošie apstiprinājumi, jāiestata darbplūsmas, lai rīkotos ar piegādātāju sadarbības lietotāju pieprasījumiem.

Piegādātāju sadarbības lietotāja pieprasījumus iesniedz vai nu ārējie piegādātāji, kuriem ir **Piegādātāja administratora (ārēja)** drošības loma, vai līdzīgas atļaujas, vai sagādes profesionāļi jūsu uzņēmumā. Tos var arī ģenerēt no potenciālā piegādātāja reģistrācijas pieprasījumiem piegādātāja reģistrācijas procesa laikā.

Ir pieejami trīs piepresījumu veidi.

- Pieprasījumi nodrošināt jaunu lietotāju
- Pieprasījumi deaktivizēt esošu lietotāju
- Pieprasījumi modificēt esoša lietotāja drošības lomas

Papildinformāciju par jauna piegādātāja sadarbības lietotāju pieprasījumiem, skatiet tēmā [Pārvaldīt piegādātāju sadarbības lietotājus](manage-vendor-collaboration-users.md).

Lai apstrādātu visus trīs piegādātāju sadarbības lietotāja pieprasījumus, ir jāizveido divas vai vairākas darbplūsmas. Jaunas darbplūsmas tiek izveidotas **Lietotāju darbplūsmu** lapā.

### <a name="example-of-a-workflow-for-provisioning-new-users-and-modifying-security-roles"></a>Darbplūsmas piemērs jaunu lietotāju nodrošinājumam un drošības lomu modificēšanai

Lai apstrādātu piegādātāja lietotāja pieprasījumus izveidot jaunus lietotājus un modificēt drošības lomas, darbplūsmas sākumā varat iestatīt zarošanas nosacījumu. Šādā veidā tiek izmantots cits darbplūsmas atzars atkarībā no tā, vai pieprasījums ir izveidot jaunu lietotāju vai pārveidot esošo lietotāju.

Lai iestatītu šo zarošanu, izveidojiet jaunu darbplūsmas tipu **Lietotāja pieprasījuma darbplūsma (Platforma)**. Šīs darbplūsmas atzaros var būt šādi elementi.

#### <a name="branch-to-provision-new-users"></a>Zars jaunu lietotāju nodrošināšanai

1. Piešķirt apstiprinājuma uzdevumu personai, kura ir atbildīga par jaunu lietotāju apstiprināšanu, ka piešķirt piekļuvi piegādātāja sadarbības informācijai.
2. Piešķiriet uzdevumu personai, kas ir atbildīga par jaunu Microsoft Azure Active Directory (Azure AD) lietotāju kontu pieprasīšanu Azure portālā. Izmantojiet iepriekš definēto **Sūtīt Azure B2B lietotāja uzaicinājumu** uzdevumu šai darbībai. B2B lietotājus var automātiski eksportēt Azure AD. Izmantojiet iepriekš definēto **Uzkrājumu Azure AD B2B lietotāju**. Papildinformāciju skatiet sadaļā [B2B lietotāju eksportēšana Azure AD](../../fin-ops-core/dev-itpro/sysadmin/implement-b2b.md).
3. Piešķiriet apstiprinājuma uzdevumu personai, kas tiek augšupielādēta pakalpojumā Azure. Ja konts nav veiksmīgi izveidots, šī persona noraida uzdevumu un beigs darbplūsmu. Šo apstiprināšanas uzdevumu var izlaist, ja esat ietveris darbību, kas automātiski eksportē jaunos lietotāja kontus uz Azure, izmantojot B2B programmas programmēšanas interfeisu (API).
4. Pievienojiet automatizētu uzdevumu, kas nodrošina jaunu lietotāju. Izmantojiet iepriekš definēto **Automātiskās nodrošināšanas lietotājs** uzdevumu šai darbībai.
5. Pievienojiet uzdevumu, kas informē jauno lietotāju. Jūs, iespējams, vēlēsieties nosūtīt jaunajam lietotājam sveiciena e-pastu, kurā ir iekļauts URL Supply Chain Management. Šajā e-pasta ziņojumā var izmantot **E-pasta ziņojumu** lapā izveidoto veidni un pēc tam atlasīt lapā **Lietotāja darbplūsmas parametri**. Veidnē var būt ietverta **%portalURL%** etiķete. Kad tiek ģenerēts sveiciena e-pasta ziņojums, šis tags tiks aizstāts ar Supply Chain Management nomnieka vietrādi URL.

    > [!NOTE]
    > Šo darbplūsmu var izmantot vairākos scenārijos, kuros ir iesaistīts lietotājs, kurš to ietver. Piemēram, to var izmantot, kad potenciālajiem piegādātājiem vai kontaktpersonām nepieciešams piegādātāja sadarbības konts. Tāpēc e-pastu vajadzētu uzskatīt par vispārēju pārskatu, ko var izmantot vairākiem nolūkiem.

#### <a name="branch-to-modify-security-roles"></a>Zars drošības lomu modificēšanai

1. Piešķirt apstiprinājuma uzdevumu personai, kura ir atbildīga par drošības lomu izmaiņu apstiprināšanu.
2. Pievienojiet automatizētu uzdevumu, kas pievieno vai noņem atbilstošās drošības lomas. Izmantojiet **Automātiskās nodrošināšanas lietotājs** uzdevumu šai darbībai.

### <a name="example-of-a-workflow-for-inactivating-a-user"></a>Darbplūsmas piemērs lietotāja deaktivizēšanai

Izveidojiet **Deaktivizēšanas lietotāju pieprasījumu darbplūsmas platformas** tipa darbplūsmu un pēc tam pievienojiet šādus uzdevumus.

1. Piešķirt apstiprinājuma uzdevumu personai, kura ir atbildīga par pieprasījumu pieņemšanu, lai deaktivizētu lietotājus. Varat pievienot nosacījumus, lai automatizētu šo apstiprināšanas darbību.
2. Pievienojiet automatizētu uzdevumu, kas deaktivizē lietotāju. Izmantojiet **Automātiska lietotāja deaktivizācija** uzdevumu šai darbībai.
3. Pievienojiet visus nepieciešamos tīrīšanas uzdevumus. Piemēram, varat pievienot uzdevumu, kas noņem kontu no jūsu direktorija Azure portālā.

## <a name="enable-vendor-collaboration-for-a-specific-vendor"></a>Iespējot kreditoru sadarbību konkrētam kreditoram

Pirms kādam kreditoru sadarbības lietotājam izveidot lietotāja kontu, jāiestata kreditors tā, lai tas varētu izmantot kreditoru sadarbību. Lapas **Kreditori** cilnē **Vispārīgi** iestatiet lauku **Sadarbības aktivizēšana**. Pieejamas šādas opcijas:

- **Aktīvs (PP tiek akceptēts automātiski)** – ja kreditors pirkšanas pasūtījumus pieņem bez izmaiņu pieprasījuma, šie pirkšanas pasūtījumi tiek akceptēti automātiski.
- **Aktīvs (pirkšanas pasūtījums netiek akceptēts automātiski)** — kad kreditors ir pieņēmis pirkšanas pasūtījumus, jūsu organizācijai šie pirkšanas pasūtījumi ir jāakceptē manuāli.

> [!NOTE]
> Šo uzdevumu var izpildīt arī sagādes profesionāļi jūsu uzņēmumā.

## <a name="troubleshoot-the-provisioning-of-new-vendor-collaboration-users"></a>Novērst problēmu saistībā ar jaunu kreditoru sadarbības lietotāju nodrošināšanu

Jauni kreditoru sadarbības lietotāji tiek nodrošināti, izmantojot darbplūsmu, kuru iestatāt, lai apstrādātu kreditoru sadarbības lietotāja pieprasījumus, kuru tips ir **Nodrošināt kreditora lietotāju**.

Ja jauna kreditora sadarbības lietotāja e-pasta adrese pieder domēnam, kas ir reģistrēts Azure kā nomnieks (t.i., ja tas ir pārvaldīts domēna konts), e-pasta adresei ir jābūt esošam Azure AD kontam. Pretējā gadījumā nodrošinājuma procesu nevar pabeigt.

Papildinformāciju par procesu, kas tiek izmantots **Sūtīt Azure B2B lietotāja uzaicinājumu** uzdevumā Azure AD konta pārvaldības darbplūsmā, skatiet [Azure Active Directory B2B sadarbība](/azure/active-directory/external-identities/what-is-b2b).

## <a name="additional-resources"></a>Papildu resursi

[Kreditoru sadarbība ar ārējiem kreditoriem](vendor-collaboration-work-external-vendors.md)

Noskatīties īsu video par kreditora pievienošanas procesu: [Pievienot jaunu kreditoru](https://www.youtube.com/watch?v=0KUc3AGaTKk&feature=youtu.be)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
