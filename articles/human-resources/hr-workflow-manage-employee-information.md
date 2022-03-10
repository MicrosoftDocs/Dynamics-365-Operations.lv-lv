---
title: Darbplūsmu izmantošana, lai pārvaldītu informāciju par darbiniekiem
description: Šajā tēmā ir paskaidrots, kā var izmantot darbplūsmas, lai pārvaldītu informāciju par darbiniekiem.
author: twheeloc
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d80ed49a4f423179997ac35562284a4e28af803f
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068089"
---
# <a name="use-workflows-to-manage-employee-information"></a>Darbplūsmu izmantošana, lai pārvaldītu informāciju par darbiniekiem


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā tēmā ir aprakstīts, kā varat izmanto personāla vadības darbplūsmu iespējas, lai pārvaldītu darbinieku informāciju. Piemēram, varat saistīt darbplūsmu ar pozīciju un konfigurēt apstiprināšanas darbplūsmu, kas tiek sākta, kad darbinieki maina savu ierakstu.

Personāla vadības darbplūsmu iespējas nodrošina vairākas darbplūsmas personāla vadības darbību pārvaldībai. Turklāt ir pieejamas vairākas opcijas, kas sniedz iespēju modificēt noteiktas darbplūsmas un saistīt tās ar padotības hierarhiju. Darbplūsmas ir pieejamas, lai palīdzētu pārvaldīt izmaiņas vairāku tipu darbinieku informācijā. Varat saistīt darbplūsmu ar pozīciju. Šādā gadījumā, ja darbinieki maina savu darbinieka ierakstu, tiek sākta darbplūsma, kas pieprasa apstiprināšanu pirms jaunās informācijas saglabāšanas. Darbplūsmas ir iepriekš definētas šāda veida informācijai, lai palīdzētu efektīvi pārvaldīt izmaiņas un uzturēt darbinieku datus precīzus:

-   Identifikācijas numuri
-   Kursi
-   Izglītība
-   Attēls
-   Patapinātie krājumi
-   Profesionālā pieredze
-   Projektu pieredze
-   Prasmes
-   Atbildīgie amati
-   Personāla vadības darbības
-   Kursu reģistrācija

Kad darbinieki tiek pieņemti darbā, pārcelti citā amatā vai ar viņiem tiek pārtrauktas darba attiecības, darbplūsma var tikt ietverts pārskatīšanas process. Tādā veidā dokumentu var pārskatīt vai darbības nosacījumus var definēt kā daļu no darbplūsmas. Kad pārskatīšanas process ir pabeigts, dokuments vai darbība tiek pabeigta un darbplūsma pāriet pie galīgās apstiprināšanas darbības.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Darbplūsmas saistīšana ar padotības hierarhiju
Varat saistīt darbplūsmu ar jebkuru konfigurēto hierarhiju. Piemēram, ja pozīcija ir saistīta ar matricas padotības hierarhiju, varat konfigurēt darbplūsmu, kas nodrošina noteikta projekta izmaksu novirzīšanu projekta vadītajam, nevis tā darbinieka vadītājam, kurš ir saistīts ar šo pozīciju. Lai izveidotu jaunu darbplūsmu vai modificētu esošu darbplūsmu, **lapā Personāla vadības darbplūsma** atlasiet **Jauns**. Sarakstā atlasiet darbplūsmu, lai atvērtu darbplūsmas noformētāju. Varat izmantot noformētāju, lai izveidotu jaunu darbplūsmu vai mainītu esošas darbplūsmas darbības. Ja maināt esošu darbplūsmu, izmaiņas tiek saglabātas kā jauna versija. Tāpēc vienmēr varat atgriezieties pie iepriekšējās versijas, ja tas ir nepieciešams.

## <a name="configure-a-human-resources-workflow"></a>Personāla vadības darbības konfigurēšana
Lai konfigurētu pamata darbplūsmu, kas tiek sākta, kad darbinieks pieprasa savas personiskās informācijas izmaiņas, veiciet tālāk norādītās darbības.

1.  **Lapā Personāla vadības darbplūsmas** atlasiet **Jauns**.
2.  Pieejamo darbplūsmu sarakstā atlasiet vienumu **Identifikācijas numuri**.
3.  Atlasiet **Palaist**, lai atvērtu darbplūsmas noformētāju, un pēc tam ievadiet savu lietotājvārdu un paroli, kad tiek prasīts.
4.  Velciet elementu **Apstiprināt identifikācijas numuru** no darbplūsmas elementu saraksta uz noformētāja rāmi.
5.  Savienojiet apstiprināšanas elementu ar elementiem **Sākt** un **Pabeigt**.
6.  Veiciet dubultskārienu (vai dubultklikšķi) **Apstiprināt elementu**, atlasiet un turiet (vai noklikšķiniet ar peles labo pogu) un pēc tam atlasiet **Rekvizīti**.
7.  Veiciet tālāk norādītās darbības, lai pievienotu darbplūsmas elementa instrukcijas.

    1.  Atlasiet vienumu **Piešķire** un pēc tam piešķires veida sadaļā atlasiet vienumu **Hierarhija**.
    2.  Sadaļā **Hierarhija** atlasiet vienumu **Konfigurējama hierarhija**.
    3.  Pievienojiet apturēšanas nosacījumu un aizveriet lapu.

8.  Izpildiet visas papildu instrukcijas (nedrīkst būt neviens papildu brīdinājums).
9.  Atlasiet **Saglabāt un aizvērt**. Kad tiek atvērts dialoglodziņš, aktivizējiet jauno darbplūsmu un atlasiet vienumu **Padarīt aktīvu**.
10. Pārejiet uz sadaļu **Personāla vadība** &gt; **Pozīcijas** &gt; **Pozīciju hierarhijas tipi**.
11. Atlasiet vienumu **Matrica**.
12. Pievienojiet sarakstam darbplūsmu **Nodarbinātā identifikācijas numurs**.

## <a name="additional-resources"></a>Papildu resursi

[Skatīt un pārvaldīt adreses izmaiņas](hr-personnel-view-address-changes.md) 





[!INCLUDE[footer-include](../includes/footer-banner.md)]
