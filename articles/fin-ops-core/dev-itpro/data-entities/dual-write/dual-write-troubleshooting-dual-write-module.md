---
title: Problēmu novēršana saistībā ar duālā ieraksta moduli Finance and Operations programmās
description: Šajā tēmā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas ar duālā ieraksta moduli Finance and Operations lietojumprogrammās.
author: RamaKrishnamoorthy
ms.date: 08/10/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 90ff55540c153ef4f3ac07bf5316a3abb4755f2c
ms.sourcegitcommit: caa41c076f731f1e02586bc129b9bc15a278d280
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/13/2021
ms.locfileid: "7380144"
---
# <a name="troubleshoot-dual-write-issues-in-finance-and-operations-apps"></a>Problēmu novēršana saistībā ar duālā ieraksta moduli Finance and Operations programmās

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā rakstā ir sniegta informācija par problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Dataverse. Konkrēti, šajā tēmā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas ar moduli **Duālais ieraksts** Finance and Operations lietojumprogrammās.

> [!IMPORTANT]
> Dažas no problēmām, kas risinātas šajā tēmā, var būt nepieciešama vai nu sistēmas administratora loma, vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati. Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Nevar ielādēt duālā ieraksta moduli Finance and Operations lietojumprogrammā

Ja nevarat atvērt lapu **Duālais ieraksts**, atlasot elementu **Duālais ieraksts** darbvietā **Datu pārvaldība**, visticamāk nedarbojas datu integrācijas pakalpojums. Izveidojiet atbalsta biļeti, lai pieprasītu datu integrācijas pakalpojuma restartēšanu.

## <a name="error-when-you-try-to-create-a-new-table-map"></a>Kļūda, mēģinot izveidot jaunu tabulas karti

**Nepieciešamie akreditācijas dati, lai labotu problēmu:** tas pats lietotājs, kas iestata duālo rakstīšanu.

Mēģinot konfigurēt jaunu tabulu duālajam ierakstam, jūs varētu saņemt šādu kļūdas ziņojumu. Vienīgais lietotājs, kas var izveidot karti, ir lietotājs, kas uzstāda duālās rakstīšanas savienojumu.

*Atbildes statusa kods nenorāda uz veiksmi: 401 (nesankcionēts).*

## <a name="error-when-you-open-the-dual-write-user-interface"></a>Kļūda, atverot duālā ieraksta lietotāja interfeisu

Mēģinot piekļūt duālajam ierakstam no **Datu pārvaldības** darbvietas, var tikt parādīts šāds kļūdas ziņojums:

*login.microsoftonline.com atteicās izveidot savienojumu.*

Lai labotu problēmu, piesakieties, izmantojot InPrivate logu pakalpojumā Microsoft Edge, inkognito logu pakalpojumā Chromium vai inkognito logu pārlūkprogrammā Google Chrome. Ir arī jāatbloķē vai jādzēš trešās puses sīkfaili.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a>Kļūda, saistot vidi divējādai rakstīšanai vai pievienot jaunu tabulas kartēšanu

**Nepieciešamās lomas, lai labotu problēmu:** sistēmas administrators abās Finance and Operations lietojumprogrammās un Dataverse.

Sasaistot vai veidojot kartes, var rasties šādas kļūdas:

```dos
Response status code does not indicate success: 403 (tokenexchange).
Session ID: \<your session id\>
Root activity ID: \<your root activity\> id
```

Šī kļūda var rasties, ja jums nav nepieciešamo atļauju, lai saistītu duālo ierakstu vai izveidotu kartes. Šī kļūda var parādīties arī tad, ja Dataverse vide ir atiestatīta, nesaistot duālo rakstīšanu. Ikviens lietotājs ar sistēmas administratora lomu abās Finance and Operations lietojumprogrammās un Dataverse var saistīt vides. Tikai lietotājs, kas iestatījis duālās rakstīšanas savienojumu, var pievienot jaunas tabulas kartes. Pēc iestatīšanas jebkurš lietotājs ar sistēmas administratora lomu var pārraudzīt statusu un rediģēt kartēšanas.

