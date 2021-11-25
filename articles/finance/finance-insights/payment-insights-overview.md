---
title: Debitoru maksājumu prognozes
description: Šī tēma apraksta maksājuma prognožu iespēju, kas var palīdzēt labāk izprast debitora parasto maksājumu praksi. Šis līdzeklis var arī palīdzēt identificēt apstākļus, kas varētu izraisīt to, ka jūs sākat iekasēšanas procesu agrāk, nekā to varētu sākt citādi.
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 300c835c835a5c653b75b9e151462337dfbe49a5
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752741"
---
# <a name="customer-payment-predictions"></a>Debitoru maksājumu prognozes

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šī tēma apraksta maksājuma prognožu iespēju, kas var palīdzēt labāk izprast debitora parasto maksājumu praksi. Šis līdzeklis var arī palīdzēt identificēt apstākļus, kas varētu izraisīt to, ka jūs sākat iekasēšanas procesu agrāk, nekā to varētu sākt citādi.

## <a name="overview"></a>Pārskats

Organizācijām bieži ir grūti noteikt, kad debitori apmaksās rēķinus. Šis informācijas trūkums var izraisīt šādas problēmas:

- Neprecīzākas naudas plūsmas prognozes
- Iekasēšanas procesi, kas sākas pārāk vēlu
- Pasūtījumi, kas tiek izlaisti debitoriem, kuri varētu neveikt maksājumu

Debitoru maksājumu prognozes (priekšskatījums) palīdz organizācijām prognozēt, kad tiks apmaksāts debitora rēķins. Tāpēc tās var izveidot iekasēšanas stratēģijas, kas palīdz palielināt iespējamību, ka rēķini tiks apmaksāti laikā.

## <a name="predictions"></a>Prognozes

Maksājumu prognozes ļauj organizācijām uzlabot savus biznesa procesus, palīdzot tiem identificēt rēķinus, kas varētu tikt apmaksāti ar novēlošanos. Organizācija var izmantot šo informāciju, lai veiktu darbības, kas uzlabo iespējamību, ka rēķini tiks apmaksāti laikā.

Klienta maksājumu prognožu funkcija izmanto algoritmiskās mācīšanās modeli, lai precīzāk prognozētu, kad debitors apmaksās rēķinu. Šajā algoritmiskās mācīšanās modelī ir ietverti vēsturiski rēķini, maksājumi un debitora dati.

Katram atvērtajam rēķinam līdzeklis piešķir trīs apmaksas iespējamības:

- Iespējamība, ka maksājums tiks veikts laikā
- Iespējamība, ka maksājums tiks veikts novēloti
- Iespējamība, ka maksājums tiks veikts ļoti novēloti

Šis līdzeklis sniedz arī apkopotu skatījumu par paredzētajiem maksājumiem.

[![ Apkopots skats uz maksājuma prognozēm.](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)

Turklāt katram rēķinam ir piešķirta laikā veikta maksājuma iespējamība. Rēķini, kuru laicīgas apmaksas iespējamība ir mazāka par 50 procentiem, tiek atzīmēti ar sarkanu apli, lai norādītu, ka parādu piedziņas atbildīgajam darbiniekam, iespējams, būs jāapskata šie rēķini.

[![ Maksājumu iespējamības saraksts.](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)

Debitora maksājumu prognožu līdzeklis sniedz arī kontekstuālu informāciju, lai izskaidrotu prognozēšanu. Šī informācija ietver galvenos faktorus, kas ietekmēja prognozēšanu, pašreizējo biznesa situāciju ar debitoru un detalizētu informāciju par debitora vēsturiskas darbības ar maksājumiem.

Daudzos uzņēmumos iekasēšanas process ir reaktīva darbība. Citiem vārdiem sakot, iekasēšanas process netiek sākts, kamēr nav beidzies rēķinu termiņš. Debitoru maksājumu prognozes ļauj organizācijām būt aktīvākām iekasēšanas procesā. Vairs nav jāgaida, kamēr beidzas darījuma termiņš, lai sāktu iekasēšanas procesu. Tā vietā tās var izmantot maksājumu prognozēšanas iespēju, lai noteiktu, vai proaktīvās iekasēšanas uzlabos iespējamību, ka tiks maksāts laikā.

## <a name="methodology"></a>Metodoloģija

Iepriekš parasti bija sarežģīti izstrādāt un izvietot mākslīgā intelekta (AI) risinājumu. Procesam bija nepieciešama datu zinātnieku grupa, mācību priekšmetu eksperti un inženieri, kas strādā ilgāku laika periodu, lai formulētu, attīstītu, izvietotu un uzturētu izmantojamu AI risinājumu. Debitoru maksājumu prognozes atvieglo AI risinājuma izvietošanu un izmantošanu pakalpojumā Microsoft Dynamics 365 Finance. Microsoft ir ievietojis AI risinājumus, kas ir iebūvēti papildus Microsoft AI Builder. Tāpēc lietotāji var izvietot AI risinājumu ar vienu peles klikšķi, lai izmantotu inteliģento prognožu priekšrocības. Ja neesat apmierināts ar prognožu precizitāti, prasmīgs lietotājs (atkal, izmantojot vienu klikšķi) var atvērt AI Builder paplašinājumu un pēc tam atlasīt vai noņemt laukus, ko izmanto prognožu ģenerēšanai. Kad esat gatavs, varat apmācīt modeli un publicēt izmaiņas. Jaunais apmācītais modelis tiks automātiski izvēlēts, lai ģenerētu prognozes pakalpojumā Dynamics 365 Finance.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
