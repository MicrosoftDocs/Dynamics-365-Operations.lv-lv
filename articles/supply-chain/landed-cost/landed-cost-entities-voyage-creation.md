---
title: Reisa izveides elementi
description: Šajā rakstā ir sniegta informācija par reisa izveides datu elementiem, kas grupē datu elementus, kas nepieciešami darba reisa izveidei.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: cb2e2f53942015caf9462692515f24deb9689aed
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873903"
---
# <a name="voyage-creation-entities"></a>Reisa izveides elementi

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

Reisa izveides datu entītiju grupa grupē datu elementus, kas ir nepieciešami darba reisa izveidei. Jūs vai jūsu kravas ekspediators var izmantot šīs datu entītijas, lai izveidotu reisu, pārvadāšanas konteineru, folio un reisa rindu ierakstus, kam ir atsauce uz esošo pirkšanas pasūtījumu vai pārsūtīšanas pasūtījuma rindām.

## <a name="voyages-itmtableentity"></a>Reisi (ITMTableEntity)

Reiss ir ienākošo preču maršruts, un tas darbojas kā augstākā līmeņa izmaksu apgabals zemes izmaksās. Tajā ir virsraksta līmeņa informācija, kas saistīta ar kuģi, izcelsmes ostu un mērķa ostu. Šo funkcionalitāti atbalsta elements `ITMTableEntity`. Šajā tabulā ir uzskaitīti lauki un kartējumi, kas veido šo elementu.

| Nosaukums/vārds, uzvārds | Kartēšana | Datu veids | Taustiņš | Obligāts |
|---|---|---|---|---|
| Piegādes veids | ITMTable.DlvModeId | Nvarchar(10) | Nē | Nē |
| Brokeris ieteica | ITMTable.ITMBrokerAdvised | Datetime | Nē | Nē |
| Norunātā tikšanās ar klientu | ITMTable.ITMCustomerAppointment | Datetime | Nē | Nē |
| Sūtījums piegādāts noliktavā | ITMTable.ITMDelAtWarewareware | Datetime | Nē | Nē |
| Piegādes instrukcijas | ITMTable.ITMDeliveryInstructions | Datetime | Nē | Nē |
| Izbraukšanas datums | ITMTable.ITMDepartureDate | Datetime | Nē | Nē |
| Preces izpildītas | ITMTable.ITMGoodsReleased | Datetime | Nē | Nē |
| Vietējā transporta datums | ITMTable.ITMLocalTransportdate | Datetime | Nē | Nē |
| Vietējā transporta laiks | ITMTable.ITMLocalTransportTime | Int | Nē | Nē |
| Sākotnējais piegādes rēķins nosūtīts | ITMTable.ITMOriginalBOLSebt | Datetime | Nē | Nē |
| Oriģinālais dokuments saņemts | ITMTable.ITMOriginalDocsReceived | Datetime | Nē | Nē |
| Pirkšanas pasūtījuma statuss | ITMTable.ITMPurchStatus | Int | Nē | Nē |
| Pārbaudes datums | ITMTable.ITMVerificationDate | Datetime | Nē | Nē |
| Muitas ieraksta identifikators | ITMTable.ShipCustomsEntryId | Nvarchar(20) | Nē | Nē |
| Nosūtīšanas datums | ITMTable.ShipDate (nosūtīšanas datums) | Datetime | Nē | Nē |
| Apraksts | ITMTable.ShipDescription | Nvarchar(60) | Nē | Nē |
| Saņemtie dokumenti | ITMTable.ShipDocReceived | Int | Nē | Nē |
| Aprēķinātais piegādes datums | ITMTable.ShipEstDlvDate | Datetime | Nē | Nē |
| ETA nosūtīšanas ostā | ITMTable.ShipEstPortDate | Datetime | Nē | Nē |
| No porta | ITMTable.ShipFromPort | Nvarchar(20) | Nē | Nē |
| Komu gaisa ceļš/Preču transporta pavadzīme | ITMTable.ShipHAWB | Nvarchar(20) | Nē | Nē |
| Reiss | ITMTable.ShipId | Nvarchar(20) | **Jā** | **Jā** |
| Rezervēšanas atsauce | ITMTable.ShipIdExternal | Nvarchar(20) | Nē | Nē |
| Maršruta veidne | ITMTable.ShipJourmidId | Nvarchar(20) | Nē | Nē |
| Vietējais ekspeditors | ITMTable.ShipLocalForwarder | Nvarchar(20) | Nē | Nē |
| Galvenais gaisa veids/preču transporta pavadzīme | ITMTable.ShipmAWB | Nvarchar(20) | Nē | Nē |
| Mērījums | ITMTable.ShipMeasurement | Skaitlis (32, 6) | Nē | Nē |
| Mērvienība | ITMTable.ShipMeasurementUnit | Int | Nē | Nē |
| Palešu skaits | ITMTable.ShipNoOfPallets | Int | Nē | Nē |
| Neapstiprināts reiss | ITMTable.ShipPending | Int | Nē | Nē |
| Atzīmes | ITMTable.ShipRemarks | Nvarchar (MAX) | Nē | Nē |
| Noma | ITMTable.ShipRental | Int | Nē | Nē |
| Reisa statuss | ITMTable.ShipStatusId | Nvarchar(20) | Nē | Nē |
| Neskaitļa skaitlis | ITMTable.ShiptallyInNumber | Nvarchar(20) | Nē | Nē |
| Uz ostu | ITMTable.ShipToPort (tikai datu tips) | Nvarchar(20) | Nē | Nē |
| Apstiprināšanas datums | ITMTable.ShipValuationDate | Datetime | Nē | Nē |
| Nosūtīšanas uzņēmums | ITMTable.ShipVendAccount | Nvarchar(20) | Nē | Nē |
| Kuģis | ITMTable.ShipVesselId | Nvarchar(20) | Nē | **Jā** |
| Ārējais reisa ID | ITMTable.ShipVoyage | Nvarchar(20) | Nē | Nē |

