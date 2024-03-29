---
title: Lapas vietrāža URL izveide
description: Šajā rakstā ir ietvertas pamata koncepcijas un procedūras lapas URL izveidošanai jūsu vietnē.
author: bicyclingfool
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 8718a3a2854ecdc7aec0853569dcba9e26a86d67
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270159"
---
# <a name="create-a-page-url"></a>Lapas vietrāža URL izveide

[!include [banner](includes/banner.md)]

Šajā rakstā ir ietvertas pamata koncepcijas un procedūras lapas URL izveidošanai jūsu vietnē.

Pilns vai absolūts vietrādis URL, kas norāda uz jūsu vietnes lapu, sastāv no atšķirīgām daļām. Piemēram, vietrādim URL `https://www.contoso.com/en-us/contactus` ir šādas daļas.

- `https://www.contoso.com`– HTTP protokols un vietnes domēns.
- `/en-us`– vietnes valodas ceļš.
- `/contactus`– relatīvais URL lapai **Sazinieties ar mums**. Relatīvais URL, ko sauc arī par URL *rindu*.

Iestatot vietni, jūs izveidojat savas vietnes domēnu un izvēles valodas ceļu. Savai vietnei varat pievienot vairāk domēnu un valodu ceļu, izmantojot tiešsaistes veikalus vietnes iestatījumos.

Lapas URL rinda pastāv kā savrupa entītija vietnes autorēšanas vidē. Lapas vietrādis URL sastāv no divām daļām: nosaukuma, kas apzīmē URL rindu, un norādes uz lapu vai nu jūsu vietnē, vai ārējā vietnē. Lapas vietrādi URL var arī konfigurēt tā, lai tas darbotos kā novirzīšanas vietrādis uz citu lapu vai nu jūsu vietnē, vai ārējā vietnē.

## <a name="create-a-page-url"></a>Lapas vietrāža URL izveide

Ir divi veidi, kā izveidot lapu vietrāžus URL.

- Automātiski, veidojot lapu
- Manuāli, no **vietrāžu URL** lapas

### <a name="create-a-page-url-when-you-create-a-page"></a>Lapas vietrāža URL izveide, veidojot lapu

Veidojot jaunu lapu un **URL** laukā norādot nosaukumu, lapas vietrādis URL, kas norāda uz šo lapu, tiek automātiski izveidots **URL** lapā. Pēc tam, kad publicējāt vietrādi URL un lapu, uz ko tas norāda, vietnes lietotāji (jūsu klienti) var piekļūt ar vietrādi URL saistītajai lapai.

> [!NOTE]
> Ja publicējat vietrādi URL, nepublicējot lapu, uz kuru tas norāda, tad vietnes lietotāji, mēģinot piekļūt lapai, saņem kļūdu 404. Ja publicējat lapu, nepublicējot vietrādi URL, kas norāda uz to, lapai nevar piekļūt, izmantojot vietrādi URL.

### <a name="manually-create-a-page-url"></a>Lapas vietrāža URL manuālā izveide

Veidojot jaunas lapas, nav nepieciešams norādīt lapas vietrādi URL. Ja vietrāža URL lauks tiek atstāts tukšs, tad lapa tiek izveidota nesaistītā stāvoklī. Šādā gadījumā klienti nevarēs piekļūt lapai, pat ja tā ir publicēta. Lai padarītu lapu pieejamu, ir manuāli jāizveido vietrādis URL un tas ir jāsaista ar lapu.

Lai manuāli izveidotu lapas vietrādi URL, veiciet šādas darbības.

1. Lapā **Vietrāži URL** atlasiet **Jauns**.
1. Izvēlieties vietnes lapu, kuru saistīt ar vietrādi URL.
1. Ievadiet URL rindu un pēc tam atlasiet **Labi**.

Šajā brīdī URL ir melnraksta statusā. Tas ir jāpublicē, pirms vietnes lietotāji var piekļūt saistītajai lapai.

## <a name="update-a-page-url"></a>Lapas vietrāža URL atjaunināšana

Lai atjauninātu lapas URL mērķa lapu, veiciet šādas darbības.

1. Lapā **Vietrāži URL** atlasiet vietrādi URL atjaunināšanai.
1. Rekvizītu rūtī labajā pusē atlasiet daudzpunktes pogu (**...**) blakus mērķa lapas laukam.
1. Dialoglodziņā atlasiet citu lapu un pēc tam atlasiet **Labi**.
1. Saglabājiet un publicējiet vietrādi URL.

## <a name="redirect-a-page-url"></a>Lapas vietrāža URL novirzīšana

Dažreiz, iespējams, vēlēsieties, lai klienti redzētu citu lapu, kad viņi pieprasa specifisku vietrādi URL. Šādos gadījumos bieži vislabākā un vienkāršākā metode ir mainīt lapu, uz kuru norāda lapas vietrādis URL. Tomēr jums, iespējams, ir likumīgi iemesli izmantot HTTP 301 vai 3023 pārvirzīšanu, lai novirzītu pieprasījumus uz citu vietrādi URL.

Lai novirzītu vietrādi URL uz citu vietrādi URL, rīkojieties šādi.

1. Lapā **Vietrāži URL** atlasiet vietrādi URL atjaunināšanai.
1. Rekvizītu rūts labajā pusē atlasiet rekvizītu **Novirzīšana**.
1. Novirzīšanai atlasiet galamērķi.

    - Lai norādītu uz citu jūsu vietnes lapu, atlasiet **Iekšējais vietrādis URL**, atlasiet daudzpunktes pogu **(...**) un pēc tam atlasiet vietrādi URL, uz kuru veikt novirzīšanu.
    - Lai norādītu uz lapu ārējā vietnē, atlasiet **Ārējais vietrādis URL** un pēc tam ievadiet pilnu vietrādi URL šai lapai. Noteikti iekļaujiet protokolu. Piemēram, ievadiet `https://domain.com/new/page`. Ja vietrādis URL jau novirza uz iekšējo vietrādi URL, jums ir jāatlasa **Noņemt atlasi** pirms varat ieiet ārējā vietrādī URL.

1. Novirzīšanas tipa izvēle.

    - **Pastāvīga novirzīšana** (301) — atlasiet šo opciju, ja zināt, ka saturs tiek pārvietots uz visiem laikiem, un tas netiks atgriezts tā iepriekšējā vietrādī URL. Meklētājprogrammas piešķirs novirzošā vietrāža URL meklētājprogrammas optimizācijas (SEO) vērtību vietrādim, uz kuru notiek novirzīšana, un atjauninās savu ierakstu, lai parādītu jauno vietrādi URL. 
    - **Pagaidu novirzīšana (302)** — atlasiet šo opciju, lai novirzītu datplūsmu, neatjauninot meklētājprogrammas. Šo pieeju parasti izmanto, ja saturs drīz atgriezīsies uz iepriekšējo vietrādi URL.

1. Kad esat gatavs ieviest novirzīšanu, saglabājiet un publicējiet vietrādi URL.

## <a name="additional-resources"></a>Papildu resursi

[Vietnes navigācijas pielāgošana](customize-site-navigation.md)

[Jaunas vietnes lapas pievienošana](add-new-page.md)

[Domēna nosaukuma konfigurēšana](configure-your-domain-name.md)

[Valodu pievienošana vietnei](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
