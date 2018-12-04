---
title: "Finanšu integrācija mazumtirdzniecības kanālam"
description: "Šajā tēmā ir sniegts apskats par finanšu integrāciju programmai Retail POS."
author: josaw
manager: annbe
ms.date: 11/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: c852d095505abecbd44d29e9e7b53875e9069def
ms.contentlocale: lv-lv
ms.lasthandoff: 11/01/2018

---
# <a name="fiscal-integration-for-retail-channel"></a>Finanšu integrācija mazumtirdzniecības kanālam

[!include [banner](../includes/banner.md)]

Šajā tēmā ir apskats par finanšu integrācijas funkcionalitāti, kas ir pieejama programmā Microsoft Dynamics 365 for Retail. Finanšu integrācijas funkcionalitāte ir struktūra, kas ir izstrādāta lokālo finanšu likumu atbalstīšanai ar mērķi novērst krāpšanu mazumtirdzniecības nozarē. Tālāk ir nepilnīgs saraksts ar tipiskajiem scenārijiem, uz kuriem attiektos finanšu integrācijas lietošana.

- Finanšu dokumentu drukāšana un izsniegšana debitoram.
- Informācijas iesniegšanas drošināšana saistībā ar POS veikto pārdošanu un atgriešanu uz ārēju pakalpojumu, ko nodrošina iestāde.
- Datu aizsardzības izmantošana ar elektronisko parakstu, ko ir autorizējusi iestāde.

Šajā tēmā ir sniegtas vadlīnijas par finanšu integrācijas iestatīšanu, lai lietotāji varētu veikt tālāk norādītos uzdevumus. 

- Konfigurēt finanšu savienotājus, kas ir finanšu ierīces vai pakalpojumi, kurus izmanto finanšu reģistrācijas nolūkiem, piemēram, finanšu datu saglabāšanai, digitālajiem parakstiem un drošinātai iesniegšanai.
- Konfigurēt dokumentu nodrošinātāju, kas nosaka finanšu dokumentu ģenerēšanas izvades metodi un algoritmu.
- Konfigurēt finanšu reģistrācijas procesu, kas nosaka darbību secību un katrā darbībā izmantoto savienotāju grupu.
- Piešķirt finanšu reģistrācijas procesus POS funkcionalitātes profiliem.
- Piešķirt savienotāju tehniskos profilus aparatūras profiliem (lokālajiem finanšu savienotājiem) vai POS funkcionalitātes profiliem (citiem finanšu savienotāju tipiem).

## <a name="fiscal-integration-execution-flow"></a>Finanšu integrācijas izpildes plūsma
Nākamajā scenārijā ir parādīta parastā finanšu integrācijas izpildes plūsma.

1. Inicializējiet fiskālās reģistrācijas procesu.
  
   Kad ir izpildītas kādas darbības, kurām ir nepieciešama finanšu reģistrācija, piemēram, pēc mazumtirdzniecības transakcijas pabeigšanas, šis finanšu reģistrācijas process ir saistīts ar pašreizējo POS funkcionalitātes profilu.

1. Meklējiet finanšu savienotāju.
   
   Katrai finanšu reģistrācijas procesā ietvertajai finanšu reģistrācijas darbībai sistēma nosaka atbilstību ar finanšu savienotāju sarakstu. Šiem savienotājiem ir funkcionālais profils, kas ir ietverts norādītajā savienotāju grupā, un saraksts ar savienotājiem, kuru tehniskais profils ir saistīts ar pašreizējo aparatūras profilu (tikai savienotāju tipam, kas ir vienāds ar **Lokāls**) vai ar pašreizējo POS funkcionalitātes profilu (citiem savienotāju tipiem).
   
1. Veiciet finanšu integrāciju.

   Sistēma izpilda visas nepieciešamās darbības, kuras nosaka ar atrasto savienotāju saistītā komplektācija. Tas tiek darīts saskaņā ar šim savienotājam iepriekšējā darbībā atrastā funkcionālā profila un tehniskā profila iestatījumiem.

