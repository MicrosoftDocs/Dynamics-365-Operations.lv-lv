---
title: Preču klāsta pārvaldība
description: Šajā tēmā ir paskaidroti pamata jēdzieni, kas tiek izmantoti preču klāsta pārvaldībai programmā Dynamics 365 Commerce, un ir sniegti jūsu projekta ieviešanas apsvērumi.
author: jblucher
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: Global
ms.author: jeffbl
ms.search.validFrom: 2017-11-21
ms.dyn365.ops.version: Application update 5
ms.openlocfilehash: 981d1c604a7ed461f207e78c8c7f073aff03be9e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980002"
---
# <a name="assortment-management"></a>Preču klāsta pārvaldība

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Pārskats

Programmā Dynamics 365 Commerce ir pieejami *preču klāsti*, kas sniedz iespēju pārvaldīt preču pieejamību dažādos kanālos. Preču klāsti norāda, kuras preces ir pieejamas noteiktos veikalos un noteiktā periodā.

Risinājumā Commerce ir preču klāsts viena vai vairāku kanālu (vai kanālu grupas, ja tiek izmantotas organizācijas hierarhijas) kartējums ar vienu vai vairākām precēm (vai preču grupām, ja tiek izmantotas kategoriju hierarhijas).

Kanāla kopējo preču kombināciju nosaka publicētie preču klāsti, kas piešķirti kanālam. Tādēļ katram kanālam varat konfigurēt vairākus aktīvus preču klāstus.

### <a name="basic-assortment-setup"></a>Pamata preču klāsta iestatīšana

Šajā piemērā katrā veikalā tiek konfigurēts unikāls preču klāsts. Šajā gadījumā 1. veikalā ir pieejama tikai 1. prece, bet 2. veikalā ir pieejama tikai 2. prece.

![Katra prece ir pieejama vienā veikalā](./media/Managing-assortments-figure1.png)

Lai 2. prece būtu pieejama 1. veikalā, varat pievienot preci 1. preču klāstam.

![2. prece pievienota 1. klāstam](./media/Managing-assortments-figure2.png)

Varat arī pievienot 2. preču klāstam 1. veikalu.

![1. veikals pievienots 2. klāstam](./media/Managing-assortments-figure3.png)

### <a name="organization-hierarchies"></a>Organizācijas hierarhijas

Ja vairākos kanālos ir vienāds preču klāsts, varat konfigurēt preču klāstu, izmantojot Commerce preču klāsta organizācijas hierarhiju. Pievienojot mezglus no šīs hierarhijas, tiks iekļauti visi šī mezgla un tā apakšmezglu kanāli.

![Organizācijas hierarhija](./media/Managing-assortments-figure4.png)

### <a name="product-categories"></a>Preces kategorijas

Līdzīgi var rīkoties arī ar precēm: var ietvert preču grupas, izmantojot preču kategoriju hierarhijas. Varat konfigurēt preču klāstus, iekļaujot vienu vai vairākus kategoriju hierarhijas mezglus. Tādā gadījumā preču klāstā tiks iekļautas visas kategorijas mezglā un tā apakšmezglos esošās preces.

![Preces kategorijas](./media/Managing-assortments-figure5.png)

### <a name="excluded-products-or-categories"></a>Izslēgtās preces vai kategorijas

Papildus preču un kategoriju iekļaušanai preču klāstos varat izmantot opciju Izslēgt, lai definētu konkrētas preces vai kategorijas, kas ir jāizslēdz no preču klāstiem. Šajā piemērā iekļausim visas preces noteiktā kategorijā, izņemot 2. preci. Šajā gadījumā nav jādefinē preču klāsta prece pēc preces vai jāizveido papildu kategoriju mezgli. Tā vietā varat vienkārši iekļaut kategoriju, bet izslēgt preci.

> [!NOTE]
> Ja saskaņā ar definīciju prece ir gan iekļauta vienā vai vairākos preču klāstos, gan izslēgta no tiem, prece vienmēr tiks uzskatīta kā izslēgta.

![Izslēgta prece](./media/Managing-assortments-figure6.png)

### <a name="global-and-released-products"></a>Globālas un realizētas preces

Preču klāsti tiek definēti globālā līmenī, un tiem var būt kanāli no vairākām juridiskajām personām. Preces un kategorijas, kas ir iekļautas preču klāstos tiek arī koplietotas starp juridiskajām personām. Tomēr, lai preci varētu pārdot, pasūtīt, iekļaut inventarizācijā vai saņemt kanālā (piemēram, pārdošanas punktā \[POS\]), tā ir jāatbrīvo. Lai gan divi atšķirīgu juridisko personu veikali var koplietot preču klāstu, kas ietver tādas pašas preces, šīs preces būs pieejamas tikai tad, ja tās tika izlaistas šīm juridiskajām personām.

### <a name="dynamic-and-static-assortments"></a>Dinamiskais un statiskais preču klāsts

Preču klāstus var definēt, izmantojot noteiktus kanālus un preces vai iekļaujot organizācijas vienības un kategorijas. Preču klāsti, kuros iekļauta atsauce uz šīm grupām, tiek uzskatīti par dinamiskajiem preču klāstiem. Ja šo grupu definīcija vai saturs tiek mainīts, kamēr preču klāsts ir aktīvs, mainīsies arī preču klāsta definīcija.

