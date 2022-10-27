---
title: Konfigurēt kontu struktūras
description: Šajā rakstā ir sniegta informācija par kontu struktūrām un finanšu dimensijām.
author: aprilolson
ms.date: 10/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: twheeloc
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3fbdd6e2cac61c358848a21e1126bea900e86b2
ms.sourcegitcommit: c6c2486be2359bd30106f7f52bda788239147d8c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/22/2022
ms.locfileid: "9713948"
---
# <a name="configure-account-structures"></a>Kontu struktūru konfigurēšana

[!include[banner](../includes/banner.md)]

Kontu struktūras izmanto galveno kontu un finanšu dimensijas, lai izveidotu kārtulu kopu, kas nosaka konta numura ievadīšanai izmantoto kārtību un vērtības. Varat iestatīt tik daudz kontu struktūru, cik vien nepieciešams jūsu uzņēmumam. Konta struktūras tiek piešķirtas uzņēmuma Virsgrāmatas iestatījumiem, tāpēc tās var koplietot.

Kad veidojat konta struktūru, maksimālais segmentu skaits ir 11. Ja ir nepieciešami vairāk nekā 11 segmenti, pārbaudiet iestatījumus un prasības, jo tas ietekmēs lietotāja pieredzi. Apsveriet, vai segmentu var atvasināt pārskatu veidošanas scenārijā, izmantojot hierarhiju, nevis datu ievades laikā, vai izmantojot lietotāja definētu lauku. Piemēram, ja vēlaties ziņot par vietu, bet atrašanās vietu varat aprēķināt pēc nodaļas vai izmaksu centra, atrašanās vieta nav vajadzīga kā finanšu dimensija. Ja pēc izvērtēšanas izlemjat, ka ir nepieciešams vairāk par 11 segmentiem, papildu segmentus varat pievienot, izmantojot papildu kārtulas.

Kontu struktūrām ir nepieciešams galvenais konts. Galvenais konts nav nepieciešams kā pirmais segments struktūrā, bet tas norāda, kura konta struktūra tiek izmantota konta numura ievades laikā. Tāpēc galvenā konta vērtība var pastāvēt tikai vienā Virsgrāmatā piešķirtai struktūrai, lai tā nepārklātos. Kad konta struktūra ir identificēta, atļauto vērtību saraksts tiek filtrēts, lai nodrošinātu, ka lietotājam ir iespējas izvēlēties tikai derīgas dimensiju vērtības, samazinot nepareiza žurnāla ieraksta iespējamību.

> [!NOTE] 
> Ja budžetu plānojat pret kādu finanšu dimensiju, tai ir jābūt daļai no konta struktūras. Pašlaik budžeta veidošanai netiek izmantotas papildu kārtulas.

## <a name="example"></a>Piemērs
Lai ilustrētu labāko praksi konta struktūras iestatīšanai, pieņemsim, ka uzņēmums vēlas izsekot savus bilances kontus (100000..399999) konta un biznesa vienības finanšu dimensijas līmenī. Ieņēmumu un izdevumu kontiem (400000..999999) uzņēmums izseko finanšu dimensijas Biznesa vienība, Nodaļa un Izmaksu centrs. Ja tiek veikta pārdošana, uzņēmums vēlas izsekot arī dimensiju Debitors. Lietojot šo scenāriju, uzņēmuma Virsgrāmatai ir piešķirtas divas konta struktūras - viena bilances kontiem, viena peļņas un zaudējumu kontiem. Lai optimizētu lietotāja funkcionalitāti un validēšanu, kārtulai Debitors vajadzētu būt papildu kārtulai, kura tiek izmantota tikai tad, kad tiek izmantots pārdošanas konts.

**Bilances konta struktūra**

|Galvenais konts          | Biznesa vienība    |
|----------------------|-----------|
|100000..399999 | *;"&nbsp;"|

**Peļņas un zaudējumu konta struktūra**

|Galvenais konts          | Biznesa vienība    |Nodaļa          | Izmaksu centrs    | &nbsp; |
|----------------------|------------------|--------------------|-----------|---|
|400000..999999 | \*;"&nbsp;"| \*;"&nbsp;"| \*;"&nbsp;"| \*;"&nbsp;"|

**Papildu kārtula Debitora pievienošanai**

Kritēriji: ja Galvenais konts ir no 400000 līdz 499999, tad pievienot debitoru. To nevar atstāt tukšu.

|Debitors         |
|-----------------|
|\* |

Šajā vienkāršotajā piemērā visas vērtības un tukšs tiek atļauti un \* "&nbsp;" tiek izmantoti.

## <a name="segments-and-allowed-values"></a>Segmenti un atļautās vērtības
Sadaļā **Segmenti** un **Informācija par atļautajām vērtībām** ir režģa formas funkcionalitāte, lai ievadītu kārtulas, kas grāmatošanas laikā tiek ievērotas validēšanai. Varat rakstīt tieši režģa šūnās, importēt no Excel vai izmantot sadaļu **Informācija par atļautajām vērtībām**, lai jūs tiktu vadīts caur to.

Sadaļa **Informācija par atļautajām vērtībām** jūs vada caur izveidošanas kritērijiem, izmantojot tādus kritērijus **Operatori** kā, piemēram, sākas ar, ir starp, ietver un daudzus citus.

