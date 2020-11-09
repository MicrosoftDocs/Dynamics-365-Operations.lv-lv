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
ms.openlocfilehash: f99f3760e75ec1bbf2ccdea497cf2eec3e28e233
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997378"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a>Problēmu novēršana saistībā ar duālā ieraksta moduli Finance and Operations lietojumprogrammās

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir sniegta informācija par problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Common Data Service. Konkrēti, šajā tēmā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas ar moduli **Duālais ieraksts** Finance and Operations lietojumprogrammās.

> [!IMPORTANT]
> Dažas no problēmām, kas risinātas šajā tēmā, var būt nepieciešama vai nu sistēmas administratora loma, vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati. Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Nevar ielādēt duālā ieraksta moduli Finance and Operations lietojumprogrammā

Ja nevarat atvērt lapu **Duālais ieraksts** , atlasot elementu **Duālais ieraksts** darbvietā **Datu pārvaldība** , visticamāk nedarbojas datu integrācijas pakalpojums. Izveidojiet atbalsta biļeti, lai pieprasītu datu integrācijas pakalpojuma restartēšanu.

## <a name="error-when-you-try-to-create-a-new-entity-map"></a>Kļūda, mēģinot izveidot jaunu elementa karti

**Nepieciešamie akreditācijas dati, lai labotu problēmu:** tas pats lietotājs, kas iestata duālo rakstīšanu.

Mēģinot konfigurēt jaunu elementu duālajam ierakstam, jūs varētu saņemt šādu kļūdas ziņojumu. Vienīgais lietotājs, kas var izveidot karti, ir lietotājs, kas uzstāda duālās rakstīšanas savienojumu.

*Atbildes statusa kods nenorāda uz veiksmi: 401 (nesankcionēts)*


## <a name="error-when-you-open-the-dual-write-user-interface"></a>Kļūda, atverot duālā ieraksta lietotāja interfeisu

Mēģinot piekļūt duālajam ierakstam no **Datu pārvaldības** darbvietas, var tikt parādīts šāds kļūdas ziņojums:

*login.microsoftonline.com atteicās izveidot savienojumu.*

Lai labotu problēmu, piesakieties, izmantojot InPrivate logu pakalpojumā Microsoft Edge, inkognito logu pakalpojumā Chromium vai inkognito logu pārlūkprogrammā Google Chrome. Ir arī jāatbloķē vai jādzēš trešās puses sīkfaili.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a>Kļūda, saistot vidi divējādai rakstīšanai vai pievienot jaunu elementu kartēšanu

**Nepieciešamās lomas, lai labotu problēmu:** sistēmas administrators abās Finance and Operations lietojumprogrammās un Common Data Service.

Sasaistot vai veidojot kartes, var rasties šādas kļūdas:

*Atbildes statusa kods nenorāda uz izdošanos: 403 (tokenexchange).<br> Sesijas ID: \<your session id\><br> saknes aktivitātes ID: \<your root activity id\>*

Šī kļūda var rasties, ja jums nav nepieciešamo atļauju, lai saistītu duālo ierakstu vai izveidotu kartes. Šī kļūda var parādīties arī tad, ja Common Data Service vide ir atiestatīta, nesaistot duālo rakstīšanu. Ikviens lietotājs ar sistēmas administratora lomu abās Finance and Operations lietojumprogrammās un Common Data Service var saistīt vides. Tikai lietotājs, kas iestatījis duālās rakstīšanas savienojumu, var pievienot jaunas elementa kartes. Pēc iestatīšanas jebkurš lietotājs ar sistēmas administratora lomu var pārraudzīt statusu un rediģēt kartēšanas.

## <a name="error-when-you-stop-the-entity-mapping"></a>Kļūda, apturot elementa kartēšanu

Mēģinot konfigurēt jaunu elementu duālajam ierakstam, jūs varētu saņemt šādu kļūdas ziņojumu:

*\[Aizliegts\], \[{"statuss": 403, "avots": ","ziņojums":"Kļūda no marķiera maiņas: lietotājam nav atļauts piekļūt savienojumam dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], Attālais serveris atgrieza kļūdu: (403) Aizliegts.*

Šī kļūda rodas, ja nav pieejama saistītā Common Data Service vide.

Lai atrisinātu problēmu, izveidojiet biļeti datu integrācijas grupai. Pievienojiet tīkla izsekošanu, lai datu integrācijas grupa varētu atzīmēt kartes kā **Nedarbojošās** aizmugursistēmā.

## <a name="error-while-trying-to-start-an-entity-mapping"></a>Kļūda, mēģinot sākt elementa kartēšanu

Mēģinot iestatīt šo kartēšanas stāvokli uz **Darbojas** , var tikt parādīta šāda kļūda:

*Nevar pabeigt sākotnējo datu sinhronizāciju. Kļūda: duālās rakstīšanas kļūme - spraudņa reģistrācija neizdevās: nevar izveidot duālās rakstīšanas uzmeklēšanas metadatus. Kļūdas objekta atsauce nav iestatīta uz objekta instanci.*

Šīs kļūdas labojums ir atkarīgs no kļūdas cēloņa:

+ Ja kartēšanai ir atkarīgi kartējumi, pārliecinieties, ka iespējojat šīs elementa kartēšanas atkarīgos kartējumus.
+ Kartēšanai var trūkt avota vai mērķa lauku. Ja trūkst lauks programmā Finance and Operations, izpildiet sekojošos soļus sadaļā [Trūkst entītiju lauku kartēs](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps). Ja trūkst lauks programmā Common Data Service, noklikšķiniet uz pogas **Atsvaidzināt entītijas** kartēšanā, lai lauki tiktu automātiski aizpildīti atpakaļ kartēšanā.
