---
title: Store Commerce programma mobilajām platformām
description: Šajā rakstā ir aprakstīts, kā sākt darbu, izmantojot Microsoft Dynamics 365 Commerce programmu Store Commerce for un Android iOS.
author: stuharg
ms.date: 11/30/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2018-10-29
ms.openlocfilehash: dc952698a2a3301aff312e8310c58cbbb9cfe290
ms.sourcegitcommit: 2804b05214c87f76457608b5db072582ff339852
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/01/2022
ms.locfileid: "9815788"
---
# <a name="store-commerce-app-for-mobile-platforms"></a>Store Commerce programma mobilajām platformām

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Šajā rakstā ir aprakstīts, kā sākt darbu, izmantojot Microsoft Dynamics 365 Commerce Store Commerce programmas un Android iOS.

Mobilās Dynamics 365 Commerce lietojumprogrammas Android darbam ar iOS un tās ļauj jums nekavējoties un vienkārši izvietot pilnas lietojumprogrammas pārdošanas punkta (POS) ierīces. Store Commerce mobilās programmas [nodrošina jums visas Programmas Store Commerce for Windows iespējas un plašu klāstu, kā arī tas sniedz plašu iOS](store-commerce.md) Android  un tālruņu klāstu. Store Commerce mobilās programmas var tikt instalētas tieši no Pirkšanas un lietojumprogrammu veikaliem, un tām nav nepieciešams izstrādātājs, lai izveidotu jaunu programmu pakotni, ko izvietot vai atjaunināt. 

Store Commerce mobilās programmas saglabā pilnu funkcionālo paramiju ar pašreizējām mazumtirdzniecības programmu lietojumprogrammām. Turklāt programma Store Commerce for iOS ietver atbalstu atvēlētai aparatūras stacijai, lai iOS ierīces varētu sazināties ar tīkla maksājumu termināļiem, kvīšu printeriem un naudas kasieriem, neprasot koplietotas aparatūras stacijas izvietošanu. 

> [!IMPORTANT]
> Store Commerce programmas operētājsistēmai Windows un Android  iOS ir nākamās ģenerēšanas POS programmas Dynamics 365 Commerce. Store Commerce lietojumprogrammas piedāvā vairākus uzlabojumus salīdzinājumā ar pirmstecīgām funkcijām, saglabājot pilnu funkcionalitāti un līdzekļu paritāti. Korporācija Microsoft novecos MPOS Android un iOS Retail POS aparatūras programmas 2023. gada beigās, un iesaka visām jaunajām POS izvietošanām izmantot Store Commerce vai Cloud POS (CPOS). Esošajiem debitoriem ir jāplāno migrēt no Retail commerce programmām uz Store Commerce. Papildinformāciju skatiet sadaļā Modern [POS migrēšana uz Store Commerce](pos-extension/migrate-mpos-store-commerce.md). 

## <a name="app-architecture"></a>Programmas arhitektūra

Store Commerce mobilās programmas izmanto to pašu topoloģiju, kas ir programmai Store Commerce operētājsistēmai Windows, ja šī programma ir izvietota režīmā Telefoni. Store Commerce mobilās programmas ir čaulas programmas, kas renderē CPOS tieši no Commerce Scale Unit (CSU) un savienosies ar bez headless Commerce un Commerce galveno biroju, izmantojot CSU. Shell programmas modelis ļauj Store Commerce programmām atbalstīt atvēlētu aparatūras staciju tiešai integrācijai ar maksājumu termināli, printeri, naudas kasti un citām perifērijas ierīcēm. Nav jāiestata koplietojama aparatūras stacija, lai lietotu aparatūras ierīces. 

Lai atjauninātu Store Commerce mobilo programmu, vienkārši atjauniniet CSU. Visas jaunās POS funkcijas un funkcijas automātiski tiks paņemtas no programmas. Papildinformāciju par to, kā atjaunināt CSU, skatiet sadaļā [Lietot atjauninājumus un paplašinājumus Commerce Scale Unit (mākonī).](../../fin-ops-core/dev-itpro/deployment/update-retail-channel.md)

Shell programmas tiek apkalpotas, izmantojot programmu veikala atjauninājumus. Kad papildversija sasniedz vispārējo pieejamību (GA), Microsoft to publicēs programmu veikalos. Korporācija Microsoft var publicēt arī ielāpus starp papildversija atjauninājumiem, lai izlaistu augstas prioritātes kļūdu labojumus.

## <a name="prerequisites"></a>Priekšnosacījumi

Store Commerce mobilajām programmām ir nepieciešami Dynamics 365 Commerce it īpaši Commerce Headquarters un CSU komponenti. Šajā tabulā uzskaitītas minimālās operētājsistēmas (OS) un CSU versijas, kas nepieciešamas no Android iOS mobilajām programmām. 

| Priekšnoteikumi | Android      | iOS  |
| ------------ | ------------ | ---- |
| OS versija   | 7.0          | 15.0 |
| CSU versija  | 9.38.22266.8 | Tiks noteikts  |

## <a name="install-the-app"></a>Programmas instalēšana

Varat instalēt Store Commerce mobilās programmas tieši no Esat uzstādījumi veikala vaiInstalēt programmas veikala. 

