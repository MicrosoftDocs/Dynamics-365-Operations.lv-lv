---
title: "Noliktavas mobilo ierīču displeja iestatījumi"
description: "Šajā rakstā ir izskaidrots, kā iestatīt mobilās ierīces displeja izskatu un kartēt vadīklu tastatūras īsinājumtaustiņus, piemēram, pogas."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserSetup, WHSRFColor, WHSRFColorPicker, WHSWorkUserDisplaySettings
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 29071
ms.assetid: 931a02e8-b561-45e3-9c44-06b875ced1b4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 799cd4a940813e39f8be6b4c127b9efabc88e909
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="warehouse-mobile-device-display-settings"></a>Noliktavas mobilo ierīču displeja iestatījumi

[!include[banner](../includes/banner.md)]


Šajā rakstā ir izskaidrots, kā iestatīt mobilās ierīces displeja izskatu un kartēt vadīklu tastatūras īsinājumtaustiņus, piemēram, pogas. 

Šis raksts attiecas uz moduļa Noliktavas pārvaldība "uzlabotās noliktavas" līdzekļiem. Mobilās ierīces var izmantot daudziem uzdevumiem, ko veic noliktavas darbinieki.

## <a name="specify-styles-and-map-keyboard-shortcuts"></a>Stilu norādīšana un īsinājumtaustiņu kartēšana
Kā daļu no mobilās ierīces konfigurācijas var definēt dažādus izkārtojumus mobilajām ierīcēm. Lai to paveiktu, jums ir jāzina kaskadētā stila lapu (CSS) faila nosaukumu un Active Server lapas paplašinājuma (ASPX) faila nosaukumu. Noklusējuma faili tiek instalēti kā daļa no noliktavas mobilo ierīču portāla instalācijas. Ja nezināt failu nosaukumus, sazinieties ar sistēmas administratoru. Jaunu stilu ir iespējams definēt lapā **Mobilās ierīces displeja iestatījumi**:

-    laukā **CSS fails** ievadiet CSS faila nosaukumu. Iekļaujiet .css faila nosaukuma paplašinājumu.
-   Laukā **Mobilās ierīces displeja iestatījumu skats** norādiet ASPX failu. **Neiekļaujiet** .aspx faila nosaukuma paplašinājumu.

CSS un ASPX failus jānovieto īpašā direktorijā, lai interneta informācijas pakalpojumu (IIS) programma tos varētu ielādēt. Varētu būt noderīgi definēt dažādus CSS failus, ja mobilās ierīces funkcionalitātei izmantojat dažādos pārlūkos vai dažāda veida aparatūrā, kas pieprasa dažādas izkārtojuma vadīklas. Vienkāršus iestatījumus, piemēram, fona krāsu, fontu un fonta lielumu tekstam, un pogu platumu un uzvedību var viegli kontrolēt, izmantojot CSS failus dažādos veidos. ASPX fails tiek izmantots, lai parādītu mobilo vietni servera puses ASP.NET programmā. Šis fails kontrolē veidu, kā ir izkārtota HTML vispārējā struktūra. Šo funkcionalitāti ir ieteicams pielāgot tikai tad, ja jums ir nopietnas strukturālās problēmas ar HTML un JavaScript, un šis kods ir jāmaina jūsu konkrētajām ierīcēm. Lai kartētu HTML vadīklas mobilās ierīces lapā īsinājumtaustiņos, lapā **Mobilās ierīces displeja iestatījumi** laukā **Īsinājumtaustiņš** piešķiriet taustiņiem ciparu kodus. Var izmantot izvēlni **Skatīt īsinājumtaustiņu kodus** mobilajā ierīcē, lai atrastu ciparzīmju kodus. Ievērojiet, ka kartējumi var atšķirties atkarībā no izmantotās aparatūras. Lai izveidotu kartēšanu, jāizmanto tālāk aprakstītā sintakse.

&lt;vadīklas nosaukums&gt;(&lt;taustiņa nosaukums&gt;)=&lt;taustiņa kods&gt;;

Šeit ir sintakses daļu paskaidrojums:

-   **&lt;vadīklas nosaukums&gt;** — nosaukums vadīklai (piemēram, pogai), kas ir atveidota HTML.
-   **(&lt;taustiņa nosaukums&gt;)** — tā tastatūras taustiņa nosaukums, kam veidojat saīsni.
-   **&lt;Taustiņa kods&gt;** — tā taustiņa ciparzīmju kods, ko izmantosiet kā īsinājumtaustiņu.

Tas ir piemērs:

Atcelt(Esc)=27; Pilna(F2)=113

Visām lapām, kas ietver pogu **Atcelt**, pogai būs šis teksts:

**(Esc) Atcelt**

Nospiežot tastatūras taustiņu Esc, tiks aktivizēta poga **Atcelt**. Lai lietotu stila un īsinājumtaustiņu iestatījumus konkrētai ierīcei, ir jāizveido kartēšana laukā **Kritēriji**. .NET regulārā izteiksme jāizmanto, izveidojot kartēšanu, un izteiksmei jāsastāv no trim sadaļām, kas ir atdalītas ar vertikālu joslu (|), kā parādīts šeit:

