---
title: Kreditora rēķina ieraksta darbvieta
description: Šajā tēmā ir paskaidrots, kā iestatīt darbvietu, kas saistīta ar kreditora rēķiniem, un kas parāda informāciju, kura pieejama izmantojot programmu Microsoft Power BI.
author: abruer
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2020-09-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: bac57056af6d85bb30600e13628279801508741d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837263"
---
# <a name="vendor-invoice-entry-workspace"></a>Kreditora rēķina ieraksta darbvieta

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šajā tēmā ir paskaidrots, kā iestatīt darbvietu, kas saistīta ar kreditora rēķiniem, un kas parāda informāciju, kura pieejama izmantojot programmu Microsoft Power BI. Kreditora rēķina informācija šajā darbvietā tiek filtrēta noteiktiem lietotājiem, un tā tiek rādīta grafiskā formātā.

## <a name="overview"></a>Pārskats

Darbvietā **Kreditoru rēķina ieraksts** tiek rādīta informācija, kas ir saistīta ar kreditora rēķina apstrādi. Tajā ir ietverts skats **Mans darbs** un lapa **Analīze — visi uzņēmumi**. Skatā **Mans darbs** tiek rādīti kopsavilkuma elementi, kreditoru transakciju režģi un saistītā kreditoru informācija. Lapā **Analīze — visi uzņēmumi** tiek izmantotas Microsoft Power BI iespējas, lai parādītu ar kreditora rēķiniem saistītās vizualizācijas.

## <a name="set-up-the-workspace-to-show-power-bi-content"></a>Darbvietas iestatīšana, lai rādītu Power BI saturu

Šis iestatījums ir jāpabeidz, pirms dati var tikt parādīti Power BI vizualizācijās, kas atrodas darbvietā **Kreditora rēķina ieraksts**.

1. Darbvietā **Līdzekļu pārvaldība** filtrējiet sarakstu, lai atrastu līdzekli **Kreditora rēķina automatizācija**.
3. Atlasiet **Iespējot tagad**.
4. Lai nodrošinātu, ka rēķinus var apstrādāt no sākuma līdz beigām bez manuālas iejaukšanās, iestatiet kreditora rēķinu darbplūsmu. Lai iestatītu darbplūsmu, dodieties uz **Kreditori \> Iestatījumi \> Kreditoru darbplūsmas**.
5. Dodieties uz **Kreditori \> Iestatījumi \> Kreditoru parametri** un atlasiet cilni **Kreditora rēķina automatizācija**. Papildinformāciju skatiet sadaļā [Kreditora rēķina automatizācijas iestatīšanas opcijas](vnd-invoice-set-up-options.md).
6. Iestatiet opciju **Automātiski iesniegt importētos rēķinus darbplūsmai** uz **Jā**.
7. Ja preču kvītis būtu automātiski jāsaskaņo, iestatiet opciju **Automātiski saskaņot preču kvītis ar rēķina rindām** uz **Jā**.
8. Pārskatiet atlikušos, neobligātos iestatījumus un konfigurējiet tos atbilstoši savas organizācijas prasībām.
9. Dodieties uz **Sistēmas administrēšana \> Iestatīšana \> Sistēmas parametri** un iestatiet laukus **Sistēmas valūta** un **Sistēmas maiņas kurss**.
10. Dodieties uz **Virsgrāmata \> Iestatīšana \> Virsgrāmata** un iestatiet laukus **Uzskaites valūta** un **Maiņas kursa veids**.
11. Dodieties uz **Virsgrāmata \> Valūtas \> Valūtas maiņas kursi** un ievadiet maiņas kursus starp darījuma valūtu un uzskaites valūtu un starp uzskaites valūtu un sistēmas valūtu.
12. Dodieties uz **Sistēmas administrēšana \> Iestatīšana \> Elementu krātuve** un meklējiet **Kreditora rēķina automatizācijas mērvienība**. Atlasiet **Atsvaidzināt**.

Lai skatītu informāciju, kas parādīta darbvietā, ir jābūt kreditoru pārvaldnieka vai kreditoru darbinieka drošības lomai.

## <a name="my-work-view"></a>Skats Mans darbs

### <a name="company-selection"></a>Uzņēmuma atlasīšana

