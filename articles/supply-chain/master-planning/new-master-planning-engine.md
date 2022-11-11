---
title: Migrācija uz Plānošanas optimizāciju vispārējai plānošanai
description: Šajā rakstā ir sniegta informācija par jauno vispārējās plānošanas programmu, plānošanas optimizāciju un par migrāciju no esošās programmas.
author: t-benebo
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: ''
ms.author: benebotg
ms.search.validFrom: 2020-11-05
ms.dyn365.ops.version: ''
ms.openlocfilehash: dbbc58f0dcd833f63e84a73ac68ada60bd0c291d
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739956"
---
# <a name="migration-to-planning-optimization-for-master-planning"></a>Migrācija uz Plānošanas optimizāciju vispārējai plānošanai

[!include [banner](../includes/banner.md)]

Iebūvēto vispārējās plānošanas programmu ir paredzēts padarīt par novecojušu (novecojis). Tas tiek aizstāts ar Plānošanas optimizācijas pievienojumprogrammu risinājumam Microsoft Dynamics 365 Supply Chain Management. Šajā rakstā ir sniegta informācija par ietekmi uz jauniem un esošiem izvietojumiem. Tajā ir iekļauta informācija par nepieciešamajām darbībām.

Plānošanas optimizācija ļauj veikt vispārējās plānošanas aprēķinus, kas notiek ārpus Supply Chain Management un Azure SQL datu bāzes. Priekšrocības, kas saistītas ar Plānošanas optimizācijas funkcionalitāti, vispārējās plānošanas izpildes laikā ietver uzlabotu veiktspēju un minimālu ietekmi uz SQL datu bāzi. Jo ātro plānošanu var veikt arī darba stundu laikā, lai plānotāji varētu nekavējoties reaģēt uz pieprasījumu vai parametru izmaiņām.

Papildinformāciju par plānošanas optimizāciju skatiet vispārējās [plānošanas sistēmas arhitektūrā](master-planning-architecture.md).

## <a name="obsolescence-of-the-existing-master-planning-engine"></a>Esošās vispārējās plānošanas programmas novecošanās

Microsoft pašlaik veic novecojušu vispārējās plānošanas programmu novecojušu plānošanas optimizāciju. Šīs izmaiņas ietekmē visas mākoņa vides. Lokālās instalācijas netiek ietekmētas. Versijā 10.0.16 un vēlāk, palaižot novecojušu vispārējās plānošanas programmu, neveidojot plānotos ražošanas pasūtījumus, saņemsit kļūdas ziņojumu. Tomēr vispārējās plānošanas izpilde tiks veiksmīgi pabeigta, neskatoties uz kļūdas ziņojumu.

Papildinformāciju par novecojušu vispārējās plānošanas programmu skatiet paziņojumus [sadaļā Noņemtie vai novecojušie līdzekļi Dynamics 365 Supply Chain Management](../get-started/removed-deprecated-features-scm-updates.md).

## <a name="migration-messages-and-exceptions"></a>Migrācija, ziņojumi un izņēmumi

Esošo vides īpašnieki, kas palaiž novecojušu vispārējās plānošanas programmu, neveidojot plānotus ražošanas pasūtījumus, saņems e-pastu, kas nodrošina detalizētu informāciju par izņēmumu procesu. Iesakām jums strādāt ar partneri, lai novērtētu un plānotu migrāciju uz plānošanas optimizāciju.

Kā tika norādīts, saņemsit kļūdas ziņojumu versijā 10.0.16 un vēlāk, ja palaižat novecojušu vispārējās plānošanas programmu, neveidojot plānotos ražošanas pasūtījumus. Šis kļūdas ziņojums ietver norādījumus par migrāciju un norādījumus par izņēmuma pieprasīšanu.

### <a name="new-deployments"></a>Jauni izvietojumi

Plānošanas optimizāciju ir jāuzskata par noklusējuma vispārējās plānošanas programmu visām jaunajām izvietošanām mākonī. Vispārīgi Plānošanas optimizācija ir jāizmanto visiem jaunajiem izvietojumiem, kas vispārējās plānošanas laikā neģenerē plānotos ražošanas pasūtījumus. Ja jaunā izvietošana ir atkarīga no funkcionalitātes, ko pašlaik neatbalsta plānošanas optimizācija, varat pieprasīt izņēmumu, tādējādi varat turpināt izmantot novecojušu vispārējās plānošanas programmu.

