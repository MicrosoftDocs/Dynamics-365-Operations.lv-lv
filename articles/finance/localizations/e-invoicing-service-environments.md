---
title: Pakalpojumu vides
description: Šajā rakstā ir sniegta informācija par pakalpojumu vidi elektronisko rēķinu izrakstīšanai un skaidrots, kā tās iestatīt.
author: gionoder
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: ff6f50ff78676f5efed7d905fb622ad662b541d7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291605"
---
# <a name="service-environments"></a>Pakalpojumu vides

[!include [banner](../includes/banner.md)]

Pakalpojumu vides ir loģiskie nodalījumi, kas izveidoti, lai atbalstītu globalizācijas līdzekļus un atbilstošos dokumentus, kas tiek apstrādāti Elektronisko rēķinu izrakstīšanas pakalpojumā. Pakalpojuma vides līmenī ir jākonfigurē drošības noslēpumi un ciparsertifikātus un piekļuves atļaujas (valdības).

Ir iespējams izveidot tik daudz pakalpojumu vides, cik nepieciešams. Visas jūsu veidotās pakalpojumu vides nav atkarīgas viena no otras. Saskaņā ar labāko praksi ieteicams izveidot vismaz divas pakalpojumu vides:

- Viena vide galvenajiem izstrādes un apstiprināšanas nolūkiem. Šī vide parasti ir lietotāju pieņemšanas testēšanas (UAT) vide.
- Viena vide ražošanas nolūkiem. Šī vide parasti ir ražošanas vide.

Šis nodalīšanas veids palīdz nodrošināt, ka e-rēķinu izrakstīšanas procesi tiek validēti un pielāgoti kastēs, pirms tie pāriet uz ražošanu.

Pakalpojuma vides ir jāizveido un jāuztur regulēšanas konfigurācijas pakalpojumā (RCS). Pēc tam, kad tās ir gatavas, tās ir jāpublicē Elektronisko rēķinu izrakstīšanas pakalpojumā. Publicēšanas process sūta pakalpojuma vides parametrus no RCS instances uz elektronisko rēķinu izrakstīšanas pakalpojumu.

Ja publicēšanas process netiek pabeigts pēc jaunas pakalpojumu vides izveides vai esošas pakalpojumu vides pielāgošanas (piemēram, Microsoft Azure pievienojot vai noņemot lietotājus vai Atslēgas Lietotāja noslēpumus), izmaiņas nebūs spēkā. Dynamics 365 Finanses vai var piekļūt tikai publicētām vidēm Dynamics 365 Supply Chain Management.

## <a name="service-environment-statuses"></a>Pakalpojumu vides statusi

Pakalpojumu vides var pārvaldīt ar to statusu. Vides statusu varat skatīt lapā **Pakalpojumu** vides. Ir pieejami šādi statusi:

- **Nav publicēts** – vide ir izveidota, bet vēl nav publicēta.
- **Publicēts** – vide ir publicēta Elektronisko rēķinu izrakstīšanas pakalpojumā.
- **Mainīts** – publicētās vides atribūti ir izmainīti, bet izmaiņas vēl nav publicētas.

## <a name="users"></a>Lietotāji

Katrai pakalpojumu videi jāsarakstam tās personas, kas var pievienoties Elektronisko rēķinu izrakstīšanai no Finanšu vai Piegādes ķēžu pārvaldības.

## <a name="applications"></a>Programmas

Dažos scenārijos programmām, kas nav Finanses vai Piegādes ķēžu pārvaldība, var būt nepieciešams izveidot savienojumu ar Elektronisko rēķinu izrakstīšanas pakalpojumu, lai iesniegtu elektroniskos dokumentus turpmākai apstrādei vai lai izgūtu tādu informāciju kā dokumenta iesniegšanas statuss. Šajos scenārijos pieteikums jādefinē lietojumprogrammu sarakstā. Šādā veidā tai būs piekļuve Elektronisko rēķinu izrakstīšanas pakalpojumam. Programmai jābūt reģistrētai arī kā programma (Azure Active Directory) un Azure AD objekta ID ir jāizmanto, lai to identificētu. 

Tā kā korporācijai Microsoft ir nepieciešama augsta līmeņa drošības kontrole pār programmām, kas var izveidot savienojumu ar elektronisko rēķinu izrakstīšanas pakalpojumu, jums ir jāsazinās ar Microsoft <DGXRegulatoryservicesengineering@service.microsoft.com> un jānorāda sava lietojumprogrammas informācija:

- Azure AD nomnieka ID
- Microsoft Dynamics Dzīves cikla pakalpojumu (LCS) vides ID
- Programmas ID (klienta ID)
- Objekta ID
- Pieteikuma līdzināšanas un augsta līmeņa apraksts