Kad ir ieslēgts līdzeklis **Automatizēt kreditora rēķinus**, darbvietas augšpusē tiek parādīts lauks **Uzņēmums**. Atlase laukā **Uzņēmums** ietekmē visu darbvietā parādīto informāciju. Pēc noklusējuma skats parāda informāciju par uzņēmumu, kurā esat pierakstījies. Laukā **Uzņēmums** atlasot citu uzņēmumu, darbvietā varat parādīt informāciju par šo uzņēmumu. Pēc tam varat atlasīt kādu no darbvietas elementiem, lai atlasītajā uzņēmumā dotos uz saistīto lapu.

### <a name="summary-tiles"></a>Kopsavilkuma elementi

Sadaļas **Mans darbs** elementi **Neapmaksāto rēķinu kopsavilkums** sniedz pārskatu par jūsu kreditora rēķinu stāvokli. Var redzēt žurnālus, kas vēl nav grāmatoti, un rēķinus, kas ir aizturēti. Turklāt ir četri elementi, kas ir saistīti ar kreditora rēķina automatizācijas līdzekli:

- Nepieciešama manuāla ieejas plūsmas saskaņošana
- Saskaņošanas pārbaude neizdevās
- Rēķini nav iesniegti darbplūsmā
- Rēķini nav importēti

(Šiem četriem elementiem ir nepieciešams, lai Līdzekļu pārvaldībā būtu ieslēgts līdzeklis Kreditora rēķina automatizācija.)

Lai izmantotu elementu **Atgūt kreditora rēķinus**, līdzeklim ir jābūt ieslēgtam Kreditora parametros. Dodieties uz **Kreditori \> Kreditoru parametri** un pēc tam cilnē **Rēķins** iestatiet opciju **Atļaut kreditora rēķinu atgūšana** uz **Jā**.

Kad līdzeklis ir ieslēgts, redzēsit arī trīs elementus, kas sagrupēti kopā darbvietas sadaļā ar nosaukumu **Žurnāli**. Elementi ir ar nosaukumu **Žurnāli**, **Žurnāli — piešķirts man** un **Rēķinu kopa**. 

Informācija sadaļā **Neapmaksātu rēķinu kopsavilkums** ir paredzēta uzņēmumam, kas iestatīts kā noklusējuma uzņēmums, jums pierakstoties.

### <a name="creating-new-records"></a>Jaunu ierakstu veidošana

Lai izveidotu jaunu rēķina ierakstu, atlasiet **Jauns** un pēc tam sarakstā atlasiet vienu no šiem ierakstu veidiem:

- Kreditora rēķins
- Rēķinu žurnāls
- Globāls rēķinu žurnāls
- Rēķinu reģistrs
- Rēķinu apstiprināšana

Ņemiet vērā, ka jūsu izveidotais ieraksts ir balstīts uz uzņēmuma filtru, nevis uzņēmumu, kurā esat pierakstījies. Piemēram, jūs esat pierakstījies uzņēmumā **UMSF**, bet uzņēmuma filtrs ir iestatīts uz **GBSI**. Šādā gadījumā, atlasot **Jauns** un pēc tam atlasot ieraksta veidu sarakstā, ieraksts tiek izveidots uzņēmumā GBSI.

### <a name="documents-not-invoiced-grids"></a>Dokumenti, kas nav rēķinos iekļautie režģi

Sadaļā **Rēķinā neiekļautie dokumenti** ir ietverti režģi, kas parāda dokumentus, kuri gaida kreditora rēķinus.

Režģī **Atvērtie pirkšanas pasūtījumi** tiek rādīti visi pirkšanas pasūtījumi, kas vēl nav pilnībā iekļauti rēķinā. Varat izmantot pogu **Izrakstīt rēķinu tūlīt**, lai izveidotu kreditora rēķinu pirkšanas pasūtījumam. Varat izmantot pogu **Priekšapmaksas rēķins**, lai izveidotu priekšapmaksas rēķinu pirkšanas pasūtījumam.

Režģī **Preču saņemšana** tiek rādītas visas saņemšanas transakcijas, kas vēl nav pilnībā iekļautas rēķinā. Varat izmantot pogu **Izrakstīt rēķinu tūlīt**, lai izveidotu kreditora rēķinu pirkšanas pasūtījumam.

