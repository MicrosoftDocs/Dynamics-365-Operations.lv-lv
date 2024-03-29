---
title: Patēriņa reģistrēšana
description: Šajā rakstā skaidrots, kā reģistrēt patēriņu Pamatlīdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderJournal, EntAssetWorkOrderAddSparePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 729ef6aae228ad1e528945031567b92c44cdf256
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111760"
---
# <a name="register-consumption"></a>Patēriņa reģistrēšana

[!include [banner](../../includes/banner.md)]

 

Kad uzturēšanas darbs ir pabeigts darba pasūtījumā, nākamā darbība ir izveidot patēriņa reģistrācijas un grāmatot žurnālus. Varat izveidot reģistrācijas tālāk norādītajos patēriņa veidos: stundas, krājumi un izdevumi. Dažādie patēriņa veidi tiek reģistrēti un grāmatoti lapā **Darba pasūtījuma žurnāli**. Žurnāla iestatījumi **Līdzekļu pārvaldībā** tiek izmantoti, lai izveidotu un grāmatotu atsevišķus žurnālus stundām, krājumiem un izdevumiem modulī **Projektu pārvaldība un uzskaite**.

Dažos gadījumos, iespējams, jūs varat pievienot vai dzēst prognozes rindas darba pasūtījumā. Darba pasūtījuma dzīves cikla stāvokļa iestatījums, saistītais projekta tips un stadijas noteikumi, kas saistīti ar projekta tipu, nosaka, vai varat pievienot vai rediģēt žurnāla rindas. Lasiet vairāk informācijas par darba pasūtījumu dzīves cikla stāvokļiem un saistītiem projekta posmiem [Prognozes, darba pasūtījumi un projekti](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).

>[!NOTE]
>Var iestatīt automātisku žurnālu grāmatošanu darba pasūtījuma dzīves cikla stāvoklī. Vairāk informācijas skatiet sadaļā [Darba pasūtījuma dzīves cikla stāvokļi](../setup-for-work-orders/work-order-lifecycle-states.md).

1. Noklikšķiniet **uz Līdzekļu pārvaldības** > **darbs pasūtījumiem** > **visi darba pasūtījumi** vai aktīvie **darba pasūtījumi**.

2. Atlasiet darba pasūtījumu un noklikšķiniet uz **Žurnāli**.

3. Noklikšķiniet uz **Kopēt no prognozes**, lai pārsūtītu jebkuras prognozes rindas, kas var būt saistītas ar darba pasūtījumu. Varat atlasīt, kurus patēriņa veidus vēlaties pārsūtīt.

4. Ja nepieciešams, varat pievienot papildu patēriņa rindas attiecīgajā kopsavilkuma cilnē, noklikšķinot uz **Pievienot rindu** un aizpildot rindas datus.

5. Noklikšķiniet uz **Validēt žurnālus**, lai validētu žurnāla rindas pirms grāmatošanas.

6. Noklikšķiniet uz **Grāmatot žurnālus**, lai grāmatotu žurnāla rindas.

7. Pēc patēriņa žurnālu grāmatošanas varat atjaunināt darba pasūtījuma dzīves cikla stāvokli. Piemēram, lai norādītu, ka darba pasūtījums ir pabeigts, varat atjaunināt dzīves cikla stāvokli uz "Pabeigts".

    - Laukā **Rādīt**, kas atrodas lapas **Darba pasūtījuma žurnāli** augšdaļā, atlasiet, kuras žurnāla rindas vēlaties skatīt: **Visas**, **Negrāmatotās** vai **Grāmatotās**. Grāmatotajiem žurnāliem ir atzīme izvēles rūtī **Grāmatotas**.  
    - Kad krājumu rindas ir veidotas darba pasūtījumu žurnālā, preču dimensijas un izsekošanas dimensijas, kas saistītas ar krājumu, tiek automātiski pārsūtītas uz žurnāla rindu.  

Tālāk redzamajā ekrānuzņēmumā ir parādīts stundas vai krājuma reģistrācijas piemērs darba pasūtījumā **Darba pasūtījuma žurnāli**.

![1. attēls.](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a>Stundu sadalīšana darba pasūtījumos ar vairākiem darbu pasūtījuma uzdevumiem

Ja darba pasūtījumā ir vairāki darba pasūtījuma uzdevumi, varat reģistrēt darba stundas, izmantojot funkciju **Sadalīt stundas**, t. i., vienas stundas reģistrācijas rinda var tikt vienmērīgi sadalīta katrā darba pasūtījuma uzdevumā.

1. Noklikšķiniet **uz Līdzekļu pārvaldības** > **darbs pasūtījumiem** > **visi darba pasūtījumi** vai aktīvie **darba pasūtījumi**.

2. Atlasiet darba pasūtījumu un noklikšķiniet uz **Žurnāli**.

3. Atlasiet stundu reģistrācijas rindu, kuru vēlaties sadalīt, un noklikšķiniet uz **Sadalīt stundas**.

4. Dialoglodziņā **Sadalīt stundas darba pasūtījuma uzturēšanas darbiem** laukā **Nodarbinātais** automātiski tiek parādīt tā darbinieka vārds, kas ir pieteicies. Ja nepieciešams, varat atlasīt citu darbinieku.

5. Atlasiet kategoriju stundu reģistrācijai laukā **Kategorija**.

6. Ievadiet darba stundu skaitu, kas jāsadala, laukā **Stundas**.

    ![2. attēls.](media/02-consumption.png)

7. Noklikšķiniet uz **Labi**.

*Piemērs:* tālāk redzamajā ekrānuzņēmumā ir parādītas žurnāla rindas darba pasūtījumam, kas ietver trīs darba pasūtījuma uzdevumus. Pirmā rinda, kas ietver trīs darba stundas, ir sadalīta, un viena darba stunda tiek reģistrēta katram darba pasūtījuma uzdevumam. Pēc tam, kad ir izveidotas trīs stundu reģistrācijas rindas, varat izlemt, ko darīt ar sākotnējo stundu reģistrācijas rindu (piemērā norādīta kā pirmā rinda). Varat to atstāt tādu, kāda tā ir, vai dzēst. 

![3. attēls.](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a>Finanšu dimensijas patēriņa reģistrācijās

Veicot patēriņa reģistrācijas, noteiktā secībā reģistrācijām tiek pievienotas ar dažādiem reģistrācijas tipiem saistītās finanšu dimensijas. 

- *Stundu un izdevumu reģistrācijas:* vispirms tiek pievienotas finanšu dimensijas no žurnāla virsraksta, ja tādas ir. Pēc tam tiek pievienotas finanšu dimensijas no saistītā darba pasūtījuma projekta. Visbeidzot, tiek pievienotas finanšu dimensijas no resursa (nodarbinātā).

- *Krājumu reģistrācijas:* vispirms tiek pievienotas finanšu dimensijas no žurnāla virsraksta, ja tādas ir. Pēc tam tiek pievienotas finanšu dimensijas no saistītā darba pasūtījuma projekta. Pēc tam tiek pievienotas finanšu dimensijas no vietas. Visbeidzot, tiek pievienotas finanšu dimensijas no krājuma.

>[!NOTE]
>Visiem trim reģistrācijas tipiem tiek validēta finanšu dimensiju kombinācija, un nederīgas kombinācijas tiek atstatas tukšas. Tas ir standarta iestatījums ar citām finanšu un operāciju programmām.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
