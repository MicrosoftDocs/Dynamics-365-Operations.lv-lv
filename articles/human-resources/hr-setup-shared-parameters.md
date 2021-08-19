---
title: Konfigurēt koplietotos parametrus
description: Jums ir jāiestata koplietotie parametri ierakstiem, kas tiek koplietoti uzņēmumu starpā, piemēram, amatu ierakstiem. Šajā rakstā ir paskaidrots, kā iestatīt personāla vadības parametrus juridiskām personām.
author: andreabichsel
ms.date: 06/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 66f57c9613ba04ebb3748699105469586c27d66131c062d1af286b24199c4be7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723651"
---
# <a name="configure-shared-parameters"></a>Konfigurēt koplietotos parametrus

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Jums ir jāiestata koplietotie parametri ierakstiem, kas tiek koplietoti uzņēmumu starpā, piemēram, amatu ierakstiem. Šajā rakstā ir paskaidrots, kā iestatīt personāla vadības parametrus juridiskām personām.

Uzņēmumi koplieto dažu veidu ierakstus, piemēram, amatu ierakstus. Šiem ierakstiem ir jāiestata koplietojamie parametri. Piemēram, lapu **Personāla vadības kopīgie parametri** var izmantot, lai iestatītu Personāla vadības parametrus juridiskām personām. 

Lapā **Personāla vadības kopīgie parametri** parametri tiek grupēti apgabalos, pamatojoties uz to funkcionalitāti. 

### <a name="settings"></a>Iestatījumi
Cilnē **Identifikācija** ir jāatlasa identifikācijas tipi, kas pārstāv šajā lapā uzskaitītos identifikācijas numurus. Identifikācijas tipi ir jāiestata, pirms darbiniekiem varat ievadīt identifikācijas informāciju. Informācija par sociālās apdrošināšanas numuru, nacionālo ID numuru, ārzemnieka ID numuru un personas kodu tiek glabāta lapā **Identifikācijas tips**. Lai definētu jaunu identifikācijas tipu vai pārskatītu esošo tipu sarakstu, noklikšķiniet uz **Personāla vadība** &gt; **cilne Saites** &gt; **Iestatījumi** &gt; **Identifikācijas tipi**. Var ievadīt vienkāršu kodu un aprakstu. 

Cilnē **Numuru sērijas** var atlasīt numuru sērijas, kas tiek izmantotas šiem ierakstiem: Personāla numurs, Amats, Lietotāja pieprasījuma ID, I-9 dokuments, Kandidāts, Diskusija, Atvieglojumu ID un Personāla darbība (ja ir aktivizēts šis ieraksta tips). Lai saglabātu numuru sēriju atsauces un kodus, lietojiet saraksta lapu **Numuru sērijas**. Lai atrastu šo lapu, lietojiet lapu meklēšanas funkciju. 

Cilnē **Amati** norādiet, vai jauni amati ir pieejami piešķiršanai pēc noklusējuma:

- **Vienmēr** — darbiniekus jauniem amatiem var piešķirt amatu izveides brīdī. Izveidojot amatus, datums un laiks **Pieejams piešķirei** cilnē **Vispārīgi** lapā **Amati** tiek automātiski iestatīti uz izveides datumu un laiku.
- **Nekad** — darbiniekus jauniem amatiem nevar piešķirt amatu izveides brīdī. Ja izvēlaties šo opciju, jums jāatver lapa **Pozīcija** katrai jaunai pozīcijai, kad tā ir pieejama. Pēc tam cilnē **Vispārīgi** ievadiet datumu **Pieejams piešķirei**, lai iespējotu darbinieka piešķiri.

Cilnē **Paplašināta piekļuve** var ierobežot piekļuvi informācijai vai saitēm:

- **Ierobežot piekļuvi darbinieka informācijai** – Ieslēniet šo funkciju, ja lietotājiem vajadzētu būt spēt skatīt darbinieku informāciju tikai par tām juridiskajām personām, kurām viņiem ir piekļuve, un darbiniekiem, kuriem ir nodarbinātība šajās juridiskajās personas.

    Kad šī funkcija ir ieslēgta, jums jāveic šādas darbības, lai katram lietotājam, kura skats ir jāierobežo, iestatītu atbilstošās atļaujas:

    1. Lapā **Lietotāji** atlasiet lietotāju.
    1. Izvēlieties lietotājam lomu. Opcija **Piešķirt organizācijas** kļūst pieejama.
    1. Atlasiet **Piešķirt organizācijas**.
    1. Jaunajā lapā atlasiet **Atsevišķi piešķirt piekļuvi noteiktām organizācijām** un pēc tam atlasiet organizācijas, kurām lietotājam būs piekļuve.
    1. Atkārtojiet 2. līdz 4. darbību visām citām lietotāja lomām, ieskaitot sistēmas lietotāja lomu.

    > [!NOTE]
    > Uzņēmumiem, kuriem lietotājam ir piekļuve, ir jāatbilst visām lietotāja lomām.

- **Iespējot starpuzņēmumu kompensāciju skatu** — atlīdzība darbiniekiem tiek piešķirta katrai nodarbinātības juridiskajai personai. Dažreiz darbinieks var tikt nodarbināts vairākās juridiskajās personās vienlaicīgi. Ja šis līdzeklis ir ieslēgts, kompensācija katrai juridiskajai personai parādīsies Darbinieku pašapkalpošanas un Vadītāja pašapkalpošanās sistēmā bez nepieciešamības mainīt juridiskās personas. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
