---
title: Problēmu novēršana saistībā ar duālā ieraksta moduli Finance and Operations lietojumprogrammās
description: Šajā tēmā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas ar duālā ieraksta moduli Finance and Operations lietojumprogrammās.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2241e7e6219f95115f55bc45a4d94550276e1e21
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683627"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a>Problēmu novēršana saistībā ar duālā ieraksta moduli Finance and Operations lietojumprogrammās

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā rakstā ir sniegta informācija par problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Dataverse. Konkrēti, šajā tēmā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas ar moduli **Duālais ieraksts** Finance and Operations lietojumprogrammās.

> [!IMPORTANT]
> Dažas no problēmām, kas risinātas šajā tēmā, var būt nepieciešama vai nu sistēmas administratora loma, vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati. Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Nevar ielādēt duālā ieraksta moduli Finance and Operations lietojumprogrammā

Ja nevarat atvērt lapu **Duālais ieraksts**, atlasot elementu **Duālais ieraksts** darbvietā **Datu pārvaldība**, visticamāk nedarbojas datu integrācijas pakalpojums. Izveidojiet atbalsta biļeti, lai pieprasītu datu integrācijas pakalpojuma restartēšanu.

## <a name="error-when-you-try-to-create-a-new-table-map"></a>Kļūda, mēģinot izveidot jaunu tabulas karti

**Nepieciešamie akreditācijas dati, lai labotu problēmu:** tas pats lietotājs, kas iestata duālo rakstīšanu.

Mēģinot konfigurēt jaunu elementu duālajam ierakstam, jūs varētu saņemt šādu kļūdas ziņojumu. Vienīgais lietotājs, kas var izveidot karti, ir lietotājs, kas uzstāda duālās rakstīšanas savienojumu.

*Atbildes statusa kods nenorāda uz veiksmi: 401 (nesankcionēts)*


## <a name="error-when-you-open-the-dual-write-user-interface"></a>Kļūda, atverot duālā ieraksta lietotāja interfeisu

Mēģinot piekļūt duālajam ierakstam no **Datu pārvaldības** darbvietas, var tikt parādīts šāds kļūdas ziņojums:

*login.microsoftonline.com atteicās izveidot savienojumu.*

Lai labotu problēmu, piesakieties, izmantojot InPrivate logu pakalpojumā Microsoft Edge, inkognito logu pakalpojumā Chromium vai inkognito logu pārlūkprogrammā Google Chrome. Ir arī jāatbloķē vai jādzēš trešās puses sīkfaili.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a>Kļūda, saistot vidi divējādai rakstīšanai vai pievienot jaunu tabulas kartēšanu

**Nepieciešamās lomas, lai labotu problēmu:** sistēmas administrators abās Finance and Operations lietojumprogrammās un Dataverse.

Sasaistot vai veidojot kartes, var rasties šādas kļūdas:

*Atbildes statusa kods nenorāda uz izdošanos: 403 (tokenexchange).<br> Sesijas ID: \<your session id\><br> saknes aktivitātes ID: \<your root activity id\>*

Šī kļūda var rasties, ja jums nav nepieciešamo atļauju, lai saistītu duālo ierakstu vai izveidotu kartes. Šī kļūda var parādīties arī tad, ja Dataverse vide ir atiestatīta, nesaistot duālo rakstīšanu. Ikviens lietotājs ar sistēmas administratora lomu abās Finance and Operations lietojumprogrammās un Dataverse var saistīt vides. Tikai lietotājs, kas iestatījis duālās rakstīšanas savienojumu, var pievienot jaunas tabulas kartes. Pēc iestatīšanas jebkurš lietotājs ar sistēmas administratora lomu var pārraudzīt statusu un rediģēt kartēšanas.

## <a name="error-when-you-stop-the-table-mapping"></a>Kļūda, apturot tabulas kartēšanu

Mēģinot apturēt tabulas kartēšanu, jūs varētu saņemt šādu kļūdas ziņojumu:

*\[Aizliegts\], \[{"statuss": 403, "avots": ","ziņojums":"Kļūda no marķiera maiņas: lietotājam nav atļauts piekļūt savienojumam dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], Attālais serveris atgrieza kļūdu: (403) Aizliegts.*

Šī kļūda rodas, ja nav pieejama saistītā Dataverse vide.

Lai atrisinātu problēmu, izveidojiet biļeti datu integrācijas grupai. Pievienojiet tīkla izsekošanu, lai datu integrācijas grupa varētu atzīmēt kartes kā **Nedarbojošās** aizmugursistēmā.

## <a name="error-while-trying-to-start-an-table-mapping"></a>Kļūda, mēģinot sākt tabulas kartēšanu

Mēģinot iestatīt šo kartēšanas stāvokli uz **Darbojas**, var tikt parādīta šāda kļūda:

*Nevar pabeigt sākotnējo datu sinhronizāciju. Kļūda: duālās rakstīšanas kļūme - spraudņa reģistrācija neizdevās: nevar izveidot duālās rakstīšanas uzmeklēšanas metadatus. Kļūdas objekta atsauce nav iestatīta uz objekta instanci.*

Šīs kļūdas labojums ir atkarīgs no kļūdas cēloņa:

+ Ja kartēšanai ir atkarīgi kartējumi, pārliecinieties, ka iespējojat šīs tabulas kartēšanas atkarīgos kartējumus.
+ Kartēšanai var trūkt avota vai mērķa lauku. Ja trūkst lauks programmā Finance and Operations, izpildiet sekojošos soļus sadaļā [Trūkst entītiju lauku kartēs](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps). Ja trūkst lauks programmā Dataverse, noklikšķiniet uz pogas **Atsvaidzināt tabulas** kartēšanā, lai lauki tiktu automātiski aizpildīti atpakaļ kartēšanā.
