---
title: Līdzekļu defektu analīze
description: Šajā tēmā ir paskaidrota līdzekļu kļūmju analīze programmā Asset Management.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectFaultCalculate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e911f7ca3b67acd9d5a1b170d8c99135da730847
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432893"
---
# <a name="asset-fault-analysis"></a>Līdzekļu defektu analīze

[!include [banner](../../includes/banner.md)]

 

Programmā Asset Management varat analizēt reģistrētās kļūdas, lai iegūtu pārskatu par kopējo kļūmju skaitu, kas reģistrēts noteiktā laika posmā. Kļūdu reģistrācijas var analizēt no dažādiem aspektiem, piemēram, koncentrējoties uz līdzekļiem, līdzekļu veidiem, funkcionālajiem novietojumiem, kļūmju simptomiem vai kļūmju veidiem.

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Pieprasījumi** > **Līdzekļu kļūme** > **Līdzekļu kļūmes analīze**.

2. Dialogā **Līdzekļu kļūmes analīzes aprēķins** varat izmantot lauku **Līmenis**, lai noteiktu, cik detalizētas vēlaties līdzekļu kļūmes rindas attiecībā uz funkcionālo novietojumu. 

    Piemēram, ja laukā ievadāt ciparu „1” un jums ir vairāklīmeņu funkcionālā novietojuma struktūra, visas aktīvu kļūmju rindas funkcionālajam novietojumam tiks uzrādītas augstākajā līmenī, tāpēc stundas rindā var tikt pievienotas no funkcionāliem novietojumiem, kas atrodas zemākā līmenī. 
        
    Ja laukā **Līmenis** ievadāt ciparu „0”, jūs redzēsit detalizētu rezultātu, kas uzrādīs visas līdzekļu kļūmju rindas visos funkcionālā novietojuma līmeņos, ar kuriem tās ir saistītas.

3. Ja vēlaties ierobežot meklēšanu, varat izvēlēties konkrētus līdzekļus, kļūmju datumus un kļūmju iemeslus, un kļūmju labojumus kopsavilkuma cilnē **Iekļaujamie ieraksti**.

4. Noklikšķiniet uz **Labi**, lai sāktu aprēķināšanu.

5. Cilnē **Līdzekļu kļūmju analīze** noklikšķiniet uz vienas vai vairākām pogām **Grupēt pēc**, lai parādītu detalizētas informācijas līmeni, kādu vēlaties redzēt. Aktivizētās pogas ir izceltas. Noklikšķiniet uz pogas, lai to aktivizētu vai deaktivizētu.

6. Noklikšķiniet uz **Atjaunināt aprēķinus**, lai parādītu savas atlases ekrānā. 

>[!NOTE]
>Katru reizi, kad aktivizējat vai deaktivizējat pogu **Grupēc pēc**, neaizmirstiet noklikšķināt uz pogas **Atjaunināt aprēķinus**. Tas tādēļ, ka tiek apstrādāts liels datu daudzums, atkārtoti pārrēķinot kļūmes iespēju.

## <a name="examples"></a>Piemēri

Ir daudzi veidi, kā analizēt kļūmju reģistrācijas. Šajā sadaļā ir sniegti pieci piemēri tam, kā dažādas datu atlases var sniegt dziļāku ieskatu un detalizētāku informāciju, analizējot kļūmju reģistrācijas.

### <a name="group-by-symptoms"></a>Grupēt pēc simptomiem

Attēluzņēmumā šeit tālāk ir atlasīta tikai poga **Simptoms**.

- Kļūmes var reģistrēt trim kļūmju simptomiem: „Gaisa sūce”, „Izsists drošinātājs”, „Iekārta aizsprostojusies”.  
- Slejā **Iespējamība %** visas procentu vērtības kopā sasniedz 100 %. Iespējamība balstīta uz visu **Simptomu** reģistrācijām šai kļūmju analīzei.

![1. attēls](media/06-controlling-and-reporting.png)

### <a name="group-by-symptoms-and-time-period"></a>Grupēt pēc simptomiem un laika perioda

Šajā ekrānuzņēmumā pievienots **Gads** un **Mēnesis**, lai parādītu, kā var skatīt kļūmju reģistrācijas noteikta laika posmā.

- Kļūmju simptomus tagad rāda kā reģistrācijas gadā/mēnesī.  
- Slejā **Iespējamība %**, ja pievienojat visas procentu vērtības katram mēnesim, kopā tās sasniedz 100 %. Iespējamība balstīta uz **Simptomu** reģistrācijām šai kļūmju analīzei. Ja jums ir daudz rindu līdzeklim, bet rindai izceļas liels procentu skaits, tā ir norāde, ka ir kļūmes simptoms, kas jāizpēta sīkāk, lai ierobežotu reģistrāciju skaitu šim kļūmes simptomam.

