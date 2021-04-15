---
title: Darbs ar veidnēm
description: Šajā tēmā ir aprakstīts, kā strādāt ar veidnēm programmā Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 96a8cbfd208095833514f374c060bb2d43781913
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793853"
---
# <a name="work-with-templates"></a>Darbs ar veidnēm

[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīts, kā strādāt ar veidnēm programmā Microsoft Dynamics 365 Commerce.

Kā tika apspriests sadaļā [Veidņu un izkārtojumu pārskats](templates-layouts-overview.md), veidnes nosaka opciju kopu, kas ir pieejama lejupstraumes autoriem. Veidnes noder uzņēmuma tīmekļa autorēšanas grupai vairāku iemeslu dēļ, un labi strukturētas veidnes var palīdzēt ar tālāk norādītajiem mērķiem.

- Vienkāršojiet satura redaktora lomu ikdienas autorēšanas pieredzi.

    - Filtra moduļa opcijas, lai konkrētai lapas sekcijai tiktu parādīti tikai saistītie moduļi. (Piemēram, veidnes mārketinga sadaļu var konfigurēt, lai filtrētu neatbilstošos moduļus, kurus nekad nedrīkst izmantot šajā kontekstā, un to klātesamība tikai sarežģī satura autorēšanas uzdevumus.)
    - Konfigurēt noklusējuma moduļa iestatījumu, lai palīdzētu uzlabot autorēšanas efektivitāti.
    - Nosakiet noklusējuma lappušu fragmentus, lai palīdzētu uzlabot autorēšanas efektivitāti. (Piemēram, galveņu un kājeņu fragmenti veidnē tiks automātiski rādīti katrā lejupstraumes lapā.)

- Uzturēt uzņēmuma vietnes pēc zīmola, definējot apstiprinātu moduļa izkārtojuma un konfigurācijas opciju kopu.

    > [!TIP] 
    > Veiksmīgas e-komercijas vietnes nodrošina klientus ar pazīstamiem, atkārtojamiem un zīmolam atbilstošiem lietotāja pieredzes (UX) dizaina paraugiem. Lietojot veidnes, jūs palīdzēsiet kontrolēt konsekvenci visā jūsu vietnē.

- Uzlabot meklētājprogrammas optimizācijas (SEO) rezultātus, nodrošinot atkārtojamas un programmiski definētas lapas definīcijas un metadatus.

> [!NOTE]
> Lai gan veidnes ir veidotas, lai kontrolētu konsekvenci visā vietnē, tās teorētiski var konfigurēt tā, lai tās neieviestu konsekvenci. Zīmola un vietnes administratori var definēt jebkuru lapas lapu mainīguma līmeni. Piemēram, veidni var atstāt pavisam atvērtu, lai satura autori varētu izveidot jebkādu lapas dizainu, kādu tie izvēlas. Šādā gadījumā neviens no iepriekšējā sarakstā minētajiem ieguvumiem nav piemērojams.

## <a name="modify-a-template"></a>Modificēt veidni

Veidnes tiek modificētas, izmantojot veidnes redaktoru.

Lai atvērtu veidnes redaktoru, veiciet vienu no tālāk norādītajām darbībām.

- Jūsu vietnes navigācijas rūtī atlasiet **Veidnes** un pēc tam atlasiet modificējamo veidni.
- Esošās lapas redaktorā atlasiet augšējo zaru pa kreisi esošajā struktūras kokā. Pēc tam rekvizītu rūts labajā pusē atlasiet **Rediģēt veidni**.

Struktūras koka skats kreisajā pusē rāda moduļu opcijas un struktūras, kas ir pieejamas atvasinātajiem izkārtojumiem un lapām. Atlasot moduli struktūras kokā, varat skatīt veidnes rekvizītus atlasītajam modulim rekvizītu rūtī labajā pusē. Daži no šiem rekvizītiem ir unikāli veidnes rediģēšanai. Tabulā ir sniegts šo rekvizītu apraksts.

| Rekvizīta nosaukums | Apraksts |
|---|---|
| Min. atkārtošanās skaits | Šis rekvizīts definē minimālo atkārtojumu skaitu atlasītajam modulim. Piemēram, ja vērtība ir iestatīta uz **1**, tad modulis ir nepieciešams lejupstraumes autoriem, bet, ja vērtība ir iestatīta uz **0** (nulle), modulis nav obligāts. |
| Maks. atkārtošanās skaits | Šis rekvizīts definē maksimālo atkārtojumu skaitu atlasītajam modulim. Piemēram, ja vērtība ir iestatīta uz **1**, moduli var pievienot tikai vienu reizi. |
| Minimālie moduļi (konteineri) | Moduļos, kas ietver citus moduļus (*konteineru moduļi*), šis rekvizīts nosaka minimālo kopējo moduļu skaitu, kas jāpievieno kā apakšelementi. Piemēram, karuseļa modulim vērtība var būt iestatīta uz skaitli, kas ir lielāks par 1. |
| Maksimālie moduļi (konteineri) | Konteineru moduļiem šis rekvizīts nosaka maksimālo kopējo moduļu skaitu, kas jāpievieno kā apakšelementi. Piemēram, karuseļa modulim vērtība var būt iestatīta uz skaitli, kas ir mazāks par 10. |
| Bloķēts | **Bloķēta** Būla vadīkla tiek parādīta blakus visiem pamata moduļa rekvizītiem. Tas ļauj veidnes autoram bloķēt moduļa iestatījumus veidnē. Moduļa iestatījumu, kas ir bloķēts, nevar ignorēt neviens no pakārtotajiem izkārtojumiem vai lapām. Tas kļūst par centralizēti rediģējamu rekvizīta vērtību visiem izkārtojumiem un lapām, kurās tiek izmantota veidne. |

## <a name="create-a-new-template"></a>Izveidot jaunu veidni

Lai izveidotu jaunu veidni, veiciet tālāk norādītās darbības.

1. Jūsu vietnes navigācijas rūtī atlasiet **Veidnes**, lai atvērtu veidni inspektora skatā.
1. Atlasiet **Jauna veidne**.
1. Veidnes izveides dialoglodziņā ievadiet nosaukumu un veidnes aprakstu. Ievadītās vērtības tiks rādītas autoriem, kad viņi izveido jaunas lapas. Tāpēc ievadiet metadatus, kas noderēs lapu autoriem. Piemēram, ievadiet **Izmantojiet šo veidni, lai izveidotu vispārīgas mārketinga lapas** kā aprakstu. Šos metadatus vēlāk var rediģēt.
1. Atlasiet **Labi**, lai izveidotu jaunu veidni un atvērtu veidnes redaktoru. Veidnes redaktorā tiek rādīts struktūras koks kreisajā pusē un rekvizītu rūts labajā pusē.
1. Struktūras kokā izvērsiet zarus un atlasiet **HTML galveno** slotu.
1. Ja šajā slotā vēl nav neviena moduļa, izvēlieties daudzpunktes pogu (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet **Noklusējuma lapas kopsavilkums** un tad atlasiet **Labi**.
1. Struktūras kokā atlasiet jauno moduli un pēc tam rekvizītu rūtī ievadiet visus noklusējuma iestatījumus, kas jākonfigurē automātiski visām veidnes pakārtotajām lapām. Ja nevēlaties nekādus noklusējuma iestatījumus, atstājiet vērtības tukšas.
1. Struktūras kokā atlasiet slotu **Pamatteksts**, atlasiet daudzpunktes pogu un pēc tam atlasiet **Pievienot moduli**.
1. Atlasiet lapas konteinera moduli (var būt tikai viena opcija) un pēc tam atlasiet **Labi**.

Jaunās lapas konteinera modulī redzēsiet jaunu slotu kopu **(Galvene**, **Galvenais** utt.). Šeit varat pievienot un konfigurēt moduļu opcijas, kas būs pieejamas autoriem, veidojot lapas no šīs veidnes. Pēc noklusējuma, ja slotam netiek pievienoti moduļi, visi pieejamie moduļu tipi tiek atbalstīti šim slotam.

Tagad veidne ir tehniski derīga, un to var saglabāt, atdot un izmantot, lai izveidotu jaunas lapas. Tomēr nākamajās trīs sadaļās ir aprakstīti daži citi noklusējuma iestatījumi, kurus, iespējams, vēlaties konfigurēt vispirms.

## <a name="add-a-header-and-a-footer"></a>Galvenes un kājenes pievienošana

Ja vietnei jau ir galvenes fragments, izpildiet šīs darbības, lai pievienotu veidnei galveni un kājeni.

1. Struktūras kokā izvērsiet slotu **Pamatteksts** un tā pakārtotās lapas moduli.
1. Atlasiet slotu **Galvene**.
1. Atlasiet daudzpunktes pogu HTML slotam **Galvene** un pēc tam atlasiet **Pievienot fragmentu**.
1. Meklējiet un atlasiet savas vietnes galvenes fragmentu un pēc tam atlasiet **Labi**.

Visas lapas, kas izmanto šo veidni, tagad automātiski pārmantos šo galvenes fragmentu.

Ja vietnē vēl nav ietverts galvenes fragments, skatiet sadaļu [Fragmenta izveide](work-with-fragments.md#create-a-fragment), lai iegūtu informāciju par to, kā to izveidot, un pēc tam pabeidziet iepriekšējo procedūru.

## <a name="change-the-template-theme"></a>Veidnes dizaina maiņa

Lai iestatītu noklusējuma dizainu visām lapām, kurās tiek izmantota veidne, veiciet tālāk norādītās darbības.

1. Lapas struktūras kokā kreisajā pusē izvērsiet slotu **Pamatteksts**.
1. Slotā **Pamatteksts** atlasiet lapas konteinera moduli (piemēram, **Noklusējuma lapa**).
1. Rekvizītu rūtī labajā pusē, lauka **Dizains** atlasiet dizainu.

Pēc noklusējuma visās jaunajās lapās tiks lietots atlasītais dizains. Lai novērstu to, ka lapas ignorē šo iestatījumu izkārtojuma vai lappuses līmenī, iestatiet **Bloķētās** Būla vadīklas vērtību kā **Patiess**.

## <a name="add-a-script-to-a-template"></a>Skripta pievienošana veidnei

Jūsu veidnei varat pievienot HTML **&lt;skripta&gt;** elementus, kas ietver JavaScript. Šādā veidā varat nodrošināt noklusējuma skripta uzvedību jūsu lapas HTML galvenajai, pamatteksta sākuma un pamatteksta beigu sadaļai.

Lai veidnei pievienotu skriptu, veiciet tālāk norādīto.

1. Struktūras kokā pa kreisi atlasiet slotu, kur vēlaties pievienot **&lt;skripta&gt;** elementu (piemēram, HTML pamatteksta, ķermeņa sākumu vai pamatteksta beigas).
1. Atlasiet daudzpunktes pogu slotam un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet skripta moduli (piemēram, **Ārējais skripts** vai **Iekļautais skripts**).
1. Rekvizītu rūtī labajā pusē atbilstošajā skripta rekvizīta vadīklā (piemēram, **Iekļautais skripts** vai **Skripta tagi**) ievadiet savu skriptu.
1. Rekvizītu rūtī ievadiet jebkurus citus neobligātos iestatījumus, ko vēlaties konfigurēt.

> [!TIP]
> Ja vēlaties atkārtoti izmantot visus skripta moduļus citās veidnēs, varat tos pārvērst par fragmentiem. Šādā veidā jūs palīdzēsiet padarīt autorēšanas procesu efektīvāku, un jūs centralizējat atjaunināšanas procesu. Lai iegūtu informāciju par to, kā skriptu moduli pārvērst par fragmentu, skatiet sadaļu [Esošas moduļa konfigurācijas kā fragmenta saglabāšana](work-with-fragments.md#save-an-existing-module-configuration-as-a-fragment).

## <a name="save-check-in-preview-and-publish-a-template"></a>Saglabājiet, atdodiet, priekšskatiet un publicējiet veidni

Lai saglabātu un atdotu veidni, izpildiet tālāk aprakstītās darbības.

1. Veidnes redaktora augšā atlasiet **Saglabāt**. Saglabātās izmaiņas neietekmē lejupstraumes lapas, kamēr tās nav atdotas.
1. Atlasiet **Beigt rediģēšanu**. Jūsu veiktās izmaiņas tagad ir redzamas lejupstraumes darbplūsmām.

Lai priekšskatītu izmaiņas, vai nu atveriet esošu lapu, kas izmanto veidni, vai izveidojiet jaunu lapu no veidnes.

Pēc tam, kad veidnes izmaiņas ir priekšskatītas, veiciet vienu no tālāk norādītajām darbībām, lai publicētu veidni jūsu tiešsaistes vietnē.

* Dodieties uz **Veidnes**, atlasiet veidni un pēc tam atlasiet **Publicēt**.
* Atlasiet izkārtojuma nosaukumu, lai atvērtu izkārtojuma redaktoru, un tad atlasiet **Publlicēt**.
* Publicējiet lapu, kurā ir atsauce uz nepublicēto veidni. Veidne tiek publicēta automātiski.

> [!WARNING]
> Publicējot veidni vai jebkuru citu satura pārvaldības sistēmas (CMS) vienumu, tas ir redzams internetā. Nepublicējiet dokumentus vai līdzekļus, kamēr neesat gatavs tos publiskot. Dokumentu versijas, kas ir saglabātas un atdotas, bet nav publicētas, ir redzamas tikai autentificētiem sistēmas lietotājiem.

## <a name="additional-resources"></a>Papildu resursi

[Pārskats par veidnēm un izkārtojumiem](templates-layouts-overview.md)

[Darbs ar iepriekš iestatītiem izkārtojumiem](work-with-layouts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
