---
title: Elektroniskās rēķinu izveides administrēšanas komponenti
description: Šajā rakstā ir sniegta informācija par komponentiem, kas ir saistīti ar Elektronisko rēķinu administrēšanu.
author: gionoder
ms.date: 08/31/2021
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
ms.openlocfilehash: cdd4d6705730bca967bb1bbff528df6d83a2390d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876005"
---
# <a name="electronic-invoicing-administration-components"></a>Elektroniskās rēķinu izveides administrēšanas komponenti

[!include [banner](../includes/banner.md)]


Šajā rakstā ir sniegta informācija par komponentiem, kas ir saistīti ar Elektronisko rēķinu administrēšanu. Tā sniedz arī informāciju par elektronisko rēķinu izrakstīšanas pakalpojuma konfigurēšanu.

## <a name="azure"></a>Azure

Lietojiet Microsoft Azure, lai izveidotu atslēgu akreditācijas datu komplekta slepenās vērtības un iestatītu krātuves kontu. Pēc tam izmantojiet atslēgu akreditācijas datu komplekta slepenās vērtības un krātuves konta SAS marķieri elektroniskās rēķinu izrakstīšanas konfigurācijā.

## <a name="lifecycle-services"></a>Lifecycle Services

Lietojiet  Microsoft Dynamics Lifecycle Services (LCS), lai iespējotu jūsu LCS izvietošanas projekta elektroniskās rēķinu izrakstīšanas pievienojumprogrammu.

