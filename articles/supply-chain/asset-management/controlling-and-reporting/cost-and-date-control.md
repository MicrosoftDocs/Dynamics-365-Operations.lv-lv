---
title: Izmaksu un datuma kontrole
description: Šajā tēmā ir paskaidrota izmaksu un datuma kontrole programmā Asset Management.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetBICostControlWorkspace, EntAssetWorkOrderDateControl, EntAssetWorkOrderForecastCostInfoPart, EntAssetMaintenanceCostTrans, EntAssetWorkOrderDateControlCalcDialog, EntAssetCostControl, EntAssetCostObjectCalendar, EntAssetWorkOrderCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1de12233ff296f77ba9984fa8d957d4c2bc90b3f
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019079"
---
# <a name="cost-and-date-control"></a>Izmaksu un datuma kontrole

[!include [banner](../../includes/banner.md)]

 

Programmā Asset Management varat aprēķināt faktisko līdzekļu kļūmju izmaksas, lai iegūtu pārskatu salīdzinājumā ar kļūmju, funkcionālo novietojumu un darba pasūtījumu budžetētajām izmaksām. Faktiskās izmaksas ir balstītas uz publicētajiem darījumiem. 

Varat veikt datuma aprēķinu, arī ja vēlaties salīdzināt plānoto sākuma datumu un beigu datumu ar faktisko sākuma un beigu datumu darba pasūtījumiem.

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a>Līdzekļu izmaksu kontrole, funkcionālie novietojumi un darba pasūtījumi

Aprēķini, kas veikti līdzekļiem, funkcionālajam novietojumam un darba pasūtījumiem, ir gandrīz identiski. Vienīgā atšķirība ir tā, ka līdzekļiem un funkcionālajam novietojumam aprēķinā var iekļaut arī pakārtotus līdzekļus un pakārtotas atrašanās vietas. Datums ir transakcijas datums, kad reģistrācija tika ierakstīta.

1. Klikšķiniet uz **Līdzekļu pārvaldība** > **Pieprasījumi** > **Līdzekļi** > **Līdzekļu izmaksu kontrole** vai **Funkcionālā novietojuma izmaksu kontrole**, vai **Aktīvu pārvaldība** > **Pieprasījumi** > **Darba pasūtījumi** > **Darba pasūtījumu izmaksu kontrole**.

2. Dialog­ā **Līdzekļu izmaksu kontrole** / **Funkcionālā novietojuma izmaksu kontrole** / **Darba pasūtījuma izmaksu kontrole** atlasiet aprēķina laika diapazonu.

3. Ja vajadzīgs, izvēlieties finansiālo parametru kopu, ko iekļaut aprēķinā.

4. Pārslēgšanas pogā **Izlaist nulli** atlasiet „Jā”, ja nevēlaties, lai rāda rezultātus, kas satur nulles izmaksas.

5. Jūs varat izmantot lauku **Līmenis**, lai noteiktu, cik detalizētas vēlaties izmaksu kontroles rindas attiecībā uz funkcionālo novietojumu. 

    Piemēram, ja laukā ievadāt ciparu „1” un jums ir vairāklīmeņu funkcionālā novietojuma hierarhija, visas izmaksu kontroles rindas funkcionālajam novietojumam tiks uzrādītas augstākajā līmenī, tāpēc stundas rindā var tikt pievienotas no funkcionāliem novietojumiem, kas atrodas zemākā līmenī. 
    
    Ja laukā **Līmenis** ievadāt ciparu „„0””, jūs redzēsit detalizētu rezultātu, kas uzrādīs visas izmaksu kontroles rindas visos funkcionālā novietojuma līmeņos, ar kuriem tās ir saistītas.

6. Pārslēgšanas pogā **Parādīt atvērto saistību izmaksas** atlasiet "Jā", ja vēlaties iekļaut aprēķinā to sleju.

7. Atlasiet “Jā” pārslēgšanas pogā **Ietvert pakārtotos līdzekļus**, lai parādītu izmaksas, kas saistītas ar pakārtotajiem līdzekļiem kā atsevišķas rindas.

8. Ja vēlaties ierobežot meklēšanu, varat atlasīt konkrētus līdzekļus/funkcionālos novietojumus/darba pasūtījumus, lai iekļautu kopsavilkuma cilnē **Ieraksti, kas jāiekļauj**.

9. Noklikšķiniet uz **Labi**, lai sāktu aprēķināšanu.

    Zemāk esošajā attēlā ir parādīts **Līdzekļu izmaksu kontroles** dialogs.

    ![Līdzekļu izmaksu kontroles dialoglodziņš](media/01-controlling-and-reporting.png)

