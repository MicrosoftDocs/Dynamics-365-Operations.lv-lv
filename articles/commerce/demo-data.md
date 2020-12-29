---
title: Demonstrācijas datu ekrāna izkārtojumi programmā Modern POS (MPOS) un Cloud POS
description: Šajā tēmā ir sniegta informācija par ekrāna izkārtojumiem, kas ir pieejami programmā Dynamics 365 Commerce kopā ar pārdošanas punkta (POS) lietošanas iespēju demonstrācijas datiem.
author: josaw1
manager: AnnBe
ms.date: 10/05/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2017-10-05
ms.dyn365.ops.version: Retail April 2017 update
ms.openlocfilehash: 935e1a550160515e2c325c39eab86be3b9fa5394
ms.sourcegitcommit: d82f319cf7dd26c93a3fd342de4fd537272fa8d2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2020
ms.locfileid: "4414206"
---
# <a name="demo-data-screen-layouts-in-modern-pos-mpos-and-cloud-pos"></a>Demonstrācijas datu ekrāna izkārtojumi programmā Modern POS (MPOS) un Cloud POS

[!include [banner](includes/banner.md)]

Šajā tēmā ir sniegta informācija par ekrāna izkārtojumiem, kas ir pieejami programmā Dynamics 365 Commerce kopā ar pārdošanas punkta (POS) lietošanas iespēju demonstrācijas datiem.

## <a name="overview"></a>Pārskats

Pieejamie programmas Commerce demonstrācijas datu ekrāna izkārtojumu paraugi nodrošina saturu, kas ir optimizēts dažādiem mazumtirdzniecības segmentiem, veikala darbinieku lomām un ierīcēm. Vienā izkārtojumā var būt ietverti vairāki izkārtojuma lieluma iestatījumi un pogu režģu kombinācijas, lai palīdzētu nodrošināt piemērotību dažādām ierīcēm un stacijām, ko izmanto veikala darbinieki. Šajā tēmā ir aprakstītas šo izkārtojumu atšķirības, kā arī to nodrošinātās darbības un vispārīgā funkcionalitāte.

![Demonstrācijas datu izkārtojumi dažādām ierīcēm](../commerce/media/demo-screen-layouts-fig-1-1.png)

## <a name="anatomy-of-a-screen-layout-id"></a>Ekrāna izkārtojuma ID sastāvs

Lai atrastu ekrāna izkārtojumus, pārejiet uz sadaļu **Mazumtirdzniecība un komercija** \> **Kanāla iestatīšana** \> **POS iestatīšana** \> **POS** \> **Ekrāna izkārtojumi**.

![Ekrāna izkārtojumu lapa](../commerce/media/demo-screen-layouts-fig-2-1.png)

Ekrāna izkārojuma ID var būt ietvertas ne vairāk kā 10 rakstzīmes. ID ir virkne, kas sastāv no trim informācijas daļām tālāk norādītajā secībā.

1. Uzņēmums
2. Izkārtojuma versija
3. Persona

### <a name="company"></a>Uzņēmums

| Burts | Uzņēmums         |
|--------|-----------------|
| A      | Adventure Works |
| F      | Fabrikam        |
| U      | Contoso         |

### <a name="layout-version"></a>Izkārtojuma versija

| Versijas numurs | apraksts                                                                                |
|----------------|--------------------------------------------------------------------------------------------|
| 3              | Pamata versija, kas atbalsta vairākus ekrāna izmērus un ir piemērota dažādām ierīcēm un proporcijām |
| 3.1            | Pamata versija ar papildu paneļa **Ieteiktās preces** atbalstu        |
| 4              | Paplašinātā versija paplašinātajam Fabrikam atjauninātajam izkārtojumam                                  |

### <a name="persona"></a>Persona

| Saīsinājums | Persona       | Saturs |
|--------------|---------------|----------|
| CSH          | Kasieris       | Kasierim paredzētajos izkārtojumos ir ietvertas visas ar transakcijām saistītās operācijas, piemēram, debitoru pasūtījumi, atgriešanas, atlaides, anulēšanas un dāvanu kartes. Šajos izkārtojumos ir ietverti arī krājumu pārvaldības ikdienas uzdevumi, piemēram, cenas pārbaude, krājumu uzmeklēšana un krājumu uzskaite. Ir nodrošinātas arī pamata maiņas pārvaldības iespējas, kas ir saistītas ar sākuma summu, maiņas aizturēšanu un laika uzskaiti. |
| MGR          | veikala vadītājs; | Veikala vadītājam paredzētajos izkārtojumos ir ietvertas visas kasierim paredzētajos izkārtojumos ietvertās ar transakcijām saistītās operācijas, kā arī nodokļu ignorēšanas operācijas. Šajos izkārtojumos ir ietverti arī krājumu pārvaldības ikdienas uzdevumi, piemēram, cenas pārbaude, krājumu uzmeklēšana un krājumu uzskaite. Ir nodrošinātas maiņas pārvaldības operācijas, kas ir saistītas ar maiņu sākšanu, aizturēšanu un slēgšanu. Šajos izkārtojumos ir ietvertas arī naudas kastes operācijas, kas ir saistītas ar naudas ievietošanu un izņemšanu, norēķinu uzskaiti, ievietošanu seifā un noguldīšanu bankā. Turklāt šajos izkārtojumos ir ietverta iespēja piekļūt veiktspējas pārskatiem un drukāt X un Z pārskatus. |
| STK          | Noliktavas darbinieks   | Noliktavas darbiniekam paredzētie izkārtojumi ir optimizēti krājumu pārvaldībai. Tajos ir ietvertas iespējas piekļūt ikdienas uzdevumiem, kas ir saistīti art cenas pārbaudi, krājumu uzmeklēšanu, izdošanu un saņemšanu, krājumu uzskaiti un komplektu izjaukšanu. Šie izkārtojumi nodrošina arī pamata maiņas operācijas, kas ir saistītas ar laika uzskaiti un maiņas aizturēšanu. Lai gan šie izkārtojumi galvenokārt ir paredzēti vadības uzdevumiem, noliktavas darbiniekiem transakciju ekrānos ir pieejamas tādas pašas operācijas kā kasieriem. |

