---
title: Elektronisko parakstu apskats
description: "Šajā rakstā ir sniegts pārskats par elektroniskajiem parakstiem un ir aprakstīts, kā tos var izmantot programmatūrā Microsoft Dynamics 365 for Finance and Operations."
author: maertenm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SIGParameters, SIGProcSetup, SIGReasonCode
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13611
ms.assetid: 98dc6b79-1895-45d8-9dd1-2c8a351b58af
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 298ac47e2253f8add1aa3938dda15afe186afbeb
ms.openlocfilehash: 0cebd30a560ff033efab89c2055827b62cf31576
ms.contentlocale: lv-lv
ms.lasthandoff: 06/20/2017


---

# <a name="electronic-signature-overview"></a>Elektronisko parakstu apskats

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegts pārskats par elektroniskajiem parakstiem un ir aprakstīts, kā tos var izmantot programmatūrā Microsoft Dynamics 365 for Finance and Operations.

<a name="what-is-an-electronic-signature"></a>Kas ir elektronisks paraksts?
--------------------------------

Elektroniskais paraksts apstiprina personas identitāti, kas gatavojas sākt vai apstiprināt skaitļošanas procesu. Dažās nozarēs elektroniskais paraksts ir tikpat juridiski saistošs kā ar roku veikts paraksts. Vairākās regulētas nozarēs, piemēram, farmācijas, pārtikas un dzērienu un aviācijas un aizsardzības nozarēs, elektronisko parakstu izmantošana ir normatīva prasība. Tie ir arī nepieciešami, lai izpildītu ASV Pārtikas un zāļu pārvaldes (FDA) izdotā standarta 21 CFR 11. daļas normatīvās prasības. **Piezīme.** Elektroniskais paraksts pats par sevi nav tas pats kas ciparparaksts. Elektroniskais paraksts ir vienkārši ar roku rakstīta paraksta aizstājējs, bet ciparparaksts sniedz papildu drošības pasākumus. Ciparparaksts var palīdzēt identificēt, vai cits lietotājs vai process ir darbojies ar datiem. Ciparparakstu var arī verificēt, un šo verifikāciju nevar atspēkot datu parakstīšanai izmantotā sertifikāta īpašnieks. Kā tas ir aprakstīts tālāk, elektroniskajiem parakstiem programmatūrā Microsoft Dynamics 365 for Finance and Operations ir iebūvēta ciparparaksta funkcionalitāte.

