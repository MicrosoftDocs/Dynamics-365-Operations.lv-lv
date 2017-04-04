---
title: "Kreditoru sadarbība ar debitoriem"
description: "Šajā tēmā ir aprakstīts, kā varat izmantot kreditoru sadarbību programmā Dynamics 365 for Operations, lai strādātu ar pirkšanas pasūtījumiem un uzraudzītu sūtījuma krājumus."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ConsignmentProductReceiptLines, ConsignmentVendorPortalOnHand, PurchVendorPortalConfirmedOrders, PurchVendorPortalOriginalOrder, PurchVendorPortalResponsesHistoryList, PurchVendorPortalResponsesPart
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 221234
ms.assetid: 6e69fb8b-6d3a-46ef-88cf-6d01212aa7c3
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 11cd2242b5a575ae87b0dbcf6f8ce268fcea5377
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-collaboration-with-customers"></a>Kreditoru sadarbība ar debitoriem

Šajā tēmā ir aprakstīts, kā varat izmantot kreditoru sadarbību programmā Dynamics 365 for Operations, lai strādātu ar pirkšanas pasūtījumiem un uzraudzītu sūtījuma krājumus.

Šajā tēmā ir aprakstīts, kā varat izmantot kreditoru sadarbību, lai strādātu ar debitoriem programmā Microsoft Dynamics 365 for Operations. Tas ietver informāciju par to, kā uzraudzīt un reaģēt uz pirkšanas pasūtījumu, un kā kontrolēt sūtījuma krājumu. Ir iespējams arī izmantot piegādātāju sadarbība darbā ar rēķiniem. Lai iegūtu papildinformāciju, skatiet [piegādātāja sadarbības rēķina izrakstīšanas darbvietu](/dynamics365/operations/financials/accounts-payable/vendor-portal-invoicing-workspace).

## <a name="working-with-purchase-orders"></a>Darbs ar pirkšanas pasūtījumiem
Darbvieta **Pirkšanas pasūtījuma akceptēšana** jums ļauj atbildēt uz pirkšanas pasūtījumiem, kas jums ir nosūtīti pārskatīšanai. Tā jums ļauj skatīt arī informāciju par pirkšanas pasūtījumiem, kas gaida rīcību no debitora, un pirkšanas pasūtījumiem, kas ir akceptēti, bet joprojām ir atvērti. Darbvietā **Pirkšanas pasūtījuma akceptēšana** pastāv trīs tālāk aprakstītie saraksti.

-   **Pirkšanas pasūtījumiem, kas izskatīšanai** -šajā sarakstā ir redzami POs, kas ir nosūtīts uz jums un gaida atbildi no jums. Pēc tam, kad esat atbildējis, PO pazūd no saraksta. Ja debitors jums nosūta jaunu pirkšanas pasūtījuma versiju, pirms esat atbildējis uz iepriekšējo, tiek rādīta tikai jaunākā versija.
-   **Tiek gaidīta debitora darbība** — šis saraksts jums ļauj redzēt pirkšanas pasūtījumus, uz kuriem esat atbildējis, bet kurus debitors vēl nav akceptējis. Ja esat pieņēmis pirkšanas pasūtījumu, varat to uzraudzīt šajā sarakstā, līdz tā statuss mainās uz **Akceptēts**. Ja pirkšanas pasūtījumu noraidījāt vai pieņēmāt to ar izmaiņām, tad šeit šo pirkšanas pasūtījumu varat uzraudzīt, līdz debitors sūta jaunu versiju.
-   **Atvērtie akceptētie pirkšanas pasūtījumi** — šajā sarakstā ir visi pirkšanas pasūtījumi jūsu kontam, kuru statuss ir **Akceptēts**. Kad preces vai pakalpojumi ir pilnīgi saņemti pret pirkšanas pasūtījumu, šis pirkšanas pasūtījums pazūd no saraksta.

Nākamajā sarakstā ir parādīts četras lapas, kuras varat izmantot darbam ar pirkšanas pasūtījumiem; divas no tām ietver tādu pašu informāciju kā saraksti darbvietā.

