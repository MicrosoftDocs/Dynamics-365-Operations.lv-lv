---
title: Multivides galerijas modulis
description: Šajā tēmā tiek stāstīts par multivides galerijas moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 809916118d8eb709c0bde31bb23fa8daa1f7e60c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022524"
---
# <a name="media-gallery-module"></a>Multivides galerijas modulis

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šajā tēmā tiek stāstīts par multivides galerijas moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.

Multivides galerijas moduļi rāda vienu vai vairākus attēlus galerijas skatā. Multivides galerijas moduļi atbalsta sīktēlu attēlus, kas var sakārtot vai nu horizontāli (kā rindu zem attēla), vai vertikāli (kā kolonnu blakus attēlam). Multivides galerijas moduļi nodrošina arī iespējas, kas ļauj tālummainīt attēlus (palielināt) vai skatīt pilnekrāna režīmā. Lai attēls multivides galerijas modulī tiktu atveidots, tam ir jābūt pieejamam Commerce vietnes veidotāja multivides bibliotēkā. Pašlaik multivides galerijas moduļi atbalsta tikai attēlus.

Noklusētajā režīmā multivides galerijas modulis izmanto preces ID, kas ir pieejams preces informācijas lapas kontekstā (PDP), lai atveidotu atbilstošos preču attēlus. Programmā Commerce Headquarters visām precēm ir jādefinē multivides faila ceļš. Pēc tam attēli ir jāaugšupielādē vietnes veidotāja multivides bibliotēkā atbilstoši faila ceļam, kas tika noteikts precēm Commerce Headquarters. Šajos attēlos ir ietverti preču attēli un visi preču varianti. Papildinformāciju par to, kā augšupielādēt attēlus vietnes veidotāja multivides bibliotēkā, skatiet [Augšupielādēt attēlus](dam-upload-images.md).

Alternatīvi multivides galerijas modulis var viesot pilnībā pārraudzītu attēlu kopu, kas atrodas attēlu galerijas lapā, kur preces ID vai lapas kontekstam nav atkarību. Šādā gadījumā attēli ir jāaugšupielādē vietnes veidotāja multivides bibliotēka un norādīti vietnes veidotājā.

Piedāvājam dažus lietojuma piemērus plašsaziņas līdzekļu galerijas moduļiem:

- Preču attēlu atveidošana uz PDP
- Preču attēlu atveidošana preču mārketinga lapā
- Demonstrējiet pārraudzītu attēlu kopu mārketinga lapā, piemēram, galerijas lapu

Piemērā nākamajā attēlā ir norādīta, ka pirkšanas lodziņš uz PDP vieso preču attēlus, izmantojot multivides galerijas moduli.

![Pirkšanas lodziņa piemērs preču informācijas lapā, kas vieso preču attēlus, izmantojot multivides galerijas moduli](./media/ecommerce-pdp-buybox.PNG)

## <a name="media-gallery-properties"></a>Multivides galerijas rekvizīti

| Rekvizīta nosaukums | Vērtības | apraksts |
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

Sekojošajā attēlā ir parādīts plašsaziņas galerijas moduļa piemērs, kurā ir pieejamas pilnekrāna un tālummaiņas opcijas.

![Plašsaziņas galerijas moduļa piemērs, kurā ir pieejamas pilnekrāna un tālummaiņas opcijas](./media/ecommerce-media-zoom.png)

Sekojošajā attēlā ir parādīts tādas multivides galerijas moduļa piemērs, kurā ir pārraudzīti attēli (t.i., norādītie attēli nav atkarīgi no produkta ID vai lapas konteksta).

![Multivides galerijas moduļa piemērs, kurā ir pārraudzīti attēli](./media/ecommerce-media-curated.PNG)

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unit mijiedarbība

Kad attēla avots tiek atvasināts no lapas konteksta, preces ID no PDP tiek izmantots, lai izgūtu attēlus. Multivides galerijas modulis izgūst attēla faila ceļu precēm, izmantojot Commerce Scale Unit pieteikuma programmēšanas interfeisus (API). Pēc tam attēli tiek izvilkti no multivides bibliotēkas, lai tos varētu atveidot modulī.

## <a name="add-a-media-gallery-module-to-a-page"></a>Multivides galerijas moduļa pievienošana lapā

Lai mārketinga lapai pievienotu multivides galerijas moduli, veiciet tālāk minētās darbības.

1. Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu jaunu veidni.
1. Dialoglodziņā **Jauna veidne** zem **Veidnes nosaukums** ievadiet **Mārketinga veidne** un pēc tam atlasiet **Labi**.
1. Slotā **Pamatteksts** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Noklusējuma lapa** un pēc tam atlasiet **Labi**.
1. Noklusējuma lapas slotā **Galvenais** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Konteiners** un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Dodieties uz **Lapas** un atlasiet **Jauns**, lai izveidotu jaunu lapu.
1. Dialoglodziņā **Izvēlēties veidni** atlasiet veidni **Mārketinga veidne**. Sadaļā **Lapas nosaukums** ievadiet **Multivides galerijas lapa** pēc tam atlasiet **Labi**.
1. Jaunās lapas slotā **Galvenais** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Konteiners** un pēc tam atlasiet **Labi**.
1. Slotā **Konteiners** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Mediju galerija** un pēc tam atlasiet **Labi**.
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
