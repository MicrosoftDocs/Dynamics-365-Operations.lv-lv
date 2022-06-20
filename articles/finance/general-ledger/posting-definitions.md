---
title: Grāmatošanas definīcijas
description: Šajā rakstā ir sniegta informācija par grāmatošanas definīcijām un veidu, kā tās definēt un saistīt. Lai uzskaites ierakstos klasificētu galvenos kontus un finanšu dimensijas, atbalstītajiem grāmatošanas veidiem un dokumentiem var izmantot grāmatošanas definīcijas nevis grāmatošanas metodes.
author: kweekley
ms.date: 09/03/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans, LedgerParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 15741
ms.assetid: 1495e7e0-2e39-464c-8da9-f55b1ca1c6bb
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f60506e039623ae7a97f6b4e835f751da15ac0c1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898154"
---
# <a name="posting-definitions"></a>Grāmatošanas definīcijas

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija par grāmatošanas definīcijām un veidu, kā tās definēt un saistīt.
Lai uzskaites ierakstos klasificētu galvenos kontus un finanšu dimensijas, atbalstītajiem grāmatošanas veidiem un dokumentiem var izmantot grāmatošanas definīcijas nevis grāmatošanas metodes. Atbalstītos dokumentus un grāmatošanas veidus varat skatīt lapā **Transakcijas grāmatošanas definīcijas**. 

Lai sāktu lietot grāmatošanas definīcijas, atlasiet opciju **Izmantot grāmatošanas definīcijas** lapā **Virsgrāmatas parametri**. Pat ja izmantojat grāmatošanas definīcijas, vienalga ir jādefinē sākotnējo ierakstu grāmatošanas metodes un neatbalstītie grāmatošanas veidi un dokumenti. 

Lai pirkšanas pasūtījumiem iespējotu apgrūtinājumu uzskaiti un pirkšanas pieprasījumiem iespējotu apgrūtinājumu bez juridiskām saistībām uzskaiti, izmantotjiet grāmatošanas definīcijas.

## <a name="defining-posting-definitions"></a>Grāmatošanas definīciju definēšana
Izmantojiet lapu **Grāmatošanas definīcijas**, lai norādītu atbilstības kritērijus un definētu ierakstus, kas ir jāģenerē rodoties atbilstībai. Atbilstības kritēriji tiek novērtēti sākotnējiem ierakstiem kā uzskaites sadalēm. 

Lapā **Grāmatošanas definīcijas** var arī piešķirt prioritātes numurus ierakstu rindām, lai kontrolētu secību, kādā rindas tiek novērtētas. Rindas, kurām ir zemāks prioritātes numurs, tiek novērtētas vispirms. Piemēram, tiek novērtētas visas rindas, kam ir prioritātes numurs 1, pēc tam rindas, kam ir prioritātes numurs 2, un tā tālāk. Ja konstatēta atbilstība, citi atbilstības kritēriji tiek ignorēti. Turklāt, tikai sākotnējai transakcijai atbilstošās grupas kritēriji rada ģenerētos ierakstus. 

Varat pārbaudīt grāmatošanas definīcijas, izmantojot vedni **Grāmatošanas definīcijas pārbaude**. Kad ir definēts grāmatošanas definīcijas parauga sākotnējais ieraksts, redzēsit ģenerētos ierakstus. 

Varat izmantot grāmatošanas definīcijas versijas kopā ar spēkā stāšanās datumiem. Piemēram, varat izveidot nākamo grāmatošanas definīcijas versiju, lai jaunajā finanšu gadā grāmatotu citā virsgrāmatas kontā. 

Izmantojiet lapu **Transakcijas grāmatošanas definīcijas**, lai grāmatošanas definīcijas piešķirtu darbību veidiem.

## <a name="linking-posting-definitions"></a>Grāmatošanas definīciju piesaiste
Piesaisti var veikt no vienas grāmatošanas definīcijas citā, veidojot grāmatošanas definīcijas. Pēc tam piesaistītās definīcijas kritēriji tiek ņemti vērā papildus pašreizējās grāmatošanas definīcijas kritērijiem. Šis līdzeklis palīdz ietaupīt laiku, jo pašreizējai grāmatošanas definīcijai kritēriji nav atkārtoti jāievada kopsavilkuma cilnē **Ieraksti** lapā **Grāmatošanas definīcijas**, ja šīs rindas jau ievadījāt citā definīcijā. 

Diagrammās vai tabulās ietveriet visas saites, ko jūs varētu izmantot. Lai izvairītos no konfliktiem ar pašreizējo grāmatošanas definīciju, pārliecinieties, vai visās grāmatošanas definīcijās, kam veicat piesaisti, rindas ir unikālas. 

Veidojot saites grāmatošanas definīcijās, tiek lietoti šādi ierobežojumi:

-   norādītajā grāmatošanas definīcijā var būt ietverta saite uz citu grāmatošanas definīciju vai uz to var būt izveidota saite citā grāmatošanas definīcijā, bet vienlaicīgi ne abas saites. Tomēr grāmatošanas definīcijā var ietvert saiti uz vairākām grāmatošanas definīcijām;
-   varat iestatīt saites tikai starp tām grāmatošanas definīcijām, kas atrodas vienā modulī;
-   grāmatošanas definīciju var piešķirt jebkuram transakcijas veidam, bet šim transakcijas veidam jābūt tajā pašā modulī, kur ir grāmatošanas definīcija. Izmantojiet lapu **Darījuma grāmatošanas definīcijas**, lai redzētu, kurā modulī ir transakcijas veids.


Papildinformāciju skatiet tēmā [Grāmatošanas definīcijas piemēri](example-posting-definitions.md). 




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
