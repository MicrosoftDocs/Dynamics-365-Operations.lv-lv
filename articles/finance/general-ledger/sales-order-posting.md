---
title: Pārdošanas pasūtījumu grāmatošana
description: Šajā tēmā ir sniegta informācija par pārdošanas pasūtījuma cilni krājumu grāmatošanas metodes lapā.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 5d84723b51d6977867fa162c4a47befa61bd9ef6
ms.sourcegitcommit: dc3053625dfe24aef64399dd1d002214e7f7619f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/13/2022
ms.locfileid: "8755933"
---
# <a name="sales-order-posting"></a>Pārdošanas pasūtījumu grāmatošana

Pārdošanas **pasūtījuma cilne** lapā Noliktavas grāmatošanas profili **tiek** izmantota, lai kontrolētu to, kā pārdošanas pasūtījumi tiks grāmatoti Virsgrāmatā. Pārdošanas pasūtījuma divas galvenās aktivitātes tiek grāmatotas Virsgrāmatā: 

- Pavadzīme
- Rēķins

Lai fiziskas darbības (pavadzīme) grāmatotu virsgrāmatā pārdošanas pasūtījumam, jābūt šādiem nosacījumiem:

- Lapā Krājumu **un noliktavas pārvaldības parametri** ir jābūt atzīmētai **izvēles rūtiņai Grāmatot** pavadzīmi Virsgrāmatā.
- Pārdošanas pasūtījuma **rindā atlasītā** krājuma lapā **Krājumu** modeļu grupa jāatlasa izvēles rūtiņa Grāmatot fiziskos krājumus Virsgrāmatā.
- **Lapā Krājumu grāmatošanas** metode galvenie konti jānorāda šādiem grāmatošanas tipiem:
  - Piegādāto vienību izmaksas
  - Nosūtītās pārdoto preču pašizmaksas

Lai finanšu darbība (rēķins) tiktu iegrāmatota virsgrāmatā pārdošanas pasūtījumam, jābūt šādiem nosacījumiem:

- Pārdošanas pasūtījuma **rindā atlasītā** krājuma lapā **Krājumu** modeļu grupa ir jābūt atzīmētai izvēles rūtiņai Grāmatot finanšu krājumus Virsgrāmatā.
- Krājumu grāmatošanas metodes lapā ir jānorāda **galvenie konti** šādiem grāmatošanas tipiem:
  - Rēķinā iekļauto vienību izmaksas
  - Rēķinā iekļauto pārdoto preču pašizmaksa
  - Ieņēmumi
  - Atlaide\*

> [!NOTE]
> Atlaižu konts nav obligāts. Daudziem grāmatvedības noteikumiem, piemēram, GAAP un IFRS, ir nepieciešams, lai atlaides samazinātu pārdošanas ieņēmumus, un tāpēc šie konti netiek izmantoti daudzos scenārijos. Ja to ļauj lokālie noteikumi, izmantojiet atsevišķu galveno kontu, lai grāmatotu pārdošanas cenas daļu, kam ir atlaide.

Lai, ģenerējot pārdošanas pasūtījuma pavadzīmi, virsgrāmatā grāmatotu atlikto (novērtēto) ieņēmumu vērtību, jāizpilda šādi nosacījumi:

- Pārdošanas pasūtījuma **rindā atlasītā** krājuma lapā **Krājumu** modeļu grupa jāatlasa izvēles rūtiņa Grāmatot fiziskos krājumus Virsgrāmatā.
- **Lapā Krājumu modeļu grupa jābūt** atzīmētai izvēles **rūtiņai Grāmatot atlikto** ieņēmumu kontā pārdošanas piegādē.
- Lapā Krājumu **un noliktavas pārvaldības parametri** ir jābūt atzīmētai **izvēles rūtiņai Grāmatot** pavadzīmi Virsgrāmatā.
- Lapā Krājumu **un noliktavas pārvaldības parametri** ir jābūt **atzīmētai izvēles rūtiņai** Grāmatot fizisko PVN.
- Lapā Debitoru **parādu parametri** ir jābūt atzīmētai **izvēles rūtiņai Grāmatot pavadzīmi** Virsgrāmatā.
- **Lapā Krājumu grāmatošanas** metode galvenie konti jānorāda šādiem grāmatošanas tipiem:
  - Atliktie piegādes ieņēmumi
  - Atlikto piegādes ieņēmumu korespondēšana
  - Atliktais PVN par piegādi

> [!NOTE]
> Ieteicams aktivizēt opcijas Grāmatot fiziskos krājumus **un Grāmatot pavadzīmi** **Virsgrāmatā**. Šo opciju iespējošana var palīdzēt paātrināt mēneša beigu slēgšanas procedūras, jo neviens atliktais nodoklis nav manuāli jāaprēķina un jāgrāmato. Turklāt finanšu pārskati automātiski atspoguļos atlikto maksājumu summas, neveicot manuālu iejaukšanos.

