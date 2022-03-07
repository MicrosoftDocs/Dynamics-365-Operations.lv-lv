---
title: Drukas pārvaldības ierakstam raksturīgo ER adresātu konfigurēšana
description: Šajā tēmā ir paskaidrots, kā konfigurēt drukas pārvaldības ierakstam raksturīgus adresātus elektroniskās ziņošanas (ER) formātā, kas ir konfigurēts izejošo dokumentu ģenerēšanai.
author: NickSelin
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-08-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 1e06fafe8d8bbe92ddf4fcd94d7271a1fbb6362a
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413605"
---
# <a name="configure-print-management-record-specific-er-destinations"></a>Drukas pārvaldības ierakstam raksturīgo ER adresātu konfigurēšana

[!include [banner](../includes/banner.md)]

Šī tēma skaidro, kā lietotājs sistēmas administratora vai debitoru parādu lietveža lomā var veikt tālāk minētos uzdevumus.

- Konfigurējiet nosauktos [Elektronisko pārskatu (ER)](general-electronic-reporting.md) galamērķus ER risinājumam, kas ģenerē brīvā teksta rēķinus.
- Piešķiriet ER adresātu vienam [drukas pārvaldības](document-reporting-services.md) ierakstam.

Šīs procedūras var veikt uzņēmumā USMF. Kodēšana nav nepieciešama.

## <a name="introduction"></a>Ievads

