---
title: "Sadarbība ar kreditoriem, izmantojot kreditoru portālu"
description: "Šajā tēmā ir aprakstīts, kā iepirkuma aģenti var izmantot kreditoru portālu, lai sadarbotos ar ārējiem kreditoriem pirkšanas pasūtījumu apstiprināšanas procesa laikā. Šī informācija attiecas tikai uz 2016. februāra un 2016. gada maija Dynamics AX versijām."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: b4628977ec7a88a698f7b5af55ff049f7f76ecd6
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="collaborate-with-vendors-by-using-the-vendor-portal"></a>Sadarbība ar kreditoriem, izmantojot kreditoru portālu

[!include[banner](../includes/banner.md)]


Šajā tēmā ir aprakstīts, kā iepirkuma aģenti var izmantot kreditoru portālu, lai sadarbotos ar ārējiem kreditoriem pirkšanas pasūtījumu apstiprināšanas procesa laikā. Šī informācija attiecas tikai uz 2016. februāra un 2016. gada maija Dynamics AX versijām.

Šajā tēmā sniegtā informācija attiecas tikai uz 2016. februāra un 2016. gada maija Dynamics AX versijām. Dynamics 365 for Operations versijā 1611 kreditoru portāla funkcionalitāte ir aizstāta ar paplašināto kreditoru sadarbības funkcionalitāti. Papildinformāciju par jauno kreditoru sadarbības funkcionalitāti skatiet rakstā [Kreditoru sadarbības izmantošana darbam ar ārējiem kreditoriem](vendor-collaboration-work-external-vendors.md).  

Kreditoru portāls ir paredzēts kreditoriem, kuriem nav elektronisko datu savstarpējas apmaiņas (EDI) integrācijas ar programmu Microsoft Dynamics AX pirkšanas pasūtījumu (PP) informācijas apmaiņai. Portāls ļauj iepirkuma aģentiem nosūtīt PP kreditoram un pēc tam saņemt atbildi Akceptēts vai Noraidīts tieši programmā Dynamics AX.  

Procesu var konfigurēt tā, lai apstiprinājums no kreditora automātiski apstiprinātu pasūtījumu. Šajā gadījumā sekošana ir nepieciešama tikai laiku pa laikam, kad pasūtījums tiek noraidīts vai kad kreditora apstiprinājums tiek reģistrēts kā atbilde, bet PP statuss netiek atjaunināts uz **Akceptēts**, jo apstiprinājuma procesā radās problēma.

## <a name="po-confirmation-and-rejection"></a>PP akceptēšana un noraidīšana
PP tiek sagatavoti programmā Dynamics AX. Ja jums ir PP, kura statuss ir **Apstiprināts**, tas tiek nosūtīts kreditoram, ģenerējot apstiprinājuma pieprasījumu. Ja vēlaties pievērst kreditora uzmanību jaunam PP, var izmantot arī drukas pārvaldības sistēmu, lai nosūtītu PP pa e-pastu. PP parādās kreditoru portālā, un tajā ir ietverta opcija, kuru kreditors var izmantot, lai to apstiprinātu vai noraidītu. Kreditors var arī pievienot komentārus, lai darītu zināmu informāciju, piemēram, PO izmaiņas.  

Kreditoru portālā kreditors var redzēt pasūtījuma rindas. Šīs rindas ietver informāciju, piemēram, ārējo preces numuru, dimensijas, cenu informāciju, daudzumu, piegādes datumu un piegādes adresi. Kreditors var izveidot pārskatu, kurā attēlota PP informācija, kā arī kopējā cena. Maksas, kas attiecas uz kreditoru, tiek rādītas, ja kreditors noklikšķina uz pogas **Maksas** galvenē vai uz rindām. Kreditori var importēt PP informāciju savā sistēmā, izmantojot funkcionalitāti **Eksportēt programmā Excel**.  

Tālāk redzamajā tabulā ir parādīta tipiska informācijas apmaiņa atkarībā no tā, kā kreditors atbild, kad nosūtāt tām PP apstiprināšanai.

