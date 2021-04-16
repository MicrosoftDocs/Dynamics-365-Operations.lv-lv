---
title: Kopējo izmaksu pārskati
description: Šajā tēmā ir aprakstīts, kā atrast un izmantot dažādus pārskatu tipus, kas ir pieejami Kopējo izmaksu modulim.
author: sherry-zheng
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-21
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 90630a29d8ad77931735a81ee152aa76514a387c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821085"
---
# <a name="landed-cost-reports"></a>Kopējo izmaksu pārskati

[!include [banner](../../includes/banner.md)]

## <a name="outstanding-invoices"></a>Neapmaksātie rēķini

Neapmaksāto rēķinu pārskatā ir visu neapmaksāto rēķinu saraksts no dažādiem izmaksu līmeņiem, kas saistīti ar katru reisu. Tas tiek izmantots, lai regulāri saskaņotu reisa un reisa izmaksas kopā ar Virsgrāmatas darbību sarakstu. Pēc tam, kad pieskaitāmās izmaksas ir iekļautas rēķinā, tās tiek izņemtas no pārskata.

Lai ģenerētu neapmaksāto rēķinu pārskatu, veiciet tālāk minētās darbības.

1. Pārejiet uz **Kopējās izmaksas \> Pārskati \> Izsekošana \> Neapmaksātie rēķini**.
1. Dialoglodziņa **Neapmaksātie rēķini** laukā **Uz datumu** norādiet datumu. Jebkurš rēķins, kas neapmaksāts šajā datumā vai pirms tā, tiks iekļauts izvadē.
1. Sadaļā **Parādīt** atlasiet vienu no tālāk aprakstītajām opcijām:

    - **Izmaksas nav iekļautas rēķinā** – iekļaujiet rēķinos iekļautu sūtījumu izmaksas, kurām ir novērtētā izmaksu vērtība, bet ne faktiskās izmaksas.
    - **Krājums nav iekļauts rēķinos** – iekļaujiet izmaksas, kurām ir izrakstīts rēķins, bet kam vēl nav saņemts pirkšanas pasūtījums.
    - **Visi nav iekļauti rēķinos** – ietveriet gan opciju **Izmaksas, kuru izmaksas nav iekļautas rēķinā**, gan opciju **Krājumi nav iekļauti rēķinos**.

1. Iestatiet opciju **Iekļaut jaunās izmaksas** uz *Jā*, lai ietvertu izmaksas, kam vēl nav faktiskas cenas un kuru krājumi vel nav saņemti. Ja iestatāt to uz *Nē*, pārskats ietvers tikai rēķinā iekļautās izmaksas.
1. Sadaļā **Skats** iespējojiet katru detaļas tipu, ko vēlaties iekļaut pārskatā.
1. Tāpat kā cita veida pārskatiem programmā Microsoft Dynamics 365 Supply Chain Management, izmantojiet kopsavilkuma cilni **Mērķis**, lai atlasītu pārskata izvades formātu.
1. Tāpat kā citiem pārskatu veidiem Supply Chain Management, izmantojiet kopsavilkuma cilni **Iekļaut ierakstus**, lai ierobežotu ierakstus, kas tiks iekļauti pārskatā.
1. Atlasiet **Labi**, lai izveidotu pārskatu.

## <a name="activityprovider-analysis-reports"></a>Darbību/nodrošinātāja analīzes pārskats

Aktivitātes/nodrošinātāja analīzes pārskati ļauj pārskatīt katra nodrošinātāja laika novērtējumu precizitāti.

Lai ģenerētu darbību/nodrošinātāja analīzes pārskatu, veiciet tālāk minētās darbības.