### <a name="example-layout"></a>Izkārtojuma piemērs

Tālāk ir sniegts ekrāna izkārtojuma ID, kam atbilst uzņēmuma Fabrikam versijas 4 izkārtojums, kas ir paredzēts veikala vadītājam.

F4MGR

Tālāk esošajā attēlā ir redzams Fabrikam veikala vadītāja sveiciena ekrāna piemērs.

![Fabrikam veikala vadītāja sveiciena ekrāns.](../commerce/media/demo-screen-layouts-fig-2-2.png)

## <a name="layout-sizes"></a>Izkārtojumu lielumi

### <a name="full-vs-compact-layouts"></a>Pilno un kompakto izkārtojumu salīdzinājums

Ekrāna izkārtojumam var būt pieejamas pilna lieluma ierīcēm un kompaktām ierīcēm paredzētas konfigurācijas. Tāpēc lietotāju var piešķirt vienam ekrāna izkārtojumam, kas ir piemērots veikalā izmantotajām dažāda lieluma un formas ierīcēm.

- **Modern POS — pilns** — parasti pilnie izkārtojumi ir vispiemērotākie lielākiem displejiem, piemēram, personālo datoru monitoriem vai planšetdatoriem. Lietotāji var atlasīt izkārtojumā ietvertos lietotāja interfeisa elementus, norādīt šo elementu lielumu un novietojumu un konfigurēt to detalizētos rekvizītus. Pilnie izkārtojumi atbalsta gan portreta, gan ainavorientācijas konfigurācijas.
- **Modern POS — kompakts** — parasti kompaktie izkārtojumi ir vispiemērotākie tālruņiem vai maziem planšetdatoriem. Kompaktā izkārtojuma ierīcēm ir ierobežotas izstrādes iespējas. Lietotāji var konfigurēt saņemšanas rūts un kopsummu rūts kolonnas un laukus.

### <a name="screen-resolutions-that-are-provided"></a>Nodrošinātās ekrāna izšķirtspējas

Tālāk esošajā tabulā ir norādīti standarta ekrāna izšķirtspējām nodrošinātie ekrāna izkārtojumi.

| Izkārtojuma veids | Novēršana | Proporcijas | Mērķa displejs          |
|-------------|------------|--------------|-------------------------|
| Sablīvēt\*   | 480 × 853  | 16:9         | Tālruņi                  |
| Pilns        | 1024 × 768 | 4:3          | Planšetdatori                 |
| Pilns\*      | 1280 × 720 | 16:9         | Planšetdatori                 |
| Pilns        | 1366 × 768 | 16:9         | Planšetdatori ar lieliem ekrāniem |
| Pilns        | 1440 × 960 | 3:2          | Planšetdatori ar lieliem ekrāniem |
| Pilns\*      | 1536 x 864 | 16:9         | Planšetdatori ar lieliem ekrāniem |

\* Šie papildu izkārtojumu lielumi ir pieejami tikai Adventure Works un Fabrikam izkārtojumiem.

> [!TIP]
> POS sistēmā tiek automātiski atlasīts izkārtojuma lielums, izvēloties pašreizējās programmas loga ekrāna izšķirtspējai tuvāko pieejamo lielumu. Lai uzzinātu pašlaik izmantotā ekrāna izkārtojuma ID un izšķirtspēju, programmā Modern POS (MPOS) vai Retail Cloud POS (CPOS) atvariet lapu **Iestatījumi** un skatiet sadaļu **Sesijas informācija**. Varat arī skatīt pašreizējās programmas vai pārlūkprogrammas rāmja faktisko loga izšķirtspēju. Kad esat uzzinājis šo informāciju, varat skatīt izkārtojuma satura avotu, pārejot uz sadaļu **Kanāla iestatīšana** \> **POS iestatīšana** \> **POS** \> **Ekrāna izkārtojumi**.

![Ekrāna izkārtojumi un izkārtojumu izšķirtspēja/lielums modulī Commerce un POS sistēmā](../commerce/media/demo-screen-layouts-fig-3-1.png)

