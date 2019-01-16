---
title: "Kandidātu piesaiste, izmantojot LinkedIn Recruiter"
description: "Šajā tēmā ir sniegta informācija par algoritmiskās mācīšanās izmantošanu, lai iegūtu darba un amata kandidātu ieteikumus."
author: josaw
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: 
ms.author: josaw
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: be66d9f95551066bb8bc25445c652d4fa59066d4
ms.openlocfilehash: 9bb323728923ff3b09ff0bfba3849f3c5d84eb34
ms.contentlocale: lv-lv
ms.lasthandoff: 12/07/2018

---

# <a name="sourcing-with-linkedin-recruiter"></a>Kandidātu piesaiste, izmantojot LinkedIn Recruiter
[!include[banner](../includes/banner.md)]

LinkedIn ir pasaulē lielākā potenciālo kandidātu datu bāze un bieži vien galvenā sistēma, ko izmanto personāla atlases darbinieki, lai atrastu kandidātus aktuālajām vakancēm, sazinātos ar šiem kandidātiem un piesaistītu viņus. LinkedIn Recruiter integrācija ar programmu Dynamics 365 for Talent: Attract atvieglo pieņemšanu darbā un datu sinhronizāciju abās sistēmās.

> [!NOTE]
> Lai varētu izmantot LinkedIn Recruiter integrāciju ar Attract, ir nepieciešams visaptverošais darbā pieņemšanas papildinājums un LinkedIn Recruiter licences.

## <a name="set-up-linkedin-recruiter-with-attract"></a>LinkedIn Recruiter iestatīšana programmā Attract 

Lai varētu izmantot LinkedIn Recruiter iespējas, vispirms Attract instancē ir jākonfigurē līguma līmeņa vai uzņēmuma līmeņa piekļuve. Lai pabeigtu konfigurēšanas procesu, ir jāizmanto lietotāja konts, kas LinkedIn Recruiter līgumā ir norādīts kā administrators. Veiciet tālāk norādītās darbības, lai konfigurētu LinkedIn Recruiter programmā Attract.

1.  Pierakstieties programmā Attract, izmantojot administratora kontu, un pārejiet uz sadaļu **Administratora iestatījumi**.

2.  Kreisajā rūtī noklikšķiniet uz cilnes **LinkedIn integrācija**.

