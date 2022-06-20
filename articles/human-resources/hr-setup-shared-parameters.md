---
title: Konfigurēt koplietotos parametrus
description: Šajā rakstā ir paskaidrots, kā iestatīt personāla vadības parametrus juridiskām personām.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c0d8dbca302d90cc402feb4715a6fcc2b935d8b1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906187"
---
# <a name="configure-shared-parameters"></a>Konfigurēt koplietotos parametrus

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Jums jāiestata koplietojamie parametri ierakstiem, kas tiek koplietoti visu uzņēmumu, piemēram, amatu **ierakstu** gadījumos. Šajā rakstā ir paskaidrots, kā iestatīt personāla vadības parametrus juridiskām personām.

Daži ierakstu veidi, piemēram, Amatu **ieraksti**, tiek koplietoti uzņēmumu dažādos uzņēmumos. Šiem ierakstiem ir jāiestata koplietojamie parametri. Piemēram, lapa Cilvēkresursu **kopīgie parametri** tiek izmantota, lai iestatītu personāla vadības parametrus dažādām juridiskajām personām. 

Lapā **Personāla vadības kopīgie parametri** parametri tiek grupēti apgabalos, pamatojoties uz to funkcionalitāti. 

### <a name="settings"></a>Iestatījumi
Cilnē **Identifikācija** ir jāatlasa identifikācijas tipi, kas pārstāv šajā lapā uzskaitītos identifikācijas numurus. Identifikācijas tipi ir jāiestata, pirms darbiniekiem varat ievadīt identifikācijas informāciju. Informācija par sociālās apdrošināšanas numuru, nacionālo ID numuru, ārzemnieka ID numuru un personas kodu tiek glabāta lapā **Identifikācijas tips**. Lai definētu jaunu identifikācijas tipu vai pārskatītu esošo tipu sarakstu, dodieties uz personāla vadības saišu **iestatījuma** &gt; **·** &gt; **identifikācijas** &gt; **tipiem.** Var ievadīt vienkāršu kodu un aprakstu. 

**Cilnē Numuru sērijas var atlasīt numuru sērijas, kas tiek izmantotas šādiem ierakstiem:** **personāla numurs, amats,** **lietotāja pieprasījuma ID**, **I**-9 dokuments **,** **·** **kandidāts, diskusija,** atvieglojumu **ID** **un personāla darbība (ja šis ieraksta tips ir iespējots).** Lai saglabātu numuru sēriju atsauces un kodus, lietojiet saraksta lapu **Numuru sērijas**. Lai atrastu šo lapu, lietojiet lapu meklēšanas funkciju. 

Cilnē **Amati** norādiet, vai jauni amati ir pieejami piešķiršanai pēc noklusējuma:

- **Vienmēr** — darbiniekus jauniem amatiem var piešķirt amatu izveides brīdī. Izveidojot amatus, datums un laiks **Pieejams piešķirei** cilnē **Vispārīgi** lapā **Amati** tiek automātiski iestatīti uz izveides datumu un laiku.
- **Nekad** — darbiniekus jauniem amatiem nevar piešķirt amatu izveides brīdī. Ja izvēlaties šo opciju, jums jāatver lapa **Pozīcija** katrai jaunai pozīcijai, kad tā ir pieejama. Pēc tam cilnē **Vispārīgi** ievadiet datumu **Pieejams piešķirei**, lai iespējotu darbinieka piešķiri.

Cilnē **Paplašināta piekļuve** var ierobežot piekļuvi informācijai vai saitēm:

- **Ierobežot piekļuvi darbinieka informācijai** – atlasiet šo funkciju, ja lietotājiem vajadzētu būt spēt skatīt darbinieku informāciju tikai tām juridiskajām personām, kurām viņiem ir piekļuve, un darbiniekiem, kuriem ir nodarbinātība šajās juridiskajās personām.

    Pēc šīs funkcijas izvēles izpildiet šīs darbības, lai iestatītu atbilstošās atļaujas katram lietotājam, kura skatījums ir jāierobežo:

    1. Lapā **Lietotāji** atlasiet lietotāju.
    1. Izvēlieties lietotājam lomu. Opcija **Piešķirt organizācijas** kļūst pieejama.
    1. Atlasiet **Piešķirt organizācijas**.
    1. Jaunajā lapā atlasiet **Atsevišķi piešķirt piekļuvi noteiktām organizācijām** un pēc tam atlasiet organizācijas, kurām lietotājam būs piekļuve.
    1. Atkārtojiet no 2. līdz 4. solim katrai lietotāja papildu lomai, tostarp sistēmas lietotāja lomai.

    > [!NOTE]
    > Uzņēmumiem, kuriem lietotājam ir piekļuve, ir jāatbilst visām lietotāja lomām.

- **Iespējot starpuzņēmumu kompensāciju skatu** — atlīdzība darbiniekiem tiek piešķirta katrai nodarbinātības juridiskajai personai. Dažreiz darbinieks var tikt nodarbināts vairākās juridiskajās personās vienlaicīgi. Kad šī funkcija ir atlasīta, atlīdzība katrai **juridiskajai personai tiks parādīta darbinieku pašapkalpošanās** **un pārvaldnieka pašapkalpošanās sistēmā** bez nepieciešamības mainīt juridiskās personas. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
