---
title: Common Data Service virtuālo elementu konfigurēšana
description: Šajā tēmā parādīts, kā konfigurēt virtuālos elementus Dynamics 365 Human Resources. Ģenerējiet un atjauniniet esošos virtuālos elementus un analizējiet ģenerētos un pieejamos elementus.
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2b590faeab600d04c9d5303693ec1e9ac682250d
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645605"
---
# <a name="configure-common-data-service-virtual-entities"></a>Common Data Service virtuālo elementu konfigurēšana

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Human Resources ir virtuālais datu avots platformā Common Data Service. Tas nodrošina pilnīgas izveides, lasīšanas, atjaunināšanas un dzēšanas (CRUD) operācijas no Common Data Service un Microsoft Power Platform. Dati virtuālajiem elementiem netiek saglabāti Common Data Service, bet gan lietojumprogrammas datu bāzē. 

Lai iespējotu CRUD operācijas personāla vadības elementos no Common Data Service, jums jāpadara šos elementus pieejamus kā virtuālus elementus Common Data Service. Tas ļauj veikt CRUD operācijas no Common Data Service un Microsoft Power Platform personāla vadības datos. Operācijas atbalsta arī pilnas biznesa loģikas personāla vadības pārbaudes, lai nodrošinātu datu integritāti, rakstot datus elementos.

## <a name="available-virtual-entities-for-human-resources"></a>Pieejamie virtuālie elementi personāla vadībai

Visi atvērtie datu protokola (OData) elementi personāla vadībā ir pieejami kā virtuālie elementi Common Data Service. Tie ir pieejami arī Power Platform. Tagad varat veidot lietojumprogrammas un pieredzi ar datiem tieši no personāla vadības ar pilnām CRUD iespējām, nekopējot vai nesinhronizējot datus ar Common Data Service. Varat izmantot Power Apps portālus, lai veidotu tīmekļa vietnes ar ārējo piekļuvi, kas iespējo sadarbības scenārijus biznesa procesiem personāla vadībā.