Piemēram, preču klāsts sākotnēji tika definēts un publicēts tā, lai tas būtu saistīts ar preču kategoriju. Ja kategorijai vēlāk tiek pievienotas papildu preces, šīs preces tiek automātiski iekļauts esošo preču klāsta definīcijā. Preces nav manuāli jāpievieno preču klāstam. Līdzīgi, ja organizācijas vienība tiek pievienota citam mezglam, organizācijas vienības preču klāsts tiek automātiski koriģēts, ņemot vērā šo definīciju.

### <a name="stopped-products"></a>Apturētās preces

Izlaistu preču izmantošanu pārdošanas procesā var apturēt, ieslēdzot iestatījumu formā **Pasūtījuma noklusējuma iestatījumi**. Šis iestatījums visbiežāk tiek izmantots tad, kad pienāk preces dzīves cikla beigas un to vairs nedrīkst pārdot nevienā kanālā. Šis iestatījums tiek ievērots preču klāstā, un neatkarīgi no preču klāsta konfigurācijas apturētas preces tajā šķirotas.

### <a name="blocked-products"></a>Bloķētās preces

Tā vietā, lai apturētu preces pārdošanu, tās pārdošanu uz laiku var bloķēt. Šo iestatījumu var konfigurēt izlaistās preces cilnē **Tirdzniecība**. Bloķētās preces joprojām tiek šķirotas, tomēr POS tiks saņemts ziņojums par to, ka preci nevar pārdot.

### <a name="date-effectivity"></a>Datuma efektivitāte

Preču klāstiem var izmantot datumus. Tādēļ mazumtirgotāji var konfigurēt, kad precēm ir vai nav jābūt pieejamām katrā kanālā. Varat noteikt un publicēt preču klāstus pirms laika, kā arī norādīt sākuma un beigu datumus. Preces automātiski kļūst pieejamas vai nepieejamas norādītajos datumos.

### <a name="process-assortments-batch-job"></a>Pakešuzdevums Apstrādāt preču klāstu

Lai preču klāsti, kas ir definēti risinājumā Commerce, stātos spēkā, tie vispirms ir jāapstrādā. Šo apstrādi jāveic tālāk norādīto iemeslu dēļ.

- Preču klāsta definīcijas ir jānormalizē tā, lai tās būtu vieglāk izmantojamas kanālos. Kanāla preču komplektēšanu var definēt, izmantojot vairākus preču klāstus, kas aptver dažādus datumus diapazonus. Ja serverī daļa šīs informācijas tiek aprēķināta pirms laika, tiek uzlabota veiktspēja kanālā.
- Preču klāstā esošās preces un kanālus var mainīt ārpus preču klāsta. Dynamic preču klāsti, kas satur atsauces uz kategorijām vai organizācijas vienībām, periodiski jāapstrādā tā, lai tajos tiktu iekļauti vai no tiem tiktu izslēgti ieraksti, pamatojoties uz to pašreizējo piešķiri.

## <a name="implementation-considerations"></a>Ieviešanas apsvērumi

Commerce implementēšanas nolūkā plānojot un pārvadot preču klāstus, ņemiet vērā tālāk minētās ieviešanas prasības.

- **Datu replicēšana un datu bāzes lielums** — lai gan preču klāsti palīdz uzņēmumam pārvaldīt preču pieejamību, tie ir arī svarīgs rīks kanāla lieluma un bezsaistes datu bāzu pārvaldīšanā. Labi pārvaldīti preču klāsti samazina to datu apjomu, kas jāapstrādā un jāreplicē kanālā un bezsaistes datu bāzēs. Tie arī palīdz samazināt nepieciešamo ierakstu skaitu. Mazāks ierakstus skaits šajās datu bāzēs sekmēs veiktspēju,kad pievienosiet transakcijai krājumus vai meklēsiet un pārlūkosiet preces.
- **Preču klāsti, kas ir derīgi/kam ir beidzies derīguma termiņš** — viens no visefektīvākajiem rīkiem, kā pārvaldīt preču skaitu kanālā un bezsaistes datu bāzēs, ir noteikt preču klāstiem to derīguma termiņu. Ja atstāsiet beztermiņa (kam nebeidzas termiņš) sezonas preču klāstus vai tādu preču klāstus, kam ir beidzies derīguma termiņš, šo datu bāzu apjoms nepārtraukti palielināsies. Situāciju var risināt dažādos veidos. Piemēram, varat glabāt atsevišķus sezonas preču klāstus un tādu preču klāstus, kuras ir vienmēr pieejamas.
- **Preču klāstā neesošu preču pārdošana un ieņēmumi no tām** — šī iespēja palīdz mazumtirgotājiem efektīvi pārvaldīt preču klāstus, ļaujot ierobežot pieejamo preču skaitu līdz precēm, kas pieder pie veikala pamata preču komplekta. Šī iespēja arī palīdz mazumtirgotājiem rīkoties situācijās, kad prece kļūdaini tiek izlaista preču klāstā vai kad prece tiek atgriezta ārpus preču klāsta derīguma termiņiem.

Ja kanāla datu bāzē preces dati nepastāv, POS veic reālā laika zvanu galvenajam birojam, lai izgūtu nepieciešamo informāciju, lai preci varētu pārdot, atgriezt vai ietvert debitora pasūtījumā. Šādā veidā izgūta preces informācija ir pieejama tikai šīs transakcijas ietvaros. Prece netiek pievienota preču klāsta definīcijai. Tādēļ nepieciešamības gadījumā tiks veikti turpmāki reāllaika zvani.