| Atbildes tips                                                                                                  | Rezultāts                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kreditors apstiprina pasūtījumu. Sistēma ir konfigurēta, lai automātiski apstiprinātu PP, kad kreditors veic apstiprinājumu.    | Pasūtījuma statuss tiek atjaunināts uz **Akceptēts**. Ja kaut kas liedz atjaunināt pasūtījumu, tad kreditora atbilde joprojām tiks ierakstīta kā **Akceptēts**, bet PP paliek statuss **Tiek pārskatīts ārēji**.                                                                       |
| Kreditors apstiprina pasūtījumu. Sistēma nav konfigurēta, lai automātiski apstiprinātu PP, kad kreditors veic apstiprinājumu. | Kreditora atbilde tiek ierakstīta kā **Akceptēts**, bet PP joprojām paliek statuss **Tiek pārskatīts ārēji**.                                                                                                                                                                                      |
| Kreditors noraida pasūtījumu.                                                                                     | Kreditora atbilde tiek ierakstīta kā **Noraidīts**, un PP joprojām paliek statuss **Tiek pārskatīts ārēji**. Noraidījums tiek saņemts kopā ar iemeslu un ierosinājumu par izmaiņām, piemēram, alternatīvu piegādes datumu. Jūs atjaunināt PP un pēc tam nosūtāt jaunu versiju apstiprināšanai. |

## <a name="changes-to-a-po"></a>Izmaiņas PP
Kad ir jāmaina PP, kas jau ir akceptēts, varat nosūtīt kreditoram jaunu PP caur kreditoru portālu. Jaunam PP būs versijas sufikss, lai norādītu, ka tā ir iepriekš nosūtīta PP mainīta versija. Kreditoru portāls ļauj kreditoriem izsekot katra pasūtījuma vēsturi. Iepriekš akceptēta PP versija paliks apstiprināto PP sarakstā līdz jaunā PP apstiprināšanai.  

Kad atceļat PP, tā statuss tiek mainīts atpakaļ uz **Apstiprināts**. Jums ir jāsūta PP atpakaļ kreditoram, izmantojot kreditoru portālu, lai tas varētu apstiprināt vai noraidīt atcelšanu. Pēc tam, kad atcelšana ir apstiprināta, PP parādās apstiprināto PP kreditora sarakstā kā **Atcelts**.

## <a name="versions-status-transitions-and-change-management"></a>Versijas, statusa pārejas un izmaiņu pārvaldība
Kad PP tiek nosūtīts kreditoram, tas tiek reģistrēts sistēmā kā specifiska PP versija un statuss mainās no **Apstiprināts** uz **Tiek pārskatīts ārēji**. Ja PP tiek mainīts vēlāk, tiek izveidota PP jauna versija, un statuss tiek mainīts atpakaļ uz **Apstiprināts** (vai **Melnraksts**, ja ir aktivizēta izmaiņu pārvaldība).  

Tālāk redzamajā tabulā ir parādīts statusa un versijas izmaiņu piemērs, kādas var notikt PP.

| Darbība                                                   | Statuss un versija                                                                                    |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| PP sākotnējā versija tiek izveidota programmā Dynamics AX. | Statuss ir **Apstiprināts**.                                                                           |
| PP tiek nosūtīts uz kreditoru portālu.                     | Versija tiek reģistrēta kreditoru portālā, un statuss tiek mainīts uz **Tiek pārskatīts ārēji**.    |
| Jūs veicat izmaiņas pēc kreditora pieprasījuma.  | Statuss tiek mainīts atpakaļ uz **Apstiprināts**.                                                            |
| Jūs nosūtāt PP jauno versiju uz kreditoru portālu. | Jaunā versija tiek reģistrēta kreditoru portālā, un statuss tiek mainīts uz **Tiek pārskatīts ārēji**. |
| Kreditors apstiprina PP jauno versiju.           | Statuss tiek mainīts uz **Akceptēts**.                                                                |

Lai apskatītu pirkšanas pasūtījumu versijas, kas ir nosūtītas kreditoram, un kreditora atbildes, pirkšanas pasūtījumā noklikšķiniet uz **Žurnāli** &gt; **Apstiprinājuma pieprasījumi**.  

Pasūtījumi, kuri nosūtīti kreditoram kā atbilde un kuriem ir statuss **Tiek pārskatīts ārēji**, parādīsies sarakstā **Pirkšanas pasūtījumi nosūtīti uz kreditoru portālu, tiek gaidīta atbilde** vai **Pirkšanas pasūtījumi nosūtīti uz kreditoru portālu, atbildēšanai ir nepieciešama darbība**. Ja maināt pasūtījumu, kas ir nosūtīts kreditoram, tā, ka statuss mainās atpakaļ uz **Apstiprināts**, tas vairs neparādās šajos sarakstos. Lai redzētu, vai no kreditora iepriekš ir saņemta atbilde uz pasūtījumu, noklikšķiniet uz **Žurnāli** &gt; **Apstiprinājuma pieprasījumi**.  

