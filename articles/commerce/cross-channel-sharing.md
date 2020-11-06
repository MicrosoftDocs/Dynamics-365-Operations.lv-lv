---
title: Starpkanālu koplietošanas iespējošana un izmantošana
description: Šajā tēmā ir aprakstīts, kā iespējot un izmantot Microsoft Dynamics 365 Commerce vietņu veidotāja starpkanālu koplietošanas līdzekli.
author: psimolin
manager: annbe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 77284045bda193500117978102c0565c5f15ec6d
ms.sourcegitcommit: b063bf3a52f19baa11ddba31ef9313d58a0f610e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4019522"
---
# <a name="enable-and-use-cross-channel-sharing"></a>Starpkanālu koplietošanas iespējošana un izmantošana

[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīts, kā iespējot un izmantot Microsoft Dynamics 365 Commerce vietņu veidotāja starpkanālu koplietošanas līdzekli.

## <a name="overview"></a>Pārskats

Starpkanālu koplietošana ļauj mazumtirgotājiem atkārtoti izmantot un kopīgot saturu starp vairākiem vietnes kanāliem. Šī iespēja noder, ja vietņu kanāliem ir saderīga pamatvaloda vai ja tiem ir daudz kopīgu satura vienību.

Starpkanālu koplietošana darbojas, iespējojot noklusējuma kanālu, kurā tiks meklēts pieejamais saturs, ja pieprasītā satura kanālam raksturīgā versija netiek atrasta. Saturs, kas paredzēts koplietošanai starp kanāliem, tiek izveidots noklusējuma kanālā. Šo saturu var lokalizēt jebkurai lokalizācijai, kas tiek lietota jebkurā vietnes kanālā.

## <a name="when-to-use-cross-channel-sharing"></a>Starpkanālu koplietošanas izmantošana

Starpkanālu koplietošana ir noderīga, kad vienas vietnes vairāki kanāli var kopīgot saturu. Piemēram, mazumtirgotājs, kam ir vairāki zīmoli un tīmekļa vitrīnas, kas ir grupētas zem vienas vietnes, var kopīgot atsevišķu saturu starp dažām vai visām tīmekļa vitrīnām. Šis koplietojamais saturs var ietvert lapas, kā noteikumi un nosacījumi, maksājuma nosacījumi, nosūtīšanas metodes un bieži uzdotie jautājumi.

Starpkanālu koplietošana atbalsta arī fragmentus. Tāpēc satura lapa, kas ietver kanālam raksturīgos fragmentus, var tikt izveidota kā starpkanālu satura lapa. Šajā gadījumā, lai gan lielākā daļa satura tiks kopīgots starp kanāliem, kanālam raksturīgie fragmenti starpkanālu lapā tiks atveidoti tikai tad, kad tie tiks pieprasīti atbilstošajā tīmekļa vitrīnas kanālā.

Vietnes, kurām ir tikai viens kanāls vai vietnes, kurām ir vairāki kanāli, kas nevar kopīgot saturu, negūs labumu no starpkanālu koplietošanas.

## <a name="enable-cross-channel-sharing"></a>Starpkanālu koplietošanas iespējošana

Starpkanālu koplietošana tiek iespējot vietnes līmenī. Šī ir vienvirziena operācija. Citiem vārdiem sakot, ja starpkanālu koplietošana tiek iespējota, to nevar atspējot.

Lai iespējotu starpkanālu koplietošanu Commerce vietņu veidotājā, izpildiet tālāk norādītās darbības.

1. Dodieties uz **Vietnes iestatījumi \> Līdzekļi**.
1. Iestatiet līdzekļa **Starpkanāls** opciju uz **Ieslēgts**.

    ![Starpkanāls opcija Commerce vietņu veidotājā ir iestatīta uz Ieslēgts](./media/enabling-cross-channel-sharing.png)

Kad ir iespējota starpkanālu koplietošana, starpkanālu informācija tiks parādīta sadaļā **Kanāli** , kas atrodas **Vietnes iestatījumi \> Līdzekļi** , kā parādīts piemēra nākamajā attēlā.

![Kanālu informācija, kas redzama pēc starpkanālu koplietošanas iespējošanas](./media/channels-cross-channel.png)

Turklāt pēc starpkanālu koplietošanas iespējošanas Commerce vietņu veidotāja augšējā labajā pusē esošajā laukā **Kanāls** tiks iekļauta opcija **Starpkanālu tiešsaistes veikals** , ko var izmantot, lai pārvaldītu starpkanālu saturu, kā parādīts nākamajā attēlā.

![Starpkanālu tiešsaistes veikala opcija laukā Kanāli pēc starpkanālu koplietošanas iespējošanas](./media/cross-channel-dropdown.png)

## <a name="create-and-use-cross-channel-content"></a>Starpkanālu satura izveidošana un izmantošana

Varat izveidot un izmantot starpkanālu saturu vairākos veidos. Piemēram, varat izveidot starpkanālu fragmentus, starpkanālu lapas, kurās tiek izmantots starpkanālam un kanālam raksturīgs saturs, kā arī pārlabot starpkanālu fragmentus ar kanālam raksturīgām fragmentu versijām.

### <a name="create-a-cross-channel-fragment"></a>Starpkanālu fragmenta izveidošana

Lai izveidotu starpkanālu fragmentu Commerce vietņu veidotājā, izpildiet tālāk norādītās darbības.

1. Dodieties uz **Fragmenti** un atlasiet **Jauns** , lai izveidotu jaunu fragmentu.
1. Dialoglodziņā **Jauns fragments** atlasiet moduli **Veicināšanas reklāmkarogs** un pēc tam **Fragmenta nosaukums** ievadiet nosaukumu (piemēram, **Starpkanālu reklāmkarogs** ). Pēc tam atlasiet **Labi**.
1. Moduļa **Veicināšanas reklāmkarogs** rekvizītu rūtī atlasiet **Pievienot ziņojumu** un pēc tam atlasiet **Ziņojums**.
1. Dialoglodziņa **Ziņojums** sadaļā **Teksts** ievadiet **Starpkanāls** un atlasiet **Labi**. 
1. Atlasiet **Saglabāt** , atlasiet **Pabeigt rediģēšanu** , lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt** , lai publicētu to.

Šo starpkanālu fragmentu var izmantot starpkanāla vai kanālam raksturīgās lapās, kas izveidotas jebkurā vietnes kanālā.

### <a name="create-a-cross-channel-page-that-uses-cross-channel-content"></a>Starpkanālu lapas izveidošana, kurā tiek izmantots starpkanālu saturs

Starpkanālu lapas var izmantot jebkurā jūsu vietnes kanālā. Tādējādi varat vienreiz izveidot koplietojamu satura lapu un visus turpmākos atjauninājumus veikt vienuviet. Piemēram, starpkanālu lapa **Noteikumi un nosacījumi** , kuras URL ir `/toc`, var tikt koplietota starp visiem vietnes kanāliem. Ja vietnes kanāla bāzes URL `www.fabrikam.com/brand1` un `www.fabrikam.com/brand2` pieder vienam starpkanālam, kopīgotā lapa **Noteikumi un nosacījumi** būs attiecīgi pieejama gan vietnes kanāla URL `www.fabrikam.com/brand1/toc`, gan `www.fabrikam.com/brand2/toc`. Ja lapa **Noteikumi un nosacījumi** ir jāatjaunina vēlāk, atjauniniet tikai vienu koplietojamo lapu.

Lai izveidotu starpkanālu lapu Commerce vietņu veidotājā, kurā tiek izmantots starpkanālu saturs, veiciet tālāk norādītās darbības.

1. Dodieties uz **Lapas** un atlasiet **Jauns** , lai izveidotu jaunu lapu.
1. Dialoglodziņā **Izvēlēties veidni** atlasiet veidni **Mārketings**.
1. Laukā **Lapas nosaukums** ievadiet lapas nosaukumu (piemēram, **Starpkanālu lapa** ).
1. Sadaļā **Lapas URL** ievadiet lapas URL (piemēram, **examplepage** ) un pēc tam atlasiet **Labi**.
1. Jaunās lapas **Galvenajā** slotā atlasiet daudzpunkti ( **...** ) un pēc tam atlasiet **Pievienot fragmentu**.
1. Dialoglodziņā **Pievienot fragmentu** , atlasiet iepriekš izveidoto starpkanālu fragmentu ar veicināšanas reklāmkarogu, un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums** , lai priekšskatītu lapu. Jums vajadzētu redzēt veicināšanas reklāmkarogu ar tekstu “starpkanāls”.
1. Atlasiet **Pabeigt rediģēšanu** , lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt** , lai publicētu to.

### <a name="create-a-channel-specific-page-that-uses-cross-channel-content"></a>Kanālam raksturīgas lapas izveide, kurā tiek izmantots starpkanālu saturs

Izmantojot starpkanālu saturu kanālam raksturīgās lapās, varat vienreiz izveidot koplietojamā satura fragmentu un pēc tam to izmantot kanālam raksturīgās lapās. Šis “vienotais resurss” ir noderīgs koplietojamajam saturam, piemēram, noteikumiem un nosacījumiem, maksājuma nosacījumiem vai kontaktinformācijai.

Lai izveidotu kanālam raksturīgu lapu Commerce vietņu veidotājā, kurā tiek izmantots starpkanālu saturs, veiciet tālāk norādītās darbības.

1. Noteiktā kanālā, piemēram, **Fabrikam paplašinātais tiešsaistes veikals** dodieties uz **Lapas** un pēc tam atlasiet **Jauns** , lai izveidotu jaunu lapu.
1. Dialoglodziņā **Izvēlēties veidni** atlasiet veidni **Mārketings**.
1. Laukā **Lapas nosaukums** ievadiet lapas nosaukumu (piemēram, **Kanālam raksturīga lapa** ).
1. Sadaļā **Lapas URL** ievadiet lapas URL (piemēram, **channelspecificpage** ) un pēc tam atlasiet **Labi**.
1. Jaunās lapas **Galvenajā** slotā atlasiet daudzpunkti ( **...** ) un pēc tam atlasiet **Pievienot fragmentu**.
1. Dialoglodziņa **Pievienot fragmentu** sadaļā **Kanāls** , atlasiet **Starpkanālu tiešsaistes veikals**. Iepriekš izveidotajam starpkanāla fragmentam vajadzētu tikt parādītam sarakstā. Atlasiet to un pēc tam atlasiet **Labi**.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums** , lai priekšskatītu lapu. Jums vajadzētu redzēt veicināšanas reklāmkarogu ar tekstu “starpkanāls”.
1. Atlasiet **Pabeigt rediģēšanu** , lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt** , lai publicētu to.

### <a name="create-a-channel-specific-version-of-a-cross-channel-page"></a>Kanālam raksturīgas starpkanālu lapas versijas izveidošana

Starpkanālu koplietošana atbalsta starpkanālu satura pārlabošanu. Piemēram, visiem vietnes kanāliem, izņemot vienu, ir viens un tas pats saturs. Šim vienam vietnes kanālam ir nepieciešams atšķirīgs saturs. Lai tam ieviestu atšķirīgu saturu, tiek pārlabots starpkanālu saturs, izmantojot kanālam raksturīgu saturu, tādā veidā izveidojot kanālam raksturīgu starpkanālu lapas versiju.

Lai izveidotu kanālam raksturīgu starpkanālu lapas versiju Commerce vietņu veidotājā, veiciet tālāk norādītās darbības.

1. Lauka **Kanāls** augšējā labajā stūrī atlasiet **Starpkanālu tiešsaistes veikals**.
1. Atveriet iepriekš izveidoto starpkanālu lapu.
1. Lauka **Kanāls** augšējā labajā stūrī atlasiet kanālu, kam jābūt ar raksturīgu saturu. Lapas redaktors parāda ziņojumu ar aicinājumu izveidot jaunu lapas variantu.
1. Atlasiet **Izveidot lapas variantu**.
1. Lapas varianta **Galvenajā** slotā atlasiet daudzpunkti ( **...** ) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Veicināšanas reklāmkarogs** un pēc tam atlasiet **Labi**.
1. Moduļa **Veicināšanas reklāmkarogs** rekvizītu rūtī atlasiet **Pievienot ziņojumu** un pēc tam atlasiet **Ziņojums**.
1. Dialoglodziņa **Ziņojums** sadaļā **Teksts** ievadiet **Kanālam raksturīgs** un atlasiet **Labi**.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums** , lai priekšskatītu lapu. Jums vajadzētu redzēt veicināšanas reklāmkarogu ar tekstu “Kanālam raksturīgs”.
1. Atlasiet **Pabeigt rediģēšanu** , lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt** , lai publicētu to.

Tagad, izmantojot kanāla bāzes URL un dodoties uz šīs vietnes starpkanālu lapas URL, starpkanālu satura vietā redzēsit kanālam raksturīgo saturu.

## <a name="additional-resources"></a>Papildu resursi

[Satura pievienošanas veidi](add-manage-content.md)

[Lapas modeļa glosārijs](page-elements-overview.md)

[Dokumenta stāvokļi un dzīves cikls](document-states-overview.md)

[Darbs ar publicēšanas grupām](publish-groups.md)
