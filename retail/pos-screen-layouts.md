---
title: "POS ekrāna izkārtojumu konfigurēšana"
description: "Šajā tēmā ir sniegta informācija par Microsoft Dynamics 365 for Operations —Retail pārdošanas punkta (POS) ekrāna izkārtojumu."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application user
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: efded720c40feb8a4541b52b40b88c377e32594e
ms.contentlocale: lv-lv
ms.lasthandoff: 04/26/2017


---

# <a name="configure-screen-layouts-for-pos"></a>POS ekrāna izkārtojumu konfigurēšana

[!include[banner](includes/banner.md)]


Šajā tēmā ir sniegta informācija par Microsoft Dynamics 365 for Operations —Retail pārdošanas punkta (POS) ekrāna izkārtojumu.

Microsoft Dynamics 365 for Operations — Retail pārdošanas punkta (POS) lietotāja interfeisu var konfigurēt, izmantojot gan vizuālos profilus, gan ekrāna izkārtojumus, kas ir piešķirti veikaliem, kases sistēmām un/vai lietotājiem.

## <a name="visual-profile"></a>Vizuālais profils
Vizuālie profili tiek piešķirti kases sistēmām un tiek izmantoti, lai norādītu vizuālos elementus, kas ir raksturīgas konkrētai kases sistēmai un tiek lietoti visiem lietotājiem. Jebkuram lietotājam, kurš piesakās kases sistēmā, tiek rādīts viena un tas pats dizains, krāsa un attēli. 

**Profila numurs** — profila numurs ir vizuālā profila unikālais identifikators. 

**Apraksts** — apraksts sniedz iespēju norādīt jēgpilnu nosaukumu, kas palīdzēs noteikt konkrētajai situācijai piemērotāko profilu.

**Dizains** — lietotāji var izvēlēties dizainu Gaišs vai Tumšs. Šie iestatījumi ietekmē fontu un fona krāsu visā programmā.

**Izcēluma krāsa** — izcēluma krāsa tiek izmantota visā POS interfeisā, lai izceltu vai iezīmētu noteiktus vizuālos elementus, piemēram elementus, komandpogas vai hipersaites. Parasti šos elementus var izmantot, lai veiktu kādu darbību.

**Virsraksta krāsa** — virsraksta krāsa sniedz lietotājam iespēju konfigurēt lapas virsraksta krāsu atbilstoši mazumtirgotāja zīmolrades vajadzībām. Šis līdzeklis ir pieejams tikai Dynamics 365 for Operations versijā 1611.

**Pieteikšanās foni** — lietotāji var norādīt pieteikšanās ekrāna fona attēlu. Fona attēla faila lielumam ir jābūt pēc iespējas mazākam, jo lielu failu uzglabāšana un ielāde var ietekmēt lietojumprogrammas darbību un veiktspēju.

**Lietojumprogrammas fons** — POS lietojumprogrammas tīrtoņa fona krāsas vietā visā lietojumprogrammā var izmantot arī attēlu. Līdzīgi kā pietiekšanās fonam, arī šī faila lielumam ir jābūt pēc iespējas mazākam.

## <a name="screen-layouts"></a>Ekrāna izkārtojumi
Izmantojot ekrāna izkārtojuma konfigurācijas, tiek noteiktas darbības, saturs un UI vadīklu novietojums POS sveiciena ekrānā un transakciju ekrānā. 

**Sveiciena ekrāns** — vairumā gadījumu sveiciena ekrāns ir lapa, kas tiek parādīta lietotājiem, kad viņi pirmo reizi piesakās POS. Sveiciena ekrānā var būt ietverts zīmolrades attēls un pogu režģi, kas nodrošina piekļuvi POS operācijām. Parasti šeit ir pieejamas operācijas, kas nav raksturīgas pašreizējai transakcijai. 

**Transakciju ekrāns** — transakciju ekrāns ir galvenais POS ekrāns, kas ir paredzēts pārdošanas transakciju un pasūtījumu apstrādei. Transakciju ekrānu var konfigurēt, izmantojot ekrāna izkārtojuma dizaineru. 

**Noklusējuma sākuma ekrāns** — daži mazumtirgotāji vēlas, lai kasieri uzreiz pēc pieteikšanās tiktu novirzīti uz transakciju ekrānu. Noklusējuma sākuma ekrāna iestatījumi sniedz lietotājiem iespēju iestatīt šo opciju katram ekrāna izkārtojumam.

### <a name="assignment"></a>Piešķire

Ekrāna izkārtojumus var piešķirt veikala, kases sistēmas vai lietotāja līmenī. Lietotāja piešķirei ir augstāka prioritāte nekā kases sistēmas un veikala piešķirei, un kases sistēmas piešķirei ir augstāka prioritāte nekā veikala piešķirei. Vienkāršā scenārijā, kad visi lietotāji izmanto vienu izkārtojumu neatkarīgi no kases sistēmas vai lomas, ekrāna izkārtojumu var iestatīt tikai veikalam. Gadījumos, ja noteiktām kases sistēmām vai lietotājiem ir nepieciešami īpaši izkārtojumi, tos var atbilstoši piešķirt.

### <a name="layout-sizes"></a>Izkārtojumu lielumi

