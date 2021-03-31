---
title: Darbs ar CSS pārlabošanas failiem
description: Šajā tēmā aprakstīts, kāpēc, kad un kā lietot Stila lapu kaskadēšanas (CSS) labošanas failus risinājumā Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 41fb0be51f7af25faba1b860319aea84ae7a8b56
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207803"
---
# <a name="work-with-css-override-files"></a>Darbs ar CSS ignorēšanas failiem


[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīts, kāpēc, kad un kā lietot Stila lapu kaskadēšanas (CSS) labošanas failus risinājumā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Pastāvīgā vietā stili parasti būtu jāapstrādā, izmantojot vietnes tēmu. Tēmas nodrošina galvenos CSS un stila iestatījumus moduļiem jebkurā lapā jūsu vietnē. Tēmas tiek izveidotas, izmantojot Dynamics 365 Commerce tiešsaistes programmatūras izstrādes komplektu (SDK), un tās tiek izvietotas jūsu tīmekļa vietnēs, izmantojot Microsoft Dynamics Lifecycle Services (LCS). Tēmas atkļūdošanas iespējas un moduļa saskarnes konfigurācijas SDK palīdz vietnes izstrādātājiem izveidot pielāgojamas un vienotas vietņu noformējuma pakotnes. Kad šīs dizaina pakotnes ir izvietotas vietnē, vietnes autori var koncentrēties uz satura izveidi, rediģēšanu un publicēšanu, nevis vietnes izstrādi.

Ņemot vērā parasto tēmas dzīves ciklu, atkarība no izstrādātājiem, lai veiktu stila izmaiņas, izmantojot SDK un LCS izvietošanas konveijeru, dažos gadījumos var būt pārmērīgi augsta. Vietnes prototipi vai labojumfaili var šķist apgrūtinoši, ja SDK nav konfigurēts vai jums nav laika gaidīt uz LCS izvietošanu.

Minētajās situācijās var palīdzēt CSS pārlabošanas faili. Commerce autorēšanas rīkos autentificēti lietotāji var augšupielādēt CSS failu, priekšskatīt to un pēc tam aktivizēt, lai pārlabotu vietnes tēmu. SDK vai LCS papildu izvietošana nav nepieciešama. CSS pārlabošanas failā norādītie labojumi var būt tik mazi kā viena teksta stila maiņa vai tik plaši kā pilnīgas zīmola izmaiņas.

Pirms izmantojat CSS pārlabošanas failus, ņemiet vērā šādus ierobežojumus:

- Vietnē vienlaikus var būt aktīvs tikai viens CSS pārlabošanas fails. Tādēļ visiem aktīvajiem labojumiem ir jābūt vienā pārlabošanas failā.
- Lai gan jūs varat priekšskatīt labojumus Commerce autorēšanas rīkos, nav īpašu atkļūdošanas iespēju, lai palīdzētu identificēt visas kļūmes, kuras labojumi varētu ieviest. Citiem vārdiem sakot, izmantojot CSS pārlabošanas failus, jūsu rīcībā nav tāda pati rīkkopa, ko SDK nodrošina moduļa un autorēšanas validācijai.

Tomēr CSS pārlabošanas faili nodrošina ātru veidu, kādā izveidot dizaina prototipu vai ieviest labojumfailu, pirms pilns tēma atjauninājums ir izstrādāts un izvietots.

## <a name="create-a-css-override-file"></a>CSS pārlabošanas faila izveide

Lai izveidotu CSS pārlabošanas failu, varat izmantot jebkuru integrēto izstrādes vidi (IDE), teksta redaktoru vai avota koda redaktoru. Tipiska pieeja ir izmantot standarta tīmekļa atkļūdotājus jūsu pārlūkprogrammā, lai identificētu stilu atlasītājus, rekvizītus un vērtības jūsu esošajā vietnē. Vairākums pārlūkprogrammu ļauj mainīt vērtības un priekšskatīt tās atkļūdotājā. Kad esat identificējis izmaiņas, kuras vēlaties veikt, varat tās saglabāt savā CSS failā.

## <a name="upload-a-css-override-file"></a>CSS pārlabošanas faila augšupielāde

Lai Commerce vietnē augšupielādētu CSS failu, veiciet tālāk norādītās darbības.

1. Autorēšanas rīkos dodieties uz savu vietni.
1. Navigācijas rūtī kreisajā pusē atlasiet **Dizains**.

    > [!NOTE]
    > Atkarībā no Commerce autorēšanas rīku versijas, ko lietojat, iespējams, navigācijas rūtī ir jāpaplašina **Iestatījumi**, lai varētu atlasīt **Dizainu**.

1. Galvenās noformējuma rūts augšdaļā atlasiet cilni **CSS pārlabošana**, ja tā vēl nav atlasīta.
1. Sadaļā **Pieejamie CSS labojumi** atlasiet **Augšupielādēt CSS failu**. Parādās failu pārlūka logs.
1. Failu pārlūkā atrodiet un atlasiet CSS failu un pēc tam atlasiet **Atvērt**. Augšupielādētais CSS fails tagad tiek parādīts sadaļā **Pieejamie CSS labojumi**.

## <a name="preview-a-css-override-file"></a>CSS pārlabošanas faila priekšskatīšana

Lai priekšskatītu CSS pārlabošanas failu, pirms veicat tā aktīvu darbību savā tiešsaistes vietnē, veiciet tālāk norādītās darbības.

1. Kreisajā navigācijas rūtī atlasiet **Dizains** un pēc tam cilnē **CSS labojums** sadaļā **Pieejamie CSS labojumi** atrodiet CSS failu, kuru vēlaties priekšskatīt.
1. Blakus CSS faila nosaukumam atlasiet **Priekšskatījuma vietne**.
1. Dialoglodziņā **Atlasīt vietrādi URL** atlasiet tās vietnes vietrādi URL, kurai vēlaties skatīt ignorēšanas opciju, un pēc tam atlasiet **Labi**.
1. Ja atlasītajam vietrādim URL ir vairāki varianti, parādītajā dialoglodziņā **Priekšskatījuma variācijas** atlasiet vēlamo variantu.

Tiek atvērta jauna pārlūkprogrammas cilne vai logs, kurā varat validēt stila labojumus jūsu vietnē. Pēc tam varat kopīgot vietrādi URL ar citiem autentificētiem Commerce lietotājiem apskatiem un atsauksmēm.

## <a name="activate-a-css-override-file-on-your-live-site"></a>CSS pārlabošanas faila aktivizēšana jūsu tiešsaistes vietnē

Kad esat priekšskatījis un apstiprinājis CSS pārlabošanas failu, varat to aktivizēt tiešsaistes vietnē.

> [!NOTE]
> Vietnē vienlaikus var būt aktīvs tikai viens CSS pārlabošanas fails. Ja aktivizējat jaunu pārlabošanas failu, iepriekšējais pārlabošanas fails tiek deaktivizēts. Tādēļ pārliecinieties, ka visi nepieciešamie labojumi atrodas vienā CSS pārlabošanas failā.

Lai aktivizētu CSS pārlabošanas failu, izpildiet tālāk aprakstītās darbības.

1. Kreisajā navigācijas rūtī atlasiet **Dizains** un pēc tam cilnē **CSS labojums** sadaļā **Pieejamie CSS labojumi** atrodiet CSS failu, kuru vēlaties aktivizēt.
1. Sadaļā CSS faila nosaukums atlasiet **Aktivizēt**. Pārlabotais fails nekavējoties kļūst aktīvs jūsu tiešsaistes vietnē.

## <a name="deactivate-a-css-override-file-on-your-live-site"></a>CSS pārlabošanas faila deaktivizēšana jūsu tiešsaistes vietnē

Lai deaktivizētu CSS pārlabošanas failu savā vietnē, veiciet tālāk norādītās darbības.

1. Kreisajā navigācijas rūtī atlasiet **Dizains** un pēc tam cilnē **CSS labojums** sadaļā **Pieejamie CSS labojumi** atrodiet CSS failu, kuru vēlaties deaktivizēt.
1. Sadaļā CSS faila nosaukums atlasiet **Deaktivizēt**. Pārlabotais fails nekavējoties kļūst neaktīvs jūsu tiešsaistes vietnē.

> [!TIP]
> Lai piekļūtu papildu opcijām CSS pārlabošanas failiem, atlasiet daudzpunkti (**...**) blakus CSS faila nosaukumam. Opcijas **Lejupielādēt**, **Pārdēvēt** un **Aizstāt** ir noderīgas, lai ātri varētu veikt esošā CSS pārlabošanas faila izmaiņas.

## <a name="additional-resources"></a>Papildu resursi

[Logotipa pievienošana](add-logo.md)

[Vietnes dizaina atlase](select-site-theme.md)

[Darbs ar stilu priekšiestatījumiem](style-presets.md)

[Izlases ikonas pievienošana](add-favicon.md)

[Sveiciena ziņojuma pievienošana](add-welcome-message.md)

[Autortiesību paziņojuma pievienošana](add-copyright-notice.md)

[Valodu pievienošana vietnei](add-languages-to-site.md)

[Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju](add-telemetry.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]