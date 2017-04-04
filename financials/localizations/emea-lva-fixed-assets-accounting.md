---
title: " Pamatlīdzekļu uzskaite nodokļu aprēķinam"
description: "Šajā tēmā ir sniegta informācija par nodokļu nolietojuma funkcionalitātei Latvija."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetBookTable, AssetDepreciationProfile, AssetTable, AssetTaxDepreciation
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264374
ms.assetid: cbf94106-2c1b-45dd-8734-18a2a56a4682
ms.search.region: Latvia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 2947747c583955b73cd4fb0b9ad74982bf51d896
ms.lasthandoff: 03/31/2017


---

# <a name="fixed-assets-accounting-for-tax-purposes"></a> Pamatlīdzekļu uzskaite nodokļu aprēķinam

Šajā tēmā ir sniegta informācija par nodokļu nolietojuma funkcionalitātei, Latvija, tai skaitā nodokļu nolietojuma iestatīšanai un aprēķināšanai un nodokļu nolietojums pārskata drukāšana. 
> [!NOTE]
> Nodokļu nolietojuma strādā ar vērtību modeļus. Vērtības modelī un nolietojuma grāmatā ir sapludināti vienotā koncepcija, ko sauc *grāmatu.* Lai iegūtu papildinformāciju, skatiet [pamatlīdzekļa vērtības modeli un nolietojuma grāmatu sapludināšanas](../fixed-assets/fixed-asset-value-model-depreciation-book-merge.md).

## <a name="set-up-a-depreciation-profile"></a>Iestatiet nolietojuma profilu, kas
Iestatot nolietojuma tabulu, apsveriet šādas iespējas.

|                       |                                                                                                                                                                                                                                                                                                                    |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Depreciation year** | Izvēlieties, kāda veida, ko izmanto, lai aprēķinātu nolietojuma gadu. Nolietojuma aprēķina gads un perioda biežums ir saistīti. Tāpēc iespējas **perioda biežums** lauks ir atkarīgs no **nolietojuma aprēķina gads** lauka vērtību.                                                                                 |
| **Period frequency**  | Atlasiet virsgrāmatas uzkrājumu biežumu kalendārā gada vai finanšu gada laikā. Šajā laukā rādītās opcijas ir atkarīgas no jūsu atlasītā nolietojuma gada. Ja esat atlasījis **Kalendārs** kā nolietojuma aprēķina gadu, iespējas ir **gada**, **ikmēneša**, **ceturkšņa**, **pusgada**. |
| **Full depreciation** | Atzīmējiet šo opciju, lai pamatlīdzekli uzskatītu par pilnīgi nolietotu, kad atlikušais lietošanas ilgums ir 0 (nulle).                                                                                                                                                                                                             |

<!---To set up a depreciation profile, complete the following procedure, [Set up and create depreciation profiles](http://ax.help.dynamics.com/en/wiki/set-up-and-create-depreciation-profiles/).-->

## <a name="set-up-books"></a>Grāmatas
Izmantojiet **grāmatām** lapu, lai noteiktu nodokļu kategorijai. Grāmatas tiek saukti arī par nodokļu kategorijas. Lai izveidotu grāmatu, atlasiet nolietojuma tabulu, kas ir **atlikumu samazinošā** atlasīto **metodi** lauku **nolietojuma profilos** lapā. **Grāmatām** lapa par juridiskām personām Latvija ietver šādus laukus:

-   **Grāmatošanas slānis** – atlasiet **nodokļu** šajā jomā.
-   **Apkopot kategorijai** – atlasiet šo opciju, ja nodokļu nolietojums būtu apkopoti un aprēķinātas visiem pamatlīdzekļiem, kas ir pašā grāmatā atlasīti **kategorija** lauks.
-   **Nodokļu koeficientiem** -var iestatīt nodokļa koeficientus katram koeficients iegādes cenu regulēt finanšu gadam.

<!---For more information about setting up books, see [Set up depreciation books](http://ax.help.dynamics.com/en/wiki/set-up-depreciation-books/).-->

### <a name="set-up-tax-depreciation-calculation"></a>Iestatīt nodokļu nolietojuma aprēķins

Iestatīt nodokļu nolietojuma aprēķins par **Pamatlīdzekļi** lapu, atlasiet pamatlīdzekli. Tad, **vispārējā** FastTab, atlasiet **grāmatu**, **kategorija** lauks. Pamatlīdzeklis ir tikai viena grāmata, kas saistīta ar pašreizējo grāmatošanas slānis. 
> [!NOTE]
> Šajā laukā norādīts grāmatas ieraksta grāmatošanas slānis vērtība vienāda ar nodokli tikai.

## <a name="calculate-tax-depreciation"></a>Nodokļu nolietojuma aprēķins
Aprēķināt pamatlīdzekļa nolietojumu nodokļa aprēķina, no **nodokļu nolietojumam** lapu, izveidot jaunu taksācijas periodā izmanto atskaišu veidošanai.

|                   |                                                                                                                                                                |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field name**    | **Description**                                                                                                                                                |
| **Start date**    | Atlasiet datumu, no kura periods ir derīgs.                                                                                                                |
| **End date**      | Atlasiet datumu, līdz kuram ir derīgs laika posmā.                                                                                                               |
| **Period status** | Atlasiet perioda statuss (**Open** vai **slēgts**). Ja statuss ir **slēgts**, **kategorijas** par **kategoriju detaļas** FastTab nevar pievienot vai dzēst. |

Par **kategoriju detaļas** FastTab, izvēlieties grāmatu **kategorija** lauku, kuru vēlaties aprēķināt nolietojumu nodokļa. Noklikšķiniet uz **aprēķināt** nodokļu nolietojuma aprēķināšanai. Nodokļu nolietojuma aprēķina vai nu atsevišķie pamatlīdzekļi vai kopsavilkuma informāciju no visiem pamatlīdzekļiem, kas piešķirti vienas kategorijas pamatlīdzekļu nodokļu pamatots. Aprēķins tiek veikts, pamatojoties uz nodokļa koeficients no atlasīto grāmatu un grāmatvedības datus par pamatlīdzekļu grāmatām, kas saistīti ar atlasīto grāmatu **kategorija** lauks.

|                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------|
| **Aprēķinu formulas**                                                                                         |
| Koriģēt vērtību = sākuma bilance + vērtības korekcijas - apglabāšanas + iegādes cena \*iegādes koeficients |
| Nodokļu nolietojuma summa = vērtību koriģē \*bāze nolietojuma \*2 /100 \*mēnešu periodu skaits / 12        |
| Beigu atlikums = koriģēt vērtību – nodokļu nolietojuma summa                                                           |
| Sākuma atlikums (perioda nolietojums) = beigu bilance (iepriekšējās nolietojuma aprēķina periods)          |

Lai skatītu nolietojumu nodokļu detaļas, noklikšķiniet uz **nodokļu nolietojuma informāciju** atvērt **nodokļu nolietojuma informāciju** lapā.

## <a name="print-the-tax-depreciation-report"></a>Drukāt nodokļu nolietojuma pārskats
**Nodokļu nolietojumam** pārskats sniedz latviešu lietotājiem ar nodokļu pārskatam, kas attiecas uz pamatlīdzekļiem uzņēmumā. Lai izdrukātu atskaiti, dodieties uz **nodokļu nolietojuma aprēķina** lapu, izvēlieties konkrētu ierakstu apkopot pie **kategorija** līmeņa. Noklikšķiniet uz **nodokļu nolietojuma atskaiti** kategorijām, kas tiek apkopoti, izmantojot **nodokļu nolietojumam** atskaite.


