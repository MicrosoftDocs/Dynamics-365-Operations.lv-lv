---
title: Indijas No kopējo ienākumu summas atskaitītā nodokļa (TDS) pārskats
description: Šajā tēmā sniegta detalizēta informācija par Indijas No kopējo ienākumu summas atskaitīto nodokli (TDS). TDS dokumentācija sedz šīs iespējas funkcionalitāti.
author: kailiang
ms.date: 03/19/2021
ms.topic: overview
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "15721"
- intro-internal
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: d33faaff8be4821005b8772875eb91f0afe26cb0
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2022
ms.locfileid: "7983907"
---
# <a name="indian-tax-deducted-at-source-tds-overview"></a>Indijas No kopējo ienākumu summas atskaitītā nodokļa (TDS) pārskats

[!include [banner](../includes/banner.md)]

Šajā tēmā sniegta detalizēta informācija par Indijas No kopējo ienākumu summas atskaitīto nodokli (TDS).

TDS dokumentācija sedz šīs iespējas funkcionalitāti. Tajā skaidrots arī, kā veikt pamata iestatījumus TDS, aprēķināt TDS darījumos, pabeigt TDS norēķinu procesu, reģistrēt TDS sertifikātu numurus un ģenerēt TDS pieprasījumus, TDS pārskatus un TDS sertifikātus. Šajā dokumentācijā ir iekļautas šādas tēmas:

- [TDS pamata iestatījumi](apac-ind-TDS-TDS-ledger-accounts-setup.md)
- [TDS aprēķinam izmantotā formulas veidotāja un sliekšņa ierobežojuma funkcionalitāte](apac-ind-TDS-Formula-designer.md)
- [TDS aprēķināšana rēķinos, maksājumos, parādzīmēs un starpuzņēmumu darījumos](apac-ind-TDS-Calculate-TDS-on-invoices-using-journals.md)
- [Periodisks TDS norēķinu process un TDS summu nosegšana TDS iestādes kreditoriem](apac-ind-TDS-Run-the-periodic-TDS-settlement-process.md)
- [TDS sertifikātu numuru un datumu ierakstīšana un atjaunināšana](apac-ind-TDS-Record-TDS-concession-certificate-numbers.md)

## <a name="introduction-to-tds"></a>Ievads TDS

Saskaņā ar 1961. gada ienākumu nodokļa aktu ieturēto nodokli atskaita pakalpojumu saņēmējs avansa maksājuma vai kredīta uzskaites laikā atkarībā no tā, kas notiek vispirms. Personai, kas veic maksājumu, jāatskaita nodokļa summa, un pakalpojuma sniedzējam jāsamaksā tikai neto bilance. TDS tiek lietots pakalpojumiem, kurus norāda valdība, un nodoklis tiek atskaitīts, izmantojot likmes, ko valdība norāda periodam. Ieturējumu likme ir balstīta uz entītijas statusu, kas saņem maksājumu vai nodrošina pakalpojumu. Statusi ietver **Individuālu**, **Nedalītu ģimeni** (**HUF**), **Uzņēmumu**, **Firmu**, **Personu asociāciju** (**AOP**), **Personu grupu** (**BOI**) un **Vietējo pašvaldību**.

Šajās sadaļās norādīti pakalpojumi, kam tiek pielietots TDS, kā to ir norādījusi Indijas valdība.

**Iedzīvotāji**

