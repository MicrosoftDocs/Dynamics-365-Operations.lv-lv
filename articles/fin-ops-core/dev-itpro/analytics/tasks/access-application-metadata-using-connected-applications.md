---
title: Piekļuve programmas metadatiem, izmantojot saistītās programmas
description: Šajā tēmā ietvertajās darbībās ir paskaidrots, kā Regulatory Configuration Service (RCS) lietotājs var noformēt jauna elektronisko pārskatu (Electronic Reporting — ER) modeļa kartēšanu, izmantojot Finance and Operations metadatus.
author: NickSelin
manager: AnnBe
ms.date: 06/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a476163ba6f66ab60ed8bfea6198d02f13ac5136
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182719"
---
# <a name="access-application-metadata-by-using-connected-applications"></a>Piekļuve programmas metadatiem, izmantojot saistītās programmas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Nākamajās darbībās ir paskaidrots, kā Regulatory Configuration Service (RCS) lietotājs ar lomu “Sistēmas administrators” vai “Elektronisko pārskatu izstrādātājs” var noformēt jauna elektronisko pārskatu (Electronic reporting — ER) modeļa kartēšanu, izmantojot metadatus programmā Finance and Operations. Programmas metadatiem jāpiekļūst tiešsaistē, izmantojot ar RCS saistīto programmu. Parauga ER modeļa kartēšana jākonfigurē piekļuvei ārējās tirdzniecības transakcijām. Lai izpildītu šīs darbības, vispirms pakalpojumā RCS izpildiet darbības, kas ir aprakstītas tēmā [Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu](er-configuration-provider-mark-it-active-2016-11.md). Ja neesat izpildījis tēmā [Piekļuve programmas metadatiem, izmantojot ER konfigurāciju](access-application-metadata-er-configuration.md) norādītās darbības, dodieties uz [Elektronisko pārskatu piemēru lapu](https://go.microsoft.com/fwlink/?linkid=862266), lai lejupielādētu un saglabātu šādas ER konfigurācijas: Ārējās tirdzniecības metadati.xml; Ārējās tirdzniecības modelis.xml; Ārējās tirdzniecības kartēšana.xml. Pēc tam izpildiet procedūras darbības.

## <a name="prerequisites"></a>Priekšnosacījumi
1. Dodieties uz **Visas darbvietas** > **Elektroniskie pārskati**. 
2. Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam Litware, Inc. ir pieejams un ir atzīmēts kā **Aktīvs**. Ja neredzat šo konfigurācijas nodrošinātāju, jums vispirms ir jāizpilda darbības, kas ir aprakstītas procedūrā [Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu](er-configuration-provider-mark-it-active-2016-11.md). 

## <a name="get-required-er-configurations"></a>Nepieciešamo ER konfigurāciju iegūšana
1. Noklikšķiniet uz **Pārskatu veidošanas konfigurācijas**. 
2. Ja esat jau izpildījis darbības, kas ir aprakstītas procedūrā [(RCS) Piekļuve programmas metadatiem, izmantojot ER konfigurāciju](access-application-metadata-er-configuration.md), jums jau ir visas nepieciešamās ER konfigurācijas (ārējās tirdzniecības metadatu, modeļa un kartēšanas konfigurācijas) pašreizējā RCS instancē. Visas atlikušās šī apakšuzdevuma darbības varat izlaist. 
3. Noklikšķiniet uz **Maiņa**. 
4. Noklikšķiniet uz **Ielādēt no XML faila**. 
5. Noklikšķiniet uz **Pārlūkot** un atlasiet failu **Ārējās tirdzniecības metadati.xml**. 
6. Noklikšķiniet uz **Labi**. 
7. Noklikšķiniet uz **Maiņa**. 
8. Noklikšķiniet uz **Ielādēt no XML faila**. 
9. Noklikšķiniet uz **Pārlūkot** un atlasiet failu **Ārējās tirdzniecības modelis.xml**. 
10. Noklikšķiniet uz **Labi**. 
11. Noklikšķiniet uz **Maiņa**. 
12. Noklikšķiniet uz **Ielādēt no XML faila**. 
13. Noklikšķiniet uz **Pārlūkot** un atlasiet failu **Ārējās tirdzniecības kartēšana.xml**. 
14. Noklikšķiniet uz **Labi**. 

