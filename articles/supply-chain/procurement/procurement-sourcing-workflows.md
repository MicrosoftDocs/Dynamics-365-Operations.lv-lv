---
title: Sagādes un avotu darbplūsmas
description: Dažas organizācijas pieprasa, lai pirkšanas pieprasījumus un pirkšanas pasūtījumus apstiprinātu cits lietotājs nekā persona, kura ievadīja darījumu. Lai iestatītu apstiprināšanas procesu, varat izveidot darbplūsmu.
author: kamaybac
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd9ee69e180f2ff605c4f373a95d2346ccc73c0e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807948"
---
# <a name="procurement-and-sourcing-workflows"></a>Sagādes un avotu darbplūsmas

[!include [banner](../includes/banner.md)]

Dažas organizācijas pieprasa, lai pirkšanas pieprasījumus un pirkšanas pasūtījumus apstiprinātu cits lietotājs nekā persona, kura ievadīja darījumu. Lai iestatītu apstiprināšanas procesu, varat izveidot darbplūsmu.

Darbplūsma attēlo biznesa procesu. Izmantojot darbplūsmu, tiek noteikta dokumenta plūsma caur sistēmu un norādīts, kuram ir jāpabeidz uzdevums vai jāapstiprina dokuments. Darbplūsmas sistēmas lietošanai organizācijā ir vairākas priekšrocības.

- **Saskaņoti procesi** — varat definēt noteiktu dokumentiem, piemēram, pirkšanas pieprasījumu un izdevumu pārskatu, apstiprināšanas procesu. Izmantojot darbplūsmas sistēmu, varat nodrošināt saskaņotu un efektīvu dokumentu apstrādes un apstiprināšanas procesu.
- **Procesa pārskatāmība** — varat sekot līdzi noteiktas darbplūsmas instances statusa, vēsturiskajiem un veiktspējas rādītājiem. Tādējādi varat noteikt, vai ir jāveic darbplūsmas izmaiņas, lai uzlabotu efektivitāti.
- **Centralizēts darbu saraksts** — lietotāji var skatīt centralizētu darbu sarakstu, lai skatītu darbplūsmas uzdevumus un apstiprinājumus, kas viņiem ir piešķirti visās darbplūsmās, kurās viņi piedalās. Šī funkcija ir pieejama lapā Darba vienumi.

## <a name="the-types-of-workflows-that-you-can-create"></a>Izveidojamo darbplūsmu veidi

Sagādei un avotiem ir pieejami šādi darbplūsmu veidi.

| tips | Šī tipa lietošanas nolūks |
|---|---|
| Pirkšanas pieprasījuma pārskats | Izveidot pārskatīšanas un apstiprināšanas darbplūsmas pirkšanas pieprasījumiem. |
| Pirkšanas pieprasījuma rindas pārskats | Izveidot pārskatīšanas un apstiprināšanas darbplūsmas pirkšanas pieprasījumu rindām. |
| Pirkšanas pasūtījuma darbplūsma | Izveidojiet pārskatīšanas un apstiprināšanas darbplūsmas pirkšanas pasūtījumiem. |
| Pirkšanas pasūtījuma rindas darbplūsma | Izveidojiet pārskatīšanas un apstiprināšanas darbplūsmas pirkšanas rindas pasūtījumiem. |
| Kreditoru pievienošanas pieteikumu darbplūsma | Izveidot pārskatīšanas un apstiprināšanas darbplūsmas jaunu piegādātāju pievienošanai, izmantojot piegādātāju pieprasījumus. |

> [!IMPORTANT]
> Kad jūs pievienojat jaunu darbplūsmu, jūs varētu redzēt arī šādas novecojušas darbplūsmas, kas uzskaitītas dialoglodziņā **Izveidot darbplūsmu**. Tie ir saistīti ar *kvīts apstiprinājuma* funkcionalitāti, kas bija pieejams [Dynamics AX 2012](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows), bet tagad ir novecojis. Šīs darbplūsmas pašlaik netiek atbalstītas.
> 
> - Piegādes izpildes datuma paziņojuma darbplūsma
> - Rēķina saņemšanas paziņojuma darbplūsma
> - Produktu ieejas plūsma neizdevās paziņojumu darbplūsmai.
> - Neapstiprinātu produktu ieejas plūsmas noraidīšanas paziņojuma darbplūsma

## <a name="creating-a-workflow"></a>Darbplūsmas izveide

Lai izveidotu darbplūsmu, pārejiet uz sadaļu Sagāde un avoti &gt; Iestatījumi &gt; Sagādes un avotu darbplūsmas un izveidojiet jaunu darbplūsmu, atlasot izveidojamās darbplūsmas veidu. 

Darbplūsmas audeklā varat vilkt darbplūsmas elementus uz veidotāju un saistīt elementus plūsmā. Darbplūsmas elementi ir jākonfigurē. Apstiprinājumam un uzdevuma darbplūsmas elementiem var konfigurēt to, kuram dalībniekam jāveic darbība.

## <a name="types-of-participants"></a>Dalībnieku tipi

Apstiprināšanas darbību varat piešķirt šādām dalībnieku grupām.

| Lietotāju grupa | Apraksts |
|---|---|
| Dalībnieks | Piešķiriet apstiprināšanas darbību kādas grupas vai lomas dalībniekiem. |
| Hierarhija | Piešķiriet apstiprināšanas darbību lietotājiem noteiktā organizācijas hierarhijā. |
| Darbplūsmas lietotājs | Piešķiriet apstiprināšanas darbību šīs darbplūsmas lietotājiem. |
| Rinda | Piešķiriet apstiprinājuma darbību darba vienumu rindai. |
| Lietotājs | Piešķiriet apstiprināšanas darbību konkrētiem lietotājiem. |

## <a name="additional-resources"></a>Papildu resursi

- [Biznesa procesu darbplūsmu definēšana pirkšanas pieprasījumiem](https://www.microsoft.com/download/details.aspx?id=101821)
- [Pirkšanas pieprasījuma darbplūsma](purchase-requisitions-workflow.md)
- [Kreditoru pievienošana](vendor-onboarding.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]