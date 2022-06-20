---
title: Abonementu norēķinu Power BI saturs
description: Šajā rakstā ir aprakstīts, kas ir iekļauts abonementa norēķinu saturā Microsoft Power BI.
author: JodiChristiansen
ms.date: 04/13/2022
ms.topic: article
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-04-13
ms.openlocfilehash: 6cee01eb5b8bb8296b6e7f638b565c999ccc023e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849965"
---
# <a name="subscription-billing-power-bi-content"></a>Abonementu norēķinu Power BI saturs

[!include[banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kas ir iekļauts abonementa norēķinu saturā Microsoft Power BI. Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī ir sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem. 

## <a name="overview"></a>Pārskats

Abonementa norēķinu Power BI saturs tika izveidots abonementa norēķinu darbinieki un vadītāji. Tā sniedz atslēgas abonementa norēķinu rādītājus, piemēram, ikmēneša periodiskos ieņēmumus (MRR) norēķinu grafikiem, un degresīvās bilances un papildu informāciju atlikto maksājumu grafikiem. Tas izmanto datus no rēķinu grafikiem un atlikto maksājumu grafikiem, lai nodrošinātu periodisku ienākumu un ieņēmumu apskatu.

Saturam Power BI ir šādas trīs cilnes, kas nodrošina četru analītisko pārskatu kopsummu: 

- **Analītika - MRR** – šī cilne sniedz mēneša **periodisko norēķinu** pārskatu un norēķinu **grafika detalizētas informācijas** pārskatu.
- **Analīze - Konta** – šī cilne nodrošina ieņēmumu **pārskatu**.
- **Analīze - degresīvā bilance** - šī cilne sniedz degresīvās **līdzsvarošanas** pārskatu.

## <a name="view-data-on-the-analytical-reports"></a>Skatīt datus par analītiskajiem pārskatiem

Pirms varat skatīt datus par analītiskajiem pārskatiem, jāpalaiž periodisks process, kas ģenerē pārskata datus katram pārskatam. Šie dati, kurus pieprasa pārskati, ir jāģenerē, jo tie netiek saglabāti tieši datu bāzē. 

1. Pārejiet uz Sadaļu **Abonementa \> norēķini Periodiskie līguma norēķini \> Periodiskie uzdevumi \> MRR analītiskā** pārskata pakešapstrāde un sekojiet šiem soļiem:

    1. Ievadiet datumu diapazonu, kas nav lielāks par trim gadiem.
    2. Nav obligāti: iestatiet periodisku pakešveida apstrādes darbu, lai periodiski atsvaidzinātu datus.
    3. Atlasiet **Labi**.

2. Kad pakešuzdevums ir pabeigts, **dodieties uz sistēmas administrēšanas iestatījumu \> elementa \> veikalu** un atsvaidziniet **MRR pārskata apkopošanas** mērījumu. 
3. Pārejiet uz Abonementa **rēķinu \> ieņēmumu un izdevumu atlikto maksājumu periodiskajiem \> uzdevumiem \> Analītiskā pārskata pakešapstrāde** un sekojiet šiem soļiem:

    1. Ievadiet sākuma un beigu datumu, kas ietver ne vairāk kā 26 periodus. 
    2. Ja vēlaties skatīt iepriekšējo periodu budžeta summu pašreizējā periodā, **iestatiet opciju Budžeta iepriekšējās summas pašreizējā** periodā uz **Jā**.
    3. Nav obligāti: iestatiet periodisku pakešveida apstrādes darbu, lai periodiski atsvaidzinātu datus.
    4. Atlasiet **Labi**. 

4. Kad pakešuzdevums ir beidzis darbību, dodieties uz sistēmas **\> administrēšanas iestatīšanas elementa \> veikalu** un atsvaidziniet **Rezultātu pārskata apkopošanas** mērījumu.
5. Pārejiet uz abonementa **rēķinu \> ieņēmumu un izdevumu atlikto maksājumu periodiskajiem uzdevumiem \> Samazināt \> bilances** analītisko pārskatu pakešveida apstrādi un sekojiet šiem soļiem:

    1. Ievadiet sākuma un beigu datumu, kas ietver ne vairāk kā 26 periodus. 
    2. Ja vēlaties skatīt iepriekšējo periodu budžeta summu pašreizējā periodā, **iestatiet opciju Budžeta iepriekšējās summas pašreizējā** periodā uz **Jā**.
    3. Nav obligāti: iestatiet periodisku pakešveida apstrādes darbu, lai periodiski atsvaidzinātu datus.
    4. Atlasiet **Labi**.

6. Kad pakešuzdevums ir pabeigts, **\>\>** dodieties uz sistēmas administrēšanas iestatīšanas elementa veikalu un atsvaidziniet racionalizēšanas **bilances pārskata apkopošanas** mērījumu.

## <a name="accessing-the-power-bi-content"></a>Piekļuve Power BI satura pakotnei

Abonementa norēķinu saturs Power BI ir parādīts abonementa norēķinu **darbvietā**.
