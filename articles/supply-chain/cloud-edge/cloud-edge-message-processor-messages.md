---
title: Ziņojumu apstrādātāja ziņojumi
description: Šajā tēmā ir sniegta informācija par ziņojumu procesora ziņojumu līdzekli mēroga vienības darba noslodzei.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysMessageProcessorMessage, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 68db4c6561f2cc3fcfd64b49da59a4cc164685f2
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069433"
---
# <a name="message-processor-messages"></a>Ziņojumu apstrādātāja ziņojumi

[!include [banner](../includes/banner.md)]

Ziņojumu procesora ziņojumi tiek izmantoti, palaižot mākoņa un malas skalas vienības [ražošanas darba noslodzei](cloud-edge-workload-manufacturing.md) un [noliktavas pārvaldības darba noslodzei](cloud-edge-workload-warehousing.md).

Centrmezgla un mēroga vienības izvietošanas vides apmainās ar lielu datu apjomu, lai saglabātu sinhronizāciju. Daži no apmainītajiem datiem izraisīs papildu loģiku *ziņojumu procesors*. Varat skatīt ziņojumus, kurus ir apstrādājis ziņojumu procesors, dodoties uz **Sistēmas administrēšana > Ziņojumu procesors > Ziņojumu procesora ziņojumi**.

## <a name="message-grid-columns-and-filters"></a>Ziņojumu režģa kolonnas un filtri

Jūs varat izmantot laukus **Ziņojumu procesoru ziņojumu** lapas augšpusē, lai palīdzētu atrast jebkurus jūsu meklētos ziņojumus. Lielākā daļa šo filtru atbilst kolonnu virsrakstiem ziņojumu režģī. Ir pieejami šādi filtri un kolonnu virsraksti:

- **Ziņojuma veids** – norāda ziņojuma veidu.
- **Ziņojumu rinda** – norāda rindas nosaukumu, kurā tiek apstrādāts ziņojums. Ir sniegtas šādas rindas:
  - *Mēroga vienība uz centrmezglu*
  - *Noliktavas izpildes mērogotās vienības centrmezgls*
  - *Ražošanas izpildes mērogotās vienības centrmezgls*
- **Ziņojuma stāvoklis** - norāda ziņojuma stāvokli. Pastāv sekojošie statusi:
  - *Ievietots rindā* – Ziņojumu ir gatavs ziņojuma procesora apstrādei.
  - *Apstrādāts* – Ziņojuma procesors veiksmīgi apstrādāja ziņojumu.
  - *Atcelts* – ziņojums tika apstrādāts, bet apstrāde neizdevās.
- **Zīņojuma saturs** - Šis filtrs veic pilnu teksta meklēšanu ziņojuma saturam. (Ziņojuma saturs režģī netiek rādīts.) Vairumu speciālo simbolu (piemēram, "-") filtrs uzskata par atstarpēm, un visus atstarpju simbolus uzskata par Būla OR operatoriem. Piemēram, tas nozīmē, ka, ja meklējat konkrētu `journalid` vērtību, kas vienāda ar "USMF-123456", sistēma atradīs visus ziņojumus, kuri satur "USMF" vai "123456", kas visdrīzāk būs garš saraksts. Tāpēc labāk būtu ievadīt tikai "123456", jo tādējādi tiks atgriezti precīzāki rezultāti.

## <a name="example-message-type-request-inventory-adjustment-financial-update"></a>Ziņojuma veida piemērs: pieprasīt krājumu korekcijas finanšu atjauninājumu

Piemēram, **Ziņojuma veids** *Pieprasīt krājumu korekcijas finanšu atjauninājumu* tiek izmantots, lai izveidotu un grāmatotu inventarizācijas žurnālu centrmezglā, kad darbinieks izmanto noliktavas programmu, lai [reģistrētu krājumu korekciju](cloud-edge-warehouse-inventory-adjustment.md) mēroga vienības noliktavas pārvaldības darba noslodzei. Tā kā šis konkrētais process rodas no mēroga vienības, lauks **Ziņojumu rinda** rāda vērtību *Mēroga vienība centrmezglam*.

Šim ziņojuma veidam mēroga vienības darba noslodze ieraksta ziņojumu kā daļu no noliktavas programmas krājumu pielāgošanas operācijas. Ziņojuma dati pēc tam tiek pārsūtīti uz centrmezglu kā daļa no tā paša procesa, ko izmanto [Commerce Data Exchange arhitektūrai](../../commerce/commerce-architecture.md). Ziņojums tiks atjaunināts, lai parādītu **Ziņojuma stāvokli** kā *Ievietots rindā*. Ziņojumu procesors tad mēģina apstrādāt ziņojumu un atjaunina **Ziņojuma stāvokli** uz *Apstrādāts* veiksmīgi, vai *Atcelts* kļūmes gadījumā.

## <a name="view-the-message-log-message-content-and-details"></a>Apskatīt ziņojumu žurnālu, ziņojuma saturu un detalizētu informāciju