![2. attēls](media/07-controlling-and-reporting.png)

### <a name="group-by-multiple-symptoms-and-assets"></a>Grupēt pēc vairākiem simptomiem un līdzekļiem

Līdzekļu un līdzekļu veida kombinācija tiek izmantota, kā pamats šajos trijos ekrānuzņēmumos parādītajiem aprēķiniem, un tiem samazinās detalizācijas līmenis.  

Vispārīgi pogas Darbību rūts grupās **Grupēt pēc datuma**, **Grupēt pēc līdzekļa**, **Grupēt pēc funkcionālā novietojums**, kā arī poga **Kļūme** (Kļūmes ID) satur periodus vai līdzekļu saistības. Pogas **Simptoms**, **Joma**, **Veids**, **Iemesls** un **Labojums** ir kategorizācijas, ko izmanto kļūmju pārvaldībā, lai analizētu līdzekļu kļūmes un noteiktu problēmu jomas.  

**Grupēt pēc simptoma, līdzekļa un līdzekļa veida**

Šajā ekrānuzņēmumā pievienots **Līdzeklis** un **Līdzekļa veids**, lai parādītu detalizētāku informāciju par kļūmju reģistrācijām.

- Kļūmju simptomi tagad ir sadalīti kombinācijās **Līdzekļi** / **Līdzekļu veids** / **Simptoms**.  
- Slejā **Iespējamība %**, ja pievienojat visas procentu vērtības kombinācijai **Līdzeklis** / **Līdzekļa veids** / **Simptoms**, kopā tā sasniedz 100 %. Iespējamība balstīta uz **Simptomu** reģistrācijām šai kļūmju analīzei. Ja jums ir daudz rindu līdzeklim, bet rindai izceļas liels procentu skaits, tā ir norāde, ka ir kļūmes simptoms, kas jāizpēta sīkāk, lai ierobežotu reģistrāciju skaitu šim kļūmes simptomam.

![3. attēls](media/08-controlling-and-reporting.png)

**Grupēt pēc diviem simptomiem, līdzekļa un līdzekļa veida**

Šajā ekrānuzņēmumā **Simptomam** pievienota **Joma**, **Līdzeklis** un **Līdzekļa veids**, lai parādītu detalizētāku informāciju par kļūmju reģistrācijām.

- Slejā **Iespējamība %**, ja pievienojat līdzeklim visas procentu vērtības kombinācijai **Līdzeklis** / **Līdzekļa veids** / **Simptoms**, kopā tā sasniedz 100 %. Iespējamība balstīta uz kombināciju **Simptoms** un **Joma** šai kļūmju analīzei. Ja jums ir daudz rindu līdzeklim, bet rindai izceļas liels procentu skaits, tā ir norāde, ka ir kļūmes joma, kas jāizpēta sīkāk, lai ierobežotu reģistrāciju skaitu šai kļūmes jomai.  

![4. attēls](media/09-controlling-and-reporting.png)

**Grupēt pēc trim simptomiem, līdzekļa un līdzekļa veida**

Šajā ekrāuzņēmumā pievienots **Veids**, un šajā piemērā parādīts visdetalizētākais aprēķins,
 
- Slejā **Iespējamība %**, ja pievienojat līdzeklim visas procentu vērtības kombinācijai **Līdzeklis** / **Līdzekļa veids** / **Simptoms**, kopā tā sasniedz 100 %. Iespējamība balstīta uz kombināciju **Simptoms** un **Joma**, un **Veids** šai kļūmju analīzei. Ja jums ir daudz rindu līdzeklim, bet rindai izceļas liels procentu skaits, tā ir norāde, ka ir kļūmes veids, kas jāizpēta sīkāk, lai ierobežotu reģistrāciju skaitu šim kļūmes veidam.

![5. attēls](media/10-controlling-and-reporting.png)


>[!NOTE]
>Lai pārskatītu visas kļūmju reģistrācijas, kas izveidotas darbu pasūtījumiem un uzturēšanas pieprasījumiem, klikšķiniet uz **Līdzekļu pārvaldība** > **Pieprasījumi** > **Līdzekļu kļūme** > **Līdzekļu kļūmes**. Lapā **Līdzekļu kļūmes** atlasiet līdzekļu kļūmes reģistrāciju un izvērsiet rūti **Saistītā informācija**, lai redzētu informāciju par saistīto darba pasūtījumu vai uzturēšanas pieprasījumu



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]