- Ienākumi no algām (saskaņā ar 192. sadaļu)
- Ienākumi no vērtspapīru procentiem (atbilstoši 193. sadaļai)
- Ienākumi no dividendēm (saskaņā ar 194. sadaļu)
- Ienākumi no procentiem (saskaņā ar 194.A sadaļu)
- Ienākumi no loteriju vai mīklām (saskaņā ar 194.B sadaļu)
- Uzvara no zirgu skriešanas sacensībām (saskaņā ar 194.BB sadaļu)
- Darbuzņēmēji un apakšuzņēmumi (saskaņā ar 194.C sadaļu)
- Apdrošināšanas komisija (saskaņā ar 194.D sadaļu)
- Ienākumi no noguldījumiem saskaņā ar valsts taupības shēmu (saskaņā ar 194.EE sadaļu)
- Ienākumi no kopfonda vai UTI (saskaņā ar 194.F sadaļu)
- Komisija, atlīdzība, balva utt., par pārdošanu vai loteriju (saskaņā ar 194.G sadaļu)
- Komisijas vai starpnieka maksājums (saskaņā ar 194.H sadaļu)
- Noma (saskaņā ar 194.I sadaļu)
- Profesionālais pakalpojums (saskaņā ar 194.J sadaļu)
- Ienākumi no vienībām (saskaņā ar 194.K sadaļu)
- Kompensācijas izmaksa par noteikta nekustamā īpašuma iegādi (saskaņā ar 194.LA sadaļu)

**Nerezidenti**

- Maksājumi nerezidentu sporta veidiem vai sporta asociācijām (saskaņā ar 194.E sadaļu)
- Citas summas (saskaņā ar 195. sadaļu)
- Ienākumi attiecībā uz nerezidentu vienībām (saskaņā ar 196.A sadaļu)

    - Ienākumi no ārvalstu valūtas parādzīmēm vai Indijas uzņēmuma daļām (saskaņā ar 196.C sadaļu)
    - Ārvalstu investoru ienākumi no vērtspapīriem (saskaņā ar 196.D sadaļu)
    - Alga un visi citi pozitīvie ienākumi, kas nav saistīti ar ienākumiem (192. sadaļa)
    - Vērtspapīru procenti (193. sadaļa)
    - Procenti, kas nav procenti no vērtspapīriem (194.A sadaļa)
    - Maksājumi līgumslēdzējiem un apakšuzņēmumi (194.C sadaļa)
    - Laimesti no loterijas vai krustvārdu mīklām (194.B sadaļa)
    - Uzvaras no zirgu skriešanas sacensībām (194.BB sadaļa)
    - Apdrošināšanas komisija, kas sedz visus maksājumus par apdrošināšanas uzņēmumu (194.D sadaļa)
    - Visi procenti, izņemot procentus par vērtspapīriem, kas tiek maksāti nerezidentiem, kas nav uzņēmums vai ārvalstu uzņēmums (195. sadaļa)
    - Maksājums nerezidentam sportistiem, tostarp sporta asociācijai vai institūcijai. Nerezidenta sportista gadījumā maksājumi par reklāmām, kā arī raksti par jebkuru spēli/sportu Indijā laikrakstos, žurnālos utt. ir iekļauti (194.E sadaļa)
    - Maksājums attiecībā uz depozītiem saskaņā ar NSS \[Valsts uzkrājumu shēmu\] (194.EE sadaļa)
    - Maksājums saskaņā ar savstarpējo fondu vai UTI veikto vienību atpirkšanu (194.F sadaļa)
    - Komisijas vai starpnieka maksājums (194.H sadaļa)
    - Īres maksājums (194.I sadaļa)
    - Maksa par profesionāliem vai tehniskiem pakalpojumiem (194.J sadaļa)
    - Komisija tirdzniecības uzņēmumiem, izplatītājiem, pircējiem un loterijas biļešu pārdevējiem, ieskaitot atlīdzību vai laimestu par šādām biļetēm (194.G sadaļa)
    - Ieņēmumi no ārvalstu valūtā iegādātajām vienībām vai ilgtermiņa kapitāla ieguvumiem, ko rada tādu vienību nodošana, kas iegādātas ārzemju valūtā (196.B sadaļa)
    - Visu ienākumu izmaksāšana nerezidentiem attiecībā uz procentiem vai dividendēm par obligācijām un akcijām (196.C sadaļa)

