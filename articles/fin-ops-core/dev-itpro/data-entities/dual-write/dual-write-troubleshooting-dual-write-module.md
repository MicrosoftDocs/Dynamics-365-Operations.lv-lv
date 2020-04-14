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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 34c10e38400a72a670a93f2a72d0aa7a4aed561a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172764"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a>Problēmu novēršana saistībā ar duālā ieraksta moduli Finance and Operations lietojumprogrammās

[!include [banner](../../includes/banner.md)]



Šajā rakstā ir sniegta informācija par problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Common Data Service. Konkrēti, šajā tēmā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas ar moduli **Duālais ieraksts** Finance and Operations lietojumprogrammās.

> [!IMPORTANT]
> Dažas no problēmām, kas risinātas šajā tēmā, var būt nepieciešama vai nu sistēmas administratora loma, vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati. Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Nevar ielādēt duālā ieraksta moduli Finance and Operations lietojumprogrammā.

Ja nevarat atvērt lapu **Duālais ieraksts**, atlasot elementu **Duālais ieraksts** darbvietā **Datu pārvaldība**, visticamāk nedarbojas datu integrācijas pakalpojums. Izveidojiet atbalsta biļeti, lai pieprasītu datu integrācijas pakalpojuma restartēšanu.

## <a name="error-when-you-try-to-create-a-new-entity-mapping"></a>Kļūda, mēģinot izveidot jaunu elementa kartēšanu

**Nepieciešamie akreditācijas dati problēmas novēršanai:** Azure AD nomnieka administrators

Mēģinot konfigurēt jaunu elementu duālajam ierakstam, jūs varētu saņemt šādu kļūdas ziņojumu:

*Atbildes statusa kods nenorāda uz veiksmi: 401 (nesankcionēts)*

Šī kļūda rodas, jo tikai Azure AD nomnieka administrators var pievienot jaunu elementa kartēšanu.

Lai labotu problēmu, piesakieties Finance and Operations programmā kā Azure AD administratora nomnieks. Jums ir arī jādodas uz web,PowerApps.com un atkārtoti jāvalidē savienojums.

## <a name="error-when-you-open-the-dual-write-user-interface"></a>Kļūda, atverot duālā ieraksta lietotāja interfeisu

Mēģinot piekļūt duālajam ierakstam no **Datu pārvaldības** darbvietas, var tikt parādīts šāds kļūdas ziņojums:

*login.microsoftonline.com atteicās izveidot savienojumu.*

Lai labotu problēmu, piesakieties, izmantojot InPrivate logu pakalpojumā Microsoft Edge, inkognito logu pakalpojumā Chromium vai inkognito logu pārlūkprogrammā Google Chrome. Ir arī jāatbloķē vai jādzēš trešās puses sīkfaili.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a>Kļūda, saistot vidi divējādai rakstīšanai vai pievienot jaunu elementu kartēšanu

**Nepieciešamie akreditācijas dati problēmas novēršanai:** Azure AD nomnieka administrators

Sasaistot vai veidojot kartes, var rasties šādas kļūdas:

*Atbildes statusa kods nenorāda uz izdošanos: 403 (tokenexchange). <br>Sesijas ID: \<jūsu sesijas id\><br> saknes aktivitātes ID \<jūsu saknes aktivitātes id\>*

Šī kļūda var rasties, ja jums nav nepieciešamo atļauju, lai saistītu duālo ierakstu vai izveidotu kartes. Lai piesaistītu vides un pievienotu jaunus elementa kartējumus, ir jāizmanto Azure AD nomnieka administratora konts. Tomēr pēc iestatīšanas varat izmantot kontu, kas nav administratora konts, lai pārraudzītu statusu un rediģētu kartējumus.

## <a name="error-when-you-stop-the-entity-mapping"></a>Kļūda, apturot elementa kartēšanu

Mēģinot konfigurēt jaunu elementu duālajam ierakstam, jūs varētu saņemt šādu kļūdas ziņojumu:

*\[Aizliegts\], \[{"statuss": 403, "avots": ","ziņojums":"Kļūda no marķiera maiņas: lietotājam nav atļauts piekļūt savienojumam dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], Attālais serveris atgrieza kļūdu: (403) Aizliegts.*

Šī kļūda rodas, ja nav pieejama saistītā Common Data Service vide.

Lai atrisinātu problēmu, izveidojiet biļeti datu integrācijas grupai. Pievienojiet tīkla izsekošanu, lai datu integrācijas grupa varētu atzīmēt kartes kā **Nedarbojošās** aizmugursistēmā.