[![Atļaut vērtības.](./media/account.png)](./media/account.png) 

Atļautās vērtības mainās uz noklusējuma vērtībām žurnāla vai uzskaites sadales ieraksta lapā, ja atbilstoši konta struktūras iestatījumam nav citu iespējamo vērtību, ko atlasīt.

Tālāk ir parādīts struktūras **Peļņas un zaudējumu konta struktūra** piemērs.

|Galvenais konts          | Biznesa vienība    |Nodaļa          | Izmaksu centrs    |
|----------------------|-----------|----------------------|-----------|
|400000..999999 | 002 | 022 | 014 |

Ievadot žurnālu un atlasot kontu peļņas un zaudējumu diapazonā, biznesa vienības “002” atlasīšana izraisīs vērtības 022 un 014 mainīšanos uz noklusējuma vērtībām konta kontrolē. Šī uzvedība notiks arī uzskaites sadales lapā. 

## <a name="more-than-seven-criteria-needed"></a>Nepieciešami vairāk nekā septiņi kritēriji

Ja nepieciešami vairāk nekā septiņi kritēriji, varat turpināt to pievienošanu nākamajā rindā. Strādājot sadaļā Atļautās vērtības detalizēta informācija **, tiks** ievērots, ka **pēc** pievienošanas pievienotie kritēriji vairs nebūs aktīvi. To izraisa daudzi faktori, piemēram, tālāk norādītie. 
 - Kolonnas platums 
 - Datu glabāšanas veids 
 - Vadīklas **Informācija par atļautajām vērtībām** veiktspēja
 - Izmantojamība  

> [!NOTE]
> Jauninājums no Microsoft Dynamics AX 2012. gada, kurā ir norādīti vairāk nekā septiņi kritēriji, netiek atbalstīts. Tas jāizlabo pirms jaunināšanas uz finanšu un operāciju programmām pabeigšanas. 

Lai turpinātu pievienot papildu kritērijus, noklikšķiniet uz **Dublēt segmentā** un **Atļauto vērtību sadaļa**. Tādējādi kritēriji tiek kopēti jaunā rindā. Pēc tam varat tos pārrakstīt vai modificēt sadaļu **Informācija par atļautajām vērtībām**.

## <a name="best-practices"></a>Paraugprakses
Iestatot konta struktūras, var sekot kāda labākā prakse. Taču tās ir tikai vadlīnijas, tādēļ daļu no šīs diskusijas ir jāveido visaptverošai apspriešanai par jūsu uzņēmumu, izaugsmes plānu un uzturēšanas plānu.

- Vispirms vai pēc iespējas tuvāk galvenā konta struktūrai izveidojiet galveno kontu, lai lietotāji iegūtu vislabāko vadīto pieredzi, ko tie var gūt konta ieraksta laikā.
  
  - Pārliecinieties, ka visus trešās puses risinājumus, kurus plānojat izmantot galvenā konta atbalstam pirmajā amatā.

- Pēc iespējas vairāk atkārtoti izmantojiet tās pašas kontu struktūras, lai samazinātu uzturēšanu visās jūsu juridiskajās personās.

- Ja dažādās juridiskajās personās pastāv atšķirības, apsveriet iespēju ieviest papildu kārtulas, lai varētu atkārtoti izmantot tās pašas kontu struktūras.

- Definējot atļautās vērtības, pēc iespējas vairāk izmantojiet diapazonus un aizstājējzīmes. Tādējādi varat ne tikai augt un mainīties, neveicot uzturēšanu, bet ar šo konfigurāciju sistēma turklāt darbojas nevainojamāk.

- Nevar vienkārši pielikt zvaigznīti ikvienam segmentam konta struktūrā un pēc tam paļauties tikai uz papildu kārtulām. To varētu būt grūti pārvaldīt, un šāda konfigurācija bieži izraisa lietotāju kļūdas uzturēšanas laikā, neļaujot sistēmai veikt grāmatošanu.

## <a name="account-structure-activation"></a>Konta struktūras aktivizācija
Kad esat apmierināts ar jauno iestatījumu vai konta struktūras maiņu, jums tas ir jāaktivizē. Ja konta struktūra ir piešķirta kādai virsgrāmatai, šī aktivizēšana var būt ilgstošs process, jo visas negrāmatotās transakcijas sistēmā ir jāsinhronizē ar jauno struktūru. Iegrāmatotās darbības neietekmē konta struktūras izmaiņas. Attiecībā uz programmas versiju 10.0.31 līdzekļu **pārvaldībā** ir pieejama jauna funkcija ar nosaukumu Konta struktūras aktivizēšanas veiktspējas uzlabojumi. Papildinformāciju par šo jauno līdzekli konta struktūras aktivizēšanai skatiet konta struktūras [aktivizēšanas veiktspējas uzlabojumi.](account-structure-improvement.md) 

Papildinformāciju skatiet sadaļā [Kontu plāna, Finanšu dimensiju](plan-chart-of-accounts.md) un [...](financial-dimensions.md)[Konta un dimensiju kombināciju ievadīšana (segmentēta ierakstu kontrole).](enter-account-dimension-combinations-segmented-entry-control.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
