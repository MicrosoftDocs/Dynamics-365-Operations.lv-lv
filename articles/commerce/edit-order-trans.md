---
title: Tiešsaistes pasūtījumu un asinhrono debitoru pasūtījumu darījumu rediģēšana un auditēšana
description: Šajā rakstā aprakstīts, kā rediģēt un auditēt tiešsaistes pasūtījumu un asinhrono debitoru pasūtījumu darījumus programmā Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3c4219e082466bdfd1426710cecf25fd350d0767
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873063"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a>Tiešsaistes pasūtījumu un asinhrono debitoru pasūtījumu darījumu rediģēšana un auditēšana

[!include [banner](../includes/banner.md)]

Šajā rakstā aprakstīts, kā rediģēt un auditēt tiešsaistes pasūtījumu un asinhrono debitoru pasūtījumu darījumus programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Starp programmas Commerce versijām 10.0.5 un 10.0.6 tika pievienots atbalsts darījumu, kas ir saistīti ar pārdošanu skaidrā naudā bez piegādes (piemēram, pārdošana un atgriešana), un skaidras naudas pārvaldības darījumu (piemēram, mainīgā ievade un norēķinu noņemšana) rediģēšanai. Programmas Commerce versijā 10.0.7 tika pievienots atbalsts tiešsaistes pasūtījumu darījumu un asinhrono debitoru pasūtījumu darījumu rediģēšanai.

## <a name="edit-and-audit-order-transactions"></a>Pasūtījumu darījumu rediģēšana un auditēšana

Lai rediģētu un auditētu pasūtījumu darījumus komponentā Commerce Headquarters, veiciet tālāk norādītās darbības.

1. Instalējiet [Microsoft Dynamics Office pievienojumprogrammu](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).
1. Lapas **Mazumtirdzniecības parametri** cilnes **Debitoru pasūtījumi** kopsavilkuma cilnē **Pasūtījums** norādiet aizturēšanas kodu elementam **Aizturēšanas kods pasūtījumu sinhronizācijas kļūdām**.
1. Atveriet darbvietu **Veikala finanses**. Elementi **Tiešsaistes pasūtījumu sinhronizācijas kļūdas** un **Debitoru pasūtījumu sinhronizācijas kļūdas** nodrošina iepriekš filtrētu mazumtirdzniecības darījumu lapas skatu. Katrā no tiem ir parādīti darījumu ieraksti, kuru sinhronizācija neizdevās atbilstoši pasūtījuma veidam.
1. Atveriet lapu **Tiešsaistes pasūtījumu sinhronizācijas kļūdas** vai lapu **Debitoru pasūtījumu sinhronizācijas kļūdas**. Atlasiet ierakstu, lai skatītu detalizētu informāciju par sinhronizācijas kļūdu. Kopsavilkuma cilnē **Sinhronizācijas statuss** ir sniegta tālāk norādītā detalizētā informācija par kļūdu.

    - Gaidošā pasūtījuma statuss
    - Detalizēta informācija par pasūtījuma kļūdām
    - Modificēšanas datums un laiks
    - Atkārtoto mēģinājumu skaits