### <a name="number-sequences-for-voyages"></a>Reisu numuru sērijas

Reisu koplietojamā numuru sērija kontrolē reisu IDENTIFIKĀCIJAS numuru sadalījumu.

Vērtība, kas tiek nodota datu elementam kā reisa **ID** (`ShipId`) vērtība tiek izmantota, lai identificētu esošu ierakstu atjaunināšanai. Ja šis ieraksts nepastāv, uzvedība ir atkarīga no tā, vai piešķirtā numuru sērija ir konfigurēta manuālai ievadei:

- Ja ir aktivizēta manuālā ievade, tiek izveidots jauns ieraksts, kas izmanto nodoto vērtību.
- Ja nav aktivizēta manuālā ievade, nākamais numurs piešķirtā numuru sērijā tiek izmantots nodotās vērtības vietā.

Importēšanas sesijas laikā tiek saglabāta viettura vērtība, kas tiek importēta kā reisa ID. Šī darbība nodrošina, ka nosūtīšanas konteiners un reisa rindas, kas norāda, ka vietturis ir iekļautas reisā un ka tās tiek atjauninātas, lai attēlotu vērtību, kas ir piešķirta no numuru sērijas.

### <a name="automatic-cost-transactions"></a>Automātiskas izmaksu darbības

Automātiskās izmaksas var pievienot reisam no Automātiskās **izmaksu lapas** Microsoft Dynamics 365 Supply Chain Management (**Kopējās izmaksas \> iestatījuma \> Automātiskās izmaksas**). Automātisko izmaksu ierakstus var izveidot arī, izmantojot izmaksu darbību datu elementus katrai izmaksu jomai, ko atbalsta zemes izmaksas.

Automātiskās izmaksas, kas ir konfigurētas Piegādes ķēžu pārvaldībā, tiek piemērotas reisam, kad tiek izveidota reisa rinda. Šim ierakstam izmaksas nav redzamas, līdz virsraksta ieraksts nav saistīts ar rindas informāciju.

## <a name="shipping-containers-itmcontainersentity"></a>Sūtījumu konteineri (ITMContainersEntity)

