---
title: "Darbības darbplūsmas apstiprināšanas procesos"
description: "Šajā rakstā ir paskaidrotas darbības, kuras darbplūsmas apstiprināšanas procesā var veikt katrs dalībnieks."
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56411
ms.assetid: 65fb711c-6474-42d1-81ed-ca657c29bf1f
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 829ee16b8fd72a0808a657419524487d9c1b3123
ms.contentlocale: lv-lv
ms.lasthandoff: 12/18/2018

---

# <a name="actions-in-workflow-approval-processes"></a>Darbības darbplūsmas apstiprināšanas procesos

[!include [banner](../includes/banner.md)]

Šajā rakstā ir paskaidrotas darbības, kuras darbplūsmas apstiprināšanas procesā var veikt katrs dalībnieks.

Darbplūsma var ietvert vairākas cilvēku grupas: iniciatoru, uzdevuma veicējus, lēmumu pieņēmējus un apstiprinātājus. Piemēram, nākamajā izdevumu atskaites darbplūsmā Sems ir iniciators, rindas dalībnieki ir uzdevumu veicēji, Džons ir lēmumu pieņēmējs, bet Frenks, Sjū un Anna ir apstiprinātāji.

[![Darbplūsma\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif)

Nākamajās sadaļās ir skaidrotas darbplūsmas darbības, ko var veikt katra no šīm grupām.

## <a name="actions-that-an-originator-can-perform"></a>Darbības, ko var izpildīt iniciators

Iniciators uzsāk darbplūsmas instanci, iesniedzot dokumentu apstrādei. Piemēram, lai iesniegtu savu izdevumu atskaiti, Semam lapā **Izdevumu atskaite** ir jānoklikšķina uz pogas **Iesniegt**.

## <a name="actions-that-a-task-assignee-can-perform"></a>Darbības, ko var izpildīt uzdevuma veicējs

Uzdevumu var piešķirt vairākām personām vai darba vienumu rindai, ko uzrauga vairākas personas. Taču uzdevumu izpildīt var tikai viena persona. Piemēram, Sems ir iesniedzis izdevumu atskaiti un savas ienākošās plūsmas ir novirzījis pārskatīšanai uz savas organizācijas nodaļu Izdevumu atskaites.

Uzņēmuma Adventure Works nodaļas Izdevumu atskaites darbinieki pārrauga šo rindu. Šīs nodaļas dalībniece Jūlija ir pieņēmusi uzdevumu pārskatīt Sema izdevumu atskaiti un ieejas plūsmas. Tagad viņa var veikt kādu no šādām darbībām: pabeigt, noraidīt, deleģēt, pieprasīt izmaiņas, mainīt piešķiri vai izlaist.

> [!NOTE]
> Pieejamās darbības atšķiras atkarībā no tā, kā programmatūras izstrādātājs šo uzdevumu projektēja.

### <a name="complete"></a>Izpildīt

Ja lietotājs pabeidz uzdevumu, apstrādei iesniegtais dokuments tiek piešķirts nākamajam lietotājam šajā darbplūsmā, ja nākamais lietotājs pastāv. Ja papildu apstrāde nav nepieciešama, darbplūsmas process beidzas.

Piemēram, Adventure Works nodaļas Izdevumu atskaites dalībniece Jūlija ir pieņēmusi uzdevumu pārskatīt Sema izdevumu atskaiti un ieejas plūsmas. Kad Jūlija pabeidz savu pārskatīšanu, dokuments tiek piešķirts Džonam.

### <a name="reject"></a>Noraidīt

Kad lietotājs noraida dokumentu, darbplūsmas process beidzas.

Piemēram, Adventure Works nodaļas Izdevumu atskaites dalībniece Jūlija ir pieņēmusi uzdevumu pārskatīt Sema izdevumu atskaiti un ieejas plūsmas. Ja Jūlija noraida izdevumu atskaiti, darbplūsmas process beidzas.

Pēc tam Sems šo izdevumu atskaiti var iesniegt atkārtoti. Viņš pirms tam var veikt izmaiņas vai atkārtoti iesniegt sākotnējo versiju. Ja Sems izdevumu atskaiti iesniedz atkārtoti, darbplūsmas process sākas ar manuālās pārskatīšanas uzdevumu.

### <a name="delegate"></a>Deleģēt

Kad lietotājs deleģē uzdevumu, šis uzdevums tiek piešķirts citam lietotājam.

Piemēram, Adventure Works nodaļas Izdevumu atskaites dalībniece Jūlija ir pieņēmusi uzdevumu pārskatīt Sema izdevumu atskaiti un ieejas plūsmas. Jūlija šo uzdevumu deleģē savam asistentam Timam.

Pēc tam Tims darbojas Jūlijas vārdā. Tāpēc, kad Tims pabeidz savu pārskatīšanu, izdevumu atskaite tiek piešķirta Džonam, it kā šo uzdevumu būtu pildījusi Jūlija.

### <a name="request-change"></a>Pieprasīt izmaiņas

Kad lietotājs pieprasa iesniegtā dokumenta izmaiņas, dokuments tiek nosūtīts atpakaļ iniciatoram.

Piemēram, Adventure Works nodaļas Izdevumu atskaites dalībniece Jūlija ir pieņēmusi uzdevumu pārskatīt Sema izdevumu atskaiti un ieejas plūsmas. Jūlija izdevumu atskaitē pamana dažas kļūdas un pieprasa izmaiņas. Izdevumu atskaite tiek nosūtīta atpakaļ Semam.

Sems šo izdevumu atskaiti var iesniegt atkārtoti. Viņš pirms tam var veikt pieprasītās izmaiņas vai atkārtoti iesniegt sākotnējo versiju. Ja Sems šo izdevumu atskaiti iesniedz atkārtoti, kādam darba vienumu rindas dalībniekam šī izdevumu atskaite un ieejas plūsmas ir jāpārskata vēlreiz.

### <a name="reassign"></a>Mainīt piešķiri

Darba vienumu rindas dalībnieki šajā rindā esošajiem dokumentiem var mainīt piešķiri uz citu rindu.

Piemēram, uzņēmuma Adventure Works nodaļas Izdevumu atskaites dalībniece Jūlija uzrauga šo rindu. Lai palīdzētu sabalansēt darba slodzi, izdevumu atskaites un tajā iekļauto ieejas plūsmu piešķiri viņa var mainīt uz citu rindu.

### <a name="release"></a>Izlaist

Laiku pa laikam kāds darba vienumu rindas dalībnieks var pieņemt uzdevumu, bet pēc tam izlemt, ka viņš vai viņa šo uzdevumu nevar izpildīt līdz galam. Tādā gadījumā persona, kas pieņēma uzdevumu, šo dokumentu var izlaist atpakaļ uz darba vienumu rindu.

Piemēram, Adventure Works nodaļas Izdevumu atskaites dalībniece Jūlija ir pieņēmusi uzdevumu pārskatīt Sema izdevumu atskaiti un ieejas plūsmas. Ja Jūlija izlemj, ka viņa uzdevumu nevar pabeigt, viņa šo dokumentu var izlaist. Izdevumu atskaite tiek atgriezta rindā, lai citi Adventure Works nodaļas Izdevumu atskaites dalībnieki šo uzdevumu varētu pabeigt.

## <a name="actions-that-a-decision-maker-can-perform"></a>Darbības, ko var izpildīt lēmumu pieņēmējs

Parasti dokuments tiek piešķirts lēmumu pieņēmējam, jo pastāv kāds jautājums, uz kuru lēmumu pieņēmējam ir jāatbild. Atbilde uz šo jautājumu ir parasti ir **Jā** vai **Nē**, vai **Patiess** vai **Aplams**. Ja lēmumu pieņēmējs neatlasa vienu no šiem izvēles variantiem, viņš vai viņa šo lēmumu var deleģēt.

### <a name="choice-1-or-choice-2"></a>\[1. izvēles variants\] vai \[2. izvēles variants\]

Lēmumu pieņēmējam ir jāatbild uz jautājumu, kas ir saistīts ar dokumentu. Atbilde uz šo jautājumu ir parasti ir **Jā** vai **Nē**, vai **Patiess** vai **Aplams**. Lēmumu pieņēmēja izvēlētā atbilde nosaka darbplūsmas zaru, kas tiek izmantots šī dokumenta apstrādāšanai.

Piemēram, Sema izdevumu atskaite tiek piešķirta Džonam. Džonam ir jāizlemj, vai saistībā ar dokumentā ietverto informāciju ir nepieciešams zvanīt Sema vadītājam. Ja Džons izlemj, ka šāds zvans ir nepieciešams, izdevumu atskaite tiek piešķirta Ārijai, kurai pēc tam ir jāzvana Sema vadītājam. Ja Džons izlemj, ka zvans nav nepieciešams, izdevumu atskaite tiek piešķirta Frenkam apstiprināšanai.

### <a name="delegate"></a>Deleģēt

Kad lēmumu pieņēmējs deleģē kādu lēmumu, dokuments tiek piešķirts citam lietotājam, kuram ir jāpieņem lēmums.

Piemēram, Sema izdevumu atskaite tiek piešķirta Džonam. Džons šo lēmumu deleģē savai asistentei Marijai.

Pēc tam Marija darbojas Džona vārdā. Ja Marija izlemj, ka ir nepieciešams zvanīt Sema vadītājam, izdevumu atskaite tiek piešķirta Ārijai, kurai pēc tam ir jāzvana Sema vadītājam. Ja Marija izlemj, ka zvans nav nepieciešams, izdevumu atskaite tiek piešķirta Frenkam apstiprināšanai.

## <a name="actions-that-an-approver-can-perform"></a>Darbības, ko var izpildīt apstiprinātājs

Kad dokuments tiek piešķirts apstiprinātājam, apstiprinātājs var izpildīt vienu no šādām darbībām: apstiprināt, noraidīt, deleģēt vai pieprasīt izmaiņas.

### <a name="approve"></a>Apstiprināt

Kad apstiprinātājs dokumentu apstiprina, šis dokuments tiek piešķirts nākamajam lietotājam darbplūsmā, ja pastāv nākamais lietotājs. Ja papildu apstrāde nav nepieciešama, darbplūsmas process beidzas.

Piemēram, Sems ir iesniedzis izdevumu atskaiti par 6000 USD, un šis dokuments tiek piešķirts Frenkam. Kad Frenks dokumentu apstiprina, tas tiek piešķirts Sjū apstiprināšanai. Kad Sjū apstiprina šo izdevumu atskaiti, darbplūsmas process beidzas.

### <a name="reject"></a>Noraidīt

Kad apstiprinātājs noraida dokumentu, darbplūsmas process beidzas.

Piemēram, Sems ir iesniedzis izdevumu atskaiti par 12 000 USD, un šis dokuments tiek piešķirts Sjū. Ja Sjū noraida šo izdevumu atskaiti, darbplūsmas process beidzas.

Sems šo izdevumu atskaiti var iesniegt atkārtoti. Viņš pirms tam var veikt izmaiņas vai atkārtoti iesniegt izdevumu atskaites sākotnējo versiju. Ja Sems atkārtoti iesniedz šo izdevumu atskaiti, tad darbplūsmas process sākas no apstiprināšanas procesa.

### <a name="delegate"></a>Deleģēt

Kad apstiprinātājs deleģē dokumentu, dokuments tiek piešķirts citam lietotājam apstiprināšanai.

Piemēram, Sems ir iesniedzis izdevumu atskaiti par 12 000 USD, un šis dokuments tiek piešķirts Frenkam. Frenks deleģē izdevumu pārskatu Annai.

Pēc tam Anna darbojas Frenka vārdā. Līdz ar to, kad Anna apstiprina šo dokumentu, tas tiek piešķirts Sjū apstiprināšanai, it kā to būtu apstiprinājis Frenks. Kad Sjū apstiprina šo dokumentu, tas tiek nosūtīts Annai apstiprināšanai.

### <a name="request-change"></a>Pieprasīt izmaiņas

Kad apstiprinātājs pieprasa dokumenta izmaiņas, dokuments tiek nosūtīts atpakaļ iniciatoram.

Piemēram, Sems ir iesniedzis izdevumu atskaiti par 12 000 USD, un šis dokuments tiek piešķirts Sjū. Ja Sjū pieprasa veikt izmaiņas, izdevumu atskaite tiek sūtīta atpakaļ Semam.

Sems šo izdevumu atskaiti var iesniegt atkārtoti. Viņš pirms tam var veikt pieprasītās izmaiņas vai atkārtoti iesniegt izdevumu atskaites sākotnējo versiju. Ja Sems izdevumu atskaiti iesniedz atkārtoti, tas tiek nosūtīts Frenkam apstiprināšanai, jo Frenks ir pirmais apstiprinātājs šajā apstiprināšanas procesā.