Detalizētu informāciju par ziņojumu var atrast, atlasot to režģī un pēc tam atverot cilnes **Žurnāls** vai **Ziņojuma saturs** ziņojumu režģī, kur tiek rādīts katrs apstrādes notikums.

Cilne **Ziņojuma saturs** ir atkarīga no **Ziņojuma veida**, un tādēļ tā teksta garums būs atšķirīgs. Tipisks ziņojuma satura teksts tiks sākts ar **{** un beigties ar **}** un starp tiem ir tādi lauku nosaukumi kā `journalId` kam seko **:** un vērtība, piemēram, *USMF-123456*.

Rīkjosla cilnē **Žurnāls** ietver šādas pogas:

- **Žurnāls** – parāda apstrādes rezultātus. Tas ir īpaši noderīgi, lai saprastu iemeslus apstrādes kļūmei ziņojumiem, kuru **Apstrādes rezultāts** ir *Neizdevās*.
- **Komplekts** – vairākas ziņojumu apstrādes operācijas var tikt izpildītas kā daļa no vienas un tās pašas pakešapstrādes. Izvēlieties šo pogu, lai aplūkotu šos detalizētos datus. Piemēram, varat redzēt, vai eksistē atkarības, kurām nepieciešams, lai sistēma apstrādātu noteiktus ziņojumus noteiktā secībā.

## <a name="message-processor-batch-job"></a>Ziņojumu procesora pakešuzdevums

Palaižot izdalīto hibrīdu topoloģiju ar mēroja vienībām, pakešuzdevums *Ziņojuma apstrāde* tiks automātiski izsaukts, kad apstrādei tiek izveidots jauns ziņojums, tāpēc jums nevajadzēs šo darbu plānot manuāli.

Ja nepieciešams, varat piekļūt pakešuzdevumam, noklikšķinot uz **Sistēmas administrēšana > Ziņojumu procesors > Ziņojumu procesors**.

## <a name="manually-process-or-cancel-a-message"></a>Manuāli apstrādāt vai atcelt ziņojumu

Ja nepieciešams, varat manuāli apstrādāt vai atcelt ziņojumu atkarībā no tā pašreizējā stāvokļa. Lai to izdarītu, atlasiet ziņojumu režģī un pēc tam atlasiet **Apstrādāt** vai **Atcelt** darbību rūtī

## <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a>Iestatīt biznesa notikumus, lai piegādātu brīdinājumus par nesekmīgiem apstrādes rezultātiem

Papildus filtrēšanai **Ziņojuma stāvokļa** vērtībā *Atcelts*, lai pieprasītu neizdevušos ziņojumus, varat iestatīt [biznesa notikumus](../../fin-ops-core/dev-itpro/business-events/home-page.md) centrmazglā, lai brīdinātu jūs par neizdevušos apstrādes rezultātiem. Lai to izdarītu, aktivizējiet biznesa notikumu ar nosaukumu *Ziņojumu procesora ziņojums apstrādāts*  lapā **Biznesa notikumu katalogs** (**Sistēmas administrēšana > Iestatīšana > Biznesa notikumi > Biznesa notikumu katalogs**).

Kā aktivizēšanas procesa daļa jums tiks sniegta informācija, kas norāda, vai notikums ir specifisks vienai vai visām juridiskajām personām, un jānorāda **Galapunkta nosaukums**, kas jādefinē vispirms.

>[!NOTE]
> Ja **Kad rodas biznesa notikums** ir iestatīts uz *Microsoft Power Automate* (nevis *HTTPS*, piemēram), **Galapunkta nosaukums** tiks automātiski izveidots Supply Chain Management, pamatojoties uz *Microsoft Power Automate* iestatījumu.

### <a name="microsoft-power-automate-example"></a>Microsoft Power Automate piemērs

Šajā piemērā izmantojiet **Kad rodas biznesa notikums** ar *Microsoft Power Automate* nosūta e-pasta ziņojumus, kuros ir InfoLog ziņojumi un hipersaites, lai atvērtu lapu **Ziņojumu procesora ziņojumi** noteiktam neizdevušās ziņojumam centrmezgla izvietošanā. Ja nepieciešams, varat pievienot papildu loģiku, lai paziņojumus nosūtītu paralēli, izmantojot dažādus kanālus, un kontrolētu saņēmējus, balstoties uz notikuma datiem.

