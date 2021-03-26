---
title: Darījumu, kas saistīti ar pārdošanu skaidrā naudā bez piegādes, un skaidras naudas pārvaldības darījumu rediģēšana un auditēšana
description: Šajā tēmā aprakstīts, kā rediģēt un auditēt darījumus, kas saistīti ar pārdošanu skaidrā naudā bez piegādes, un skaidras naudas pārvaldības darījumus programmā Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 296dbf03ed65c1994562149a2c4b8fccd9073f0d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221923"
---
# <a name="edit-and-audit-cash-and-carry-and-cash-management-transactions"></a>Darījumu, kas saistīti ar pārdošanu skaidrā naudā bez piegādes, un skaidras naudas pārvaldības darījumu rediģēšana un auditēšana

[!include [banner](../includes/banner.md)]

Šajā tēmā aprakstīts, kā rediģēt un auditēt darījumus, kas saistīti ar pārdošanu skaidrā naudā bez piegādes, un skaidras naudas pārvaldības darījumus programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Dynamics 365 Commerce klienti izmanto gan pirmās puses pārdošanas punkta (POS) programmu, gan trešās puses POS programmas. Izmantojot pirmās puses programmu, veikala darījumi tiek importēti komponentā Commerce Headquarters no kanāliem ar pakešveida apstrādes palīdzību. Izmantojot trešās puses programmas, darījumi tiek importēti komponentā Commerce Headquarters ar integrācijas palīdzību. Abos gadījumos pēc darījumu importēšanas komponentā Commerce Headquarters ir jāveic konsekvences pārbaudes process. Šis process veic vairākas darījumu pārbaudes, un pārskatā tiek importētas tikai tie darījumi, kas tika veiksmīgi pārbaudīti, lai tos varētu grāmatot komponentā Commerce Headquarters.

Tirdzniecības darījumi var neizturēt pārbaudi dažādu iemeslu dēļ. Integrācijas koda vai POS programmas kļūda var izraisīt nekonsekventus datus. Vai arī lietotāja kļūda var izraisīt nekonsekventus datus. Piemēram, lietotājs dzēš preci pēc tam, kad tā tika sinhronizēta ar kanālu, vai arī lietotājs aizver finanšu periodu, negrāmatojot šī perioda darījumus. Lai gan šie darījumi ir atzīmēti ar karodziņu un izslēgti no pārskatiem, tie var traucēt klienta pārdošanas ikdienas grāmatošanas procesu. Programmā Commerce varat rediģēt darījumus, kuri neiztur pārbaudi, saglabājot visu izmaiņu auditu.

## <a name="edit-transactions"></a>Darījumu rediģēšana

Programmas Commerce versijā 10.0.5 var rediģēt tikai darījumus, kas ir saistīti ar pārdošanu skaidrā naudā bez piegādes, piemēram, pārdošanas un atgriešanas darījumi. Debitoru pasūtījumus un tiešsaistes pasūtījumus nevar rediģēt. Programmas Commerce versijā 10.0.6 un jaunākās versijās var rediģēt arī skaidras naudas pārvaldības darījumus.

Lai rediģētu darījumus komponentā Commerce Headquarters, veiciet tālāk norādītās darbības.

1. Instalējiet [Microsoft Dynamics Office pievienojumprogrammu](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).
1. Komponentā Commerce Headquarters atveriet darbvietu **Veikala finanses**. Elements **Darījumu validācijas kļūmes** nodrošina iepriekš filtrētu tā darījuma lapas skatu, kurš neatbilda vienai vai vairākām validēšanas kārtulām.
1. Atveriet darījuma lapu, atlasiet ierakstu, kuru neizdevās validēt, atlasiet **Office pievienojumprogramma** un pēc tam atlasiet **Rediģēt atlasīto darījumu**. Tiks atvērts Excel fails, kurā parādīta detalizēta informācija par atlasīto darījumu. Šajā failā ir tālāk norādītās darblapas.

    - **Rindas** — šī darblapa satur darījuma virsrakstu, preču rindas un ar darījumu saistītos datus.
    - **Maksājumi** — šī darblapa satur detalizētu informāciju par maksājumu rindām attiecībā uz darījumu.
    - **Atlaides** — šī darblapa satur detalizētu informāciju par atlaidēm attiecībā uz darījumu.
    - **Nodokļi** — šī darblapa satur detalizētu informāciju par nodokļiem attiecībā uz darījumu.
    - **Izmaksas** — šī darblapa satur ar izmaksām saistītus datus attiecībā uz darījumu.