Varat konfigurēt [adresātus](electronic-reporting-destinations.md) katrai mapei failu izvades komponentā elektroniskās ziņošanas (ER) [formāta](general-electronic-reporting.md#FormatComponentOutbound) [konfigurācijā](general-electronic-reporting.md#Configuration), kas tiek izmantota izejošā dokumenta izveidei. Izmantojot šī tipa ER formātu, ja jums ir atbilstošas piekļuves tiesības, izpildlaikā varat mainīt arī konfigurētos adresāta iestatījumus.

Microsoft Dynamics 365 Finance **10.0.17 un jaunākā versijā** darbības kodu var [iestatīt](er-apis-app10-0-17.md) ER formātam, lai norādītu darbību, kuru lietotāji izpilda, palaižot šo ER formātu. Piemēram, **Debitoru parādu** modulī drukas pārvaldības iestatījumos varat atlasīt ER formātu, kas ģenerē noteiktu biznesa dokumentu, piemēram, brīva teksta rēķinu. Pēc tam varat atlasīt **Skatīt**, lai priekšskatītu rēķinu, vai **Drukāt**, lai nosūtītu to uz printeri. Ja izpildlaikā darbība ir izpildīta ER formātam, varat [konfigurēt dažādus ER adresātus dažādām lietotāja darbībām](er-action-dependent-destinations.md).

Finance **10.0.21 un jaunākā versijā** nosauktu adresātu var [iestatīt](er-apis-app10-0-21.md) ER formātam un piešķirt drukas pārvaldības ierakstam, kas tiek apstrādāts, palaižot ER formātu. Piemēram, **Debitoru parādu** modulī drukas pārvaldības iestatījumos vēlaties konfigurēt **Oriģinālo** ierakstu, lai veiktu tālāk minētās darbības.

- Palaidiet ER formātu.
- Ģenerēto rēķinu nosūtiet debitoram pa e-pastu.
- Konfigurējiet ierakstu **Kopēt**, lai palaistu to pašu formātu.
- Drukājiet rēķina kopiju tīkla printerī.

Šajā gadījumā ER formātam, kas darbojas, ir jākonfigurē dažādi ER adresāti, un ir jāatlasa adresāti dažādiem drukas pārvaldības ierakstiem.

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms sākat, līdzeklim **Atļaut iestatīt ER adresātus katram drukas pārvaldības vienumam** jābūt ieslēgtam darbvietā [Līdzekļu pārvaldība](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace). Avota kods arī ir jāmaina, lai atļautu nosauktu ER adresātu konfigurāciju pašreizējā Finance instancē un iespējotu [jauno](er-apis-app10-0-21.md) ER API.

Turklāt **Brīva teksta rēķina (Excel)** ER konfigurācija ir [jāimportē](er-download-configurations-global-repo.md) jūsu Finance instancē.

## <a name="configure-a-new-er-destination"></a>Jauna ER adresāta konfigurēšana

1. Atveriet sadaļas **Debitoru parādi** \> **Rēķini** \> **Visi brīvā teksta rēķini**.
2. Atlasiet debitora konta **US-001** rēķinu.
3. Lapā **Brīva teksta rēķins**, cilnē **Rēķins**, grupā **Drukas pārvaldība** atlasiet **Drukas pārvaldība**.
4. Lapā **Drukas pārvaldības iestatījumi** izvērsiet vienumu **Modulis — debitoru parādi** \> **Dokumenti** \> **Brīva teksta rēķins**, atlasiet ierakstu **Oriģināls** un pēc tam veiciet tālāk minētās darbības.

    1.  Ievērojiet atlasītā ieraksta pašreizējos tālāk norādītos iestatījumus.
        -   Noklusējuma SSRS pārskats **FreeTextInvoice.Report** ir atlasīts laukā **Pārskata formāts**.
        -   Nosaukums **\<Default\>** tiek parādīts laukā **Adresāts**, kas informē, ka piešķirtajam SSRS pārskatam nav atlasīts pielāgots adresāts. 
    2.  Laukā **Pārskata formāts** atlasiet ER formta konfigurēšanu **Brīva teksta rēķins (Excel)**.
        -   Lauka **Adresāts** nosaukums ir mainīts uz **Adresāta nosaukums**.
        -   Nosaukums **\<No named destination\>** tiek parādīts laukā **Adresāta nosaukums**, informējot, ka piešķirtajam ER formātam nav atlasīts nosaukts adresāts.
    3.  Atlasiet bultiņas pogu pa labi no lauka **Adresāta nosaukums**.    
    4. Lapā **Elektroniskā pārskata nosauktais adresāts**, laukā **Nosaukums** ievadiet **Galvenais adresāts**.
    5. Atlasiet **Saglabāt**.
    6. Kopsavilkuma cilnē **Faila adresāts** [konfigurējiet](er-destination-type-email.md) adresātu **E-pasts** komponentam **Pārskats**.
    7. Aizveriet lapu **Elektronisko pārskatu nosauktais adresāts**.
    8. Lapas **Drukas pārvaldības iestatījumi** laukā **Adresāta nosaukums** atlasiet nosaukto adresātu **Galvenais adresāts**.

    ![Nosaukta ER adresāta konfigurēšana atlasītajam ER formātam un tā piešķiršana konfigurētam drukas pārvaldības ierakstam drukas pārvaldības iestatījumu lapā](./media/er-named-destinations-01.gif)

    Tagad nosauktais ER adresāts **Galvenais adresāts** formātam **Brīva teksta rēķins (Excel)** ir konfigurēts un piešķirts drukas pārvaldības ierakstam **Oriģināls** sadaļā **Modulis — debitoru parādi** \> **Dokumenti** \> **Brīva teksta rēķins**.

5. Izvērsiet **Modulis — debitoru parādi** \> **Konts — US-001** \> **Brīva teksta rēķins**, atlasiet ierakstu **Oriģināls** un pēc tam izpildiet tālāk norādītās darbības.

    1. Atlasiet un turiet (vai noklikšķiniet ar peles labo pogu) ierakstu, un pēc tam atlasiet **Pārlabot**.
    2. Atlasiet bultiņas pogu pa labi no lauka **Adresāta nosaukums**.
    3. Lapā **Elektronisko pārskatu nosauktais adresāts** darbību rūtī atlasiet **Jauns**.
    4. Laukā **Nosaukums** ievadiet **US-001 adresāts**.
    5. Kopsavilkuma cilnē **Faila adresāts** [konfigurējiet](er-destination-type-print.md) adresātu **Printeris** komponentam **Pārskats**.
    6. Aizveriet lapu **Elektronisko pārskatu nosauktais adresāts**.
    7. Lapas **Drukas pārvaldības iestatījumi** laukā **Adresāta nosaukums** atlasiet nosaukto adresātu **US-001 adresāts**.

    ![Nosaukta ER adresāta konfigurēšana atlasītajam ER formātam un tā piešķiršana konfigurētajam drukas pārvaldības ierakstam drukas pārvaldības iestatījumu lapā](./media/er-named-destinations-02.gif)

    Tagad nosauktais ER adresāts **US-001 adresāts** formātam **Brīva teksta rēķins (Excel)** ir konfigurēts un piešķirts drukas pārvaldības ierakstam **Oriģināls** sadaļā **Modulis — debitoru parādi** \> **Konts —US-001** \> **Brīva teksta rēķins**.

Tagad, kad brīva teksta rēķins ir apstrādāts, tiek palaists ER formāts **Brīva teksta rēķins (Excel)** un notiek viens no tālāk minētajiem notikumiem.

- Ja brīva teksta rēķins ir paredzēts klientam, kas nav US-001, ģenerētais dokuments tiek nosūtīts pa e-pastu.
- Ja brīva teksta rēķins ir paredzēts klientam US-001, ģenerētais dokuments tiek izdrukāts.

> [!NOTE]
> Ja nosauktais adresāts nav definēts izpildlaikā apstrādātam drukas pārvaldības ierakstam, tiek izmantoti noklusējuma ER adresāti, ja tie ir pieejami ER formātā, kas darbojas.

> [!IMPORTANT]
> Lapā **Elektronisko pārskatu adresāts** (**Organizācijas administrācija** \> **Elektronisko pārskatu veidošana** \> **Elektronisko pārskatu adresāts**), atlasot ER formātu, kuram konfigurēts vismaz viens nosauktais adresāts, tiekat informēts par nosaukto adresātu esamību.
>
> ![Paziņojums par konfigurētu nosaukto adresātu esamību atlasītajam ER formātam elektronisko pārskatu adresātu lapā](./media/er-named-destinations-03.png)
>
> Izdzēšot noklusējuma adresātu, tad tiek izdzēsti arī visi nosauktie adresāti. Ja šie nosauktie adresāti tika atlasīti drukas pārvaldības ierakstiem, šo nosaukto adresātu atlase tiek atcelta.

## <a name="copy-an-existing-er-destination-as-a-new-named-destination"></a>Esoša ER adresāta kopēšana par jaunu nosaukto adresātu

Kad noklusētais nosauktais ER adresāts ir pieejams ER formātam, to var izmantot kā veidni jauniem ER adresātiem. Lai izveidotu jaunu ER adresātu, kura pamatā ir noklusējuma adresāts, lapā **Elektronisko pārskatu nosauktais adresāts** atlasiet **Kopēt no noklusējuma**. Jaunais adresāts tiek nosaukts kā **Noklusējums**. Šo darbību var atkārtot tik daudz reižu, cik nepieciešams.

Jebkuru esošu nosaukto adresātu var atlasīt kā veidni jaunam nosauktam adresātam. Lai izveidotu jaunu nosaukto ER adresātu, kura pamatā ir atlasīts nosauktais adresāts, lapā **Elektronisko pārskatu nosauktais adresāts** atlasiet **Kopēt**. Jaunajam adresātam ir tāds pats nosaukums kā atlasītajam nosauktajam adresātam, taču tiek pievienots sufikss "Kopija". Šo darbību var atkārtot tik daudz reižu, cik nepieciešams.

## <a name="security-considerations"></a>Drošības apsvērumi

Nosauktos ER adresātus varat iestatīt lapā **Drukas pārvaldības iestatījumi** tikai tad, ja jums ir [atļauja](../sysadmin/role-based-security.md#permissions) veikt šo uzdevumu. Atļauju jums var piešķirt, ja **Elektronisko pārskatu formāta adresāta konfigurēšanas** [pienākums](../sysadmin/role-based-security.md#duties) ir piešķirts kādai no jūsu [drošības lomām](../sysadmin/role-based-security.md#security-roles). Papildinformāciju skatiet sadaļā [Drošības apsvērumi](electronic-reporting-destinations.md#security-considerations).

## <a name="additional-resources"></a>Papildu resursi

[Elektronisko pārskatu veidošanas (ER) apskats](general-electronic-reporting.md)

[Elektroniskās pārskatu veidošanas (ER) adresāti](electronic-reporting-destinations.md)

[Elektronisko atskaišu veidošanas struktūras API izmaiņas atjauninājumam Application update 10.0.17](er-apis-app10-0-17.md)

[Elektronisko atskaišu veidošanas struktūras API izmaiņas atjauninājumam Application update 10.0.21](er-apis-app10-0-21.md)

[Mainīt kodu, lai dotu lietotājiem iespēju konfigurēt un izmantot nosauktos ER adresātus](er-api-named-destinations.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
