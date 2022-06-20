---
title: Personāla atlases kandidāti
description: Šajā rakstā aprakstīts, kā darbiniekus pieņemt darbā Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 743c78d3526db2707630229d4cf21531f9641dd6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879255"
---
# <a name="recruit-job-candidates"></a>Personāla atlases kandidāti


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources palīdz pārvaldīt personāla atlases pieprasījumus. Tas palīdz arī netraucēti pāriet no kandidātiem uz darbiniekiem. Ja jūsu uzņēmums izmanto atsevišķu personāla atlases programmu, personāla atlases process var ietvert šādas darbības:<!--note from editor: Should this be a numbered list? These steps do seem to follow a particular order.-->

- Ievadiet darbinieku atlases pieprasījumu Personāla vadībā.
- Saņemt kandidātu nosūtījumus Personāla vadībā no personāla atlases programmas.
- Pabeigt kandidātu apstiprināšanas procesu Personāla vadībā.

Ja neizmantojat atsevišķu personāla atlases programmu, varat arī manuāli pārvaldīt kandidātus Personāla vadībā.

> [!NOTE]
> Ja esat administrators vai izstrādātājs un vēlaties integrēt cilvēkresursus ar trešās puses personāla atlases programmu, [dodieties uz "Konfigurēt Dataverse](hr-admin-integration-common-data-service.md) integrāciju" un "Konfigurēt [Dataverse virtuālās tabulas"](hr-admin-integration-common-data-service-virtual-entities.md)
>
> Varat arī atrast darbā pieņemšanas integrācijas programmas [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).
>
## <a name="enable-recruiting-requests-on-the-merged-infrastructure"></a>Iespējot personāla atlases pieprasījumus sapludinātajā infrastruktūrai

Ja vēlaties iesniegt personāla atlases pieprasījumus HR personāla atlasei, jums vispirms jāiespējo **HR lietotāja pieredze un personāla** **atlases procesa pārvaldības funkcijas**.

Tiklīdz funkcijas ir ieslēgtas, izvēlieties funkcionalitāti ar šādiem soļiem: 
1. Dodieties uz **sadaļu Cilvēkresursu** > **iestatīšanas** > **personāla vadības parametri**.
2.  **Cilnē Personāla atlase** iestatiet personāla atlasei iespējoto **lauku** uz **Jā**.
3. Nolaižot **personāla atlases** pieredzi, atlasiet HR personāla **atlasi**.  
4. Noklikšķiniet uz **Saglabāt**. 

> [!Note] 
> Kad **personāla atlase ir** atlasīta, **personāla atlases projekti** (mantojuma) nebūs pieejami. 


## <a name="add-a-recruiting-request-location"></a>Pievienot personāla atlases pieprasījuma vietu

Ja jūsu uzņēmuma ir vairākas atrašanās vietas, varat pievienot tās, lai pieprasītāji varētu izvēlēties vietu, kur jaunais darbinieks strādās. Atrašanās vieta tiks iekļauta darba sludinājumā.

1. Meklēšanas joslā ievadiet personāla atlases **pieprasījuma atrašanās vietu**.
2. Atlasiet **Jauna**.
3. Laukā **Personāla atlases pieprasījuma vieta** ievadiet atrašanās vietas nosaukumu.

    ![Pievienot personāla atlases pieprasījuma vietu.](./media/hr-recruit-0a-add-location.png)