> [!NOTE]
> Lai LCS instalētu pievienojumprogrammas, ir vajadzīga vismaz **2. līmeņa vide**. Lai iegūtu vairāk informācijas par vides plānošanu, skatiet [Vides plānošana](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
 

## <a name="regulatory-configuration-services"></a>Regulatory Configuration Services

Dynamics 365 Regulatory Configuration Services (RCS) ir interfeiss, ko izmanto, lai konfigurētu elektronisko rēķinu izrakstīšanu. Resursi, piemēram, vides un elektronisko rēķinu izrakstīšanas līdzekļi, tiek izveidoti, uzturēti un viesoti pakalpojumā RCS. Kad resursi ir gatavi, tie tiek publicēti Elektronisko rēķinu izrakstīšanas pakalpojumā.

Informāciju par RCS pierakstīšanos skatiet sadaļā [Regulatory services](https://marketing.configure.global.dynamics.com/).

Papildinformāciju par RCS skatiet sadaļā [Regulatory Configuration Services (RCS) — Globalizācijas līdzekļi](rcs-globalization-feature.md)

### <a name="integration-with-electronic-invoicing"></a>Integrēšana ar elektroniskās rēķinu izrakstīšanu 

Pirms RCS izmantošanas Elektronisko rēķinu konfigurēšanai, jums jākonfigurē RCS, lai ļautu sazināties ar Elektronisko rēķinu izrakstīšanu. Šī konfigurācija tiek pabeigta **Elektronisko pārskatu parametru** lapas **Elektronisko rēķinu izrakstīšanas** cilnē.

#### <a name="service-endpoint"></a><a id='svc-endpoint-uris'></a>Pakalpojuma galapunkts

Elektronisko rēķinu izrakstīšana ir pieejama vairākās Azure datucentru ģeogrāfijās. Tabulā zemāk ir uzskaitīti pieejamības dati par reģionu.


| Datacenter Azure ģeogrāfija | Pakalpojuma galapunkta URI                                                       |
|----------------------------|----------------------------------------------------------------------------|
| ASV              | <p>https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing</p> |
| Eiropa                     | <p>https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/</p> |
| Apvienotā Karaliste             | <p>https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p> |
| Āzija                       | <p>https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p> |

### <a name="service-environments"></a>Pakalpojumu vides

Pakalpojumu vides ir loģiski dalījumi, kuri tiek izveidoti, lai sekmētu globalizācijas līdzekļu izpildi elektroniskajā rēķinu izrakstīšanā. Drošības noslēpumi un digitālie sertifikāti, un vadība (tas ir, piekļuves atļaujas) ir jākonfigurē pakalpojuma vides līmenī.

Klienti var izveidot tik daudz pakalpojumu vides, cik nepieciešams. Visas klientu izveidojušās pakalpojumu vides ir neatkarīgas viena no otras.

Pakalpojuma vides ir jāizveido un jāuztur pakalpojumā RCS. Kad pakalpojumu vides ir gatavas, tām jābūt publicētām Elektronisko rēķinu izrakstīšanā.

#### <a name="service-environment-status"></a>Vides statusa pakalpojums

Pakalpojuma vides var pārvaldīt ar statusu. Iespējamās opcijas ir šādas:

- **Nav publicēts** – vide ir izveidota, bet vēl nav publicēta.
- **Publicēts** – vide ir publicēta Elektronisko rēķinu izrakstīšanā .
- **Mainīts** – publicētās vides atribūti ir izmainīti, bet izmaiņas vēl nav publicētas.

#### <a name="customer-secrets"></a>Klienta noslēpumi

Elektronisko rēķinu izrakstīšana ir atbildīga par visu jūsu uzņēmuma datu glabāšanu Azure resursos, kas pieder jūsu uzņēmumam. Lai nodrošinātu, ka pakalpojums darbojas pareizi un ka visiem biznesa datiem, kas ir nepieciešami un ko ģenerē Elektronisko rēķinu izrakstīšana, ir atbilstoši pieejami, ir jāizveido divi galvenie Azure resursi:

- Azure krātuves konts (BLOB krātuve), kurā tiks glabāti elektroniskie dokumenti, tostarp elektroniskie rēķini, dokumentu pārveidojumu rezultāti un atbildes no ārējiem tīmekļa pakalpojumiem.
- Azure atslēgu akreditācijas datu komplekts, kurā tiks glabāti sertifikāti un krātuves konta (SAS marķieris) vienotais resursu identifikators (URI).


Īpašam Key Vault un debitora krātuves kontam ir jābūt piešķirtiem tieši lietošanai ar Elektronisko rēķinu izrakstīšanu . Papildinformāciju skatiet šeit: [Azure krātuves konta un Key Vault izveide](e-invoicing-create-azure-storage-account-key-vault.md).

Lai pārraudzītu savas Key Vault darbspēju un saņemtu brīdinājumus, konfigurējiet Azure Monitor pakalpojumam Key Vault. Aktivizējot Key Vault reģistrāciju, var pārraudzīt, kad un kam ir piekļuve Key Vault. Papildinformāciju skatiet [Azure Key Vault uzraudzība un brīdināšana](/azure/key-vault/general/alert) un [Kā iespējot Key Vault reģistrāciju](/azure/key-vault/general/howto-logging?tabs=azure-cli).

Kā labākā prakse - periodiski pagriezt noslēpumus. Papildinformāciju skatiet [Noslēpumu dokumentācijā](/azure/key-vault/secrets/).

#### <a name="users"></a>Lietotāji

Katrai pakalpojumu videi ir jāsarakstam tās personas, kas var pievienoties no Dynamics 365 Finanšu un elektronisko Dynamics 365 Supply Chain Management rēķinu izrakstīšanas.

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

Lai konfigurētu pakalpojuma galapunktu, **\>\>** **·** **dodieties uz Organizācijas administrēšanas iestatījuma elektronisko dokumentu parametrus un pēc tam cilnes Elektronisko rēķinu izrakstīšana laukā Galapunkta URL** ievadiet attiecīgo URL [no](#svc-endpoint-uris) tabulas pakalpojuma galapunkta sadaļā iepriekš šajā rakstā.

#### <a name="environments"></a>Vides

Vides nosaukums, kas ir ievadīts pakalpojumos Finance un Supply Chain Management, attiecas uz vides nosaukumu, kas ir izveidots pakalpojumā RCS un publicēts Elektronisko rēķinu izrakstīšanā.

Videi jābūt konfigurētai lapas **Elektronisko dokumentu parametri** cilnē **Elektroniskā rēķinu izrakstīšana**. Tādējādi katrs pieprasījums izdot elektroniskus rēķinus satur vidi, kurā elektroniskā rēķinu izrakstīšana var noteikt, kuram līdzeklim ir šis pieprasījums jāapstrādā.

## <a name="additional-resources"></a>Papildu resursi

- [Konfigurēt elektroniskos rēķinus pakalpojumā RCS](e-invoicing-configuration-rcs.md)
- [Elektronisko rēķinu izdošana programmās Finance un Supply Chain Management](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