## <a name="setup-needed-before-using-fiscal-integration"></a>Pirms finanšu integrācijas lietošanas nepieciešamā iestatīšana
Pirms sākat lietot finanšu integrācijas funkcionalitāti, vajadzētu definēt tālāk norādītos iestatījumus.

- Lapā **Mazumtirdzniecības parametri** definējiet numuru sēriju finanšu funkcionālā profila numuram.
  
- Lapā **Mazumtirdzniecības koplietojamie parametri** definējiet numuru sērijas tālāk norādītajām atsaucēm.
  
  - Finanšu tehniskā profila numurs
  - Finanšu savienotāja grupas numurs
  - Reģistrācijas procesa numurs

- Sadaļā **Retail > Kanāla iestatīšana > Finanšu integrācija > Finanšu savienotāji** izveidojiet vienumu **Finanšu savienotājs** katrai ierīcei vai pakalpojumam, ko plānojat izmantot finanšu integrācijas nolūkos.

-  Sadaļā **Retail > Kanāla iestatīšana > Finanšu integrācija > Finanšu dokumentu nodrošinātāji** izveidojiet vienumu **Finanšu dokumentu nodrošinātājs** visiem finanšu savienotājiem. Datu kartēšana tiek uzskatīta par daļu no finanšu dokumentu nodrošinātāja. Lai iestatītu citus datu kartējumus tam pašam savienotājam (piemēram, ja pastāv valstij raksturīgi noteikumi), jums vajadzētu izveidot dažādus finanšu dokumentu nodrošinātājus.

- Sadaļā **Retail > Kanāla iestatīšana > Finanšu integrācija > Savienotāja funkcionālie profili** izveidojiet vienumu **Savienotāja funkcionālais profils** katram finanšu dokumentu nodrošinātājam.
  - Atlasiet savienotāja nosaukumu.
  - Atlasiet kādu dokumentu nodrošinātāju.
  - Cilnē **Pakalpojuma iestatīšana** norādiet PVN likmju iestatījumus.
  - Cilnē **Datu kartēšana** norādiet PVN kodu kartējumu un norēķinu tipu kartējumu.

  #### <a name="examples"></a>Piemēri 

  |  | Formāts | Piemērs | 
  |--------|--------|--------|
  | PVN likmju iestatījumi | value : VATrate | 1 : 2000, 2 : 1800 |
  | PVN kodu kartējums | VATcode : value | vat20 : 1, vat18 : 2 |
  | Norēķinu tipu kartējums | TenderTyp : value | Cash : 1, Card : 2 |

- Izveidojiet vienumu **Finanšu savienotāju grupas** sadaļā **Retail > Kanāla iestatīšana > Finanšu integrācija > Finanšu savienotāju grupa**. Savienotāju grupa ir apakškopa no funkcionālajiem profiliem, kas ir saistīti ar finanšu savienotājiem, kuri veic identiskas funkcijas un finanšu reģistrācijas procesā tiek izmantoti tajā pašā posmā.

   - Pievienojiet funkcionālos profilus savienotāju grupai. Lapā **Funkcionālie profili** noklikšķiniet uz **Pievienot** un atlasiet kādu profila numuru.
   - Ja vēlaties pārtraukt šī funkcionālā profila izmantošanu, vienumu **Atspējot** iestatiet uz **Jā**. 
   
     Šīs izmaiņas ietekmē tikai pašreizējo savienotāju grupu. Varat turpināt tā paša funkcionālā profila lietošanu citās savienotāju grupās.

     >[!NOTE]
     > Vienā savienotāju grupā katram finanšu savienotājam var būt tikai viens funkcionālais profils.