TDS tiek aprēķināts pirkšanas, pārdošanas, pārdošanas ieņēmumiem, kredīta notām, pamatlīdzekļu iegādei, priekšapmaksai, avansa maksājumiem, parādzīmēm, būvdarbu nodokļiem un starpuzņēmumu darījumiem.

> [!NOTE]
> Pašreizējā Indijas nodokļa scenārijā TDS netiek aprēķināts pārdošanas darījumiem. Tomēr sistēma ietver uzkrājumu, lai aprēķinātu TDS, kas atgūstami pārdošanas darījumos, jo īpaši starpuzņēmumu darījumos.

TDS aprēķinā vienmēr ņem vērā TDS komponentam noteikto slieksni un izņēmuma slieksni.

Periodisko TDS norēķinu process ir jāpalaiž, un TDS maksājumi ir jānokārto TDS iestādes kreditoriem.

No piegādātājiem vai debitoriem saņemto TDS sertifikātu numurus un datumus var reģistrēt un atjaunināt. Turklāt veidlapu 26Q un 27Q ceturkšņa pārskatos var ģenerēt veidlapas 16A sertifikātu TDS, kas var tikt ģenerēts sadaļā Finanses.

## <a name="setting-up-and-working-with-tds"></a>TDS iestatīšana un darbs ar to

Šeit sniegts pārskats par TDS iestatīšanu un darbu ar to.

1. **TDS iestatīšana:**

    - Parametru iestatīšana:

        - Virsgrāmatas parametros aktivizējiet ar TDS saistītos parametrus.
        - Virsgrāmatas parametros iestatiet numuru sēriju ieturētā nodokļa maksājumiem.
        - Iestatiet parametrus sadaļās Kreditori un Debitori.

    - Pamata iestatīšana:

        - Iestatiet TDS reģistrācijas numurus uzņēmumam, debitoriem un kreditoriem.
        - TDS komponentu grupu iestatīšana.
        - Iestatiet TDS komponentus, pievienojiet tiem TDS sastāvdaļu grupas un nosakiet to slieksni un izņēmuma slieksni.
        - Iestatiet TDS iestādes.
        - Iestatīt TDS norēķinu periodus.
        - Iestatiet TDS nodokļu kodus un pievienojiet tiem TDS komponentus.
        - Iestatiet TDS nodokļu grupas un pievienojiet tiem TDS nodokļu kodus.
        - Formulas veidotājā definējiet aprēķināmo TDS nodokļa grupai.
        - Ierakstīt TDS koncesijas sertifikātu numurus.

    - Virsgrāmatas konti un uzņēmuma iestatījumi:

        - Iestatiet TDS kreditoru un debitoru virsgrāmatas kontus.
        - Iestatiet uzņēmumam nodokļu atskaitīšanas un iekasēšanas konta numuru (TAN) un atskaitītāja veida kategoriju.

    - Citi iestatījumi:

        - Iestatiet maksājumu grafiku, kas ietver TDS sadalījumu.
        - Iestatiet maksājumu nodevas tipu maksājumiem TDS iestādei.
        - Iestatiet informāciju par TDS grupām, pastāvīgajiem kontu numuriem (PAN) un kreditoru un debitoru TAN.

2. **TDS aprēķina darījumos:**

    - Rēķini un maksājumi
    - Parādzīmes
    - Avansa maksājumi
    - Priekšapmaksas

3. **TDS norēķini:**

    - Periodisko TDS norēķinu process
    - TDS maksājumu norēķini TDS iestādes kreditoriem un TDS challan izveide

4. **TDS uzziņas, pārskati un sertifikāts:**

    - Ierakstīt un atjaunināt TDS sertifikātu numurus un datumus.
    - Ģenerēt TDS pieprasījumu un grāmatoto TDS pieprasījumu.
    - Ģenerēt formu 27A, formu 26Q, formu 27Q TDS un e-TDS ceturkšņa pārskatus.
    - Ģenerēt formu 16A TDS sertifikātu.
