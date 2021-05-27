---
title: Iespējot vairākus pasūtījuma piegādes veidus klientu pasūtījumiem
description: Šī tēma izskaidro Microsoft Dynamics 365 Commerce funkcionalitāti, kas ļauj izveidot klientu pasūtījumus saņemšanai veikalā.
author: hhainesms
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 124765a3d4d2ebd01e200b76fc862e2c37073b8e
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020655"
---
# <a name="enable-multiple-pickup-delivery-modes-for-customer-orders"></a>Iespējot vairākus pasūtījuma piegādes veidus klientu pasūtījumiem

[!include [banner](includes/banner.md)]


Programmas Microsoft Dynamics 365 Commerce versijā 10.0.16 un jaunākās organizācijas var noteikt vairākus piegādes veidus, kurus pircēji vai pārdošanas dalībnieki var izvēlēties brīdī, kad tie izveido pasūtījumu, kas tiks saņemts veikalā. Šādā veidā organizācijas var nodrošināt vairākas saņemšanas opcijas saviem pircējiem. Piemēram, daudzi mazumtirgotāji tagad pircējiem piedāvā pasūtījumu saņemšanu veikalā vai saņemšanu pa ceļam. Commerce atbalsta šo atšķirīgo saņemšanas piegādes veidu konfigurāciju. Lietotāji pēc tam var izmantot tos, kad tie izveido klientu pasūtījumus jebkādā atbalstītā Commerce kanālā (e-komercija, zvanu centrs vai veikals).

## <a name="enable-and-configure-pickup-delivery-modes"></a>Piegādes veidu iespējošana un konfigurēšana

Lai izmantotu šo funkcionalitāti, ieslēdziet **Vairāku saņemšanas piegādes veidu atbalsts** līdzekli darbvietā **Līdzekļu pārvaldība** Commerce Headquarters. Pēc līdzekļa ieslēgšanas ir nepieciešama papildu konfigurācija.

Commerce Version 10.0.15 un vecākās versijās uzņēmumi var definēt tikai vienu piegādes veidu kā noteikto saņemšanas piegādes veidu. Šī definīcija tiek veikta lapā **Commerce parametri**. Versijā 10.0.16 un jaunākās versijās, ieslēdzot **Vairāku saņemšanas piegādes veidu atbalsts** līdzekli, piegādes veids, kas iepriekš tika definēts kā pasūtījumu piegādes veids lapā **Commerce parametri**, tiek automātiski kopēts uz jauno konfigurāciju pasūtījumu piegādes veidiem.

![Pasūtījumu piegādes veidi lapā Commerce parametri](media/multiplepickupparameter.png)

Pēc tam, kad esat ieslēdzis **Vairāku saņemšanas piegādes veidu atbalsts** līdzekli, varat definēt vairākus saņemšanas piegādes veidus režģī **Saņemšanas piegādes veidi** kopsavilkuma cilnē **Piegādes veidi** cilnē **Klientu pasūtījumi** , kas atrodas lapā **Commerce parametri**.

Lauki **Carry Out piegādes veids** un **Elektroniskās piegādes veids**, kā arī opcija **Rādīt tikai pārvadātāja veidu opcijas kuģu pasūtījumiem** ir pārvietota uz šo kopsavilkuma cilni.

Pirms konfigurējat papildu saņemšanas piegādes veidus, ir jādefinē piegādes veidi. Lapā **Piegādes veidi** sadaļā Commerce Headquarters pievienojiet piegādes veidus, kas jāuzskata par saņemšanas piegādes veidiem. Pārliecinieties, vai visas konfigurācijas ir pabeigtas. Piemēram, pārliecinieties, ka piegādes veids ir saistīts ar atbilstošiem kanāliem un krājumiem. Kad esat pabeidzis, palaidiet darbu **Apstrādāt piegādes veidus**, lai izveidotu attiecības starp piegādes veidu, kanāliem un krājumiem. Kad darbs ir pabeigts, atveriet **Sadales grafika** lapu sadaļā Commerce Headquarters un palaidiet **1120** sadales darbu, lai nodrošinātu, ka attiecīgās Commerce kanāla datu bāzes tiek atjauninātas ar jauno piegādes veida konfigurāciju.

![Piegādes konfigurācijas veida piemērs saņemšanai pa ceļam](media/pickupmodes.png)

Pēc tam, kad esat definējis papildu saņemšanas piegādes veidus, pievienojiet tos režģī **Saņemšanas piegādes veids** lapā **Commerce parametri**. Pēc tam palaidiet atbilstošos sadales darbus, lai atjauninātu attiecīgās Commerce kanāla datu bāzes ar konfigurācijas izmaiņām.

> [!NOTE]
> Papildus jau esošajam saņemšanas piegādes veidam, kas tiek kopēts uz režģi **Saņemšanas piegādes veids**, kad ieslēdzat līdzekli **Atbalsts vairākiem saņemšanas piegādes veidiem**, katrai papildu izveidotajai saņemšanas piegādes veida konfigurācijai ir jākonfigurē jauni piegādes veidi. Kad pievienojat piegādes veidus režgī **Saņemšanas piegādes veids**, Commerce pārbauda, vai visas aktīvās atvērtās pārdošanas rindas jau tās lieto. Ja tiek atrastas jebkādas atvērtās pārdošanas rindas, saņemsit kļūdas ziņojumu. Piegādes veidi netiek uzskatīti par saņemšanas piegādes veidiem, kamēr visas atvērtās pārdošanas rindas, kas tās izmanto, nav aizslēgtas (vai nu iekļautas rēķinā, vai atceltas).