1. Excel failā varat modificēt attiecīgos laukus un pēc tam augšupielādēt datus atpakaļ komponentā Commerce Headquarters, izmantojot Dynamics Excel pievienojumprogrammas publicēšanas funkcionalitāti. Pēc datu publicēšanas izmaiņas tiks atspoguļotas sistēmā. Publicēšanas laikā lietotāju veiktajām izmaiņām validācija netiek veikta.
1. Pilnīgus auditācijas pierakstus varat skatīt, galvenē **Mazumtirdzniecības darījums** (galvenes līmeņa izmaiņu gadījumā) un attiecīgajā sadaļā un ierakstā atbilstošajā darījumu lapā noklikšķinot uz **Skatīt auditācijas pierakstus**. Piemēram, visas ar pārdošanas rindām saistītās izmaiņas tiks rādītas lapā **Pārdošanas darījumi** un visas ar maksājumiem saistītās izmaiņas tiks rādītas lapā **Maksājumu darījumi**. Saistībā ar izmaiņām tiek uzturēta tālāk norādītā detalizētā informācija par auditu.

    - Modificēšanas datums un laiks
    - Lauks
    - Vecā vērtība
    - Jaunā vērtība
    - Modificēja

1. Kad esat veicis un publicējis izmaiņas, palaidiet opciju **Validēt veikala darījumus**, lai pārbaudītu, vai šīs izmaiņas ir saskaņotas un derīgas.

> [!NOTE]
> Varat rediģēt tikai tos darījumus, kuru validācija neizdevās. Ja vēlaties rediģēt darījumu, kura validācija izdevās, mainiet darījuma validācijas statusu uz **Kļūda** vai **Nav** un pēc tam publicējiet izmaiņas. Pēc tam varat rediģēt galvenes datus vai datus jebkuros citos darījuma atvasinātajos ierakstos un publicēt galveni vai ierakstus.

## <a name="bulk-edit-transactions-that-are-linked-to-a-statement"></a>Ar pārskatu saistīto darījumu lielapjoma rediģēšana

Programmas Commerce versijā 10.0.6 un jaunākās versijās tiek atbalstīta opcija darījumu lielapjoma rediģēšanai pārskata līmenī.

Lai veiktu ar pārskatu saistīto darījumu lielapjoma rediģēšanu komponentā Commerce Headquarters, veiciet tālāk norādītās darbības.