1. Atkarībā no pārskata tipa, ko vēlaties izveidot, veiciet vienu no šīm darbībām:

    - Dodieties uz **Kopējās izmaksas \> Pārskati \> Aktivitātes/nodrošinātāja analīze pēc aktivitātes**. Šajā gadījumā laika novērtējumi tiek grupēti pēc aktivitātes.
    - Dodieties uz **Kopējās izmaksas \> Pārskati \> Aktivitātes/nodrošinātāja analīze pēc aktivitātes**. Šajā gadījumā laika novērtējumi tiek grupēti pēc nodrošinātāja.

    Parādās vai nu **Aktivitāšu/nodrošinātāja analīze pēc aktivitātes** dialoglodziņš, vai nu **Aktivitāšu/nodrošinātāja analīze pēc nodrošinātāja** dialoglodziņš. Abi dialoglodziņi nodrošina vienādas opcijas.

1. Tāpat kā cita veida pārskatiem programmā Supply Chain Management, izmantojiet kopsavilkuma cilni **Mērķis**, lai atlasītu pārskata izvades formātu.
1. Tāpat kā citiem pārskatu veidiem Supply Chain Management, izmantojiet kopsavilkuma cilni **Iekļaut ierakstus**, lai ierobežotu ierakstus, kas tiks iekļauti pārskatā.
1. Atlasiet **Labi**, lai izveidotu pārskatu.

## <a name="voyage-costing-reports"></a>Reisa izmaksu aprēķināšanas pārskati

Reisa izmaksu aprēķināšanas pārskati parāda krājumu izmaksas un importa izmaksas pēc folio, pārvadāšanas konteinera vai reisa atkarībā no opcijām, ko atlasāt, kad ģenerējat pārskatu. Katrs reisa izmaksu pārskats ļauj skatīt reisa novērtētās izmaksas attiecībā pret faktiskajām izmaksām, un to var sadalīt pēc vairākiem identificējošajiem faktoriem.

Lai ģenerētu reisa izmaksu pārskatu, veiciet tālāk minētās darbības.

1. Atkarībā no pārskata tipa, ko vēlaties izveidot, veiciet vienu no šīm darbībām:

    - Dodieties uz **Kopējās izmaksas \> Pārskati \> Izmaksas \> Reisa izmaksu aprēķināšana pēc atsevišķām izmaksām**. Šajā gadījumā atsevišķa izmaksu opcija parādīs importa izmaksas uz vienu izmaksu zonas izmaksu tipa kodu.
    - Dodieties uz **Kopējās izmaksas \> Pārskati \> Izmaksas \> Reisa izmaksu aprēķināšana pēc pārskata kategorijas**. Šajā gadījumā importa izmaksas tiks sadalītas dažādās pārskatu kategorijās. Izmaksu tipi tiek grupēti pēc pārskata kategorijām.

    Parādās vai nu **Reisa izmaksu aprēķināšanas pēc atsevišķām izmaksām** dialoglodziņš, vai nu **Reisa izmaksu aprēķināšana pēc pārskata kategorijas** dialoglodziņš. Šie dialoglodziņi ir līdzīgi. Visas atšķirības ir atzīmētas pārējā procedūrā.

1. Ja jūs atvērāt **Reisu izmaksu aprēķināšanu pēc pārskata kategorijas** dialoglodziņu, laukā **Izmaksas** atlasiet vienu no šīm vērtībām:

    - **Izmaksu vērtība** – vērtība tiek aprēķināta, izmantojot automātiskās izmaksas, vai manuāli izveidota izmaksu zonā.
    - **Novērtēts** – pēc preču saņemšanas, tiek iestatītas novērtētās izmaksas.
    - **Faktiskās** – pēc pasūtījuma rēķina izrakstīšanas faktiskās izmaksas tiek iestatītas uz rēķina izmaksām.
    - **Labākais** – Sistēma izmantos vienu no trim iepriekšējām opcijām, kura ir visprecīzākā. (Ieteicams atlasīt šo opciju.)

