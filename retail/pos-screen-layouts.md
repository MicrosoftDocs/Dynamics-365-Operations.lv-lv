---
title: "Konfigurēt ekrāna izkārtojumu POS"
description: "Šajā tēmā ir sniegta informācija par ekrāna izkārtojumu par Microsoft Dynamics 365 operācijām - mazumtirdzniecības punktam sale (POS) pieredzi."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application user
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d49c5c9773047940e524c71e59a674ebe8460ad7
ms.lasthandoff: 03/31/2017


---

# <a name="configure-screen-layouts-for-pos"></a>Konfigurēt ekrāna izkārtojumu POS

Šajā tēmā ir sniegta informācija par ekrāna izkārtojumu par Microsoft Dynamics 365 operācijām - mazumtirdzniecības punktam sale (POS) pieredzi.

Microsoft Dynamics 365 operācijām - mazumtirdzniecības punktam sale (POS) lietotāja interfeisu var konfigurēt kombinējot vizuālo profilus un ekrāna izkārtojumu, piešķirti veikali, reģistrus un/vai lietotājiem.

## <a name="visual-profile"></a>Vizuālais profils
Vizuālo profili tiek piešķirti reģistros un tiek izmantotas, lai norādītu vizuālie elementi, kas ir specifisks reģistrs un dalītu pāri lietotājiem. Jebkuram lietotājam, kas piesakās reģistrā būs pašu dizainu, krāsas un attēli. **Profila numuru** -profilu skaits ir unikāls identifikators Visual profilu. **Aprakstu** -aprakstā var norādīt jēgpilnu nosaukumu, kas palīdzēs noteikt pareizo profilu jūsu situāciju. **Dizaina** -lietotāji var izvēlēties gaišs vai tumšs pieteikuma motīvus. Šie iestatījumi ietekmē visā app fontu un fona krāsas. **Izcēluma krāsa** -Izcēluma krāsa tiek izmantota visā POS diferencēt vai izcelt dažus vizuālos elementus, piemēram, flīzes, komandu pogas vai hipersaites. Šie elementi ir parasti ierosināt. **Galvenes krāsu** -galvenes krāsu ļauj lietotājam konfigurētu krāsu lappuses galveni, lai apmierinātu mazumtirgotāja zīmolu. Šis līdzeklis ir pieejams programmā Dynamics 365 darbību versija 1611 tikai. **Pieteikšanās fonus** -lietotāji var norādīt pieteikšanās ekrāna fona attēlu. Fona attēlu failu izmēri ir jātur tik mazam, cik iespējams, kā glabāšanai un ielādējot lielus failus var ietekmēt lietojumprogrammas darbību un izpildi. **Lietojumprogrammas fons** -POS var arī izmantot attēlu kā fona visā programmā vietā cieta dizaina krāsu. Kā ar pieteikšanās fonus, tiek ieteikts, lai saglabātu faila lielums tik nenozīmīga, cik vien iespējams.

## <a name="screen-layouts"></a>Ekrāna izkārtojumi
Ekrāna izkārtojums konfigurācija nosaka darbības, saturu un UI kontroli POS Welcome ekrāna un darījuma ekrāna izvietojumu. * Welcome ekrāna * *-vairumā gadījumu ir lapas, ko lietotāji redzēs, kad tie pirmo reizi ieiet POS ekrānā Esiet sveicināts!. Esiet sveicināts var sastāvēt no zīmola tēlu un pogu maģistrālajiem tīkliem, kas nodrošina piekļuvi POS operāciju. Darbības, kas nav specifiskas dotajai darbībai parasti tiek ievietoti šeit. **Darījuma ekrāna** -darījumu ekrāns ir galvenais ekrāns POS pārdošanas un pasūtījumu apstrādei. Darbība ekrānā var konfigurēt, izmantojot ekrāna izkārtojuma dizainers. **Noklusējuma sākuma ekrānu** -daži mazumtirgotāji izvēlas, ka kasieris naviģēt tieši uz ekrāna darbību pēc piesakoties. Noklusējuma sākuma ekrāna iestatījums ļauj lietotājiem iestatīt šo katra ekrāna izkārtojumam.

### <a name="assignment"></a>Piešķire

Ekrāna izkārtojumu var piešķirt veikalā, reģistrā vai lietotāja līmenī. Lietotāja uzdevuma ignorē reģistru un glabāt norīkojumu, un ignorē reģistra uzdevums veikalu nodošanu. Vienkāršs scenārijs, kur visi lietotāji izmanto tādu pašu izkārtojumu neatkarīgi no reģistra vai loma, ekrāna izkārtojumu var iestatīt tikai pie veikala. Gadījumos, ja noteiktu reģistros vai lietotāji pieprasa specializētā izkārtojumus, tos var piešķirt pienācīgi.

### <a name="layout-sizes"></a>Izkārtojumu lielumi

