---
title: Izmaksu aprēķināšanas parametru vērtību iestatījumi
description: Iestatot zemes izmaksu moduli, varat definēt vairākas kopējās vērtības kopas, kas būs pieejamas, kad atlasāt noteiktus izmaksu aprēķināšanas parametru vērtību tipus citās programmas daļās. Šajā tēmā ir paskaidrots, kā iestatīt šīs vērtību kopas.
author: Weijiesa
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMCostTypeTable, ITMCostTypeGroup, ITMCostTransferGroup, ITMCostTemplateTable, ITMVolumetricDivisorTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ed20181201a2f3f84c3dc08549f4f107d46a50a2
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689752"
---
# <a name="costing-parameter-values-setup"></a>Izmaksu aprēķināšanas parametru vērtību iestatījumi

[!include [banner](../../includes/banner.md)]

Iestatot **Kopīgo izmaksu** moduli, var definēt vairākas kopējo vērtību un saistīto iestatījumu kopas katrai vērtībai. Šīs vērtības būs pieejamas, ja citās programmas daļās atlasīsiet noteiktus izmaksu aprēķināšanas parametru vērtību tipus. Šajā tēmā ir paskaidrots, kā iestatīt šīs vērtību kopas.

## <a name="set-up-cost-type-codes"></a>Iestatīt izmaksu tipu kodus

Izmaksu tipu kodi nosaka izmaksu tipu, kas rodas, kad preces tiek nosētas noliktavā, vai reisa zemes izmaksas. Kaut arī tie parasti palielina preču vērtību, tos var arī izmantot, lai virsgrāmatā uzkrātu summas. Virsgrāmatas korekcijas tiek izmantotas, kad izmaksas tiek uzkrātas laika gaitā vai reisu un korespondējošās sērijas laikā vienā darbībā.

> [!NOTE]
> Ja izmaksu tipu tabula tiek koplietota visām juridiskajām personām, kontu plāns jāsalieto arī visām juridiskajām personām. Pretējā gadījumā grāmatošanas darbības nedarbosies pareizi.

Lai iestatītu izmaksu tipu kodus, dodieties uz sadaļu **Kopīgās izmaksas \> Izmaksu iestatījumi \> Izmaksu tipu kodi**. Varat izmantot pogas Darbību rūtī, lai izveidotu jaunus izmaksu tipu kodus, labotu esošos kodus vai dzēstu atlasīto izmaksu tipu.

Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katram izmaksu tipu kodam.

