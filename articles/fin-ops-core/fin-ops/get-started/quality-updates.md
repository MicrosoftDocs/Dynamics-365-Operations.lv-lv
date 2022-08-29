---
title: Apsteidzās kvalitātes atjauninājumi
description: Šajā rakstā ir sniegta informācija par apsteidz aktīvo kvalitātes atjauninājumu piegādi.
author: rashmansur
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2022-08-19
ms.search.form: ''
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 9d81cb15e9a127e7bea7ad9b5e0f50a1ee543f71
ms.sourcegitcommit: 78e85ad49634cd31459fdb7325cb273352bf1501
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/23/2022
ms.locfileid: "9338142"
---
# <a name="proactive-quality-updates"></a>Apsteidzās kvalitātes atjauninājumi

[!include[banner](../includes/banner.md)]

Pēdējos gados Microsoft ir progresējusi attiecībā uz to, ko mēs nosaucām par [vienu versiju](../../dev-itpro/lifecycle-services/oneversion-overview.md). Vienas versijas priekšnoteikums ir vienkāršs: jo tuvāk var būt visiem klientiem tajā pašā programmatūras versijā, jo augstāka kvalitātes, ko mēs varam piegādāt. Kļūdas tiek meklētas un izlabotas vienu reizi, un šie risinājumi tiek ievadīti ātrāk un ātrāk.

Šo telpu apstiprina rezultāti: zemāka incidentu skaits starp mūsu produktiem. Ja debitori nav ar vienu versiju, pastāvīgi redzams, ka tos ietekmē problēmas, kurām risinājums jau ir pieejams. Dynamics 365 Finanses, Dynamics 365 Piegādes Dynamics 365 Project Operations Dynamics 365 Commerce ķēde jau ir progresējusi un paldies nesenajiem tehniskajiem avansiem, tagad ir iespējams veikt nākamo soli. Tālāk ir aprakstīts, ko mēs gatavojam darīt, ko mēs jau esam veikuši, lai iestatītu pakāpi un to, kā un kad mēs ieviesām jaunās iespējas bez pārrāvuma.

## <a name="focus-on-quality-updates"></a>Fokuss uz kvalitātes atjauninājumiem

Šobrīd gadā tiek nodrošināti [septiņi](public-preview-releases.md) pakalpojumu atjauninājumi. Piemēram, versija 10.0.29 ir pakalpojuma atjauninājums. Līdz nesen ir astoņi atjauninājumi gadā. Tomēr viens atjauninājums tika nomests, atbildot uz debitora datiem, kas norāda uz vēlmi izvairīties no izmaiņām kalendārā gada beigās.

Mēs mainīsim pakalpojumu atjauninājumu laiku. Tā vietā nākamais solis vienas versijas ceļojuma laikā ir fokusēts uz kvalitātes *atjauninājumiem*. Kvalitātes atjauninājumi ir labojumfailu kumulatīvie būvumi. Tajos nav iekļautas jaunas funkcijas. Jebkurā laikā mūsu visa debitoru kopiena tiek izplatīta starp trim vai četriem jaunākajiem pakalpojuma atjauninājumiem. Tomēr jebkurā konkrētā pakalpojuma atjauninājumā grupā var izmantot ducis dažādu kvalitātes atjauninājumu versiju, atkarībā no lietotāju izvietošanas datumiem. Nākamajā solī mēs apsteidzam kvalitātes atjauninājumus. Mēs jau izmantojam šo modeli mūsu programmām Dataverse un esiet redzams uzlabotās kvalitātes rezultātu paredzamais rezultāts un jāsamazina atbalsta incidenti.

Protams, defektu samazināšana var samazināt vai pilnībā izslēgt nepieciešamību pēc kvalitātes atjauninājumiem. Lidojumam ir vairākas iniciatīvas, lai samazinātu defektus, kuriem nepieciešami kvalitātes atjauninājumi. Pat ja kvalitātes atjauninājumā tiek samazinātas lietderīgās noslodzes, saskaņotība starp debitora bāzi uzlabos izmantojamību, ātrāku uzlabojumus debitoriem un samazina debitoru frekvenci, kas saskaras ar problēmām, kam jau pastāv risinājumi.