## <a name="register-a-connected-application"></a>Savienotas programmas reģistrēšana
1. Aizvērt lapu. 
2. Aizvērt lapu. 
3. Dodieties uz **Visas darbvietas** > **Elektroniskie pārskati**. 
4. Noklikšķiniet uz **Savienotās programmas**. 
5. Pārliecinieties, vai konfigurētā programma ir Azure programma un ir pieejama pašreizējam RCS lietotājam. Turklāt pašreizējam RCS lietotājam ir arī jābūt piekļuvei atlasītajai programmai un ir jābūt reģistrētam kā šīs programmas lietotājam ar lomu, kas dod viņam privilēģijas piekļūt programmas metadatiem. 
6. Klikšķiniet **Jauns**. 
7. Laukā **Nosaukums** ierakstiet “MyConnectedApp”. 
8. Laukā **Programma** ievadiet “https:// mycompany.operations.dynamics.com”. 
9. Laukā **Nomnieks** ievadiet “mycompany.onmicrosoft.com”. 
10. Noklikšķiniet uz **Saglabāt**. 
11. Kad tiek pārbaudīts savienojums ar konfigurēto programmu, lapā **Savienojuma izveide ar attālo programmu** noklikšķiniet uz saites **Noklikšķināt šeit, lai izveidotu savienojumu ar atlasīto attālo programmu**. 
12. Noklikšķiniet uz **Pārbaudīt savienojumu**. 
13. Noklikšķiniet uz **Aizvērt**. 
14. Ja savienojuma validācija ir izdevusies, pašreizējā režģī konfigurētajai programmai tiks atjaunināta versija un nomnieka informācija. 

## <a name="review-existing-model-mapping-configuration"></a>Esošas ER modeļa kartēšanas konfigurācijas pārskatīšana
1. Aizvērt lapu. 
2. Noklikšķiniet uz **Pārskatu veidošanas konfigurācijas**. 
3. Kokā izvērsiet sadaļu **Ārējās tirdzniecības modelis**. 
4. Kokā atlasiet **Ārējās tirdzniecības modelis\Ārējās tirdzniecības kartēšana**. 
5. Izvērsiet sadaļu **Priekšnosacījumi**. 

> [!NOTE]
> Pašlaik šī kartēšana attiecas uz metadatu konfigurāciju. Izstrādājot šī modeļa kartēšanu, tiks piedāvāti šīs konfigurācijas programmas metadati. 

6. Noklikšķiniet uz **Veidotājs**. 
7. Noklikšķiniet uz **Veidotājs**. 
8. Kokā atlasiet **Dynamics 365 for Operations\Tabulas ieraksti**. 
9. Noklikšķiniet uz **Pievienot sakni**. 
10. Laukā **Tabula** ievadiet vai atlasiet kādu vērtību. 

> [!NOTE]
> Pašlaik šī kartēšana attiecas uz metadatu konfigurāciju. Izstrādājot šī modeļa kartēšanu, tiks piedāvāti šīs konfigurācijas programmas metadati. 

11. Noklikšķiniet uz **Atcelt**. 
12. Aizvērt lapu. 
13. Aizvērt lapu. 

## <a name="assign-connected-application-to-model-mapping"></a>Savienotās programmas piešķiršana modeļa kartēšanai 
1. Noklikšķiniet uz **Rediģēt**. 
2. Atlasiet programmu **MyConnectedApp**. 

> [!NOTE]
> Pašlaik šī kartēšana attiecas uz atlasītās savienotās programmas metadatiem. Ja tā pati kartēšana attiecas vienlaikus uz metadatu konfigurāciju un uz savienoto programmu, tiks izmantoti savienotās programmas metadati. 

3. Noklikšķiniet uz **Veidotājs**. 
4. Noklikšķiniet uz **Veidotājs**. 
5. Kokā atlasiet **Dynamics 365 for Operations\Tabulas ieraksti**. 
6. Noklikšķiniet uz **Pievienot sakni**. 
7. Laukā **Tabula** ievadiet vai atlasiet kādu vērtību. 

> [!NOTE]
> Tiek piedāvātas vairāk nekā divas programmas tabulas, jo šī kartēšana izmanto visus tai piešķirtās savienotās programmas metadatus. 

8. Noklikšķiniet uz **Atcelt**. 
9. Noklikšķiniet uz **Validēt**. 

> [!NOTE]
> Datu modeļa elementi ir veiksmīgi saistīti ar datu avotu vienībām, kas aprakstītas, lietojot detalizētu informāciju par kartēšanai piešķirtās savienotās programmas metadatiem. 

10. Aizvērt lapu. 
11. Aizvērt lapu. 

Ja ir jānovērtē šī modeļa kartēšana, izmantojot citas versijas programmas metadatus, reģistrējiet citu savienoto programmu, piešķiriet to šai modeļa kartēšanai un validējiet to ar jauniem metadatiem.
