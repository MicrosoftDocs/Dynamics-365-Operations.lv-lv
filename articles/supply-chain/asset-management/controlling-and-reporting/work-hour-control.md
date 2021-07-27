---
title: Darba stundu kontrole
description: Šajā tēmā ir aprakstīta darba stundu kontrole līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetHourControl
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 88ae7faabe7af25f6e3b95c7217d91e440c94da2
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346206"
---
# <a name="work-hour-control"></a>Darba stundu kontrole

[!include [banner](../../includes/banner.md)]

 

Līdzekļu pārvaldībā varat aprēķināt stundas, lai iegūtu pārskatu par faktiskajām stundām, salīdzinot ar budžeta stundām uz līdzekļiem, funkcionālajiem novietojumiem vai darba pasūtījumiem. Faktiskās stundas ir balstītas uz grāmatotajām transakcijām.

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a>Darba stundu kontrole līdzekļiem, funkcionālajam novietojumam un darba pasūtījumiem

Aprēķini, kas veikti līdzekļiem, funkcionālajam novietojumam un darba pasūtījumiem, ir gandrīz identiski. Tikai atšķirība ir tā, ka līdzekļiem un funkcionālajam novietojumam aprēķinā var iekļaut arī pakārtotus līdzekļus un pakārtotas atrašanās vietas. Datums ir transakcijas datums, kad reģistrācija tika ierakstīta.

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Pieprasījumi** > **Līdzekļi** > **Līdzekļu stundu kontrole** vai **Funkcionālā novietojuma stundu kontrole**, vai **Līdzekļu pārvaldība** > **Pieprasījumi** > **Darba pasūtījumi** > **Darba pasūtījumu stundu kontrole**.

2. Dialoglodziņā **Līdzekļu stundu kontrole**.

3. Dialoglodziņā **Līdzekļa stundu kontrole** / **Funkcionālā novietojuma stundu kontrole** / **Darba pasūtījumu stundu kontrole** atlasiet periodu, kas jāaprēķina laukos **No datuma** un **Līdz datumam**.

4. Ja nepieciešams, atlasiet **Finanšu dimensiju kopu**, kas jāiekļauj aprēķinā.

5. Ja nevēlaties rādīt rezultātus, kas satur nulles, atlasiet “Jā” pārslēgšanas pogā **Izlaist nulles**.

6. Varat izmantot lauku **Līmenis**, lai norādītu, cik detalizētas jūs vēlaties stundu kontroles rindas attiecībā uz funkcionālajiem novietojumiem. 

    Piemēram, ja laukā tiek ievietots skaitlis “1” un jums ir vairāku līmeņu funkcionālo novietojumu hierarhija, visaugstākajā līmenī tiks rādītas visas stundu kontroles rindas funkcionālā novietojumā, tāpēc stundas rindā var tikt pievienotas no funkcionālajiem novietojumiem, kas atrodas zemākā līmenī. 
    
    Ja laukā **Līmenis** tiek ievadīts skaitlis “0”, tiek parādīts detalizēts rezultāts, kas parāda visas stundu kontroles rindas visiem funkcionālā novietojuma vietas līmeņiem, ar kuriem tās ir saistītas.

7. Atlasiet “Jā” pārslēgšanas pogā **Ietvert pakārtotos līdzekļus**, lai parādītu izmaksas, kas saistītas ar pakārtotajiem līdzekļiem kā atsevišķas rindas.

8. Ja vēlaties ierobežot meklēšanu, varat atlasīt konkrētus līdzekļus/funkcionālos novietojumus/darba pasūtījumus, lai iekļautu kopsavilkuma cilnē **Ieraksti, kas jāiekļauj**.

9. Noklikšķiniet uz **Labi**, lai sāktu aprēķināšanu.

10. Lapā **Stundu izmaksu kontrole** noklikšķiniet uz attiecīgās pogas **Grupēt pēc**, lai uzrādītu nepieciešamo aprēķina informācijas detalizācijas līmeni. Atlasītās **Grupēt pēc** pogas ir izceltas. Noklikšķiniet uz pogas, lai to aktivizētu vai deaktivizētu.

## <a name="example"></a>Paraugs

Ekrānšāviņā redzams aprēķina **Līdzekļu stundu kontrole** piemērs.

- Lauks **Sākotnējais budžets** rāda budžeta stundas no darba pasūtījuma prognozes. 
- Lauks **Faktiskās stundas** rāda darba pasūtījumu grāmatotās stundas. 
- Lauks **Fiksētās stundas** parāda kopējo stundu summu, ko jūsu uzņēmums ir izmantojis saistībā ar darba pasūtījumiem.

![Pamatlīdzekļu stundu kontroles aprēķina piemērs.](media/04-controlling-and-reporting.png)

Cits stundu aprēķina veids ir vairāku atlasīto līdzekļu atlasīšana sadaļās **Visi līdzekļi** vai **Aktīvie līdzekļi** Pēc tam noklikšķiniet uz pogas **Stundu kontrole**, kas atrodas kopsavilkuma cilnē **Vispārīgi**. Atlasītie līdzekļi automātiski tiek ievietoti laukā **Līdzekļi** kopsavilkuma cilnē **Ieraksti, kas jāiekļauj**. Noklikšķiniet uz **Labi** dialoglodziņā **Līdzekļu stundu kontrole**, un tiks parādīts atlasīto līdzekļu aprēķins. To pašu procedūru var veikt funkcionālajiem novietojumiem sadaļās **Visi funkcionālie novietojumi** vai **Aktīvie funkcionālie novietojumi** un darba pasūtījumiem sadaļās **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**.




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]