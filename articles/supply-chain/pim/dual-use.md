---
title: Divējāda lietojuma preces
description: Šajā rakstā ir izskaidrots, kā sekot līdzi precēm, kas ir identificētas kā dubultās lietošanas preces, saglabāt sertifikātu numurus katrai atbilstošai precei un mērķa valstij, un drukāt derīgus sertifikātu numurus atbilstošos rēķinos, pavadzīmēs un/vai pārdošanas pasūtījumos.
author: t-benebo
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: COODualUseCerts, COORules, COODualUseCountries
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 5147a837be91aab519c373e624acc036f9293641
ms.sourcegitcommit: 555de844b8ba02fe095c28a2d447fc7c441ae549
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460553"
---
# <a name="dual-use-goods"></a>Divējāda lietojuma preces

[!include [banner](../includes/banner.md)]

Divējāda lietojuma preces parasti ir krājumi, kas tiek izmantoti gan civiliem, gan militāriem mērķiem. Piemēram, ķīmiskas vielas var izmantot gan kā mēslojumu, gan sprāgstvielu. Daudzās valstīs ir īpaši noteikumi, kas attiecas uz divējāda lietojuma preču eksportu, importu un transportēšanu. Tāpēc ir svarīgi, ka divējāda lietojuma preču starptautiskajā tirdzniecībā iesaistītie uzņēmumi seko dažādām politikām un sertifikātiem.

Divējādā lietojuma līdzeklis palīdz uzņēmumiem izsekot precēm, kas tiek identificētas kā divējāda lietojuma preces, saglabāt sertifikātu numurus katrai attiecīgajai precei un galamērķa valstij un drukāt derīgos sertifikātu numurus attiecīgajos rēķinos, pavadzīmēs un/vai pārdošanas pasūtījumos. Tas palīdz nodrošināt, ka preču nosūtīšanas brīdī tās vienmēr iekļauj atjauninātus sertifikātus.

Izskatiet tālāk norādīto scenāriju:

1. Sistēmas lapa **Divējāda lietojuma valsts iestatīšana** norāda, ka sūtījumiem uz Franciju ir nepieciešama sertificēšana.
2. Produkta X-100 lapa **Izlaisto preču detalizēta informācija** norāda, ka tā ir divējāda lietojuma prece. Kods, kategorija, grupa un režīms kopā norāda eksporta kontroles klasifikāciju, kurai prece pieder.
3. Lapā **Divējāda lietojuma sertifikāti** ir ietverts sertifikāts precei X-100, kad tas tiek nosūtīts uz Franciju. Sertifikāta derīguma termiņš beidzas 2020. gada 1. janvārī.
4. 2020. gada 17. jūnijā jūs izveidojat pārdošanas pasūtījumu klienta uzņēmumam, kas atrodas Francijā, un pasūtījumā ir ietverta prece X-100.
5. Kad jūs apstipriniet pārdošanas pasūtījumu, sistēma nosaka šādu informāciju:

    1. Vai pasūtījumā ir iekļautas preces, kas ir divējāda lietojuma preces?
    2. Ja pasūtījumā iekļautas divējāda lietojuma preces, vai galamērķa valsts pieprasa divējāda lietojuma sertifikātus?
    3. Ja valsts pieprasa divējāda lietojuma sertifikātus, vai pastāv derīgs sertifikāts katrai divējāda lietojuma precei galamērķa valstī?

6. Pasūtījumā ir ietverta prece X-100, prece tiek nosūtīta uz Franciju un šai precei ir Francijas sertifikāts. Tomēr sertifikāta derīguma termiņš ir beidzies. Tāpēc tiek parādīts šāds brīdinājuma ziņojums: “Divējāda lietojuma sertifikāti, vienam vai vairākiem divējāda lietojuma krājumiem šajā pārdošanas pasūtījumā, nav derīgi. Vai vēlaties turpināt apstiprināšanu?”

Šajā rakstā ir izskaidrots, kā konfigurēt visus iestatījumus, kas ir nepieciešami dubultās lietošanas preču iestatīšanai un šī scenārija atbalstam.

