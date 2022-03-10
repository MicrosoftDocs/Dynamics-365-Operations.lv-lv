---
title: Starpuzņēmumu pārdošanas pasūtījumu ārējam debitoram izveide un rēķina izrakstīšana
description: Šajā tēmā skaidrots, kā izveidot starpuzņēmumu pārdošanas pasūtījumu un izrakstīt rēķinu ārējam debitoram
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: b5f7342a997407c8701b836c2a6a6222d8512121
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8074998"
---
# <a name="create-and-invoice-an-intercompany-sales-order-for-an-external-customer"></a>Starpuzņēmumu pārdošanas pasūtījumu ārējam debitoram izveide un rēķina izrakstīšana

[!include [banner](../../includes/banner.md)]

Starpuzņēmumu tirdzniecību var izmantot, lai reģistrētu preces pārdošanu no vienas juridiskās personas citai juridiskai personai tajā pašā organizācijā.

Veidojot oriģinālo pārdošanas pasūtījumu, var automātiski izveidot starpuzņēmumu pirkšanas pasūtījumu starpuzņēmumu kreditoram. Tā automātiski tiek izveidots starpuzņēmumu pārdošanas pasūtījums starpuzņēmumu kreditora juridiskā personā.

Šajā attēlā parādītas transakciju plūsmas, kad veidojat pārdošanas pasūtījumu ārējam debitoram, bet pirms preces var piegādāt klientam, preces ir jāpasūta no citas juridiskas personas jūsu organizācijā. Šajā gadījumā starpuzņēmumu pirkšanas pasūtījums tiek izveidots kreditora kontam, kas pārstāv citu juridisku personu. Savukārt, starpuzņēmumu pārdošanas pasūtījums tiek izveidots citā juridiskā personā debitora kontam, kas pārstāv jūsu juridisku personu. Ja notiek tiešā piegāde, izrakstot rēķinu starpuzņēmuma pirkuma pasūtījumam, sistēma automātiski grāmato rēķinu oriģinālajam pārdošanas pasūtījumam.

![Starpuzņēmumu ārējās pārdošanas process](media/intercompanyexternalsalesprocess.png)

Ja izmantojat tiešo piegādi un atlasāt **Pavadzīme** lauka **Skaits** lapā **Grāmatot rēķinu**, starpuzņēmumu kreditora rēķins ir balstīts uz starpuzņēmumu produktu ieejas plūsmu, kas tikusi iepriekš iegrāmatota.

## <a name="prerequisites"></a>Priekšnosacījumi

Lai varētu automātiski grāmatot un drukāt starpuzņēmumu rēķinus, pirms sākat, pārliecinieties, vai izpildās šādi priekšnosacījumi.

1. Dodieties uz **Pārdošana un mārketings \> Debitori \> Visi debitori**.
1. Darbību rūts cilnē **Vispārīgi** atlasiet **Starpuzņēmums**.
1. Pārejiet uz sadaļu **Sagāde un avoti \> Kreditori \> Visi kreditori**.
1. Darbību rūts cilnē **Vispārīgi** atlasiet **Starpuzņēmums**.
1. **Starpuzņēmumu** lapā par kreditoru vai debitoru **Pirkšanas pasūtījumu politikas**, apgabalā, kas atrodas lauku grupā **Starpuzņēmumu pirkšanas pasūtījums (tiešā piegāde)**, atlasiet **Grāmatot rēķinu automātiski**.
1. Apgabalā **Pirkšanas pasūtījumu politikas**, lauku grupā **Starpuzņēmumu pirkšanas pasūtījums (tiešā piegāde)** atlasiet izvēles rūtiņu **Grāmatot rēķinu automātiski**. Atzīmējiet šo izvēles rūtiņu, ja vēlaties, lai rēķins par sākotnējo pārdošanas pasūtījumu tiktu automātiski drukāts, grāmatojot starpuzņēmumu kreditoru rēķinu.

> [!NOTE]
> Drukas iestatījumus rēķinam nosaka iestatījumi modulī, dokumentā vai transakcijā **Drukas pārvaldības iestatījumu** lapā.

## <a name="create-an-original-sales-order-for-an-external-customer"></a>Sākotnējo pārdošanas pasūtījumu izveide ārējam debitoram

Izpildiet šīs darbības juridiskajā personā A. Šī procedūra atbilst 1. lodziņam ilustrācijā.

