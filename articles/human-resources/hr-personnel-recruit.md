---
title: Personāla atlases kandidāti
description: Šajā tēmā ir parādīts, kā pieņemt kandidātus darbā risinājumā Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 12/03/2020
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
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9a35abcb8a2f6aa8031c8d84a44c2a8ad93883ac
ms.sourcegitcommit: 0354ca7e566fbd2eb0aabdd40000d4ac5c44ea78
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/04/2020
ms.locfileid: "4669179"
---
# <a name="recruit-job-candidates"></a>Personāla atlases kandidāti

[!include [banner](includes/preview-feature.md)]

Dynamics 365 Human Resources palīdz pārvaldīt personāla atlases pieprasījumus. Tas palīdz arī netraucēti pāriet no kandidātiem uz darbiniekiem. Ja jūsu uzņēmums izmanto atsevišķu personāla atlases programmu, personāla atlases process var ietvert šādas darbības:

- Ievadiet darbinieku atlases pieprasījumu Personāla vadībā.
- Saņemt kandidātu nosūtījumus Personāla vadībā no personāla atlases programmas.
- Pabeigt kandidātu apstiprināšanas procesu Personāla vadībā.

Ja neizmantojat atsevišķu personāla atlases programmu, varat arī manuāli pārvaldīt kandidātus Personāla vadībā.

>[!NOTE]
>Ja jūs esat administrators vai izstrādātājs un vēlaties integrēt Personāla vadību, izmantojot trešās puses personāla atlases programmu, skatiet [Konfigurēt Common Data Service integrāciju](hr-admin-integration-common-data-service.md) un [Konfigurēt Common Data Service virtuālos elementus](hr-admin-integration-common-data-service-virtual-entities.md)
>
> Varat arī atrast darbā pieņemšanas integrācijas programmas [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).
>
> Lai izmēģinātu mūsu priekšskatījuma līdzekli integrēšanai ar LinkedIn Talent Hub, skatiet sadaļu [Integrēt ar LinkedIn Talent Hub](hr-admin-integration-linkedin.md).

## <a name="enable-recruiting-requests"></a>Iespējot personāla atlases pieprasījumus

Ja vēlaties iesniegt darbā pieņemšanas pieprasījumus Personāla vadībā, vispirms ir jāaktivizē funkcionalitāte **Personāla vadības parametros**.

1. Darbvietā **Personāla vadība** atlasiet **Saites**.

2. Sadaļā **Iestatījumi** atlasiet **Personāla vadības parametri**.

3. Cilnē **Vispārīgi** sadaļā **Personāla atlase** iestatiet **Iespējot personāla atlases pieprasījumus** uz **Jā**.

   ![Iespējot personāla atlases pieprasījumus](./media/hr-recruit-0-enable-requests.png)

## <a name="add-a-recruiting-request-location"></a>Pievienot personāla atlases pieprasījuma vietu

Ja jūsu uzņēmuma ir vairākas atrašanās vietas, varat pievienot tās, lai pieprasītāji varētu izvēlēties vietu, kur jaunais darbinieks strādās. Atrašanās vieta tiks iekļauta darba sludinājumā.

1. Meklēšanas joslā ievadiet **personāla atlases pieprasījuma vietu**.

2. Atlasiet **Jauns**.

3. Laukā **Personāla atlases pieprasījuma vieta** ievadiet atrašanās vietas nosaukumu.

   ![Pievienot personāla atlases pieprasījuma vietu](./media/hr-recruit-0a-add-location.png)

4. Laukā **Apraksts** ievadiet atrašanās vietas aprakstu.

5. Sadaļā **Atrašanās vieta** atlasiet **Pievienot**. Ja parādās uznirstošais logs **Jaunā adrese**, ievadiet atrašanās vietas adresi.

   ![Ievadiet adresi](./media/hr-recruit-0b-address.png)

6. Sadaļā **Kontaktinformācija** ievadiet atrašanās vietas kontaktinformāciju.

7. Atlasiet **Saglabāt**.

## <a name="add-a-recruiting-request"></a>Pievienot personāla atlases pieprasījumu