Šis līdzeklis attiecas tikai uz Dynamics 365 for Operations versiju 1611. Tā kā daudzos gadījumos ekrāna izkārtojumus var lietot ar dažādiem ekrāna izmēriem un izšķirtspējām, lietotāji var konfigurēt savu izkārtojumu un saturu katrai ierīcei. Startēšanas laikā POS lietojumprogrammā tiek automātiski izvēlēts ierīcei piemērotākais izkārtojuma izmērs. Ekrāna izkārtojumā var ietvert arī pilna un kompakta izkārtojuma ierīces konfigurācijas. Šī konfigurācija sniedz iespēju lietotāju piešķirt vienam ekrāna izkārtojumam, kas darbojas dažādu izmēru un formas ekrānos, kas tiek lietoti veikalā. 

**Modern POS — pilns** — pilnos izkārtojumus parasti ir vislabāk piemēroti lielākiem displejiem, piemēram, personālo datoru monitoriem vai planšetdatoriem. Lietotāji var izvēlēties ietveramos UI elementus, noteikt to lielumu un novietojumu un konfigurēt to detalizētos rekvizītus. Pilnie izkārtojumi atbalsta gan portreta, gan ainavorientācijas konfigurācijas. 

**Modern POS — kompakts** — kompaktie izkārtojumi parasti ir vislabāk piemēroti tālruņiem vai maziem planšetdatoriem. Kompaktā izkārtojuma ierīcēm ir ierobežotas izstrādes iespējas. Lietotāji var konfigurēt saņemšanas un kopsummu rūts kolonnas un laukus.

### <a name="screen-layout-designer"></a>Ekrāna izkārtojuma dizainers

Katrs ekrāna izkārtojumā ietvertais izkārtojuma lielums ir jākonfigurē, izmantojot ekrāna izkārtojuma dizaineru. Dizainers sniedz lietotājiem iespēju norādīt un konfigurēt transakciju ekrāna UI elementus. Ekrāna izkārtojuma dizainerā tiek izmantots līdzeklis ClickOnce, lai lejupielādētu, instalētu un palaistu jaunāko lietojumprogrammas versiju ikreiz, kad lietotājs tam piekļūst. Noteikti pārbaudiet pārlūkprogrammas prasības attiecībā uz ClickOnce lietošanu — dažās pārlūkprogrammās, piemēram, Chrome, ir nepieciešami paplašinājumi. 

**Ciparu tastatūra** — ciparu tastatūra ir galvenais lietotāja ievades līdzeklis informācijas ievadīšanai POS transakciju ekrānā. To var konfigurēt tā, lai tiktu rādīta visa ekrāna tastatūra, kas ir lieliski piemērots risinājums skārienekrāniem, vai tikai ievades laiks, ko var izmantot kopā ar fizisku tastatūru. Ciparu tastatūras iestatījumi ir pieejami tikai pilnajā izkārtojumā. Dynamics 365 for Operations versijas 1611 kompaktajos izkārtojumos transakciju ekrānā vienmēr ir pieejama pilnā ciparu tastatūra.

**Kopsummu panelis** — kopsummu paneli var konfigurēt ar vienu vai divām kolonnām, lai tiktu parādīti tādi lauki kā rindu skaits, atlaides summa, izmaksas, apakšsumma un nodokļi. Dynamics 365 for Operations versijas 1611 kompaktajos izkārtojumos tiek atbalstīta tikai viena kopsummu kolonna. 

**Ieejas plūsma** — ieejas plūsmas panelī ir ietvertas pārdošanas rindas, maksājuma rindas un piegādes informācija par precēm un pakalpojumiem, kas tiek apstrādāti POS. Lietotāji var norādīt kolonnas, platumu un novietojumu. Dynamics 365 for Operations versijas 1611 kompaktajos izkārtojumos varat konfigurēt arī papildu informāciju, kas tiks rādīta rindā zem galvenās rindas. 

**Debitora karte** — debitora kartē tiek rādīta informācija par debitoru, kas pašlaik ir saistīts ar transakciju. Debitora karti var konfigurēt papildinformācijas slēpšanai vai parādīšanai. 

**Ciļņu vadīkla** — ciļņu vadīklu var ievietot ekrāna izkārtojumā, un cilnē var ievietot citas vadīklas, piemēram, ciparu tastatūru, debitora karti vai pogu režģus. Ciļņu vadīkla ir konteiners, kas palīdz lietotājiem ievietot ekrānā vairāk satura. Ciļņu vadīkla ir pieejama tikai pilnajos izkārtojumos. 

**Attēls** — attēla vadīklu var izmantot, lai transakcijas ekrānā parādītu veikala logotipu vai citu zīmolrades attēlu. Attēla vadīkla ir pieejama tikai pilnajos izkārtojumos. 

**Ieteiktās preces** — ja videi ir konfigurēta ieteikto preču vadīkla, tā nodrošina preču ieteikumu rādīšanu, pamatojoties uz algoritmisko mācīšanos. Ieteikto preču vadīkla ir pieejam tikai Dynamics 365 for Operations versijas 1611 pilnajos izkārtojumos. **Pielāgota kontrole** — pielāgotā vadīkla darbojas kā vietturis ekrāna izkārtojumā, lai sniegtu lietotājiem iespēju rezervēt vietu pielāgotam saturam. Pielāgotā vadīkla ir pieejama tikai pilnajos izkārtojumos.

<a name="see-also"></a>Skatiet arī
--------

[Retail POS izkārtojuma dizainera instalēšana](install-pos-layout-designer.md)




