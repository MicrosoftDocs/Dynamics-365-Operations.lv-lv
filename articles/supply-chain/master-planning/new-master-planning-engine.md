---
title: Migrācija uz Plānošanas optimizāciju vispārējai plānošanai
description: Šajā tēmā ir sniegta informācija par jauno vispārējās plānošanas programmu, Plānošanas optimizāciju un par migrēšanu no esošās programmas.
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
ms.openlocfilehash: 598e29ead50e1ecb249a7338c7f0952a912b4f69
ms.sourcegitcommit: cbe9493d479f96f271d94599ec1b85131b26169f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/27/2022
ms.locfileid: "8809100"
---
# <a name="migration-to-planning-optimization-for-master-planning"></a>Migrācija uz Plānošanas optimizāciju vispārējai plānošanai

[!include [banner](../includes/banner.md)]

Iebūvēto vispārējās plānošanas programmu ir paredzēts padarīt par novecojušu (novecojis). Tas tiek aizstāts ar Plānošanas optimizācijas pievienojumprogrammu risinājumam Microsoft Dynamics 365 Supply Chain Management. Šajā tēmā ir sniegta informācija par ietekmi uz jauno un esošo izvietošanu. Tajā ir iekļauta informācija par nepieciešamajām darbībām.

Plānošanas optimizācija ļauj veikt vispārējās plānošanas aprēķinus, kas notiek ārpus Supply Chain Management un Azure SQL datu bāzes. Priekšrocības, kas saistītas ar Plānošanas optimizācijas funkcionalitāti, vispārējās plānošanas izpildes laikā ietver uzlabotu veiktspēju un minimālu ietekmi uz SQL datu bāzi. Jo ātro plānošanu var veikt arī darba stundu laikā, lai plānotāji varētu nekavējoties reaģēt uz pieprasījumu vai parametru izmaiņām.

Papildinformāciju par Plānošanas optimizāciju skatiet sadaļā [Plānošanas optimizācijas apskats](planning-optimization/planning-optimization-overview.md).

## <a name="obsolescence-of-the-existing-master-planning-engine"></a>Esošās vispārējās plānošanas programmas novecošanās

Korporācija Microsoft pašlaik padara iebūvētu plānošanas programmu novecojušu, lai atbalstītu Plānošanas optimizāciju. Šīs izmaiņas ietekmē visas mākoņa vides. Lokālās instalācijas netiek ietekmētas. Versijā 10.0.16 un jaunākās tiks parādīts kļūdas ziņojums, ja palaižat iebūvēto vispārējo plānošanu, neveidojot plānotos ražošanas pasūtījumus. Tomēr vispārējās plānošanas izpilde tiks veiksmīgi pabeigta, neskatoties uz kļūdas ziņojumu.

Lai iegūtu vairāk informācijas par iebūvētās plānošanas programmas novecošanos, skatiet paziņojumus par [Noņemtajiem vai novecojušiem līdzekļiem sadaļā Dynamics 365 Supply Chain Management](../get-started/removed-deprecated-features-scm-updates.md).

## <a name="migration-messages-and-exceptions"></a>Migrācija, ziņojumi un izņēmumi

Īpašnieki, kam pieder esošās vides, kurās darbojas iebūvētā vispārējās plānošanas programma bez plānoto ražošanas pasūtījumu ģenerēšanas, saņems e-pastu ar sīkāku informāciju par izņēmuma procesu. Iesakām jums strādāt ar partneri, lai novērtētu un plānotu migrāciju uz plānošanas optimizāciju.

Kā minēts iepriekš versijā 10.0.16 un jaunākās tiks parādīts kļūdas ziņojums, ja palaižat iebūvēto vispārējo plānošanu, neveidojot plānotos ražošanas pasūtījumus. Šis kļūdas ziņojums ietver norādījumus par migrāciju un norādījumus par izņēmuma pieprasīšanu.

### <a name="new-deployments"></a>Jauni izvietojumi

