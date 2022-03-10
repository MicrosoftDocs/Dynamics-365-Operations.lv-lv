---
title: Kreditoru maksājumu darbvieta
description: Šajā tēmā ir sniegta informācija par darbvietu Kreditoru maksājumi. Darbvietā Kreditoru maksājumi tiek rādīta informācija, kas ir saistīta ar kreditoru maksājumu apstrādi.
author: abruer
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymentWorkspace
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 084a18d1af789c7ebb89d9a598754a9478a48b83fb949241c9fc34fefa7c152b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6749274"
---
# <a name="vendor-payments-workspace"></a>Kreditoru maksājumu darbvieta

[!include [banner](../includes/banner.md)]

Darbvietā **Kreditoru maksājumi** tiek rādīta informācija, kas ir saistīta ar kreditoru maksājumu apstrādi. Šajā darbvietā ir ietverts skats **Mans darbs** un lapa **Analīze**. Skatā **Mans darbs** tiek rādīti kopsavilkuma elementi, kreditoru transakciju režģi un saistītā kreditoru informācija. Lapā **Analīze** tiek izmantotas programmas Microsoft Power BI iespējas, lai parādītu ar kreditoru maksājumiem saistītas vizualizācijas.

## <a name="setup-needed-to-view-power-bi-content"></a>Power BI satura skatīšanai nepieciešamie iestatījumi

Lai datus varētu parādīt sadaļas **Kreditoru maksājumi** Power BI vizuālajos līdzekļos, ir jāizpilda tālāk aprakstītā iestatīšana.
1. Dodieties uz **Sistēmas administrēšana > Iestatīšana > Sistēmas parametri** un iestatiet parametrus **Sistēmas valūta** un **Sistēmas maiņas kurss**.
2. Lai validētu finanšu kalendāra datumus, kas piešķirti aktīvajam laika periodam, dodieties uz **Virsgrāmata > Kalendāri > Finanšu kalendāri**.
3. Dodieties uz **Virsgrāmata > Iestatīšana > Virsgrāmata**, lai iestatītu vienumu **Uzskaites valūta** un **Maiņas kursa tips**. 
4. Nosakiet maiņas kursu starp transakciju valūtām un uzskaites valūtu un starp uzskaites valūtu un sistēmas valūtu. Lai to izdarītu, dodieties uz **Virsgrāmata > Valūtas > Valūtas maiņas kursi**.
5. Dodieties uz **Sistēmas administrēšana > Iestatīšana > Elementu krātuve**, lai atsvaidzinātu apkopošanas mērījumu **VendPaymentBIMeasureV2**.

## <a name="my-work-view"></a>Skats Mans darbs

### <a name="summary-tiles"></a>Kopsavilkuma elementi

Elementi sadaļā **Kopsavilkums** sniedz pārskatu par jūsu maksājumu informācijas stāvokli. Varat skatīt maksājumu žurnālus, kas vēl nav iegrāmatoti, rēķinus ar nokavētu termiņu, visus kreditorus un kreditorus, kas ir aizturēti. Sadaļā **Kopsavilkums** varat izveidot jaunu maksājuma izpildi.

Informācija sadaļā **Kopsavilkums** tiek rādīta par uzņēmumu, kura kontā esat pierakstījies.

### <a name="vendor-transactions-grids"></a>Kreditoru transakciju režģi

Sadaļā **Kreditoru transakcijas** ir režģi, kuros tiek rādīti rēķini ar nokavētu termiņu un maksājumi, kas nav nosegti. Režģī **Rēķini ar nokavētu termiņu** varat skatīt atlasītā rēķina segšanas vēsturi. Režģī **Nesegtie maksājumi** varat skatīt atlasītā rēķina segšanas vēsturi un nosegt rēķinu.

Centralizēto maksājumu darbinieki uzņēmuma atlasei var izmantot filtru, kas pieejams katra režģa augšdaļā. Režģis tiek filtrēts tā, lai tiktu parādīti tikai tie uzņēmumi, kas ir definēti centralizēto maksājumu organizācijas hierarhijā, ko centralizēto maksājumu darbiniekam ir tiesības skatīt.

Sadaļas **Kreditoru transakcijas** cilnē **Meklēt transakcijas** varat meklēt kreditoru transakcijas.

### <a name="related-information"></a>Saistītā informācija

Pārskatu **Kreditoru vecumstruktūra** un pārskatu **Maksājumu kopsavilkums pēc datuma** varat skatīt, izmantojot darbvietas sadaļā **Saistītā informācija** esošās saites.

## <a name="analytics-page"></a>Lapa Analīze

Lapā **Analīze** ir sniegti svarīgi rādītāji, piemēram, kreditoru rēķini ar nokavētu termiņu un kreditoru rēķini ar izpildes termiņu nākotnē. Šajā lapā ir deviņas pārskatu lapas. Vienā lapā ir sniegts pārskats, savukārt pārējās astoņās lapās ir sniegta detalizēta informācija par kreditoru maksājumu rādītājiem.

