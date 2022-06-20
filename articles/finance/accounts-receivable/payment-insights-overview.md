---
title: Klienta maksājumu ieskati (priekšskatījums)
description: Šajā dokumentā ir aprakstīta maksājumu ieskatu iespēja, kas palīdz uzlabot izpratni par atsevišķu debitoru tipisko maksājumu praksi. Šis līdzeklis var arī palīdzēt identificēt apstākļus, kas attaisno iekasēšanas procesu sākšanu agrāk, nekā to varētu sākt citādi.
author: ShivamPandey-msft
ms.date: 11/06/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 54655d2b1cfb4b11f32842d4c3cff2f4d8e97ef5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856804"
---
# <a name="customer-payment-insights-preview"></a>Klienta maksājumu ieskati (priekšskatījums)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šajā dokumentā ir aprakstīta maksājumu ieskatu iespēja, kas palīdz uzlabot izpratni par atsevišķu debitoru tipisko maksājumu praksi. Šis līdzeklis var arī palīdzēt identificēt apstākļus, kas attaisno iekasēšanas procesu sākšanu agrāk, nekā to varētu sākt citādi. 

## <a name="overview"></a>Pārskats

Var būt grūti noteikt, kad debitori apmaksās rēķinus. Šis informācijas trūkums noved pie ne tik precīzām naudas plūsmas prognozēm, iekasēšanas procesiem, kas sākas ar novēlošanos, un pasūtījumiem, kas tiek nodoti debitoriem, kuri var neizpildīt savus maksājumus. Debitoru maksājumu ieskati (priekšskatījums) palīdz organizācijām prognozēt, kad tiks apmaksāts debitora rēķins. Šī informācija var palīdzēt organizācijām izveidot iekasēšanas stratēģijas, kas uzlabo iespējamību par laicīgu apmaksu. 

## <a name="predictions"></a>Prognozes

Maksājumu prognozes dos iespēju uzņēmumiem uzlabot savus biznesa procesus, palīdzot tiem viegli identificēt rēķinus, kas varētu tikt apmaksāti ar novēlošanos, un veikt piemērotus pasākumus, kas uzlabo viņu iespējas saņemt atalgojumu laika gaitā.

Izmantojot mašīnu mācīšanās modeli, kas palīdz veikt vēsturiskos rēķinus, maksājumus un debitora datus, debitoru maksājumu ieskatus (priekšskatījums) precīzāk prognozē, kad debitors maksās nenomaksātu rēķinu.

Katram neapmaksātajam rēķinam līdzeklis Debitoru maksājumu ieskati (priekšskatījums) prognozē trīs maksājumu iespējamības:

-   Iespējamība, ka maksājums tiek veikts laikā 
-   Iespējamība, ka maksājums tiek veikts novēloti
-   Iespējamība, ka maksājums tiek veikts ļoti novēloti

Debitora maksājumu ieskati (priekšskatījums) sniedz arī apkopotu skatu par gaidāmajiem maksājumiem, kas var palīdzēt organizācijām izprast kopējo maksājuma summu, ko tās var sagaidīt no debitora vienā no trijiem intervāliem (Laikā, Novēloti un Ļoti novēloti).

[![Apkopots skats uz maksājuma prognozēm.](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)

Turklāt katram rēķinam ir piešķirta maksājuma iespējamība laikā. Ja maksājuma iespējamība laikā ir mazāka par 50%, rēķini tiek atzīmēti ar sarkanu apli, lai norādītu, ka šiem rēķiniem var būt nepieciešama uzmanība iekasēšanā. 

[![Maksājumu iespējamības saraksts.](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)

Debitora maksājuma ieskats (priekšskatījums) sniedz arī kontekstuālu informāciju, lai izskaidrotu prognozēšanu, piemēram, vislabākos faktorus, kas ietekmēja prognozes, pašreizējo biznesa situāciju ar debitoru un detalizētu informāciju par vēsturisko debitoru maksājumu uzvedību. Daudzos uzņēmumos iekasēšanas process ir aktīva darbība; iekasēšanas process netiek sākts, līdz pienāk rēķinu apmaksas laiks. 

Ar debitoru maksājumu ieskatu (priekšskatījums), organizācijas var būt aktīvākas iekasēšanas procesā. Vairs nav jāgaida uz transakcijām, lai sāktu iekasēšanas procesu. Tā vietā tās var izmantot maksājumu prognozēšanas iespēju, lai noteiktu, vai proaktīvās iekasēšanas uzlabos iespējamību, ka tiks maksāts laikā. Maksājumu prognozēšana arī sniedz uzņēmumiem informāciju, kas nepieciešama, lai attaisnotu agrāku iekasēšanas procesu.

## <a name="methodology"></a>Metodoloģija

AI risinājuma izstrāde un izvietošana ir grūta. Ir nepieciešama datu zinātnieku grupa, mācību priekšmetu eksperti un inženieri, kas strādā ilgāku laika periodu, lai formulētu, attīstītu, izvietotu un uzturētu izmantojamu AI risinājumu. Mēs atvieglojam AI risinājumu izvietošanu un izmantošanu programmā Finance. Mēs esam prepackaging AI risinājumi Finansēs, kas ir veidotas uz Microsoft bāzes AI Builder. Gala lietotājs ar vienu pogas klikšķi var izvietot AI risinājumu un sākt izmantot inteliģento prognožu iespējas. Ja organizācija nav apmierināta ar prognožu precizitāti, prasmīgs lietotājs, atkal izmantojot vienu klikšķi, var ievadīt AI builder paplašināšanas pieredzi un pēc tam atlasīt vai noņemt laukus, ko izmanto prognožu ģenerēšanai. Kad tas ir sagatavots, tie var apmācīt un publicēt izmaiņas, un jaunais modelis tiks automātiski ievākts prognozēm programmā Finance.

## <a name="how-to-get-customer-payment-insights-preview"></a>Kā iegūt debitoru maksājumu ieskatus (priekšskatījums)?

Nosūtiet e-pasta ziņojumu uz [Debitoru maksājumu ieskati (priekšskatījums)](mailto:fiap@microsoft.com), ja vēlaties izmēģināt Debitoru maksājumu ieskatus (priekšskatījums).

## <a name="privacy-notice"></a>Paziņojums par konfidencialitāti

Priekšskatījumi (1) var izmantot mazāk konfidencialitātes un drošības pasākumus nekā Dynamics 365 Finanšu un operāciju pakalpojums, (2) nav iekļauti šī pakalpojuma līmeņa līgumā, (3) nedrīkst izmantot personas datu apstrādāšanai vai citiem datiem, uz kuriem attiecas juridiskās vai regulēšanas saskaņotības prasības, un 4. ir ierobežots atbalsts.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