## <a name="electronic-signatures-in-dynamics-365-for-finance-and-operations"></a>Elektroniskie paraksti programmatūrā Dynamics 365 for Finance and Operations
Programmatūrā Dynamics 365 for Finance and Operations varat izmantot elektroniskos parakstus īpaši svarīgiem biznesa procesiem. Dažiem procesiem ir iebūvētas elektronisko parakstu iespējas. Varat arī izveidot pielāgotas parakstu prasības jebkurai datu bāzes tabulai un laukam. Elektroniskajiem parakstiem ir iebūvēta ciparparaksta funkcionalitāte. Katram lietotājam, kas paraksta dokumentus, ir jāiegūst derīgs šifrēšanas sertifikāts. Kad dokuments ir parakstīts, tiek validēta ar šo sertifikātu saistītā privātā atslēga. Programmatūrā Dynamics 365 for Finance and Operations elektroniskā paraksta informācija tiek reģistrēta žurnālā, lai nodrošinātu auditācijas pierakstus. Lai iestatītu elektroniskos parakstus, skatiet rakstu [Iestatīt elektroniskos parakstus (uzdevuma ceļvedis)](http://ax.help.dynamics.com/en/wiki/set-up-electronic-signatures/).

## <a name="users-who-require-access-to-electronic-signatures"></a>Lietotāji, kuriem ir nepieciešama piekļuve elektroniskajiem parakstiem
Elektroniskajiem parakstiem drošības piekļuve parasti ir nepieciešama trīs veidu lietotājiem: elektronisko parakstu administratoriem, parakstītājiem un elektronisko parakstu auditoriem.

### <a name="electronic-signature-administrator"></a>Elektronisko parakstu administrators

Elektronisko parakstu administrators iestata parakstu prasības, vispārējos parametrus un apstiprinātājus, kā arī saņem brīdinājumus, kad parakstus neizdodas verificēt. Lietotājam, kuram ir piešķirta drošības loma **Informācijas tehnoloģiju vadītājs**, pēc noklusējuma ir atļauts administrēt elektroniskos parakstus.

### <a name="signer"></a>Parakstītājs

Parakstītājs sniedz elektroniskos parakstus dokumentiem un procesiem, kam ir nepieciešami paraksti. Lietotājam, kuram ir piešķirta drošības loma **Sistēmas lietotājs**, pēc noklusējuma ir atļauts elektroniski parakstīt dokumentus. **Piezīme.** Parakstītājam var būt nepieciešamas papildu atļaujas, pirms tiek nodrošināta piekļuve datiem, kas ir saistīti ar parakstāmo dokumentu vai procesu. Lietotājam, kas veic izmaiņas datos un kam pēc tam ir jāparakstās par šīm izmaiņām, ir nepieciešama atļauja mainīt šos datus. Lietotājam, kurš parakstās cita lietotāja vārdā, var nebūt nepieciešama piekļuve datiem. Šāda lietotāja piemērs ir supervizors, kas parakstās par darbinieka veiktajām izmaiņām.

### <a name="electronic-signature-auditor"></a>Elektronisko parakstu auditors

Elektronisko parakstu auditors pārskata datu bāzes žurnālu un parakstu pārskata žurnālu, kas ir pieejams no datu bāzes žurnāla. Lietotājam, kuram ir piešķirta drošības loma **Informācijas tehnoloģiju vadītājs**, pēc noklusējuma ir atļauts auditēt elektroniskos parakstus. Ja izmantojat citu lomu, nevis **Informācijas tehnoloģiju vadītā**, pārliecinieties, ka lomai ir piešķirtas tālāk norādītās privilēģijas.

-   Skatīt elektroniskā paraksta kļūmes
-   Skatīt datu bāzes žurnālu

## <a name="signing-documents-electronically"></a>Elektroniska dokumentu parakstīšana
### <a name="get-a-certificate"></a>Sertifikāta iegūšana

Pirms dokumentu elektroniskas parakstīšanas programmatūrā Dynamics 365 for Finance and Operations ir jāpieprasa sertifikāts. **Piezīme.** Sertifikātu izveidei un elektroniskās parakstīšanas iespējošanai programmatūrā Dynamics 365 for Finance and Operations tiek izmantoti Microsoft SQL Server līdzekļi. Nav nepieciešami nekādi papildu sertifikāti vai publisku atslēgu infrastruktūra (PKI). Kad pieprasāt sertifikātu, programmatūras Dynamics 365 for Finance and Operations datu bāzē jums tiek izveidota publiskā atslēga un privātā atslēga. Privātā atslēga ir šifrēta, izmantojot tikai jums zināmu paroli. Kad parakstāt dokumentu elektroniski, jūsu identitāti verificē, kad ievadāt paroli. Lai pieprasītu sertifikātu, lapas **Opcijas** cilnē **Konti** noklikšķiniet uz **Iegūt sertifikātu**. Jums ir jāievada un jāapstiprina parole, ko izmantosiet parakstīšanai. Šo paroli izmanto, lai aizsargātu jūsu privāto atslēgu un autorizētu jūsu sertifikāta lietošanu. Šī parole netiek glabāta datu bāzē un nav pieejama nevienam citam, tostarp Dynamics 365 for Finance and Operations administratoram. Ja aizmirstat ar savu sertifikātu saistīto paroli, šo sertifikātu ir nepieciešams atiestatīt. Ja atiestatāt šo sertifikātu, jūs neietekmējat ar iepriekšējo sertifikātu parakstītos dokumentus. Lai atiestatītu sertifikātu, lapā **Opcijas** noklikšķiniet uz **Atiestatīt sertifikātu**.

### <a name="sign-a-document-electronically"></a>Elektroniska dokumentu parakstīšana

Lapa **Parakstīt dokumentu** tiek parādīta, kad veicat izmaiņas, kurām nepieciešams elektroniskais paraksts.

1.  Lapā **Parakstīt dokumentu** noklikšķiniet uz cilnes **Dokuments**, lai pārskatītu dokumentā veiktās izmaiņas.
2.  Cilnē **Paraksts** atlasiet pamatojuma kodu.
3.  Ievadiet komentāru, ja ir nepieciešami kādi komentāri.
4.  Ja jūsu lietotāja ID netiek rādīts laukā **Parakstītājs**, tad atlasiet to sarakstā.
5.  Ievadiet savu atrašanās vietu, ja šāda informācija ir nepieciešama.
6.  Noklikšķiniet uz **OK**.

### <a name="sign-for-another-users-changes"></a>Parakstīties par cita lietotāja veiktām izmaiņām

Iespējams, reizēm jūs vēlaties, lai lietotājs parakstītos par cita lietotāja veiktajām izmaiņām. Piemēram, supervizoram varētu būt jāparakstās par izmaiņām, ko kāds darbinieks ir veicis materiālu komplektā (MK). Izmantojiet šo procedūru, lai norādītu Dynamics 365 for Finance and Operations lietotāju, kas parakstās par cita lietotāja veiktajām izmaiņām. **Piezīme.** Kad viens lietotājs parakstās par cita lietotāja veiktajām izmaiņām, paraksts ir jānodrošina izmaiņas veikušā lietotāja darbstacijā. Lietotājs nevar saglabāt izmaiņas, pirms ir sniegts paraksts. Lai norādītu apstiprinātājus, rīkojieties šādi.

1.  Lapas **Opcijas** cilnē **Konti** noklikšķiniet uz **Norādīt apstiprinātāju**.
2.  Laukā **Apstiprinātāja lietotāja ID** atlasiet tā lietotāja ID, kuram ir jāparakstās par cita lietotāja veiktajām izmaiņām.
3.  Laukā **Parakstīties par lietotāja ID** atlasiet tā lietotāja ID, par kura veiktajām izmaiņām ir jāparakstās.