Pārvadāšanas konteiners ir fizisks konteiners, kurā tiek transportētas preces. Šis fiziskais konteiners var būt kravas pārvadāšanas konteiners kravām vai viena palete gaisa transportam. Nosūtīšanas konteiners ietver virsraksta līmeņa informāciju, kas ir saistīta ar pārvadāšanas konteinera ID, zīmoga numuru un pārvadāšanas konteinera veidu. (Nosūtīšanas konteinera veids nodrošina dimensijas informāciju.) Šo funkcionalitāti atbalsta elements `ITMContainersEntity`. Šajā tabulā ir uzskaitīti lauki un kartējumi, kas veido šo elementu.

| Nosaukums/vārds, uzvārds | Kartēšana | Datu veids | Taustiņš | Obligāts |
|---|---|---|---|---|
| Izbraukšanas datums | ITMContainers.ITMDepartureDate | Datetime | Nē | Nē |
| Vietējā transporta datums | ITMContainers.ITMLocalTransportdate | Datetime | Nē | Nē |
| Vietējā transporta laiks | ITMContainers.ITMLocalTransportTime | Int | Nē | Nē |
| Oriģinālais reiss | ITMContainers.OrigShipId | Nvarchar(20) | Nē | Nē |
| Faktiskais svars | ITMContainers.ShipActualWeight | Skaitlis (32, 6) | Nē | Nē |
| Brokeris ieteica | ITMContainers.ShipBrokerAdvised | Datetime | Nē | Nē |
| Nosūtīšanas konteiners | ITMContainers.ShipContainerId | Nvarchar(20) | **Jā** | **Jā** |
| Nosūtīšanas konteinera veids | ITMContainers.ShipContainerTypeId | Nvarchar(20) | Nē | Nē |
| Vienības veids | ITMContainers.ShipContainerUnitTypeId | Nvarchar(10) | Nē | Nē |
| Pārvērsts par nomas līgumu | ITMContainers.ShipConvertedToRental | Int | Nē | Nē |
| Norunātā tikšanās ar klientu | ITMContainers.ShipCustomerAppointment | Datetime | Nē | Nē |
| Nosūtīšanas datums | ITMContainers.ShipDate | Datetime | Nē | Nē |
| Sūtījums piegādāts noliktavā | ITMContainers.ShipDelAtWarewareware; | Datetime | Nē | Nē |
| Piegādes instrukcijas | ITMContainers.ShipDeliveryInstructions | Datetime | Nē | Nē |
| Pārbaudes sertifikāta piemērošanas datums | ITMContainers.ShipECApplieddate | Datetime | Nē | Nē |
| Pārbaudes sertifikāta derīguma beigu datums | ITMContainers.ShipECExpiryDate | Datetime | Nē | Nē |
| Pārbaudes sertifikāta numurs | ITMContainers.ShipECNum | Nvarchar(20) | Nē | Nē |
| Pārbaudes sertifikāta saņemšanas datums | ITMContainers.ShipECReceivedDate | Datetime | Nē | Nē |
| Aprēķinātais piegādes datums | ITMContainers.ShipEstDlvDate | Datetime | Nē | Nē |
| ETA nosūtīšanas ostā | ITMContainers.ShipEstPortDate | Datetime | Nē | Nē |
| Paredzamais iekraušanas datums | ITMContainers.ShipExpectedLoadingDate | Datetime | Nē | Nē |
| No porta | ITMContainers.ShipFromPort | Nvarchar(20) | Nē | Nē |
| Preču apraksts | ITMContainers.ShipGoodsDesc | Nvarchar(60) | Nē | Nē |
| Preces izpildītas | ITMContainers.ShipGoodsReleased | Datetime | Nē | Nē |
| GPS izsekošanas vienība | ITMContainers.ShipGPSUnit | Nvarchar(30) | Nē | Nē |
| Komu gaisa ceļš/Preču transporta pavadzīme | ITMContainers.ShipHAWB | Nvarchar(20) | Nē | Nē |
| Reiss | ITMContainers.ShipId | Nvarchar(20) | **Jā** | **Jā** |
| Maršruta veidne | ITMContainers.ShipJourmidId | Nvarchar(20) | Nē | Nē |
| Vietējais ekspeditors | ITMContainers.ShipLocalForwarder | Nvarchar(20) | Nē | Nē |
| Mērījums | ITMContainers.ShipMeasurement | Skaitlis (32, 6) | Nē | Nē |
| Mērvienība | ITMContainers.ShipMeasurementUnit | Int | Nē | Nē |
| Kastu skaits | ITMContainers.ShipNoOfCartons | Skaitlis (32, 6) | Nē | Nē |
| Sākotnējais piegādes rēķins nosūtīts | ITMContainers.ShipOriginalBOLSebt | Datetime | Nē | Nē |
| Oriģinālais dokuments saņemts | ITMContainers.ShipOriginalDocsReceived | Datetime | Nē | Nē |
| Mūsu zīmoga numurs | ITMContainers.ShipOurSealNum | Nvarchar(20) | Nē | Nē |
| Izmantots | ITMContainers.ShipPendingUsed | Int | Nē | Nē |
| Pirkšanas pasūtījuma statuss | ITMContainers.ShipPurchStatus | Int | Nē | Nē |
| Dzesēšanas veids | ITMContainers.ShipRefmererationTypeId | Nvarchar(10) | Nē | Nē |
| Atzīmes | ITMContainers.ShipRemarks | Nvarchar (MAX) | Nē | Nē |
| Noma | ITMContainers.ShipRental | Int | Nē | Nē |
| Atgriežams | ITMContainers.ShipReturnable (francija) | Int | Nē | Nē |
| Reisa statuss | ITMContainers.ShipStatusId | Nvarchar(20) | Nē | Nē |
| Nosūtīšanas uzņēmuma zīmoga numurs | ITMContainers.ShipTheirSealNum | Nvarchar(20) | Nē | Nē |
| Uz ostu | ITMContainers.ShipToPort | Nvarchar(20) | Nē | Nē |
| Pārbaudes datums | ITMContainers.ShipVerificationDate | Datetime | Nē | Nē |
| Kuģis | ITMContainers.ShipVesselId | Nvarchar(20) | Nē | **Jā** |