| Lauks | Apraksts |
|---|---|
| Izmaksu veida kods | Ievadiet izmaksu tipa koda nosaukumu. |
| Apraksts | Ievadiet izmaksu tipa koda aprakstu. |
| Izmantot nosūtīšanas likmi | Iestatiet šo opciju kā *Jā*, ja reisa maiņas kurss (dažreiz saukts par pārvaldības kursu) ir jāizmanto šo izmaksu vērtības aprēķinam. Šajā gadījumā, lai apmainītos ar ārvalstu valūtas rēķiniem, tiek izmantots nosūtīšanas kurss, nevis standarta noklusējuma vai vietas maiņas kurss. |
| Pārskata izveides kategorija | Šis lauks izveido izmaksu tipa pārskata kategoriju. Pārskatus var drukāt vai nu pēc pārskatu kategorijām, vai pēc izmaksu tipa. |
| Debeta tips | Atlasiet, vai izmaksu tipam jādebetē krājums, Virsgrāmatas konts vai kreditors. |
| Debeta grāmatošana | Ja lauka **Debeta tips** iestatījums ir *Virsgrāmatas konts*, atlasiet grāmatošanas aprakstu. |
| Debeta konts | Ja lauka **Debeta tips** iestatījums ir *Virsgrāmatas konts*, atlasiet izmantojamo Virsgrāmatas kontu. |
| Kredīta tips | Atlasiet, vai izmaksu tipam jākreditē krājums, Virsgrāmatas konts vai kreditors. |
| Kredīta grāmatošana | Ja lauka **Kredīta tips** iestatījums ir *Virsgrāmatas konts*, atlasiet grāmatošanas aprakstu. |
| Kredīta konts | Ja lauka **Debeta tips** iestatījums ir *Virsgrāmatas konts*, atlasiet izmantojamo Virsgrāmatas kontu. |
| Dzēšanas konts | Izvēlieties izmaksu tipa klīringa kontu. Lai saņemtu palīdzību saistībā ar saskaņošanu, ieteicams norādīt atsevišķu klīringa kontu katram izmaksu tipam. |
| Standarta izmaksu gramatošanas tips | Ja izmantojat standarta izmaksu grāmatošanu, atlasiet grāmatošanas aprakstu. |
| Standarta izmaksu novirzes konts | <p>Ja izmantojat standarta izmaksu grāmatošanu, šeit norādītais konts tiks izmantots jebkādu noviržu grāmatošanai. Šis konts izmanto zemes izmaksu sadalījumu **Krājumu cenu** lapā. Šis sadalījums tiek izveidots, atjauninot cenas, izmantojot periodisko kārtību.</p><p>Piemēram, krājuma standarta izmaksas ir $15,00, FOB ir $13,00 un krava ir $2,00. Kad krājuma rēķins ir saņemts, krājums tiek saņemts $15,00 laikā, bet krājumam ir standarta $2,00 novirze, jo faktiskā FOB ir $13,00. Šī novirze tiek grāmatota standarta cenas novirzes kontā, kas ir iestatīts krājumu grāmatošanas profilā. Tā kā novērtētā krava $2,00 aprēķināta, krājumu rēķina grāmatošanas laikā nav novirzes. Tomēr, kad ir saņemts rēķins par kravu, tā maksā $2,50 par vienu vienību. Tāpēc $0,50 novirze tiek grāmatota norādītajām izmaksām. |
| Slīdošo vidējo noviržu konts | <p>Ja izmantojat mainīgās vidējās izmaksas, šeit norādītais konts tiks izmantots jebkādu noviržu grāmatošanai.</p><p>Piemēram, prognozētā kravas pārvadāšana $2,00. Tomēr, kad ir saņemts rēķins par kravu, tā maksā $2,50 par vienu vienību. Tādēļ $0,50 novirze ir jāiegrāmato.</p><p>Ja lapas **Kopīgo izmaksu parametri** opcija **Grāmatot korekcijas kā novirzes** ir iestatīta uz *Jā*, visas aprēķināto un reālo sūtījumu izmaksu novirzes tiks grāmatotas šeit norādītajā mainīgo vidējo noviržu kontā. Ja opcija **Grāmatot korekcijas kā novirzes** ir iestatīta uz *Nē*, tiks izmantota standarta funkcionalitāte un novirze tiks piemērota vai nu krājumos, vai šeit norādītajā pārvietojamā vidējā novirzes kontā atkarībā no rīcībā esošo krājumu.</p> |
| Maksājumu uzkrājumu principa uzskaite | Atlasiet kontu, kuru lieto, lai uzkrātu izmaksu novērtējumus, kad tiek grāmatots pirkšanas rēķins. Šis lauks tiek izmantots tikai tad, ja opcija **Izmantot izmaksu tipa maksas uzkrājuma kontu** ir iestatīta uz *Jā* kopsavilkuma cilnē **Izmaksas**, kas atrodas lapas **Kopīgo izmaksu parametri** cilnē **Vispārīgi**. |
| Maksājuma konts | Atlasiet kontu, kas tiek lietots, lai iegūtu ienākošās transportēšanas izmaksas, kuras ir izrakstījis piegādātājs. Summa tiek grāmatota kā debets. Korespondējošais konts ir krājumu novirzes konts. Šo grāmatošanu izmanto tikai tad, ja opcija **Grāmatot izmaksu kontu Virsgrāmatā** ir iestatīta uz *Jā* lapā **Kreditoru parametri**. |
| Noviržu konts | Konts, kas tiks izmantots, lai nobīdītu izmaksu uzkrājumus, kad tiek grāmatots pirkšanas rēķins. Šis lauks tiek izmantots tikai tad, ja opcija **Izmantot izmaksu tipa maksas uzkrājuma kontu** ir iestatīta uz *Jā* kopsavilkuma cilnē **Izmaksas**, kas atrodas lapas **Kopīgo izmaksu parametri** cilnē **Vispārīgi**. |

## <a name="vendor-cost-type-groups"></a>Kreditora izmaksu veida grupas

Kreditoru izmaksu tipu grupas palīdz noteikt, kā tiek atrastas un ar reisu lietotas *Automātiskās izmaksu maksas*. Saistīti kreditori ar līdzīgām importa izmaksām. Piemēram, visi kreditori no iepirktajiem tirgiem maksā vienādu nodokļa likmi par to pašu produktu tipu, kas pirkts no kopējā tirgus.

Kreditora izmaksu tipu grupas var uzturēt, ejot uz **Kopīgās izmaksas \>Izmaksu iestatījumi \> Kreditora izmaksu tipu grupas**. Lapa **Kreditora izmaksu tipu grupas** nodrošina režģi, kurā uzskaitītas visas esošās kreditoru izmaksu tipu grupas. Jūs varat izmantot pogas Darbību rūtī, lai pievienotu, noņemtu un rediģētu rindas režģī.

Tālāk esošajā tabula apraksta laukus, kas ir pieejami Darbības kopsavilkuma cilnē.

