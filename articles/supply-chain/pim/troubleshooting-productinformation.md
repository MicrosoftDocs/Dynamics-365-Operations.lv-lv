---
title: Problēmu novēršana saistībā ar preču informāciju
description: Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar preču informāciju.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 87b04998889b86a79fd8dabde422147c5494b003
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516833"
---
# <a name="troubleshoot-product-information"></a>Problēmu novēršana saistībā ar preču informāciju

Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar preču informāciju.

## <a name="i-cant-delete-a-released-product"></a>Nevar izdzēst izlaisto preci.

### <a name="issue-description"></a>Problēmas apraksts

Izlaisto preci un visus tā variantus var dzēst tikai tad, ja izlaistajai precei nav nevienas saistītās darbības.

### <a name="issue-resolution"></a>Problēmas risinājums

Sekojiet šiem soļiem, lai dzēstu izlaisto preci vai preču šablonu.

1. Aizveriet visas atvērtās krājumu darbības.
1. Samaziniet krājumu uz 0 (nulli).
1. Veiciet krājumu slēgšanu.
1. Dzēsiet visus preču šablona preces variantiem, kurus vēlaties dzēst.

## <a name="can-i-change-the-item-number-of-a-released-product"></a>Vai var mainīt izlaistās preces krājuma kodu?

Vairumā gadījumu nevar rediģēt izlaisto preču numurus, jo šīs izmaiņas rezultātā dati kļūs bojāti. Krājuma kodu var rediģēt tikai tad, ja ir jālabo datu bojājums, ko izraisījusi šīs izlaistās preces iepriekšējā pārdēvēšana, kā norādīts [noņemto vai novecojušo funkciju Finance and Operations 10.0.0 ar platformas atjauninājumu 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24) sarakstā.

Ja vēlaties rediģēt izlaisto preču krājumu numurus, [nobalsojiet par šo ideju Ideju portālā](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).

## <a name="the-default-flushing-principle-from-the-product-isnt-being-entered-on-the-bill-of-materials-line"></a>Noklusējuma norakstīšanas princips no preces netiek ievadīts materiālu komplekta rindā.

### <a name="issue-description"></a>Problēmas apraksts

Kad pievienojat krājumu materiālu komplekta (MK) rindai, sistēma neizmanto noklusējuma norakstīšanas principa informāciju, kas ir iestatīta krājumam. Citiem vārdiem, norakstīšanas princips no krājuma netiek parādīts **MK rindas** lapā.

### <a name="issue-resolution"></a>Problēmas risinājums

Ja MK rindā tiek norādīts norakstīšanas princips, tas tiek lietots šai MK rindai. Tomēr, ja norakstīšanas princips ir tukšs vai arī tas nav iestatīts MK rindā, tad krājumam iestatītais norakstīšanas princips joprojām būs spēkā šai MK rindai, pat ja tas nav redzams MK rindā.

Noklusējuma loģika citos Microsoft Dynamics 365 Supply Chain Management līdzekļos parasti nedarbojas šādā veidā. Tomēr pašreizējo darbību nevar mainīt. Pretējā gadījumā var tikt bojāti daži esošie pielāgojumi, kas ir atkarīgi no tā.

## <a name="the-system-lets-me-save-duplicate-bar-codes-for-different-items-or-for-the-same-item-that-has-different-dimensions"></a>Sistēma ļauj man saglabāt dublētus svītrkodus dažādiem krājumiem vai vienam krājumam ar atšķirīgām dimensijām.

Sistēma pašlaik neievieš unikālus svītrkodus, un šī ierobežojuma pievienošana ir pārrāvuma izmaiņas. Patiesībā korporācija Microsoft ir apliecinājusi, ka ar šīm izmaiņām tiks bojātas dažas esošās klientu instalācijas. Tomēr tiks apsvērta plašāka dizaina maiņa, lai nākotnē iespējotu šo funkciju.