### <a name="existing-deployments"></a>Esošās izvietošanas

Esošo mākonī balstītu izvietojumu īpašnieki, kas atkarīgi no vispārējās plānošanas, plāno migrēt uz plānošanas optimizāciju. Ja jūsu ieviešana ir atkarīga no funkcionalitātes, ko šobrīd neatbalsta plānošanas optimizācija, varat pieprasīt izņēmumu, tādējādi varat turpināt izmantot novecojušu vispārējās plānošanas programmu.

Vidēm, kas pašlaik izmanto vispārējās plānošanas procesus, kas ir novecojuši, korporācija Microsoft nosūtīs e-pastu vides administratoram. Šī e-pasta adrese sniegs informāciju par darbībām, kas nepieciešamas, lai migrētu vai pieprasītu izņēmumu.

## <a name="the-exception-process"></a>Izņēmuma process

Varat pieprasīt izņēmumu, ja jums ir jāturpina izmantot novecojušu vispārējās plānošanas programmu, jo biznesa procesi ir atkarīgi no vismaz vienas pašlaik neieviešamās funkcionalitātes plānošanas optimizācijā. Pieejamo līdzekļu sarakstu skatiet šeit: [Plānošanas optimizācijas ietilpināšanas analīze](planning-optimization/planning-optimization-fit-analysis.md).

Šobrīd optimizācijas migrācijas plānošanas izņēmumi ir svarīgi tikai tad, ja vispārējās plānošanas procesā nav ietverta ražošana (t.i., plānotie ražošanas pasūtījumi, kas tiek ģenerēti vispārējās plānošanas ietvaros) un ir nepieciešama novecojusi vispārējās plānošanas programma papildus versijai 10.0.15.

Pēc tam, kad būs pieejamas nepieciešamās funkcijas, korporācija Microsoft nodrošinās pagarinājuma periodu līdz izņēmuma termiņa beigām. Vides administrators tiks informēts, kad vajadzīgie līdzekļi ir kļuvuši pieejami un pagarinājuma periods ir sācies.