Nākamajā tabulā ir redzama katrā pārskata lapā pieejamā vizuālā informācija.


|            Pārskata lapa            |                                                                                                                                                                                Vizualizēšana                                                                                                                                                                                |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     Pārskats par kreditoru maksājumiem      | <ul><li>Rēķini ar nokavētu termiņu</li><li>Rēķini, kuru termiņš iestājas šodien</li><li>Saņemtās atlaides pret zaudētajām atlaidēm</li><li>Rēķini, kuru izpildes termiņš ir nākotnē, pēc termiņatlaides datuma</li><li>Rēķini, kuru izpildes termiņš ir nākotnē, pēc izpildes datuma</li><li>Rēķini, kuri apmaksāti novēloti, pret rēķiniem, kuri apmaksāti laikus</li><li>Maksājumu darbplūsmas piešķire</li><li>Kreditora bilance pret debitora bilanci</li><li>Atvērtie rēķini ar maksājuma aizturi</li></ul> |
|         Rēķini ar nokavētu termiņu         |                                                                                             <ul><li>Rēķini ar nokavētu termiņu</li><li>Rēķinu ar nokavētu termiņu detaļas</li><li>Atvērto rēķinu kopsumma</li><li>Rēķini ar nokavētu termiņu pēc kreditoru grupas</li><li>Rēķini ar nokavētu termiņu pēc uzņēmuma</li></ul>                                                                                              |
|        Rēķini, kuru termiņš iestājas šodien         |                                                                                                         <ul><li>Rēķini, kuru termiņš iestājas šodien</li><li>Rēķinu, kuru termiņš iestājas šodien, detaļas</li><li>Rēķini, kuru termiņš iestājas šodien, pēc uzņēmuma</li><li>Rēķini, kuru termiņš iestājas šodien, pēc kreditoru grupas</li></ul>                                                                                                          |
| Saņemtās atlaides pret zaudētajām atlaidēm |                                                                             <ul><li>Saņemtās atlaides pret zaudēto atlaidi</li><li>Saņemto atlaižu pret zaudēto atlaidi detaļas</li><li>Saņemtās atlaides pret zaudēto atlaidi pēc uzņēmuma</li><li>Saņemtās atlaides pret zaudēto atlaidi pēc kreditoru grupas</li></ul>                                                                              |
|      Rēķini, kuru izpildes termiņš ir nākotnē       |                                                 <ul><li>Rēķini, kuru izpildes termiņš ir nākotnē</li><li>Rēķinu, kuru izpildes termiņš ir nākotnē, detaļas</li><li>Rēķini, kuru izpildes termiņš ir nākotnē, pēc uzņēmuma</li><li>Rēķini, kuru izpildes termiņš ir nākotnē, pēc kreditoru grupas</li><li>Rēķini, kuru izpildes termiņš ir nākotnē, pēc termiņatlaides datuma</li><li>Rēķini, kuru izpildes termiņš ir nākotnē, pēc izpildes datuma</li></ul>                                                  |
|        Novēloti apmaksātie rēķini         |                                                         <ul><li>Rēķini, kas apmaksāti pēc izpildes datuma</li><li>Rēķinu, kas apmaksāti pēc izpildes datuma, detaļas</li><li>Rēķini, kas apmaksāti pēc izpildes datuma, pēc uzņēmuma</li><li>Rēķini, kas apmaksāti pēc izpildes datuma, pēc kreditoru grupas</li><li>Rēķini, kuri apmaksāti novēloti, pret rēķiniem, kuri apmaksāti laikus</li></ul>                                                          |
|         Maksājumu darbplūsma          |                                                                                <ul><li>Kreditora maksājumu darbplūsmas instances</li><li>Kreditora maksājumu darbplūsmas instances pēc apstiprinātāja</li><li>Kreditora maksājumu darbplūsmas instances pēc uzņēmuma</li><li>Vidējais dienu skaits darbplūsmā pēc apstiprinātāja</li></ul>                                                                                |
|    Kreditora bilance pret debitora bilanci     |                                                                                                                   <ul><li>Kreditora bilance pret debitora bilanci</li><li>Kreditora bilance pret debitora bilanci pēc uzņēmuma</li><li>Kreditora bilances pret debitora bilanci detaļas</li></ul>                                                                                                                    |
|    Rēķini ar maksājuma aizturi     |                                                                                         <ul><li>Rēķini ar maksājuma aizturi</li><li>Rēķinu ar maksājuma aizturi detaļas</li><li>Rēķini ar maksājuma aizturi pēc uzņēmuma</li><li>Rēķini ar maksājuma aizturi pēc kreditoru grupas</li></ul>                                                                                          |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]