---
title: Darba sākšana ar elektroniskās rēķinu izveidi
description: Šajā tēmā ir sniegta informācija, kas palīdzēs sākt darbu ar elektronisko rēķinu izrakstīšanu programmās Microsoft Dynamics 365 Finance un Dynamics 365 Supply Chain Management.
author: gionoder
ms.date: 08/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 3ba0b68ee61b130b8d0304d0bac6d1d720af8139
ms.sourcegitcommit: baf82100f0aa7d5f5f47c7f54bc155d8a07beab5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/31/2021
ms.locfileid: "7463844"
---
# <a name="get-started-with-electronic-invoicing"></a>Darba sākšana ar elektroniskās rēķinu izveidi

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija, kas palīdzēs sākt darbu ar elektronisko rēķinu izveidi. Šajā tēmā ir sniegta informācija par Regulatory Configuration Services (RCS) un Dynamics 365 Finance, kā arī sniegtas darbības, kas jāveic, lai iesniegtu biznesa dokumentus un pārskatītu apstrādes rezultātus.

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms pabeidzat šajā tēmā norādītās procedūras, ir jāievieš šādi priekšnosacījumi:

- Konfigurējiet Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Service (RCS) un Microsoft Dynamics 365 Finance vai Dynamics 365 Supply Chain Management vidi. Papildinformāciju skatiet sadaļā [Sākt ar elektronisko rēķinu izrakstīšanas pakalpojuma administrēšana](e-invoicing-get-started-service-administration.md).
- Izveidojiet konfigurācijas nodrošinātāju jūsu uzņēmumam. Papildinformāciju skatiet [Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider"></a>Importēt Elektronisko rēķinu izrakstīšanas līdzekli no Microsoft konfigurācijas nodrošinātāja 

1. Piesakieties savā Regulēšanas konfigurācijas pakalpojuma (RCS) kontā.
2. Darbvietas **Globalizācijas līdzekļi** sadaļā **Līdzekļi** atlasiet elementu **Elektronisko rēķinu izrakstīšana**.
3. Atlasiet **Importēt** un pēc tam atlasiet **Sinhronizēt**.
4. Filtrējiet kolonnu **Konfigurācijas nodrošinātājs** pēc termina **Microsoft**.
5. Tabulā atlasiet elektroniskās rēķinu izrakstīšanas līdzekļa nosaukumu un atlasiet **Importēt**.

## <a name="create-an-electronic-invoicing-feature-under-your-organization-provider"></a>Izveidojiet Elektronisko rēķinu izrakstīšanas līdzekli jūsu organizācijas nodrošinātājā

1. RCS darbtelpas **Globalizācijas līdzekļi** sadaļā **Līdzekļi** atlasiet rūti **Elektroniskā rēķinu izrakstīšana**.
2. Atlasiet **Pievienot** > **Pamatojoties uz esošo līdzekli**, un laukā **Nosaukums** ievadiet Elektronisko rēķinu izrakstīšanas līdzekļa nosaukumu.
3. Laukā **Apraksts** ievadiet līdzekļa aprakstu.
4. Sadaļā **Bāzes līdzekļa lauks** atlasiet importēto elektronisko rēķinu izrakstīšanas līdzekli no Microsoft konfigurācijas nodrošinātāja.
5. Atlasiet **Izveidot līdzekli**.

## <a name="country-specific-configuration-for-electronic-invoicing-feature"></a>Valsts konfigurācijas elektronisko rēķinu līdzeklim

Atkarībā no valsts vai reģiona elektronisko rēķinu izrakstīšanas funkcijai var būt nepieciešama specifiska konfigurācija. 

Īpašiem soļiem skatiet dokumentāciju "Sākt darbu", kas ir pieejama jūsu valstij vai reģionam.

## <a name="import-the-model-mapping-configurations-from-electronic-reporting"></a>Modeļu kartēšanas konfigurāciju importēšana no elektronisko pārskatu veidošanas

1. Programmā RCS atlasiet darbvietu **Elektronisko pārskatu veidošana**.
2. Sarakstā **Microsoft** konfigurācijas nodrošinātāji, atlasiet **Repozitoriji**.
3. Atlasiet **Globāls** un darbību rūtī atlasiet **Atvērt**.
4. Importējiet modeļa kartēšanas konfigurācijas atbilstoši tālāk norādītajai tabulai pēc līdzekļa nosaukuma.

| Līdzekļa nosaukums                         | Modeļa kartējuma konfigurācija |
|--------------------------------------|-----------------------------|
| Austrijas elektroniskie rēķini (AT)    | <p>Debitora rēķina konteksta modelis</p><p>Rēķina modelis</p> |
| Beļģijas elektroniskais rēķins (BE)      | <p>Debitora rēķina konteksta modelis</p><p>Rēķina modelis</p> |
| Brazīlijas NF-e (BR)                  | <p>Debitora rēķina konteksta modelis</p><p>Finanšu dokumenti</p><p>Atbildes ziņojuma modelis</p> |
| Brazīlijas NFS-e ABRASF Curitiba (BR) | <p>Debitora rēķina konteksta modelis</p><p>Finanšu dokumenti</p><p>Atbildes ziņojuma modelis</p> |
| Dānijas elektroniskais rēķins (DK)       | <p>Debitora rēķina konteksta modelis</p><p>Rēķina modelis</p> |
| Ēģiptes elektroniskais rēķins (EG)     | <p>Debitora rēķina konteksta modelis</p><p>Rēķina modelis</p><p>Atbildes ziņojuma modelis</p> |
| Igaunijas elektroniskais rēķins (EE)     | <p>Debitora rēķina konteksta modelis</p><p>Rēķina modelis</p> |
| Somijas elektroniskais rēķins (FI)       | <p>Debitora rēķina konteksta modelis</p><p>Rēķina modelis</p> |
| Francijas elektroniskais rēķins (FR)       | <p>Debitora rēķina konteksta modelis</p><p>Rēķina modelis</p> |
| Vācijas elektroniskais rēķins (DE)       | <p>Debitora rēķina konteksta modelis</p><p>Rēķina modelis</p> |
| FatturaPA (IT)                       | <p>Debitora rēķina konteksta modelis</p><p>Rēķina modelis</p> |
| Meksikas CFDI Interfactura (MX)       | <p>Debitora rēķina konteksta modelis</p><p>Rēķina modelis</p><p>Atbildes ziņojuma modelis</p> |
| Nīderlandes elektroniskais rēķins (NL)        | <p>Debitora rēķina konteksta modelis</p><p>Rēķina modelis</p> |
| Norvēģijas elektroniskais rēķins (NO)    | <p>Debitora rēķina konteksta modelis</p><p>Rēķina modelis</p> |
| Spānijas elektroniskais rēķins (ES)      | <p>Debitora rēķina konteksta modelis</p><p>Rēķina modelis</p> |
| PEPPOL elektroniskais rēķins            | <p>Debitora rēķina konteksta modelis</p><p>Rēķina modelis</p> |


## <a name="configure-the-application-setup"></a>Lietojumprogrammas iestatīšanas konfigurēšana

1. Atlasiet jūsu izveidoto elektronisko rēķinu izrakstīšanas līdzekli.
2. Cilnē **Iestatījumi** atlasiet **Lietojumprogrammas iestatīšana**.
3. Laukā **Savienot programmu** atlasiet savienojumu, kas ir saistīts ar jūsu Finance vai Supply Chain Management instanci.
4. Sadaļā **Elektronisko dokumentu tipi** atlasiet **Pievienot**.
5. Atlasiet un ievadiet vērtību **Tabulas nosaukums** atbilstoši tālāk norādītajai tabulai.

    | Līdzekļa nosaukums                         | Biznesa dokuments | Tabulas nosaukums |
    |--------------------------------------|-------------------|------------|
    | Austrijas elektroniskie rēķini (AT)    | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Debitoru rēķinu žurnāls</p><p>Projekta rēķins</p> |
    | Beļģijas elektroniskais rēķins (BE)      | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Debitoru rēķinu žurnāls</p><p>Projekta rēķins</p> |
    | Brazīlijas NF-e (BR)                  | <p>Finanšu dokuments</p><p>Labojuma vēstule</p> | Finanšu dokuments |
    | Brazīlijas NFS-e ABRASF Curitiba (BR) | Pakalpojuma finanšu dokumenti | Finanšu dokuments |
    | Dānijas elektroniskais rēķins (DK)       | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Debitoru rēķinu žurnāls</p><p>Projekta rēķins</p> |
    | Ēģiptes elektroniskais rēķins (EG)     | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Debitoru rēķinu žurnāls</p><p>Projekta rēķins</p> |
    | Igaunijas elektroniskais rēķins (EE)     | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Debitoru rēķinu žurnāls</p><p>Projekta rēķins</p> |
    | Somijas elektroniskais rēķins (FI)       | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Debitoru rēķinu žurnāls</p><p>Projekta rēķins</p> |
    | Francijas elektroniskais rēķins (FR)       | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Debitoru rēķinu žurnāls</p><p>Projekta rēķins</p> |
    | Vācijas elektroniskais rēķins (DE)       | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Debitoru rēķinu žurnāls</p><p>Projekta rēķins</p> |
    | FatturaPA (IT)                       | <p>Pārdošanas rēķins</p><p>Projekta rēķins | <p>Debitoru rēķinu žurnāls</p><p>Projekta rēķins</p> |
    | Meksikas CFDI Interfactura (MX)       | <p>Pārdošanas rēķins</p><p>Pavadzīme</p><p>Krājumu pārsūtīšana</p><p>Maksājuma papildinājums</p> | Debitoru rēķinu žurnāls |
    | Nīderlandes elektroniskais rēķins (NL)        | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Debitoru rēķinu žurnāls</p><p>Projekta rēķins</p> |
    | Norvēģijas elektroniskais rēķins (NO)    | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Debitoru rēķinu žurnāls</p><p>Projekta rēķins</p> |
    | Spānijas elektroniskais rēķins (ES)      | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Debitoru rēķinu žurnāls</p><p>Projekta rēķins</p> |
    | PEPPOL elektroniskais rēķins            | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Debitoru rēķinu žurnāls</p><p>Projekta rēķins</p> |

6. Katram izveidotajam tabulas nosaukumam atlasiet un ievadiet konteksta vērtību atbilstoši šai tabulai.

    | Līdzekļa nosaukums                         | Biznesa dokuments | Konteksts |
    |--------------------------------------|-------------------|---------|
    | Austrijas elektroniskie rēķini (AT)    | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Klienta rēķina konteksta modelis — Klienta rēķina konteksts</p><p>Klienta rēķina konteksta modelis — Projekta rēķina konteksts</p> |
    | Beļģijas elektroniskais rēķins (BE)      | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Klienta rēķina konteksta modelis — Klienta rēķina konteksts</p><p>Klienta rēķina konteksta modelis — Projekta rēķina konteksts</p> |
    | Brazīlijas NF-e (BR)                  | <p>Finanšu dokuments</p><p>Labojuma vēstule</p> | <p>Klienta rēķina konteksta modelis — Finanšu dokumenta konteksts</p><p>Klienta rēķina konteksta modelis — FD labojuma vēstules konteksts</p> |
    | Brazīlijas NFS-e ABRASF Curitiba (BR) | Pakalpojuma finanšu dokumenti| Klienta rēķina konteksta modelis — Finanšu dokumenta konteksts |
    | Dānijas elektroniskais rēķins (DK)       | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Klienta rēķina konteksta modelis — Klienta rēķina konteksts</p><p>Klienta rēķina konteksta modelis — Projekta rēķina konteksts</p> |
    | Ēģiptes elektroniskais rēķins (EG)     | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Klienta rēķina konteksta modelis — Klienta rēķina konteksts</p><p>Klienta rēķina konteksta modelis — Projekta rēķina konteksts</p> |
    | Igaunijas elektroniskais rēķins (EE)     | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Klienta rēķina konteksta modelis — Klienta rēķina konteksts</p><p>Klienta rēķina konteksta modelis — Projekta rēķina konteksts</p> |
    | Somijas elektroniskais rēķins (FI)       | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Klienta rēķina konteksta modelis — Klienta rēķina konteksts</p><p>Klienta rēķina konteksta modelis — Projekta rēķina konteksts</p> |
    | Francijas elektroniskais rēķins (FR)       | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Klienta rēķina konteksta modelis — Klienta rēķina konteksts</p><p>Klienta rēķina konteksta modelis — Projekta rēķina konteksts</p> |
    | Vācijas elektroniskais rēķins (DE)       | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Klienta rēķina konteksta modelis — Klienta rēķina konteksts</p><p>Klienta rēķina konteksta modelis — Projekta rēķina konteksts</p> |
    | FatturaPA (IT)                       | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Klienta rēķina konteksta modelis — Klienta rēķina konteksts</p><p>Klienta rēķina konteksta modelis — Projekta rēķina konteksts</p> |
    | Meksikas CFDI Interfactura (MX)       | <p>Pārdošanas rēķins</p><p>Pavadzīme</p><p>Krājumu pārsūtīšana</p><p>Maksājuma papildinājums</p> | Klienta rēķina konteksta modelis — Klienta rēķina konteksts |
    | Nīderlandes elektroniskais rēķins (NL)        | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Klienta rēķina konteksta modelis — Klienta rēķina konteksts</p><p>Klienta rēķina konteksta modelis — Projekta rēķina konteksts</p> |
    | Norvēģijas elektroniskais rēķins (NO)    | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Klienta rēķina konteksta modelis — Klienta rēķina konteksts</p><p>Klienta rēķina konteksta modelis — Projekta rēķina konteksts</p> |
    | Spānijas elektroniskais rēķins (ES)      | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Klienta rēķina konteksta modelis — Klienta rēķina konteksts</p><p>Klienta rēķina konteksta modelis — Projekta rēķina konteksts</p> |
    | PEPPOL elektroniskais rēķins            | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Klienta rēķina konteksta modelis — Klienta rēķina konteksts</p><p>Klienta rēķina konteksta modelis — Projekta rēķina konteksts</p> |

7. Katram tabulas nosaukumam un kontekstam atlasiet un ievadiet biznesa dokumenta kartējuma vērtību atbilstoši šai tabulai.

    | Līdzekļa nosaukums                         | Biznesa dokuments | Biznesa dokumenta kartējums |
    |--------------------------------------|-------------------|---------------------------|
    | Austrijas elektroniskie rēķini (AT)    | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Rēķina modeļa kartēšana - Klienta rēķins</p><p>Rēķina modeļa kartēšana - Projekta rēķins</p> |
    | Beļģijas elektroniskais rēķins (BE)      | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Rēķina modeļa kartēšana - Klienta rēķins</p><p>Rēķina modeļa kartēšana - Projekta rēķins</p> |
    | Brazīlijas NF-e (BR)                  | <p>Finanšu dokuments</p><p>Labojuma vēstule</p> | <p>Finanšu dokumenta kartēšana — Finanšu dokumenta kartēšana</p><p>Finanšu dokumenta kartēšana — labojumu vēstules kartēšana</p> |
    | Brazīlijas NFS-e ABRASF Curitiba (BR) | Pakalpojuma finanšu dokumenti | Finanšu dokumenta kartēšana — Finanšu dokumenta kartēšana |
    | Dānijas elektroniskais rēķins (DK)       | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Rēķina modeļa kartēšana - Klienta rēķins</p><p>Rēķina modeļa kartēšana - Projekta rēķins</p> |
    | Ēģiptes elektroniskais rēķins (EG)     | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Rēķina modeļa kartēšana - Klienta rēķins</p><p>Rēķina modeļa kartēšana - Projekta rēķins</p> |
    | Igaunijas elektroniskais rēķins (EE)     | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Rēķina modeļa kartēšana - Klienta rēķins</p><p>Rēķina modeļa kartēšana - Projekta rēķins</p> |
    | Somijas elektroniskais rēķins (FI)       | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Rēķina modeļa kartēšana - Klienta rēķins</p><p>Rēķina modeļa kartēšana - Projekta rēķins</p> |
    | Francijas elektroniskais rēķins (FR)       | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Rēķina modeļa kartēšana - Klienta rēķins</p><p>Rēķina modeļa kartēšana - Projekta rēķins</p> |
    | Vācijas elektroniskais rēķins (DE)       | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Rēķina modeļa kartēšana - Klienta rēķins</p><p>Rēķina modeļa kartēšana - Projekta rēķins</p> |
    | FatturaPA (IT)                       | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Rēķina modeļa kartēšana - Klienta rēķins</p><p>Rēķina modeļa kartēšana - Projekta rēķins</p> |
    | Meksikas CFDI Interfactura (MX)       | <p>Pārdošanas rēķins</p><p>Pavadzīme</p><p>Krājumu pārsūtīšana</p><p>Maksājuma papildinājums</p> | Rēķina modeļa kartēšana - Klienta rēķins |
    | Nīderlandes elektroniskais rēķins (NL)        | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Rēķina modeļa kartēšana - Klienta rēķins</p><p>Rēķina modeļa kartēšana - Projekta rēķins</p> |
    | Norvēģijas elektroniskais rēķins (NO)    | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Rēķina modeļa kartēšana - Klienta rēķins</p><p>Rēķina modeļa kartēšana - Projekta rēķins</p> |
    | Spānijas elektroniskais rēķins (ES)      | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Rēķina modeļa kartēšana - Klienta rēķins</p><p>Rēķina modeļa kartēšana - Projekta rēķins</p> |
    | PEPPOL elektroniskais rēķins            | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> | <p>Rēķina modeļa kartēšana - Klienta rēķins</p><p>Rēķina modeļa kartēšana - Projekta rēķins</p> |


## <a name="country-specific-configuration-of-application-setup"></a>Valstij specifiska lietojumprogrammas iestatījumu konfigurācija

Atkarībā no valsts vai reģiona Programmas iestātījumam var būt nepieciešama specifiska konfigurācija. 

Īpašiem soļiem skatiet dokumentāciju "Sākt darbu", kas ir pieejama jūsu valstij vai reģionam.

## <a name="deploy-the-electronic-invoicing-feature-to-service-environment"></a>Elektroniskās rēķinu izrakstīšanas līdzekļa izvietošana pakalpojuma vidē

1. Cilnē **Versijas** atlasiet izvietojamā elektronisko rēķinu izrakstīšanas līdzekļa versiju.
2. Atlasiet **Mainīt statusu** \> **Pabeigts**.
3. Atlasiet **Mainīt statusu** \> **Publicēt**.
4. Atlasiet **Izvietot**.
5. Iestatiet opciju **Izvietot savienotā programmā** uz **Nē**.
6. Iestatiet opciju **Izvietot pakalpojuma vidē** uz **Jā**.
7. Laukā **Pakalpojumu vide** atlasiet elektronisko rēķinu izrakstīšanu pakalpojuma vidi, kurā vēlaties izvietot Elektronisko rēķinu izrakstīšanas līdzekli.
8. Laukā **No datuma** atlasiet datumu, kad Elektronisko rēķinu izrakstīšanas funkcijai jāstājas spēkā Elektronisko rēķinu izrakstīšanā.
9. Atlasiet **Labi**.

## <a name="deploy-the-electronic-invoicing-feature-to-connected-application"></a>Elektroniskās rēķinu izrakstīšanas līdzekļa izvietošana saistītajā programmā

1. Cilnē **Versijas** atlasiet izvietojamā elektronisko rēķinu izrakstīšanas līdzekļa versiju.
2. Atlasiet **Izvietot**.
3. Iestatiet opciju **Izvietot savienotā programmā** uz **Jā**.
4. Laukā **Savienot programmu** atlasiet savienojumu, kas ir saistīts ar jūsu Finance vai Supply Chain Management instanci.
5. Iestatiet opciju **Izvietot pakalpojuma vidē** uz **Nē**.
6. Atlasiet **Labi**.

## <a name="turn-on-the-electronic-invoicing-feature-in-finance-or-supply-chain-management"></a>Ieslēdziet Elektronisko rēķinu izrakstīšanas līdzekli Finance vai Supply Chain Management instancēs

1. Piesakieties Finance vai Supply Chain Management instancēs un pārbaudiet, vai esat pareizajā juridiskajā personā.
2. Dodieties uz **Organizācijas administrēšana** \> **Iestatījumi** \> **Elektronisko dokumentu parametri**.
3. Cilnē **Līdzekļi** atlasiet valstij/reģionam specifisko līdzekli, lai ieslēgtu Elektronisko rēķinu izrakstīšanas līdzekli programmai Finance vai Supply Chain Management. Tabulā zemāk sniegts saraksts ar elektroniskajiem rēķinu izrakstīšanas līdzekļiem, kas pieejami noteiktai valstij/reģioniem. 

    | Līdzekļa nosaukums                                          | Valsts/reģions  |
    |-------------------------------------------------------|-----------------|
    | Austrijas elektroniskie rēķini (AT)                     | Austrija         |
    | Beļģijas elektroniskais rēķins (BE)                       | Beļģija         |
    | CFDI Meksikas elektroniskais rēķins (MX)                  | Meksika          |
    | Dānijas elektroniskais rēķins (DK)                        | Dānija         |
    | Nīderlandes elektroniskais rēķins (NL)                         | Nīderlande |
    | Ēģiptes elektroniskais rēķins (EG)                      | Ēģipte           |
    | Igaunijas elektroniskais rēķins (EE)                      | Igaunija         |
    | Somijas elektroniskais rēķins (FI)                       | Somija         |
    | Francijas elektroniskais rēķins (FR)                        | Francija          |
    | Vācijas elektroniskais rēķins (DE)                        | Vācija         |
    | Itālijas elektroniskais rēķins (IT)                       | Itālija           |
    | NF-e Federal — Brazīlijas elektroniskais rēķins (BR)      | Brazīlija          |
    | NFS-e — Brazīlijas pakalpojumu (pilsētas) elektroniskais rēķins   | Brazīlija          |
    | Norvēģijas elektroniskais rēķins (NO)                     | Norvēģija          |
    | PEPPOL elektroniskais rēķins                             | Globāls          |
    | Spānijas elektroniskais rēķins (ES)                       | Spānija           |

4. Atlasiet **Saglabāt**.

## <a name="issue-electronic-invoices"></a>Izsniegt elektroniskos rēķinus

1. Dodieties uz **Organizācijas administrēšana** \> **Periodiskais** \> **Elektroniskie dokumenti** \> **Iesniegt elektroniskus dokumentus**.
2. Kopsavilkuma cilnē **Ieraksti, kas jāiekļauj** atlasiet **Filtrs**.
3. Atlasiet **Pievienot**, lai vaicājuma filtram pievienotu tabulas nosaukumu.
4. Atlasiet tabulu, kurā ir rēķini.

    > [!NOTE]
    > Tabulas nosaukumam jābūt uzskaitītam tabulā iepriekš šīs tēmas sadaļā [Konfigurēt lietojumprogrammas iestatīšanu](#configure-the-application-setup).

5. Atlasiet lauka nosaukumu tabulā, kurā vēlaties vaicāt.
6. Ievadiet tabulas nosaukumu un lauka nosaukumu vaicājuma kritērijiem.
7. Atkārtojiet 5. un 6. darbību, lai pievienotu vaicājumam vairāk lauku un kritēriju, un pēc tam atlasiet **Labi**.
8. Atlasiet **Labi**.

## <a name="view-submission-logs"></a>Skatīt iesniegšanas žurnālus

1. Dodieties uz **Organizācijas administrēšana** \> **Periodiskais** \> **Elektroniskie dokumenti** \> **Elektronisko dokumentu iesniegšanas žurnāls**.
2. Laukā **Dokumentu tips** izvēlieties tabulu, kurā ir rēķini.

    > [!NOTE]
    > Tabulas nosaukumam jābūt uzskaitītam tabulā iepriekš šīs tēmas sadaļā [Konfigurēt lietojumprogrammas iestatīšanu](#configure-the-application-setup).

3. Atlasiet režģī esošu rēķinu un pēc tam atlasiet **Uzziņas** \> **Iesniegšanas informācija**.


## <a name="related-topics"></a>Saistītās tēmas

- [Elektroniskās rēķinu izveides pārskats](e-invoicing-service-overview.md)
- [Darba sākšana ar elektroniskās rēķinu izveides servisa administrēšanu](e-invoicing-get-started-service-administration.md)
- [Darba sākšana ar elektronisko rēķinu izveidi lietošanai Brazīlijā](e-invoicing-bra-get-started.md)
- [Darba sākšana ar elektronisko rēķinu izveidi lietošanai Meksikā](e-invoicing-mex-get-started.md)
- [Darba sākšana ar elektroniskās rēķinu izveidi lietošanai Itālijā](e-invoicing-ita-get-started.md)
- [Klientu elektroniskie rēķini Ēģiptē](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