Vadītāji var iesniegt personāla atlases pieprasījumus Personāla vadībā. Ja izmantojat atsevišķu personāla atlases programmu, pabeidzot šos soļus, tiks nosūtīts personāla atlases pieprasījums un sāksies personāla atlases process šajā lietojumprogrammā. Pretējā gadījumā veiciet šo procedūru, lai sāktu darbplūsmu savam iekšējam personāla atlases procesam.

1. Atlasiet **Darbinieku pašapkalpošanās pakalpojums**.

2. Atlasiet cilni **Mana komanda**.

3. Atlasiet **Pieprasījums, lai pieņemtu darbā**.

   ![Sākt personāla atlases pieprasījumu](./media/hr-recruit-1-request-to-recruit.png)

4. Aizpildiet laukus **Apraksts**, **Darbs** un **Plānotais sākuma datums**.

   ![Pabeigt personāla atlases pieprasījumu](./media/hr-recruit-2-request-to-recruit.png)

5. Atlasiet **Turpināt**. Tiek parādīts jūsu pozīcijas personāla atlases pieprasījums.

6. Sadaļā **Vispārīgi** atlasiet rekrutētāju no **Rekrutētāju** nolaižamā saraksta un pēc tam atlasiet atrašanās vietu **Personāla atlases pieprasījuma vietas** nolaižamajā sarakstā.

7. Sadaļā **Darbs** mainiet nepieciešamo informāciju un pēc tam atlasiet **Izveidot detalizētu informāciju no darba**.

   ![Izveidot detalizētu informāciju no darba](./media/hr-recruit-3-create-details-from-job.png)

   Pārējā informācija jūsu ievadītajam darbam atlases pieprasījumā tiks aizpildīta ar noklusējuma informāciju.

8. Sadaļā **Ārējais apraksts** ievadiet ārēju darba aprakstu.

9. Sadaļā **Amati** atlasiet **Pievienot** un pēc tam atlasiet amatu šim personāla atlases pieprasījumam.

   ![Pievienot amatu](./media/hr-recruit-4-select-position.png)

10. Sadaļā **Prasmes** atlasiet **Pievienot** un pēc tam atlasiet prasmi.

11. Sadaļā **Izglītības prasības** atlasiet **Pievienot** un pēc tam atlasiet vērtības no **Izglītības** un **Izglītības līmeņa** nolaižamajiem logiem.

   ![Pievienot izglītības prasības](./media/hr-recruit-5-select-educational-requirements.png)

12. Sadaļā **Komentārs** pievienojiet komentārus pēc nepieciešamības.

13. Sadaļā **Kompensācija** atlasiet līmeni no **Līmeņa** nolaižamā saraksta un pēc tam pielāgojiet **Zemu slieksni**, **Kontrolpunktu** un **Augstu slieksni**.

14. Kad jūsu personāla atlases pieprasījums ir pabeigts un jūs esat gatavs sākt personāla atlases procesu, izvēlņu joslā atlasiet **Aktivizēt**.

   ![Aktivizēt personāla atlases pieprasījumu](./media/hr-recruit-6-activate-recruit-request.png)

15. Atlasiet **Saglabāt**.

## <a name="view-and-edit-your-recruiting-requests"></a>Skatīt un rediģēt atlases pieprasījumus

Ja esat vadītājs un vēlaties skatīt savus pieprasījumus:

1. Atlasiet **Darbinieku pašapkalpošanās pakalpojums**.

2. Atlasiet cilni **Mana komanda**.

3. Sadaļā **Manas darba grupas informācija** atlasiet cilni **Personāla atlases pieprasījumi**.

   ![Atlasiet cilni Personāla atlases pieprasījumi](./media/hr-recruit-7-recruiting-requests.png)

4. Lai apskatītu vai rediģētu personāla atlases pieprasījumu, atlasiet to režģī.

Ja esat HR pro un vēlaties skatīt visus personāla atlases pieprasījumus:

1. Atlasiet **Personāla pārvaldība**.