1. Doties uz **Debitoru parādi \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Saraksta lapā **Visi pārdošanas pasūtījumi** izveidojiet sākotnējo pārdošanas pasūtījumu. Lauku vērtības tiek kopētas no debitora konta uz pārdošanas pasūtījumu.
1. Lapā **Pārdošanas pasūtījumi** Darbību rūtī atlasiet **Galvenes skats**.
1. Kopsavilkuma cilnē **Starpuzņēmumu iestatījumi** atzīmējiet izvēles rūtiņu **Automātiski izveidot starpuzņēmumu pasūtījumus**.
1. Ja starpuzņēmumu kreditoram krājums ir jāpiegādā tieši ārējam debitoram, atzīmējiet izvēles rūtiņu **Tiešā piegāde**.
1. Kad esat beidzis ievadīt pārdošanas pasūtījumu, aizveriet lapu **Pārdošanas pasūtījums**.

Starpuzņēmumu pirkšanas pasūtījums tiek automātiski izveidots visiem krājumiem, kuriem ir piešķirts starpuzņēmumu kreditors, un pēc tam tiek izveidots starpuzņēmumu pārdošanas pasūtījums. Informatīvs ziņojums pavēsta, ka starpuzņēmumu pirkšanas pasūtījums un starpuzņēmumu pārdošanas pasūtījums ir izveidots. Ziņojums satur arī saites uz šiem pasūtījumiem. Ja krājums nav atrasts, tiek parādīts sarkans brīdinājums, kas nozīmē, ka pasūtījuma izveides process nav pabeigts.

> [!NOTE]
> Ja veidojat vairākus pasūtījumus dažādās juridiskās personās un vienā no juridiskām personām krājumi netika atrasti, pasūtījuma izveides process tiek pārtraukts pat tām juridiskām personām, kas varēja izpildīt savus pasūtījumus.

## <a name="invoice-an-intercompany-sales-order"></a>Starpuzņēmumu pārdošanas pasūtījuma iekļaušana rēķinā

Izrakstot rēķinu starpuzņēmumu pārdošanas pasūtījumam, korespondējošais starpuzņēmumu pirkšanas pasūtījums tiek iekļauts rēķinā automātiski. Tad, ja sākotnējais pārdošanas pasūtījums ir tiešās piegādes pasūtījums, sākotnējais pārdošanas pasūtījums tiek automātiski iekļauts rēķinā.

Izpildiet šīs darbības juridiskajā personā B. Šī procedūra atbilst 2. lodziņam ilustrācijā.

1. Doties uz **Debitoru parādi \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Atgriezieties lapā **Visi pārdošanas pasūtījumi** un vēlreiz atlasiet starpuzņēmumu pārdošanas pasūtījumu.
1. Darbības rūtī atlasiet cilni **Rēķins** un pēc tam vēlreiz atlasiet **Rēķins**.
1. Atzīmējiet izvēles rūtiņu **Grāmatot**.
1. Atlasiet pārdošanas pasūtījumu un pēc tam noklikšķiniet uz **Labi**.

Debitora rēķins starpuzņēmumu pārdošanas pasūtījumam tiek automātiski iegrāmatots juridiskajai personai B. Pēc tam, starpuzņēmumu kreditora rēķins tiek automātiski izveidots un iegrāmatots juridiskajā personā B. Ja sākotnējais pārdošanas pasūtījums ir iestatīts kā tiešā piegāde, debitora rēķins tiek izveidots sākotnējam pārdošanas pasūtījumam juridiskajā personā A.

> [!NOTE]
> Iepriekš starpuzņēmumu pārdošanas scenārijos, ja piegādātāja rēķina darbplūsma bija konfigurēta starpuzņēmumu pirkšanas uzņēmumā, starpuzņēmumu pārdošanas pasūtījumu nevarēja sekmīgi izrakstīt. Tāpēc starpuzņēmumu iepirkumu uzņēmumam bija jāizslēdz pārdevēja rēķinu darbplūsma. 
> 
> Šis ierobežojums ir novērsts, izmantojot neseno līdzekli 10.0.25. Par starpuzņēmumu pārdošanas pasūtījumiem tagad var izrakstīt rēķinus, kad starpuzņēmumu pirkšanas uzņēmumā ir konfigurēta piegādātāja rēķinu darbplūsma.
> 
> Lai iespējotu šo funkciju, veiciet šīs darbības.
>
> 1. Izvēlieties starpuzņēmumu pārdošanas juridisko personu.  
> 2. Dodieties uz **Debitoru parādi \> Debitori \> Visi debitori**.
> 3. Izvēlieties klientu starpuzņēmumu iepirkumu uzņēmumam.
> 4. Iet uz **Ģenerālis \> Uzstādīt \> Starpuzņēmums**.
> 5. Uz **Pirkuma pasūtījumu politikas** cilnē atlasiet **Apiet piegādātāja rēķinu darbplūsmu starpuzņēmumu piegādātāju rēķiniem** parametrs.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