### <a name="voyage-id-validation"></a>Reisa ID apstiprināšana

Piegādes konteinera ID nekontrolē numuru sērija. Tas ir unikāls tikai reisa kontekstā, kurā tas tiek izmantots.

Ja nosūtīšanas konteinera elements (`ITMContainersEntity`) tiek izmantots neatkarīgi no reisa elementa (), `ITMTableEntity` reisa ID **(**`ShipId`) vērtībai ir jāatbilst reisa tabulas esošajam ierakstam. Pretējā gadījumā imports neizdosies.

Ja sūtījuma konteinera elements (`ITMContainersEntity`) un reisa elements (`ITMTableEntity`) tiek izmantoti kā daļa no tās pašas importēšanas sesijas, reisa elementam pirms nosūtīšanas konteinera izveides ir jābūt pirms nosūtīšanas konteinera izveides. Pretējā gadījumā **reisa ID** (`ShipId`) vērtību nevar sekmīgi validēt. Ja reisa **ID () vērtībai tiek izmantota viettura vērtība, saistību var izveidot tikai tad,** ja nosūtīšanas konteinera elementam tiek izmantots tas pats vietturis kā Reisa ID`ShipId`**(**`ShipId`) vērtība.

### <a name="other-field-validations"></a>Citu lauku pārbaudes

Tabulā ir parādīti lauki nosūtīšanas konteinera tabulā (`ITMContainers`), kas ir pārbaudīti attiecībā uz zemes izmaksu iestatījumu tabulām. Rāda arī zemes izmaksu datu elementus, ko kravas ekspediators var izmantot, lai lasītu esošās vērtības un nodrošinātu, ka jūsu vidē tiek saņemtas derīgas vērtības.

| Lauks tabulā ITMContainers | Zemes izmaksu datu elements |
|---|---|
| Nosūtīšanas konteinera veids | ITMShippingContainerTypeEntity |
| Preču apraksts | ITMGoodsDescriptionEntity |
| Dzesēšanas veids | ITMShippingContainerRefmererationTypeEntity |

## <a name="folios-itmfolioentity"></a>Kases (ITMFolioEntity)