- Sadaļā **Retail > Kanāla iestatīšana > Finanšu integrācija > Savienotāja tehniskie profili** izveidojiet vienumu **Savienotāja tehniskais profils** katram finanšu savienotājam.
  - Atlasiet savienotāja nosaukumu.
  - Atlasiet savienotāja tipu. 
      - **Lokāls** — iestatiet šo tipu fiziskām ierīcēm vai programmām, kas ir instalētas lokāla mašīnā.
      - **Iekšējs** — iestatiet šo tipu finanšu ierīcēm un pakalpojumiem, kas ir saistīti ar Retail Server.
      - **Ārējs** — ārējiem finanšu pakalpojumiem, piemēram, tīmekļa portālam, ko nodrošina nodokļu iestāde.
    
  - Norādiet iestatījumus cilnē **Savienojums**.

      
 >[!NOTE]
 > Iepriekš ielādētās konfigurācijas atjaunināta versija tiek ielādēta gan funkcionālajam, gan tehniskajam profilam. Ja atbilstošs savienotājs vai dokumentu nodrošinātājs jau tiek lietots, jums par to tiek paziņots. Pēc noklusējuma tiek saglabātas visas izmaiņas, kas funkcionālajā un tehniskajā profilā ir veiktas manuāli. Lai šos profilus pārrakstītu ar noklusējuma parametru kopu no kādas konfigurācijas, noklikšķiniet uz **Atjaunināt** lapā **Savienotāja funkcionālie profili** un lapā **Savienotāja tehniskie profili**.
 
- Sadaļā **Retail > Kanāla iestatīšana > Finanšu integrācija > Finanšu reģistrācijas process** izveidojiet vienumu **Finanšu reģistrācijas process** katram unikālajam finanšu integrācijas procesam. Reģistrācijas procesu nosaka reģistrācijas darbību secība un katrā darbībā izmantotā savienotāju grupa. 
  
  - Pievienojiet procesam reģistrācijas darbības.
      - Noklikšķiniet uz **Pievienot**.
      - Atlasiet kādu savienotāja tipu.
      
      >[!NOTE]
      > Šis lauks nosaka, vai sistēma tehniskajā profilā meklē savienotāju, aparatūras profilos meklē savienotāja tipu **Lokāls** vai POS funkcionalitātes profilos meklē citus savienotāju tipus.
      
   - Atlasiet savienotāju grupu.
   
     >[!NOTE]
     > Noklikšķiniet uz **Validēt**, lai pārbaudītu reģistrācijas procesa struktūras integritāti. Validācijas ir ieteicams veikt tālāk aprakstītajos gadījumos.
       >- Jaunam reģistrācijas procesam, kad ir pabeigti visi iestatījumi, tostarp saistīšana ar POS funkcionalitātes profiliem un aparatūras profiliem.
       >- Pēc atjauninājumu veikšanas esošam reģistrācijas procesam.

-  Saistiet finanšu reģistrācijas procesus ar POS funkcionalitātes profiliem sadaļā **Retail > Kanāla iestatīšana > POS iestatīšana > POS profili > Funkcionalitātes profili**.
   - Noklikšķiniet uz **Rediģēt** un atlasiet vienumu **Procesa numurs** cilnē **Finanšu reģistrācijas process**.
- Savienotāju tehniskos profilus saistiet ar aparatūras profiliem sadaļā **Retail > Kanāla iestatīšana > POS iestatīšana > POS profili > Aparatūras profili**.
   - Noklikšķiniet uz **Rediģēt** un pēc tam noklikšķiniet uz **Jauns** cilnē **Finanšu tehniskais profils**.
   - Atlasiet kādu savienotāja tehnisko profilu laukā **Profila numurs**.
   
     >[!NOTE]
     > Vienam aparatūras profilam varat pievienot vairākus tehnisko profilus. Taču tas netiek atbalstīts, ja aparatūras profilam ir vairākas krustošanās ar jebkuru savienotāju grupu. Lai nepieļautu nepareizus iestatījumus, pēc visu aparatūras profilu atjaunināšanas ir ieteicams validēt reģistrācijas procesu.