> [!IMPORTANT]
> Pēc tam, kad lapā **Commerce parametri** tiek definēts vairāk kā viens saņemšanas piegādes veids, līdzeklis **Vairāku saņemšanas piegādes režīmu atbalsts** kļūst obligāts, un to vairs nevar izslēgt. Ja jums ir jāizslēdz līdzeklis, izvēlieties tikai vienu saņemšanas piegādes veidu no režģa **Saņemšanas piegādes veids**. Ja tiek noteikts tikai viens saņemšanas piegādes veids, šis līdzeklis tiek uzskatīts par obligātu, un to var izslēgt.

### <a name="e-commerce-site-configurations"></a>E-commerce vietnes konfigurācijas

Kad ir ieslēgts līdzeklis **Vairāku saņemšanas piegādes režīmu atbalsts**, šādi moduļi e-komercijas lapās parāda jaunos saņemšanas piegādes veidus kā konfigurētus:

- Pirkšanas lodziņš
- Veikala atlasītājs
- Grozs
- Saņemšanas informācija
- Pasūtījuma apstiprināšana
- Pasūtījumu informācija

E-komercijas lapās nav nepieciešamas papildu darbības, lai saņemšanas piegādes veidus padarītu pieejamus.

## <a name="work-with-multiple-pickup-delivery-modes"></a>Darbs ar vairākiem saņemšanas piegādes veidiem

Kad kanālam ir pieejami vairāki saņemšanas piegādes veidi, klientiem tiek nodrošināta uzlabota pieredze, kad tie iepērk preces, kas tiks saņemtas. 

- E-komercijas kanālos pircēji var izvēlēties jebkuru derīgu saņemšanas piegādes veidu, kas ir pieejams. Piemēram, mazumtirgotājs definē divus saņemšanas piegādes veidus (saņemšana veikalā un saņemšana pa ceļam), un tie abi ir konfigurēti režģī **Saņemšanas piegādes veids**, un abi ir derīgi pasūtījuma izpildes kanālam un precei, kuru pircējs pašlaik iegādājas. Šādā gadījumā pircējs var izvēlēties sev vēlamo saņemšanas piegādes veidu. Atlasītais saņemšanas piegādes veids kļūst par piegādes veidu, kas ir saistīts ar pārdošanas pasūtījuma rindu, kad pasūtījums ir izveidots programmā Commerce Headquarters.

    ![E-komercijas saņemšanas opcijas atlasīšana](media/pickupecommerce.png)

- Veikala kanālos, ja klienta pasūtījums saņemšanai tiek veidots, izmantojot pārdošanas punktu (POS) programmu, pārdošanas dalībniekam tiek piedāvāts izvēlēties no pieejamajiem saņemšanas piegādes veidiem, ja tādi ir konfigurēti. Ja kanālam un krājumam ir pieejams tikai viens derīgs saņemšanas piegādes veids, pārdošanas partneris netiek mudināts uz to, lai to izvēlētos. Tā vietā ir pieejams saņemšanas piegādes veids, kas tiek automātiski pielietots pasūtījuma rindām.

    ![Saņemšanas opcijas atlasīšana POS programmā](media/pickuppos.png)

- Kad lietotāji izveido izdošanas pasūtījumus zvanu centra kanālos, viņi var manuāli atlasīt jebkuru definēto saņemšanas piegādes veidu, kas ir saistīts ar zvanu centra kanālu. Pēc tam sistēma pārbauda, ka atlasīto saņemšanas piegādes veidu var izmantot, ja ir pasūtīts krājums, ar kuru tas ir saistīts. Kad zvanu centra kanālos ir izvēlēts saņemšanas piegādes veids, pārdošanas pasūtījuma rindām ir jābūt saistītām ar derīgu veikala noliktavu. Ja zvanu centra pārdošanas rindā nav norādīta veikala noliktava, šai pārdošanas rindai nevar iestatīt saņemšanas piegādes veidu.
- Pārdošanas dalībnieki var izmantot **Pasūtījuma atgriešanas** vai **Pasūtījuma izpildes** darbību POS programmā, lai izgūtu pasūtījumu vai pasūtījuma rindu saņemšanai. Ja pārdošanas asociētais uzņēmums izmanto iepriekš definētu meklēšanas filtru, lai parādītu visus pasūtījumus, kas tiks saņemti izvēlētajā veikalā, vaicājumi tiks modificēti, lai nodrošinātu, ka meklēšanas rezultāti ietver visus atbilstīgos pasūtījumus, kas izmanto jebkuru saņemšanas piegādes veidu. POS lietotāji var arī izmantot esošos filtrus, lai sašaurinātu pasūtījumu sarakstu līdz noteiktam saņemšanas piegādes veidam. Piemēram, tie var rādīt tikai pasūtījumus saņemšanai pa ceļam.

    ![Filtrs saņemšanas piegādes veidiem, kas tiek lietoti pasūtījumu saraksta atsaukšanai](media/pickuprecallorder.png)

## <a name="considerations-for-distributed-order-management"></a>Konfigurācijas sadalīto pasūtījumu pārvaldībai

[Sadales pasūtījumu pārvaldība (DOM)](./dom.md) līdzekļi Commerce ignorē visas pārdošanas rindas, kas ir atzīmētas saņemšanai veikalā. Šie līdzekļi ir atjaunināti, lai nodrošinātu, ka pārdošanas rindas, kas ir saistītas ar konfigurētajiem saņemšanas piegādes veidiem, apiet DOM loģiku un netiek pārdalītas uz jaunu izpildes noliktavu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]