---
title: Store Commerce programmas iespējas
description: Šajā rakstā ir aprakstīta funkcija, kas ir pieejama programmā Store Commerce Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2022-09-30
ms.openlocfilehash: d713cc0e9537ae20ffddee6e77779a16e74bd779
ms.sourcegitcommit: eb9a53d5cf10f1ada68757536d6a94b2cb00929d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/27/2022
ms.locfileid: "9728029"
---
# <a name="store-commerce-app-capabilities"></a>Store Commerce programmas iespējas

[!include [banner](includes/banner.md)]

Store Commerce programma ir modernā pārdošanas punkta (POS) pieredze Microsoft Dynamics 365 Commerce. Tas ļauj uzņēmumiem apstrādāt veikala darbības un pārvaldīt uzskaites biroja darbības, piemēram, krājumu un pasūtījumu procesēšanu. Šī programma arī iespējo uzņēmumus pārvaldīt debitoru attiecības ar lojalitāti un klientu aktivizēšanu. 

Commerce Scale Unit (CSU) rīcībā ir programma Store Commerce, kas nodrošina pilnīgu uzņēmuma kanāla risinājumu. Piemēram, debitors var iegādāties preci tiešsaistē un saņemt to tuvējā veikalā, tādējādi turpinot iepirkties kanālos, nezaudējot nekādus datus. 

Šajā rakstā ir sniegts pārskats par Store Commerce programmas iespējām.

## <a name="platform"></a>Platforma