-   **Pārskatāmie pirkšanas pasūtījumi** (skatiet iepriekš)
-   **Pirkšanas pasūtījuma kreditora akceptēšanas vēsture** — šajā lapā ir visi pirkšanas pasūtījumi un visas pirkšanas pasūtījumu versijas, kas ir nosūtītas kreditoram, kā arī visas kreditora sniegtās atbildes.
-   **Atvērtie akceptētie pirkšanas pasūtījumi** (skatiet iepriekš)
-   **Visi akceptētie pirkšanas pasūtījumi** — šajā lapā ir visi pirkšanas pasūtījumi, kas ir akceptēti, tostarp tādi, kuriem ir saņemtas preces vai pakalpojumi. Šo sarakstu varat izmantot, lai uzraudzītu, kuriem pirkšanas pasūtījumiem varat sūtīt rēķinus.

### <a name="responding-to-purchase-orders"></a>Atbildēšana uz pirkšanas pasūtījumiem

Pirkšanas pasūtījumus, kas klientam ir nosūtījis jums izskatīšanai ir redzamas **iepirkuma pasūtījuma apstiprinājums** darbvietu un **pirkšanas pasūtījumu pārskatīšanai** lapā. Kad esat atvēris PO, var to akceptēt, noraidīt vai pieņemt to ar izmaiņām. Pirkšanas pasūtījuma virsrakstā vai atsevišķās rindās var būt pielikumi. Tāpat arī jūs varat pievienot informāciju savai atbildei šī pirkšanas pasūtījuma virsrakstā vai atsevišķās rindās. Piemēram, varat ierosināt aizstāšanas krājumu kādai no rindām. Pirkšanas pasūtījumu varat priekšskatīt un izdrukāt kā PDF failu, izmantojot opciju **Priekšskatīt/Drukāt**. Izmantojot darbību **Parādīt dimensijas**, varat paslēpt vai parādīt šādas dimensiju kolonnas: Vieta, Noliktava, Krāsa, Lielums, Stils, Konfigurācija. Ja jūs lietojat **akceptēt izmaiņas** variants, var akceptēt vai noraidīt atsevišķas rindas. Izmaiņas var veikt arī šādas rindas:

-   Mainīt datumus vai daudzumus. Ja vēlaties atjaunināt akceptēto piegādes datumu visās rindās, izmantojiet opciju **Atjaunināt piegādes datumu** pirkšanas pasūtījuma virsrakstā.
-   Sadalīt rindas dažādiem piegādes datumiem vai daudzumiem
-   Aizstājiet kādu krājumu. Lai to izdarītu, ievadiet krājuma aprakstu un savu krājuma numuru laukā **Ārējais** sadaļā **Detalizēta rindas informācija**.

Jūs nevarat mainīt izcenojuma informāciju vai maksas, bet varat sniegt ierosinājumus par to izmaiņām, izmantojot piezīmes. Ja debitors jums nosūta jaunu pirkšanas pasūtījuma versiju, tai būs versijas sufikss, lai norādītu, ka tā ir iepriekš nosūtīta PP mainīta versija. Lapā **Pirkšanas pasūtījuma kreditora akceptēšanas vēsture** jūs varat izsekot katra pasūtījuma vēsturei.

## <a name="monitoring-consignment-inventory"></a>Sūtījuma krājumu uzraudzīšana
Ja izmantojat sūtījuma krājumus, tad varat izmantot kreditoru sadarbības interfeisu, lai skatītu informāciju tālāk norādītajās lapās.

-   **Pirkšanas pasūtījumus, kas patērē sūtījuma krājumu** -sūtījuma krājumu pirkšanas pasūtījumiem tiek ģenerēti, kad klients uzņemas atbildību par inventāra. Šie sūtījuma pirkšanas pasūtījumi tiek rādīti tikai lapā **Pirkšanas pasūtījumi, kuros tiek patērēti sūtījuma krājumi**. Tie nav iekļauti lapā **Visi akceptētie pirkšanas pasūtījumi**.
-   **No sūtījuma krājumiem saņemtās preces** — šajā lapā ir uzskaitītas visas transakcijas, kur preces īpašumtiesības tiek nodotas uzņēmumam, kurš šo krājumu patērē. Varat izmantot šo informāciju, lai debitoram izrakstītu rēķinu.
-   **Rīcībā esošie sūtījuma krājumi** — šajā lapā tiek rādīti rīcībā esošie sūtījuma krājumi, kas pieder jūsu uzņēmumam un kas ir rīcībā esoši debitora noliktavā.


<a name="see-also"></a>Skatiet arī
--------

[Pārvaldīt kreditoru sadarbības lietotājus](manage-vendor-collaboration-users.md)


