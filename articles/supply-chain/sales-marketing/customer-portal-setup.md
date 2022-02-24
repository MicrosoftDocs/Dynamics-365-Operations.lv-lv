---
title: Debitoru portāla instalēšana, iestatīšana un atjaunināšana
description: Šajā tēmā ir sniegta informācija par licencēšanu un iestatīšanas instrukcijas Debitoru portālam.
author: dasani-madipalli
manager: tfehr
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e61fc5f7151a0bb61d496d47f4ad4e727a2a1d65
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529534"
---
# <a name="install-set-up-and-update-the-customer-portal"></a>Debitoru portāla instalēšana, iestatīšana un atjaunināšana

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="licensing-requirements"></a>Licencēšanas prasības

Lai ieviestu Debitoru portālu, ir jābūt tālāk minētajām licencēm.

- **Power Apps portāli** — šī licence ir nepieciešama, lai viesotu Debitoru portālu. Portāli tiek licencēti, pamatojoties uz lietojumu. Plašāku informāciju skatiet [Power Apps portālu licencēšanas prasības](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).
- **Duālais ieraksts** — jums ir jābūt nepieciešamajām licencēm, lai iespējotu duālo ierakstu Supply Chain Management entītijām. Plašāku informāciju skatiet [duālā ieraksta sistēmas prasības](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a>Atkarības no duālā ieraksta un Power Apps portāli

Debitoru portāls ir atkarīgs no Power Apps portāliem un duālā ieraksta, kā parādīts attēlā zemāk.

![Debitoru portāla atkarības](media/customer-portal-elements.png "Debitoru portāla atkarības")

Atšķirībā no citiem Supply Chain Management līdzekļiem, Debitoru portāla veidne atrodas Power Apps portālos. Tāpēc Debitoru portālu ierobežo funkcionalitāte un iespējas, ko sniedz Power Apps portāli un entītijas duālajā ierakstā.

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a>Nepieciešamais iestatījums Debitoru portāla iespējošanai

Kad esat pārliecinājies, ka jums ir nepieciešamās licences, varat iestatīt duālo ierakstu, kā aprakstīts [duālā ieraksta sākotnējās sinhronizācijas instrukcijas](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).

Duālajā ierakstā noteikti iespējojiet tālāk minēto elementu kartējumus.

- Pārdošanas pasūtījuma virsraksts
- Pārdošanas pasūtījumu informācija
- Konti
- Kontaktpersonas
- Preces

Kad iestatīšana ir pabeigta, varat nodrošināt Debitoru portāla veidni.

## <a name="provision-the-customer-portal"></a>Debitoru portāla nodrošinājums

Pirms sākat, pārliecinieties, ka esat jau pabeidzis [nepieciešamo iestatīšanu](#required-setup). Pēc tam veiciet tālāk minētās darbības, lai nodrošinātu Debitoru portālu.

1. Dodieties uz [make.powerapps.com](https://make.powerapps.com/).
2. Pārliecinieties, ka izmantojat vidi, kurā iespējojāt duālo ierakstu.
3. Cilnē **Izveidot** ritiniet uz leju līdz sadaļai **Sākt no veidnes** un atlasiet veidni ar nosaukumu **Debitoru portāls**.
4. Izpildiet ekrānā redzamos norādījumus.

Kad nodrošinājums ir pabeigts, varat piekļūt Debitoru portālam lapas **Sākums** sadaļā **Jūsu programmas**.

> [!NOTE]
> Ja duālā ieraksta risinājums nav instalēts vidē, kurā strādājat, tiks parādīts kļūdas ziņojums, un Debitoru portāls netiks nodrošināts.

## <a name="update-the-customer-portal"></a>Debitoru portāla atjaunināšana

Papildu funkcionalitāti Debitoru portālam var pievienot vēlāk. Visas izmaiņas, ko korporācija Microsoft veic pamata risinājuma komponentiem, automātiski parādīsies jūsu vidē. Tomēr tīmekļa vietne, kas tiek nodrošināta jūsu vidē, automātiski neatspoguļos izmaiņas, kas veiktas konfigurācijas datos. Jums būs manuāli jāpiemēro šīs izmaiņas, iegūstot kodu no jaunās veidnes un apvienojot to ar nodrošināto tīmekļa vietni.

## <a name="additional-resources"></a>Papildu resursi

Lai uzzinātu, kā var iestatīt un pielāgot Debitoru portālu, jāsāk ar sekojošās pamattehnoloģiju dokumentācijas pārskatīšanu.

- [Power Apps portālu dokumentācija](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [Duālā ieraksta dokumentācija](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

Lai efektīvi pārvaldītu portālus, ir jāizprot Power Apps portāli un Common Data Service dzīves cikls. Papildinformāciju skatiet tālāk norādītajos resursos.

- [Par portāla dzīves ciklu](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [Portāla jaunināšana](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [Portāla konfigurācijas migrācija](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [Risinājuma dzīves cikla pārvaldība: programma Dynamics 365 for Customer Engagement](https://www.microsoft.com/download/details.aspx?id=57777)
