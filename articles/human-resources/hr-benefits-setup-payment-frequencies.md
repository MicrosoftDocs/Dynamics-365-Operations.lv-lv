---
title: Iestatīt maksājumu biežumu
description: Microsoft Dynamics 365 Human Resources izmanto maksājuma biežumu, lai aprēķinātu gada atvieglojumu algu, noteiktu atvieglojumu piemaksas summu, ko nodarbinātais maksā katram apmaksas periodam, un cik bieži pakalpojumu sniedzējiem tiek samaksāts.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 738df6a31ec8e9f50259461cd7bbf30bd5c2b73c6f8a23ffacba53ab261a80ed
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732756"
---
# <a name="set-up-payment-frequencies"></a>Iestatīt maksājumu biežumu

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources izmanto maksājuma biežumu, lai aprēķinātu gada atvieglojumu algu, noteiktu atvieglojumu piemaksas summu, ko nodarbinātais maksā katram apmaksas periodam, un cik bieži pakalpojumu sniedzējiem tiek samaksāts.

Atvieglojumu maksājumu biežums izmanto pārveidošanas koeficientus, lai konvertētu atvieglojumu maksājumu periodus no mēneša, daļēji mēneša, divreiz nedēļā, nedēļas un ikdienas maksājuma biežumiem. Tas ļauj uzņēmumiem noteikt izmaksu biežuma savstarpējo atkarību atvieglojumu plāna ietvaros.

Pārveidošanas koeficienta lauki identificē pārveidošanas koeficientu no maksājuma biežuma uz standarta maksājumu periodiem un ļauj sistēmai veikt aprēķinus starp maksājumu biežumiem. Konvertēšanas koeficienta summa arī nosaka atvieglojumu prēmijas summu, kas darbiniekam jāapmaksā katru apmaksas biežumu.

1. Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Maksājuma biežums**.

2. Atlasiet **Jauns**.

3. Norādiet vērtības tālāk minētajos laukos.

   | Lauks | Apraksts |
   | --- | --- |
   | **Maksājumu biežums** | Unikāls maksājuma biežuma nosaukums. |
   | **Apraksts** | Maksājuma biežuma apraksts. |
   | **Periods** | Atbilstošais periods, kas vislabāk atbilst atvieglojumu nodrošinātāja un nodarbinātā maksājuma biežumam. Periodu saraksts sastāv no standarta maksājumu periodiem. |
   | **Apmaksas periodu skaits** | Apmaksas periodu skaits, kas parāda, cik bieži atvieglojumu nodrošinātājs vai nodarbinātie tiek apmaksāti. Šī summa tiks izmantota, lai aprēķinātu nodarbinātā gada atvieglojumu algas summu. |
   | **Gada pārrēķināšanas koeficients** | Gada pārvēršanas koeficients maksājuma biežumam. Piemēram, gada konvertēšanas koeficients ikmēneša izmaksas biežumam ir: </br></br>(12 mēneša maksājumi / 1 gadā) = 12 |
   | **Pusgada pārveidošanas koeficients** | Pusgada konvertēšanas koeficients maksājuma biežumam. Piemēram, pusgada konvertēšanas koeficients ikmēneša izmaksas biežumam ir: </br></br>(12 mēneša maksājumi / 2 reizes gadā) = 6 |
   | **Ceturkšņa pārveidošanas koeficients** | Ceturkšņa konvertēšanas koeficients maksājuma biežumam. Piemēram, ceturkšņa konvertēšanas koeficients ikmēneša izmaksas biežumam ir: </br></br>(12 ikmēneša maksājumi/4 ceturkšņi) = 3 |
   | **Ikmēneša pārveidošanas koeficients** | Ikmēneša pārvēršanas koeficients maksājuma biežumam. Piemēram, ikmēneša konvertēšanas koeficients ikmēneša izmaksas biežumam ir: </br></br>(12 mēneša maksājumi / 12 mēnešos) = 1 |
   | **Pusmēneša pārveidošanas koeficients** | Pusmēneša pārvēršanas koeficients maksājuma biežumam. Piemēram, pusmēneša konvertēšanas koeficients ikmēneša izmaksas biežumam ir: </br></br>(12 ikmēneša maksājumi/ 24 (2x mēnesī)) = 0.5 | 
   | **Katras otrās nedēļas pārveidošanas koeficients** | Gada pārvēršanas koeficients maksājuma biežumam. Piemēram, gada konvertēšanas koeficients ikmēneša izmaksas biežumam ir: </br></br>(12 mēneša maksājumi / 26 nedēļās) = 0.461538 |
   | **Nedēļas pārveidošanas koeficients** | Gada pārvēršanas koeficients maksājuma biežumam. Piemēram, gada konvertēšanas koeficients ikmēneša izmaksas biežumam ir: </br></br>(12 mēneša maksājumi / 52 nedēļās) = 0.230769 |
   | **Dienas pārveidošanas koeficients** | Gada pārvēršanas koeficients maksājuma biežumam. Piemēram, gada konvertēšanas koeficients ikmēneša izmaksas biežumam ir: </br></br>(12 mēneša maksājumi / 365 dienās) = 0.032877 |
   | **Stundas pārveidošanas koeficients** | Gada pārvēršanas koeficients maksājuma biežumam. Piemēram, gada konvertēšanas koeficients ikmēneša izmaksas biežumam ir: </br></br>(12 mēneša maksājumi / 2080 stundas) = 0.005769

4. Atlasiet **Saglabāt**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]