Request.UserHostAddress=&lt;lietotāja resursdatora adrese&gt;|HostName=&lt;lietotāja resursdatora nosaukums&gt;|Request.UserAgent=&lt;lietotāja aģents&gt;

Šeit ir izteiksmes daļu paskaidrojums:

-   **&lt;lietotāja resursdatora adrese&gt;** — .NET regulārā izteiksme, kas atbilst pieprasītāja IP adresei.
-   **&lt;lietotāja resursdatora nosaukums&gt;** — .NET regulārā izteiksme, kas atbilst pieprasītāja tīkla nosaukumam.
-   **&lt;lietotāja aģents&gt;** — .NET regulārā izteiksme, kas atbilst pārlūkprogrammas identifikatoram, ko izmanto pieprasītājs.

Tālāk minētais piemērs iespējo programmas Internet Explorer 8 lietošanu:

Request.UserHostAddress=.\*|HostName=.\*|Request.UserAgent=MSIE\\s8\\.0

Var izmantot izvēlni **Skatīt servera konfigurāciju displeja iestatījumiem** mobilajā ierīcē, lai atrastu informāciju par iestatījumiem.

## <a name="define-text-colors-for-messages"></a>Ziņojumu teksta krāsu definēšana
Var izmantot lapu **Mobilās ierīces teksta krāsas**, lai kontrolētu dažādas krāsas, kas tiek izmantotas sistēmas ģenerētajos ziņojumos, piemēram, kļūdu ziņojumos. Piemēram, teksta krāsa var norādīt uz ziņojuma mērķi vai stingrību. Ir parādīti šādi ziņojumu tipi.

| Ziņojuma tips | Apraksts                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Noklusējums      | Noklusējuma ziņojumos tiek izmantoti noklusējuma krāsu iestatījumi visiem ziņojumiem, kā definēts Noliktavas mobilo ierīču portāla CSS failā.                                                   |
| Kļūda        | Kļūdu ziņojumi norāda uz problēmu, ko lietotājam jāatrisina pirms viņš var turpināt.                                                                                             |
| Sekmīgi      | Veiksmes ziņojumi apstiprina, ka darbība bijusi veiksmīga.                                                                                                                                |
| Brīdinājums      | Brīdinājuma ziņojumi informē darbinieku, ka ir problēma vai ka varētu būt problēma, ja darbinieks turpinās. Tomēr, darbiniekam nav jāatrisina problēma, lai turpinātu. |

Lai atlasītu krāsu, lapā **Atlasīt krāsu** noklikšķiniet uz paletes vai ierakstiet heksadecimālo krāsas kodu.

## <a name="define-the-date-format-to-use-on-mobile-devices"></a>Mobilajās ierīces lietojamā datumu formāta definēšana
Katrai instalācijai varat paplašināt pieņemto datumu formātu sarakstu. Piemēram, šī iespēja var būt noderīga, ja vēlaties norādīt tādu formātu, kas ļauj darbiniekam ērtāk ievadīt datumus mobilajā ierīcē. Noklusējuma formātu nosaka lietotāja noklusējuma valoda, kas ir norādīta laukā **Valoda** lapā **Lietotāja opcijas**. (Tā pati lapa tiek izmantota arī, lai darbinieku saistītu ar konkrētu noliktavas darba lietotāju.) **Piezīme.** Noliktavas mobilo ierīču portāls neizmanto lauka **Datuma, laika un skaitļu formāts** iestatījumu lapā **Valodas un reģiona preferences**. Lai mainītu datuma formātu, jums jāzina Microsoft .NET Framework regulārās izteiksmes. Papildinformāciju skatiet šeit: [.NET Framework regulārās izteiksmes](http://go.microsoft.com/fwlink/?LinkId=391260). Lai definētu datuma formātus, rediģējiet failu Dates.ini, kas noliktavas mobilo ierīču portāla serverī atrodas šeit: Saturs\\Iestatījumi\\Dates.ini. Šis fails izmanto .NET regulārās izteiksmes, lai norādītu datuma formātu. Regulārajai izteiksmei ir jāietver apakšizteiksmes, kas izveido nosauktas grupas dienai, mēnesim un gadam (DDMMGG), kā parādīts šajā piemērā:

^(?&lt;diena&gt;\\d{2})(?&lt;mēnesis&gt;\\d{2})(?&lt;gads&gt;\\d{2})$

Katra apakšizteiksme pieprasa no viena līdz diviem cipariem dienai un mēnesim, un no viena līdz četriem cipariem gadam. Piemēram, šī apakšizteiksme definē nosauktu grupu gadam un tai ir nepieciešami 2–4 cipari:

(?&lt;gads&gt;\\d{2,4})

Vienā failā var norādīt vairāk nekā vienu izteiksmi. Katrai izteiksmei jābūt atsevišķā rindā. Pirmā atbilstoša izteiksme tiek izmantota, lai parsētu datumu.

<a name="see-also"></a>Skatiet arī
--------

[Mobilo ierīču konfigurācija darbam noliktavā](configure-mobile-devices-warehouse.md)




