---
title: Multivides galerijas modulis
description: Šajā rakstā ir apskatīti plašsaziņas līdzekļu galerijas moduļi un aprakstīts, kā pievienot tos vietnes lapām Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 5e2d0a4422341badee906c71bebdd491e18a38cc
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273463"
---
# <a name="media-gallery-module"></a>Multivides galerijas modulis

[!include [banner](includes/banner.md)]

Šajā rakstā ir apskatīti plašsaziņas līdzekļu galerijas moduļi un aprakstīts, kā pievienot tos vietnes lapām Microsoft Dynamics 365 Commerce.

Multivides galerijas moduļi rāda vienu vai vairākus attēlus galerijas skatā. Multivides galerijas moduļi atbalsta sīktēlu attēlus, kas var sakārtot vai nu horizontāli (kā rindu zem attēla), vai vertikāli (kā kolonnu blakus attēlam). Multivides galerijas moduļi nodrošina arī iespējas, kas ļauj tālummainīt attēlus (palielināt) vai skatīt pilnekrāna režīmā. Lai attēls multivides galerijas modulī tiktu atveidots, tam ir jābūt pieejamam Commerce vietnes veidotāja multivides bibliotēkā. Pašlaik multivides galerijas moduļi atbalsta tikai attēlus.

Noklusētajā režīmā multivides galerijas modulis izmanto preces ID, kas ir pieejams preces informācijas lapas kontekstā (PDP), lai atveidotu atbilstošos preču attēlus. Programmā Commerce Headquarters visām precēm ir jādefinē multivides faila ceļš. Pēc tam attēli ir jāaugšupielādē vietnes veidotāja multivides bibliotēkā atbilstoši faila ceļam, kas tika noteikts precēm Commerce Headquarters. Šajos attēlos ir ietverti preču attēli un visi preču varianti. Papildinformāciju par to, kā augšupielādēt attēlus vietnes veidotāja multivides bibliotēkā, skatiet [Augšupielādēt attēlus](dam-upload-images.md).

Alternatīvi multivides galerijas modulis var viesot pilnībā pārraudzītu attēlu kopu, kas atrodas attēlu galerijas lapā, kur preces ID vai lapas kontekstam nav atkarību. Šādā gadījumā attēli ir jāaugšupielādē vietnes veidotāja multivides bibliotēka un norādīti vietnes veidotājā.

Piedāvājam dažus lietojuma piemērus plašsaziņas līdzekļu galerijas moduļiem:

- Preču attēlu atveidošana uz PDP
- Preču attēlu atveidošana preču mārketinga lapā
- Demonstrējiet pārraudzītu attēlu kopu mārketinga lapā, piemēram, galerijas lapu

Piemērā nākamajā attēlā ir norādīta, ka pirkšanas lodziņš uz PDP vieso preču attēlus, izmantojot multivides galerijas moduli.

![Pirkšanas lodziņa piemērs preču informācijas lapā, kas vieso preču attēlus, izmantojot multivides galerijas moduli.](./media/ecommerce-pdp-buybox.PNG)

## <a name="media-gallery-properties"></a>Multivides galerijas rekvizīti

| Rekvizīta nosaukums | Vērtības | Apraksts |
|---------------|--------|-------------|
| Attēla avots | **Lapas konteksts** vai **Preces ID** | Noklusējuma vērtība ir **Lapas konteksts**. Ja ir atlasīts **Lapas konteksts**, modulis sagaida, ka lapa nodrošinās preces ID informāciju. Ja ir izvēlēts **Preces ID**, preces ID attēlam jābūt norādītam kā **Preces ID** rekvizīta vērtībai. Šī iespēja ir pieejama Commerce versijā 10.0.12. |
| Preces ID | Preces ID | Šis rekvizīts ir piemērojams tikai tad, ja **Attēla avota** rekvizīta vērtība ir **Preces ID**. |
| Attēla tālummaiņa | **Iekļautais** vai **Konteiners** | Šis rekvizīts ļauj lietotājam tālummainīt attēlus, kas atrodas multivides galerijas modulī. Attēlu var tuvināt vai nu kā iekļautu, vai arī atsevišķā konteinerā blakus attēlam. Šī iespēja ir pieejama versijā 10.0.12. |
| Tālummaiņas koeficients | Decimālskaitlis | Šis rekvizīts norāda mēroga koeficientu attēlu tālummaiņai. Piemēram, ja vērtība ir iestatīta uz **2,5**, attēli tiek palielināti 2,5 reizes. |
| Pilnekrāna režīms | **Patiess** vai **Nepatiess** | Šis rekvizīts norāda, vai attēlus var skatīt pilnekrāna režīmā. Pilnekrāna režīmā attēlus var arī vairāk palielināt, ja tālummaiņas iespēja ir ieslēgta. Šī iespēja ir pieejama Commerce versijas 10.0.13 laidienā. |
| Tuvināta attēla kvalitāte | Skaitlis no 1 līdz 100, kas apzīmē procentus un kas atlasīts, izmantojot kursorstieņa kontroli | Šis rekvizīts nosaka attēla kvalitāti tuvinātajiem attēliem. Lai nodrošinātu, ka tuvināts attēls vienmēr izmanto augstāko iespējamo izšķirtspēju, to var iestatīt uz 100 procentiem. Šis rekvizīts nav piemērojams PNG failiem, jo tie izmanto bezzudumu formātu. Šī iespēja ir pieejama, kā Commerce versijas 10.0.19 laidienā. |
| Attēli | Attēli, kas ir atlasīti no vietnes veidotāja multivides bibliotēkas | Papildus atveidošanai no preces, attēli var tikt pārraudzīti multivides galerijas modulī. Šie attēli tiks pievienoti visiem pieejamiem preces attēliem. Šī iespēja ir pieejama Commerce versijā 10.0.12. |
| Sīktēla orientācija | **Vertikāli** vai **horizontāli** | Šis rekvizīts norāda, vai sīktēli ir jārāda vertikālā vai horizontālā joslā. |
| Paslēpt varianta šablona preces attēlus | **Patiess** vai **Nepatiess** | Ja šis rekvizīts ir iestatīts kā **Patiess**, ja ir atlasīts variants, tiek paslēpti šablona preces attēli, ja vien variantam nav attēlu. Šis rekvizīts neietekmē preces, kam nav variantu. |
| Atjaunināt datu nesēju dimensiju atlasē | **Patiess** vai **Nepatiess** | Ja šis rekvizīts ir iestatīts kā **Patiess**, jebkuras dimensijas (piemēram, krāsas, stila vai izmēra) attēlos plašsaziņas bibliotēku tiks atjaunināti un, ja ir pieejams attēls. Šis rekvizīts palīdz vienkāršot pārlūkošanas pieredzi, jo ne visas preces varianta dimensijas ir jāatlasa atbilstošajam attēlam, kas jāatjaunina. Šis rekvizīts ir pieejams cilnē **Papildu**. |

