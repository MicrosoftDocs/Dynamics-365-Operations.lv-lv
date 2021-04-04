---
title: Sākt darbu ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu
description: Šajā tēmā ir sniegta informācija, kas palīdzēs sākt darbu ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu programmās Microsoft Dynamics 365 Finance un Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 02/22/2021
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
ms.openlocfilehash: 56227e031f8205836bcae9ce26006fc8091c2863
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592554"
---
# <a name="get-started-with-the-electronic-invoicing-add-on"></a>Sākt darbu ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija, kas palīdzēs sākt darbu ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu.

Šajā tabulā uzskaitīti Elektronisko rēķinu izrakstīšanas līdzekļi un biznesa dokumenti, kuriem tie var tikt pielietoti.

| Līdzekļa nosaukums                         | Biznesa dokuments |
|--------------------------------------|-------------------|
| Austrijas elektroniskie rēķini (AT)    | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> |
| Beļģijas elektroniskais rēķins (BE)      | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> |
| Brazīlijas NF-e (BR)                  | <p>55. modeļa finanšu dokuments</p><p>Labojuma vēstule</p> |
| Brazīlijas NFS-e ABRASF Curitiba (BR) | Pakalpojuma finanšu dokumenti |
| Dānijas elektroniskais rēķins (DK)       | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> |
| Ēģiptes elektroniskais rēķins (EG)     | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> |
| Igaunijas elektroniskais rēķins (EE)     | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> |
| Somijas elektroniskais rēķins (FI)       | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> |
| Francijas elektroniskais rēķins (FR)       | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> |
| Vācijas elektroniskais rēķins (DE)       | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> |
| FatturaPA (IT)                       | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> |
| Meksikas CFDI Interfactura (MX)       | <p>Pārdošanas rēķins</p><p>Pavadzīme</p><p>Krājumu pārsūtīšana</p><p>Maksājuma papildinājums</p> |
| Nīderlandes elektroniskais rēķins (NL)        | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> |
| Norvēģijas elektroniskais rēķins (NO)    | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> |
| Spānijas elektroniskais rēķins (ES)      | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> |
| PEPPOL elektroniskais rēķins            | <p>Pārdošanas rēķins</p><p>Projekta rēķins</p> |

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms pabeidzat šajā tēmā norādītās procedūras, ir jāievieš šādi priekšnosacījumi:

- Konfigurējiet savu Regulēšanas konfigurācijas pakalpojumu (RCS) un jūsu Microsoft Dynamics 365 Finance vai Dynamics 365 Supply Chain Management vidi, lai jūs varētu iesniegt elektronisko rēķinu izrakstīšanas pievienojumprogrammu.
- Izveidojiet pakalpojumu vidi un publicējiet to Elektronisko rēķinu izrakstīšanas pievienojumprogrammā. Papildinformāciju skatiet sadaļā [Sākt ar elektronisko rēķinu izrakstīšanas pievienojumprogrammas pakalpojuma administrēšana](e-invoicing-get-started-service-administration.md).
- Izveidojiet pievienotu pievienojumprogrammu. Papildinformāciju skatiet sadaļā [Sākt ar elektronisko rēķinu izrakstīšanas pievienojumprogrammas pakalpojuma administrēšana](e-invoicing-get-started-service-administration.md).
- Izveidojiet konfigurācijas nodrošinātāju jūsu uzņēmumam. Papildinformāciju skatiet [Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider"></a>Importēt Elektronisko rēķinu izrakstīšanas līdzekli no Microsoft konfigurācijas nodrošinātāja 

1. Piesakieties savā Regulēšanas konfigurācijas pakalpojuma (RCS) kontā.
2. Darbvietā **Globalizācijas līdzeklis** sadaļā **Līdzekli** atlasiet elementu **Elektronisko rēķinu izrakstīšanas pievienojums**.
3. Atlasiet **Importēt** un pēc tam atlasiet **Sinhronizēt**.
4. Filtrējiet kolonnu **Konfigurācijas nodrošinātājs** pēc termina **Microsoft**.
5. Šīs tēmas sākumā tabulā atlasiet Elektroniskās rēķinu izrakstīšanas līdzekļa nosaukumu un pēc tam atlasiet **Importēt**.

## <a name="create-an-electronic-invoicing-feature-under-your-organization-provider"></a>Izveidojiet Elektronisko rēķinu izrakstīšanas līdzekli jūsu organizācijas nodrošinātājā

1. Darbvietas **Globalizācijas līdzekļi** sadaļas **Līdzekļi** RCS atlasiet elementu **Elektronisko rēķinu izrakstīšanas pievienojumprogramma**.
2. Atlasiet **Pievienot** > **Pamatojoties uz esošo līdzekli**, un laukā **Nosaukums** ievadiet Elektronisko rēķinu izrakstīšanas līdzekļa nosaukumu.
3. Laukā **Apraksts** ievadiet līdzekļa aprakstu.
4. Sadaļā **Bāzes līdzekļa lauks** atlasiet importēto elektronisko rēķinu izrakstīšanas līdzekli no Microsoft konfigurācijas nodrošinātāja.
5. Atlasiet **Izveidot līdzekli**.

## <a name="configure-the-electronic-invoicing-feature"></a>Elektronisko rēķinu izrakstīšanas funkcijas konfigurēšana

Atkarībā no valsts vai reģiona elektronisko rēķinu izrakstīšanas funkcijai var būt nepieciešama papildu konfigurācija. 

Īpašiem soļiem skatiet dokumentāciju "Sākt darbu", kas ir pieejama jūsu valstij vai reģionam.

## <a name="configure-the-application-setup"></a>Lietojumprogrammas iestatīšanas konfigurēšana

1. Atlasiet jūsu izveidoto elektronisko rēķinu izrakstīšanas līdzekli.
2. Cilnē **Versija** pārbaudiet, vai ir atlasīta **Melnraksta** versija.
3. Cilnē **Iestatījumi** atlasiet **Lietojumprogrammas iestatīšana**.

    > [!NOTE]
    > Pārbaudiet, vai jūsu uzņēmums ir iestatīts kā **Aktīvs** konfigurācijas nodrošinātājs. Papildinformāciju skatiet [Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu.](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

4. Atlasiet **Līdzekļa iestatīšana** un pēc tam atlasiet **Saistītā lietojumprogramma**.
5. Sadaļā **Elektronisko dokumentu tipi** atlasiet **Pievienot**.
6. Katram biznesa dokumentam, kuru šī funkcija atbalsta, atlasiet un ievadiet **Tabulas nosaukuma** vērtību saskaņā ar šo tabulu.

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

7. Katram biznesa dokumentam, kuru šī funkcija atbalsta, atlasiet un ievadiet **Konteksta** vērtību saskaņā ar šo tabulu.

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

8. Katram biznesa dokumentam, kuru šī funkcija atbalsta, atlasiet un ievadiet **Biznesa dokumentu kartēšanas** vērtību saskaņā ar šo tabulu.

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

Atkarībā no valsts vai reģiona elektronisko rēķinu izrakstīšanas funkcijai var būt nepieciešama papildu konfigurācija.

Īpašiem soļiem skatiet dokumentāciju "Sākt darbu", kas ir pieejama jūsu valstij vai reģionam.

## <a name="deploy-the-electronic-invoicing-feature"></a>Elektronisko rēķinu izrakstīšanas funkcijas izvietošana

1. Cilnē **Versijas** atlasiet izvietojamā elektronisko rēķinu izrakstīšanas līdzekļa versiju.
2. Atlasiet **Mainīt statusu** \> **Pabeigts**.
3. Atlasiet **Mainīt statusu** \> **Publicēt**.
4. Atlasiet **Izvietot**.
5. Iestatiet opciju **Izvietot savienotā programmā** uz **Jā**.
6. Lapā **Savienot programmu** atlasiet savienojumu, kas ir saistīts ar jūsu Finance vai Supply Chain Management instanci.
7. Iestatiet opciju **Izvietot pakalpojuma vidē** uz **Jā**.
8. Laukā **Pakalpojumu vide** atlasiet elektronisko rēķinu izrakstīšanas pievienojumprogrammu pakalpojuma vidi, kurā vēlaties izvietot Elektronisko rēķinu izrakstīšanas līdzekli.
9. Laukā **No datuma** atlasiet datumu, kad Elektronisko rēķinu izrakstīšanas funkcijai jāstājas spēkā Elektronisko rēķinu izrakstīšanas pievienojumprogrammā.
10. Atlasiet **Labi**.

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
2. Kopsavilkuma cilnē **Ieraksts, kas jāiekļauj** atlasiet **Filtrs**.
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

- [Elektroniskās rēķinu izveides pievienojumprogrammas pārskats](e-invoicing-service-overview.md)
- [Darba sākšana ar elektroniskās rēķinu izveides pievienojumprogrammas servisa administrēšanu](e-invoicing-get-started-service-administration.md)
- [Sākt ar elektronisko rēķinu pievienojumu Brazīlijai](e-invoicing-bra-get-started.md)
- [Sākt ar elektronisko rēķinu pievienojumu Meksikai](e-invoicing-mex-get-started.md)
- [Sākt ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu Itālijai](e-invoicing-ita-get-started.md)
- [Klientu elektroniskie rēķini Ēģiptē](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