| Lauks | Apraksts |
|---|---|
| Kreditora izmaksu veida grupas | Ievadiet unikālu nosaukumu kreditora izmaksu tipu grupai (piemēram, *Jaunie tirgi*). |
| Apraksts | Ievadiet kreditora izmaksu tipa koda aprakstu. Šajā aprakstā var būt sniegta detalizēta informācija par maksas līmeni vai tipu, kas ir saistīts ar kreditoru grupu. |

## <a name="item-cost-type-groups"></a>Krājuma izmaksu veida grupas

Kreditoru izmaksu tipu grupas palīdz noteikt, kā tiek atrastas un ar reisu lietotas *Automātiskās izmaksu* maksas. Līdzīgas preces ir saistītas kopā. Piemēram, visi krājumi, kuru nodokļa likme ir 5 procenti, var piederēt specifiskai izmaksu tipa grupai.

Kreditora izmaksu tipu grupas var uzturēt, ejot uz **Kopīgās izmaksas \>Izmaksu iestatījumi \> Kreditora izmaksu tipu grupas**. Lapa **Kreditora izmaksu tipu grupas** nodrošina režģi, kurā uzskaitītas visas esošās kreditoru izmaksu tipu grupas. Jūs varat izmantot pogas Darbību rūtī, lai pievienotu, noņemtu un rediģētu rindas režģī.

Tālāk esošajā tabula apraksta laukus, kas ir pieejami Darbības kopsavilkuma cilnē.

| Lauks | Apraksts |
|---|---|
| Krājuma izmaksu veida grupas | Ievadiet unikālu nosaukumu kreditora izmaksu tipu grupai (piemēram, *5% nodoklis*). |
| Apraksts | Ievadiet krājuma izmaksu tipa koda aprakstu. Šajā aprakstā var būt sniegta detalizēta informācija par maksas līmeni vai tipu, kas ir saistīts ar krājumu grupu. |

> [!NOTE]
> Krājuma izmaksu tips ir saistīts ar krājumu, izmantojot **Izmaksu tipu grupas** lauku kopsavilkuma cilnē **Pirkumi** krājumu lapai **Izlaistā prece**.

## <a name="transfer-order-cost-type-groups"></a>Pārsūtīšanas pasūtījuma izmaksu tipu grupas

Pārsūtīšanas pasūtījumu izmaksu tipu grupas palīdz noteikt, kā tiek atrastas un ar reisu lietotas *Automātiskās izmaksu* maksas. Līdzīgas preces ir saistītas kopā. Piemēram, visi krājumi, kuru nodokļa likme ir 7 procenti, var piederēt specifiskai izmaksu tipa grupai.

Pārsūtīšanas pasūtījumu izmaksu tipu grupas var uzturēt, ejot uz **Kopīgās izmaksas \> Izmaksu iestatījumi \> Pārsūtīšanas pasūtījumu izmaksu tipu grupas**. Lapa **Kreditora izmaksu tipu grupas** nodrošina režģi, kurā uzskaitītas visas esošās pārsūtīšanas pasūtījumu izmaksu tipu grupas. Jūs varat izmantot pogas Darbību rūtī, lai pievienotu, noņemtu un rediģētu rindas režģī.

Tālāk esošajā tabula apraksta iestatījumus, kas ir pieejami Darbības kopsavilkuma cilnē.

| Lauks | Apraksts |
|---|---|
| Pārsūtīšanas pasūtījuma izmaksu tipu grupas | Ievadiet unikālu nosaukumu pārsūtīšanas pasūtījumu izmaksu tipu grupai (piemēram, *7% nodoklis*). |
| Apraksts | Ievadiet pārsūtīšanas pasūtījuma izmaksu tipa koda aprakstu. Šajā aprakstā var būt sniegta detalizēta informācija par maksas līmeni vai tipu, kas ir saistīts ar pārsūtīšanas pasūtījumu izmaksu tipu grupu. |

> [!NOTE]
> Krājuma izmaksu tips ir saistīts ar krājumu, izmantojot **Pārsūtīšanas pasūtījumu izmaksu grupas** lauku kopsavilkuma cilnē **Pirkumi** krājumu lapai **Izlaistā prece**.

## <a name="cost-templates"></a>Izmaksu veidnes

Jūs izmantojat izmaksu veidnes, lai iestatītu noklusējuma vērtības iestatījumiem, ko lietotāji, kuri iegūst izmaksu novērtējumu, var nezināt. Izmaksu veidnes var palīdzēt samazināt novērtēšanas procesa sarežģītību, samazinot atlases, kas jāveic lietotājiem, lai iegūtu precīzu novērtējumu.