> [!IMPORTANT]
> Rekvizīts **Atjaunināt datu nesēju dimensiju atlasei** ir pieejams kā Commerce versijas 10.0.21 laidiena versijā. Nepieciešams, lai būtu instalēta Commerce moduļa bibliotēkas pakotnes versija 9.31.

Sekojošajā attēlā ir parādīts plašsaziņas galerijas moduļa piemērs, kurā ir pieejamas pilnekrāna un tālummaiņas opcijas.

![Plašsaziņas galerijas moduļa piemērs, kurā ir pieejamas pilnekrāna un tālummaiņas opcijas.](./media/ecommerce-media-zoom.png)

Sekojošajā attēlā ir parādīts tādas multivides galerijas moduļa piemērs, kurā ir pārraudzīti attēli (t.i., norādītie attēli nav atkarīgi no produkta ID vai lapas konteksta).

![Multivides galerijas moduļa piemērs, kurā ir pārraudzīti attēli.](./media/ecommerce-media-curated.PNG)

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unit mijiedarbība

Kad attēla avots tiek atvasināts no lapas konteksta, preces ID no PDP tiek izmantots, lai izgūtu attēlus. Multivides galerijas modulis izgūst attēla faila ceļu precēm, izmantojot Commerce Scale Unit pieteikuma programmēšanas interfeisus (API). Pēc tam attēli tiek izvilkti no multivides bibliotēkas, lai tos varētu atveidot modulī.

## <a name="add-a-media-gallery-module-to-a-page"></a>Multivides galerijas moduļa pievienošana lapā

Lai mārketinga lapai pievienotu multivides galerijas moduli, veiciet tālāk minētās darbības.

1. Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu jaunu veidni.
1. Dialoglodziņa Jauna **veidne sadaļā** Veidnes nosaukums, **ievadiet** Mārketinga **veidne un** pēc tam atlasiet **Labi**.
1. Pamatteksta **slotā** atlasiet daudzpunkti (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet noklusējuma lapas **moduli** un pēc tam atlasiet **Labi**.
1. Noklusējuma lapas **galvenajā** slotā atlasiet daudzpunkti (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Moduļu **atlase** atlasiet moduli Konteiners **un** pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Dodieties uz **Lapas** un atlasiet **Jauns**, lai izveidotu jaunu lapu.
1. Dialoglodziņā Izveidot **jaunu lapu ar** lapas nosaukumu **ievadiet** **plašsaziņas līdzekļu galerijas lapu** un pēc tam atlasiet **Tālāk**.
1. Zem **Izvēlēties veidni**, atlasiet izveidoto **mārketinga** veidni un pēc tam atlasiet **Tālāk**.
1. Sadaļā **Izvēlēties izkārtojumu atlasiet** lapas izkārtojumu (piemēram, Elastīgs **izkārtojums**) un pēc tam atlasiet **Tālāk**.
1. Sadaļā **Pārskatīt un pabeigt** pārskatiet lapas konfigurāciju. Ja jums ir jārediģē lapas informācija, atlasiet **Atpakaļ**. Ja lapas informācija ir pareiza, atlasiet Izveidot **lapu**. 
1. Jaunās lapas **galvenajā** slotā atlasiet daudzpunkti (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Moduļu **atlase** atlasiet moduli Konteiners **un** pēc tam atlasiet **Labi**.
1. Konteinera slotā **atlasiet** daudzpunkti (**...) un** pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet mediju galerijas **moduli** un pēc tam atlasiet **Labi**.
1. Multivides galerijas moduļa rekvizītu rūtī sadaļā **Attēla avots** atlasiet **Preces ID**. Tad laukā **Preces ID** ievadiet preces ID.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu. Jums vajadzētu redzēt preces attēlus galerijas skatā.
1. Lai izmantotu tikai pārraudzītus attēlus, rekvizītu rūtī zem **Attēla avota** atlasiet **Preces ID**. Pēc tam sadaļā **Attēli** atlasiet **Pievienot attēlu** tik reižu, cik nepieciešams, lai pievienotu attēlus no multivides bibliotēkas.
1. Iestatiet jebkādus papildu rekvizītus, kurus vēlaties iestatīt, piemēram, **Attēla tālummaiņa**, **Tālummaiņas koeficients** un **Sīktēlu orientācija**.
1. Kad esat pabeidzis, atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Pirkšanas lodziņa modulis](add-buy-box.md)

[Konteinera modulis](add-container-module.md)

[Attēlu augšupielāde](dam-upload-images.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
