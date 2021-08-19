---
title: Konfigurēt lomu Prombūtnes pārvaldnieks
description: Šajā tēmā skaidrots, kā iestatīt lomu Prombūtnes pārvaldnieks darbinieku atvaļinājuma pārvaldībai.
author: hasrivas
ms.date: 07/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace, LeaveAbsenceManager
audience: Application User
ms.search.scope: Human Resources
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: hasrivas
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 050874628388629569751afae201ef346af020da09c81d24a69e1a4b5eb41b6f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732349"
---
# <a name="configure-the-absence-manager-role"></a>Konfigurēt lomu Prombūtnes pārvaldnieks

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

Dažās organizācijās cilvēku vadītāji var ne pārvaldīt atvaļinājumu savas komandas vadītājiem. Tā vietā prombūtnes vadītājs var apstrādāt šo procesu grupas dalībniekiem vairākās nodaļās un komandās. Prombūtnes pārvaldniekiem atvaļinājumu pārvaldībai ir šādas iespējas:

- Pārskatīt un apstiprināt brīvo laiku, balstoties uz alternatīvu hierarhiju.
- Skatīt grupas dalībnieku bilances.
- Skatīt prombūtnes kalendāru.

## <a name="turn-on-the-feature"></a>Līdzekļa iespējošana

1. Darbvietā **Sistēmas administrēšana** atlasiet **Līdzekļu pārvaldība**.

2. Cilnē **Līdzekļu pārvaldība** aktivizējiet līdzekli **(Priekšskatījums) Prombūtnes pārvaldnieks, lai pārvaldītu atvaļinājumu**.

## <a name="define-a-custom-hierarchy"></a>Definēt pielāgotu hierarhiju

Prombūtnes pārvaldnieka funkcionalitāte izmanto pielāgotu hierarhiju, kas ir jākonfigurē.

1. Darbvietā **Organizācijas administrēšana** atlasiet **Amatu hierarhijas tipi**.

2. Izveidojiet amatu hierarhijas tipu ar nosaukumu **Atvaļinājums**.

3. Darbvietā **Atvaļinājums un prombūtne** sadaļā **Saites** atlasiet **Atvaļinājumu un prombūtnes parametri**.

4. Cilnes **Vispārīgi** nolaižamajā sarakstā **Kavējumu hierarhija** atlasiet iepriekš izveidoto hierarhijas tipu **Atvaļinājums**. Šo Atvaļinājuma hierarhiju saistību jāaizpilda visām juridiskajām personām, kur tiks izmantota kavējumu pārvaldnieka funkcionalitāte.

Kad hierarhijas tips ir definēts, amatam ir jāpiešķir amatu hierarhijas pārskats.

1. Darbvietā **Organizācijas administrēšana** atlasiet **Visi amati**.

2. Atlasiet amatu, lai pievienotu Atvaļinājumu hierarhiju.

3. Cilnē **Attiecības** atlasiet **Pievienot**.

4. Laukā **Hierarhijas nosaukums** atlasiet **Atvaļinājums**.

5. Laukā **Ziņojumi par amatiem** ievadiet vai atlasiet amatu. Kad atlasāt amatu, darbinieka vārds tiek ievadīts automātiski.

## <a name="assign-the-absence-manager-role-to-a-user"></a>Prombūtnes pārvaldnieka lomas piešķiršana lietotājam

Prombūtnes pārvaldnieka loma ir jāpiešķir darbiniekiem, lai tie varētu apstiprināt vai noraidīt atvaļinājumu pieprasījumus.

1. Darbvietā **Sistēmas administrators** atlasiet **Saites**.

2. Sadaļā **Lietotāji** atlasiet saiti **Lietotāji**.

3. Lietotāju sarakstā atlasiet lietotāju, kam piešķirt Prombūtnes pārvaldnieka lomu.

4. Cilnē **Lietotāja loma** atlasiet **Piešķirt lomas**.

5. Sarakstā atlasiet lomu **Prombūtnes pārvaldnieks**. Pēc tam atlasiet **Labi**.

    > [!IMPORTANT]
    > Pārliecinieties, vai darbinieka loma ir piešķirta arī lietotājam, kuram tiek piešķirta Prombūtnes pārvaldnieka loma. Pretējā gadījumā darbinieks nevarēs izmantot šo funkciju.

6. Pēc atvaļinājumu hierarhijas izveides to var skatīt, veicot šādas darbības:

    1. Darbvietā **Organizācijas administrēšana** atlasiet **Amatu hierarhija**.
    
    2. Laukā **Hierarhijas tips** atlasiet **Atvaļinājums**.

## <a name="absence-manager-workspace"></a>Kavējumu pārvaldnieka darbvieta

Darbvietā **Darbinieku pašapkalpošana** cilne **Kavējumu pārvaldnieks** parāda kavējumu informāciju par darbiniekiem, kas ir piešķirti kavējumu pārvaldniekam atvaļinājumu hierarhijā. Kavējumu pārvaldniekam ir pieejamas dažas opcijas: 
 - Prombūtnes pieprasījumu atcelšana.</br>
 - Iesniedziet darba laika pieprasījumu darbinieka vārdā.</br>
 - Skatiet visus darbiniekus, kam tie tika piešķirti kā daļa no kavējumu hierarhijas.</br>
 - Skatīt kavējumu pārvaldnieka kalendāru.</br>