2. Atlasiet **Personāla atlases pieprasījumi**.

   ![Skatīt personāla atlases pieprasījumus Personāla pārvaldībā](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. Lai apskatītu vai rediģētu personāla atlases pieprasījumu, atlasiet to režģī.

## <a name="add-or-edit-a-candidate-profile"></a>Pievienot vai rediģēt kandidāta profilu

Ja jūsu uzņēmums ir integrēts ar citu programmu, lai pārvaldītu personāla atlases pieprasījumus, personāla atlases pieprasījumi tiek pārsūtīti uz šo programmu. Pēc tam personāla atlases programma nosūta informāciju par kandidātu uz Personāla vadību. Pretējā gadījumā varat sekot saviem iekšējiem personāla atlases procesiem un ievadīt informāciju par kandidātu manuāli.

1. Atlasiet **Personāla pārvaldība**.

2. Atlasiet **Saites**.

3. Sadaļā **Personāla atlase** atlasiet **Kandidāti**.

   ![Skatīt kandidātus](./media/hr-recruit-9-candidates.png)

4. Lai pievienotu kandidātu, atlasiet **Jauns**. Lai rediģētu esošu kandidātu, izvēlieties kandidātu no saraksta un pēc tam atlasiet **Rediģēt**. Tiek parādīts kandidāta profils.

5. Sadaļā **Kandidāta kopsavilkums** ievadiet vai rediģējiet informāciju par kandidātu pēc nepieciešamības.

6. Sadaļā **Personāla atlases pieprasījums** atlasiet atlases pieprasījumu, lai saistītu kandidātu. Pēc tam pabeidziet **Aprēķināto sākuma datumu**, **Pieņemšanas vadītāju**, **Amatu** un **Apraksta laukus**.

   ![Saistīt ar personāla atlases pieprasījumu](./media/hr-recruit-10-link-to-recruiting-request.png)

7. Aizpildiet visu informāciju, ko vēlaties iekļaut kandidāta ierakstā, sekojošajās jomās:
   - **Komentāri**
   - **Profesionālā pieredze**
   - **Kontaktinformācija**
   - **Izglītība**
   - **Prasmes**
   - **Sertifikāti**
   - **Izvērtēšana**

8. Atlasiet **Saglabāt**.

## <a name="hire-a-candidate"></a>Pieņemt darbā kandidātu

Kad esat gatavs pieņemt darbā kandidātu, ievērojiet šo procedūru, lai nomainītu kandidātu uz darbinieku.

1. Kandidāta veidlapā atlasiet **Pieņemt darbā**.

   ![Pieņemt darbā kandidātu](./media/hr-recruit-11-hire.png)

2. Aizpildiet visus laukus veidlapā **Pieņemt darbā jaunu darbinieku**, sadaļā **Detalizēti** .

   ![Ievadīt jaunā darbinieka informāciju](./media/hr-recruit-12-hire-new-worker.png)

3. Sadaļā **Amata detaļas** pēc nepieciešamības pārbaudiet un mainiet informāciju.

4. Sadaļā **Iekārtošanas kontrolsaraksti** atlasiet šim darbiniekam atbilstīgos iekārtošanas kontrolsarakstus.

5. Atlasiet **Turpināt**, lai izveidotu darbinieka ierakstu.

   >[!NOTE]
   >Atkarībā no jūsu organizācijas darbplūsmām kandidāta ieraksts var iziet caur papildu apstiprināšanas soļiem, pirms kļūst par darbinieka ierakstu.

## <a name="decide-not-to-hire-a-candidate"></a>Nolemt nepieņemt darbā kandidātu

Ja izlemjat nepieņemt kandidātu, sekojiet šai procedūrai, lai noņemtu to no pārbaudes procesa. 

1. Kandidāta veidlapā atlasiet **Nepieņemt darbā**.

   ![Nepieņemt darbā kandidātu](./media/hr-recruit-13-do-not-hire.png)

2. Atlasiet **Pamatojuma kodu** un iekļaujiet komentārus.

3. Atlasiet **Labi**.

## <a name="dismiss-a-candidate"></a>Noraidīt kandidātu

Ja nepieciešams, varat noraidīt kandidātu pēc pieņemšanas darbā. Piemēram, kandidāts var noraidīt jūsu piedāvājumu vai neierasties darbā pirmajā dienā.

- Kandidāta veidlapā atlasiet **Noraidīt kandidātu**.

  ![Noraidīt kandidātu](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a>Skatiet arī

[Common Data Service virtuālo elementu konfigurēšana](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Darbaspēka pārvaldība](hr-personnel-departments-jobs-positions.md)<br>
[Darba komponentu iestatīšana](hr-personnel-jobs.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]