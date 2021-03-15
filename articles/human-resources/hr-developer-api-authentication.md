---
title: Autentifikācija
description: Šajā rakstā ir sniegta informācija par to, kā autentificēties Microsoft Dynamics 365 Human Resources datu programmu programmēšanas interfeisā (API).
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 963bec2b817c59e3b5860c5ff5885e165ec8656a
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115564"
---
# <a name="authentication"></a>Autentifikācija

Šajā rakstā ir sniegta informācija par to, kā autentificēties Microsoft Dynamics 365 Human Resources datu programmu programmēšanas interfeisā (API).

## <a name="overview"></a>Pārskats

Personāla vadības datu API ir OData ieviešana. Papildinformāciju skatiet šeit: [Atvērto datu protokols (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).

Jūsu pieteikumam ir jābūt autentificētam kā autorizētam zvanītājam, pirms API apkalpos pieprasījumus no jūsu pieteikumu.

## <a name="fundamentals"></a>Pamati

Lai izsauktu datu API, jūsu pieteikumam ir jāiegūst piekļuves marķieris no Microsoft identitātes platformas. Piekļuves marķieris satur informāciju par jūsu pieteikumu un atļauju, kurai tai ir, lai zvanītu personāla vadības resursiem.

### <a name="access-token"></a>Piekļuves marķieris

Microsoft identitātes platformas izsniegtie piekļuves marķieri ir base64 kodēti JavaScript objekta notācijas (JSON) tīmekļa marķieri (JWT). Tajos ir ietverta informācija (apgalvojumi), kuru datu API (un citi tīmekļa API, ko aizsargā Microsoft identitātes platforma) izmanto, lai apstiprinātu zvanītāju un pārliecinātos, ka zvanītājam ir atbilstošas atļaujas, lai veiktu pieprasīto operāciju. Zvanu laikā varat apstrādāt piekļuves marķierus kā necaurredzamus. Vienmēr vajadzētu pārraidīt piekļuves marķierus, izmantojot drošu kanālu, piemēram, transportēšanas slāņa drošību (TLS) un hiperteksta pārsūtīšanas protokolu (HTTPS).

Šajā piemērā ir parādīts piekļuves marķieris, ko izsniegusi Microsoft identitātes platforma.

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

Lai izsauktu datu API, jums ir jāpievieno piekļuves marķieris kā datu nesēja marķieris autorizācijas virsrakstam HTTP pieprasījumā. Tālāk ir minēts piemērs.

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a>REģistrējiet jaunu pieteikumu, izmantojot Azure portālu

1. Piesakieties [Microsoft Azure portālā](https://portal.azure.com) ar darba vai skolas kontu vai personīgu Microsoft kontu.

2. Ja jūsu konts sniedz piekļuvi vairāk nekā vienam nomniekam, izvēlieties savu kontu augšējā labajā stūrī un iestatiet savu portāla sesiju uz Azure Active Directory (Azure AD) nomnieku, kuru vēlaties izmantot.

3. Kreisajā rūtī atlasiet **Azure Active Directory** pakalpojumu un pēc tam atlasiet **Pieteikumu reģistrācijas \>Jauna reģistrācija**.

4. Kad parādās lapa **Reģistrēt pieteikumu**, ievadiet savu pieteikuma reģistrācijas informāciju:

    - **Nosaukums**: Ievadiet jēgpilnu pieteikuma nosaukumu, kas tiks rādīts programmas lietotājiem.
    - **Atbalstītie kontu veidi**: Atlasiet kontu tipus, kurus jūsu programmai vajadzētu atbalstīt.

        | Atbalstītie kontu veidi | Apraksts |
        |-------------------------|-------------|
        | Tikai šajā organizatoriskajā direktorijā iekļautie konti | Atlasiet šo opciju, ja veidojat biznesa programmu. Šī opcija nav pieejama, ja nereģistrējat programmu direktorijā.<p>Šī opcija ir kartēta **Azure AD tikai vienam nomniekam**.</p><p>Šī opcija ir noklusējuma opcija, izņemot tad, ja reģistrējat programmu ārpus direktorija. Šādā gadījumā noklusētā opcija ir **Azure AD vairāku nomnieku un personīgais Microsoft konts**.</p> |
        | Jebkurā organizatoriskajā direktorijā iekļautie konti | Atlasiet šo opciju, lai adresētu visus biznesa un izglītības klientus.<p>Šī opcija ir kartēta **Azure AD tikai vairākiem nomniekiem**.</p><p>Ja reģistrējāt programmu kā **Azure AD tikai vienam nomniekam**, varat izmantot **Autentifikācijas** disku, lai to atjauninātu uz **Azure AD tikai vairākiem nomniekiem** un pēc tam atgrieztos **Azure AD tikai vienam nomniekam**.</p> |
        | Konti jebkurā organizācijas direktorijā un personiskajā Microsoft kontā | Atlasiet šo opciju, lai sasniegtu visplašāko klientu kopu.<p>Šī opcija ir kartēta uz **Azure AD vairāku nomnieku un personīgais Microsoft konts**.</p><p>Ja reģistrējāt programmu kā **Azure AD vairāku nomnieku un personīgie Microsoft konti**, šo iestatījumu nevar mainīt lietotāja interfeisā (UI). Tā vietā ir jāizmanto pieteikuma manifesta redaktors, lai mainītu atbalstītos kontu tipus.</p> |

    - **Novirzīt URI (nav obligāti)** — atlasiet veidojamās programmas tipu: **Tīmekļa** vai **Publiskais klients (mobilā un datora)**. Pēc tam ievadiet programmas novirzīšanas URI (vai atbildes vietrādi URL).

        - Tīmekļa lietotnēm norādiet programmas bāzes vietrādi URL. Piemēram, `http://localhost:31544`var būt tīmekļa programmas vietrādis URL, kas tiek palaists lokālajā datorā. Pēc tam lietotāji izmanto šo vietrādi URL, lai pieteiktos tīmekļa klienta programmā.
        - Publiskajām klientu lietotnēm norādiet URI, kuras Azure AD izmanto, lai atgrieztu marķiera atbildes. Ievadiet vērtību, kas ir konkrēta jūsu programmai, piemēram,`myapp://auth`.

        Lai skatītu konkrētus piemērus tīmekļa programmām vai vietējām programmām, iesākumam skatiet [Microsoft identitātes platforma (iepriekš Azure Active Directory izstrādātājiem)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).

5. Sadaļā **API atļaujas** atlasiet **Pievienot atļauju**. Pēc tam cilnē **API, kurus izmanto mana organizācija** meklējiet **Dynamics 365 Human Resources** un pievienojiet **user\_impersonation** atļauju savai programmai. Personāla vadības pieteikuma ID ir f9be0c49-aa22-4ec6-911a-c5da515226ff. Lietojiet šo ID, lai nodrošinātu, ka esat izvēlējies pareizo pieteikumu.

6. Atlasiet **Reģistrēt**.

   [![Jaunas programmas reģistrēšana Azure portālā](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)

Azure AD piešķir jūsu programmai unikālu pieteikuma ID (klienta ID) un aizved jūs uz jūsu programmas **Pārskata** lapu. Lai savai programmai pievienotu vairāk iespēju, varat izvēlēties citas konfigurācijas opcijas, piemēram, opcijas zīmolradei un sertifikātiem un slepenajām vērtībām.

## <a name="retrieving-an-access-token"></a>Piekļuves marķiera izgūšana

Dati par to, kā tiek izgūts piekļuves marķieris, lai izsauktu personāla vadības datu API, būs atkarīgi no tā, kādas tehnoloģijas izmantojat, lai izstrādātu savu klientu programmu. Piemēram, jūs varētu [testēt ar trešās puses utilītu](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (piemēram, Postman), izstrādājot C# konsoles programmu vai tīmekļa pakalpojumu vai veidojot JavaScript/TypeScript klientu.

Piemērs C# klienta pieteikumam:
```C#
using System;
using System.Net.Http;
using System.Threading.Tasks;

// requires appropriate NuGet package references in the project
using Microsoft.IdentityModel.Clients.ActiveDirectory;

namespace TalentODataPoC
{
    class Program
    {
        // prereq: This client app must be registered in Azure Active Directory. The app must be
        // registered as requiring permission to the Dynamics 365 for Talent API (with the Dynamics
        // HCM Workload delegated permission).
        static string clientId = "4fc703ef-672c-4e2c-813f-2f9d29d726db"; // This value should be obtained from AAD and must match your registered app
        static string talentNamespaceUri = "";

        public static async Task CallTalentODataService()
        {
            // authority URI
            UriBuilder uri = new UriBuilder("https://login.microsoftonline.com/common");
            AuthenticationContext authenticationContext = new AuthenticationContext(uri.ToString());

            // request token for the resource we want to access (Human Resources). This will authenticate
            // the user and return an access token containing claims for the authenticated user.
            var authResult = await authenticationContext.AcquireTokenAsync(
                "http://hr.talent.dynamics.com", /*Talent app id or resource URI*/
                clientId, /*registered client app id*/
                new Uri("https://localhost"), /*redirect URI, as registered in your AAD app*/
                new PlatformParameters(PromptBehavior.SelectAccount));

            // create the authorization header, which needs to be passed in the Header of the HTTP Requests to Talent
            string authHeader = authResult.CreateAuthorizationHeader();

            // HINT: paste the JWT into https://jwt.ms to decode and view it
            Console.Write("authHeader: ");
            Console.WriteLine(authHeader);
            Console.WriteLine();

            HttpClient client = new HttpClient();
            client.DefaultRequestHeaders.Add("Authorization", authHeader);

            string s;

            Console.Write("Talent Namespace URI: ");
            Console.WriteLine(talentNamespaceUri);
            Console.WriteLine();

            // call the OData service to get JobType data from Talent
            var resultOdata = await client.GetAsync(talentNamespaceUri + "data/JobTypes");
            s = await resultOdata.Content.ReadAsStringAsync();
            Console.WriteLine(s);
            Console.WriteLine();
        }

        static void Main(string[] args)
        {
            Console.WriteLine();

            // if the user passes in a single parameter, assume it is the namespaceUri for Talent
            if (args.Length == 1)
            {
                talentNamespaceUri = args[0];
            } else if (args.Length == 0)
            {
                Console.WriteLine("Enter Talent URL including namespace.");
                Console.WriteLine("Example: https://aos-rts-sf-21454f9d830-prod-westus2.hr.talent.dynamics.com/namespaces/2328af1a-2d45-4c6a-99e3-12a4c3867dcf/");
                Console.Write("> ");
                talentNamespaceUri = Console.ReadLine();
                if (!talentNamespaceUri.EndsWith("/"))
                {
                    talentNamespaceUri = talentNamespaceUri + "/";
                }
            } else
            {
                Console.WriteLine("Unexpected Arguments");
                System.Environment.Exit(1);
            }

            Task t = Program.CallTalentODataService();
            t.Wait();
        }
    }
}
```

Kad esat izguvis piekļuves tiesības, marķieris tiks nodots autorizācijas galvenē kā datu nesēja marķieris ar katru pieprasījumu, ko nosūtāt datu API, kā aprakstīts iepriekš.


[!INCLUDE[footer-include](../includes/footer-banner.md)]