## <a name="error-when-you-stop-the-table-mapping"></a>Kļūda, apturot tabulas kartēšanu

Mēģinot apturēt tabulas kartēšanu, jūs varētu saņemt šādu kļūdas ziņojumu:

*\[Aizliegts\], \[{"statuss": 403, "avots": ","ziņojums":"Kļūda no marķiera maiņas: lietotājam nav atļauts piekļūt savienojumam dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], Attālais serveris atgrieza kļūdu: (403) Aizliegts.*

Šī kļūda rodas, ja nav pieejama saistītā Dataverse vide.

Lai atrisinātu problēmu, izveidojiet biļeti datu integrācijas grupai. Pievienojiet tīkla izsekošanu, lai datu integrācijas grupa varētu atzīmēt kartes kā **Nedarbojošās** aizmugursistēmā.

## <a name="errors-while-trying-to-start-a-table-mapping"></a>Kļūdas, mēģinot sākt tabulas kartēšanu

### <a name="unable-to-complete-initial-data-sync"></a>Nevar pabeigt sākotnējo datu sinhronizāciju.

Mēģinot palaist sākotnējo sinhronizēšanu, jūs varētu saņemt šādu kļūdas ziņojumu:

*Nevar pabeigt sākotnējo datu sinhronizāciju. Kļūda: duālās rakstīšanas kļūme - spraudņa reģistrācija neizdevās: nevar izveidot duālās rakstīšanas uzmeklēšanas metadatus. Kļūdas objekta atsauce nav iestatīta uz objekta instanci.*

Mēģinot iestatīt šo kartēšanas stāvokli uz **Darbojas**, var tikt parādīta šāda kļūda: Šīs kļūdas labojums ir atkarīgs no kļūdas cēloņa:

+ Ja kartēšanai ir atkarīgi kartējumi, pārliecinieties, ka iespējojat šīs tabulas kartēšanas atkarīgos kartējumus.
+ Kartēšanai var trūkt avota vai mērķa kolonnu. Ja trūkst kolonnas programmā Finance and Operations, izpildiet sekojošos soļus sadaļā [Tabulu kolonnu trūkums kartēs](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps). Ja trūkst lauks programmā Dataverse, noklikšķiniet uz pogas **Atsvaidzināt tabulas** kartēšanā, lai kolonnas tiktu automātiski novirzītas atpakaļ kartēšanā.

### <a name="version-mismatch-error-and-upgrading-dual-write-solutions"></a>Versiju neatbilstības kļūda un duālo rakstīšanas risinājumu jaunināšana

Mēģinot apturēt tabulas kartēšanu, jūs varētu saņemt šādus kļūdas ziņojumus:

+ *Debitoru grupas (msdyn_customergroups) : duālā rakstīšanas kļūme — Dynamics 365 for Sales risinājumam 'Dynamics365Company' ir versiju neatbilstība. Versija: '2.0.2.10' Nepieciešamā versija: '2.0.133'*
+ *Dynamics 365 for Sales risinājumam 'Dynamics365FinanceExtended' ir versijas neatbilstība. Versija: '1.0.0.0' Nepieciešamā versija: '2.0.227'*
+ *Dynamics 365 for Sales risinājumam 'Dynamics365FinanceAndOperationsCommon'  ir versijas neatbilstība. Versija: '1.0.0.0' Nepieciešamā versija: '2.0.133'*
+ *Dynamics 365 for Sales risinājumam 'CurrencyExchangeRates' ir versijas neatbilstība. Versija: '1.0.0.0' Nepieciešamā versija: '2.0.133'*
+ *Dynamics 365 for Sales risinājumam 'Dynamics365SupplyChainExtended' ir versijas neatbilstība. Versija: '1.0.0.0' Nepieciešamā versija: '2.0.227'*

Lai novērstu problēmas, atjauniniet duālās rakstīšanas Dataverse risinājumus. Noteikti jauniniet uz jaunāko risinājumu, kas atbilst nepieciešamajam risinājuma versijai.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