> [!IMPORTANT]
> Opcija **Grāmatot atlikto ieņēmumu kontu pārdošanas piegādē** netiek izmantota ar ieņēmumu atzīšanu. Papildinformāciju par ieņēmumu atzīšanu skatiet ieņēmumu [atzīšanas apskatā](/accounts-receivable/revenue-recognition-overview.md)

## <a name="sample-posting-profile-configuration"></a>Grāmatošanas metodes konfigurācijas paraugs 

Tālāk sniegtajā tabulā ir norādīti noklusējuma grāmatošanas tipu piemēri ar galvenajiem kontiem un aprakstiem:
 
- Kolonna **Klīringa** konts norāda, ka grāmatošanas tips ir tīrīšanas konts. Šajā kontā grāmatotā summa tiek automātiski apgriezta, grāmatojot vēlāku darbību. 
- P **/F kolonna** norāda P fiziskai **grāmatošanai** un **F finanšu** grāmatošanai. 
- Kolonna **Vienāda** norāda, vai galvenais konts noteiktam grāmatošanas tipam parasti ir tāds pats kā cits grāmatošanas tips. Vērtība kolonnā norāda grāmatošanas tipu, kas parasti tiek izmantots.

> [!NOTE]
> Šie galvenie konti un galveno kontu nosaukumi ir tikai ieteikumi. Ieteicams strādāt ar savu grāmatvedi, lai noteiktu biznesa vajadzībām labāko konfigurāciju.


| Grāmatošanas tips | Galvenā konta piemērs | Galvenā konta nosaukuma piemērs | Konta veids | Vai debets/kredīts? | Dzēšanas konts | P/F | Izpildiet | Apraksts |
|------------|------------------------|-------------------------|--------------|---------|-------------------|------------|------|-------------------------|
| Piegādāto vienību izmaksas | 140100</br>140101 | Materiālu krājumi</br>Piegādātie materiāli, kas nav izrakstīti rēķinā | Līdzeklis | Kredīts | Jā | P | Rēķinā iekļauto vienību izmaksas | Tiek izmantota, kad tiek grāmatota pārdošanas pasūtījuma pavadzīme. Korespondējošais konts ir pārdoto, piegādāto preču izmaksas. Summa šajā kontā tiek anulēta, kad tiek grāmatots pārdošanas pasūtījuma rēķins. Jūs, iespējams, vēlēsieties izmantot materiālus, kas ir nosūtīti, bet kuriem nav izrakstīts rēķins, lai atspoguļotu fiziskos krājumus, un finanšu atjaunināšanai rezervēt materiālu krājumu kontu. |
| Nosūtītās pārdoto preču pašizmaksas | 500150 | Atliktā PPPI | Izdevumi | Debets | Jā | P  | Tiek izmantota, kad tiek grāmatota pārdošanas pasūtījuma pavadzīme. Korespondējošais konts ir piegādāto vienību izmaksas. Summa šajā kontā tiek anulēta, kad tiek grāmatots pārdošanas pasūtījuma rēķins. |
| Rēķinā iekļauto vienību izmaksas | 140100 | Materiālu krājumi | Līdzeklis | Kredīts | Nē | F | Piegādāto vienību izmaksas | Tiek izmantots, kad tiek grāmatots pārdošanas pasūtījuma rēķins. Korespondējošais konts ir pārdoto preču izmaksas, par ko ir izrakstīts rēķins. Šis konts parāda krājumu jūsu bilancē. |
| Rēķinā iekļauto pārdoto preču pašizmaksa | 500100 | PPPI materiāli | Izdevumi | Debets | Nē | F  | Tiek izmantots, kad tiek grāmatots pārdošanas pasūtījuma rēķins. Korespondējošais konts ir vienību izmaksas, par ko izrakstīts rēķins. Šis konts ataino PPPI savā PL&amp; pārskatā. |
| Ieņēmumi (pārdošanas pasūtījuma ieņēmumi*) | 400100 | Ieņēmumu materiāli | Ieņēmumi | Kredīts | Nē | F   | Tiek izmantots, kad tiek grāmatots pārdošanas pasūtījuma rēķins. Korespondējošais konts ir summu konts (Debitora bilance*) debitoru parādu **grāmatošanas profilā**. |
| Komisija (pārdošana, komisija*) | 602150 | Komisijas izdevumi | Izdevumi | Debets | Nē | F  | Izmanto, kad komisija ir iespējota un aprēķināta pārdošanai un grāmatota pārdošanas pasūtījuma rēķina procesa laikā. Korespondējošais konts ir komisijas maksājums. |
| Komisijas korespondējošais konts (pārdošana, komisijas korespondējošais*) | 201110 | Maksājamās komisijas | Saistības | Kredīts | Jā | F | Izmanto, kad komisija ir iespējota un aprēķināta pārdošanai un grāmatota pārdošanas pasūtījuma rēķina procesa laikā. Korespondējošais konts ir komisijas izdevumi. |
| Atliktie piegādes ieņēmumi (Pārdošana – pavadzīmes ieņēmumi*) | 401400 | Uzkrātā pārdošana | Ieņēmumi | Kredīts | Jā | P  | Izmanto, kad atliktie piegādes ieņēmumi ir aktivizēti un tiek grāmatoti, kad apstrādājāt pārdošanas pasūtījuma pavadzīmi. Korespondējošais konts ir atlikto ieņēmumu korespondējošais konts. Šī konta summas tiek automātiski apgrieztas, grāmatojot pārdošanas pasūtījuma rēķinu. |
| Atlikto piegādes ieņēmumu korespondēšana (pārdošana – pavadzīmes ieņēmumu korespondējošais)* | 130400 | Debitoru parādi — nav izrakstīti rēķini | Līdzeklis | Debets | Jā | P  | Izmanto, kad atliktie piegādes ieņēmumi ir aktivizēti un tiek grāmatoti, kad apstrādājāt pārdošanas pasūtījuma pavadzīmi. Korespondējošais konts ir atliktie piegādes ieņēmumi. Šī konta summas tiek automātiski apgrieztas, grāmatojot pārdošanas pasūtījuma rēķinu. |
| Atliktais PVN par piegādi (Pārdošana, pavadzīmes nodoklis*) | 250500 | Atliktais PVN | Saistības | Kredīts | Jā | P  | Tiek lietots, ja ir aktivizēti atliktie piegādes ieņēmumi un aktivizēts režīms Grāmatot fizisko PVN. Nodokļu summa tiek grāmatota, apstrādājot pārdošanas pasūtījuma pavadzīmi. |