Šī iespēja attiecas tikai uz dinamiku 365 darbību versija 1611. Jo daudzos gadījumos ekrāna izkārtojumu var izmantot vairākos ekrāna izmērus un izšķirtspēju, katram lietotāji var konfigurēt to izkārtojumu un saturu. POS programma automātiski izvēlēties tuvāko izkārtojuma lieluma ierīces startēšanas laikā. Ekrāna izkārtojumu var būt arī pilns un kompaktās ierīces konfigurācijas. Šāda konfigurācija ļauj lietotājam piešķirt vienu ekrāna izkārtojumu, kas strādās dažādās izmēriem un formu faktoriem krātuvē. **Pilnu mūsdienu POS -** -pilnu izkārtojumu vislabāk parasti izmanto lielākas parāda kā datoru monitorus vai tabletes. Lietotāji var izvēlēties, kurus UI elementus iekļaut, noteikt to lielumu un izvietojumu un konfigurēt to detalizēti rekvizīti. Pilnu izkārtojumu atbalsta gan portretorientācijas, gan ainavorientācijas sastāvi. **Kompakts mūsdienu POS -** -Compact izkārtojumi parasti vislabāk izmantot telefonu vai nelielu tabletes. Dizaina iespējas ir ierobežotas, kompakts ierīcēm. Lietotāji var konfigurēt, kolonnu un lauku saņemšanas un kopsummas rūtīm.

### <a name="screen-layout-designer"></a>Ekrāna izkārtojuma dizainers

Katra izkārtojuma izmēra ekrāna izkārtojumu ir konfigurēta, izmantojot ekrāna izkārtojuma dizainers. Designer ļauj lietotājiem noteikt un konfigurēt lietotāja interfeisa elementus darījuma ekrāna. Ekrāna izkārtojums noformētājs lieto ClickOnce var lejupielādēt, instalēt un palaist programmas jaunāko versiju katru reizi, kad lietotājs tai piekļūst. Noteikti pārbaudiet pārlūkprogrammas prasības, izmantojot ClickOnce — dažās pārlūkprogrammās, piemēram, hroma, pieprasīt paplašinājumi. **Ciparu** -numura paliktnis ir galvenā lietotāja ievadi POS darījumu ekrānā. To var konfigurēt, lai parādītu visu ekrāna bloks, kas ir ideāli piemērots touchscreens, vai tikai ievades lauks, kas var tikt izmantoti ar fizisku tastatūru. Numuru spilventiņu iestatījumi programmā ir pieejami tikai pilnu izkārtojumu. Dynamics 365 darbību versija 1611, kompaktu izkārtojumu vienmēr ir pieejams no darījuma ekrāna pilnu ciparu tastatūru. **Kopsummu panelis** - kopsummas panelis var konfigurēt vai nu vienu vai divas kolonnas rādīt laukus, piemēram, līniju skaits, atlaides summu, izmaksas, subtotal un nodokļu. Programmā Dynamics 365 darbību versija 1611, kompaktu izkārtojumu atbalsta tikai vienu kopsummu kolonnā. **Apliecinājumu** -* * * * saņemšanas panelis satur pārdošanas rindās, maksājuma līnijas un piegādes informāciju par produktiem un pakalpojumiem, kas apstrādā, POS. Lietotāji var norādīt kolonnas platumu un izvietojumu. Kompakts izkārtojumus programmā Dynamics 365 darbību versija 1611, jūs varat arī konfigurēt papildu informāciju, kas parādīsies rindu zem galvenās līnijas. **Klienta kartes** - klientu kartes rāda informāciju, kas attiecas uz klientu šobrīd saistīts ar darījumu. Klienta kartes var konfigurēt, lai paslēptu vai parādītu papildu informāciju. **Cilnes vadīkla** - cilnes vadīklas var novietot uz ekrāna izkārtojumu un citas vadīklas, piemēram, ciparu tastatūru, klienta kartē vai pogas grids var ievietot iekšpusē tab. Cilnes vadīklas ir konteiners, kas palīdz lietotājiem ekrānā ietilpinātu vairāk satura. Ir pieejama pilna izkārtojumi tikai cilnes vadīklas. * Attēla * *-attēla vadīklu var izmantot, lai rādītu veikala logotipu vai citu zīmolu attēlu uz ekrāna darbību. Ir pieejama pilna izkārtojumi tikai attēla vadīklu. **Ieteicamie produkti** - ja konfigurēts vidi, Iesakam produkti kontroli parādīs produktu ieteikumus, pamatojoties uz mašīnu apmācības. Iesakam produkti kontroles pieejams tikai pilnu izkārtojumus programmā Dynamics 365 darbību versija 1611. * * Pielāgota vadīkla * *-pielāgota vadīkla darbojas, kā uz ekrāna izkārtojumā vietturi ļauj lietotājiem, lai rezervētu vietas pielāgots saturs. Pielāgoto vadīklu pieejams tikai pilnu izkārtojumu.

<a name="see-also"></a>Skatiet arī
--------

[Install the Retail POS Layout designer](install-pos-layout-designer.md)


