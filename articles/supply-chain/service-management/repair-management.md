---
title: Labošanas pārvaldība
description: Sistemātiski sagrupējiet problēmas, lai palīdzētu ar ieteiktiem risinājumiem, kas bijuši veiksmīgi iepriekš.
author: sorenva
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAConditionTable, SMASymptomArea, SMADiagnosisArea, SMAResolutionTable, SMARepairStage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 32372a6a54e2adfbf511e2247be4a9baa28b4b53
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015206"
---
# <a name="repair-management"></a>Labošanas pārvaldība       

[!include [banner](../includes/banner.md)]


Labošanas pārvaldībai varat sistemātiski grupēt problēmas. Tas tiek darīts, lai palīdzētu ar ieteiktiem risinājumiem, kas bijuši veiksmīgi iepriekš.

Iestatiet simptomu, diagnozes un atrises iestatījumus. Tos visus vēlāk var pielietot gadījumā, ja labošanai saņemat līdzīgu krājumu. Varat arī iestatīt labošanas posmus, kuri ļauj sekot labošanas gaitai.

## <a name="setting-up-repair-management"></a>Labošanas pārvaldības iestatīšana

Izmantojiet šīs iestatīšanas veidlapas, lai ievadītu informāciju, kas tiks izmantota, lai norādītu labošanai simptomus, diagnozi un atrisinājumu.

- **Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Labošana** \> **Nosacījumi**.
- **Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Labošana** \> **Simptomu apgabali**.
-  **Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Labošana** \> **Diagnozes apgabali**.
- **Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Labošana** \> **Atrisinājumi**.
- **Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Labošana** \> **Labošanas posmi**.

## <a name="symptoms-and-conditions"></a>Simptomi un nosacījumi

Simptomi ir tas, kā klients raksturo problēmu. Simptomos iekļauti klienta novērojumi, kas norāda uz remonta nepieciešamību.

Varat iestatīt simptomu apgabalus, simptomu kodus un nosacījumus. Simptomu apgabals attiecas uz kļūmes jomu, un simptomu kods attiecas uz kļūmes simptomu. Nosacījumi apraksta situāciju vai vidi situāciju problēmas rašanās brīdī.

**Piemērs**

Remontam tiek nodots dators cietā diska kļūmes dēļ pēc ilgstoša lietošanas perioda. Cietā diska kļūmes rezultātā tiek parādīta zilā ekrāna kļūda. Tehniķis, kurš pieņem datoru, ievada šādus simptomus un nosacījumus:

1.  Simptomu apgabals ir cietais disks

2.  Simptomu kods ir zilā ekrāna kļūda

3.  Nosacījums ir tāds, ka rodas cietā diska kļūme pēc ilgstoša lietošanas perioda.

## <a name="diagnosis-and-resolutions"></a>Diagnoze un atrises

Diagnozes un atrises lauki ir pārskati no remonta perspektīvas. Šie ir soļi, ko tehniķis veic problēmas izpētes laikā.

Diagnozes apgabals sedz darbību, kas jāveic problēmas risināšanas laikā. Diagnozes kods ir veids, kā problēma tiek apstrādāta, atrise var būt tāda, ka vienība tiek salabota, nomainīta vai klients atceļ pasūtījumu. Piemēram, ja dators tiek salabots, diagnozes apgabals varētu būt “bojāta detaļa”, diagnozes kods varētu būt “uzstādīta jauna videokarte”, bet atrisinājums varētu būt “nomainīts”.

## <a name="repair-stages"></a>Remonta pakāpes

Remonta pakāpes nosaka remonta procesa stāvokli. Labošanas posmam ir beigu parametrs **Pabeigts**, kas norāda, ka labošanas rinda ir pabeigta un beigšanas datums un laiks ir ierakstīti.

## <a name="applying-repair-management"></a>Remonta pārvaldības pielietošana

Lai pielietotu remonta pārvaldību vienībai, vienībai jābūt iestatītam ar pakalpojumu objektu, kas ir saistībā ar pakalpojuma pasūtījumu. No pakalpojuma pasūtījuma variet pēc tam izveidot remonta rindu ar informāciju par pašreizējo problēmu. remonta rindā definējiet labojamo pakalpojuma objektu un informāciju par simptomiem, diagnozi un izpildījumu. Variet arī izveidot piezīmi remonta rindai.

Variet izveidot arī remonta rindas katram remonta procesa solim.

## <a name="create-a-repair-line-on-a-service-order"></a>Izveidojiet remonta rindu pakalpojuma pasūtījumā

1.  Dodieties uz **Pakalpojumu pārvaldības** \> **Pakalpojumu pasūtījumi** \> **Pakalpojumu pasūtījumi**.

2.  Izvēlieties pakalpojuma pasūtījumu ar pakalpojuma objektu, ko nepieciešams izlabot.

3.  Noklikšķiniet uz **Labot** \> **Labot rindas**, lai atvērtu veidlapu **Labot rindas**.

4.  Atlasiet **Jauns**, lai izveidotu jaunu rindu.

5.  Izvēlieties pakalpojuma objektu. Varat izvēlēties jebkuru objektu, kam pakalpojuma pasūtījumā iestatīta objekta relācija.

6.  Izvēlieties jebkuru priekšiestatīto simptomu, diagnozes un izpildes vērtību, kas ir svarīga labošanas rindā un, ja nepieciešams, pēc tam klikšķiniet uz cilnes **Piezīme**, lai izveidotu piezīmi labošanas rindai.

7.  Atlasiet **Saglabāt**, lai saglabātu jauno, laboto rindu. Veidlapas **Labošanas rindas** cilnē **Vispārīgi** lauks **Izveides datums un laiks** tiek atjaunināts ar saglabāšanas laiku.

## <a name="tracking-progress-and-resolving-a-repair-issue"></a>Sekošana norisei un labošanas problēmu atrisināšana

Varat izvēlēties labošanas rindas posmus, lai sekotu labošanas gaitai.

Kad labošanas problēma ir atrisināta, varat aizvērt labošanas rindu. Iestatiet tādu labošanas posmu, kuram ir iespējots rekvizīts **Pabeigts**. Pašreizējais datums un laiks tiek reģistrēti rindā kā pabeigšanas laiks.

## <a name="close-a-repair-line-for-a-resolved-issue"></a>Aizveriet izlabotās problēmas remonta rindu

1.  Atveriet veidlapu **Labošanas rindas**. Lai izveidotu labošanas rindu, rīkojieties iepriekš šajā rakstā.

2.  Izvēlieties remonta rindu ar remonta problēmu, ko vēlaties aizvērt.

3.  Laukā **Labošanas posms** atlasiet posmu, kuram ir iespējots rekvizīts **Pabeigts**.

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]