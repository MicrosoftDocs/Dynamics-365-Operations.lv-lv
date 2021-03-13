---
title: ER dokumentu pārvaldības faili, ko izmanto formāta izvades datos (1. daļa. Datu modeļa sagatavošana)
description: Šajā tēmā ir aprakstīts, kā konfigurēt elektronisko pārskatu (ER) formātu dokumentu pārvaldības failu (pielikumu) izmantošanai ER izvadē. (1. daļa)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bff518c60f0f36bdc88245d79bd82f0c4d0599ed
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092645"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1---prepare-data-model"></a>ER dokumentu pārvaldības faili, ko izmanto formāta izvades datos (1. daļa. Datu modeļa sagatavošana)

[!include [banner](../../includes/banner.md)]

Tālāk aprakstītie soļi izskaidro, kā lietotājs, kam piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektroniskā pārskata (ER) formātu, lai izmantotu dokumentu pārvaldības failus (pielikumi) ER izvadē. Šīs darbības var veikt jebkurā uzņēmumā.

Lai izpildītu tālāk norādītās darbības, vispirms izpildiet darbības, kas aprakstītas procedūrā "Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu".

Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Iegūt piekļuvi korporācijas Microsoft nodrošināto konfigurāciju sarakstam
1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.

    Pārliecinieties, vai "Litware, Inc." ir pieejams un atzīmēts kā aktīvs.  

2. Atlasiet Litware, Inc. nodrošinātāju.
3. Noklikšķiniet uz Repozitoriji.

    Ja tipa Operācijas resursi repozitorijs jau pastāv, izlaidiet pašreizējā apakšuzdevuma pārējos soļus.  

4. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
5. Laukā Konfigurācijas repozitorija tips ievadiet Operācijas resursi.
6. Noklikšķiniet uz Izveidot repozitoriju.
7. Noklikšķiniet uz OK.

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a>Saņemiet debitoru rēķinu modeļa konfigurācijas, ko nodrošina korporācija Microsoft
1. Noklikšķiniet uz Rādīt filtrus.
2. Aktivizējiet šādus filtrus: Ievadīt vienuma “Operāciju resursi” filtrēšanas vērtību laukā “Nosaukums”, izmantojot filtra operatoru “sākas ar”; Ievadīt "" filtra vērtību laukā “Apraksts”, izmantojot filtra operatoru “sākas ar”
3. Noklikšķiniet uz Rādīt filtrus.
4. Noklikšķiniet uz Atvērt.
5. Koka struktūrā atlasiet 'Customer invoice model'.

    Atlasiet modeļa konfigurāciju 'Customer invoice model', lai to importētu.  

6. Noklikšķiniet uz Importēt.

    Noklikšķiniet uz Atlasītās konfigurācijas versijas 1 importēšana.  

7. Noklikšķiniet uz Jā.
8. Aizvērt lapu.
9. Aizvērt lapu.
10. Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.
11. Koka struktūrā atlasiet 'Customer invoice model'.

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a>Izveidot atvasināto modeli, lai atbalstītu piekļuvi dokumentu pārvaldības failiem.
Tiks izveidota sava debitoru rēķina modeļa konfigurācija, iegūstot to no korporācijas Microsoft nodrošinātas konfigurācijas. Šī konfigurācija tiks izmantota, lai izveidotu piekļuvi dokumentu pārvaldības failiem un nodrošinātu to pieejamību elektroniskajiem dokumentiem, kas tiks izveidoti, izmantojot šo modeli.  
1. Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.
2. Laukā Jauns ievadiet 'Derive from Name: Customer invoice model, Microsoft.
3. Laukā Nosaukums ierakstiet 'Customer invoice model (custom)'.
4. Klikšķiniet Izveidot konfigurāciju.