Folio ir krājumu grupējums pārvadāšanas konteinerā muitas deklarāciju nolūkos. Folio ietver virsraksta līmeņa informāciju, kas ir saistīta ar muitas starpnieku, un preču aprakstu. Šo funkcionalitāti atbalsta elements `ITMFolioEntity`. Šajā tabulā ir uzskaitīti lauki un kartējumi, kas veido šo elementu.

| Nosaukums/vārds, uzvārds | Kartēšana | Datu veids | Taustiņš | Obligāts |
|---|---|---|---|---|
| Brokeris ieteica | ITMFolioTable.ShipBrokerAdvised | Datetime | Nē | Nē |
| Kravas kontroles numurs | ITMFolioTable.ShipCargoControlNumber | Nvarchar(20) | Nē | Nē |
| Norunātā tikšanās ar klientu | ITMFolioTable.ShipCustomerAppointment | Datetime | Nē | Nē |
| Muitas aģents | ITMFolioTable.ShipCustomsBroker | Nvarchar(20) | Nē | Nē |
| Muitas ID | ITMFolioTable.ShipCustomsId | Nvarchar(60) | Nē | Nē |
| Uzņēmums | ITMFolioTable.ShipDataArea | Nvarchar(4) | Nē | **Jā** |
| Sūtījums piegādāts noliktavā | ITMFolioTable.ShipDelAtWarewareware; | Datetime | Nē | Nē |
| Piegādes instrukcijas | ITMFolioTable.ShipDeliveryInstructions | Datetime | Nē | Nē |
| Saņemtie dokumenti | ITMFolioTable.ShipDocReceived | Int | Nē | Nē |
| Aprēķinātais piegādes datums | ITMFolioTable.ShipEstDlvDate | Datetime | Nē | Nē |
| ETA nosūtīšanas ostā | ITMFolioTable.ShipEstPortDate | Datetime | Nē | Nē |
| Eksportētājs | ITMFolioTable.ShipExporterId | Nvarchar(20) | Nē | Nē |
| Nosaukums/vārds, uzvārds | ITMFolioTable.ShipExporterName | Nvarchar(60) | Nē | Nē |
| Folio datums | ITMFolioTable.ShipFolioDate | Datetime | Nē | Nē |
| Folio | ITMFolioTable.ShipFolioId | Nvarchar(20) | **Jā** | **Jā** |
| No porta | ITMFolioTable.ShipFromPort | Nvarchar(20) | Nē | Nē |
| Preču apraksts | ITMFolioTable.ShipGoodsDesc | Nvarchar(60) | Nē | Nē |
| Preces izpildītas | ITMFolioTable.ShipGoodsReleased | Datetime | Nē | Nē |
| Komu gaisa ceļš/Preču transporta pavadzīme | ITMFolioTable.ShipHAWB | Nvarchar(20) | Nē | Nē |
| Reiss | ITMFolioTable.ShipId | Nvarchar(20) | Nē | **Jā** |
| Mērījums | ITMFolioTable.ShipMeasurement | Skaitlis (32, 6) | Nē | Nē |
| Mērvienība | ITMFolioTable.ShipMeasurementUnit | Int | Nē | Nē |
| Kastu skaits | ITMFolioTable.ShipNoOfCartons | Skaitlis (32, 6) | Nē | Nē |
| Sākotnējais piegādes rēķins nosūtīts | ITMFolioTable.ShipOriginalBOLSebt | Datetime | Nē | Nē |
| Oriģinālais dokuments saņemts | ITMFolioTable.ShipOriginalDocsReceived | Datetime | Nē | Nē |
| Pirkšanas pasūtījuma statuss | ITMFolioTable.ShipPurchStatus | Int | Nē | Nē |
| Atzīmes | ITMFolioTable.ShipRemarks | Nvarchar (MAX) | Nē | Nē |
| Reisa statuss | ITMFolioTable.ShipStatusId | Nvarchar(20) | Nē | Nē |
| Tarifa kods | ITMFolioTable.ShipTariffCode | Nvarchar(10) | Nē | Nē |
| Uz ostu | ITMFolioTable.ShipToPort (tikai datu tips) | Nvarchar(20) | Nē | Nē |
| Apstiprināšanas datums | ITMFolioTable.ShipValuationDate | Datetime | Nē | Nē |
| Pārbaudes datums | ITMFolioTable.ShipVerificationDate | Datetime | Nē | Nē |
| Kreditora konts | ITMFolioTable.VendAccount | Nvarchar(20) | Nē | Nē |