**Atvaļinājumu pārvaldības** darbvietā ir divas cilnes:
 - **Neierašanās pieprasījumi**: šajā cilnē tiks uzskaitīts visi nenokārtoto laiku kavējumu pieprasījumi, kurus kavējumu vadītājs var apstiprināt. Kavējumu pārvaldnieks var atlasīt vairākus ierakstus un rīkoties ar tiem vienlaicīgi. Ja starpuzņēmumu atvaļinājumu skats ir iespējots, šajā sarakstā tiks rādīti neizlemto laiku pieprasījumi visām juridiskajām personām, kurām viņiem ir piekļuve. Pretējā gadījumā tiks rādīti pašlaik atlasītās juridiskās personas neizlemto laiku pieprasījumi. </br>
 - **Visi darbinieki** : šajā cilnē tiks uzskaitīti visi darbinieki, kas ir piešķirti kavējumu vadītājam Atvaļinājumu hierarhijā. Katram darbiniekam ir pieejamas dažas opcijas:
    - **Pieprasījuma laiks** ir izslēgts - iesniegt jaunu atlasītā darbinieka aiziešanas pieprasījuma laiku.</br>
    - **Brīvais laiks** – skatiet bilances, apstiprinātos izslēgtos laikus un izvēlētā darbinieka brīvā laika pieprasījumus.</br>

## <a name="approve-time-off-requests"></a>Prombūtnes pieprasījumu apstiprināšana

Prombūtnes pārvaldnieki var apstiprināt vai noraidīt darbinieku brīvā laika pieprasījumus. 

> [!IMPORTANT]
> Pirms prombūtnes pārvaldnieki var apstiprināt vai noraidīt brīvā laika pieprasījumus, atvaļinājumu pieprasījuma darbplūsma ir jākonfigurē, lai piešķirtu tiem darba pieprasījuma krājumus pārskatīšanai.
>
> 1. Lapā **Personāla vadības darbplūsmas** atlasiet vai izveidojiet atvaļinājuma pieprasījuma darbplūsmu.
> 2. Atlasiet opciju **Saistīt hierarhiju** un pēc tam laukā **Hierarhijas nosaukums** atlasiet **Atvaļinājums**.
> 3. Atjaunināt darbplūsmu darbplūsmas veidotājā. Sadaļā **Piešķires tips** atlasiet opciju **Hierarhija** un pēc tam cilnē **Hierarhijas atlase** atlasiet **Konfigurējama hierarhija**.
>
> Informāciju par to, kā izveidot atvaļinājuma pieprasījuma darbplūsmu, skatiet šeit: [Atvaļinājuma pieprasījuma darbplūsmas izveide](hr-leave-and-absence-workflow.md).

1. Darbvietā **Darbinieka pašapkalpošana** atlasiet cilni **Atvaļinājumu pārvaldnieks**.

2. Cilnē **Izslēgt laiku pieprasījumus** atlasiet pieprasījumus, ar kuriem vēlaties veikt darbības. Šajā saraksta skatā varat atlasīt vairākus ierakstus.

3. Izmantojiet darbības pogas režģa augšpusē, lai apstiprinātu, liegtu vai deleģētu pieprasījumu pēc laika. 

Vai arī lietotājs var izmantot arī **Laiku pieprasījumu** elementu kreisajā pusē, lai pārvietotos uz visu nepieprasamo darba vienumu sarakstu. 

## <a name="view-time-off-in-the-calendar"></a>Skatīt kalendārā brīvo laiku

Prombūtnes pārvaldnieka lomas lietotāji kalendārā var skatīt brīvā laika pieprasījumus. Lai piekļūtu atvaļinājuma kalendāram, rīkojieties šādi.

> [!IMPORTANT]
> Sistēmas administratoram ir jākonfigurē prombūtnes pārvaldnieka kalendāra skatīšanas opcijas. Lapas **Atvaļinājuma un prombūtnes parametri** cilnē **Kalendārs** ir opcijas, kas ļauj paslēpt vai rādīt dzimšanas dienas, kavējumus bez detalizētas informācijas, prombūtnes atvaļinājumus un gaidošos atvaļinājumu pieprasījumus. Pastāv arī opcija, lai filtrētu kalendāra skata opciju pēc darbinieka veida.

1. Darbvietā **Darbinieku pašapkalpošana** atlasiet **Prombūtnes pārvaldnieks** un pēc tam **Prombūtnes pārvaldnieka kalendārs**.

2. Laukā **Datums** ievadiet vajadzīgos datumus.

3. Pēc vajadzības atjauniniet skata opcijas.

Prombūtnes pārvaldnieku kalendārs rāda visus ierakstus par darbiniekiem, kuri sniedz pārskatu prombūtnes pārvaldniekam atvaļinājumu hierarhijā.

## <a name="see-also"></a>Skatiet arī

- [Atvaļinājumu un kavējumu apskats](hr-leave-and-absence-overview.md)
- [Atvaļinājuma pieprasījuma izveide darbplūsmai](hr-leave-and-absence-workflow.md)
- [Grupas un uzņēmuma kalendāru skatīšana](hr-employee-self-service-calendar.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
