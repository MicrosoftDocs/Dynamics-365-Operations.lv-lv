---
title: "Noliktavas mobilo ierīču displeja iestatījumi"
description: "Šajā rakstā ir izskaidrots, kā iestatīt mobilās ierīces displeja izskatu un kartēt vadīklu tastatūras īsinājumtaustiņus, piemēram, pogas."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysUserSetup, WHSRFColor, WHSRFColorPicker, WHSWorkUserDisplaySettings
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 29071
ms.assetid: 931a02e8-b561-45e3-9c44-06b875ced1b4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: afa59439e06aad9d669eb352a9837a013f447249
ms.openlocfilehash: 721b293d1f8c76458ca510732f9bb94f003ac6e3
ms.lasthandoff: 03/31/2017


---

# <a name="warehouse-mobile-device-display-settings"></a>Noliktavas mobilo ierīču displeja iestatījumi

Šajā rakstā ir izskaidrots, kā iestatīt mobilās ierīces displeja izskatu un kartēt vadīklu tastatūras īsinājumtaustiņus, piemēram, pogas. 

Šis raksts attiecas uz moduļa Noliktavas pārvaldība "uzlabotās noliktavas" līdzekļiem. Mobilās ierīces var izmantot daudziem uzdevumiem, ko veic noliktavas darbinieki.

## <a name="specify-styles-and-map-keyboard-shortcuts"></a>Stilu norādīšana un īsinājumtaustiņu kartēšana
Kā daļu no mobilās ierīces konfigurācijas var definēt dažādus izkārtojumus mobilajām ierīcēm. Lai to paveiktu, jums ir jāzina kaskadētā stila lapu (CSS) faila nosaukumu un Active Server lapas paplašinājuma (ASPX) faila nosaukumu. Noklusējuma faili tiek instalēti kā daļa no noliktavas mobilo ierīču portāla instalācijas. Ja nezināt failu nosaukumus, sazinieties ar sistēmas administratoru. Jaunu stilu ir iespējams definēt lapā **Mobilās ierīces displeja iestatījumi**:

-    laukā **CSS fails** ievadiet CSS faila nosaukumu. Iekļaujiet .css faila nosaukuma paplašinājumu.
-   Laukā **Mobilās ierīces displeja iestatījumu skats** norādiet ASPX failu. **Neiekļaujiet** .aspx faila nosaukuma paplašinājumu.

CSS un ASPX failus jānovieto īpašā direktorijā, lai interneta informācijas pakalpojumu (IIS) programma tos varētu ielādēt. Varētu būt noderīgi definēt dažādus CSS failus, ja mobilās ierīces funkcionalitātei izmantojat dažādos pārlūkos vai dažāda veida aparatūrā, kas pieprasa dažādas izkārtojuma vadīklas. Vienkāršus iestatījumus, piemēram, fona krāsu, fontu un fonta lielumu tekstam, un pogu platumu un uzvedību var viegli kontrolēt, izmantojot CSS failus dažādos veidos. ASPX fails tiek izmantots, lai parādītu mobilo vietni servera puses ASP.NET programmā. Fails kontrolē, kā izkārtota HTML vispārējā struktūra. Šo funkcionalitāti ir ieteicams pielāgot tikai tad, ja jums ir nopietnas strukturālās problēmas ar HTML un JavaScript, un ir jāmaina šis kods konkrētām ierīcēm. Lai kartētu HTML vadīklas mobilās ierīces lapā īsinājumtaustiņos, lapā **Mobilās ierīces displeja iestatījumi** laukā **Īsinājumtaustiņš** piešķiriet taustiņiem ciparu kodus. Var izmantot izvēlni **Skatīt īsinājumtaustiņu kodus** mobilajā ierīcē, lai atrastu ciparzīmju kodus. Ievērojiet, ka kartējumi var atšķirties atkarībā no izmantotās aparatūras. Lai izveidotu kartēšanu, jāizmanto tālāk aprakstītā sintakse.

&lt;vadīklas nosaukumu&gt;(&lt;atslēgas nosaukums&gt;) =&lt;atslēgas kodu&gt;;

Šeit ir sintakses daļu paskaidrojums:

