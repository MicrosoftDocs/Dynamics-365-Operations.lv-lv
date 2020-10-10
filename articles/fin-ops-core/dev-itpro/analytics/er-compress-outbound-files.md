---
title: Elektroniskajos pārskatos ģenerētu dokumentu saspiešana
description: Šajā tēmā ir paskaidrots, kā saspiest lielus dokumentus, kas tiek ģenerēti, izmantojot elektronisko pārskatu (ER) formātu.
author: NickSelin
manager: kfend
ms.date: 09/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner, ERFormatDestinationTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: ef024185c4654804f6f260a43c1bf294b33c10e2
ms.sourcegitcommit: 6e290b0d3aeedd0e234ac4f1df92b1b9afd6fccc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/22/2020
ms.locfileid: "3829683"
---
# <a name="compress-large-documents-that-are-generated-in-electronic-reporting"></a>Elektroniskajos pārskatos ģenerētu dokumentu saspiešana 

[!include [banner](../includes/banner.md)]

Varat izmantot [elektronisko pārskatu (ER) veidošanas struktūru](general-electronic-reporting.md), lai konfigurētu risinājumu, kas ienes transakciju datus, lai ģenerētu izejošo dokumentu. Ģenerētais dokuments var būt diezgan liels. Ģenerējot šī veida dokumentu, tiek izmantota [Lietojumprogrammas objektu servera (AOS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/access-instances#location-of-packages-source-code-and-other-aos-configurations) atmiņa, lai to uzglabātu. Kādā brīdī pēc tam dokuments ir jālejupielādē no Microsoft Dynamics 365 Finance programmas. Pašlaik maksimālais viena elektroniskā pārskata ģenerēta dokumenta lielums ir ierobežots līdz 2 gigabaitiem (GB). Savukārt, Finance pašlaik [ierobežo](https://fix.lcs.dynamics.com/Issue/Details?bugId=489291) lejupielādējamo failu lielumu līdz 1 GB. Tāpēc ir jākonfigurē elektronisko pārskatu risinājums, kas samazina iespējamību, ka šie ierobežojumi tiks pārsniegti un ka jūs saņemsit izņēmumu **Straume bija pārāk gara** vai **Pārpilde vai izzude aritmētiskajā operācijā**.

Konfigurējot risinājumu, varat pielāgot savu elektronisko pārskatu formātu operāciju noformētājā, pievienojot **Mapes** veida saknes elementu, lai saspiestu saturu, kas tiek ģenerēts ar to ligzdotajiem elementiem. Saspiešana darbojas “tieši laikā”, tādējādi samazinot maksimālo atmiņas izmantojumu un lejupielādējamā faila lielumu.

> [!NOTE]
> Failu saspiešana aizņem papildu procentus no centrālā procesora lietojuma.

Papildinformācijai par šo pieeju, aizpildiet šajā tēmā sniegto piemēru.

## <a name="example-compress-an-outbound-document"></a>Piemērs: izejoša dokumenta saspiešana

Šajā piemērā ir parādīts, kā lietotājs, kuram ir piešķirta loma **Sistēmas administrators** vai **Elektronisko pārskatu veidošanas funkcionālais konsultants** , var konfigurēt elektronisko pārskatu formātu, lai saspiestu ģenerētu dokumentu.

### <a name="prerequisites"></a>Priekšnosacījumi

Lai varētu pabeigt procedūras šajā tēmā, ir jāveic tālāk norādītās darbības.

1. [Aktivizēt konfigurāciju nodrošinātāju](er-defer-xml-element.md#activate-a-configuration-provider).
2. [Importēt ER konfigurāciju failu paraugu](er-defer-xml-element.md#import-the-sample-er-configurations).
3. [Pārskatīt importēto formātu](er-defer-xml-element.md#review-the-imported-format).

> [!NOTE]
> Pašlaik formāta struktūra sākas no **Faila** veida **Pārskata** elementa un satur XML elementus. Tādējādi izejošais dokuments tiks ģenerēts XML formātā un saspiešana netiks izmantota.

### <a name="generate-an-er-format-to-get-an-uncompressed-document"></a>Elektronisko pārskatu formāta ģenerēšana, lai iegūtu nesaspiestu dokumentu

1. [Importētā formāta palaišana](er-defer-xml-element.md#run-the-imported-format).
2. Ievērojiet, ka ģenerētā dokumenta lielums XML formātā ir 3 kilobaiti (KB).

    ![Nesaspiestā izejošā dokumenta priekšskatījums](./media/er-compress-outbound-files1.png)

### <a name="modify-the-format-to-compress-the-generated-output"></a>Formāta modificēšana, lai saspiestu ģenerēto izvadi

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā **Konfigurācijas**, konfigurāciju kokā izvērsiet vienumu **Modelis atlikto elementu apgūšanai**.
3. Atlasiet konfigurāciju **Formāts atlikto XML elementu apgūšanai**.
4. Atlasiet **Noformētājs**, lai modificētu formāta struktūru.
5. Lapas **Formāta noformētājs** cilnē **Formāts** atlasiet **Pievienot sakni**, lai pievienotu saknes formāta elementu.
6. Dialoglodziņā **Pievienot** atlasiet **Vispārīgi\\Mape**.
7. Atlasiet **Labi**, lai apstiprinātu jauna saknes elementa pievienošanu.
8. Atlasiet **Saglabāt**.

> [!NOTE]
> Formāta struktūra sākas no **Mapes** veida elementa. Šis elements ģenerēs izvadi kā saspiestu (zip) failu. Kad dokumentu, kas ģenerēts, izmantojot **Pārskata** elementu, ievieto izejošajā zip failā, tā saturs tiks saspiests, lai samazinātu izejošā faila lielumu.

### <a name="generate-an-er-format-to-get-a-compressed-document"></a>Elektronisko pārskatu formāta ģenerēšana, lai iegūtu saspiestu dokumentu

1. Lapā **Formāta veidotājs** atlasiet **Palaist**.
2. Lejupielādējiet zip failu, ko piedāvā tīmekļa pārlūkprogramma, un atveriet to pārskatīšanai.
3. Ievērojiet, ka ģenerētā dokumenta lielums zip formātā ir 1 KB.

    > [!NOTE] 
    > Šajā zip failā esošā XML faila saspiešanas koeficients ir 87 procenti. Saspiešanas koeficients ir atkarīgs no saspiestajiem datiem.

    ![Saspiestā izejošā dokumenta priekšskatījums](./media/er-compress-outbound-files2.png)

> [!NOTE]
> Ja elektronisko pārskatu [galamērķis](electronic-reporting-destinations.md) ir konfigurēts formāta elementam, kas ģenerē izvadi (**Pārskata** elementam šajā piemērā), tad izvades saspiešana tiks apieta.

## <a name="additional-resources"></a>Papildu resursi

[Elektronisko pārskatu veidošanas (ER) apskats](general-electronic-reporting.md)

[Elektroniskās pārskatu veidošanas (ER) adresāti](electronic-reporting-destinations.md)

[XML elementu izpildes atlikšana elektronisko pārskatu formātos](er-defer-xml-element.md)
