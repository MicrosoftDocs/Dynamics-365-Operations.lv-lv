---
title: Drukāt nodokļu informāciju pārsūtīšanas pasūtījuma dokumentos
description: Šajā tēmā skaidrots, kā pārsūtīšanas pasūtījuma dokumentos var drukāt nodokļu informāciju, ko nosaka nodokļu aprēķināšanas pakalpojums.
author: Kai-Cloud
ms.date: 10/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-10-12
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: d55767ef47e01edd11099f644134cfa48ea70e18
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/23/2021
ms.locfileid: "7675736"
---
# <a name="print-tax-information-on-transfer-order-documents"></a>Drukāt nodokļu informāciju pārsūtīšanas pasūtījuma dokumentos

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Šajā tēmā skaidrots, kā drukāt nodokļu informāciju par pārsūtīšanas pasūtījuma dokumentiem. Varat izdrukāt pārsūtīšanas pasūtījuma pro-forma rēķina dokumentu krājumu pārsūtīšanai, kas tiek uzskatīts par iekšējo piegādi un kopienas iekšējām iegādēm Eiropas Savienības (ES) pievienotās vērtības nodokļa (PVN) noteikumos. 

Pārsūtīšanas pasūtījuma dokumentiem tiek pievienoti šādi ar nodokļiem saistīti dati:

- Krājumu pārsūtīšanas nosaukumi un piegādes un nosūtīšanas adreses
- Piegādātāja un saņēmēja nodokļu identifikācijas numuri
- Piegādāto preču vienības cena un apliekamais daudzums
- Nodokļu kods, nodokļu likme, nodokļu summa un nodokļu direktīvas

Lai konfigurētu šos datus, ir jāveic šādas galvenās darbības.

1. [Iespējojiet un iestatiet nodokļu līdzekli pārsūtīšanas pasūtījumiem](tasks/Tax-feature-support-for-transfer-order.md).
2. [Izveidojiet un iestatiet vairākus juridiskas personas nodokļa reģistrācijas numurus](emea-multiple-vat-registration-numbers.md).
3. Iestatiet neapliekamā nodokļa kodu, aprakstu, nodokļu direktīvas un drukājiet kodu nodokļu kodā. Šajā piemērā ir izveidoti trīs nodokļu kodi un sinhronizēti Microsoft Dynamics 365 Finance: **NL-Neapliekamais**, **BE-RC-21** un **BE-RC+21**.

    1. Programmā Finance dodieties uz **Nodoklis** \> **Uzstādīšana** \> **PVN** \> **PVN reģistrācijas kodi**.
    2. Atlasiet **Labot** un ievadiet **EK** reģistrācijas koda aprakstu. Piemēram, ievadiet **EK bez nodokļiem brīvās kravas ar nodokļa reģistrācijas numuru**.
    3. Dodieties uz **Nodoklis** \> **Netiešie nodokļi** \> **PVN** \> **PVN kodi**.
    4. Atlasiet **BE-RC-21** nodokļa kodu un pēc tam atlasiet **Nodokļu direktīvas**.
    5. Atlasiet **Jauns**.
    6. Laukā **Valoda** atlasiet **EN-US**. Pēc tam laukā **Teksts** ievadiet **Dokumentu ar atbilstošiem noteikumiem preču pārsūtīšana ES PVN direktīvas 2006/112/EK 138. 2. c) panta nozīmē**.
    7. Aizvērt lapu.
    8. Kopsavilkuma cilnes **Vispārīgi** laukā **Drukāt** atlasiet **PVN likmi**.
    8. Atlasiet **NL-Neapliekamā** nodokļa kodu un pēc tam kopsavilkuma cilnes **Vispārīgi** laukā **Drukāt** atlasiet **PVN likmi**.

    > [!NOTE] 
    > Nodokļu kods, nodokļa likme un ar nodokli neapliekamais apraksts netiek drukāts pārsūtīšanas pasūtījuma dokumentos, ja nodokļu kodam netiek saglabāts nodokļu koda kods vai nodokļu direktīvas.

## <a name="print-the-transfer-order---shipment-document"></a>Drukāt pārsūtīšanas pasūtījumu - nosūtīšanas dokuments

Pēc pārsūtīšanas nosūtīšanas sekojiet šiem soļiem, lai izdrukātu pārsūtīšanas pasūtījumu - nosūtīšanas dokumentu.

1. Dodieties uz **Krājumu pārvaldība** \> **Vaicājumi un pārskati** \> **Pārsūtīšanas pasūtījumi** \> **Sūtījums**.
2. Cilnes **Parametri** grupā **Drukāt** iespējojiet **Informāciju par nodokļiem**.
3. Cilnē **Ieraksti, kas jāiekļauj**, atlasiet **Filtrēt**, atlasiet pārsūtīšanas pasūtījuma numuru un pēc tam atlasiet **Labi**.
4. Atlasiet **Labi**, lai drukātu pārsūtīšanas pasūtījumu - nosūtīšanas dokuments.

## <a name="print-the-transfer-order---receipt-document"></a>Drukāt pārsūtīšanas pasūtījumu - saņemšanas dokuments

Pēc pārsūtīšanas saņemšanas sekojiet šiem soļiem, lai izdrukātu pārsūtīšanas pasūtījumu - saņemšanas dokumentu.

1. Dodieties uz **Krājumu pārvaldība** \> **Vaicājumi un pārskati** \> **Pārsūtīšanas pasūtījumi** \> **Saņemt**.
2. Cilnes **Parametri** grupā **Drukāt** iespējojiet **Informāciju par nodokļiem**.
3. Cilnē **Ieraksti, kas jāiekļauj**, atlasiet **Filtrēt**, atlasiet pārsūtīšanas pasūtījuma numuru un pēc tam atlasiet **Labi**.
4. Atlasiet **Labi**, lai drukātu pārsūtīšanas pasūtījumu - saņemšanas dokuments.

## <a name="print-the-transfer-overview-document"></a>Drukāt pārsūtīšanas pārskata dokumentu

Izpildiet šīs darbības, lai drukātu pārsūtīšanas pārskata dokumentu.

> [!NOTE]
> Nodokļu informācija ir pieejama tikai tad, kad pārsūtīšanas pasūtījums ir nosūtīts vai saņemts.

1. Dodieties uz **Krājumu pārvaldība** \> **Vaicājumi un pārskati** \> **Pārsūtīšanas pasūtījumi** \> **Pārsūtīšanas pārskats**.
2. Cilnes **Parametri** grupā **Drukāt** iespējojiet **Informāciju par nodokļiem**.
3. Cilnē **Ieraksti, kas jāiekļauj**, atlasiet **Filtrēt**, atlasiet pārsūtīšanas pasūtījuma numuru un pēc tam atlasiet **Labi**.
4. Atlasiet **Labi**, lai drukātu pārsūtīšanas pārskata dokuments.

[!INCLUDE [footer-include](../../includes/footer-banner.md)]
