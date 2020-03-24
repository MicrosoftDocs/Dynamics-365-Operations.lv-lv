---
title: Iestatīt maksājumu biežumu
description: Microsoft Dynamics 365 Human Resources izmanto maksājuma biežumu, lai aprēķinātu gada atvieglojumu algu, noteiktu atvieglojumu piemaksas summu, ko nodarbinātais maksā katram apmaksas periodam, un nosaka biežuma maksājumus, kas tiek veikti pakalpojumu sniedzējiem.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b786485ab53dcdb3b7e5ff02562f674a7f8e6eae
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092595"
---
# <a name="set-up-payment-frequencies"></a>Iestatīt maksājumu biežumu

[!include [banner](includes/preview-feature.md)]

Microsoft Dynamics 365 Human Resources izmanto maksājuma biežumu, lai aprēķinātu gada atvieglojumu algu, noteiktu atvieglojumu piemaksas summu, ko nodarbinātais maksā katram apmaksas periodam, un nosaka biežuma maksājumus, kas tiek veikti pakalpojumu sniedzējiem.

Atvieglojumu maksājumu biežums izmanto pārveidošanas koeficientus, lai konvertētu atvieglojumu maksājumu periodus no mēneša, daļēji mēneša, divreiz nedēļā, nedēļas un ikdienas maksājuma biežumiem. Tas ļauj uzņēmumiem noteikt izmaksu biežuma savstarpējo atkarību atvieglojumu plāna ietvaros.

Pārveidošanas koeficienta lauki identificē pārveidošanas koeficientu no maksājuma biežuma uz standarta maksājumu periodiem un ļauj sistēmai veikt aprēķinus starp maksājumu biežumiem. Konvertēšanas koeficienta summa tiek izmantota arī, lai noteiktu atvieglojumu prēmijas summu, kas darbiniekam jāapmaksā katru apmaksas biežumu.

1. Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Maksājuma biežums**.

2. Atlasiet **Jauns**.

3. Norādiet vērtības tālāk minētajos laukos.

   | Lauks | Apraksts |
   | --- | --- |
   | Maksājumu biežums | Unikāls maksājuma biežuma nosaukums. |
   | Apraksts | Maksājuma biežuma apraksts. |
   | Periods | Atbilstošais periods, kas vislabāk atbilst atvieglojumu nodrošinātāja un nodarbinātā maksājuma biežumam. Periodu saraksts sastāv no standarta maksājumu periodiem. |
   | Apmaksas periodu skaits | Apmaksas periodu skaits, kas parāda, cik bieži atvieglojumu nodrošinātājs vai nodarbinātie tiek apmaksāti. Šī summa tiks izmantota, lai aprēķinātu nodarbinātā gada atvieglojumu algas summu. |
   | Gada pārrēķināšanas koeficients | Gada pārvēršanas koeficients maksājuma biežumam. Piemēram, gada konvertēšanas koeficients ikmēneša izmaksas biežumam ir: </br></br>(12 mēneša maksājumi / 1 gadā) = 12 |
   | Pusgada pārveidošanas koeficients | Pusgada konvertēšanas koeficients maksājuma biežumam. Piemēram, pusgada konvertēšanas koeficients ikmēneša izmaksas biežumam ir: </br></br>(12 mēneša maksājumi / 2 reizes gadā) = 6 |
   | Ceturkšņa pārveidošanas koeficients | Ceturkšņa konvertēšanas koeficients maksājuma biežumam. Piemēram, ceturkšņa konvertēšanas koeficients ikmēneša izmaksas biežumam ir: </br></br>(12 ikmēneša maksājumi/4 ceturkšņi) = 3 |
   | Ikmēneša pārveidošanas koeficients | Ikmēneša pārvēršanas koeficients maksājuma biežumam. Piemēram, ikmēneša konvertēšanas koeficients ikmēneša izmaksas biežumam ir: </br></br>(12 mēneša maksājumi / 12 mēnešos) = 1 |
   | Pusmēneša pārveidošanas koeficients | Pusmēneša pārvēršanas koeficients maksājuma biežumam. Piemēram, pusmēneša konvertēšanas koeficients ikmēneša izmaksas biežumam ir: </br></br>(12 ikmēneša maksājum i/ 24 (2x mēnesī)) =0,5 | 
   | Katras otrās nedēļas pārveidošanas koeficients | Gada pārvēršanas koeficients maksājuma biežumam. Piemēram, gada konvertēšanas koeficients ikmēneša izmaksas biežumam ir: </br></br>(12 mēneša maksājumi / 26 nedēļās) = 0.461538 |
   | Nedēļas pārveidošanas koeficients | Gada pārvēršanas koeficients maksājuma biežumam. Piemēram, gada konvertēšanas koeficients ikmēneša izmaksas biežumam ir: </br></br>(12 mēneša maksājumi / 52 nedēļās) = 0.230769 |
   | Dienas pārveidošanas koeficients | Gada pārvēršanas koeficients maksājuma biežumam. Piemēram, gada konvertēšanas koeficients ikmēneša izmaksas biežumam ir: </br></br>(12 mēneša maksājumi / 365 dienās) = 0.032877 |

4. Atlasiet **Saglabāt**. 