Lai strādātu ar izmaksu veidnēm, dodieties uz sadaļu **Kopējās izmaksas \> Izmaksu aprēķināšanas iestatījumi \> Automātiskās izmaksas**. Izmaksu **Izmaksu veidnes** saraksta rūtī kreisajā pusē ir parādītas visas pašreizējās izmaksu veidnes. Jūs varat izmantot pogas Darbību rūtī, lai pievienotu, noņemtu un rediģētu veidnes.

Tālāk esošajā tabulā ir aprakstīti pieejamie iestatījumi katrai veidnei.

| Lauks | Apraksts |
|---|---|
| Izmaksu veidne | Ievadiet unikālu izmaksu veidnes nosaukumu. Šis nosaukums parasti apraksta veidnes faktoru vai izmaksu reizinātāju. |
| Apraksts | Ievadiet izmaksu veidnes aprakstu. |
| Nosūtīšanas uzņēmums | Atlasiet nosūtīšanas uzņēmuma kreditora kontu, ko saistīt ar izmaksu veidni. |
| Piegādes veids | Atlasiet piegādes veidu, kas izmaksu veidnei jāizmanto, kad tiek aprēķinātas krājuma novērtētās izmaksas. Šis lauks palīdzēs noteikt automātiskās izmaksas, kas ir saistītas ar precēm izmaksu novērtējumā. |
| Nosūtīšanas konteinera veids | Atlasiet nosūtīšanas konteinera tipu, ko saistīt ar izmaksu veidni. Šis lauks palīdzēs noteikt automātiskās izmaksas, kas ir saistītas ar precēm izmaksu novērtējumā. |
| Muitas aģents | Atlasiet muitas starpnieku (kreditoru), kuru saistīt ar izmaksu veidni. Šis lauks palīdzēs noteikt automātiskās izmaksas, kas ir saistītas ar precēm izmaksu novērtējumā. |
| Koeficients | Ievadiet koeficientu, ko piemērot preču galīgo izmaksu novērtējumam. Piemēram, lai novērtētu izmaksu budžetam pievienotu 10 procentus, ievadiet *1,10*. |

## <a name="volumetric-divisors"></a>Apjoma dalītāji

Tilpuma sadalītājus izmanto, lai aprēķinātu tilpuma svaru. Katrs nosūtīšanas/kravas uzņēmums formulē savus tilpuma dalītājus. Turklāt uzņēmuma dalītāji parasti mainās atkarībā no piegādes veida. Piemēram, gaiss un gaiss bieži ir ļoti dažādi dalītāji. Uzņēmums var arī padarīt savus noteikumus sarežģītākus atkarībā no tā, kur tas nosūta. Sistēma izmanto šādu formulu, lai atrastu tilpuma svaru: VolumetricWeight = volume ÷ VolumetricDivisor.

Piemēram, sūtījuma, kas tiek nosūtīta ar gaisa pārvadājumiem, tilpums ir 3 kubikmetri (m³). Uzņēmums iekasē pēc tilpuma svara un piemēro 6 tilpuma dalītāju. Šis dalītājs tiek dalīts ar tilpumu, lai noteiktu tilpuma svaru. Tāpēc, piemēram, tilpums ir 3 ÷ 6 = 0,5 kilogrami (kg).

Lai iestatītu izmaksu tipu kodus, dodieties uz sadaļu **Kopīgās izmaksas \> Izmaksu iestatījumi \> Izmaksu tipu kodi**. Lapa **Tilpuma dalītāji** nodrošina režģi, kas uzskaita visus esošos tilpuma dalītājus. Jūs varat izmantot pogas Darbību rūtī, lai pievienotu, noņemtu un rediģētu rindas režģī.

Tālāk esošajā tabula apraksta laukus, kas ir pieejami Darbības kopsavilkuma cilnē.

| Lauks | Apraksts |
|---|---|
| Nosūtīšanas uzņēmums | Atlasiet nosūtīšanas uzņēmuma kreditora kontu, kas ir saistīts ar tilpuma dalītāju. |
| Izmaksu veida kods | Atlasiet izmaksu tipa kodu, kas ir saistīts ar tilpuma dalītāju. Lietojiet šo lauku, lai izmaksu tipus ievietotu pārskata intervālos. Pārskatus var drukāt vai nu pēc pārskatu kategorijām, vai pēc izmaksu tipa. |
| No porta | Atlasiet portu "no", uz kuru attiecas tilpuma dalītājs. |
| Apjoma dalītājs | Ievadiet tilpuma dalītāja vērtību, kas piemērota rindai. Katra iepakojuma tilpums tiks sadalīts pēc šeit ievadītās vērtības, lai noteiktu šī iepakojuma tilpumu. |

> [!NOTE]
> Sistēma izmantos maksimālo vērtību starp faktisko **svaru un** tilpumu **·**.