Varat apskatīt vidē iespējoto virtuālo elementu sarakstu un sākt darbu ar elementiem pakalpojumā [Power Apps](https://make.powerapps.com), **Dynamics 365 HR Virtual Entity** risinājumā.

![Dynamics 365 HR Virtual Entity pakalpojumā Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a>Virtuālie elementi salīdzinājumā ar fiziskām personām

Virtuālie personāla vadības elementi atšķiras no fiziskajām personām Common Data Service, kas veidotas personāla vadības vajadzībām. Fiziskās personas personāla vadības vajadzībām tiek veidotas atsevišķi un uzturētas kopējā HCM risinājumā Common Data Service. Fizisku personu gadījumā dati tiek saglabāti Common Data Service un tiem nepieciešama sinhronizācija ar personāla vadības lietojumprogrammas datu bāzi.

> [!NOTE]
> Fizisko personu sarakstu Common Data Service personāla vadības vajadzībām skatiet [Common Data Service elementi](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).

## <a name="setup"></a>Iestatīt

Sekojiet šīm iestatīšanas darbībām, lai iespējotu virtuālos elementus jūsu vidē.

### <a name="enable-virtual-entities-in-human-resources"></a>Iespējot virtuālos elementus Personāla vadībā

Vispirms **Funkciju pārvaldības** darbvietā ir jāiespējo virtuālas entītijas.

1. Human Resources atlasiet **Sistēmas administrēšana**.

2. Atlasiet elementu **Funkciju pārvaldība**.

3. Atlasiet **Virtuālā elementa atbalsts HR/CD** un pēc tam atlasiet **Iespējot**.

Lai iegūtu papildinformāciju par priekšskatījuma līdzekļu iespējošanu un atspējošanu, skatiet sadaļu [Līdzekļu pārvaldība](hr-admin-manage-features.md).

### <a name="register-the-app-in-microsoft-azure"></a>Lietojumprogrammas reģistrēšana Microsoft Azure

Vispirms jūsu Personāla vadības instance ir jāreģistrē Azure portālā, lai Microsoft Identity platforma var nodrošināt autentifikāciju un autorizācijas pakalpojumus lietojumprogrammai un lietotājiem. Lai iegūtu vairāk informācijas par lietojumprogrammu reģistrāciju Azure, skatiet [Īsa pamācība: lietojumprogrammas reģistrēšana platformā Microsoft Identity](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).

1. Atveriet [Microsoft Azure portālu](https://portal.azure.com).

2. Azure pakalpojumu sarakstā atlasiet **Lietojumprogrammu reģistrācijas**.

3. Atlasiet **Jauna reģistrācija**.

4. Laukā **Nosaukums** ievadiet aprakstošu lietojumprogrammas nosaukumu. Piemēram, **Dynamics 365 Human Resources virtuālie elementi**.

5. **Novirzīšanas URI** laukā ievadiet savas personāla vadības instances nosaukumvietas URL.

6. Atlasiet **Reģistrēt**.

7. Kad reģistrācija pabeigta, Azure portālā tiek parādīta lietojumprogrammas reģistrācijas **pārskata** rūts, kurā ir ietverts tās **lietojumprogrammas (klienta) ID**. Pašlaik ņemiet vērā **lietojumprogrammas (klienta) ID**. Jūs ievadīsiet šo informāciju, kad [konfigurēsiet virtuālā elementa datu avotu](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).

8. Kreisajā navigācijas rūtī atlasiet **sertifikāti un noslēpumi**.

9. Lapas sadaļā **Klienta noslēpumi** atlasiet **Jauns klienta noslēpums**.

10. Ievadiet aprakstu, atlasiet ilgumu un atlasiet **Pievienot**.

11. Reģistrējiet noslēpuma vērtību. Jūs ievadīsiet šo informāciju, kad [konfigurēsiet virtuālā elementa datu avotu](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).

    > [!IMPORTANT]
    > Pārliecinieties, ka ņemat vērā pašreizējo noslēpuma vērtību. Pēc iziešanas no šīs lapas noslēpums nekad vairs netiek parādīts.

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a>Dynamics 365 HR Virtual Entity lietojumprogrammas instalēšana

Instalējiet Dynamics 365 HR Virtual Entity lietojumprogrammu jūsu Power Apps vidē, lai izvietotu virtuālos elementu risinājuma pakotni Common Data Service.

1. Atveriet [Power Platform administrēšanas centru](https://admin.powerplatform.microsoft.com).

2. Sarakstā **Vides** atlasiet ar jūsu personāla vadības instanci saistīto Power Apps vidi.

3. Lapas sadaļā **Resursi** atlasiet **Dynamics 365 lietojumprogrammas**.

4. Atlasiet darbību **Lietojumprogrammas instalēšana**.

5. Atlasiet **Dynamics 365 HR Virtual Entity** un atlasiet **Tālāk**.

6. Pārskatiet un atzīmējiet, ka piekrītat pakalpojuma nosacījumiem.

7. Atlasiet **Instalēt**.

Instalācija aizņem dažas minūtes. Kad tā ir pabeigta, pārejiet pie nākamajām darbībām.

![Dynamics 365 HR Virtual Entity lietojumprogrammas instalēšana no Power Platform administrēšanas centra](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a>Virtuālo elementu datu avota konfigurēšana 

Nākamais solis ir konfigurēt virtuālā elementa datu avotu Power Apps vidē. 

1. Atveriet [Power Platform administrēšanas centru](https://admin.powerplatform.microsoft.com).

2. Sarakstā **Vides** atlasiet ar jūsu personāla vadības instanci saistīto Power Apps vidi.

3. Atlasiet **Vides URL** lapas sadaļā **Detalizēti**.

4. **Risinājumu darbspējas centrmezglā** atlasiet ikonu **Detalizētā atrašana** lietojumprogrammas lapas augšējā labajā stūrī.

5. Lapā **Detalizētā atrašana**, nolaižamajā sarakstā **Meklēt** atlasiet **Finance and Operations virtuālo datu avotu konfigurācijas**.

6. Atlasiet **Rezultāti**.

7. Atlasiet ierakstu **Microsoft HR datu avots**.

8. Ievadiet nepieciešamo informāciju par datu avota konfigurāciju:

   - **Mērķa URL**: jūsu personāla vadības nosaukumvietas URL. Mērķa URL formāts ir:
     
     https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/

     Piemēram:
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     >Noteikti iekļaujiet rakstzīmi "**/**" vietrāža URL beigās, lai izvairītos no kļūdas saņemšanas.

   - **Nomnieka ID**: Azure Active Directory (Azure AD) nomnieka ID.

   - **AAD lietojumprogrammas ID**: lietojumprogrammas (klienta) ID, kas izveidots Microsoft Azure portālā reģistrētai lietojumprogrammai. Jūs saņēmāt šo informāciju iepriekš, veicot darbību [Lietojumprogrammas reģistrēšana Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).

   - **AAD lietojumprogrammas noslēpums**: klienta noslēpums, kas izveidots Microsoft Azure portālā reģistrētai lietojumprogrammai. Jūs saņēmāt šo informāciju iepriekš, veicot darbību [Lietojumprogrammas reģistrēšana Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).

   ![Microsoft HR datu avots](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. Atlasiet **Saglabāt un aizvērt**.

### <a name="grant-app-permissions-in-human-resources"></a>Piešķiriet lietojumprogrammas atļaujas personāla vadībā

Piešķiriet atļaujas abām Azure AD lietojumprogrammām personāla vadībā:

- Lietojumprogramma, kas izveidota jūsu nomniekam Microsoft Azure portālā
- Dynamics 365 HR Virtual Entity lietojumprogramma, kas instalēta Power Apps vidē 

1. Personāla vadībā atveriet **Azure Active Directory lietojumprogrammu** lapu.

2. Atlasiet **Jauns**, lai izveidotu jaunu lietojumprogrammas ierakstu:

    - Laukā **Klienta ID**, ievadiet Microsoft Azure portālā reģistrētās lietojumprogrammas klienta ID.
    - Laukā **Nosaukums** ievadiet Microsoft Azure portālā reģistrētās lietojumprogrammas nosaukumu.
    - Laukā **Lietotāja ID** atlasiet tā lietotāja ID, kam ir administratora atļaujas personāla vadībā un Power Apps vidē.

3. Atlasiet **Jauns**, lai izveidotu otru lietojumprogrammas ierakstu:

    - **Klienta Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff
    - **Nosaukums**: Dynamics 365 HR Virtual Entity
    - Laukā **Lietotāja ID** atlasiet tā lietotāja ID, kam ir administratora atļaujas personāla vadībā un Power Apps vidē.

## <a name="generate-virtual-entities"></a>Virtuālo elementu ģenerēšana

Kad iestatīšana ir pabeigta, varat atlasīt virtuālos elementus, kurus vēlaties ģenerēt un iespējot savā Common Data Service instancē.

1. Human Resources atveriet lapu **Common Data Service (CDS) integrācija**.

2. Atlasiet cilni **Virtuālie elementi**.

> [!NOTE]
> Kad visa nepieciešamā uzstādīšana būs pabeigta, slēdzis **Iespējot virtuālo elementu** automātiski tiks iestatīts uz **Jā**. Ja slēdzis tiek iestatīts uz **Nē**, pārskatiet šā dokumenta iepriekšējās sadaļās norādītās darbības, lai nodrošinātu, ka visi priekšnosacījumu iestatīšana ir pabeigta.

3. Atlasiet elementu vai elementus, kurus vēlaties ģenerēt pakalpojumā Common Data Service.

4. Atlasiet **Ģenerēt/atsvaidzināt**.

![Common Data Service integrācija](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-entity-generation-status"></a>Elementa ģenerēšanas statusa pārbaude

Virtuālie elementi pakalpojumā Common Data Service tiek ģenerēti, izmantojot asinhronu fona procesu. Procesa atjauninājumi tiek parādīti darbību centrā. Detalizēta informācija par procesu, ieskaitot kļūdu žurnālus, tiek parādīta lapā **Procesa automatizācija**.

1. Programmā Human Resources atveriet lapu **Procesa automatizācija**.

2. Atlasiet cilni **Fona procesi**.

3. Atlasiet **Virtuālo elementu kopuma asinhronās darbības fona process**.

4. Atlasiet **Skatīt pēdējos rezultātus**.

Nolaižamā saraksta rūtī tiek rādīti pēdējie procesa izpildes rezultāti. Varat skatīt procesa žurnālu, tostarp visas kļūdas, kas atgrieztas no pakalpojuma Common Data Service.

## <a name="see-also"></a>Skatiet arī

[Kas ir Common Data Service?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[Elementu pārskats](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[Elementu attiecību pārskats](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[Izveidot un rediģēt virtuālos elementus, kas satur datus no ārējo datu avota](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[Kas ir Power Apps portāli?](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[Lietojumprogrammu izveides pārskats Power Apps](https://docs.microsoft.com/powerapps/maker/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]