1. Lai parādītu katra krājuma izmaksas, iestatiet opcijas **Uz krājumu** vērtību uz *Jā*. Iestatiet to kā *Nē*, lai rādītu izmaksas par reisu.
1. Sadaļā **Skatīt** atlasiet kategorijas, ar ko sadalīt izmaksas.
1. Sadaļā **Dimensijas** atlasiet dimensijas, kas jāiekļauj pārskatā.
1. Tāpat kā cita veida pārskatiem programmā Supply Chain Management, izmantojiet kopsavilkuma cilni **Mērķis**, lai atlasītu pārskata izvades formātu.
1. Tāpat kā citiem pārskatu veidiem Supply Chain Management, izmantojiet kopsavilkuma cilni **Iekļaut ierakstus**, lai ierobežotu ierakstus, kas tiks iekļauti pārskatā.
1. Atlasiet **Labi**, lai izveidotu pārskatu.

## <a name="shipping-container-receipts-list"></a>Nosūtīšanas konteinera kvīšu saraksts

Nosūtīšanas konteineru saņemšanas sarakstā ir iekļauti visi nesaglabātie daudzumi, kas jāveic plānotajam datumam vai pirms tā. Noliktavas personāls var izmantot šo pārskatu, lai identificētu paredzamās preces pārvadāšanas konteinerā. To var arī izmantot, lai manuāli validētu preces, kad tās tiek saņemtas nosūtīšanas konteinerā.

Lai ģenerētu nosūtīšanas konteineru saņemšanas sarakstu, sekojiet šiem soļiem.

1. Dodieties uz **Kopējās izmaksas \> Pārskati \> Izsekošana \> Nosūtīšanas konteineru saņemšanas saraksts**.
1. Dialoglodziņa **Nosūtīšanas konteinera saņemšanas sarakstā** laukā **Plānotais datums** norādiet datumu. Jebkurš rēķins, kas neapmaksāts šajā datumā vai pirms tā, tiks iekļauts izvadē.
1. Sadaļā **Dimensijas** atlasiet dimensijas, kas jāiekļauj pārskatā.
1. Tāpat kā cita veida pārskatiem programmā Supply Chain Management, izmantojiet kopsavilkuma cilni **Mērķis**, lai atlasītu pārskata izvades formātu.
1. Tāpat kā citiem pārskatu veidiem Supply Chain Management, izmantojiet kopsavilkuma cilni **Iekļaut ierakstus**, lai ierobežotu ierakstus, kas tiks iekļauti pārskatā.
1. Atlasiet **Labi**, lai izveidotu pārskatu.

## <a name="expected-delivery-report"></a>Paredzamās piegādes pārskats

Gaidāmais piegādes pārskats ietver pamatinformāciju par reisu, nosūtīšanas konteineru, folio, krājumiem un paredzēto piegādes datumu.

Lai ģenerētu paredzamo rēķinu pārskatu, veiciet tālāk minētās darbības.

1. Pārejiet uz **Kopējās izmaksas \> Pārskati \> Izsekošana \> Plānotā piegāde**.
1. Dialoglodziņa **Plānotā piegāde** laukā **Plānotais datums** atlasiet datumu, kad ir gaidāma preču piegāde mērķa noliktavā. Izvadē tiks ietverta neviena reisa rinda, kuras paredzamais datums ir šajā datumā vai pirms tā un kas vēl nav saņemta.
1. Nav obligāti: laukā **Kreditora konts** atlasiet kreditora kontu, lai iekļautu tikai piegādes no konkrēta kreditora.
1. Sadaļā **Dimensijas** atlasiet dimensijas, kas jāiekļauj pārskatā.
1. Tāpat kā cita veida pārskatiem programmā Supply Chain Management, izmantojiet kopsavilkuma cilni **Mērķis**, lai atlasītu pārskata izvades formātu.
1. Tāpat kā citiem pārskatu veidiem Supply Chain Management, izmantojiet kopsavilkuma cilni **Iekļaut ierakstus**, lai ierobežotu ierakstus, kas tiks iekļauti pārskatā.
1. Atlasiet **Labi**, lai izveidotu pārskatu.
