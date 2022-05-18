---
title: Kontu struktūru konfigurēšana
description: Šajā tēmā ir sniegta informācija par kontu struktūrām un finanšu dimensijām.
author: aprilolson
ms.date: 06/03/2019
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
ms.openlocfilehash: c775703047f4d2ccf2b1c35e2810c015ee1c1506
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722609"
---
# <a name="configure-account-structures"></a>Kontu struktūru konfigurēšana

[!include[banner](../includes/banner.md)]

Kontu struktūras izmanto galveno kontu un finanšu dimensijas, lai izveidotu kārtulu kopu, kas nosaka konta numura ievadīšanai izmantoto kārtību un vērtības. Varat iestatīt tik daudz kontu struktūru, cik vien nepieciešams jūsu uzņēmumam. Kontu struktūras ir piešķirtas uzņēmuma virsgrāmatas iestatījumiem, tāpēc tās var koplietot.

Kad veidojat konta struktūru, maksimālais segmentu skaits ir 11. Ja ir nepieciešams vairāk segmentu, nekā šeit noteikts, rūpīgi izvērtējiet savus iestatījumus un prasības, jo tas ietekmēs lietotāja funkcionalitāti. Apsveriet, vai segmentu var atvasināt pārskatu veidošanas scenārijā, izmantojot hierarhiju, nevis datu ievades laikā, vai izmantojot lietotāja definētu lauku. Piemēram, ja vēlaties ziņot par atrašanās vietu, bet atrašanās vietu varat noteikt pēc nodaļas vai izmaksu centra, jums atrašanās vieta nav nepieciešama kā finanšu dimensija. Ja pēc izvērtēšanas izlemjat, ka ir nepieciešams vairāk par 11 segmentiem, papildu segmentus varat pievienot, izmantojot papildu kārtulas.

Kontu struktūrām ir nepieciešams galvenais konts. Galvenajam kontam nav jābūt pirmajam segmentam struktūrā, bet tas identificē konta struktūru, kura tiek lietota konta numura ievadīšanas laikā. Šī iemesla dēļ galvenā konta vērtība var pastāvēt tikai vienā virsgrāmatai piešķirtā struktūrā, lai tās nepārklātos. Kad konta struktūra ir identificēta, atļauto vērtību saraksts tiek filtrēts, lai nodrošinātu, ka lietotājam ir iespējas izvēlēties tikai derīgas dimensiju vērtības, samazinot nepareiza žurnāla ieraksta iespējamību.

> [!NOTE] 
> Ja budžetu plānojat pret kādu finanšu dimensiju, tai ir jābūt daļai no konta struktūras. Pašlaik budžeta veidošanai netiek izmantotas papildu kārtulas.

## <a name="example"></a>Piemērs
Lai ilustrētu labāko praksi konta struktūras iestatīšanai, pieņemsim, ka uzņēmums vēlas izsekot savus bilances kontus (100000..399999) konta un biznesa vienības finanšu dimensijas līmenī. Ieņēmumu un izdevumu kontiem (400000..999999) uzņēmums izseko finanšu dimensijas Biznesa vienība, Nodaļa un Izmaksu centrs. Ja tiek veikta pārdošana, uzņēmums vēlas izsekot arī dimensiju Debitors. Izmantojot šo scenāriju, būtu ieteicams, lai uzņēmuma virsgrāmatai būtu piešķirtas divas kontu struktūras — viena struktūra bilances kontiem un viena — peļņas un zaudējumu kontiem. Lai optimizētu lietotāja funkcionalitāti un validēšanu, kārtulai Debitors vajadzētu būt papildu kārtulai, kura tiek izmantota tikai tad, kad tiek izmantots pārdošanas konts.

**Bilances konta struktūra**

|Galvenais konts          | Biznesa vienība    |
|----------------------|-----------|
|100000..399999 | *;” “|

**Peļņas un zaudējumu konta struktūra**