4. Aprakstam **ievadiet** atrašanās vietas aprakstu.
5. Sadaļā **Atrašanās vieta** atlasiet **Pievienot**. Ja tiek **atvērts** dialogs Jauna adrese, ievadiet atrašanās vietas adresi.<!--note from editor: Please make the address in this image less plausible. Via the fictitious guidelines on CELAweb: For street addresses, you should use sequential numbers, common street names, and incorrect zip codes (e.g., 4567 Main St Buffalo, NY 98052). (See https://microsoft.sharepoint.com/sites/CELAWeb-Copyrights-Trademarks-And-Patents/SitePages/trademarks-fictitious-names.aspx)-->

    ![Ievadiet adresi.](./media/hr-recruit-0b-address.png)

6. Sadaļā **Kontaktinformācija** ievadiet atrašanās vietas kontaktinformāciju.
7. Atlasiet **Saglabāt**.

## <a name="add-a-recruiting-request"></a>Pievienot personāla atlases pieprasījumu

Vadītāji var iesniegt personāla atlases pieprasījumus Personāla vadībā. Ja izmantojat atsevišķu personāla atlases programmu, pabeidzot šos soļus, tiks nosūtīts personāla atlases pieprasījums un sāksies personāla atlases process šajā lietojumprogrammā. Pretējā gadījumā veiciet šo procedūru, lai sāktu darbplūsmu savam iekšējam personāla atlases procesam.

1. Atlasiet **Darbinieku pašapkalpošanās pakalpojums**.
2. Atlasiet cilni **Mana komanda**.
3. Atlasīt **pieprasījumu personāla atlasei**.

    ![Sākt personāla atlases pieprasījumu.](./media/hr-recruit-1-request-to-recruit.png)

4. Aizpildiet laukus **Apraksts**, **Darbs** un **Plānotais sākuma datums**.

    ![Pabeigt personāla atlases pieprasījumu.](./media/hr-recruit-2-request-to-recruit.png)

5. Atlasiet **Turpināt**. Tiek parādīts jūsu pozīcijas personāla atlases pieprasījums.
6. Sadaļā **Vispārīgi** atlasiet personāla atlases darbinieku **no** nolaižamā saraksta personāla atlase un pēc tam atlasiet atrašanās vietu no **nolaižamā** saraksta Personāla atlases pieprasījumu atrašanās vieta.
7. Sadaļā **Darbs** mainiet nepieciešamo informāciju un pēc tam atlasiet **Izveidot detalizētu informāciju no darba**.

    ![Izveidot detalizētu informāciju no darba.](./media/hr-recruit-3-create-details-from-job.png)

    Atlikusī personāla atlases pieprasījuma informācija tiks aizpildīta ar noklusējuma informāciju par ievadīto darbu.

8. Sadaļā **Ārējais apraksts** ievadiet ārēju darba aprakstu.
9. Sadaļā **Amati** atlasiet **Pievienot** un pēc tam atlasiet amatu šim personāla atlases pieprasījumam.<!--note from editor: In all of these images, are they approved fictitious names, or do they come from sample data included with the app?-->

    ![Pievienot amatu.](./media/hr-recruit-4-select-position.png)

10. Sadaļā **Prasmes** atlasiet **Pievienot** un pēc tam atlasiet prasmi.
11. Sadaļā **Izglītības prasības** atlasiet **Pievienot** un pēc tam nolaižamās **izvēlnēs** Izglītība **un Izglītības** līmenis atlasiet vērtības.

    ![Pievienot izglītības prasības.](./media/hr-recruit-5-select-educational-requirements.png)

12. Sadaļā **Komentārs** pievienojiet komentārus pēc nepieciešamības.
13. Sadaļā **Atlīdzība** atlasiet līmeni no nolaižamā saraksta **Līmenis** un pēc tam pēc **tam** pēc nepieciešamības pielāgojiet zemo slieksni, **·** **kontrolpunktu un augstu** slieksni.
14. Kad jūsu personāla atlases pieprasījums ir pabeigts un jūs esat gatavs sākt personāla atlases procesu, izvēlņu joslā atlasiet **Aktivizēt**.

    ![Aktivizēt personāla atlases pieprasījumu.](./media/hr-recruit-6-activate-recruit-request.png)

15. Atlasiet **Saglabāt**.

## <a name="view-and-edit-your-recruiting-requests"></a>Skatīt un rediģēt atlases pieprasījumus

Ja esat vadītājs un vēlaties skatīt savus pieprasījumus:

1. Atlasiet **Darbinieku pašapkalpošanās pakalpojums**.
2. Atlasiet cilni **Mana komanda**.
3. Sadaļā **Manas darba grupas informācija** atlasiet cilni **Personāla atlases pieprasījumi**.

    ![Atlasiet cilni Personāla atlases pieprasījumi.](./media/hr-recruit-7-recruiting-requests.png)

4. Lai apskatītu vai rediģētu personāla atlases pieprasījumu, atlasiet to režģī.

Ja esat HR pro un vēlaties skatīt visus personāla atlases pieprasījumus:

1. Atlasiet **Personāla pārvaldība**.
2. Atlasiet **Personāla atlases pieprasījumi**.

    ![Skatīt personāla atlases pieprasījumus Personāla pārvaldībā.](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. Lai apskatītu vai rediģētu personāla atlases pieprasījumu, atlasiet to režģī.

## <a name="add-or-edit-a-candidate-profile"></a>Pievienot vai rediģēt kandidāta profilu

Ja jūsu uzņēmums ir integrēts ar citu programmu, lai pārvaldītu personāla atlases pieprasījumus, personāla atlases pieprasījumi tiek pārsūtīti uz šo programmu. Pēc tam personāla atlases programma nosūta informāciju par kandidātu uz Personāla vadību. Pretējā gadījumā varat sekot saviem iekšējiem personāla atlases procesiem un ievadīt informāciju par kandidātu manuāli.

1. Atlasiet **Personāla pārvaldība**.
2. Atlasiet **Saites**.
3. Sadaļā **Personāla atlase** atlasiet **Kandidāti**.

    ![Skatīt kandidātus.](./media/hr-recruit-9-candidates.png)

4. Lai pievienotu kandidātu, atlasiet **Jauns**. Lai rediģētu esošu kandidātu, izvēlieties kandidātu no saraksta un pēc tam atlasiet **Rediģēt**. Tiek parādīts kandidāta profils.
5. Sadaļā **Kandidāta kopsavilkums** ievadiet vai rediģējiet informāciju par kandidātu pēc nepieciešamības.
6. Sadaļā **Personāla atlases pieprasījums** atlasiet atlases pieprasījumu, lai saistītu kandidātu. Pēc tam pēc **vajadzības aizpildiet laukus** **Plānotais sākuma datums**,**Nolīgšanas** vadītājs, **Amats** un Apraksts.

    ![Saistīt ar personāla atlases pieprasījumu.](./media/hr-recruit-10-link-to-recruiting-request.png)

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

1. Lapā Kandidāts **atlasiet** Pieņemt **darbā**.

    ![Pieņemt darbā kandidātu.](./media/hr-recruit-11-hire.png)

2. Lapā Pieņemt **darbā jaunu darbinieku** zem Detalizētas informācijas **aizpildiet** visus laukus.

    ![Ievadīt jaunā darbinieka informāciju.](./media/hr-recruit-12-hire-new-worker.png)

3. Sadaļā **Amata detaļas** pēc nepieciešamības pārbaudiet un mainiet informāciju.
4. Sadaļā **Iekārtošanas kontrolsaraksti** atlasiet šim darbiniekam atbilstīgos iekārtošanas kontrolsarakstus.
5. Atlasiet **Turpināt**, lai izveidotu darbinieka ierakstu.

    > [!NOTE]
    > Atkarībā no organizācijas darbplūsmām kandidāta ieraksts var iziet caur papildu apstiprināšanas soļiem pirms pārsāciet darbinieka ierakstu.

## <a name="decide-not-to-hire-a-candidate"></a>Nolemt nepieņemt darbā kandidātu

Ja izlemjat nepieņemt kandidātu, sekojiet šai procedūrai, lai noņemtu to no pārbaudes procesa. 

1. Lapā Kandidāts **atlasiet** Nav **nolīgšanas**.

    ![Nepieņemt darbā kandidātu.](./media/hr-recruit-13-do-not-hire.png)

2. Atlasiet **Pamatojuma kodu** un iekļaujiet komentārus.
3. Atlasiet **Labi**.

## <a name="dismiss-a-candidate"></a>Noraidīt kandidātu

Ja nepieciešams, varat noraidīt kandidātu pēc pieņemšanas darbā. Piemēram, kandidāts var noraidīt jūsu piedāvājumu vai neierasties darbā pirmajā dienā.

- Lapā Kandidāts **atlasiet** Noraidīt **kandidātu**.

    ![Noraidīt kandidātu.](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a>Skatiet arī

[Pakalpojuma Dataverse virtuālo tabulu konfigurēšana](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Darbaspēka pārvaldība](hr-personnel-departments-jobs-positions.md)<br>
[Darba komponentu iestatīšana](hr-personnel-jobs.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