### <a name="number-sequences-for-folios"></a>Numuru sērijas, kas paredzēts sarakstu numerācijai

Skaitliskā secība, kas nosaka folio IDENTIFIKĀCIJAS numuru sadalījumu.

Vērtība, kas tiek nodota datu elementam kā **Folio ID** (`FolioId`) vērtība tiek izmantota, lai identificētu esošu ierakstu atjaunināšanai. Ja šis ieraksts nepastāv, uzvedība ir atkarīga no tā, vai piešķirtā numuru sērija ir konfigurēta manuālai ievadei:

- Ja ir aktivizēta manuālā ievade, tiek izveidots jauns ieraksts, kas izmanto nodoto vērtību.
- Ja nav aktivizēta manuālā ievade, nākamais numurs piešķirtā numuru sērijā tiek izmantots nodotās vērtības vietā.

Importēšanas sesijas laikā tiek saglabāta viettura vērtība, kas tiek importēta kā folio ID. Šī darbība nodrošina, ka reisa rindas, kas atsaucas uz vietturi, ir pareizi saistītas un ka tās tiek atjauninātas, lai atspoguļotu vērtību, kas ir piešķirta no numuru sērijas.

### <a name="field-validations"></a>Lauka pārbaudes

Preču **lauka apraksts folio** tabulā (`ITMFolioTable`) ir pārbaudīts attiecībā pret tā paša nosaukuma zemes izmaksu iestatījumu tabulu. Kravas ekspediators var izmantot `ITMGoodsDescriptionEntity` zemes izmaksu datu elementu, lai lasītu esošās vērtības un nodrošinātu, ka vidē tiek saņemtas derīgas vērtības.

## <a name="voyage-lines-for-purchase-orders-itmpurchaselineentity"></a>Pirkšanas pasūtījumu reisa rindas (ITMPurchaseLineEntity)

Reisa rinda norāda vienu pirkšanas pasūtījuma rindu, kas ir iekļauta reisā. Šī saistība tiek izveidota, izmantojot pirkšanas **pasūtījuma numura un** pirkšanas **rindas numura laukus**. Reisa rinda atsaucas uz katru iepriekšējo ierakstu, kas tika izveidots reisam, nosūtīšanas konteineram un folio. Šo funkcionalitāti atbalsta elements `ITMPurchaseLineEntity`. Šajā tabulā ir uzskaitīti lauki un kartējumi, kas veido šo elementu.

| Nosaukums/vārds, uzvārds | Kartēšana | Datu veids | Taustiņš | Obligāts |
|---|---|---|---|---|
| Valūta | ITMLine.CurrencyCode | Nvarchar(3) | Nē | Nē |
| Neto summa | ITMLine.LineAmountmst | Skaitlis (32, 6) | Nē | Nē |
| Pirkšanas rindas numurs | ITMLine.RefRecId | Skaitlis (32, 6) | **Jā** | Nē |
| Nosūtīšanas konteiners | ITMLine.ShipContainerId | Int | Nē | Nē |
| Uzņēmums | ITMLine.ShipDataArea | Nvarchar(20) | **Jā** | Nē |
| Deklarētais daudzums | ITMLine.ShipDeclaredQty | Nvarchar(4) | Nē | Nē |
| Folio | ITMLine.ShipFolioId | Skaitlis (32, 6) | Nē | Nē |
| Reiss | ITMLine.ShipId | Nvarchar(20) | **Jā** | Nē |
| Krājuma numurs | ITMLine.ShipItemId | Nvarchar(20) | Nē | Nē |
| Mērījums | ITMLine.ShipMeasurement | Nvarchar(20) | Nē | Nē |
| Mērvienība | ITMLine.ShipMeasurementUnit | Skaitlis (32, 6) | Nē | Nē |
| Kastu skaits | ITMLine.ShipNoOfCartons | Int | Nē | Nē |
| Vieta | ITMLine.ShipPosition | Skaitlis (32, 6) | Nē | Nē |
| Daudzums | ITMLine.Shipqty | Int | Nē | Nē |
| Pirkšanas pasūtījuma numurs | ITMLine.TransRefId | Skaitlis (32, 6) | **Jā** | Nē |
| Vienība | ITMLine.UnitId | Int | Nē | Nē |
| Apjoms | ITMLine.Apjoms | Nvarchar(10) | Nē | Nē |
| Lielums | ITMLine.Svars | Skaitlis (32, 6) | Nē | Nē |