|Galvenais konts          | Biznesa vienība    |Nodaļa          | Izmaksu centrs    | &nbsp; |
|----------------------|------------------|--------------------|-----------|---|
|400000..999999 | \*;” “| \*;” “| \*;” “| \*;” “|

**Papildu kārtula Debitora pievienošanai**

Kritēriji: ja Galvenais konts ir no 400000 līdz 499999, tad pievienot debitoru. To nedrīkst atstāt tukšu.

|Debitors         |
|-----------------|
|* |

Šajā vienkāršotajā piemērā ir atļautas visas vērtības un tukši lauki, tādēļ tiek izmantotas vērtības * un “ “.

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

## <a name="more-than-7-criteria-needed"></a>Ir nepieciešams vairāk par 7 kritērijiem

Ja jums ir jāizmanto vairāk par 7 kritērijiem, varat turpināt, pievienojot tos nākamajā rindā. Strādājot sadaļā Atļautās vērtības detalizēta informācija **, tiks** ievērots, ka **pēc** pievienošanas pievienotie kritēriji vairs nebūs aktīvi. To izraisa daudzi faktori, piemēram, tālāk norādītie. 
 - Kolonnas platums 
 - Datu glabāšanas veids 
 - Vadīklas **Informācija par atļautajām vērtībām** veiktspēja
 - Izmantojamība  
 
Lai turpinātu pievienot papildu kritērijus, noklikšķiniet uz **Dublēt segmentā** un **Atļauto vērtību sadaļa**. Tādējādi kritēriji tiek kopēti jaunā rindā. Pēc tam varat tos pārrakstīt vai modificēt sadaļu **Informācija par atļautajām vērtībām**.

## <a name="best-practices"></a>Noteikumi
Iestatot kontu struktūras, varat ievērot dažas labākās prakses. Taču tās ir tikai vadlīnijas, tādēļ daļu no šīs diskusijas ir jāveido visaptverošai apspriešanai par jūsu uzņēmumu, izaugsmes plānu un uzturēšanas plānu.

- Galveno kontu izveidojiet kā pirmo vai pēc iespējas tuvāk konta struktūras sākumam, lai konta ievadīšanas laikā lietotāji saņemtu pēc iespējas labāku vadīto funkcionalitāti.

- Pēc iespējas vairāk atkārtoti izmantojiet tās pašas kontu struktūras, lai samazinātu uzturēšanu visās jūsu juridiskajās personās.

- Ja dažādās juridiskajās personās pastāv atšķirības, apsveriet iespēju ieviest papildu kārtulas, lai varētu atkārtoti izmantot tās pašas kontu struktūras.

- Definējot atļautās vērtības, pēc iespējas vairāk izmantojiet diapazonus un aizstājējzīmes. Tādējādi varat ne tikai augt un mainīties, neveicot uzturēšanu, bet ar šo konfigurāciju sistēma turklāt darbojas nevainojamāk.

- Nevar vienkārši pielikt zvaigznīti ikvienam segmentam konta struktūrā un pēc tam paļauties tikai uz papildu kārtulām. To varētu būt grūti pārvaldīt, un šāda konfigurācija bieži izraisa lietotāju kļūdas uzturēšanas laikā, neļaujot sistēmai veikt grāmatošanu.

## <a name="account-structure-activation"></a>Konta struktūras aktivizācija
Kad esat apmierināts ar jauno iestatījumu vai konta struktūras maiņu, jums tas ir jāaktivizē. Ja konta struktūra ir piešķirta kādai virsgrāmatai, šī aktivizēšana var būt ilgstošs process, jo visas negrāmatotās transakcijas sistēmā ir jāsinhronizē ar jauno struktūru. Konta struktūras izmaiņām nav ietekmes uz grāmatotajām transakcijām.

Papildinformāciju skatiet tēmās [Kontu plānu plānošana](plan-chart-of-accounts.md), [Finanšu dimensijas](financial-dimensions.md) un [Konta un dimensiju kombināciju ievade (segmentētu ierakstu kontrole)](enter-account-dimension-combinations-segmented-entry-control.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
