---
title: Darbs ar fragmentiem
description: Šajā tēmā aprakstīts, kāpēc, kad un kā izmantot fragmentus programmā Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 017cdc76368ae4f80131471a289aa03ab06c99bf
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6350212"
---
# <a name="work-with-fragments"></a>Darbs ar fragmentiem 

[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīts, kāpēc, kad un kā izmantot fragmentus programmā Microsoft Dynamics 365 Commerce.

Fragmenti ļauj izveidot centralizētu autorēšanas pieredzi moduļa konfigurācijām, kas atkārtoti jāizmanto visā jūsu vietnē. Piemēram, galvenes, kājenes un reklāmkarogi bieži tiek konfigurēti kā fragmenti, jo tie tiek koplietoti vairākās lapās. Fragmentus varat iedomāties kā miniatūras tīmekļa lapas, kuras var ievietot citās vietnes lapās. Fragmentiem ir savs dzīves cikls. Citiem vārdiem, tie tiek izveidoti, pieminēti, atjaunināti un dzēsti kā neatkarīgi elementi autorēšanas rīkos.

Pēc tam, kad fragmenti ir konfigurēti, tos var izmantot visur, kur var izmantot moduļus vietnes struktūrā. Uz fragmentiem var atsaukties lapās, izkārtojumos, veidnēs un citos fragmentos.

> [!NOTE]
> Fragmentus var ligzdot līdz septiņu līmeņu dziļumam citu fragmentu iekšpusē.

Piemēram, ja jūs vēlaties veicināt sezonas notikumu vairākās lapās mūsu vietnē, varat izmantot fragmentu. Pirmais solis jauna fragmenta radīšanas procesā ir atlasīt moduļa tipu, no kura vēlaties sākt. Šim piemēram jūs varat izveidot fragmentu no centrālā moduļa.

> [!NOTE]
> Fragmentus var izveidot no jebkura moduļa tipa.

Pēc tam varat konfigurēt centrālo fragmentu ar savu īpašo veicināšanas saturu. Varat arī lokalizēt to, ja nepieciešams. Pēc tam jaunais atsevišķais centrālais fragments var tikt patērēts kā iepriekš konfigurēts modulis visā jūsu vietnē. Varat viegli pievienot to veidnēm, noteiktām lapām vai citiem fragmentiem, kas var saturēt centrālos moduļus.

Visas vietas, kur šis fragments tiek pievienots, ir atsauces uz jūsu izveidoto centrālo fragmentu. Publicējot izmaiņas fragmentā, šīs izmaiņas nekavējoties tiek atspoguļotas visās vietās, kur vietnē ir atsauce uz fragmentu. Tāpēc fragmenti nodrošina spēcīgu un efektīvu veidu, kā atkārtoti izmantot un centralizēti pārvaldīt moduļu konfigurācijas vietnē. Efektīvi izmantojot tos, varat būtiski paaugstināt dinamiskumu un samazināt izmaksas, kas saistītas ar vietnes satura pārvaldību.

Tālāk esošajā attēlā ir parādīts, kā fragmentus var izmantot, lai centralizētu koplietota moduļa konfigurāciju autorēšanu e-komercijas vietnē.

![Attēlā ir parādīts, kā fragmentus var izmantot, lai centralizētu koplietota moduļa konfigurāciju autorēšanu e-komercijas vietnē.](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a>Fragmenta izveidošana

Varat izveidot jaunu fragmentu vai saglabāt esošu moduļa konfigurāciju kā fragmentu.

### <a name="save-an-existing-module-configuration-as-a-fragment"></a>Esošas moduļa konfigurācijas kā fragmenta saglabāšana

Lai konvertētu iepriekš konfigurētu moduli par atkārtoti izmantojamu fragmentu Commerce vietņu veidotājā, rīkojieties, kā norādīts tālāk.

1. Atveriet lapu vai veidni, kas satur moduli, ko vēlaties pārveidot par fragmentu.
1. Strukturējuma rūtī pa kreisi vai tieši vizuālo lapu veidotājā atlasiet iepriekš konfigurēto moduli.
1. Atlasiet daudzpunkti (**...**) blakus moduļa nosaukumam vai nu strukturējuma rūtī, vai atlasītā moduļa rīkjoslā vizuālo lapu veidotājā. 
1. Atlasiet **Koplietot kā fragmentu**. 
1. Dialoglodziņā **Saglabāt kā fragmentu** ievadiet fragmenta nosaukumu.
1. Atlasiet **Labi**, lai saglabātu moduļa konfigurāciju kā fragmentu, ko var pievienot citām lapām.
<!-- The following image shows how to save a module configuration as a fragment.-->
<!--![A screen capture of how to save a module configuration as a fragment.](./media/save-as-fragment.png)-->

### <a name="create-a-new-fragment"></a>Izveidot jaunu fragmentu

Lai izveidotu jaunu fragmentu Commerce vietņu veidotājā, izpildiet tālāk norādītās darbības.

1. Navigācijas rūtī kreisajā pusē atlasiet **Fragmenti**.
1. Atlasiet **Jauns**. Tiek parādīts dialoglodziņš **Jauns fragments**, kurā redzami visi pieejamie moduļa veidi. Kā jau tika minēts iepriekš, fragmentus var izveidot no jebkura moduļa tipa.
1. Atlasiet sava fragmenta moduļa veidu.

<!-- The following image shows where to create a new fragment.-->
<!-- ![A screen capture of where to create a new fragment.](./media/fragment-nav-menu.png)-->
> [!TIP]
> Atlasot vispārīgā konteinera moduļa tipu, jūs iegūstat augstāko elastību, kad vēlāk ir jāatjaunina un jākonfigurē jūsu fragments.

## <a name="add-remove-or-edit-fragments-on-a-page"></a>Fragmentu pievienošana, noņemšana vai rediģēšana lapā

Šīs procedūras apraksta, kā pievienot, noņemt vai rediģēt fragmentus.

### <a name="add-a-fragment"></a>Fragmenta pievienošana

Lai pievienotu fragmentu lapai Commerce vietņu veidotājā, izpildiet tālāk norādītās darbības.

1. Strukturējuma rūtī pa kreisi vai tieši vizuālo lapu veidotājā atlasiet konteineru vai slotu, kuram var pievienot atvašu moduļus.
1. Atlasiet daudzpunkti (**...**) blakus konteinera nosaukumam vai slotam.  Vai arī, ja izmantojat vizuālo lapu veidotāju, atlasiet plus zīmi (**+**).  
1. Atlasiet **Pievienot fragmentu**.
    <!-- ![A screen capture of how to add an existing fragment to a slot or container.](./media/add-fragment.png)-->
 
    > [!NOTE]
    > Ja konteiners vai slots neatbalsta jaunus atvašu moduļus, opcija **Pievienot fragmentu** nav pieejama.
    
1. Dialoglodziņā **Atlasīt fragmentu** meklējiet un atlasiet pievienojamo fragmentu. Ja pieejamo fragmentu sarakstā nav neviena fragmenta, iespējams, vispirms ir jāizveido fragments no moduļa tipa, ko atbalsta atlasītais konteiners vai slots.
1. Atlasiet vēlamo fragmentu, kuru pievienot konteineram vai slotam jūsu lapā.
<!--    ![A screen capture of the fragment picker modal window.](./media/fragment-picker.png)-->

> [!NOTE]
> Moduļi, kas ir atļauti konteinerā vai slotā, tiek definēti ar lapas veidni vai pašu moduļu definīcijām.

### <a name="remove-a-fragment"></a>Fragmenta noņemšana

Lai izņemtu fragmentu no slota vai konteinera lapā Commerce vietņu veidotājs, veiciet tālāk norādītās darbības.

1. Struktūras rūtī pa kreisi izvēlieties daudzpunktes (**...**) pogu, kas atrodas blakus fragmenta nosaukumam, lai noņemtu, un pēc tam atlasiet Miskastes simbolu.  Vai arī varat atlasīt fragmentu vizuālo lapu veidotājā un atlasīt atkritnes simbolu fragmentu rīkjoslā.
1. Kad tiek parādīta uzvedne, lai apstiprinātu, ka vēlaties noņemt fragmentu, atlasiet **Labi**.

> [!NOTE]
> Noņemot fragmentu no lapas, jūs vienkārši noņemat atsauci no tā šajā lapā. **Netiek** dzēsts fragments no jūsu vietnes. Lai dzēstu fragmentus no jūsu vietnes, jāizmanto fragmenta kontroliera lietotāja interfeiss (UI). Fragmentus no vietnes vara izdzēst tikai tad, ja neviena lapā, veidnēs vai citos fragmentos uz tiem nav atsauču.

### <a name="edit-a-fragment"></a>Fragmenta rediģēšana

Lai rediģētu fragmentus, jāizmanto fragmentu redaktora lietotāja interfeiss. Šis ierobežojums ir izstrādāts. Tas palīdz nodrošināt, ka autori nejauc moduļu rediģēšanas procesu konkrētai lappusei ar to fragmentu rediģēšanas procesu, kurus var koplietot daudzās lapās.

Lai rediģētu fragmentu Commerce vietņu veidotājā, izpildiet tālāk norādītās darbības.

1. Navigācijas rūtī kreisajā pusē atlasiet **Fragmenti**.
1. Sadaļā **Fragmenti** atlasiet rediģējamo fragmentu.
1. Rediģējiet fragmenta moduļa rekvizītus un struktūru, kā nepieciešams. Šis process līdzinās moduļu rediģēšanas procesam, kas tiek veikts lapas redaktora skatā.

Fragmentu var arī rediģēt, atlasot to lapā, veidnē vai pamata fragmentā un pēc tam labajā pusē rekvizītu rūtī atlasot opciju **Rediģēt fragmentu**.

## <a name="additional-resources"></a>Papildu resursi

[Pārskats par veidnēm un izkārtojumiem](templates-layouts-overview.md)

[Darbs ar veidnēm](work-with-templates.md)

[Darbs ar iepriekš iestatītiem izkārtojumiem](work-with-layouts.md)

[Darbs ar publicēšanas grupām](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
