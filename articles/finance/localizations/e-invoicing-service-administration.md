---
title: Elektroniskās rēķinu izveides administrēšanas komponenti
description: Šajā tēmā sniegta informācija par komponentiem, kas ir saistīti ar Elektronisko rēķinu izrakstīšanas administrēšanu.
author: gionoder
ms.date: 04/29/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 6582a0a9eda19fe69ead853ea5d79d763afcb8a468717fde84a32146fd0f79af
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721730"
---
# <a name="electronic-invoicing-administration-components"></a>Elektroniskās rēķinu izveides administrēšanas komponenti

[!include [banner](../includes/banner.md)]


Šajā tēmā sniegta informācija par komponentiem, kas ir saistīti ar Elektronisko rēķinu izrakstīšanas administrēšanu. Tā sniedz arī informāciju par elektronisko rēķinu izrakstīšanas pakalpojuma konfigurēšanu.

## <a name="azure"></a>Azure

Izmantojiet Microsoft Azure, lai izveidotu noslēpumus Key Vault un krātuves kontam. Tad izmantojiet Elektronisko rēķinu izrakstīšanas konfigurācijas noslēpumus.

## <a name="lifecycle-services"></a>Lifecycle Services

Izmantojiet Microsoft Dynamics Lifecycle Services (LCS), lai iespējotu mikropakalpojumus jūsu LCS izvietošanas projektam.

