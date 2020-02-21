---
title: Mazumtirdzniecības veikala transakciju rediģēšana un auditēšana
description: Šajā tēmā ir aprakstīta veikala transakciju rediģēšanas un auditēšanas funkcionalitāte.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 97211ee36dbaa704d3a967e9b742ff1cae708707
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004393"
---
# <a name="edit-and-audit-retail-store-transactions"></a>Mazumtirdzniecības veikala transakciju rediģēšana un auditēšana

[!include [banner](includes/banner.md)]



Dynamics 365 Commerce klienti izmanto pirmās puses, kā arī trešās puses pārdošanas punkta (POS) programmas. Izmantojot pirmās puses POS programmu, veikala transakcijas tiek importētas komponentā Headquarters no kanāliem ar pakešveida apstrādes palīdzību. Izmantojot trešās puses programmas, transakcijas tiek importētas komponentā Headquarters ar integrācijas palīdzību. Abos gadījumos pēc transakciju importēšanas komponentā Headquarters ir jāizpilda konsekvences pārbaudes process, kas veic vairākas transakciju pārbaudes, lai komponentā Headquarters grāmatojamajā pārskatā tiktu importētas tikai sekmīgi validētās transakcijas. 

Tirdzniecības transakcijas neiztur pārbaudi dažādu iemeslu dēļ. Piemēram, kļūda integrācijas kodā vai kļūda POS programmā var izraisīt pretrunīgus datus vai lietotāja kļūdu, piemēram, preces dzēšanu pēc tās sinhronizēšanas ar kanālu vai finanšu perioda slēgšanu bez tirdzniecības transakciju grāmatošanas šim periodam.

Lai gan šīs transakcijas tiek atzīmētas ar karodziņu un izslēgtas no pārskatiem, transakcijas var traucēt klienta tirdzniecības pārdošanas ikdienas grāmatošanas procesu.

Programmā Commerce varat rediģēt konkrētas transakcijas, kuras neiztur pārbaudi, saglabājot visu izmaiņu auditu. 

## <a name="edit-and-audit-transactions"></a>Transakciju rediģēšana un auditēšana

Retail versijā 10.0.5 var rediģēt tikai transakcijas, kas ir saistītas ar pārdošanu skaidrā naudā bez piegādes, piemēram, pārdošanas un atgriešanas transakcijas. Debitoru pasūtījumu vai tiešsaistes pasūtījumu rediģēšana netiek atbalstīta. Retail versijā 10.0.6 un jaunākās versijās tiek atbalstīta arī skaidras naudas pārvaldības transakciju rediģēšana.

1. Instalējiet Dynamics Excel pievienojumprogrammu.

2. Dodieties uz darbvietu **Veikala finanses**. Elements **Transakciju validācijas kļūmes** nodrošina iepriekš filtrētu tās transakcijas formas skatu, kura neatbilda vienai vai vairākām validēšanas kārtulām.
 
3. Atveriet formu. Noklikšķiniet uz ieraksta, kuru neizdevās validēt, pēc tam noklikšķiniet uz **Office pievienojumprogramma** un tad uz **Rediģēt atlasīto transakciju**. Tiek atvērts Excel fails ar detalizētu informāciju par atlasīto transakciju ar tālāk norādītajām darblapām.

    - Rindas: šī darblapa satur transakcijas virsrakstu, preču rindas un saistītos datus.
    - Maksājumi: šī darblapa satur detalizētu informāciju par maksājumu rindām attiecībā uz transakciju.
    - Atlaides: šī darblapa satur detalizētu informāciju par atlaidēm attiecībā uz transakciju.
    - Nodokļi: šī darblapa satur detalizētu informāciju par nodokļiem attiecībā uz transakciju.
    - Izmaksas: šī darblapa satur ar izmaksām saistītus datus attiecībā uz transakciju.

4. Excel failā varat modificēt attiecīgos laukus un pēc tam augšupielādēt datus atpakaļ komponentā Headquarters, izmantojot Dynamics Excel pievienojumprogrammas publicēšanas funkcionalitāti. Pēc publicēšanas izmaiņas tiks atspoguļotas sistēmā. Publicēšanas laikā lietotāju veiktajām izmaiņām validācija netiek veikta.