1. Atveriet lapu **Pārskati** un atlasiet pārskatu, kurā ir rediģējamie darījumi.
1. Atlasiet pogu **Atvērt programmā Microsoft Office**.
1. Atkarībā no rediģējamā satura atlasiet vienu no tālāk norādītajām opcijām.

    - **Rediģēt darījumus, kas ir saistīti ar pārdošanu skaidrā naudā bez piegādes** — šī opcija ļauj rediģēt visus pārskatā iekļautos darījumus, kas ir saistīti ar pārdošanu skaidrā naudā bez piegādes. Pieejamas tālāk norādītās Excel darblapas.

        - **Darījums** — šī darblapa satur visu pārdošanas darījumu galvenes līmeņa informāciju.
        - **Pārdošanas darījums** — šī darblapa satur visu pārdošanas darījumu rindu līmeņa informāciju.
        - **Maksājumu darījumi** — šī darblapa satur visu pārdošanas darījumu pārdošanas rindu informāciju.
        - **Atlaižu darījumi** — šī darblapa satur visu pārdošanas darījumu atlaižu rindu informāciju.
        - **Nodokļu darījumi** — šī darblapa satur visu pārdošanas darījumu nodokļu rindu informāciju.
        - **Izmaksu darījumi** — šī darblapa satur visu pārdošanas darījumu izmaksu rindu informāciju.

    - **Rediģēt skaidras naudas pārvaldības darījumi** — šī opcija ļauj rediģēt visus pārskatā iekļautos skaidras naudas pārvaldības darījumus. Pieejamas tālāk norādītās Excel darblapas.

        - **Darījums** — šī darblapa satur visu skaidras naudas pārvaldības darījumu galvenes līmeņa informāciju.
        - **Norēķinu darījumi noguldījumiem bankā** — šī darblapa satur visu detalizēto informāciju par darījumiem saistībā ar noguldījumiem bankā.
        - **Norēķinu darījumi noguldījumiem seifā** — šī darblapa satur visu detalizēto informāciju par darījumiem saistībā ar noguldījumiem seifā.
        - **Norēķinu uzskaite** — šī darblapa satur visu detalizēto informāciju par norēķinu uzskaites darījumiem.
        - **Ienākumu–izdevumu darījums** — šī darblapa satur visu detalizēto informāciju par ieņēmumu–izdevumu darījumu rindām.
        - **Maksājumu darījumi** — šī darblapa satur visu ar maksājumiem saistīto informāciju operācijai **Apmaksāt rēķinu** un ieņēmumu–izdevumu darījumu.

1. Rediģējiet nepieciešamos darījumus.

    > [!NOTE]
    > Publicējot lielapjoma rediģētos darījumus, validācija netiek veikta. Jums jāpārliecinās, vai visi labojumi ir precīzi un vai visās darblapās tiek uzturēta datu precizitāte. Piemēram, ja vēlaties mainīt darījuma datumu, lai pārvaldītu scenārijus, kuros finanšu vai krājumu periods atvērtajiem darījumiem ir slēgts, ir jāmaina datums visās Excel darblapās, kurās ir kolonna **Darbadiena**. Lai validētu darījumus pēc to rediģēšanas, varat atlasīt opciju **Validēt darījumus atkārtoti** lapā **Pārskati**. Pirms pārskata grāmatošanas uzgaidiet, līdz validācijas darbs tiek pabeigts.

1. Ja apkopojums jau ir ģenerēts, atveriet lapu **Apkopotie darījumi** un atlasiet **Atkārtoti ģenerēt pārdošanas pasūtījuma xml**.

## <a name="bulk-edit-transactions-that-arent-linked-to-a-statement"></a>Ar pārskatu nesaistīto darījumu lielapjoma rediģēšana

Programmas Commerce versija 10.0.10 un jaunākas versijas atbalsta to darījumu lielapjoma rediģēšanu, kuri neiztur pārbaudi, bet nav saistīti ar pārskatu.

Lai veiktu ar pārskatu nesaistīto darījumu lielapjoma rediģēšanu komponentā Commerce Headquarters, veiciet tālāk norādītās darbības.

1. Atveriet lapu **Visi veikali** un atlasiet veikalu, kuram ir jārediģē darījumi.
1. Atlasiet pogu **Atvērt programmā Microsoft Office** un pēc tam atlasiet **Rediģēt darījumus, kas ir saistīti ar pārdošanu skaidrā naudā bez piegādes**.
1. Rediģējiet vajadzīgos darījumus un pēc tam publicējiet tos.

## <a name="additional-resources"></a>Papildu resursi

[Tiešsaistes pasūtījumu un asinhrono debitoru pasūtījumu darījumu rediģēšana un auditēšana](edit-order-trans.md)

[Mazumtirdzniecības darījumu finanšu dimensiju rediģēšana](edit-financial-dim.md)

[Excel darbgrāmatas izveide, lai rediģētu mazumtirdzniecības darījumus](create-excel-edit.md)

[Lauku pievienošana Excel darbgrāmatai, lai rediģētu mazumtirdzniecības darījumus](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]