\* Šīs tabulas iekavās redzamās **vērtības norāda vērtību, kas tiek izmantota dokumenta darbību** **lapas laukā Grāmatošanas** tips. Cilnes Vispārīgi **lapā Dokumentu** darbības var **skatīt grāmatošanas** **tipu**.

## <a name="sales-category-posting"></a>Pārdošanas kategorijas grāmatošana

Kā alternatīvu krājumu grāmatošanas iestatīšanai visiem krājumiem, krājumu grupai vai atsevišķai krājumos, varat iestatīt kategorijas un kontrolēt grāmatošanu Virsgrāmatā pēc pārdošanas kategorijām. Lai iegūtu vairāk informācijas par kategoriju hierarhijas iestatīšanu un kategoriju piešķiršanu precēm, [...](/supply-chain/pim/tasks/create-hierarchy-product-classification.md)[dodieties uz Sadaļu Preču klasifikācijas hierarhijas izveide un preces klasificēšana, izmantojot kategoriju hierarhijas.](/supply-chain/pim/tasks/classify-product-category-hierarchies.md)

Pēc kategoriju hierarhijas izveides hierarhija jāpiešķir vienam vai vairākiem tipiem. Lai pārdošanas pasūtījumos lietotu kategoriju hierarhiju, kategorija ir jāpiešķir pārdošanas kategoriju hierarhijas tipam. Papildinformāciju skatiet par [kategoriju hierarhijām](/dynamicsax-2012/appuser-itpro/about-category-hierarchies.md).

## <a name="create-revenue-posting-by-sales-category"></a>Izveidot ieņēmumu grāmatošanu pēc pārdošanas kategorijas

Lai piešķirtu Virsgrāmatas grāmatojumus pārdošanas pasūtījumam, kas balstīts uz pārdošanas kategoriju, rīkojieties šādi:

1. Doties uz **Krājumu vadība** > **Iestatīšana** > **Grāmatojums** > **Grāmatošana**.
2. Atlasiet cilni **Pārdošana**.
3. Atlasiet radio pogu grāmatošanas tipam, ko vēlaties konfigurēt (piemēram, **Ieņēmumi**).
4. Atlasiet **Jauna**.
5. Laukā **Krājuma kods** atlasiet **Kategorija**.
6. Lietojiet **lauku Kategorijas** relācija, lai atlasītu kategoriju grāmatošanas metodei.
7. Laukā **Konta kods atlasiet opciju Tabulai** **, Grupai** **vai** Visiem **.** Piemēram, lai grāmatošanas metodi piemērotu visiem debitoriem, atlasiet **Visi**.
   - **Ja 6.** solī atlasījāt **Tabulu**, konta relācijas laukā atlasiet konkrētu kreditora kodu grāmatošanas **metodei**.
   - **Ja 6.** solī atlasījāt Grupu **, atlasiet kreditoru grupu** grāmatošanas metodei **laukā Kontu** saistība.
   - Ja 6. **solī** atlasījāt **Viss, konta relācijas** lauks tiks atstāts tukšs.

8. Lai asociētu īpašu nodokļu grupu, kam ir atlasīts grāmatošanas tips, atlasiet **PVN grupu**. Ja šo lauku atstāj tukšu, grāmatošanas tips attiecas uz visām esošajām PVN grupām. Grāmatošana, kura ir norādīta PVN grupām, attiecas tikai uz darbībām, kuras ir veiktas pārdošanai un pirkšanai.

9. Laukā **Galvenais** konts norādiet konta numuru, kurā grāmatot konta tipu. Atlasiet vienu no esošajiem konta numuriem kontu plānā.