| Iespēja | Apraksts | Dokumentācija | Papildu saturs |
|---|---|---|---|
| Kanāla kanāla nos. | Dynamics 365 Commerce sniedz vispārēju risinājumu, kas vienkāršo biroja darbu, veikalu, zvanu centru un digitālu pieredzi. | [Pārskats](index.md) | [Tech ar](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/dynamics-365-commerce-overview-november-2-2020) |
| Bezgalvas Commerce | Commerce Scale Unit vieso bez vājā uzņēmuma programmu. Bezslodzes komercijas programma darbojas kā centrālā vieta visām commerce biznesa loģikas vajadzībām un darbojas kā pilnīgs bankas kanāla risinājums. | <p>[Arhitektūras apskats](commerce-architecture.md)</p><p>[Bez vāja arhitektūra](dev-itpro/retail-server-architecture.md)</p> | [Tech ar](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-commerce-architecture-overview-december-4-2020) |
| Commerce Headquarters | Commerce Headquarters nodrošina atpakaļejoša biroja iespējas, kas iespējo produktu, darbinieku, biznesa procesu, cenu un citu biznesa vajadzībām nepieciešamo funkcionalitāti konfigurāciju. | [Arhitektūras apskats](commerce-architecture.md) | |
| Pārdošanas punkts (POS) | Programma Store Commerce ir POS pieredze Dynamics 365 Commerce. Tas nodrošina līdzekļu bagātus un vispusīgus POS iespējas, kas palīdz ar pārdošanu asociētajiem, kasieri un pārvaldnieki nodrošina klientu apkalpošanas vadītājus. Turklāt tā nodrošina vairākas izvietošanas opcijas mazumtirgotājiem, palīdz uzlabot veiktspēju un piedāvā uzlabotu programmas dzīves cikla pārvaldību (PASTĀV). | [Store Commerce programma](dev-itpro/store-commerce.md) | <p>[Tech ar](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/modernize-the-dynamics-365-commerce-in-store-technology-using-the-new-store-commerce-app-march-30-2022)</p><p>[Video](https://youtu.be/7B332XH_zfs)</p><p>[Migrācija no MPOS uz Store Commerce](dev-itpro/pos-extension/migrate-mpos-store-commerce.md)</p> |
| Mākoņa izvietošana | Noslodzes sadalei un ģeogrāfiskā tuvumam var izvietot vairākas Commerce Scale Units instances. | [Mākoņa izvietošana](../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md) | |
| Lokālie izvietošanas dokumenti | Izmantojot lokālu biznesa datu izvietošanu, Komercijas debitoriem var būt lielākas īpašumtiesības un Dynamics 365 vides pārvaldība. | [Lokāls izvietojums](../fin-ops-core/dev-itpro/deployment/deploy-retail-onprem.md) | |

## <a name="device-management"></a>Ierīces pārvaldība

| Iespēja | Apraksts | Dokumentācija | Papildu saturs |
|---|---|---|---|
| Vairāki formu faktori | Programmu Store Commerce atbalsta vairāki ierīces formas faktori, piemēram, datori, planšetdatori un mobilās ierīces. Konta lietotāja interfeiss (Ui) ļauj izkārtojumu automātiski samazināt un pielāgot ekrāna izmēram. | [Vizuālās konfigurācijas](pos-screen-layouts.md) | |
| Starpplatformu | Veikala Commerce programma tiek atbalstīta tīmeklī, Windows, iOS un Android platformās. | [Platformas](dev-itpro/hybridapp.md) | |
| Zīmolrade | Ekrāna veidotājs ļauj pielāgot ekrāna izkārtojumus savām biznesa vajadzībām. Turklāt tēmas, izkārtojumus, krāsas un attēlus var veidot, ņemot vērā darbinieku lomas, un pēc tam tos var koplietot starp lietotājiem, lai nodrošinātu zīmola konsekvenci un vienkāršotu lietošanu. | [Vizuālās konfigurācijas](pos-screen-layouts.md) | [Video](https://www.youtube.com/watch?v=ldqCw2wf5fY) |
| Topoloģija | Tiek atbalstītas dažādas veikala topoloģijas, pamatojoties uz tīkla pieejamību. | <p>[Topoloģija](dev-itpro/retail-modern-pos-architecture.md)</p><p>[Infografika](dev-itpro/retail-in-store-topology.md)</p> | |
| Vairāku ierīču pārvaldība | Programmā Commerce Headquarters vairākas ierīces veikalos var viegli pārvaldīt. | [Aktivizēšana](set-up-activation-accounts-validate-devices-hq.md) | [Tech ar](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/commerce-mass-deployment-with-sccm-system-center-configuration-manager-october-6-2022) |

## <a name="employee-management"></a>Darbinieku pārvaldība

| Iespēja | Apraksts | Dokumentācija | Papildu saturs |
|---|---|---|---|
| Pierakstīšanās | Katram veikala darbiniekam var būt atvēlēta pierakstīšanās. Pierakstīšanās veidi ietver lietotāja vārdu, svītrkodu, magnētiskās joslas lasītāju (MSR), biometrijas rādītājus un Azure Active Directory (Azure AD). | <p>[Azure AD](aad-pos-logon.md)</p><p>[Paplašinātā pieteikšanās](extended-logon.md)</p> | |
| Tiesības | Darbiniekiem tiek atbalstīti dažādi tiesību līmeņi, piemēram, tiesības izveidot pasūtījumus un tiesības rediģēt pasūtījumus. | [Tiesības](tasks/create-pos-permission-groups.md) | |
| Laika un apmeklētības pārvaldība | Klātbūtne var tikt pārvaldīta, izmantojot darba laika uzskaites funkciju. Klātbūtnes datus var apstrādāt algā, izmantojot Dynamics 365 Human Resources programmu. | [Laika pārvaldība](retail-time-attendance.md) | |
| Pārdošanas komisija | Pārdošanu var izsekot tirdzniecības pārstāvis, lai aprēķinātu komisijas vai citus veicināšanas pasākumus. | [Komisija](pos-sales-groups-track-commissions.md) | |

## <a name="merchandising"></a>Virzīšana tirgū

| Iespēja | Apraksts | Dokumentācija | Papildu saturs |
|---|---|---|---|
| Preču klāsta pārvaldība | Preču pārvaldnieks var sašķirot preces tā, lai tās būtu pieejamas pārdošanai noteiktā kanālā un noteiktā periodā. | [Preču klāsts](assortments.md) | |
| Katalogi | Preču pārvaldnieks var pārvaldīt katalogus, lai identificētu preces, ko vēlaties piedāvāt ar katalogam specifisku cenu noteikšanu. | [Katalogi](/dynamicsax-2012/appuser-itpro/about-retail-product-catalogs) | |
| Preču un kategoriju pārvaldība | Programmā Commerce Headquarters preču pārvaldnieks var izveidot preces, kurām ir varianti, atribūti, mērvienība utt. Tās var arī definēt kategoriju hierarhiju, lai organizētu preces. | [Produkts](retail-hierarchies.md) | |
| Komplekti | Preču pārvaldnieks var grupēt preces tā, lai tās pārdotu kā saišķi vai komplektu. | [Komplekti](/dynamicsax-2012/appuser-itpro/about-setting-up-retail-product-kits) | |
| Informācijas kodi | Izmantojiet informācijas kodus, lai kasierim pieprasītu ievadīt informāciju dažādās POS darbībās, piemēram, preču pārdošana, preču atgriešana vai debitora atlase. | [Informācijas kodi](/dynamicsax-2012/appuser-itpro/about-info-codes-retail) | |
| Saistītie krājumi | Izmantojiet saistītās preces, lai papildu preces grāmatotu, kad krājums tiek pievienots darbībai. | [Saistītie krājumi](/dynamicsax-2012/appuser-itpro/set-up-products-for-cross-selling-and-up-selling) | |
| Garantijas | Paplašinātās garantijas var pārdot kopā ar precēm. | [Garantija](extended-warranty.md) | |
| Etiķešu drukāšana | Var ģenerēt etiķetes, kurās ir informācija par preci, piemēram, partijas numurs, sērijas numurs un derīguma beigu datums. | [Etiķešu drukāšana](/dynamicsax-2012/appuser-itpro/create-and-print-labels-overview) | |

## <a name="assisted-selling"></a>Jūsu pārdošana

| Iespēja | Apraksts | Dokumentācija | Papildu saturs |
|---|---|---|---|
| Preču pārlūkošana | Pārlūkot preces pēc kategorijas. | [Preču hierarhija](retail-hierarchies.md) | |
| Preču meklēšana | Meklēt preces pēc nosaukuma un precizēt meklēšanu, izmantojot preču īpašības, piemēram, zīmolu, cenu un materiālu. Šī iespēja ir uzģenerīga, izmantojot Azure cotive meklēšanu. | [Mākoņa datora meklēšana](cloud-powered-search-overview.md) | |
| Lapa Informācija par preci | Bagātinātās preces informācijas lapas var ietvert attēlus, aprakstu, preču īpašības un rekomendētās preces. Rekomendācijas sniedz Rekomendāciju pakalpojums. | | |
| Preču salīdzināšana | Salīdziniet vairākas preces un palīdziet debitoriem izvēlēties vienu no precēm un pievienot tās darbībai. | | |
| Uzmācības aile | Viegli uzmeklē krājumus citos veikalos un izveido pasūtījumus. | [Krājumu pārlūkošana](pos-inventory-lookup-operation.md) | [Tech ar](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Ieteikumi | Upsell un šķērspārdot preces, izmantojot Rekomendāciju pakalpojumu. Šis pakalpojums izmanto patentētu tehnoloģiju, lai ieteiktu ieteikumus, balstoties uz pirkšanas tendencēm un tādiem raksturlielumiem kā nesen saņemts, līdzīgs izskats un vislabākā cena. Šie ieteikumi ir pieejami preču informācijas lapās, **Debitora informācijas** lapā un **Darbību** lapā. | [Ieteikumi](product-recommendations.md) | [Tech ar](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-recommendations-march-2-2021) |

## <a name="customer-relationship"></a>Attiecības ar debitoriem

| Iespēja | Apraksts | Dokumentācija | Papildu saturs |
|---|---|---|---|
| Debitoru pārvaldība | Izveidojiet, labojiet un pārvaldiet debitoru kontus. Debitoru kontus var pārvaldīt asinhronā režīmā, lai izvairītos no reāllaika apstrādes. | [Pārvaldības](customer-mgmt-stores.md) | |
| Debitora atribūti | Debitora atribūtu struktūra iespējo papildus ar debitoru saistītos datus, kas ir tverti atbilstoši biznesa prasībām. | [Atribūti](dev-itpro/customer-attributes.md) | |
| Lapa ar detalizētu informāciju par debitoru | Bagātinātās debitora informācijas lapa sniedz debitora saziņas kanāla kanāla skatu visos kanālos. Šīs mijiedarbības ietver pirkumus, vēlmju sarakstus un lojalitātes programmas punktus. | | |
| Mākoņa darbināta debitora meklēšana | Meklēt debitorus pēc vārda, tālruņa numura, e-pasta adreses, lojalitātes programmas kartes, adreses utt. | [Mākoņa datora meklēšana](pos-search-improvements.md#customer-search) | |
| Lojalitāte un atlīdzības | Debitori var pievienoties lojalitātes programmām un saņemt un izpirkt lojalitātes programmas punktus pa kanāliem. | [Lojalitāte](set-up-customer-loyalty-program.md) | |
| Attiecības ar klientiem | Pārvaldiet galvenos debitorus, izmantojot klienta grāmatu, un atsejiet aktivitātes un piezīmes debitora profilā. Dynamics 365 Customer Insights integrācija ļauj veikala darbiniekiem saņemt norādījumus par nākamo labāko darbību katram debitoram. | [Attiecības ar klientiem](clienteling-overview.md#activities-and-notes) | |

## <a name="pricing-and-discounts"></a>Cenu noteikšana un atlaides

| Iespēja | Apraksts | Dokumentācija | Papildu saturs |
|---|---|---|---|
| Tirdzniecības līgumi | Cenu noteikšanas vadītāji var izmantot tirdzniecības līgumus, lai noteiktu īpašas cenas, pamatojoties uz ilgtermiņa darījumiem noteiktiem debitoriem. | [Cenu noteikšana](price-management.md)| [Video](https://www.youtube.com/watch?v=r2VD8IxHesM) |
| Pārdošanas līgumi | Cenu noteikšanas vadītāji var izmantot pārdošanas līgumus, lai definētu uz līgumu balstītas cenas "bizness-biznesam" (B2B) komercijas scenārijos. | [Cenu noteikšana](price-management.md) | |
| Cenas korekcijas | Cenu noteikšanas vadītāji var izmantot cenu korekcijas iespēju, lai izveidotu, izsekotu un pārvaldītu cenu nocenojumus saviem produktiem laika gaitā. | [Cenas korekcijas](price-adjustments-discounts.md) | |
| Atlaides | Cenu noteikšanas vadītāji var iestatīt vairākus atlaižu veidus, lai darbinātu dažādus veicināšanas pasākumu veidus. Šīs atlaides ietver vienkāršas atlaides, daudzuma atlaides, sliekšņa atlaides, komplekta atlaides, uz norēķiniem balstītas atlaides un piegādes atlaides. | [Atlaides](retail-discounts-overview.md) | |
| Kuponi | Cenu noteikšanas vadītāji var iestatīt kuponu kodus vai svītrkodus, piesaistīt tos atlaidēm un izplatīt tos debitoriem. Ar pārdošanu saistīts var pievienot kuponus pārdošanas darbībām vai noņemt tos. | [Kuponi](coupons.md) | |
| Cenu grupas | Cenu noteikšanas vadītāji var izmantot cenu grupas spēju definēt kontekstuālas cenas, pamatojoties uz kanāliem, katalogiem, piederībām vai lojalitātes programmām. | [Cenu noteikšana](price-management.md) | |
| Pieejamie veicināšanas pasākumi | Ar pārdošanu saistīts var viegli atrast pieejamas veicināšanas pasākumi precēm veikalā, precēm, kas ir pievienotas darbībai, utt. | [Cenu noteikšanas funkcijas](pos-pricing-functions.md) | |
| Cenu pārbaudes | Izmantojot pārdošanas piesaistes, veikalā var ātri pārbaudīt aktīvās preču pārdošanas cenas. | [Cenu noteikšanas funkcijas](pos-pricing-functions.md) | |
| Cenu ignorēšana | Pārdošana saista, kuriem ir nepieciešamās atļaujas, var ignorēt sistēmā konfigurētas vai aprēķinātas cenas. | [Cenu noteikšanas funkcijas](pos-pricing-functions.md) | |
| Manuālas atlaides | Pārdošana saista, kuriem ir nepieciešamās atļaujas, var piemērot manuālas atlaides pārdošanas darbībai vai pārdošanas rindām. | [Cenu noteikšanas funkcijas](pos-pricing-functions.md) | |

## <a name="electronic-payments"></a>Elektroniskie maksājumi

| Iespēja | Apraksts | Dokumentācija | Papildu saturs |
|---|---|---|---|
| Kredīts un debets | Store Commerce programma atbalsta galvenos kredītkaršu un debetkaršu maksājumus, izmantojot A pirkšanas vārteju un pasūtījuma izpildi, izmantojot PayPal. Sdk Maksājumi sniedz iespēju izmantot ārējās vārtejas savienojumus, ko atbalsta neatkarīgs programmatūras izstrādātāja (ISV) integrācija. | <p>[Adyen](dev-itpro/adyen-connector.md?tabs=10-0-23)</p><p>[Paypal](paypal.md)</p><p>[Maksājumi](payment-methods.md)</p> | <p>[Tech ar](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-omni-channel-payment-configuration-february-9-2021)</p><p>[Tech ar](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-omni-channel-payment-overview-processing-february-4-2021)</p> |
| Ciparparaksta atbalsts | Programma Store Commerce atbalsta maksājumus, izmantojot ciparu maks. maksājuma metodes, kas neizmanto bankas identifikācijas numura (BIN) diapazonus kā tradicionālas kredītkartes un debetkartes. Maksāšanas metodes var kartēt uz ciparu maksājumus, piemēram, Amacen. | [Maka](wallets.md) | |
| Dāvanu kartes atbalsts | Bankas identifikācijas numurs Dynamics 365 dāvanu karte, uzglabātās vērtības risinājumi (SVS) un dāvanu kartes Givex. Dāvanu kartes var nopirkt un izpirkt pasūtījumā. | [Dāvanu kartes](dev-itpro/gift-card.md) | [Tech ar](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/d365-commerce-internal-gift-cards-november-16-2021) |
| Aizsardzība pret krāpniecību | Dynamics 365 Fraud Protection palīdz jums novērst krāpnieciskas darbības un noteikt vietas, kur konstatēt pārkāpumus, var nebūt. | [Aizsardzība pret krāpniecību](dev-itpro/dfp.md) | [Video](https://www.youtube.com/watch?v=j_1nEiq3LfM) |

## <a name="taxes-and-charges"></a>Nodokļi un maksas

| Iespēja | Apraksts | Dokumentācija | Papildu saturs |
|---|---|---|---|
| Nodokļi | Programma Store Commerce atbalsta daudzu veidu netiešos nodokļus, piemēram, PVN, pievienotās vērtības nodokli (PVN), preču un pakalpojumu nodokli (GST), vienības maksas un ieturēto nodokli. | [Nodokļi](/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json) | |
| Maksas | Maksas var konfigurēt rindu līmenī virsraksta līmenī, kā automātiskās maksas, pa kanāliem utt. | [Izmaksas](omni-auto-charges.md) | |

## <a name="order-processing-and-fulfillment"></a>Pasūtījuma apstrāde un izpilde

| Iespēja | Apraksts | Dokumentācija | Papildu saturs |
|---|---|---|---|
| Pasūtījuma izveide | Pasūtījumu var izveidot nosūtīšanai vai savākšanai tuvējā veikalā. Laika slotus var nodrošināt savākšanai. | [Pārskats](customer-orders-overview.md) | |
| Pasūtījuma modificēšana | Pasūtījumu var modificēt, atgriezt, atcelt u.tt. | <p>[Atcelt](customer-orders-overview.md#cancel-a-customer-order)</p><p>[Atgriešanas](pos-returns.md)</p> | |
| Meklēšana pasūtījumos | Meklējiet un filtrējiet pasūtījumus, izmantojot pasūtījumam raksturīgo informāciju. | [Meklēšana pasūtījumos](enhancedorderrecall.md) | |
| Pasūtījumu atribūti | Pasūtījuma atribūtu struktūra iespējo papildu ar pasūtījumu saistīto informāciju tveršanu, ņemot vērā biznesa prasības. | [Atribūti](dev-itpro/order-attributes.md) | |
| Tiešā piegāde | Kreditora tiešā piegādei debitora adresē var atzīmēt krājumus. Tiešo piegādi sauc arī par tiešo piegādi. | [Tiešā piegāde](/dynamics365/supply-chain/sales-marketing/tasks/ship-orders-direct-deliveries) | |
| Piedāvājums | Veikala darbinieki var izveidot piedāvājumus debitoriem un var norādīt īpašu cenu, manuālas atlaides un piedāvājuma derīguma datumu. | [Piedāvājums](/dynamics365/supply-chain/sales-marketing/tasks/create-edit-sales-quotations) | |
| Piegāde | Veikali var izdot, iepakot un nosūtīt pasūtījumus. Pavadzīmi var pievienot pakām, kas ir gatavas nosūtīšanai. | [Piegāde](order-fulfillment-overview.md) | [Tech ar](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-supporting-buy-online-pickup-in-store-curbside-with-dynamics-365-commerce-pos-february-3-2021) |
| Sadalīto pasūtījumu pārvaldība | Programma Store Commerce atbalsta daudzu pasūtījumu izpildes optimizāciju, kur biznesa stratēģijas var konfigurēt, ņemot vērā uzņēmējdarbības veidu, debitora veidu, pasūtījuma izcelsmi un pasūtījuma piegādes metodi. | [Dom](dom.md) | |

## <a name="inventory-management"></a>Krājumu vadība

| Iespēja | Apraksts | Dokumentācija | Papildu saturs |
|---|---|---|---|
| Sagādes sadale | Racionalizējiet pieejamo krājumu sadali no sadales centra uz vairākiem veikaliem vai noliktavām. | [Sagādes sadale](tasks/set-up-rules-parameters-cross-docking-buyers-push.md) | [Tech ar](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Pārkraušana sadales centrā | Racionalizējiet krājumu sadali ienākošajiem pirkšanas pasūtījumiem uz vairākiem veikaliem vai noliktavām. | [Pārkraušana sadales centrā](tasks/set-up-rules-parameters-cross-docking-buyers-push.md) | [Tech ar](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Ienākošie krājumi | Saņemt krājumu no kreditora, izmantojot pirkšanas pasūtījumu, vai no citas noliktavas, izmantojot pārsūtīšanas pasūtījumu. Izveidojiet ienākošā pirkšanas pasūtījuma vai pārsūtīšanas pasūtījuma pieprasījumu. | [Saņemšana](pos-inbound-inventory-operation.md) | [Tech ar](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Izejošie krājumi | Nosūtīt krājumus uz citu noliktavu, izmantojot pārsūtīšanas pasūtījumu, un izveidot nosūtīšanas pārsūtīšanas pasūtījuma pieprasījumu. | [Nosūtīšana](pos-outbound-inventory-operation.md) | [Tech ar](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Krājumu pārlūkošana | Pārbaudiet rīcībā esošos krājumus precēm veikalos un noliktavās un pārbaudiet rīcībā esošos (ATP) krājumus turpmākajos datumos. | [Krājumu pārlūkošana](pos-inventory-lookup-operation.md) | [Tech ar](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Krājumu korekcija | Pielāgojiet krājumus veikala noliktavā vai ārā no tās, lai atbilstu noteiktām biznesa prasībām, neizmantojot pārdošanu, saņemšanu vai atkārtotu uzskaiti. | [Krājumu korekcija](work-with-store-inventory.md) | [Tech ar](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Krājumu uzskaite | Saskaitiet fiziskos krājumus un pielāgojiet sistēmas grāmatvedības krājumus, lai tos saskaņotu. | [Uzskaite](work-with-store-inventory.md) | [Tech ar](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Krājumu pārvietošana | Pārvietot krājumus starp vietām veikalā. | [Kustība](work-with-store-inventory.md) | [Tech ar](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |

## <a name="financials"></a>Finanšu dati

| Iespēja | Apraksts | Dokumentācija | Papildu saturs |
|---|---|---|---|
| Kases pārvaldība | Programma Store Commerce atbalsta skaidras naudas un citu noteiktu veikala norēķinu pārvaldību. Turklāt maiņu saskaņošanu veikalā var iespējot papildu kases pārvaldības iespējām. | [Kase](cash-mgmt.md) | |
| Finanšu pārskati un saskaņošana | Veikala skaidras naudas un darbību darbības tiek ierakstītas programmā Commerce Headquarters, izmantojot izrakstu grāmatošanas procesus. | [Izraksti](retail-statements.md) | |
| Ieņēmumu un izdevumu darbības | Apstrādājiet kases darbības veikalā un ierakstiet ienākumus, kas nav tradicionāli, piemēram, zaudēto un atrasto naudu, kas ir ieņēmumu daļa no coffee shop jūsu veikalos, un veikala tīrīšanas pakalpojumus. | [Izraksti](retail-statements.md) | |
| Rēķinu maksājumi | Notvert maksājumus pret rēķiniem. | [Rēķins](payinvoice.md) | |

## <a name="employee-productivity"></a>Darbinieka produktivitāte

| Iespēja | Apraksts | Dokumentācija | Papildu saturs |
|---|---|---|---|
| Uzdevumu pārvaldība | Izveidojiet uzdevumu sarakstus un uzdevumus un piešķiriet tos veikaliem un darbiniekiem. Izsekojiet uzdevumu statusu veikalos. Ir nodrošināta viengabala Microsoft Teams integrācija. | <p>[Uzdevumu pārvaldība](task-mgmt-overview.md)</p><p>[Microsoft Teams](commerce-teams-integration.md)</p> | [Video](https://www.youtube.com/watch?v=ES1whB4C2lU) |

## <a name="hardware-and-peripherals"></a>Aparatūra un perifērijas ierīces

| Iespēja | Apraksts | Dokumentācija | Papildu saturs |
|---|---|---|---|
| Perifērijas ierīču savienošana | Pievienojiet ar POS termināli tādas perifērijas ierīces kā printeri, kases aparātus, skenerus un maksājumu ierīces. | [Perifērās ierīces](retail-peripherals-overview.md) ||
| Kopīgot perifērijas ierīces | Kvīšu printerus, kases aparātus un maksājumu ierīces var koplietot daudzos termināļos, izveidojot to savienojumu ar koplietojamu aparatūras staciju. | <p>[Aparatūras stacija](retail-peripherals-overview.md) ||
| POS un perifērijas simulators | Perifērijas simulators atbalsta scenāriju pārbaudi, kuriem parasti ir nepieciešamas fiziskas POS perifērijas ierīces. Tajā ir ietverts arī POS simulators, ko var izmantot fizisko perifērijas ierīču saderības pārbaudei, neprasot POS klienta izvietošanu. | [Simulators](dev-itpro/retail-peripheral-simulator.md) | |

## <a name="receipts"></a>Ieejas plūsma

| Iespēja | Apraksts | Dokumentācija | Papildu saturs |
|---|---|---|---|
| Drukāt kvītis | Dažādu tipu kvītis, piemēram, pārdošanas kvītis, kredītkaršu kvītis, dāvanu kvītis un rēķinus, pēc noklusējuma var izdrukāt vai pēc kasiera apstiprinājuma izrakstīšanas laikā. Tos var arī atkārtoti izdrukāt no žurnāla. | [Drukāšana](receipt-templates-printing.md) | |
| Kvīšu nosūtīšana pa e-pastu | Kvītis var nosūtīt pa e-pastu no POS pēc tam, kad ir pabeigta pārbaude. | [E-pasts](email-receipts.md) | |
| Dizaina kvītis | Veikala ieejas plūsmas var pielāgot, lai tām tiktu rādīti dati un izkārtojumi, kas atbilst mazumtirgotājam un darījuma veidam. Ieejas plūsmas var arī paplašināt, lai tiktu rādīti pielāgotie dati, ko pieprasa mazumtirgotājs. | [Dizains](receipt-templates-printing.md) | |

## <a name="offline-support"></a>Bezsaistes atbalsts

| Iespēja | Apraksts | Dokumentācija | Papildu saturs |
|---|---|---|---|
| Vienoti bezsaistē | Bezsaistē bezsaistē varat turpināt darboties pat tad, ja interneta savienojamība ir ierobežota vai nav pieejama. Datu izslēgšana palīdz samazināt bezsaistes datu bāzu datu lielumu un maksimizēt veiktspēju. | [Bezsaistē](pos-operations.md) | |
| Pārslēgšanās, kas balstīta uz veiktspēju | Pārslēdziet uz bezsaisti, kad ir konstatēta veiktspējas veiktspēja. | [Bezsaistē](dev-itpro/implementation-considerations-offline.md) | [Video](https://youtu.be/sQU-2pgHToI) |
| Bezsaistes panelis | Bezsaistes **statusa** informācijas panelis rāda bezsaistes statusu, kļūdas un detalizētu informāciju par katras ierīces datiem. Tāpēc daudzu ierīču statusu ir viegli pārvaldīt. | [Bezsaistē](dev-itpro/implementation-considerations-offline.md) | [Video](https://youtu.be/sQU-2pgHToI)|

## <a name="extensibility"></a>Paplašināmība

| Iespēja | Apraksts | Dokumentācija | Papildu saturs |
|---|---|---|---|
| Commerce Headquarters | Commerce Headquarters risinājumus var pielāgot, pievienojot vai modificējot biznesa procesus. Commerce Headquarters atbalsta metadatu un kodam orientētu paplašinājuma modeli izmantošanu, lai pievienotu pielāgotu funkcionalitāti. To var viegli integrēt ārējos risinājumos. | [Pārskats](dev-itpro/extend-customer-cdx-package.md) | [Tech ar](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-unlock-the-power-of-dynamics-365-commerce-commerce-extensibility-overview-february-23-2021) |
| Bez headless commerce | Paplašināmo Channel API struktūru var izmantot, lai pielāgotu un pievienotu biznesa loģiku. API, kuriem ir pieprasījumu apstrādātāji, kā arī iepriekšēja trigera un pēcslēgera paplašinājuma raksti. | [Csu](dev-itpro/retail-server-customer-consumer-api.md) | [Tech ar](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |
| Commerce SDK | Commerce SDK ietver koda, koda paraugus, veidnes un rīkus, kas nepieciešami funkcionalitātes paplašināšanai vai pielāgošanai Dynamics 365 Commerce. SDK tiek publicēts dažādos repozitojos (repos) GitHub, atkarībā no paplašinājuma komponentiem. | [Sdk](dev-itpro/retail-sdk/sdk-github.md) | [Tech ar](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |
| Pārdošanas punkts | Store Commerce programmu var paplašināt neatkarīgi, izmantojot Commerce SDK POS paplašinājuma funkciju. Struktūra atbalsta lietotāja pieredzes (UX), darbplūsmu un biznesa loģikas pielāgošanu. | [Pos](dev-itpro/pos-extension/pos-extension-overview.md) | [Tech ar](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |

## <a name="reporting"></a>Pārskatu veidošana

| Iespēja | Apraksts | Dokumentācija | Papildu saturs |
|---|---|---|---|
| Pārdošanas pārskats | Veikala vadītājiem ir pieejami pārdošanas pārskati par darbiniekiem, kases sistēmu, maksājuma tipu, atgriešanu, preci utt. Vadītāji var apskatīt šos pārskatus un izmantot tos, lai iedalītu komisiju un identificētu preču tendences. | | |

## <a name="diagnostics"></a>Diagnostika

| Iespēja | Apraksts | Dokumentācija | Papildu saturs |
|---|---|---|---|
| Operāciju ieskati | Veikala curated pakalpojuma drošības un veiktspējas rādītāji ir pieejami debitora abonementā Application Insights. Ir pieejamas uzlabotās brīdinājumu un pārraudzīšanas iespējas. | | |
| Darbspējas pārbaude | Ar POS pievienoto perifērijas ierīču pieejamību var pārbaudīt, veicot veselības pārbaudes darbību. Pēc tam atsevišķas perifērijas problēmas var fiksēt un pārbaudīt. | [Darbspējas pārbaude](pos-healthcheck.md) | [Video](https://www.youtube.com/watch?v=RfPDNmnqYvY) |

## <a name="globalization"></a>Globalizācija

| Iespēja | Apraksts | Dokumentācija | Papildu saturs |
|---|---|---|---|
| Vairāku tirgu atbalsts | No kastes tiek atbalstītas tirgus raksturīgās funkcijas, piemēram, fiskālā integrācija, GST, uzlabotā rēķinu izrakstīšana un priekšapmaksas. Šī iespēja aptver vairākus tirgus Eiropā, Eiropā, Krievijā, Āzijā, Saūda Arābija utt. | [Globalizācija](localizations/fiscal-integration-for-retail-channel.md) | |

## <a name="compliance"></a>Atbilstība

| Iespēja | Apraksts | Dokumentācija | Papildu saturs |
|---|---|---|---|
| Microsoft standarti | Programma Store Commerce atbilst Microsoft drošības, konfidencialitātes, pieejamības, Vispārīgo datu aizsardzības noteikumu (GDPR), Eiropas Savienības (ES) datu robežas standartiem. | | |