## <a name="making-proactive-distribution-possible"></a>Padarīt proaktīvo sadali par iespējamo

Vairāki avansi jau ir izvietoti, kas iespējo kvalitātes atjauninājumu proaktīvo piegādi:

- **Nulles dīkstāves** atjaunināšana – Lai virzītu biežākas vides, ir svarīgi samazināt ietekmi uz vides pieejamību, lai saglabātu Dynamics 365 pakalpojumu līmeņa līgumus (SLA). Sākotnēji tika ieviesta nulles dīkstāves atjaunināšana, lai palīdzētu uzlabot mēneša operētājsistēmas ielāpošanu, izmantojot klastera atteici, lai aktivizētu atjaunināto attēlu ar minimālu pārrāvumu. Atjaunināšanas lietošanas mehānisms tiek uzlabots, lai tas būtu vēl mazāk traucējošs, un tas segs gan operētājsistēmas ielāpošanu, gan kvalitātes atjauninājumu izvietošanu.

    Interaktīviem lietotājiem aktīva sesija var tikt pārtraukta, un mēģinājums tiks atkārtoti iet uz pašreiz atjaunināto vidi. Ar prioritātes balstītas [pakešuzdevumu](../../dev-itpro/sysadmin/priority-based-batch-scheduling.md) plānošanas ieviešanu, kas tagad ir pieejama izvēles pamatā, pakešveida plānošana un apstrāde atkop un atsākas tūlīt pēc atjaunināšanas. Uz prioritāti balstīta pakešuzdevumu plānošana tiks vieta debitoriem, pirms tie sāks piedalīties savā ražošanas vidē proaktīvā kvalitātes atjauninājumu sadalē.

- **Tumšas** stundas — tumšās stundas ir definētas katram Azure reģionam, un tumšajā stundu periodā tiek lietoti nulles dīkstāves atjauninājumi.

## <a name="the-proactive-update-process"></a>Proaktīvās atjaunināšanas process

Proaktīvo kvalitātes atjauninājumu izvietošana sekos drošas izvietošanas procesam (SDP). SDP specifika attīstīsies, bet kvalitātes atjauninājumi sākotnēji tiks izvietoti kastu vidēs. Šis process tiks sākts ar vidēm, kas izvēlas agrāku izvietošanu. Kad palielinās veiksmīgi izvietoto kastu procentuālā vērtība, sāks izvietot ražošanas vidēs. Šis process atkal tiks sākts ar vidēm, kas izvēlas agrāku izvietošanu. Klausības sistēmas uzraudzīs sistēmas telemārketinga un dzīves vietas incidentus un apturēs noteiktas versijas izriti, ja tiks atklāta jebkāda regresija. Ja debitori vēlas, joprojām būs iespēja izvilkt kvalitātes atjauninājumus pirms proaktīvās izvietošanas.

Pašreizējie laidiena pārvaldības dati parāda, ka kvalitātes atjauninājumos ir ieviestas mazāk nekā 3 procenti no regresijām. Kad ir palielināta fokuss uz regresijas un uzlabotās SDP likvidēšanas iespēju, regresiju potenciālā ietekme būs īpaši zemāka nekā kvalitātes ieguvumi, kas tiek sasniegti, ātrāk iegūstot klientiem plaši izvietotus labojumus.

## <a name="process-changes"></a>Apstrādāt izmaiņas

Notiek procesa izmaiņu kopa, kas apsteidz proaktīvās kvalitātes atjauninājuma izvietošanas aktivizāciju:

- **Shēma** – rīku rīks nodrošina, ka kvalitātes atjauninājumu būvējuma laikā tiek iekļautas tikai shēmu izmaiņas, kuras var tikt lietotas pakalpojuma tiešsaistes režīmā. Šī pieeja palīdzēs saglabāt iespēju pielietot atjauninājumu ar nulles dīkstāves laiku.
- **Palielināto izmaiņu** veikšana — pašlaik ir jau papildu procesa solis, lai apstiprinātu izmaiņas iekļaušanai kvalitātes atjauninājumā. Papildu darbība tiks palielināta, lai palīdzētu samazināt regresiju potenciālu. Kvalitātes atjauninājumos nav atļautas sadalīšanas izmaiņas, un palielinātais izmaiņu apraksts palīdzēs nodrošināt, ka mēs nodrošināt atbilstību šim mērķim.
- **Redzamība** – mēs nosūtīsim paziņojumus pa e-pastu un Lifecycle Services (LCS) gaidāmajiem apsteidzošo kvalitātes atjauninājumiem. Turklāt atbalsta darba grupas un incidentu potenciālie klienti būs redzamība tur, kur kvalitātes atjauninājumi ir proaktīvi izvietoti.
- **Versijas regresa –** lidojuma laikā tiks izmantots, lai grupētu visas izmaiņas proaktīvā kvalitātes atjauninājumā. Ja pēc proaktīvās izvietošanas ir nepieciešama atkāpšanās, to var veikt, izmantojot lidojuma sistēmu.
- **Slīpstlodziņa** sinhronizācijas apzīmējums — šodien mazāk nekā 20 procenti debitoru ir vairākas kastēs un viena glabāta vieta, kur versija sakrīt ar ražošanu, lai saņemtu palīdzību par problēmu novēršanas. Nākotnē mēs izsūtīsim klientiem iespēju norādīt kešlodziņa vidi, kam nevajadzētu saņemt proaktīvo kvalitātes atjauninājumu izvietošanu kopā ar citām kastēm, bet kam tā vietā jāsaņem vēlāk kopā ar ražošanas vidi. Ievērojiet, ja debitors izmanto kasti, lai pārbaudītu jaunāku ražošanas versiju, šī slīpmaksa saņems kvalitātes atjauninājumus jaunākai versijai.
- 
## <a name="when-will-proactive-quality-updates-start"></a>Kad tiks sākta proaktīvā kvalitātes atjaunināšana?

Ir paredzēts, ka proaktīvās kvalitātes atjauninājumu sadale kastu vidēm sākas vēlā septembrī vai 2022. gadā Azure publiskajiem mākoņa debitoriem. Pārbaudes vides šajā laikā arī sāks saņemt proaktīvās atjaunināšanas izvietošanu. Septembrī katram debitoram tiks nosūtīts paziņojums, lai informētu tos par paredzēto vides plānu. Proaktīvā atjauninātā sadales procesa izņēmumi būs atļauti tikai ar FDA saistīto debitoru gadījumos. Joprojām strādājam, kā tiks pārvaldītas regulējamās vides un valdības mākonī klienti.

Nākamajā sešu mēnešu periodā mēs pakāpeniski palielināsim kešlodziņa vides daļu procentos, kas saņem proaktīvos atjauninājumus, līdz visas norādītās vides ir iekļautas un turpinās atjaunināt ražošanas vides. Visa perioda laikā mēs pārraudzīsim, lai nodrošinātu, ka izvietošanas process ir efektīvi un ka mēs ieturējam mūsu mērķi - neizjaukjošas lietderīgās noslodzes.

Ņemot vērā, ka debitori regulāri saņems mazāku lietderīgo slodzi, paredzams, ka norēķinu process kļūs vienkāršāks. Tiks pielāgots atjaunināšanas biežums, kad mēs rādīsim spēju palaist procesu bez pārrāvuma. Šis process jau strādā efektīvi mūsu platformā un Dataverse lietojumprogrammās un nodrošina gaidītos pakalpojumu kvalitātes uzlabojumus. Mēs iesakām to pašu soli uz priekšu lietojumprogrammām, kas saistītas ar finansēm un operācijām.