- [Store Commerce programma priekš Android](https://aka.ms/storecommerceandroid)
- [Store Commerce programma, kas paredzēts iOS](https://aka.ms/storecommerceios)

 Android Lietojumprogrammas (.maks) un Lync programmas (.ipa) pakotnes var lejupielādēt arī no koplietojamās Microsoft Dynamics līdzekļu bibliotēkas pakalpojumos Lifecycle Services. 

## <a name="device-and-register-setup"></a>Ierīces un reģistra iestatīšana

Lai kases sistēmu varētu aktivizēt mobilajās lietojumprogrammās Store Commerce, programmā Commerce Headquarters ir jāiestata ierīce un reģistrs. Papildinformāciju skatiet sadaļā [Ierīces un reģistri](../implementation-considerations-devices.md). 

### <a name="device-setup"></a>Ierīces iestatīšana

Lai izveidotu un iestatītu jaunu ierīci, veiciet šādus soļus.

1. Programmā Commerce Headquarters pārejiet uz sadaļu **Retail un Commerce Channel \> Setup \> POS iestatīšanas \> ierīces**. 
1. Izveidojiet jaunu ierīci un **atkarībā no izmantotās mobilās programmas atlasiet Modern POS Android**  **vai Modern POS — iOS** kā programmas veidu. 

    > [!NOTE] 
    > Modern **POS -un Android**  **Modern POS - iOS** programmas tipi tiek izmantoti arī, lai izvietotu pašreizējās šīs sistēmas programmas un Android iOS. Pēc MPOS nolietojuma šo lietojumprogrammu **tipu etiķetes tiks atjauninātas uz Store Commerce - Android**  un **Modern POS - iOS**. 

### <a name="register-setup"></a>Reģistra iestatīšana

Varat izveidot jaunu kases reģistru un saistīt to ar izveidoto ierīci vai saistīt esošo kases reģistru ar jauno ierīci. Papildinformāciju par reģistriem skatiet sadaļā [Kases sistēmu izveide un saistīšana](../tasks/create-associate-registers.md).

### <a name="screen-layout-setup"></a>Ekrāna izkārtojuma iestatīšana

Ja jūs atkārtoti atpirksiet ekrāna izkārtojumu, kas ir ietverts demonstrācijas datos, kas tiek nodrošināti jūsu licencē, Store Commerce programma automātiski atlasīs Dynamics 365 Commerce iekļauto izkārtojumu, ja ierīces ekrāna izšķirtspēja ir mazāka par 480 &times; 853 pikseļiem portretorientācijā. Tomēr, ja veidojat ekrāna izkārtojumu no jauna vai ja mobilā ierīce izmanto lielāku izšķirtspēju nekā ekrānatspēka izkārtojumu, izveidojiet izšķirtspēju un saistītās pogu rindas, kas piemērotas tālruņam vai planšetdatoram, kurā plānojat izvietot. Papildinformāciju par ekrāna izkārtojuma konfigurācijām skatiet [POS lietotāja interfeisa vizuālajās konfigurācijās](../pos-screen-layouts.md). 

Kad ierīces un reģistri ir konfigurēti programmā Commerce headquarters, **pārejiet uz sadaļu Mazumtirdzniecība un Commerce \> Retail un Commerce ID \> sadales** grafiki un palaidiet kases sistēmu darbu.

## <a name="activate-a-device"></a>Ierīces aktivizēšana

Lai aktivizētu ierīci store Commerce mobilajā programmā, izpildiet šīs darbības.

1. Atveriet programmu mobilajā ierīcē.
1. Ievadiet CPOS VIETRĀDI URL, kuru varat atrast vides informācijas lapā sadaļā Lifecycle Services, **vai** programmas Commerce Headquarters kanāla profilu lapā (**Retail un Commerce Channel \> setup \> Channel profiles**).
1. Piesakieties, izmantojot tā darbinieka akreditācijas datus, kam ir atļauja pārvaldīt ierīces.
1. Atlasiet veikalu, kas ir saistīts ar programmu Commerce Headquarters izveidoto vai atkārtoti lietoto kases reģistru.
1. Atlasiet reģistru, ko esat saistījuši ar programmu Commerce Headquarters izveidoto ierīci.
1. Jūsu ierīce ir jāaktivizē. Varat pieteikties kases sistēmā, izmantojot atlasītā darbinieka operatora ID un paroli. 

Papildinformāciju par ierīces aktivizāciju skatiet [pārdošanas punkta (POS) ierīces aktivizāciju](retail-device-activation.md#activate-a-modern-pos-or-cloud-pos-device-by-using-guided-activation).

## <a name="feature-parity-with-store-commerce-for-windows"></a>Līdzekļu pārība ar Store Commerce operētājsistēmai Windows

Šajā tabulā ir salīdzinātas store Commerce programmas iespējas operētājsistēmā Windows Android un iOS platformās.

| Līdzeklis                                                                               | Windows | Android | iOS |
| ------------------------------------------------------------------------------------- | ------- | ------- | --- |
| Atvēlēta aparatūras stacija                                                            | Jā     | Jā     | Jā |
| Koplietojamā aparatūras stacija                                                               | Jā     | Jā     | Jā |
| Sakari ar tīkla perifērijas ierīcēm (maksājumu terminālis, printeris un naudas kasti) | Jā     | Jā     | Jā |
| OLE pārdošanas punkta (OPOS) perifērijas ierīcēm, izmantojot vietējo aparatūras staciju             | Jā     | Nē      | Nē  |
| Bezsaistes režīms                                                                          | Jā     | Nē      | Nē  |

## <a name="additional-resources"></a>Papildu resursi

[Store Commerce programma](store-commerce.md)

[Izvēle starp Store Commerce un Cloud POS](../mpos-or-cpos.md)

[Traucējummeklēšanu veikala Commerce iestatīšanas un instalēšanas problēmas](../troubleshoot/store-commerce-setup-installation.md)