Kreditoriem nav jāapstiprina PP kreditoru portālā. Tie var arī nosūtīt e-pasta ziņojumu vai informēt par PP pieņemšanu, izmantojot citus kanālus. Pēc tam var apstiprināt pasūtījumu manuāli programmā Dynamics AX. Šajā gadījumā tiek saņemts brīdinājums, ka pasūtījums tiek akceptēts, pat tad, ja nav atbildes no kreditora. Pēc tam PP tiek parādīts apstiprināšanas vēsturē kreditoru portālā kā atvērts akceptēts pasūtījums, kuram nav atbilžu. Turklāt kreditoram vairs nav iespējas apstiprināt vai noraidīt PP.  

**Piezīme.** PO versija, kas ir pieejama citiem procesiem programmā Dynamics AX, vienmēr ir jaunākā versija, pat ja šī versija vēl nav reģistrēta.

### <a name="change-management"></a>Izmaiņu pārvaldība

Ja ir aktivizēta PP izmaiņu pārvaldība, tas iziet cauri apstiprināšanas darbplūsmai, lai sasniegtu statusu **Apstiprināts**. Šis process nav redzams kreditoram.  

Ja PP ir aktivizēta izmaiņu pārvaldība, versija tiek reģistrēta, kad PP tiek apstiprināts, nevis kad PP tiek nosūtīts kreditoram vai akceptēts.  

Tālāk redzamajā tabulā ir parādīts statusa un versijas izmaiņu piemērs, kādas var notikt PP, kad ir aktivizēta izmaiņu pārvaldība.

| Darbība                                                                                                        | Statuss un versija                                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PP sākotnējā versija tiek izveidota programmā Dynamics AX.                                                      | Statuss ir **Melnraksts**.                                                                                                                                                                                                                                                                                                                                                                    |
| PP tiek iesniegts apstiprināšanas procesam. (Tas ir iekšējs process, kurā kreditors nav iesaistīts.) | Statuss tiek mainīts no **Melnraksts** uz **Tiek pārskatīts** un uz **Apstiprinājums**, ja PP nav noraidīts apstiprināšanas procesa laikā. Apstiprināts PP tiek reģistrēts kā versija.                                                                                                                                                                                                                     |
| PP tiek nosūtīts uz kreditoru portālu                                                                           | Versija tiek reģistrēta kreditoru portālā, un statuss tiek mainīts uz **Tiek pārskatīts ārēji**.                                                                                                                                                                                                                                                                                        |
| Jūs veicat izmaiņas pēc kreditora pieprasījuma.                                                       | Statuss tiek mainīts atpakaļ uz **Melnraksts**.                                                                                                                                                                                                                                                                                                                                                    |
| PP tiek atkārtoti iesniegts apstiprināšanas procesam.                                                            | Statuss tiek mainīts no **Melnraksts** uz **Tiek pārskatīts** un uz **Apstiprinājums**, ja PP nav noraidīts apstiprināšanas procesa laikā. Vai arī sistēmu var konfigurēt, lai noteiktu lauku izmaiņām nebūtu nepieciešams atkārtots apstiprinājums. Šajā gadījumā statuss vispirms tiek mainīts uz **Melnraksts** un pēc tam tiek automātiski atjaunināts uz **Apstiprināts**. Apstiprinātais PP tiek reģistrēts kā jauna versija. |
| Jūs nosūtāt PP jauno versiju uz kreditoru portālu.                                                      | Jaunā versija tiek reģistrēta kreditoru portālā, un statuss tiek mainīts uz **Tiek pārskatīts ārēji**.                                                                                                                                                                                                                                                                                    |
| Kreditors apstiprina PP jauno versiju.                                                                | Statuss tiek mainīts uz **Akceptēts** automātiski vai saņemot atbildi no kreditora un pēc tam akceptējot PP.                                                                                                                                                                                                                                                     |
<a name="see-also"></a>Skatiet arī
--------

[Kreditoru sadarbības lietotāju drošības konfigurācija](configure-security-vendor-portal-users.md)

[Kreditora sadarbības rēķinu izveides darbvieta](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md)