-   **&lt;vadīklas nosaukums&gt;** -kontroli (piemēram, pogas), kas sniegti šajā HTML nosaukums.
-   **(&lt;atslēgas nosaukums&gt;) ** -Tastatūras taustiņš, ka jūs gatavojat saīsnes nosaukumu.
-   **&lt;Ievadiet kodu&gt;** -skaitliskas rakstzīmes kodu atslēgas, kas jāizmanto kā īsceļa taustiņš.

Tas ir piemērs:

Atcelt(Esc)=27; Pilna(F2)=113

Visām lapām, kas ietver pogu **Atcelt**, pogai būs šis teksts:

**(Esc) Atcelt**

Nospiežot tastatūras taustiņu Esc, tiks aktivizēta poga **Atcelt**. Lai lietotu stila un īsinājumtaustiņu iestatījumus konkrētai ierīcei, ir jāizveido kartēšana laukā **Kritēriji**. .NET parasta izteiksme jāizmanto, izveidojot kartēšanu, un izteiksmei jāsastāv no trim sadaļām, kas ir atdalītas ar vertikālu joslu (|), kā parādīts šeit:

Request.UserHostAddress=&lt;lietotāja resursdatora adrese&gt;| HostName =&lt;uzņēmēja lietotājvārdu&gt;| Request.UserAgent=&lt;lietotāja aģents&gt;

Šeit ir izteiksmes daļu paskaidrojums:

-   **&lt;lietotāja resursdatora adrese&gt;** -A .NET regulāras izteiksmes, kas atbilst pieprasītājam IP adresi.
-   **&lt;uzņēmēja lietotājvārdu&gt;** -A .NET regulāras izteiksmes, kas atbilst tīkla nosaukums pieprasītājam.
-   **&lt;lietotāja aģents&gt;** -A .NET regulāras izteiksmes, kas atbilst pārlūks, kas izmanto pieprasītājam identifikators.

Tālāk minētais piemērs iespējo programmas Internet Explorer 8 lietošanu:

Request.UserHostAddress=. \*| HostName =. \*| Request.UserAgent=MSIE\\s8\\,0

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
Katrai instalācijai varat paplašināt pieņemto datumu formātu sarakstu. Piemēram, šī iespēja var būt noderīga, ja vēlaties norādīt tādu formātu, kas ļauj darbiniekam ērtāk ievadīt datumus mobilajā ierīcē. Noklusējuma formātu nosaka lietotāja noklusējuma valoda, kas ir norādīta laukā **Valoda** lapā **Lietotāja opcijas**. (Vienu un to pašu lapu izmanto arī darbinieka piesaiste ar konkrētu noliktavu darbu lietotājs.) **Piezīme:** noliktavas mobilo ierīču portāla doesn't izmantot iestatījumu **datuma, laika un skaitļa formātu** lauku **valodas un reģiona preferences** lapā. Lai mainītu datuma formātu, jums jāzina Microsoft .NET Framework parastās izteiksmes. Papildinformāciju skatiet šeit: [.NET Framework parastās izteiksmes](http://go.microsoft.com/fwlink/?LinkId=391260). Lai noteiktu datumu formātus, rediģēt Dates.ini failu, kas atrodas satura\\iestatījumus\\Dates.ini noliktavas mobilo ierīču portāla serverī. Šis fails izmanto .NET parastās izteiksmes, lai norādītu datuma formātu. Parastai izteiksmei ir jāietver apakšizteiksmes, kas izveido nosauktas grupas dienai, mēnesim un gadam (DDMMGG), kā parādīts šajā piemērā:

^(? &lt;day&gt;\\d{2})(?&lt; month&gt;\\d{2})(?&lt; gadā&gt;\\d {2}) $

Katra apakšizteiksme pieprasa no viena līdz diviem cipariem dienai un mēnesim, un no viena līdz četriem cipariem gadam. Piemēram, šī apakšizteiksme definē nosauktu grupu gadam un tai ir nepieciešami 2–4 cipari:

(? &lt;year&gt;\\d{2,4})

Vienā failā var norādīt vairāk nekā vienu izteiksmi. Katrai izteiksmei jābūt atsevišķā rindā. Pirmā atbilstoša izteiksme tiek izmantota, lai parsētu datumu.

<a name="see-also"></a>Skatiet arī
--------

[Configuration of mobile devices for warehouse work](configure-mobile-devices-warehouse.md)