5. Pilnīgus auditācijas pierakstus var skatīt, galvenē **Mazumtirdzniecības transakcija** (galvenes līmeņa izmaiņu gadījumā) un attiecīgajā sadaļā un ierakstā atbilstošajā transakciju lapā noklikšķinot uz **Skatīt auditācijas pierakstus**. Piemēram, visas izmaiņas saistībā ar pārdošanas rindām tiks rādītas lapā **Pārdošanas transakcijas**, izmaiņas saistībā ar maksājumiem būs redzamas lapā **Maksājumu transakcijas** utt. Saistībā ar izmaiņām tiem uzturēta tālāk norādītā detalizētā informācija par auditu.

   - Modificēšanas datums un laiks
   - Lauks 
   - Vecā vērtība
   - Jaunā vērtība
   - Modificēja

6. Kad izmaiņas ir veiktas un publicētas, palaidiet opciju **Validēt veikala transakcijas** vēlreiz, lai pārbaudītu, vai veiktās izmaiņas ir saskaņotas un derīgas.

> [!NOTE]
> Varat rediģēt tikai tās transakcijas, kuru validācija neizdevās. Ja vēlaties rediģēt transakcijas, kuru validācija izdevās, mainiet attiecīgās transakcijas validācijas statusu uz **Kļūda** vai **Nav** un pēc tam varēsit to rediģēt. 


## <a name="bulk-edit-transactions"></a>Transakciju lielapjoma rediģēšana

Retail versijā 10.0.6 un jaunākās versijās tiek atbalstīta opcija transakciju lielapjoma rediģēšanai pārskata līmenī. 

1. Izmantojiet Excel pievienojumprogrammu, lai atvērtu pārskatu ar transakcijām, kuras vēlaties modificēt, izmantojot iepriekš norādīto 1.—3. darbību.

2. Izvēlieties vienu no tālāk pieejamajām opcijām.

    - **Rediģēt skaidras naudas un pārvedumu transakcijas**. Šī opcija ļauj rediģēt visas pārskatā iekļautās skaidras naudas un pārvedumu transakcijas. Pieejamas tālāk norādītās Excel darblapas.
    
       - **Transakcija**: šī darblapa satur visu pārdošanas transakciju galvenes līmeņa informāciju.
       - **Pārdošanas transakcija**: šī darblapa satur visu pārdošanas transakciju rindu līmeņa informāciju.
       - **Maksājumu transakcijas**: šī darblapa satur visu pārdošanas transakciju pārdošanas rindu informāciju.
       - **Atlaižu transakcijas**: šī darblapa satur visu pārdošanas transakciju atlaižu rindu informāciju.
       - **Nodokļu transakcijas**: šī darblapa satur visu pārdošanas transakciju nodokļu rindu informāciju.
       - **Izmaksu transakcijas**: šī darblapa satur visu pārdošanas transakciju izmaksu rindu informāciju.

    - **Rediģēt skaidras naudas pārvaldības transakcijas**. Šī opcija ļauj rediģēt visas pārskatā iekļautās skaidras naudas pārvaldības transakcijas. Pieejamas tālāk norādītās Excel darblapas.
     
       - **Transakcija**: šī darblapa satur visu skaidras naudas pārvaldības transakciju galvenes līmeņa informāciju.
       - **Norēķinu transakcijas noguldījumiem bankā**: šī darblapa satur visu detalizēto informāciju par transakcijām saistībā ar noguldījumiem bankā.
       - **Norēķinu transakcijas noguldījumiem seifā**: šī darblapa satur visu detalizēto informāciju par transakcijām saistībā ar noguldījumiem seifā.
       - **Norēķinu uzskaite**: šī darblapa satur visu detalizēto informāciju par norēķinu uzskaites transakcijām.
       - **Ienākumu–izdevumu transakcija**: šī darblapa satur visu detalizēto informāciju par ieņēmumu–izdevumu transakciju rindām.
       - **Maksājumu transakcijas**: šī darblapa satur visu ar maksājumiem saistīto informāciju operācijai **Apmaksāt rēķinu**, kā arī ieņēmumu–izdevumu transakciju.

3.  Publicējot lielapjoma rediģētās transakcijas, validācija netiek veikta. Jums jāpārliecinās, vai visi labojumi ir precīzi un vai visās darblapās tiek uzturēta datu precizitāte. Piemēram, ja vēlaties mainīt transakcijas datumu, lai pārvaldītu scenārijus, kuros finanšu vai krājumu periods atvērtajām transakcijām ir slēgts, ir jāmaina datums visās Excel darblapās, kurās ir kolonna **Darbadiena**. Lai validētu transakcijas pēc to rediģēšanas, varat izmantot opciju **Validēt transakcijas atkārtoti** lapā **Pārskati**.