## <a name="define-dual-use-requirements-for-each-relevant-country"></a>Definēt divējāda lietojuma prasības katrai attiecīgajai valstij

Dažādām valstīm ir atšķirīgas prasības divējāda lietojuma precēm. Izmantojiet lapu **Divējāda lietojuma valsts iestatīšana**, lai sekotu valstīm, kas prasa un neprasa sertifikātu. Šeit norādītā informācija tiek pārbaudīta, veidojot pārdošanas pasūtījumus, un jums tiks atgādināts nodrošināt nepieciešamo sertifikāciju.

Lai iestatītu informāciju par divējāda lietojuma prasībām dažādām valstīm, veiciet tālāk norādītās darbības.

1. Dodieties uz **Preču informācijas pārvaldība \> Iestatīšana \> Preču atbilstība \> Divējāda lietojuma preces \> Divējāda lietojuma valsts iestatīšana**.
2. Atlasiet esošu valsts iestatījumu rediģēšanai vai darbību rūtī atlasiet **Jauns**, lai izveidotu jaunu valsts iestatījumu.
3. Iestatiet atlasītās vai jaunās valsts iestatījumam šādas vērtības.

    | Lauks | Apraksts |
    |---|---|
    | Valsts/reģions | Atlasiet, kuras valsts prasībām sekojat. |
    | Sertifikāts obligāts | Atzīmējiet šo izvēles rūtiņu valstīm, kas pieprasa sertifikāciju divējāda lietojuma precēm. Nodzēsiet to valstīm, kam nav nepieciešama šī sertifikācija. |

## <a name="create-dual-use-categories"></a>Divējāda lietojuma kategoriju izveide

Divējāda lietojuma preces bieži jāklasificē atbilstoši to eksporta kontroles klasifikācijas numuram (ECCN). ECCN ir burtciparu kods, kas klasificē preces, pamatojoties uz tādiem faktoriem kā prece un tehnoloģija. Lapa **Divējāda lietojuma kategorijas** palīdz izveidot to kategoriju sarakstu, kuras izmantojat pārskatu veidošanai.

Lai iestatītu divējāda lietojuma kategorijas, veiciet tālāk norādītās darbības.

1. Dodieties uz **Preču informācijas pārvaldība \> Iestatīšana \> Preču atbilstība \> Divējāda lietojuma preces \> Divējāda lietojuma kategorijas**.
2. Atlasiet rediģēšanai esošu kategoriju vai darbību rūtī atlasiet **Jauns**, lai izveidotu jaunu kategoriju.
3. Atlasītajai vai jaunajai kategorijai iestatiet šādas vērtības.

    | Lauki | apraksts |
    |---|---|
    | Divējāda lietojuma kods | Ievadiet pilnu ECCN kodu (piemēram, *3A001*).|
    | Divējāda lietojuma kategorija | Ievadiet komercijas vadīklu saraksta (CCL) kategorijas ECCN koda daļu. Piemēram, ECCN kodam *3A001* šī vērtība ir *3*. |
    | Divējāda lietojuma grupa | Ievadiet preču grupas ECCN koda daļu. Piemēram, ECCN kodam *3A001* šī vērtība ir *A*. |
    | Divējāda lietojuma režīms | Ievadiet krājuma režīma kodu. Šis kods norāda iemeslu, kāpēc krājums tiek klasificēts kā divējāda lietojuma prece. Piemēram, ECCN kodam *3A001* šī vērtība ir *001*. |

## <a name="apply-dual-use-categories-to-products"></a>Divējāda lietojuma kategoriju piemērošana precēm

Lai identificētu preci kā divējāda lietojuma preci un piemērotu tai divējāda lietojuma kategoriju, veiciet tālāk norādītās darbības.

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Atlasiet vai izveidojiet preci, lai atvērtu tās lapu **Izlaisto preču detalizēta informācija**.
1. Kopsavilkuma cilnē **Ārējā tirdzniecība** iestatiet opciju **Divējāda lietojuma preces** uz **Jā**, lai identificētu pašreizējo preci kā divējāda lietojuma preci.
1. Iestatiet lauku **Divējāda lietojuma kods** uz kodu, kas piemērots pašreizējai precei. (Jūs definējāt šo kodu lapā **Divējāda lietojuma kategorijas**.)