Korporācija Microsoft novērtēs pieprasījumu un reģistrēs šo programmu drošības reģistrā, lai nodrošinātu, ka tā var strādāt ar elektronisko rēķinu izrakstīšanu.

## <a name="number-sequences"></a>Numuru sērijas

Ja scenārijiem nepieciešamas numuru sērijas (piemēram, failu nosaukumos), ir iespējams izmantot numuru sērijas, kas ir noteiktas vides vajadzībām, bet tās var izmantot vai nu globalizācijas funkcijām, vai arī noteiktai globalizācijas funkcijai. Pēc numuru sērijas definēšanas to var izmantot mainīgajos un konveijeru apstrādē. Lai izsekotu tā izmantošanu, **lapā Numuru sērijas** meklējiet vērtību **Pašreizējais**, lai iegūtu parametru **Lietošanā**.

### <a name="working-with-number-sequences"></a>Darbs ar numuru sērijām
**Numuru sēriju** lapā: 

- Atlasiet **Jauns,** lai izveidotu numuru sēriju. Pēc tam ievadiet nosaukumu un aprakstu. 
- Atlasiet **Dzēst,** lai dzēstu numuru sēriju, ja tā vairs netiek lietota.
- Nav jāatlasa Publicēt darbību **rūtī**, lai publicētu izmaiņas numuru sērijā. Atjaunināšana tiek veikta automātiski.

## <a name="create-a-key-vault-reference"></a>Atslēgas Atsauču izveide

1. Piesakieties savā RCS kontā.
2. Darbvietā **Globalizācijas līdzeklis** sadaļā **Vide** atlasiet elementu **Elektronisko rēķinu izrakstīšana**.
3. **Lapas Vides iestatījums** darbību rūtī atlasiet Pakalpojuma **vides**.
4. **Lapas Pakalpojumu vides darbību** rūtī atlasiet Atslēgas Pasūtījuma **parametri**.
5. Lai izveidotu **atslēgu Atsauču** atsauci, **lapā** Atslēgas Lietotāja parametri atlasiet Jauns.
6. Laukā **Nosaukums** ievadiet atslēgas Atziņas atsauces nosaukumu.
7. Ievadiet aprakstu laukā **Apraksts**.
8. Laukā **Key Programma URI ielīmējiet atslēgas Atslēpeno URI no atslēgas URI** (`https://<your key vault>.vault.azure.net/`). Papildinformāciju skatiet Azure [portāla sadaļā Azure atslēgas izveide](e-invoicing-create-azure-key-vault-azure-portal.md).
9. Atlasiet **Saglabāt**.
    
## <a name="create-a-secret-for-the-storage-account-secret-token"></a>Izveidot noslēpumu glabāšanas konta noslēpuma glabāšanai

1. Lapā Atslēgas **Atsauču** **parametri izvēlieties Atslēgu Atsauču, ko izveidojāt iepriekšējā procedūrā,** un pēc tam sadaļā Sertifikāti atlasiet **Pievienot**.
2. Laukā **Nosaukums** ievadiet glabātuves konta noslēpuma nosaukumu. Šim nosaukumam ir jāatbilst atslēgas glabātāja noslēpuma nosaukumam, kurš glabā koplietojamā piekļuves paraksta (SAS) marķieri. Papildinformāciju skatiet [Azure glabāšanas konta izveidošana Azure portālā](e-invoicing-create-azure-storage-account-azure-portal.md). 
3. Ievadiet aprakstu laukā **Apraksts**.
4. Laukā **Tips** atlasiet **Noslēpums**.
5. Atlasiet **Saglabāt**.
    
## <a name="create-a-service-environment"></a>Pakalpojumu vides izveide

1. **Lapā Pakalpojumu vides atlasiet** Jauns **·**, lai izveidotu pakalpojumu vidi.
2. Laukā **Nosaukums** ievadiet elektronisko rēķinu izrakstīšanas vides nosaukumu.
3. Ievadiet aprakstu laukā **Apraksts**.
4. Laukā **Krātuves SAS marķiera noslēpums** atlasiet tā krātuves konta noslēpuma nosaukumu, kas jāizmanto, lai autentificētu piekļuvi krātuves kontam.
5. Sadaļā Lietotāji **atlasiet** Pievienot, lai **pievienotu** lietotāju, kuram ir atļauts iesniegt elektroniskos rēķinus, izmantojot vidi, un pievienojieties glabāšanas kontam.
6. Laukā **Lietotāja ID** ievadiet lietotāja aizstājvārdu. 
7. Laukā **E-pasta adrese** ievadiet lietotāja e-pasta adresi.
8. Atlasiet **Saglabāt**.
9. Darbību rūtī atlasiet Publicēt, lai **publicētu** vidi elektronisko rēķinu izrakstīšanas pakalpojumā. Pārbaudiet, vai lauka Statuss vērtība **ir** mainīta uz **Publicēts**.