## <a name="companies-and-brands"></a>Uzņēmumi un zīmoli

Katrs fiktīvais uzņēmums ir paredzēts atšķirīgam mazumtirdzniecības segmentam, un tajā ir ietverti preču katalogi, kas ir pielāgoti uzņēmuma tirgum. Katram uzņēmumam ir unikāls zīmola vizuālais noformējums, kas tiek lietots šī uzņēmuma precēm. Tiek izmantoti tādi zīmolrades elementi kā izvēluma krāsa, tumšs vai gaišs dizains un pievienotie fotoattēli, kas nodrošina reālistisku pieredzi.

### <a name="company-segment-and-visual-characteristics"></a>Uzņēmuma uzņēmējdarbības segments un vizuālās īpašības

| Uzņēmums         | Novietojums | Segments        | Izcelt | Tēma |
|-----------------|----------|----------------|--------|-------|
| Adventure Works | Sietla  | Sporta preces | Zilā   | Tumšs  |
| Fabrikam        | Sanfrancisko  | Mode        | Zaļā  | Gaišs |
| Contoso         | Bostona   | Elektropreces    | Sarkanā    | Tumšs  |

> [!NOTE]
> Adventure Works un Fabrikam ir divi vadošie zīmoli. Ir pieejams arī uzņēmums Contoso, taču tam nav nodrošināti visi izkārtojumi.

Tālāk esošajos attēlos ir redzamas trīs fiktīvo uzņēmumu sveiciena lapas un transakciju lapas.

### <a name="adventure-works"></a>Adventure Works

![Uzņēmuma Adventure Works demonstrācijas datu sveiciena lapa](../commerce/media/demo-screen-layouts-fig-4-1a.png)

![Uzņēmuma Adventure Works demonstrācijas datu transakciju lapa](../commerce/media/demo-screen-layouts-fig-4-1b.png)

### <a name="fabrikam"></a>Fabrikam

![Uzņēmuma Fabrikam demonstrācijas datu sveiciena lapa](../commerce/media/demo-screen-layouts-fig-4-2a.png)

![Uzņēmuma Fabrikam demonstrācijas datu transakciju lapa](../commerce/media/demo-screen-layouts-fig-4-2b.png)

### <a name="contoso"></a>Contoso

![Uzņēmuma Contoso demonstrācijas datu izkārtojumi](../commerce/media/demo-screen-layouts-fig-4-3.png)

## <a name="user-sign-in-matrix"></a>Lietotāju pieteikšanās tabula

Dažādajiem ekrāna izkārtojumiem ir nodrošināti lietotāji. Izmantojot tālāk esošajā tabulā sniegto informāciju, varat piekļūt jebkuram ekrānam. Jums ir tikai jāpierakstās, izmantojot atbilstošu operatora ID.

| Uzņēmums         | Ekrāna izkārtojuma ID | Persona       | Operatora ID           |
|-----------------|------------------|---------------|------------------------|
| Adventure Works | A3MGR            | veikala vadītājs; | 000154, 000137, 000073 |
| Adventure Works | A3CSH            | Kasieris       | 000150, 000175, 000165 |
| Adventure Works | A3STK            | Noliktavas darbinieks   | 000155, 000181, 000152 |
| Fabrikam        | F4MGR            | veikala vadītājs; | 000160, 000713         |
| Fabrikam        | F3CSH            | Kasieris       | 000161, 000113, 000114 |
| Fabrikam        | F3STK            | Noliktavas darbinieks   | 000164, 000112, 000123 |
| Contoso         | C3MGR            | veikala vadītājs; | 000100, 000111         |
| Contoso         | C3CSH            | Kasieris       | 000110, 000120         |
| Contoso         | Nav attiecināms   | Noliktavas darbinieks   | Nav attiecināms         |

> [!TIP]
> Lai nodrošinātu labākos rezultātus, aktivizējiet kases sistēmu attiecīgajā veikala atrašanās vietā un iestatiet tās personas uzņēmumu, ko izmantosiet pēc pierakstīšanās. Tādējādi tiek nodrošināta vizuālā profila un zīmolrades attēlu saskaņotība visā demonstrācijas datu izmantošanas laikā. Piemēram, ja vēlaties skatīt Fabrikam kasierim paredzēto izkārtojumu, aktivizējiet kases sistēmu Hjūstonas veikalā.

<!-- Hiding until the content page is available on CustomerSource -->

<!-- ## Reference icons and images -->

<!-- The screen layouts, button grids, and visual profiles were created using images and icons that can be found in **Retail and Commerce \> Channel setup \> POS setup \> POS \> Images**. -->

<!-- ![Images in Dynamics 365 Commerce](../commerce/media/demo-screen-layouts-fig-5-1.png) -->

<!-- Use the [POS Icon and Image Mapping](../commerce/media/POS_Icon_and_Image_Mapping.xlsx) reference spreadsheet to locate operation icons, reference photos, swap logos, or provide new images of your own that can be referenced in custom designs. -->

<!-- END HIDDEN CONTENT -->
