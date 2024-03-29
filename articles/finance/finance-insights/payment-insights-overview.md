---
title: Debitoru maksājumu prognozes
description: Šajā rakstā ir aprakstīta maksājumu prognozēšanas iespēja, kas var palīdzēt labāk izprast debitora parasto maksājumu praksi. Šis līdzeklis var arī palīdzēt identificēt apstākļus, kas varētu izraisīt to, ka jūs sākat iekasēšanas procesu agrāk, nekā to varētu sākt citādi.
author: ShivamPandey-msft
ms.date: 11/03/2021
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
ms.openlocfilehash: 5d16b42b4538a18ca3dd9d3bac25ed1af1441ace
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903165"
---
# <a name="customer-payment-predictions"></a>Debitoru maksājumu prognozes

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīta maksājumu prognozēšanas iespēja, kas var palīdzēt labāk izprast debitora parasto maksājumu praksi. Šis līdzeklis var arī palīdzēt identificēt apstākļus, kas varētu izraisīt to, ka jūs sākat iekasēšanas procesu agrāk, nekā to varētu sākt citādi.

## <a name="overview"></a>Pārskats

Organizācijām bieži ir grūti noteikt, kad debitori apmaksās rēķinus. Šis informācijas trūkums var izraisīt šādas problēmas:

- Neprecīzākas naudas plūsmas prognozes
- Iekasēšanas procesi, kas sākas pārāk vēlu
- Pasūtījumi, kas tiek izlaisti debitoriem, kuri varētu neveikt maksājumu

Debitoru maksājumu prognozes palīdz organizācijai prognozēt, kad debitora rēķins tiks apmaksāts. Tāpēc tās var izveidot iekasēšanas stratēģijas, kas palīdz palielināt iespējamību, ka rēķini tiks apmaksāti laikā.

## <a name="predictions"></a>Prognozes

Maksājumu prognozes ļauj organizācijām uzlabot savus biznesa procesus, palīdzot tiem identificēt rēķinus, kas varētu tikt apmaksāti ar novēlošanos. Organizācija var izmantot šo informāciju, lai veiktu darbības, kas uzlabo iespējamību, ka rēķini tiks apmaksāti laikā.

Klienta maksājumu prognožu funkcija izmanto algoritmiskās mācīšanās modeli, lai precīzāk prognozētu, kad debitors apmaksās rēķinu. Šajā algoritmiskās mācīšanās modelī ir ietverti vēsturiski rēķini, maksājumi un debitora dati.

Katram atvērtajam rēķinam līdzeklis piešķir trīs apmaksas iespējamības:

- Iespējamība, ka maksājums tiks veikts laikā
- Iespējamība, ka maksājums tiks veikts novēloti
- Iespējamība, ka maksājums tiks veikts ļoti novēloti

Šis līdzeklis sniedz arī apkopotu skatījumu par paredzētajiem maksājumiem.

[![Apkopots skats uz maksājuma prognozēm.](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)

Turklāt katram rēķinam ir piešķirta laikā veikta maksājuma iespējamība. Rēķini, kuru laicīgas apmaksas iespējamība ir mazāka par 50 procentiem, tiek atzīmēti ar sarkanu apli, lai norādītu, ka parādu piedziņas atbildīgajam darbiniekam, iespējams, būs jāapskata šie rēķini.

[![Maksājumu iespējamības saraksts.](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)

Debitora maksājumu prognožu līdzeklis sniedz arī kontekstuālu informāciju, lai izskaidrotu prognozēšanu. Šī informācija ietver galvenos faktorus, kas ietekmēja prognozēšanu, pašreizējo biznesa situāciju ar debitoru un detalizētu informāciju par debitora vēsturiskas darbības ar maksājumiem.

Daudzos uzņēmumos iekasēšanas process ir reaktīva darbība. Citiem vārdiem sakot, iekasēšanas process netiek sākts, kamēr nav beidzies rēķinu termiņš. Debitoru maksājumu prognozes ļauj organizācijām būt aktīvākām iekasēšanas procesā. Vairs nav jāgaida, kamēr beidzas darījuma termiņš, lai sāktu iekasēšanas procesu. Tā vietā tās var izmantot maksājumu prognozēšanas iespēju, lai noteiktu, vai proaktīvās iekasēšanas uzlabos iespējamību, ka tiks maksāts laikā.

## <a name="methodology"></a>Metodoloģija

Iepriekš parasti bija sarežģīti izstrādāt un izvietot mākslīgā intelekta (AI) risinājumu. Procesam bija nepieciešama datu zinātnieku grupa, mācību priekšmetu eksperti un inženieri, kas strādā ilgāku laika periodu, lai formulētu, attīstītu, izvietotu un uzturētu izmantojamu AI risinājumu. Debitoru maksājumu prognozes atvieglo AI Microsoft Dynamics risinājuma izvietošanu un izmantošanu 365 finansēs. Microsoft ir AI risinājumu prepakošana, kuru pamatā ir korporācija Microsoft AI Builder. Tāpēc lietotāji var izvietot AI risinājumu ar vienu peles klikšķi, lai izmantotu inteliģento prognožu priekšrocības. Ja neesat apmierināts ar prognozēšanas precizitāti, power lietotājs var (vēlreiz ar vienu peles klikšķi) AI Builder ievadīt paplašinājuma pieredzi, un pēc tam atlasiet vai notīriet laukus, kas tiek izmantoti prognozēšanas ģenerēšanas laikā. Kad esat gatavs, varat apmācīt modeli un publicēt izmaiņas. Jaunais ierobežotais modelis tiks automātiski paņemts, lai ģenerētu prognozes Dynamics 365 Finansēs.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