## <a name="voyage-lines-for-transfer-orders-itmtransferlineentity"></a>Pārsūtīšanas pasūtījumu reisa rindas (ITMTransferLineEntity)

Reisa rinda norāda vienu pārsūtīšanas pasūtījuma rindu, kas ir iekļauta reisā. Šī saistība tiek izveidota, izmantojot pārsūtīšanas **pasūtījuma numuru un** pārsūtīšanas **rindas numura laukus**. Reisa rinda atsaucas uz katru iepriekšējo ierakstu, kas tika izveidots reisam, nosūtīšanas konteineram un folio. Šo funkcionalitāti atbalsta elements `ITMTransferLineEntity`. Šajā tabulā ir uzskaitīti lauki un kartējumi, kas veido šo elementu.

| Nosaukums/vārds, uzvārds | Kartēšana | Datu veids | Taustiņš | Obligāts |
|---|---|---|---|---|
| Valūta | ITMLine.CurrencyCode | Nvarchar(3) | Nē | Nē |
| Neto summa | ITMLine.LineAmountmst | Skaitlis (32, 6) | Nē | Nē |
| Nosūtīšanas konteiners | ITMLine.ShipContainerId | Int | Nē | Nē |
| Uzņēmums | ITMLine.ShipDataArea | Nvarchar(20) | **Jā** | Nē |
| Deklarētais daudzums | ITMLine.ShipDeclaredQty | Nvarchar(4) | Nē | Nē |
| Folio | ITMLine.ShipFolioId | Skaitlis (32, 6) | Nē | Nē |
| Reiss | ITMLine.ShipId | Nvarchar(20) | **Jā** | Nē |
| Krājuma numurs | ITMLine.ShipItemId | Nvarchar(20) | Nē | Nē |
| Mērījums | ITMLine.ShipMeasurement | Nvarchar(20) | Nē | Nē |
| Mērvienība | ITMLine.ShipMeasurementUnit | Skaitlis (32, 6) | Nē | Nē |
| Kastu skaits | ITMLine.ShipNoOfCartons | Int | Nē | Nē |
| Vieta | ITMLine.ShipPosition | Skaitlis (32, 6) | Nē | Nē |
| Daudzums | ITMLine.Shipqty | Int | Nē | Nē |
| Pārsūtīšanas rindas numurs | ITMLine.TransferLineNumber | Skaitlis (32, 6) | **Jā** | Nē |
| Pārveduma pasūtījuma numurs | ITMLine.TransRefId | Skaitlis (32, 6) | **Jā** | Nē |
| Vienība | ITMLine.UnitId | Int | Nē | Nē |
| Apjoms | ITMLine.Apjoms | Nvarchar(10) | Nē | Nē |
| Lielums | ITMLine.Svars | Skaitlis (32, 6) | Nē | Nē |

### <a name="reference-table"></a>Atsauču tabula

Reisa rindas tiek izveidotas ar saistībām ar atvērto saņemšanas pasūtījuma rindu. Šī rinda var būt pirkšanas pasūtījumā vai arī pārsūtīšanas pasūtījumā tā var būt saņemšanas darbība. Reisa `RefTableId` rindu tabulas lauks (`ITMLine`) norāda, ar kuru pasūtījuma tipu rinda ir saistīta, atsaucoties uz tabulas numuru. Ja tabulā, kur tiek veidoti dati, ir atsauces uz specifiskiem tabulu numuriem, entītijas tiek sadalītas, pamatojoties uz šīm vērtībām.

