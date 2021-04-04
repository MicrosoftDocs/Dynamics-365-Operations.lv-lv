---
title: Elektroniskās rēķinu izrakstīšanas pievienojumprogrammas administrēšanas komponenti
description: Šajā tēmā sniegta informācija par komponentiem, kas ir saistīti ar Elektronisko rēķinu izrakstīšanas pievienojumprogrammas administrēšanu.
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 70ef47dd45200a14c9d780f3c280c554d0e52ac3
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592578"
---
# <a name="electronic-invoicing-add-on-administration-components"></a>Elektroniskās rēķinu izrakstīšanas pievienojumprogrammas administrēšanas komponenti

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Šajā tēmā sniegta informācija par komponentiem, kas ir saistīti ar Elektronisko rēķinu izrakstīšanas pievienojumprogrammas administrēšanu. Tā sniedz arī informāciju par elektronisko rēķinu izrakstīšanas pievienojumprogrammas pakalpojuma konfigurēšanu.

## <a name="azure"></a>Azure

Izmantojiet Microsoft Azure, lai izveidotu noslēpumus atslēgai, kas atrodas krātuves kontā. Tad izmantojiet Elektronisko rēķinu izrakstīšanas pievienojumprogrammas konfigurācijas noslēpumus.

## <a name="lifecycle-services"></a>Lifecycle Services

Izmantojiet Microsoft Dynamics Lifecycle Services (LCS), lai iespējotu pievienojumprogrammu mikropakalpojumiem jūsu LCS izvietošanas projektam.