1. Ja detalizētajā informācijā par kļūdu ir norādīts, ka ierakstu nepieciešams labot, atlasiet **Office pievienojumprogramma** un pēc tam atlasiet **Rediģēt atlasīto darījumu**. Tiks atvērts Excel fails, kurā parādīta detalizēta informācija par atlasīto darījumu.

    - Ja darījums, kas tiek rediģēts, ir tiešsaistes pasūtījuma darījums, Excel failā ir tālāk norādītās darblapas.

        - **Darījums** — šī darblapa satur detalizētu informāciju par darījuma galveni.
        - **Pārdošanas darījums** — šī darblapa satur detalizētu rindas informāciju par darījumu.
        - **Maksājumu darījumi** — šī darblapa satur detalizētu informāciju par maksājumu rindām attiecībā uz darījumu.
        - **Atlaižu darījumi** — šī darblapa satur detalizētu informāciju par atlaidēm attiecībā uz darījumu.
        - **Nodokļu darījumi** — šī darblapa satur detalizētu ar nodokļiem saistītu informāciju par atlaidēm attiecībā uz darījumu.
        - **Izmaksu darījumi** — šī darblapa satur ar izmaksām saistītus datus attiecībā uz darījumu.

    - Ja darījums, kas tiek rediģēts, ir asinhrons debitora pasūtījuma darījums, Excel failā ir tālāk norādītās darblapas.

        - **Rindas** — šī darblapa satur detalizētu galvenes un rindas informāciju par darījumu.
        - **Maksājumi** — šī darblapa satur detalizētu informāciju par maksājumu rindām attiecībā uz darījumu.
        - **Atlaides** — šī darblapa satur detalizētu informāciju par atlaidēm attiecībā uz darījumu.
        - **Nodokļi** — šī darblapa satur detalizētu informāciju par nodokļiem attiecībā uz darījumu.
        - **Izmaksas** — šī darblapa satur ar izmaksām saistītus datus attiecībā uz darījumu.

1. Programmas Excel faila laukā **Gaidošā pasūtījuma statuss** ievadiet **Rediģēšana** un pēc tam publicējiet izmaiņas. Tādējādi jūs neļausit veikt darbu **Sinhronizēt pasūtījumu**, kas darbojas pakešveida režīmā, izlaižot šo ierakstu apstrādes laikā.
1. Excel failā varat modificēt attiecīgos laukus un pēc tam augšupielādēt datus atpakaļ komponentā Commerce Headquarters, izmantojot Dynamics Excel pievienojumprogrammas publicēšanas funkcionalitāti. Pēc datu publicēšanas izmaiņas tiks atspoguļotas sistēmā. Publicēšanas laikā lietotāju veiktajām izmaiņām validācija netiek veikta.
1. Pilnīgus auditācijas pierakstus varat skatīt, galvenē **Mazumtirdzniecības darījums** (galvenes līmeņa izmaiņu gadījumā) un attiecīgajā sadaļā un ierakstā atbilstošajā darījumu lapā noklikšķinot uz **Skatīt auditācijas pierakstus**. Piemēram, visas ar pārdošanas rindām saistītās izmaiņas tiks rādītas lapā **Pārdošanas darījumi** un visas ar maksājumiem saistītās izmaiņas tiks rādītas lapā **Maksājumu darījumi**. Saistībā ar izmaiņām tiek uzturēta tālāk norādītā detalizētā informācija par auditu.

    - Modificēšanas datums un laiks
    - Lauks
    - Vecā vērtība
    - Jaunā vērtība
    - Modificēja

1. Pēc izmaiņu veikšanas un publicēšanas atlasiet **Sinhronizēt pasūtījumu**, lai nekavējoties sāktu sinhronizācijas procesu. Varat arī gaidīt sinhronizācijas procesu, kas darbojas pakešveida režīmā, lai apstrādātu darījumu.

Pēc noklusējuma pēc pasūtījumu veiksmīgas sinhronizēšanas tiem tiek piešķirts aizturēšanas statuss, pamatojoties uz aizturēšanas kodu, kas definēts Commerce parametros. Pasūtījumu aizturēšana ir jānoņem, pirms pasūtījumus var apstrādāt tālākai izpildei vai citām operācijām.

## <a name="additional-resources"></a>Papildu resursi

[Darījumu, kas saistīti ar pārdošanu skaidrā naudā bez piegādes, un skaidras naudas pārvaldības darījumu rediģēšana un auditēšana](edit-cash-trans.md)

[Mazumtirdzniecības darījumu finanšu dimensiju rediģēšana](edit-financial-dim.md)

[Excel darbgrāmatas izveide, lai rediģētu mazumtirdzniecības darījumus](create-excel-edit.md)

[Lauku pievienošana Excel darbgrāmatai, lai rediģētu mazumtirdzniecības darījumus](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]