10. Lapā **Līdzekļu izmaksu kontrole** noklikšķiniet uz attiecīgās pogas **Grupēt pēc..**, lai uzrādītu nepieciešamo aprēķina informācijas detalizācijas līmeni. Atlasītās **Grupēt pēc** pogas ir izceltas. Noklikšķiniet uz pogas, lai to aktivizētu vai deaktivizētu.

## <a name="example"></a>Paraugs

Tālāk esošajā ekrānuzņēmumā ir parādīts līdzekļu aprēķina rezultātu piemērs **Līdzekļu izmaksu kontrolē**.

- Laukā **Sākotnējais budžets** rāda budžetētās izmaksas no darba pasūtījuma prognozes. 
- **Saistību izmaksu** lauks rāda kopējās izmaksas, kuras juridiskā persona uzņēmusies maksāt. 
- Laukā **Atvērtās saistību izmaksa** redzamas saistība par maksājumiem par vienumiem, stundām un pakalpojumiem, ko esat pasūtījis vai saņēmis, bet vēl neesat apmaksājis. 
- Kad ir grāmatotas visas patēriņa reģistrācijas, saistītās izmaksas tiek iekļautas laukā **Faktiskās izmaksas**.

![Piemēram, aprēķina rezultāts ir Līdzekļu izmaksu kontrolē](media/02-controlling-and-reporting.png)

Cits veids, kā veikt izmaksu aprēķinu, ir atzīmēt vairākus līdzekļus sadaļā **Visi līdzekļi** vai **Aktīvie līdzekļi**. Tad klikšķiniet uz pogas **Izmaksu kontrole** cilnē **Vispārēji**. Dialogā **Līdzekļu izmaksu kontrole** atlasītie līdzekļi tiek automātiski ievietoti laukā **Līdzekļi** kopsavilkuma cilnē **Iekļaujamie ieraksti**. Klikšķiniet uz **Labi**, tiks parādīts atlasīto līdzekļu izmaksu aprēķins. To pašu procedūru var veikt funkcionālajiem novietojumiem sadaļās **Visi funkcionālie novietojumi** vai **Aktīvie funkcionālie novietojumi** un darba pasūtījumiem sadaļās **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**.


## <a name="work-order-date-control"></a>Darba pasūtījuma datuma kontrole

Izmantojiet šo lapu, lai redzētu pārskatu par plānoto sākuma datumu un beigu datumu, salīdzinot ar faktisko sākuma un beigu datumu darba pasūtījumiem.

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Pieprasījumi** > **Darba pasūtījumi** > **Darba pasūtījumu datuma kontrole**.

2. Noklikšķiniet uz **Aprēķināt**.

3. Laukā **Funkcionālais novietojums** atlasiet funkcionālo novietojumu.

4. Ievadiet diapazonu, kuram vēlaties veikt aprēķinu, laukos **Datums no** un **Datums līdz**. Tiks iekļauti visi darba pasūtījumi ar paredzamo sākuma datumu diapazonā.

5. Noklikšķiniet uz **Labi**.

6. Noklikšķiniet uz pogas **Grupēt pēc**, lai uzrādītu nepieciešamo aprēķina informācijas detalizācijas līmeni. Atlasītās **Grupēt pēc** pogas ir izceltas. Noklikšķiniet uz pogas, lai to aktivizētu vai deaktivizētu.

## <a name="example"></a>Paraugs

Tālāk esošajā ekrānuzņēmumā ir parādīts līdzekļu aprēķina rezultātu piemērs **Darba pasūtījumu datumu kontrolē**.

- Laukā **Vidējais sākuma kavējums** tiks parādīta starpība dienās starp darba pasūtījuma ieplānoto sākuma datumu un faktisko sākuma datuma. Ja, piemēram, faktiskais sākuma datums bijis divas dienas pirms ieplānotā datuma, šajā laukā rādīs „-2”.  
- Laukā **Vidējais beigu kavējums** tiks parādīta starpība starp darba pasūtījuma ieplānoto beigu datumu un faktisko beigu datumu. Ja, piemēram, faktiskais beigu datums bijis trīs dienas pēc ieplānotā datuma, šajā laukā rādīs „3”.  
- Laukā **Gadījumi** parāda skaitli, cik bieži notikušas novirzes attiecībā uz plānoto un faktisko sākuma datumu un plānoto un faktisko darba pasūtījuma datumu.

![Piemēram, aprēķina rezultāts ir Darba pasūtījuma datuma kontrole](media/03-controlling-and-reporting.png)