> [!NOTE]
> Mikropakalpojuma pievienojumprogrammas LCS instalācijai ir nepieciešama vismaz 2. pakāpes virtuālā mašīna. Lai iegūtu vairāk informācijas par vides plānošanu, skatiet [Vides plānošana](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
 

## <a name="regulatory-configuration-services"></a>Regulatory Configuration Services

Dynamics 365 Regulatory Configuration Services (RCS) ir interfeiss, ko izmanto, lai konfigurētu elektronisko rēķinu izrakstīšanas pievienojumprogrammu. Resursi, piemēram, vides un elektronisko rēķinu izrakstīšanas līdzekļi, tiek izveidoti, uzturēti un viesoti pakalpojumā RCS. Kad resursi ir gatavi, tie tiek publicēti Elektronisko rēķinu izrakstīšanas pievienojumprogrammas pakalpojumā.

Informāciju par RCS pierakstīšanos skatiet sadaļā [Regulatory services](https://marketing.configure.global.dynamics.com/).

Papildinformāciju par RCS skatiet sadaļā [Regulatory Configuration Services (RCS) — Globalizācijas līdzekļi](rcs-globalization-feature.md)

### <a name="integration-with-the-electronic-invoicing-add-on"></a>Integrēšana ar elektroniskās rēķinu izveides pievienojumprogrammu

Pirms RCS izmantošanas Elektronisko rēķinu konfigurēšanai, jums jākonfigurē RCS, lai ļautu sazināties ar Elektronisko rēķinu izrakstīšanas pievienojumprogrammu. Šī konfigurācija tiek pabeigta **Elektronisko pārskatu parametru** lapas **Elektronisko rēķinu izrakstīšanas pievienojumprogrammas** cilnē.

#### <a name="service-endpoint"></a>Pakalpojuma galapunkts

Elektronisko rēķinu izrakstīšanas pievienojumprogramma ir pieejama vairākās Azure datucentru ģeogrāfijās. Tabulā zemāk ir uzskaitīti pieejamības dati par reģionu.

| Azure datacenter ģeogrāfija |
|----------------------------|
| ASV austrumi                    |
| ASV rietumi                    |
| Ziemeļeiropa                   |
| Rietumeiropa                    |

### <a name="service-environments"></a>Pakalpojumu vides

Pakalpojumu vides ir loģiskie nodalījumi, kas izveidoti elektronisko rēķinu izrakstīšanas funkciju izpildes atbalstam Elektronisko rēķinu izrakstīšanas pievienojumprogrammai. Drošības noslēpumi un digitālie sertifikāti, un vadība (tas ir, piekļuves atļaujas) ir jākonfigurē pakalpojuma vides līmenī.

Klienti var izveidot tik daudz pakalpojumu vides, cik nepieciešams. Visas klientu izveidojušās pakalpojumu vides ir neatkarīgas viena no otras.

Pakalpojuma vides ir jāizveido un jāuztur pakalpojumā RCS. Kad pakalpojumu vides ir gatavas, tām jābūt publicētām Elektronisko rēķinu izrakstīšanas pievienojumprogrammā.

#### <a name="service-environment-status"></a>Vides statusa pakalpojums

Pakalpojuma vides var pārvaldīt ar statusu. Iespējamās opcijas ir šādas:

- **Nav publicēts** – vide ir izveidota, bet vēl nav publicēta.
- **Publicēts** – vide ir publicēta Elektronisko rēķinu izrakstīšanas pievienojumprogrammā.
- **Mainīts** – publicētās vides atribūti ir izmainīti, bet izmaiņas vēl nav publicētas.

#### <a name="customer-secrets"></a>Klienta noslēpumi

Elektronisko rēķinu izrakstīšanas pievienojumprogramma ir atbildīga par visu jūsu uzņēmuma datu glabāšanu Azure resursos, kas pieder jūsu uzņēmumam. Lai nodrošinātu, ka pakalpojums darbojas pareizi un ka visiem biznesa datiem, kas ir nepieciešami un ko ģenerē Elektronisko rēķinu izrakstīšanas pievienojumprogramma, ir piekļuve tikai pievienojumprogrammai, ir jāizveido divi galvenie Azure resursi:

- Azure krātuves konts (BLOB krātuve), kas glabās elektroniskos rēķinus
- Azure atslēgu glabātuve, kur tiks glabāti sertifikāti un krātuves konta vienoto resursu identifikatoru (URI)

> [!NOTE]
> Īpašam galvenās akreditācijas datu glabātuvei un debitora krātuves kontam ir jābūt piešķirtiem tieši lietošanai ar Elektronisko rēķinu izrakstīšanas pievienojumprogrammu.

Papildinformāciju skatiet šeit: [Azure krātuves konta un galvenās glabātavas izveide](e-invoicing-create-azure-storage-account-key-vault.md).

#### <a name="users"></a>Lietotāji

Katrai pakalpojumu videi ir jāsaraksta tās lietotājam, kas var pievienoties no Dynamics 365 Finance un Dynamics 365 Supply Chain Management Elektronisko rēķinu izrakstīšanas pievienojumprogrammā.

#### <a name="publication"></a>Publicēšana

Pakalpojumu vidēm ir jābūt publicētām Elektronisko rēķinu izrakstīšanas pievienojumprogrammā pirms to izmantošanas. Finance un Supply Chain Management var piekļūt tikai publicētām vidēm. Turklāt pakalpojumu vide ir jāpublicē pirms jebkādu tās atribūtu atjauninājumiem, kas stājas spēkā elektronisko rēķinu izrakstīšanas pakalpojumā.

### <a name="connected-applications"></a>Savienotās programmas

Saistītās programmas ir Finance un Supply Chain Management instances, kuras, iespējams, vēlēsities sasniegt, izmantojot RCS. Papildus programmas URL un tās nomniekam savienotā programma ietver akreditācijas datus, kas ļauj RCS izveidot savienojumu ar vidi.

Izmantojot savienotās programmas, varat konfigurēt daļu no elektronisko rēķinu izrakstīšanas funkcijas Finance un Supply Chain Management, lai izveidotu visu elektronisko rēķinu izrakstīšanas funkcijas darbu.

## <a name="finance-and-supply-chain-management"></a>Finance un Supply Chain Management

### <a name="integration-with-electronic-invoicing-add-on"></a>Integrēšana ar elektroniskās rēķinu izveides pievienojumprogrammu

Pirms Finance un Supply Chain Management izmantošanas, lai izsniegtu elektroniskos rēķinus ar Elektronisko rēķinu izrakstīšanas pievienojumprogrammas palīdzību, pievienojumprogramma ir jākonfigurē, lai ļautu sazināties ar pakalpojumu.

#### <a name="electronic-invoicing-add-on-integration-feature"></a>Elektronisko rēķinu izrakstīšanas pievienojumprogrammas integrēšanas līdzeklis

Lai iespējotu komunikāciju starp Finance un Supply Chain Management, un elektronisko rēķinu izrakstīšanas pievienojumprogrammu, jums jāieslēdz **Elektronisko rēķinu izrakstīšanas pievienojumprogrammas integrēšanas** līdzeklis **Līdzekļa pārvaldības** darbvietā.

#### <a name="service-endpoint"></a>Pakalpojuma galapunkts

Pakalpojuma galapunkts ir URL, kur atrodas Elektronisko rēķinu izrakstīšanas pievienojumprogramma. Pirms var tikt izdoti elektroniskie rēķini, pakalpojuma galapunktam jābūt konfigurētam pakalpojumos Finance un Supply Chain Management, lai ļautu sazināties ar pakalpojumu.

Lai konfigurētu pakalpojuma galapunktu, dodieties uz **Organizācijas administrēšana \> Iestatīšana \> Elektronisko dokumentu parametrs** un pēc tam cilnes **Iesniegšanas pakalpojumi** laukā **Elektronisko rēķinu izrakstīšanas pievienojumprogrammas URL** ievadiet URL kā aprakstīts sadaļas **Pakalpojuma galapunkts** tabulā.

#### <a name="environments"></a>Vides

Vides nosaukums, kas ir ievadīts pakalpojumos Finance un Supply Chain Management, attiecas uz vides nosaukumu, kas ir izveidots pakalpojumā RCS un publicēts Elektronisko rēķinu izrakstīšanas pievienojumprogrammā.

Vide ir jākonfigurē **Iesniegšanas pakalpojumi** cilnes **Elektronisko dokumentu parametra** lapā, lai katrā elektronisko rēķinu izsniegšanas pieprasījumā būtu vide, kur elektronisko rēķinu izrakstīšanas pievienojumprogramma var noteikt, kurai elektronisko rēķinu izrakstīšanas funkcijai ir jāapstrādā pieprasījums.

## <a name="additional-resources"></a>Papildu resursi

- [Konfigurēt elektroniskos rēķinus pakalpojumā RCS](e-invoicing-configuration-rcs.md)
- [Elektronisko rēķinu izdošana programmās Finance un Supply Chain Management](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