Plānošanas optimizāciju ir jāuzskata par noklusējuma vispārējās plānošanas programmu visām jaunajām izvietošanām mākonī. Vispārīgi Plānošanas optimizācija ir jāizmanto visiem jaunajiem izvietojumiem, kas vispārējās plānošanas laikā neģenerē plānotos ražošanas pasūtījumus. Ja jauns izvietojums ir atkarīgs no funkcionalitātes, ko plānošanas optimizācija pašlaik neatbalsta, varat pieprasīt izņēmumu, lai varētu turpināt izmantot iebūvēto vispārējās plānošanas programmu.

### <a name="existing-deployments"></a>Esošās izvietošanas

Esošo mākonī balstītu izvietojumu īpašnieki, kas atkarīgi no vispārējās plānošanas, plāno migrēt uz plānošanas optimizāciju. Ja jūsu ieviešana ir atkarīga no funkcionalitātes, ko plānošanas optimizācija pašlaik neatbalsta, varat pieprasīt izņēmumu, lai varētu turpināt izmantot iebūvēto vispārējās plānošanas programmu.

Vidēm, kas pašlaik izmanto vispārējās plānošanas procesus, kas ir novecojuši, korporācija Microsoft nosūtīs e-pastu vides administratoram. Šī e-pasta adrese sniegs informāciju par darbībām, kas nepieciešamas, lai migrētu vai pieprasītu izņēmumu.

## <a name="the-exception-process"></a>Izņēmuma process

Varat pieprasīt izņēmumu, ja ir jāturpina izmantot iebūvēto vispārējās plānošanas programmu, jo jūsu biznesa procesi lielā mērā ir atkarīgi vismaz no viena līdzekļa, kas pašlaik nav ieviests plānošanas optimizācijā. Pieejamo līdzekļu sarakstu skatiet šeit: [Plānošanas optimizācijas ietilpināšanas analīze](planning-optimization/planning-optimization-fit-analysis.md).

Šobrīd migrācijas izņēmumi plānošanas optimizācijā ir aktuāli tikai tad, ja vispārējās plānošanas process neiekļauj ražošanu (tas ir, vispārējās plānošanas ģenerētus plānotos ražošanas pasūtījumus), un jums nepieciešama iebūvētā vispārējās plānošanas programmas versija, kas jaunāka par versiju 10.0.15.

Pēc tam, kad būs pieejamas nepieciešamās funkcijas, korporācija Microsoft nodrošinās pagarinājuma periodu līdz izņēmuma termiņa beigām. Vides administrators tiks informēts, kad vajadzīgie līdzekļi ir kļuvuši pieejami un pagarinājuma periods ir sācies.