## <a name="i-receive-the-following-error-message-when-i-edit-item-record-templates-the-warehouse-location-cannot-be-created-because-the-item-is-not-stocked-to-stock-items-the-stocked-product-option-on-the-associated-item-model-group-must-be-selected"></a>Rediģējot krājumu ierakstu veidnes, tiek parādīts šāds kļūdas ziņojums: "Noliktavas novietojumu nevar izveidot, jo krājums nav uzkrāts. Lai uzkrātu krājumus, ir jāatlasa Uzkrātā produkta opcija, kas atrodas saistītajā krājumu modeļu grupā."

### <a name="issue-description"></a>Problēmas apraksts

Šī problēma rodas, ja ievērojat šos soļus, lai mēģinātu izveidot veidni krājumam, kas nav uzkrāts.

1. Atveriet izlaisto preci, kas nav uzkrāta.
1. Darbību rūts cilnē **Opcijas** atlasiet **Ieraksta informācija**.
1. Dialoglodziņā **Ieraksta informācija** atlasiet **Uzņēmuma kontu veidne**.

Šajā gadījumā, jūs saņemsit sekojošo kļūdas ziņojumu:

> Noliktavas novietojumu nevar izveidot, jo krājums nav uzkrāts. Lai uzkrātu krājumus, ir jāatlasa Uzkrātā produkta opcija, kas atrodas saistītajā krājumu modeļu grupā.

### <a name="issue-resolution"></a>Problēmas risinājums

Preču veidņu izveidošanas procesam ir nepieciešama īpašas preces loģika. Tāpēc šim nolūkam nevar izmantot vispārējo **Uzņēmuma kontu veidnes** pogu. Tā vietā rīkojieties sekojoši.

1. Atveriet izlaisto preci.
1. Darbību rūts grupas **Jauns** cilnē **Prece** atlasiet **Veidne \> Izveidot kopīgotu veidni**.

## <a name="default-help-text-that-is-added-in-product-attributes-isnt-entered-in-a-released-product"></a>Noklusējuma palīdzības teksts, kas tiek pievienots preču atribūtos, netiek ievadīts izlaistajā precē.

Apraksts un palīdzības teksts, kas tiek pievienots preču atribūtos, nav redzams vai ievadīts izlaistajās precēs pēc noklusējuma. Tas tiek darīts ar nolūku.

## <a name="the-default-quantity-that-is-entered-differs-when-its-registered-from-a-bom-and-when-its-registered-from-a-bom-version"></a>Ievadītais noklusētais daudzums atšķiras no tā, vai tas ir reģistrēts no MK, un kad tas ir reģistrēts no MK versijas.

### <a name="issue-description"></a>Problēmas apraksts

Pēc noklusējuma, kad pievienojat krājumu MK, daudzums tiek iestatīts uz 1, nevis daudzums, kas ir definēts laukā **Minimālais pasūtījuma daudzums** lapā **Noklusējuma pasūtījuma iestatījumi** atlasītajai precei. Tomēr, kad jūs pievienojat krājumu no MK versijas un ir atlasīts krājums un variants, pēc noklusējuma ievadītais daudzums ņem vērā minimālo daudzumu, kas tiek iestatīts noklusējuma pasūtījuma iestatījumos noteiktām dimensijām.

### <a name="issue-resolution"></a>Problēmas risinājums

Šāda darbība ir paredzama. Tomēr fakts, ka loģika atšķiras MK un MK versijā, ir zināma problēma. Tomēr šī uzvedība netiks mainīta, jo izmaiņas var ietekmēt daudzus dažādus klientu scenārijus.

## <a name="in-the-released-product-details-i-cant-change-the-attached-images-that-were-uploaded-from-the-product-document-attachments-data-entity"></a>Izlaistajā preces informācijā nevar mainīt pievienotos attēlus, kas tika augšupielādēti no produkta dokumentu pielikumu datu elementa.

### <a name="issue-description"></a>Problēmas apraksts

Šī problēma var rasties, pievienojot attēlu krājumam, izmantojot *Preces dokumentu pielikumu* datu elementu. Šādā gadījumā krājuma attēls tiek uzrādīts krājumam. Tomēr, atlasot **Mainīt attēlu**, nekas netiek norādīts augšupielādēto attēlu sarakstā. Turklāt krājumam netiek parādīti pielikumi.

### <a name="issue-resolution"></a>Problēmas risinājums

