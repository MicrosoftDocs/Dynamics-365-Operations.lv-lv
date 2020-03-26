---
title: Izveidot darbu sistēmā Attract
description: Šajā tēmā ir aprakstīti darba elementi programmā Attract. Tajā ir arī paskaidrots, kā izveidot darbu.
author: hasrivas
manager: AnnBe
ms.date: 07/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: hasrivas
ms.search.validFrom: 2018-10-24
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 9dcdbcea995285c879f91c0bff435103865cc10f
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124754"
---
# <a name="create-a-job-in-attract"></a>Izveidot darbu sistēmā Attract

[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīti darba elementi programmā Microsoft Dynamics 365 Talent: Attract. Tajā ir arī paskaidrots, kā izveidot darbu.

## <a name="job-creation"></a>Darba izveide

Darbus var izveidot administratori, personāla atlases darbinieki un par pieņemšanu darbā atbildīgie vadītāji. Veidojot darbu, tiek pieprasīts atlasīt jūsu lomu procesā: par pieņemšanu darbā atbildīgais vadītājs vai personāla atlases darbinieks. Pēc lomas atlasīšanas tiek pieprasīts atlasīt procesa veidni. Ja atlasāt **Izlaist**, tiek izmantota noklusējuma veidne. Papildinformāciju par procesa veidnēm skatiet tēmā [Procesa veidnes izveide programmā Attract](./process-templates-attract.md).

Darbam programmā Attract ir norādīta darba informācija, darbā pieņemšanas grupa, darbā pieņemšanas process, darba publicēšana un analīze.

## <a name="job-details"></a>Darba informācija

Cilnē **Darba informācija** ir iekļauta informācija par darba pienākumiem un atribūtiem. Amata nosaukuma, amata apraksta un darba atrašanās vietas lauki ir obligāti. Pārējie lauki nav obligāti.

Pēc noklusējuma laukā **Vakanču skaits** ir iestatīta vērtība **1**. Tomēr vērtību var mainīt. Kad darbam ir sagatavots piedāvājums, vērtība laukā **Pieejamo vakanču skaits** tiek samazināta.

Ja administrēšanas centrā ir ieslēgta amatu pārvaldība, ir pieejama meklēšana **Atjaunināt amatus**. Veicot šo meklēšanu, tiek nolasīts elements JobPosition pakalpojumā Common Data Service un tiek atgriezts amatu saraksts, kurus var atlasīt attiecīgajam darbam. Ja atlasīto amatu skaits pārsniedz atvērto amatu skaitu, saņemsit brīdinājumu. Brīdinājumu arī saņemsit gadījumā, ja amats tiek izmantots vairākos darbos.

> [!NOTE]
> Amatu pārvaldība ir pieejama tad, ja jums ir visaptverošais darbā pieņemšanas papildinājums.

Atkarībā no iestatījumiem darbā pieņemšanas procesa aktivitātei Piedāvājums amata numuru var izmantot divas reizes piedāvājumā. Lai iegūtu papildu informāciju, skatiet rakstu [Aktivitātes darbā pieņemšanas procesos](./activities-attract.md)procesos.

Programmā Attract ietilpst noklusējuma **Prasmju** komplekts. Rakstīšanas laikā šīs prasmes parādās kā ieteikumi. Varat pievienot papildu prasmes, ievadot jaunu prasmju tekstu laukā un pēc tam nospiežot pogu Enter.

Programmā Attract ietilpst noklusējuma **Darba funkciju** komplekts. Varat pievienot trīs papildu darba funkcijas, ievadot jaunu darba funkciju laukā un pēc tam nospiežot pogu Enter.

Programmā Attract ietilpst noklusējuma **Uzņēmuma nozares** komplekts. Varat pievienot trīs papildu uzņēmuma nozares, ievadot jaunu uzņēmuma nozari laukā un pēc tam nospiežot pogu Enter.

## <a name="hiring-team"></a>Darbā pieņemšanas grupa

Cilne **Darbā pieņemšanas grupa** satur sarakstu ar personām, kuras piedalīsies darbā. Pievienojot lietotājus darbā pieņemšanas grupai, tiem ir jāpiešķir loma darbā pieņemšanas grupā. Loma nosaka datus, kuriem lietotājiem ir piekļuve, un paziņojumus, kurus tie saņem. Var atlasīt šādas lomas: **Personāla atlases darbinieks**, **Par pieņemšanu darbā atbildīgais vadītājs**, **Pārstāvis** un **Intervētājs**. Papildinformāciju par lomu privilēģijām skatiet dokumentā “Lomu pārvaldība”. Personāla atlases darbinieki un par pieņemšanu darbā atbildīgie vadītāji var iecelt vienu vai vairākus pārstāvjus strādāt viņu vārdā. Papildinformāciju par pārstāvjiem skatiet tēmā [Drošība un lomu pārvaldība programmā Attract](./security-attract.md).

Darbā pieņemšanas grupu var atjaunināt pēc tam, kad darbs ir aktivizēts.

## <a name="process"></a>Apstrādāt

Noklusējuma informācija par darbā pieņemšanas procesu balstās uz procesa veidni, kas tika atlasīta, izveidojot darbu. Ja attiecīgajā brīdī netika atlasīta noteikta veidne, tiek izmantota noklusējuma veidne. Definējot darbā pieņemšanas procesu, var pievienot vai noņemt dažādus posmus, izņemot posmus Potenciālais kandidāts, Pieteikums un Piedāvājums. Lai gan posmu Potenciālais kandidāts nevar noņemt, to var izslēgt. Katra posma ietvaros var pievienot vai noņemt vienu vai vairākas iepriekš definētas aktivitātes.

Plašāku informāciju par aktivitātēm, kuras var pievienot darbā pieņemšanas procesā, skatiet tēmā [Aktivitātes darbā pieņemšanas procesos](./activities-attract.md).

> [!NOTE]
> Darbā pieņemšanas procesu nevar atjaunināt pēc tam, kad darbs ir aktivizēts.

## <a name="postings"></a>Grāmatojumi

Pēc tam, kad darbs ir aktivizēts, to var publicēt. Darbus var publicēt tikai personāla atlases darbinieki un administratori. Darbu var publicēt vietnē Talent Careers (Dynamics 365 Talent karjeras vietne) vai LinkedIn. Attract darba grupa nepārtraukti strādā, lai sadarbotos ar darba paneļu apkopotājiem. Laika gaitā šis saraksts paplašināsies. Kad darbs tiek publicēts kā tikai iekšējs, kandidātiem ir nepieciešams AAD konts, lai skatītu darbu un pieteiktos tam. Ja darbs ir publicēts kā publisks, kandidāti var skatīt darbus un pieteikties tiem, izmantojot visas autentifikācijas iespējas. 

Plašāku informāciju par darbu publicēšanu skatiet tēmā [Karjeras vietas iestatīšana Microsoft Dynamics 365 Talent - Attract](career-site.md).

> [!NOTE]
> Darbu publicēšanas funkcionalitāte ir pieejama tikai tad, ja jums ir visaptverošais darbā pieņemšanas papildinājums programmai Attract.

## <a name="activate"></a>Aktivizēt

Pēc tam, kad darbs ir aktivizēts, to var publicēt, un tam var pievienot potenciālos kandidātus un kandidātus. Opcija pievienot potenciālos kandidātus darbam ir iestatīta aktivitātē Potenciālais kandidāts darbā pieņemšanas procesā.

> [!NOTE]
> Darbā pieņemšanas procesu nevar atjaunināt pēc tam, kad darbs ir aktivizēts.

## <a name="prospects-and-applicants"></a>Potenciālie kandidāti un kandidāti

Opcija pievienot potenciālos kandidātus darbam ir iestatīta [Aktivitātes darbā pieņemšanas procesos](./activities-attract.md#prospect-activity) darbā pieņemšanas procesā. Šī opcija ir jāiestata pirms darba aktivizēšanas. Pēc tam, kad darbs ir aktivizēts, tam var pievienot potenciālos kandidātus un kandidātus.

## <a name="approvals"></a>Apstiprinājumi

Attract darbus var iesniegt apstiprināšanai. Ne visiem darbiem ir nepieciešams apstiprinājums. Prasība ir iestatīta veidnes līmenī. Pēc noklusējuma apstiprinājumi veidnē ir izslēgti. Lai iestatītu apstiprinājumus, pārejiet uz procesa veidni un iestatiet laukam **Apstiprinājums** vērtību Noklusējums. Pēc tam atlasiet attiecīgo veidni, veidojot darbu.

Pēc tam, kad darbs ir saglabāts, to var iesniegt apstiprināšanai. Šajā tabulā ir norādīti tāda dokumentu statusi, kuram tiek izmantoti apstiprinājumi.

| Statuss   | Administratīvais apgabals                                                               |
|----------|---------------------------------------------------------------------|
| Melnraksts    | Darbs ir saglabāts, bet tas nav iesniegts darbplūsmā. |
| Gaida  | Darbs tika iesniegts apstiprinātājiem.                            |
| Apstiprināts | Darbs ir apstiprināts, bet tas nav aktivizēts.            |
| Noraidījis | Darbs ir noraidīts, un to nevar aktivizēt.               |
| Aktīvie   | Darbs ir apstiprināts un aktivizēts.                            |

Darbu sarakstā var filtrēt darba statusus.

Apstiprinājumus var nosūtīt jebkuram Microsoft Azure Active Directory (Azure AD) lietotājam uzņēmumā. Apstiprinājumi tiek sūtīti paralēli visiem cilvēkiem, kas ir norādīti kā apstiprinātāji. Visiem apstiprinātājiem ir jāapstiprina darbs, pirms to var pārvietot uz priekšu. Ja viens apstiprinātājs noraida darbu, darbam tiek rādīts statuss **Noraidīts**. Pēc tam, kad darbs ir apstiprināts, to var aktivizēt.

Ja lietotājs rediģē darbu pēc tam, kad tas ir apstiprināts, bet nav aktivizēts, darba statuss tiks atiestatīts uz **Melnraksts**, un darbs ir atkārtoti jāiesniedz apstiprināšanai. Pēc apstiprināta darba aktivizēšanas to nevar rediģēt.

Cilvēki, kas ir norādīti kā apstiprinātāji, saņems paziņojumu programmā Attract un e-pasta ziņojumu, lai informētu tos, ka tiem ir jāapstiprina vienums.  E-pasta ziņojumā apstiprinātāji var noklikšķināt uz saites, lai atvērtu darbu, pārskatītu detalizētu informāciju un apstiprinātu vai noraidītu. Pēc tam, kad darba statuss tiek iestatīts kā **Apstiprināts** vai **Noraidīts**, iesniedzējs tiek informēts programmā Attract, un viņam tiek nosūtīts e-pasta ziņojums. Turklāt apstiprinātāji saņem atgādinājuma e-pasta ziņojumu, ja viņi nav reaģējuši uz apstiprinājuma pieprasījumu 24 stundu laikā.

> [!NOTE]
> Varat izveidot pielāgotas e-pasta veidnes apstiprinājuma e-pasta ziņojumiem. Plašāku informāciju skatiet rakstā [E-pasta veidņu izveide un pārvaldība](https://docs.microsoft.com/dynamics365/unified-operations/talent/email-templates).

## <a name="create-a-job"></a>Darba izveide

Lai izveidotu darbu, veiciet šādas darbības.

1. Atveriet sadaļu **Darbi**.
2. Atlasiet **Jauns**.
3. Laukā **Amata nosaukums** ievadiet amata nosaukumu. Laukā **Loma** ievadiet lomu.
4. Laukā **Veidne** atlasiet veidni. Varat arī atlasīt vienumu **Izlaist**. Atlasot **Izlaist**, tiek izmantota veidne, kas atzīmēta kā noklusējuma veidne.

    Ja dokumentam ir jāveic apstiprināšanas process, atlasiet veidni, kur laukā **Apstiprināšanas process** ir iestatīta vērtība **Noklusējums**.

5. Cilnē **Informācija** ievadiet darba informāciju. Lauki **Amats**, **Amata apraksts** un **Darba atrašanās vieta** ir obligāti.
6. Atlasiet **Saglabāt**.
7. Cilnē **Darbā pieņemšanas grupa** pievienojiet par pieņemšanu darbā atbildīgo vadītāju, personāla atlases darbinieku vai intervētāju.
8. Atlasiet **Saglabāt**.
9. Cilnē **Process** pievienojiet vai noņemiet nepieciešamos posmus:

    - Lai pievienotu posmu, atlasiet **+ jauns posms**.
    - Lai noņemtu kādu posmu, virziet peles rādītāju pār noņemšanai paredzēto posmu un pēc tam atlasiet parādīto atkritnes pogu.

        > [!NOTE]
        > Posmus Potenciālais klients, Pieteikums un Piedāvājums nevar noņemt.

10. Pievienojiet vai noņemiet nepieciešamās aktivitātes:

    - Lai pievienotu kādu aktivitāti, no saraksta labajā pusē velciet to uz atbilstošo posmu. Vai arī veiciet dubultklikšķi uz aktivitātes un pēc tam atlasiet posmu, kuram to pievienot.
    - Lai noņemtu kādu aktivitāti, izvērsiet to un pēc tam atlasiet atkritnes pogu šīs aktivitātes galvenē.

11. Atlasiet **Saglabāt**.
12. Ja atlasījāt apstiprināšanas procesa izmantošanu, veiciet šādas darbības:

    1. Atlasiet **+ Pievienot apstiprinātāju** un pēc tam ievadiet lietotāju, kuram ir Azure AD konts. Var pievienot vairākus apstiprinātājus.
    2. Atlasiet **Nosūtīt apstiprinātājiem**.

    Darba laukā **Darba statuss** ir iestatīta vērtība **Gaida**. Pēc tam, kad lauka **Darba statuss** vērtība mainās uz **Apstiprināts**, darbu var aktivizēt.

13. Lai aktivizētu darbu, atlasiet **Aktivizēt**.
14. Lai publicētu darbu, atveriet sadaļu **Publicētie darbi** un pēc tam atlasiet **Publicēt tagad** vietnē Talent Careers vai LinkedIn.