> [!NOTE]
>
> Sistēma veic šādas dubultās izmantošanas pārbaudes, kad tā ģenerē pārdošanas apstiprinājumu:
>
> 1. Vai pasūtījumā ir iekļautas jebkādas dubultās lietošanas preces?
> 1. Ja tā ir, vai mērķa valstij ir nepieciešami dubultās lietošanas sertifikāti?
> 1. Ja tā ir, vai mērķa valstij katrai dubultās izmantošanas derīgām ir sertifikāti un vai šie sertifikāti ir derīgi apstiprinātajiem nosūtīšanas datumiem?
> 1. Ja 1. un 2. jautājuma atbildes ir "Jā" un atbilde uz 3. jautājumu ir "Nē", sistēma parāda brīdinājumu, lai informētu lietotāju, ka pārdošanas pasūtījumā vienai vai vairākām duālām precēm trūkst dubultās lietošanas sertifikātu. Lietotājam, iespējams, jāiegūst nepieciešamie sertifikāti un jāmēģina vēlreiz, bet, ja vēlaties, varat noraidīt brīdinājumu un turpināt pārdošanas apstiprinājumu.

## <a name="set-up-dual-use-certificates"></a>Divējāda lietojuma sertifikātu iestatīšana

Izmantojiet lapu **Divējāda lietojuma sertifikāti**, lai iestatītu un pārvaldītu nepieciešamos divējāda lietojuma sertifikātus katrai precei un valstij. Varat izsekot katra sertifikāta informācijai, piemēram, valstij un derīguma datumiem. Varat arī iestatīt opcijas, lai norādītu, kur šī informācija ir jādrukā. Piemēram, informāciju var drukāt rēķinā, pavadzīmē un/vai pārdošanas pasūtījumā. Šis iestatījums tiek pārbaudīts, veidojot pārdošanas pasūtījumu.

1. Dodieties uz **Preču informācijas pārvaldība \> Iestatīšana \> Preču atbilstība \> Divējāda lietojuma preces \> Divējāda lietojuma sertifikāti**.
2. Atlasiet rediģēšanai esošu sertifikātu vai darbību rūtī atlasiet **Jauns**, lai izveidotu jaunu sertifikātu.
3. Atlasītajam vai jaunajam sertifikātam iestatiet šādas vērtības.

    | Lauks | apraksts |
    |---|---|
    | Krājums | Atlasiet divējāda lietojuma krājuma kodu, uz kuru attiecas šis sertifikāts. |
    | Valsts/reģions | Galamērķa valsts vai reģions, kurā jāizmanto šis sertifikāts. |
    | Sertifikāta numurs | Numurs, kas norādīts sertifikātam, kurš izsniegts kreditoram vai klientam. |
    | Spēkā esošs | Atlasiet pirmo datumu, kad pašreizējais sertifikāts ir derīgs.|
    | Termiņa beigas | Atlasiet pēdējo datumu, kad pašreizējais sertifikāts ir derīgs. |
    | Drukāt rēķinā | Atzīmējiet šo izvēles rūtiņu, lai drukātu sertifikāta numuru rēķinos, kas norādītajā datumu diapazonā ir adresēti norādītajai valstij. |
    | Drukāt pavadzīmē | Atzīmējiet šo izvēles rūtiņu, lai drukātu sertifikāta numuru pavadzīmēs, kas norādītajā datumu diapazonā ir adresētas norādītajai valstij. |
    | Drukāt pārdošanas pasūtījumā | Atzīmējiet šo izvēles rūtiņu, lai drukātu sertifikāta numuru pārdošanas pasūtījumos, kas norādītajā datumu diapazonā ir adresēti norādītajai valstij. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