Šajā plūsmkartē tiek apkopota šajā rakstā sniegtā informācija, tādējādi varat ātri noteikt, vai ir jāpieprasa izņēmums. Ja nepieciešams pieprasīt izņēmumu, lūdzu, aizpildiet un iesniedziet [Plānošanas optimizācijas migrācijas un izņēmuma anketu](https://go.microsoft.com/fwlink/?linkid=2144962). Preču grupa ir atbildīga par katra izņēmuma pieprasījuma vērtēšanu un apstiprināšanu, tāpēc, lūdzu, iesniedziet savu pieprasījumu tieši preču grupai, izmantojot norādīto saiti, un neveidojiet tai atbalsta biļeti. Ja jūsu pieprasījums tiek noraidīts, lūdzu, neveidojiet atbalsta biļeti, jo Microsoft Support nevar atkārtoti novērtēt vai piešķirt izņēmumus.

![Izņēmumu plūsmkarte.](media/exception-diagram.png "Izņēmumu plūsmkarte")

> [!NOTE]
> Var pieprasīt izņēmumu tikai nomniekiem, kas pašlaik ietver vai ietvers ražošanas vidi, nevis tikai nomniekiem ar smilškastes vidēm. Ja ir jāatspējo Plānošanas optimizācijas izņēmuma kļūda infrastruktūrā kā pakalpojuma (IaaS) smilškastes vidē, palaidiet SQL vaicājumu, kas ir nodrošināts [Smilškastes vidē](#faq-sandbox).

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi

### <a name="sandbox-environments"></a><a name="faq-sandbox"></a>Smilškastes vides

Vai ikstlodziņa vidē var izmantot vispārējās plānošanas programmu, kas ir novecojusi? Vai man ir nepieciešams izņēmums?

**Atbilde:** izņēmumi parasti nav saistīti ar kastu vides, jo plānošanas optimizācijas izņēmuma kļūda neļaus veiksmīgi palaist novecojušu vispārējās plānošanas programmu. Tomēr, ja kļūdas ziņojums traucē, varat to deaktivizēt uz IaaS (ne Service Fabrics) smilškastes vidi, jūsu datu bāzē izpildot šādu vaicājumu:

```sql
-- Insert or update an enabled flight:
DECLARE @flightName NVARCHAR(100) = 'ReqPlanningOptimizationExceptionToggle';
IF NOT EXISTS (SELECT TOP 1 1 FROM SysFlighting WHERE flightName = @flightName)
    INSERT INTO SYSFLIGHTING(FLIGHTNAME,ENABLED, FLIGHTSERVICEID,PARTITION)
    SELECT @flightName, 1, 12719367,RECID FROM DBO.[PARTITIONS];
ELSE
    UPDATE SysFlighting SET enabled = 1, flightServiceId = 12719367 WHERE flightName = @flightName;
```

### <a name="on-premises-environments"></a>Lokālas vides

Mana vide ir lokāla vide. Vai man ir nepieciešams izņēmums?

**Atbilde:** Nē. Lokālajai videi izņēmums nav nepieciešams. Varat turpināt izmantot novecojušu vispārējās plānošanas programmu. Jūsu vides administrators tiks informēts, ja ir nepieciešama kāda darbība.

### <a name="production-scenarios"></a>Ražošanas scenāriji

Mēs izmantojam plānotos ražošanas pasūtījumus, bet es esmu norūpējies par to, kas notiks, kad mēs jauninām uz versiju 10.0.16. Vai man nepieciešams veikt kādu darbību?

**Atbilde:** Jums nav jāraizējas. Varat turpināt izmantot novecojušu vispārējās plānošanas programmu versijā 10.0.16. Tomēr mēs iesakām izvērtēt, vai migrāciju uz plānošanas optimizāciju var sākt ar pašreizējo funkcionalitāti. Mēs arī iesakām palikt informētam par jauno funkcionalitāti.

### <a name="email-from-microsoft"></a>E-pasts no Microsoft

Mūsu vides administrators saņēma e-pastu no Microsoft. Šajā e-pastā teikts, ka mums jāmigrē uz plānošanas optimizāciju vai jāpieprasa izņēmums. Vai man jāveic kāda darbība?

**Atbilde:** Jā. Jūsu vide tiks ietekmēta, ja jūs neievērosiet instrukcijas e-pastā. Jūs varat vai nu migrēt uz plānošanas optimizāciju līdz norādītajam datumam vai pieprasīt izņēmumu, izmantojot e-pasta saiti. Šī saite atver anketu. Kad esat pabeidzis un iesniedzis šo anketu, jūs saņemsiet atbildi pa e-pastu. Kaut arī šis process ir manuāls, korporācija Microsoft mēģina atbildēt nedēļas laikā pēc tam, kad anketa ir iesniegta.

### <a name="error-messages"></a>Kļūdu ziņojumi

Es lietoju versiju 10.0.16 vai jaunāku, un, palaižot vispārējo plānošanu, es saņemu šādu kļūdas ziņojumu. Vai vispārējā plānošana ir bloķēta?

> Šis kļūdas ziņojums tiek parādīts, jo novecojusi vispārējās plānošanas programma tika izmantota scenārijos, kurus atbalsta Optimizācijas plānošana. Migrēt uz Plānošanas optimizāciju tagad, jo iebūvētā vispārējās plānošanas programma ir novecojusi. Ievērojiet, ka šī vispārējās plānošanas izpilde tika pabeigta sekmīgi.
>
> Ja migrācijai ir stipras atkarības no nenokārtotajām funkcijām, var tikt pieprasīts izņēmums no novecojuša vispārējās plānošanas programmas nepārtrauktas lietošanas.
>
> Lūdzu, aizpildiet šo anketu, lai sāktu darbu, un, ja nepieciešams pieprasiet izņēmumu no migrācijas uz plānošanas optimizāciju.

**Atbilde:** Nē, vispārējā plānošana netiek bloķēta. Vispārējās plānošanas izpilde tika veiksmīgi pabeigta, un rezultātu var izmantot parastajā veidā. Tomēr, lai izvairītos no šī kļūdas ziņojuma saņemšanas turpmākās vispārējās plānošanas izpildes laikā, jums ir nekavējoties jāmigrē uz plānošanas optimizāciju vai jāpieprasa izņēmums, izmantojot saiti kļūdas ziņojumā.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