*EcoResProductDocumentAttachmentEntity* elements (*Preču dokumentu pielikumi*) importē dokumentu pielikumus *precēm*, bet ne *izlaistām precēm*. (Izlaistās preces sauc arī par *krājumiem*.) Lai apskatītu preces pielikumus, kas atrodas **Izlaistajā preces informācijas** lapā, jāizmanto *EcoResReleasedProductDocumentAttachmentEntity* elements (*Izlaistās preces dokumentu pielikumi*).

## <a name="the-microsoft-flow-connector-shows-the-following-error-message-update-not-allowed-for-field-productnumber"></a>Microsoft Flow savienotājs rāda šādu kļūdas ziņojumu: "Atjaunināšana nav atļauta laukam 'ProductNumber'."

### <a name="issue-description"></a>Problēmas apraksts

Šī problēma rodas, ja mēģināt atjaunināt **Preces numura** lauku, izmantojot *Izlaisto preču* elementu v2 un Microsoft Flow.

### <a name="issue-resolution"></a>Problēmas risinājums

Šāda darbība ir paredzama. Spēja rediģēt izlaistā produkta numuru tika noņemta Dynamics 365 Finance and Operations 10.0.0 ar platformas atjauninājumu 24, lai palīdzētu novērst datu bojājumus. Izņēmumos, kad ir nepieciešams labot datu bojājumus, ko radījusi iepriekšēja izlaistās preces primārā atslēga, lūdzu, varat lūgt Microsoft atbalsta personālu, lai pieprasītu šī ierobežojuma pagaidu noņemšanu.

## <a name="i-cant-create-a-released-product-variant-in-another-legal-entity"></a>Nevar izveidot izlaistu preces variantu citā juridiskā personā.

### <a name="issue-description"></a>Problēmas apraksts

Ja mēģināsit izlaist preces šablonu bez variantiem un pēc tam izveidot variantus katrai juridiskajai personai (uzņēmums), kā tas ir nepieciešams, variantus nevar izlaist, izmantojot variantu ieteikumus. Jūs arī nevarēsit manuāli izveidot variantus.

### <a name="issue-resolution"></a>Problēmas risinājums

Tas tiek darīts ar nolūku. Preces šablona un dimensiju attiecības, kuras šablons var veikt, tiek turētas koplietojamā līmenī. Tāpēc nevar izveidot pieejamās dimensijas koplietojamam preces šablonam konkrētajā juridiskajā personā, kur šīs dimensijas tiek izlaistas, un tad atkārtot procesu katrā juridiska persona, kurai ir nepieciešamas dimensijas. Tā vietā ir jāmaina izlaišanas process, lai pielāgotos izstrādātajam procesam.

Šeit ir process, lai izlaistu preces.

1. Izveidojiet koplietojamu preču šablonu un dimensijas, ko var nodot juridiskajām personām.
1. Izlaist preces juridiskām personām vai nu izmantojot variantu ierosinājumus, vai manuāli pievienojot kombinācijas, kas ir jāatbrīvo.

Varat arī tieši izveidot izlaisto preci.

## <a name="when-i-release-a-variant-in-another-company-i-receive-the-following-error-message-product-variant-with-specified-dimensions-has-already-been-created"></a>Izlaižot variantu citā uzņēmumā, tiek parādīts šāds kļūdas ziņojums: "Preces variants ar norādītajām dimensijām jau ir izveidots."

### <a name="issue-description"></a>Problēmas apraksts

Ja preces variants jau ir izlaists uzņēmumā A, un jūs mēģināt to izlaist uzņēmumā B, izmantojot pogu **Jauns** lapā **Izlaistie preces varianti**, tiks parādīts šāds kļūdas ziņojums:

> Preces variants ar norādītajām dimensijām jau ir izveidots.

### <a name="issue-resolution"></a>Problēmas risinājums

Poga **Jauns** lapā **Izlaistās preces varianti** izveido variantu un izlaiž to uzņēmuma kontekstā. Ja variants jau ir izveidots, nevar izmantot pogu **Jauns**, lai to izlaistu citā uzņēmumā.

Lai labotu problēmu, atveriet lapu **Preču šablons** un atlasiet **Izlaistā prece**, lai izlaistu esošo variantu vēlamajā uzņēmumā.