Režģī **Neapmaksātie kreditora rēķini** tiek rādīti visi kreditoru rēķini, kas nav iesniegti darbplūsmas sistēmai. Varat izmantot lauku **Meklēšana** un/vai uzņēmuma filtru, lai meklētu konkrētu kreditora rēķinu. Varat izmantot pogu **Rediģēt**, lai labotu transakciju, kas parādās režģī.

Režģī **Meklēt pirkšanas pasūtījumu**, varat uzmantot lauku **Meklēt**, lai meklētu konkrētu pirkšanas pasūtījumu.

### <a name="related-information"></a>Saistītā informācija

Varat skatīt informāciju par grāmatotajiem rēķiniem, izmantojot saites darbvietas labajā pusē. Šīs saites ietver **Atvērtie kreditora rēķini**, **Rēķinu žurnāls** un **Rēķinu vēsture un salīdzināšanas informācija**. Sadaļā **Kreditori** varat piekļūt filtrētajam sarakstam, kurā redzami visi aizturētie kreditori, vai arī varat izmantot saiti **Visi kreditori**. Ir pieejamas arī saites **Visi pirkšanas pasūtījumi** un **Atvērtās priekšapmaksas**.

### <a name="analytics--all-companies-page"></a>Lapa Analīze — visi uzņēmumi

Kad opcija **Automātiski iesniegt importētos rēķinus darbplūsmai** ir iestatīta uz **Jā** lapā **Kreditoru parametri**, varat skatīt automatizācijas analīzi. Lapa **Analīze — visi uzņēmumi** sniedz svarīgus rādītājus, piemēram, kreditoru rēķinus, ko apstiprina apstiprinātājs un uzņēmums. Šajā lapā ir piecas pārskatu lapas. Vienā lapā ir sniegts pārskats, savukārt pārējās lapās ir sniegta detalizēta informācija par kreditora automātiskajiem rādītājiem.

Nākamajā tabulā ir redzama katrā pārskata lapā pieejamā vizuālā informācija.

| Pārskata lapa                    | Vizualizēšanas |
|--------------------------------|----------------|
| Kreditoru rēķinu pārskats        | <ul><li>Gaidošie kreditoru rēķini automatizācijā sistēmas valūtā</li><li>Rēķini, kurus neizdevās importēt</li><li>Rēķini darbplūsmā</li><li>Bezkontakta rēķini pēdējās 30 dienās</li><li>Kopējie automātiskie rēķini pēdējās 30 dienās</li><li>Atvērto rēķinu bilance sistēmas valūtā</li><li>Kļūmes iemesli, pēdējās 30 dienas</li><li>Iegrāmatoto rēķinu procentuālā attiecība, kas tika apstrādāti automātiski</li><li>Dienas, lai apstrādātu rēķinu</ul></li> |
| Automatizācijas statuss              | <ul><li>Bezkontakta rēķini pēdējās 30 dienās</li><li>Bezkontakta rēķini pēdējās 30 dienās pa uzņēmumiem</li><li>Bezkontakta rēķini pēdējās 30 dienās pa kreditoru grupām</li><li>Iegrāmatoto rēķinu procentuālā attiecība, kas tika apstrādāti automātiski</li><li>Dienas, lai apstrādātu rēķinu</li></ul> |
| Rēķini, kurus neizdevās importēt | <ul><li>Rēķini, kurus neizdevās importēt</li><li>Rēķini, kurus uzņēmumam neizdevās importēt</li></ul> |
| Automatizācijas kļūmes iemesli | <ul><li>Rēķini neizdevās</li><li>Rēķini neizdevās pēc uzņēmuma</li><li>Rēķini neizdevās pēc kreditoru grupas</li></ul> |
| Darbplūsmas statuss                | <ul><li>Rēķini darbplūsmā</li><li>Kreditora rēķina darbplūsmas instances</li><li>Piešķīrums apstiprinātājam</li><li>Kreditora rēķina darbplūsma katram uzņēmumam</li><li>Vidējais dienu skaits darbplūsmā pēc apstiprinātāja</li></ul> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]