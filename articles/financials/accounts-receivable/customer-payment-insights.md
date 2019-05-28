---
title: Debitoru maksājumu ieskati (priekšskatījums)
description: Šajā tēmā ir aprakstīts, kā līdzeklis Debitoru maksājumu ieskati var palīdzēt prognozēt, kad rēķins tiks apmaksāts, un kā tas palīdz organizācijām izveidot optimizācijas stratēģijas, kas palielina savlaicīgas apmaksas iespējamību.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-04-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 9e722db6302d7ef51c01601cde245d4f4a333eba
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566255"
---
# <a name="customer-payment-insights-preview"></a>Debitoru maksājumu ieskati (priekšskatījums)

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> Šis līdzeklis ir ietverts noteiktas mērķauditorijas laidienā un ir pieejams tikai tiem lietotājiem, kuri ir izvēlējušies privāto priekšskatījumu. Šis līdzeklis tiks ietverts turpmākā vispārējās pieejamības laidienā.

# <a name="overview"></a>Pārskats

Organizācijām bieži ir grūti noteikt, kad debitors apmaksās rēķinus. Šīs informācijas trūkuma dēļ var tikt izveidotas neprecīzas naudas plūsmas prognozes, neefektīvi iekasēšanas procesi, kā arī pasūtījumi var tikt izdoti debitoriem, kuri var radīt kredītrisku. Līdzeklis Debitoru maksājumu ieskati (priekšskatījums) rēķina apmaksas prognozei izmanto mašīnmācīšanos. Šis līdzeklis nodrošina arī optimizācijas stratēģijas, kuras var pielāgot tā, lai maksimāli palielinātu iespēju, ka debitori rēķinus apmaksās savlaicīgi.

## <a name="predictions"></a>Prognozes

Maksājumu prognozes ļauj organizācijām uzlabot biznesa procesus, sniedzot iespēju:

-   viegli identificēt rēķinus, kam tiek prognozēta kavēta apmaksa;
-   veikt atbilstošus pasākumus, kas palielina iespēju savlaicīgi saņemt samaksu.

Līdzeklis Debitoru maksājumu ieskati (priekšskatījums) rēķina apmaksas prognozei izmanto mašīnmācīšanos. Šis līdzeklis izmanto vēsturiskos rēķinu, maksājumu un debitoru datus, lai izveidotu mašīnmācīšanās modeli un izmantotu to rēķinu apmaksas prognozēm.

Katram neapmaksātajam rēķinam līdzeklis Debitoru maksājumu ieskati (priekšskatījums) prognozē trīs maksājumu iespējamības:

-  savlaicīgas maksājuma izpildes iespējamība (nepārsniedzot rēķina apmaksas termiņu);
-  iespējamība, ka maksājums tiks veikts 30 dienu laikā pēc rēķina apmaksas termiņa;
-  iespējamība, ka maksājums tiks veikts vēlāk nekā 30 dienu laikā pēc rēķina apmaksas termiņa.

Maksājumu iespējamību var redzēt prognožu sadaļā.

[![Maksājumu prognozes](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)

Katram rēķinam tiek piešķirta arī ticamākā maksājuma iespējamība, izmantojot kādu no trīs iepriekš definētajām prognozētajām maksājuma iespējamībām. Scenārijs ar lielāko maksājuma iespējamību ir ticamākais scenārijs.


Pieņemsim, ka rēķinam ir prognoze ar 71 procenta iespējamību savlaicīgai rēķina apmaksai, 13 procentu iespējamība rēķina apmaksai 30 dienu laikā pēc apmaksas termiņa un 16 procentu iespējamība rēķina apmaksai vēlāk nekā 30 dienu laikā pēc apmaksas termiņa. Saskaņā ar lielāko iespējamību rēķinam ir savlaicīgas apmaksas scenārijs, tādēļ rēķinam tiks atzīmēta savlaicīgas apmaksas iespējamība.

[![Maksājumu prognozes](./media/payment-predict.png)](./media/payment-predict.png)

## <a name="optimization-strategies"></a>Optimizācijas stratēģijas

Papildus maksājumu prognozēm līdzeklis Debitoru maksājumu ieskati (priekšskatījums) savlaicīgas apmaksas iespēju palielināšanai var izmantot optimizācijas stratēģijas. Tās organizācijām sniedz iespēju veikt “Kā būtu, ja” analīzi, lai pielāgotu rēķinu un debitoru parametrus un pēc tam salīdzinātu attiecīgo iespaidu, kas atstāts uz savlaicīgas rēķinu apmaksas iespējamību.

Piemēram, organizācija var vēlēties novērtēt, kādu iespaidu uz savlaicīgu maksājuma izpildi atstāj rēķinu termiņatlaides atjaunināšana. Kad rēķini ir optimizēti jaunās atlaides izmantošanai, lietotāji var apskatīt atstāto iespaidu, lietojot šo atlaidi attiecīgo rēķinu savlaicīgas apmaksas iespējamībai. Ja šīs atlaides lietošanas izmaksas ir minimālas, salīdzinot ar savlaicīgas maksājuma saņemšanas priekšrocībām, organizācija var izvēlēties atlasīto atlaidi lietot visiem turpmākajiem neapmaksātajiem pasūtījumiem.

> [!NOTE] 
> Pašlaik vienīgā līdzeklī Debitoru maksājumu ieskati (priekšskatījums) pieejamā optimizācijas stratēģija ir atlaide.

[![Optimizētās prognozes](./media/optimized-pay.png)](./media/optimized-pay.png)

## <a name="how-to-get-customer-payment-insights-preview"></a>Kā iegūt līdzekli Debitoru maksājumu ieskati (priekšskatījums)

Ja vēlaties izmēģināt līdzekli Debitoru maksājumu ieskati (priekšskatījums), sūtiet e-pasta ziņojumu [finanšu ieskatu priekšskatījumu grupai](mailto:fiap@microsoft.com). 

## <a name="privacy-statement"></a>Paziņojums par konfidencialitāti

Priekšskatījumos Amerikas Savienotajās Valstīs tiek glabāti debitoru dati. Turklāt priekšskatījumiem (1) var tikt izmantots mazāk konfidencialitātes un drošības pasākumu nekā pakalpojumam Dynamics 365 for Finance and Operations, (2) tie nav ietverti pakalpojuma līmeņa līgumā par šo pakalpojumu, (3) tos nedrīkst izmantot personas datu vai citu tādu datu apstrādei, uz kuriem attiecas juridiskās vai normatīvās prasības, un (4) tiem tiek nodrošināts ierobežots atbalsts.