Šajā plūsmkartē ir apkopota šajā tēmā sniegtā informācija, lai varētu ātri noteikt, vai ir jāpieprasa izņēmums. Ja nepieciešams pieprasīt izņēmumu, lūdzu, aizpildiet un iesniedziet [Plānošanas optimizācijas migrācijas un izņēmuma anketu](https://go.microsoft.com/fwlink/?linkid=2144962). Preču grupa ir atbildīga par katra izņēmuma pieprasījuma vērtēšanu un apstiprināšanu, tāpēc, lūdzu, iesniedziet savu pieprasījumu tieši preču grupai, izmantojot norādīto saiti, un neveidojiet tai atbalsta biļeti. Ja jūsu pieprasījums tiek noraidīts, lūdzu, neveidojiet atbalsta biļeti, jo Microsoft Support nevar atkārtoti novērtēt vai piešķirt izņēmumus.

![Izņēmumu plūsmkarte.](media/exception-diagram.png "Izņēmumu plūsmkarte")

> [!NOTE]
> Var pieprasīt izņēmumu tikai nomniekiem, kas pašlaik ietver vai ietvers ražošanas vidi, nevis tikai nomniekiem ar smilškastes vidēm. Ja ir jāatspējo Plānošanas optimizācijas izņēmuma kļūda infrastruktūrā kā pakalpojuma (IaaS) smilškastes vidē, palaidiet SQL vaicājumu, kas ir nodrošināts [Smilškastes vidē](#faq-sandbox).

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi

### <a name="sandbox-environments"></a><a name="faq-sandbox"></a>Smilškastes vides

Vai var izmantot iebūvēto vispārējo plānošanu manā smilškastes vidē? Vai man ir nepieciešams izņēmums?

**Atbilde:** izņēmumi parasti neattiecas uz smilškastes vidēm, jo plānošanas optimizācijas izņēmuma kļūda neaizkavē iebūvētās vispārējās plānošanas programmas veiksmīgu palaišanu. Tomēr, ja kļūdas ziņojums traucē, varat to deaktivizēt uz IaaS (ne Service Fabrics) smilškastes vidi, jūsu datu bāzē izpildot šādu vaicājumu:

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

**Atbilde:** Nē. Lokālajai videi izņēmums nav nepieciešams. Varat turpināt izmantot iebūvēto vispārējo plānošanu. Jūsu vides administrators tiks informēts, ja ir nepieciešama kāda darbība.

### <a name="production-scenarios"></a>Ražošanas scenāriji

Mēs izmantojam plānotos ražošanas pasūtījumus, bet es esmu norūpējies par to, kas notiks, kad mēs jauninām uz versiju 10.0.16. Vai man nepieciešams veikt kādu darbību?

**Atbilde:** Jums nav jāraizējas. Varat turpināt izmantot iebūvēto vispārējo plānošanu versijā 10.0.16. Tomēr mēs iesakām izvērtēt, vai migrāciju uz plānošanas optimizāciju var sākt ar pašreizējo funkcionalitāti. Mēs arī iesakām palikt informētam par jauno funkcionalitāti.

### <a name="email-from-microsoft"></a>E-pasts no Microsoft

Mūsu vides administrators saņēma e-pastu no Microsoft. Šajā e-pastā teikts, ka mums jāmigrē uz plānošanas optimizāciju vai jāpieprasa izņēmums. Vai man jāveic kāda darbība?

**Atbilde:** Jā. Jūsu vide tiks ietekmēta, ja jūs neievērosiet instrukcijas e-pastā. Jūs varat vai nu migrēt uz plānošanas optimizāciju līdz norādītajam datumam vai pieprasīt izņēmumu, izmantojot e-pasta saiti. Šī saite atver anketu. Kad esat pabeidzis un iesniedzis šo anketu, jūs saņemsiet atbildi pa e-pastu. Kaut arī šis process ir manuāls, korporācija Microsoft mēģina atbildēt nedēļas laikā pēc tam, kad anketa ir iesniegta.

### <a name="error-messages"></a>Kļūdu ziņojumi

Es lietoju versiju 10.0.16 vai jaunāku, un, palaižot vispārējo plānošanu, es saņemu šādu kļūdas ziņojumu. Vai vispārējā plānošana ir bloķēta?

> Šis kļūdas ziņojums tiek parādīts, jo iebūvētā vispārējās plānošanas programma tika izmantota scenārijiem, ko atbalsta plānošanas optimizācija. Tagad jums vajadzētu migrēt uz plānošanas optimizāciju, jo pašreizējā iebūvētā vispārējā plānošana ir novecojusi. Ievērojiet, ka šī vispārējās plānošanas izpilde tika pabeigta sekmīgi.
>
> Ja jūsu migrācijai ir stipras atkarības no nepabeigtiem līdzekļiem, var tikt pieprasīta atkāpe no iebūvētās vispārējās plānošanas programmas ilgstošas izmantošanas.
>
> Lūdzu, aizpildiet šo anketu, lai sāktu darbu, un, ja nepieciešams pieprasiet izņēmumu no migrācijas uz plānošanas optimizāciju.

**Atbilde:** Nē, vispārējā plānošana netiek bloķēta. Vispārējās plānošanas izpilde tika veiksmīgi pabeigta, un rezultātu var izmantot parastajā veidā. Tomēr, lai izvairītos no šī kļūdas ziņojuma saņemšanas turpmākās vispārējās plānošanas izpildes laikā, jums ir nekavējoties jāmigrē uz plānošanas optimizāciju vai jāpieprasa izņēmums, izmantojot saiti kļūdas ziņojumā.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