Atsauces tabulas () un darbības tipa vērtības (`RefTableId``TransType`) ir netieši ietvertas atlasē vai nu zemes izmaksu pirkšanas rindas elementu, vai zemes izmaksu pārsūtīšanas rindas elementu.

### <a name="validation"></a>Apstiprināšana

Reisa rinda tieši atsaucas uz reisa ierakstu, pārvadāšanas konteinera ierakstu un folio ierakstu. Ja pirkšanas rindas elements (`ITMPurchaseLinesEntity`) vai pārsūtīšanas rindas elements (`ITMPurchaseLinesEntity`) tiek izmantots neatkarīgi no entītijām, ko izmanto šo atsauces ierakstu veidojiet, **Reisa ID** (`ShipId`),**Nosūtīšanas** konteinera (`ShipContainerId`**) un Folio** (`ShipFolioId`) vērtībām jāatbilst esošajam ierakstam atbilstošajās tabulās. Pretējā gadījumā imports neizdosies.

Ja kā daļa no tās pašas importēšanas sesijas tiek izmantots vai nu rindas elements, šiem citiem elementiem jābūt pirms reisa rindas izveides. Pretējā gadījumā vērtības nevar sekmīgi validēt. Ja reisa vai folio numuram tiek izmantota viettura vērtība, saistību var izveidot tikai tad, ja reisa rindas entītijā reisa vai folio numuram tiek izmantots tas pats vietturis.

Ja pirkšanas pasūtījums vai pārsūtīšanas pasūtījuma rinda jau ir piešķirta esošai reisa rindai, jauna reisa rinda netiks izveidota. Pirms pasūtījuma rindu var piešķirt jaunam reisam, tas ir jānoņem no tā pašreizējā reisa.

### <a name="order-line-identification"></a>Pasūtījuma rindas identifikācija

Reisa rindas tieši atsaucas uz **atsauces ieraksta ID** (`RefRecId`), **krājumu dimensijas ID** (`InventDimId`) un **krājumu darbības ID** (`InventTransId`) vērtībām. Šīs vērtības vairs nav jāiekļauj, kad tiek izmantots datu elements. Tā vietā ir jāiekļauj pasūtījuma rindas numurs. Kopā pasūtījuma rindas numurs un pasūtījuma numurs ļauj identificēt katru no šīm atsauces vērtībām.

### <a name="voyage-line-quantity"></a>Reisa rindas daudzums

Tā kā reisa rinda ir tieši saistīta ar pasūtījuma rindu, **vērtībai Daudzums** (`ShipQty`), kas ievadīts, izmantojot elementu, ir nepieciešams, lai vērtības saskantu. Apstiprināšana tiek veikta attiecībā pret daudzumu pirkšanas pasūtījuma rindā vai pārsūtīšanas rindā. Ja apstiprināšana neizdodas, ieraksts netiks apstrādāts.

### <a name="calculated-fields"></a>Aprēķinātie lauki

Svara **un** tilpuma **aprēķinātie** lauki akceptē vērtības, kas tiek saņemtas, izmantojot datu elementu. Ja vērtības nav sniegtas, šo lauku atjaunināšanai tiek izmantotas sistēmas vērtības, ja ir pieejamas sistēmas vērtības. Zemes izmaksām vērtības tiek aprēķinātas šādi:

- *Svara* = *×* *bruto svars*
- *Tilpuma* = *×* (Krājuma bruto *dziļums* × *krājuma bruto augstums* × *krājuma bruto platums*)

## <a name="sequencing"></a>Secība

Atkarībā no tabulām, vispirms jāizveido reisa ieraksts. Reisa rindu var izveidot tikai pēc reisa, nosūtīšanas konteinera un rindu izveidošanas.

Lai izveidotu reisu bez pārbaudes brīdinājumiem, sistēmai ir jāapstrādā entītijas šādā secībā:

1. Reisi (`ITMTableEntity`)
1. Nosūtīšanas konteineri (`ITMContainersEntity`)
1. Maks. (`ITMFolioTableEntity`)
1. Reisa rindas (`ITMPurchaseLinesEntity` vai `ITMTransferLinesEntity`)