[![Attract administratora skats, kurā var sākt LinkedIn Recruiter integrāciju](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3.  Noklikšķiniet uz **Izveidot savienojumu**, lai sāktu iestatīšanu un izpildītu sniegtos LinkedIn pierakstīšanās procesa norādījumus.

4.  Ja jums ir vairāku LinkedIn līgumu licences, atlasiet to līgumu, kam vēlaties izveidot savienojumu ar sistēmu Attract. Ja jums ir tikai viena LinkedIn līguma licence, šī darbība nav jāveic.

5.  Tagad sadaļā Administratora iestatījumi tiek ielādēts LinkedIn logrīks, kurā tiek rādīts integrācijas gadījumu saraksts. Sadaļā **Recruiter System Connect** noklikšķiniet uz **Pieprasīt**.

[![Attract administratora skats, kurā var pieprasīt LinkedIn Recruiter integrāciju](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)

6.  Pēc integrācijas pieprasījuma iesniegšanas no programmas Attract, tiek parādīts statuss **Partneris gatavs** un šo līdzekli var ieslēgt sadaļā **Recruiter administratora iestatījumi**. Ja šajā lapā tiek rādīts statuss **Paziņot partnerim**, uzgaidiet pāris sekundes, noklikšķiniet uz **Paziņot partnerim** un pēc tam atsvaidziniet lapu. Tagad statusam ir jābūt **Partneris gatavs**.

[![Attract administratora skats, kurā var norādīt Attract, ka programmā Attract ir pabeigtas pieprasījumu iesniegšanas darbības](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)

Lai pabeigtu nākamo darbību, ir vajadzīga administratora atļauja, kad ir piešķirta LinkedIn Recruiter līgumā.

7.  Pierakstieties pakalpojumā LinkedIn, izmantojot administratora kontu, un pārejiet uz sadaļu LinkedIn Recruiter lapas augšējā labajā stūrī. 

8. Ekrāna augšdaļā esošajā izvēlnē **Vairāk** noklikšķiniet uz **Administratora iestatījumi** un pēc tam noklikšķiniet uz cilnes **ATS**.

Tiek parādīta sistēma Attract un dažas opcijas, ko var ieslēgt.

9. Ja vēlaties iespējot tikai **ATS pieejamo datu indikatora** un **ATS pieejamo datu profila logrīka** viena klikšķa eksportēšanu, atlasiet **Uzņēmuma līmeņa piekļuve**. Ja vēlaties iespējot visus uzņēmuma līmeņa piekļuves līmeņus, kā arī InMail vēsturi, piezīmju vēsturi un InMail pasakņa profilu, atlasiet **Līguma līmeņa piekļuve**.

10. Ieslēdziet vēlamo piekļuves līmeni LinkedIn Recruiter iestatījumu sadaļā **ATS administrēšana**.

[![Attract integrācijas ieslēgšana LinkedIn Recruiter administratora skatā](./media/EnableRSC.png)](./media/EnableRSC.png)

12. Pierakstieties kā Attract administrators, pārejiet uz Attract sadaļu Admin Settings (Administratora iestatījumi) un atlasiet cilni **LinkedIn integrācija**. Tagad tiek ielādēts LinkedIn logrīks, kurā tiek rādīts statuss **Iespējots** un ir ieslēgts atlasītais piekļuves līmenis.

[![LinkedIn Recruiter integrācija ir pabeigta](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)

## <a name="using-linkedin-recruiter-capabilities"></a>LinkedIn Recruiter iespēju lietošana

Kad Attract administrators ir iespējojis LinkedIn Recruiter iespējas, tām var piekļūt par pieņemšanu darbā atbildīgie vadītāji un personāla atlases darbinieki. Lai izmantotu šīs iespējas, sadaļā **Lietotāja iestatījumi** izveidojiet savienojumu ar savu LinkedIn kontu. Dažas iespējas kļūst pieejamas pēc tam, kad ir izveidots savienojums gan administratora, gan lietotāja iestatījumu sadaļā.

### <a name="in-ats-profile-widget"></a>ATS pieejamo datu profila logrīks

Varat skatīt kandidāta LinkedIn profilu programmā Attract. Ja lietotāju ATS informācija atbilst LinkedIn informācijai, LinkedIn logrīkā tiek rādīts kandidāta profils.

Lai skatītu profilu, pārejiet uz kandidāta profilu vakances vai potenciālo kandidātu kopas sadaļā. Kandidāta profilā atlasiet cilni **LinkedIn**, lai ielādētu profila logrīku. Šajā lapā varat arī saglabāt kandidātu savos LinkedIn Recruiter projektos.
1. Ja pakalpojumā LinkedIn ir atrasta atbilstība, pamatojoties uz e-pastu un LinkedIn dalībnieka ID (precīza atbilstība), tiek parādīts kandidāta profils. Lietotājam joprojām ir iespēja saistīt/atsaistīt profilu.

2. Ja pakalpojumā LinkedIn nevar atrast kandidātu, pamatojoties uz e-pastu vai dalībnieka ID, tiek parādīts iespējamo kandidātu atbilstību saraksts pēs kandidāta vārda, un lietotājs var izvēlēties kādu no kandidātiem un saistīt profilu.  

3. Ja pakalpojumā LinkedIn nevar atrast nevienu kandidātu pēc vārda, tiek parādīts paziņojums, ka netika atrasta neviena atbilstība.

### <a name="1-click-export"></a>Viena klikšķa eksportēšana 

Kamēr piesaistāt kandidātus pakalpojumā LinkedIn, varat ar vienu klikšķi eksportēt kandidātu uz pašlaik brīvajām vakancēm. Lai veiktu viena klikšķa eksportēšanu, izpildiet tālāk norādītās darbības. Pirms šo darbību veikšanas pārbaudiet, vai jums ir piešķirta loma Par pieņemšanu darbā atbildīgais vadītājs vai Personāla atlases darbinieks attiecīgajai vakancei un vai vakancei ir posms **Potenciālais kandidāts**.

1.  Izveidojiet vakanci, piešķiriet atbilstošās lomas un aktivizējiet šo vakanci.

2.  Kad vakance ir aktivizēta, pārejiet uz LinkedIn Recruiter.

3.  Atrodiet meklēto kandidātu un pārejiet uz viņa profilu.

4.  Izmantojot kontaktinformācijas kartiņā pieejamo vakanču meklēšanas lodziņu, atrodiet programmā Attract aktivizēto vakanci pēc nosaukuma vai vakances ID. Ja neatrodat vakanci, noklikšķiniet uz **Mainīt ATS**, lai atrastu pareizo Attract instanci.

5. Kad vakance ir atlasīta, noklikšķiniet uz **Eksportēt**. Tagad kandidāts tiek izgūts programmā Attract.

6.  Pārejiet uz programmu Attract un atveriet atbilstošo vakanci. Tikko eksportētais kandidāts ir pievienots vakances posmam **Potenciālais kandidāts**.

### <a name="in-ats-indicator"></a>ATS pieejamo datu indikators 

Izmantojot LinkedIn Recruiter, varat izsekot tam, vai kandidāts ir pietiecies citām vakancēm jūsu organizācijā, uzzināt, vai viņam ir iestatīti dažādi darba pieteikumu posmi, un skatīt programmā Attract pievienotās atsauksmes un komentārus pakalpojumā LinkedIn Recruiter.

1.  Atveriet LinkedIn Recruiter un atrodiet meklēto kandidāta profilu.

2.  Ritiniet uz leju, lai skatītu kandidāta profila sadaļu **ATS pieejamie dati**.

3.  Varat izmantot šo logrīku, lai LinkedIn Recruiter skatā piekļūtu visai informācijai par kandidātu, kas ir pieejama programmā Attract.

4.  Atlasiet cilni **Vakances un statusi**, lai skatītu ar kandidātu saistītās vakances, viņa jaunāko statusu un progresu katras vakances darbā pieņemšanas procesā.

5.  Atlasiet cilni **Atsauksmes par interviju**, lai skatītu atsauksmes, ko intervētāji ir iesnieguši programmā Attract.

6.  Atlasiet cilni **Piezīmes**, lai skatītu programmā Attract saglabātās piezīmes par šo kandidātu.

> [!NOTE]
> Ja kandidāts nav ticis tālāk par potenciālā kandidāta posmu, kandidāta un pieteikuma dati netiek sinhronizēti pakalpojumā LinkedIn Recruiter.

### <a name="inmail-history"></a>InMail vēsture

LinkedIn InMail vēsture ir pieejama tad, ja ir pieejama līguma līmeņa piekļuve pakalpojumam LinkedIn Recruiter. Ja ir iespējots šis līdzeklis, varat skatīt visu saziņas ar kandidātu InMail vēsturi. Varat arī uzzināt, kas vēl jūsu organizācijā ir sazinājies ar kandidātu, izmantojot InMail, taču nevarat skatīt šīs saziņas ziņojumus.

Lai skatītu InMail vēsturi, pārejiet uz kandidāta profilu, atveriet cilni **LinkedIn** un ritiniet līdz lapas apakšdaļai, kur ir pieejama vēsture. InMail vēsturi varat skatīt, ja jums programmā InMail ir bijusi saruna ar kandidātu. InMail ziņojumi tiek sinhronizēti ar programmu Attract ik pēc pāris stundām.

### <a name="notes-history"></a>Piezīmju vēsture 

LinkedIn piezīmju vēsture ir pieejama tad, ja ir pieejama līguma līmeņa piekļuve pakalpojumam LinkedIn Recruiter. Ja ir iespējots šis līdzeklis, varat skatīt piezīmes par kandidātu, kuras ir saglabājuši dažādi jūsu organizācijas personāla atlases darbinieki.

Lai skatītu piezīmju vēsturi, pārejiet uz kandidāta profilu, atveriet cilni **LinkedIn** un ritiniet līdz lapas apakšdaļai, kur ir pieejama vēsture. Varat skatīt visas piezīmes par kandidātu pakalpojumā LinkedIn Recruiter.

### <a name="inmail-stub-profile"></a>InMail pasakņa profils

InMail pasakņa profils ir pieejams tad, ja ir pieejama līguma līmeņa piekļuve pakalpojumam LinkedIn Recruiter. Ja kandidāti piekrīt kopīgot savu LinkedIn profilu ar jebkuru jūsu organizācijas lietotāju, jūs varat izsekot kandidātus programmā Attract un katram kandidātam tiek izveidots jauns kandidāta ieraksts. Kandidāta e-pasta adresi varat skatīt, ja kandidāts ar e-pasta adresi jau ir reģistrēts sistēmā vai ir izvēlējies koplietot adresi ar personāla atlases darbinieku.

Lai skatītu kandidātu sarakstu, pārejiet uz sadaļu **Potenciālo kandidātu kopas**, kurā ir redzama sistēmas izveidota LinkedIn potenciālo kandidātu kopa. Šajā potenciālo kandidātu kopā ir ietverts no LinkedIn saņemtais kandidātu un to pasakņa profilu saraksts, kurā ir redzams kandidāta vārds un uzvārds. Ja kandidāts ir izvēlējies kopīgot savu e-pasta adresi, tiek rādīts kandidāta e-pasta adreses ID.