> [!NOTE]
> Mikropakalpojuma LCS instalācijai ir nepieciešama vismaz 2. pakāpes virtuālā mašīna. Lai iegūtu vairāk informācijas par vides plānošanu, skatiet [Vides plānošana](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
 

## <a name="regulatory-configuration-services"></a>Regulatory Configuration Services

Dynamics 365 Regulatory Configuration Services (RCS) ir interfeiss, ko izmanto, lai konfigurētu elektronisko rēķinu izrakstīšanu. Resursi, piemēram, vides un elektronisko rēķinu izrakstīšanas līdzekļi, tiek izveidoti, uzturēti un viesoti pakalpojumā RCS. Kad resursi ir gatavi, tie tiek publicēti Elektronisko rēķinu izrakstīšanas pakalpojumā.

Informāciju par RCS pierakstīšanos skatiet sadaļā [Regulatory services](https://marketing.configure.global.dynamics.com/).

Papildinformāciju par RCS skatiet sadaļā [Regulatory Configuration Services (RCS) — Globalizācijas līdzekļi](rcs-globalization-feature.md)

### <a name="integration-with-electronic-invoicing"></a>Integrēšana ar elektroniskās rēķinu izrakstīšanu 

Pirms RCS izmantošanas Elektronisko rēķinu konfigurēšanai, jums jākonfigurē RCS, lai ļautu sazināties ar Elektronisko rēķinu izrakstīšanu. Šī konfigurācija tiek pabeigta **Elektronisko pārskatu parametru** lapas **Elektronisko rēķinu izrakstīšanas** cilnē.

#### <a name="service-endpoint"></a>Pakalpojuma galapunkts

Elektronisko rēķinu izrakstīšana ir pieejama vairākās Azure datucentru ģeogrāfijās. Tabulā zemāk ir uzskaitīti pieejamības dati par reģionu.

| Azure datacenter ģeogrāfija |
|----------------------------|
| ASV              |
| Eiropa                     |
| Apvienotā Karaliste             |
| Āzija                       |

### <a name="service-environments"></a>Pakalpojumu vides

Pakalpojumu vides ir loģiskie nodalījumi, kas izveidoti elektronisko rēķinu izrakstīšanas funkciju izpildes atbalstam Elektronisko rēķinu izrakstīšanai. Drošības noslēpumi un digitālie sertifikāti, un vadība (tas ir, piekļuves atļaujas) ir jākonfigurē pakalpojuma vides līmenī.

Klienti var izveidot tik daudz pakalpojumu vides, cik nepieciešams. Visas klientu izveidojušās pakalpojumu vides ir neatkarīgas viena no otras.

Pakalpojuma vides ir jāizveido un jāuztur pakalpojumā RCS. Kad pakalpojumu vides ir gatavas, tām jābūt publicētām Elektronisko rēķinu izrakstīšanā.

#### <a name="service-environment-status"></a>Vides statusa pakalpojums

Pakalpojuma vides var pārvaldīt ar statusu. Iespējamās opcijas ir šādas:

- **Nav publicēts** – vide ir izveidota, bet vēl nav publicēta.
- **Publicēts** – vide ir publicēta Elektronisko rēķinu izrakstīšanā .
- **Mainīts** – publicētās vides atribūti ir izmainīti, bet izmaiņas vēl nav publicētas.

#### <a name="customer-secrets"></a>Klienta noslēpumi

Elektronisko rēķinu izrakstīšana ir atbildīga par visu jūsu uzņēmuma datu glabāšanu Azure resursos, kas pieder jūsu uzņēmumam. Lai nodrošinātu, ka pakalpojums darbojas pareizi un ka visiem biznesa datiem, kas ir nepieciešami un ko ģenerē Elektronisko rēķinu izrakstīšana, ir atbilstoši pieejami, ir jāizveido divi galvenie Azure resursi:

- Azure krātuves konts (BLOB krātuve), kas glabās elektroniskos rēķinus
- Azure Key Vault, kur tiks glabāti sertifikāti un krātuves konta vienoto resursu identifikatoru (URI)


Īpašam Key Vault un debitora krātuves kontam ir jābūt piešķirtiem tieši lietošanai ar Elektronisko rēķinu izrakstīšanu . Papildinformāciju skatiet šeit: [Azure krātuves konta un Key Vault izveide](e-invoicing-create-azure-storage-account-key-vault.md).

Lai pārraudzītu savas Key Vault darbspēju un saņemtu brīdinājumus, konfigurējiet Azure Monitor pakalpojumam Key Vault. Aktivizējot Key Vault reģistrāciju, var pārraudzīt, kad un kam ir piekļuve Key Vault. Papildinformāciju skatiet [Azure Key Vault uzraudzība un brīdināšana](/azure/key-vault/general/alert) un [Kā iespējot Key Vault reģistrāciju](/azure/key-vault/general/howto-logging?tabs=azure-cli).

Kā labākā prakse - periodiski pagriezt noslēpumus. Papildinformāciju skatiet [Noslēpumu dokumentācijā](/azure/key-vault/secrets/).

#### <a name="users"></a>Lietotāji

Katrai pakalpojumu videi ir jāsaraksta tās lietotājam, kas var pievienoties no Dynamics 365 Finance un Dynamics 365 Supply Chain Management Elektronisko rēķinu izrakstīšanā.

#### <a name="publication"></a>Publicēšana

Pakalpojumu vidēm ir jābūt publicētām Elektronisko rēķinu izrakstīšanā pirms to izmantošanas. Finance un Supply Chain Management var piekļūt tikai publicētām vidēm. Turklāt pakalpojumu vide ir jāpublicē pirms jebkādu tās atribūtu atjauninājumiem, kas stājas spēkā elektronisko rēķinu izrakstīšanas pakalpojumā.

### <a name="connected-applications"></a>Savienotās programmas

Saistītās programmas ir Finance un Supply Chain Management instances, kuras, iespējams, vēlēsities sasniegt, izmantojot RCS. Papildus programmas URL un tās nomniekam savienotā programma ietver akreditācijas datus, kas ļauj RCS izveidot savienojumu ar vidi.

Izmantojot savienotās programmas, varat konfigurēt daļu no elektronisko rēķinu izrakstīšanas funkcijas Finance un Supply Chain Management, lai izveidotu visu elektronisko rēķinu izrakstīšanas funkcijas darbu.

## <a name="finance-and-supply-chain-management"></a>Finance un Supply Chain Management

### <a name="integration-with-electronic-invoicing"></a>Integrēšana ar elektroniskās rēķinu izrakstīšanu

Pirms Finance un Supply Chain Management izmantošanas, lai izsniegtu elektroniskos rēķinus ar Elektronisko rēķinu izrakstīšanas palīdzību, tas ir jākonfigurē, lai ļautu sazināties ar pakalpojumu.

#### <a name="electronic-invoicing-integration-feature"></a>Elektronisko rēķinu izrakstīšanas integrēšanas līdzeklis

Lai iespējotu komunikāciju starp Finance un Supply Chain Management, un elektronisko rēķinu izrakstīšanu, jums jāieslēdz **Elektronisko rēķinu izrakstīšanas integrēšanas** līdzeklis **Līdzekļa pārvaldības** darbvietā.

#### <a name="service-endpoint"></a>Pakalpojuma galapunkts

Pakalpojuma galapunkts ir URL, kur atrodas Elektronisko rēķinu izrakstīšana. Pirms var tikt izdoti elektroniskie rēķini, pakalpojuma galapunktam jābūt konfigurētam pakalpojumos Finance un Supply Chain Management, lai ļautu sazināties ar pakalpojumu.

Lai konfigurētu pakalpojuma galapunktu, dodieties uz **Organizācijas administrēšana \> Iestatīšana \> Elektronisko dokumentu parametrs** un pēc tam cilnes **Iesniegšanas pakalpojumi** laukā **Elektronisko rēķinu izrakstīšanas URL** ievadiet URL kā aprakstīts sadaļas **Pakalpojuma galapunkts** tabulā.

#### <a name="environments"></a>Vides

Vides nosaukums, kas ir ievadīts pakalpojumos Finance un Supply Chain Management, attiecas uz vides nosaukumu, kas ir izveidots pakalpojumā RCS un publicēts Elektronisko rēķinu izrakstīšanā.

Vide ir jākonfigurē **Iesniegšanas pakalpojumi** cilnes **Elektronisko dokumentu parametra** lapā, lai katrā elektronisko rēķinu izsniegšanas pieprasījumā būtu vide, kur elektronisko rēķinu izrakstīšana var noteikt, kurai elektronisko rēķinu izrakstīšanas funkcijai ir jāapstrādā pieprasījums.

## <a name="additional-resources"></a>Papildu resursi

- [Konfigurēt elektroniskos rēķinus pakalpojumā RCS](e-invoicing-configuration-rcs.md)
- [Elektronisko rēķinu izdošana programmās Finance un Supply Chain Management](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
