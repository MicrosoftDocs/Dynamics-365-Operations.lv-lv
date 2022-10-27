---
title: Kursu apskats
description: Šajā rakstā skaidrots kā personāla vadības administratori un vadītāji var izmantot kursu funkcijas, lai uzturētu informāciju par darbiniekiem pieejamajiem kursiem.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable, HcmLearningWorkspace
audience: Application User
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a1fd00fb9feea9ab426f67095770389696452215
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/25/2022
ms.locfileid: "9716285"
---
# <a name="courses-overview"></a>Kursu apskats

Microsoft Dynamics 365 Human Resources nodrošina risinājumu jūsu organizācijas apmācības vajadzībām. Šis risinājums piedāvā divus apmācību kursu ceļus: virtuālos *un* instruktorus *·*.

*Virtuālā apmācība* ir apmācības pieredze, kas ir paplašināta ar tiešsaistes resursu palīdzību. Instruktora *apmācības ietvaros* instruktors atvieglo apmācības sesiju darbinieku vai apmācības dalībnieku grupai.

Mūsu apmācības modulī cilvēku resursu profesionāļiem, administratoriem, apmācības vadītājiem un vadītājiem ir iespējams izveidot un piešķirt abus apmācības kursu ceļus darbiniekiem.

> [!NOTE]
> Lai lietotu virtuālos kursus, līdzekļa pārvaldībā **ir jāiespējo** funkcija Kursu uzlabojumi.

## <a name="set-up-virtual-courses"></a>Iestatīt virtuālos kursus

Lai konfigurētu virtuālos kursus, līdzekļa **pārvaldībā jāiespējo** funkcija Kursu uzlabojumi. Dodieties uz Jauns kursi un iestatiet opciju **Virtuāls \> uz** Jā **.** **·** Pēc funkcionalitātes iespējošanas nepieciešama kursu saite. Lauks **Kursu statuss** tiks iestatīts uz **Atvērts**. Opcija **Atļaut darbiniekam veikt pašreģistrēšanu** tiks iestatīta uz Jā **,** bet to var iestatīt uz **Nē**.

Kad funkcionalitātes **pārvaldībā ir iespējots** līdzeklis Kursu uzlabojumi, tiek veiktas šādas izmaiņas:

- Kursu piešķirei ir jādefinē apmaksas datums.
- Nepieciešama kursu saite.
- **Darbinieku pašapkalpošanās** rādīt darbinieka apskatu **kursos**. Lietotājs var apskatīt kursus, kas nokavēti, drīzumā un piešķirti.
- Darbinieki var izpildīt virtuālos kursus un pats tos pārbaudīt.

## <a name="set-up-instructor-led-courses"></a>Iestatiet instruktoru vadītos kursus

Instruktoru kursi ir jākonfigurē pirms to lietošanas.

Šī informācija nav obligāta un to var norādīt kursiem. Ja šī informācija tiks ievadīta kursiem, tā jāiestata pirms kursu ierakstu izveides:

- Kursu tips
- Mācību telpu grupas
- Kursu grupas
- Kursu norises vietas
- Mācību telpas
- Instruktori
- Kursu tipi

Kursu tipus *var lietot,* lai kategorizētu kursus atbilstoši to struktūrai vai saturam. Kursu tipus var izveidot lapā **Kursu** tipi.

Minimālais un maksimālais dalībnieku skaits, ko varat reģistrēt kursam **** , ir definēts kopsavilkuma cilnē **Kursi** .

### <a name="course-setup-type"></a>Kursu iestatīšanas veids 

*Iestatīšanas* tipi nosaka kursu struktūru. Kursiem ir trīs iestatījumu tipi.

| Iestatīšanas veids | Apraksts |
|------|--------|
| Standarta | Šī iestatīšanas tipa kursiem nav ikdienas darba kārtības. Tas ir noklusētais iestatījuma tips, veidojot jaunus kursus. |
| Darba kārtība | Atlasiet šo iestatījuma tipu, lai plānotu detalizētu informāciju katrai kursa dienai, kas notiek vairākās dienās. |
| Darba kārtībā + sesija | <p>Atlasiet šo iestatījuma tipu sarežģītākiem kursiem. Piemēram, kursu darba kārtību var dalīt kursos *un* *sesijās*:</p><ul><li>*Ceļi ir* specifiski kursu tēmas apgabali.</li><li>*Sesijas dala atsekošanas un palīdz noteikt specifiskus procesus vai paņēmienus*, kas ir svarīgi atsekošanai.</li></ul> |

### <a name="course-tasks"></a>Kursu uzdevumi

Katram kursam izpildiet šādus uzdevumus:

- reģistrēt dalībniekus;
- norādīt pēdējo reģistrācijas termiņu;
- definēt minimālo un maksimālo dalībnieku skaitu;
- Piešķiriet kursu atrašanās vietu un klasi.
- Iesakiet viesnīcu kursu dalībniekiem.
- Izveidojiet kursu aprakstu, ko var grāmatot darbinieku **pašapkalpošanās laikā**.

> [!NOTE]
> Kursu varat dzēst tikai tad, ja tam neviens nav reģistrēts.

### <a name="course-statuses"></a>Kursu statusi

Šajā tabulā ir uzskaitīti kursu statusi un katram no tiem pabeigtās darbības.

| Statuss | Darbības |
|------|--------|
| Izveidota | <ul><li>Ievadiet un modificējiet kursu informāciju.</li><li>Mainiet kursu statusu uz **** Atvērts, lai darbinieki varētu reģistrēties kursiem.</li></ul> | 
| Atvērt | <ul><li>Reģistrējiet dalībniekus kursiem.</li><li>Dzēsiet kursu dalībniekus.</li><li>Apstipriniet kursu dalībniekus.</li><li>Mainiet kursu statusu uz Slēgts **vai** Atcelts **tiem dalībniekiem, kuru statuss ir Apstiprināts** **.**</li></ul>|
| Slēgts | Kursus var atvērt atkārtoti. |
| Atcelta | Kursus var atvērt atkārtoti. |

### <a name="course-participants"></a>Kursu dalībnieki

*Kursa dalībnieki ir* darbinieki, kas piedalās apmācības kursā vai notikumā. Dalībniekus var reģistrēt tikai atvērtiem kursiem.

### <a name="workflow"></a>Darbplūsma

Darbinieki, kuri reģistrējas kursiem caur **** lapu Darbinieku pašapkalpošanās, var viņu reģistrāciju maršrutēt caur darbplūsmu apstiprināšanai. Varat piešķirt darbplūsmu kursiem kopsavilkuma **** cilnē Vispārīgi, lapā **Kursi** .
