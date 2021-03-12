---
title: Lapas modeļa glosārijs
description: Šajā tēmā ir aprakstīti dažādi elementi, kas tiek izmantoti Microsoft Dynamics 365 Commerce vietnes lapās.
author: phinneyridge
manager: annbe
ms.date: 10/09/2020
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f676503691049938fb8b6b7bfcac159e2f61bc6f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972686"
---
# <a name="page-model-glossary"></a>Lapas modeļa glosārijs


[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīti dažādi elementi, kas tiek izmantoti Microsoft Dynamics 365 Commerce vietnes lapās.

## <a name="page-element-definitions"></a>Lapas elementu definīcijas

Tālāk redzamajā tabulā ir sniegts kopsavilkums par terminiem, kas jums jāzina, kad maināt savas vietnes izskatu, sajūtu un saturu. Lai iegūtu pilnīgākus skaidrojumus un procedūras, izmantojiet tālāk minētās saites.

| Termiņš | Apraksts un piezīmes |
|------|-----------------------|
| [Modulis](work-with-modules.md) | <p>**Definīcija:** moduļi ir veidošanas bloks, ko var autorēt un kas veido tīmekļa lapas skeletu. Piemēram, galvenes, hero un karuseļa moduļi.</p><p>**Kur tie tiek atlasīti:** izvietotus moduļus var atlasīt un konfigurēt dažādos vietas autorēšanas darbplūsmas posmos, piemēram, veidnē, izkārtojumā, lapā un fragmenta autorēšanas posmos.</p><p>**Kur tie tiek rediģēti:** pielāgoti moduļi tiek veidoti kodā, izmantojot programmatūras izstrādes komplektu (SDK). Pēc tam tie tiek augšupielādēti jūsu vietnē, kur tie kļūst pieejami atlasei.</p> |
| Moduļa rekvizīts | <p>**Definīcija:** moduļa rekvizīti ir noteikti iestatījumi, ko nosaka modulis. Tos var rediģēt e-tirdzniecības autorēšanas rīkos. Piemēram, moduļa rekvizīti tiek izmantoti, lai iestatītu reklāmkaroga moduļa virsrakstu un fona attēlu.</p><p>**Kur tie tiek konfigurēti:** moduļa rekvizīti tiek atlasīti un konfigurēti rekvizītu rūtī, kas parādās autorēšanas vidēs (redaktori) veidnēm, izkārtojumiem, lapām, fragmentiem un programmu iestatījumiem.</p> |
| [Veidne](templates-layouts-overview.md) | <p>**Definīcija:** veidnes nosaka moduļa kombinācijas un opcijas, kas jāizmanto lapu kategorijai (piemēram, mārketinga lapas, kategoriju lapas un preču lapas).</p><p>**Kur tās tiek atlasītas:** veidnes var atlasīt lapas vai izkārtojuma izveides darbplūsmu laikā.</p><p>**Kur tās tiek rediģētas:** veidnes tiek autorētas veidnes redaktorā. Nav nepieciešams kods, lai tās izveidotu vai modificētu.</p> |
| [Izkārtojums](templates-layouts-overview.md) | <p>**Definīcija:** izkārtojumi definē pamata veidnes opciju kopas moduļu galīgo atlasi un novietojumu. Izkārtojumu var konfigurēt vienai lapai (*pielāgots izkārtojums*), vai arī to var koplietot vairākas lapas (*iepriekš iestatīts izkārtojums*).</p><p>**Kur tie tiek atlasīti:** izkārtojumus var atlasīt jaunas lapas izveides laikā vai, ja esošajai lapai ir nepieciešams cits izkārtojums.</p><p>**Kur tie tiek rediģēti:** izkārtojumi tiek autorēti izkārtojuma redaktorā. Nav nepieciešams kods, lai tās izveidotu vai modificētu.</p> |
| [Lapas instance](modify-existing-page.md) | <p>**Definīcija:** lapas instances nosaka galīgo, lapai specifiski lokalizēto saturu vienai lapai. Šis saturs tiek iegūts no moduļa rekvizītu vērtībām.</p><p>**Kur tās tiek atlasītas:** lapas tiek atlasītas, piešķirot URL.</p><p>**Kur tās tiek rediģētas:** lapas tiek rediģētas lapas redaktorā. Nav nepieciešams kods, lai tās izveidotu vai modificētu.</p> |
| [Tēma](select-site-theme.md) | <p>**Definīcija:** tēmas definē stila lapas kaskadēšanu (CSS) un nosaka to moduļu izskatu un sajūtu, kas tiek atveidoti lapā.</p><p>**Kur tās tiek atlasītas:** pēc tēmas augšupielādes jūsu vietnē, izmantojot Microsoft Dynamics Lifecycle Services (LCS), tās var atlasīt kā lapas konteinera moduļa rekvizītu.</p><p>**Kur tās tiek rediģētas:** tēmas pašlaik tiek izveidotas un rediģētas, izmantojot SDK. Pēc tam tās tiek augšupielādētas jūsu vietnē, izmantojot LCS.</p> |
| [Fragments](work-with-fragments.md) | <p>**Definīcija:** fragmenti ir pilnībā konfigurēti moduļi ar lokalizētu saturu, ko var atkārtoti izmantot un centralizēti atjaunināt vairākās lapās. Piemēram, no virsraksta moduļa izveidoto fragmentu var izmantot visās veidnēs un visās jūsu vietnes lapās, kā arī centralizēti atjaunināt vienā vietā.</p><p>**Kur tie tiek atlasīti:** fragmentus var atlasīt, kad vien var atlasīt moduļus. Tos var aizstāt ar moduli, kas palīdz uzlabot efektivitāti, izmantojot atkārtotu un centralizētu autorēšanu.</p><p>**Kur tie tiek rediģēti:** fragmenti tiek rediģēti fragmentu redaktorā. Nav nepieciešams kods, lai tās izveidotu vai modificētu.</p> |
| [Vietrādis URL](create-page-URL.md) | <p>**Definīcija:** vienotie resursu vietrāži (URL) ir adreses, kas norāda uz tīmekļa lapām vai citiem URL.</p><p>**Kur tie tiek atlasīti:** URL tiek atlasīti, kad ir saites starp lapām.</p><p>**Kur tie tiek rediģēti:** URL tiek rediģēti URL redaktorā. Nav nepieciešams kods, lai tās izveidotu vai modificētu.</p> |
| Līdzeklis | <p>**Definīcija:** līdzekļi ir failu bināri ar tādu paplašinājumu, kā .jpg, .docx, .pdf vai .mpg.</p><p>**Kur tie tiek atlasīti:** līdzekļi tiek atlasīti kā moduļa rekvizīti moduļiem, kuriem tie ir nepieciešami.</p><p>**Kur tie tiek rediģēti:** līdzekļi tiek augšupielādēti un saistītie metadati tiek rediģēti līdzekļu pārvaldniekā.</p> |

## <a name="additional-resources"></a>Papildu resursi

[Satura pievienošanas veidi](add-manage-content.md)

[Dokumenta stāvokļi un dzīves cikls](document-states-overview.md)

[Darbs ar publicēšanas grupām](publish-groups.md)

[Šķērskanālu kopīgošanas iespējošana un izmantošana](cross-channel-sharing.md)

[Darbs ar moduļiem](work-with-modules.md)

[Darbs ar fragmentiem](work-with-fragments.md)

[Pārskats par veidnēm un izkārtojumiem](templates-layouts-overview.md)

[Vietnes navigācijas pielāgošana](customize-site-navigation.md)
