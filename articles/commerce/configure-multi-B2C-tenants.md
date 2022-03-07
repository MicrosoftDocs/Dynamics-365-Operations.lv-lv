---
title: Konfigurēt vairākus B2C nomniekus Commerce vidē
description: Šajā tēmā aprakstīts, kad un kā iestatīt vairākus katra kanāla Microsoft Azure Active Directory (Azure AD) biznesa-patērētāja (B2C) nomniekus lietotāja autentifikācijai īpašā Dynamics 365 Commerce vidē.
author: BrianShook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-12
ms.dyn365.ops.version: ''
ms.openlocfilehash: a372561b8a6cdca8e1a3dc362009379884f1a3414330f3f056d4c3af7703a132
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736408"
---
# <a name="configure-multiple-b2c-tenants-in-a-commerce-environment"></a>Konfigurēt vairākus B2C nomniekus Commerce vidē

[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīts, kad un kā iestatīt vairākus katra kanāla Microsoft Azure Active Directory (Azure AD) biznesa-patērētāja (B2C) nomniekus lietotāja autentifikācijai īpašā Dynamics 365 Commerce vidē.

Dynamics 365 Commerce izmanto Azure AD B2C mākoņa identitātes pakalpojumu, lai atbalstītu lietotāja akreditācijas datus un autentifikācijas plūsmas. Lietotāji var izmantot autentifikācijas plūsmas, lai pieteiktos, pierakstītos un atjaunotu savu paroli. Azure AD B2C saglabā lietotāja sensitīvo autentifikācijas informāciju, piemēram, lietotāja vārdu un paroli. Lietotāja ieraksts ir unikāls katram B2C nomniekam, un tas izmanto vai nu lietotājvārda (e-pasta adreses) akreditācijas datus vai sociālās identitātes nodrošinātāja akreditācijas datus.

Vairākumā gadījumu Commerce vidē tiek izmantots viens Azure AD B2C nomnieks. Commerce klienti pēc tam var izveidot un publicēt vairākas vietas vienā un tajā pašā Commerce vidē, un šajos portālos tiks izmantoti vieni un tie paši klienta akreditācijas dati. Tomēr, ja vides vietas ir jāuzskata par dažādiem zīmoliem un lietotājiem tās tiek rādītas kā atsevišķi uzņēmumi, var konfigurēt B2C nomnieku šim kanālam, kas tiek izmantots vietas/zīmola nodalīšanai.

## <a name="considerations-when-multiple-b2c-tenants-are-set-up-per-channel"></a>Apsvērumi, kad katram kanālam tiek iestatīti vairāki B2C nomnieki

Bieži vien, kad katrs kanāls vai vieta tiek uzskatīts par atsevišķu biznesu, vislabākā opcija attiecībā uz lietotāja autentifikācijas plūsmām programmā Commerce ir izmantot atsevišķas juridiskās personas. Tomēr, ja vēlaties saglabāt katru kanālu/vietu tajā pašā vidē un juridiskajā personā, bet vēlaties katrai vietai izveidot atsevišķu lietotāja autentifikāciju, pirms turpināt, ir svarīgi ņemt vērā šādus punktus:

- Lietotājiem būs savi atsevišķi akreditācijas dati katram kanālam/vietai.

    Vienai personai var būt divi atsevišķi konti katram kanālam/vietai, jo katrs konts būs unikāls ieraksts atsevišķā B2C nomniekā.

- Microsoft Dynamics vidē atsevišķi debitoru ieraksti tiks atgriezti globālajā ierakstu meklēšanā.

    Ja lietotājs izmanto vienu un to pašu e-pasta adresi kanālos/vietās, globālās klientu meklēšanas rezultāts atgriezīs katra kanāla/vietas rezultātus. (Tiks parādīts kanāla indikators.)

- Var izmantot adrešu grāmatu, lai palīdzētu grupas lietotājiem būs izsekojamiem katrā kanālā.
- Var palielināties katra kanāla klientu ierakstu skaits, un šis pieaugums var ietekmēt globālo klientu meklējumu veiktspēju.
- B2C nomniekiem ir jābūt rūpīgi kartētiem kanālā, lai palīdzētu novērst situācijas, kad klienti pierakstās nepareizam nomniekam. Pretējā gadījumā var rasties apjukums vai izsekošanas problēmas.

Šajā attēlā redzami vairāki B2C nomnieki Commerce vidē.

![Vairāki B2C nomnieki Commerce vidē.](media/MultiB2C_In_Environment.png)

Ja izlemjat, ka jūsu uzņēmumam ir nepieciešams atsevišķs B2C nomnieks vienam kanālam vienā un tajā pašā Commerce vidē, izpildiet tālāk norādītās darbības, lai pieprasītu šo līdzekli.

## <a name="configure-b2c-tenants-in-your-environment"></a>Konfigurēt B2C nomniekus jūsu vidē

Lai konfigurētu B2C nomniekus savā vidē, veiciet atbilstošās procedūras, kas aprakstītas šajā sadaļā.

### <a name="add-an-azure-ad-b2c-tenant"></a>Pievienot Azure AD B2C nomnieku

Lai savai videi pievienotu Azure AD B2C nomnieku, veiciet tālāk norādītās darbības.

1. Piesakieties Commerce vietas veidotājam savai videi kā sistēmas administrators. Lai konfigurētu Azure AD B2C nomniekus, jums ir jābūt Commerce vides sistēmas administratoram.
1. Kreisās puses navigācijas rūtī atlasiet **Nomnieka iestatījumi**, lai to izvērstu.
1. Atlasiet **B2C iestatījumi** un pēc tam atlasiet **Pārvaldīt**.
1. Atlasiet **Pievienot B2C programmu**, un pēc tam ievadiet šādu informāciju.

    - **Programmas nosaukums**: ievadiet nosaukumu, kas jālieto programmai saistībā ar tās pārvaldīšanu pakalpojumā Commerce. Ieteicams izmantot programmas nosaukumu, ko izvēlējāties, iestatot Azure AD B2C lietojumprogrammu Azure portālā. Šādā veidā jūs varat palīdzēt mazināt apjukumu, kad pakalpojumā Commerce tiek pārvaldīti B2C nomnieki.
    - **Nomnieka nosaukums**: ievadiet B2C nomnieka nosaukumu, kāds tas parādās Azure portālā.
    - **Aizmirstas paroles politikas ID**: ievadiet politikas ID (politikas nosaukumu Azure portālā).
    - **Pieteikšanās Pierakstīšanās politikas ID**: ievadiet politikas ID (politikas nosaukumu Azure portālā).
    - **Klienta GUID**: ievadiet Azure AD B2C nomnieka ID, kāds tas parādās Azure portālā (nevis programmas ID B2C nomniekam).
    - **Rediģēt profila politikas ID**: ievadiet politikas ID (politikas nosaukumu Azure portālā).

1. Kad esat pabeidzis šīs informācijas ievadīšanu, atlasiet **Labi**, lai saglabātu veiktās izmaiņas. Jūsu jaunajam Azure AD B2C nomniekam tagad ir jāparādās sarakstā sadaļā **Pārvaldīt B2C programmas**.

> [!NOTE]
> Jums ir jāatstāj tādi lauki kā, piemēram, **Tvērums**, **Neinteraktīvas politikas ID**, **Neinteraktīva klienta ID**, **Pieteikšanās pielāgots domēns** un **Pieteikšanās politikas ID** tukši, ja vien Dynamics 365 Commerce grupa jums nesniedz norādījumus to iestatīšanai.


### <a name="manage-or-delete-an-azure-ad-b2c-tenant"></a>Azure AD B2C nomnieka pārvaldīšana vai dzēšana

1. Piesakieties Commerce vietas veidotājam savai videi kā sistēmas administrators. Lai konfigurētu Azure AD B2C nomniekus, jums ir jābūt Commerce vides sistēmas administratoram.
1. Kreisās puses navigācijas rūtī atlasiet **Nomnieka iestatījumi**, lai to izvērstu.
1. Atlasiet **B2C iestatījumi** un pēc tam atlasiet **Pārvaldīt**.
1. Lai labotu B2C nomnieku, blakus tam atlasiet zīmuļa simbolu. Lai dzēstu B2C nomnieku, atlasiet atkritnes simbolu tam blakus.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Publicēt**, lai aktivizētu izmaiņas.

> [!WARNING]
> Kad B2C nomnieks ir konfigurēts dzīvai/publicētai vietai, lietotāji, iespējams, ir reģistrējušies, izmantojot kontu, kas ir nomniekā. Ja izdzēšat konfigurētu nomnieku izvēlnē **Nomnieka iestatījumi \> B2C nomnieks**, jūs noņemat šī B2C nomnieka saistību no vietām, kas ir saistītas ar jebkuru nomnieka kanālu. Šādā gadījumā lietotāji, iespējams, vairs nevarēs pieteikties savos kontos. Tāpēc, dzēšot konfigurēto nomnieku, esiet ļoti piesardzīgi.
>
> Kad konfigurētais nomnieks tiek dzēsts, B2C nomnieks un ieraksti joprojām tiks uzturēti, bet šī nomnieka Commerce sistēmas konfigurācija tiks mainīta vai noņemta. Lietotāji, kuri mēģina pierakstīties vai pieteikties vietā, izveidos jaunu konta ierakstu noklusējuma vai nesen saistītajā B2C nomniekā, kas ir konfigurēts vietas kanālam.

## <a name="configure-your-channel-with-a-b2c-tenant"></a>Konfigurējiet savu kanālu ar B2C nomnieku

1. Piesakieties Commerce vietas veidotājam savai videi kā sistēmas administrators. Lai konfigurētu Azure AD B2C nomniekus, jums ir jābūt Commerce vides sistēmas administratoram.
1. Kreisās puses navigācijas rūtī atlasiet **Vietnes iestatījumi**, lai to izvērstu.
1. Atlasiet **Kanāli** un pēc tam atlasiet kanālu, ko konfigurēt.
1. Rekvizītu rūts labajā pusē, laukā **Atlasiet B2C pieteikumu** atlasiet konfigurēto Azure AD B2C nomnieku, ko izmantot šim kanālam.
1. Komandjoslā atlasiet **Saglabāt un publicēt**, lai iesniegtu jauno vai atjaunināto konfigurāciju.

> [!WARNING]
> Ja mainīsit šai stacijai piešķirto B2C programmu, noņemiet pašreizējās atsauces, kas izveidotas visiem lietotājiem, kuri jau ir pieteikušies vidē. Šādā gadījumā visi akreditācijas dati, kas ir saistīti ar pašlaik piešķirto B2C programmu, lietotājiem nebūs pieejami. Tāpēc mainiet kanāla Azure AD B2C konfigurāciju tikai tad, ja pirmo reizi iestatāt kanālu, un neviens lietotājs nevarēja pieteikties. Pretējā gadījumā lietotājiem, iespējams, būs vēlreiz jāpierakstās, lai izveidotu jaunu Azure AD B2C nomnieka ierakstu.
## <a name="additional-resources"></a>Papildu resursi

[Domēna nosaukuma konfigurēšana](configure-your-domain-name.md)

[Jauna e-tirdzniecības nomnieka izvietošana](deploy-ecommerce-site.md)

[E-komercijas vietnes izveide](create-ecommerce-site.md)

[Vietnes Dynamics 365 Commerce saistīšana ar tiešsaistes kanālu](associate-site-online-store.md)

[Failu robots.txt pārvaldība](manage-robots-txt-files.md)

[Novirzīšanas URL lielapjoma augšupielāde](upload-bulk-redirects.md)

[B2C nomnieka iestatīšana programmā Commerce](set-up-B2C-tenant.md)

[Pielāgotu lapu iestatīšana lietotāja pieteikumiem](custom-pages-user-logins.md)

[Atbalsta pievienošana satura piegādes tīklam (CDN)](add-cdn-support.md)

[Veikala noteikšanas iespējošana pēc atrašanās vietas](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