1. Sistēmā [Power Automate](https://preview.flow.microsoft.com) izveidojiet jaunu automatizētu mākoņa plūsmu plūsmas trigerim **Kad rodas biznesa notikums - Fin & Ops (Dynamics 365)**, kam seko **Parse JSON** un **Sūtīt e-pasta ziņojumu** darbības, kā parādīts šajā ilustrācijā.

    :::image type="content" source="./media/cloud-edge-power-automate-example1.png" alt-text="Power Automate automatizētā mākoņa plūsma.":::

1. Darbības **Kad rodas biznesa notikums** laikā ir iespējams atrast vai ievadīt centrmezglu **Instance** kas seko **Kategorija** un pēc tam **Biznesa notikums** *Ziņojumu procesora ziņojums apstrādāts* kā parādīts šajā ilustrācijā.

    :::image type="content" source="./media/cloud-edge-power-automate-example2.png" alt-text="Power Automate darbība Kad notiek biznesa notikums.":::

1. Darbībai **Parse JSON** ievadiet **Shēmu**, kas definē paplašinātos laukus. Varat izmantot opciju *Lejupielādes shēma* lapā **Biznesa notikumu katalogs** Supply Chain Management vai arī sāciet, ielīmējot parauga shēmas tekstu. Šis piemēra teksts ir parādīts pēc šī ilustrācijas.

    :::image type="content" source="./media/cloud-edge-power-automate-example3.png" alt-text="Power Automate Parsēt JSON darbību.":::

    ```json
    {
        "properties": {
            "BusinessEventId": {
                "type": "string"
            },
            "ControlNumber": {
                "type": "integer"
            },
            "EventId": {
                "type": "string"
            },
            "EventTime": {
                "type": "string"
            },
            "MajorVersion": {
                "type": "integer"
            },
            "MessageContent": {
                "type": "string"
            },
            "MessageDestinationCompanyId": {
                "type": "string"
            },
            "MessageDestinationOperationalSiteId": {
                "type": "string"
            },
            "MessageDestinationWarehouseId": {
                "type": "string"
            },
            "MessageDestinationWorkloadName": {
                "type": "string"
            },
            "MessageInfolog": {
                "type": "string"
            },
            "MessageProcessingResult": {
                "type": "string"
            },
            "MessageProcessingResultLabel": {
                "type": "string"
            },
            "MessageProcessorMessagePageUrl": {
                "type": "string"
            },
            "MessageQueue": {
                "type": "string"
            },
            "MessageQueueLabel": {
                "type": "string"
            },
            "MessageSourceCompanyId": {
                "type": "string"
            },
            "MessageSourceOperationalSiteId": {
                "type": "string"
            },
            "MessageSourceWarehouseId": {
                "type": "string"
            },
            "MessageSourceWorkloadName": {
                "type": "string"
            },
            "MessageState": {
                "type": "string"
            },
            "MessageStateLabel": {
                "type": "string"
            },
            "MessageType": {
                "type": "string"
            },
            "MessageTypeLabel": {
                "type": "string"
            },
            "MinorVersion": {
                "type": "integer"
            }
        },
        "type": "object"
    }
    ```

1. Darbībā **Sūtīt e-pasta zīņojumu** varat atlasīt atsevišķus laukus vai sākt, ielīmējot e-pasta pamatteksta piemēru laukā **Pamatteksts**. Šis piemērs ir parādīts pēc šī ilustrācijas.

    :::image type="content" source="./media/cloud-edge-power-automate-example4.png" alt-text="Power Automate darbība Sūtīt e-pasta ziņojumu.":::

    ```plaintext
    Message queue: @{body('Parse_JSON')?['MessageQueue']}
    Message queue label: @{body('Parse_JSON')?['MessageQueueLabel']}
    Message type: @{body('Parse_JSON')?['MessageQueueType']}
    Message type label: @{body('Parse_JSON')?['MessageQueueTypeLabel']}
    Message content: @{body('Parse_JSON')?['MessageContent']}
    Message state: @{body('Parse_JSON')?['MessageState']}
    Message state label: @{body('Parse_JSON')?['MessageStateLabel']}
    Message processing result: @{body('Parse_JSON')?['MessageProcessingResult']}
    Message processing result label: @{body('Parse_JSON')?['MessageProcessingResultLabel']}
    Message infolog: @{body('Parse_JSON')?['MessageInfolog']}
    Message source company ID: @{body('Parse_JSON')?['MessageSourceCompanyId']}
    Message source workload name: @{body('Parse_JSON')?['MessageSourceWorkloadName']}
    Message source site ID: @{body('Parse_JSON')?['MessageSourceOperationalSiteId']}
    Message source warehouse ID: @{body('Parse_JSON')?['MessageSourceWarehouseId']}
    Message destination company ID: @{body('Parse_JSON')?['MessageDestinationCompanyId']}
    Message destination workload name: @{body('Parse_JSON')?['MessageDestinationWorkloadName']}
    Message destination site ID: @{body('Parse_JSON')?['MessageDestinationOperationalSiteId']}
    Message destination warehouse ID: @{body('Parse_JSON')?['MessageDestinationWarehouseId']}
    Message processor message page URL: @{body('Parse_JSON')?['MessageProcessorMessagePageUrl']}
    ```

1. Saglabājot biznesa notikumu, tas tiks automātiski aktivizēts un gatavs lietošanai kā Supply Chain Management daļa.
