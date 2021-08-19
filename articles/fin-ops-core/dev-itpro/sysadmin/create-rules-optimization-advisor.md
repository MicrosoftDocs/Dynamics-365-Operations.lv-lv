---
title: Kārtulu izveide optimizācijas padomniekam
description: Šajā tēmā ir aprakstīts, kā pievienot jaunas kārtulas darbvietai Optimizācijas padomnieks.
author: roxanadiaconu
ms.date: 02/04/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: sericks
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: a65a71da066d70cafc641aafe21538830a9ebe56b607316570ea2435398cda1c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6734668"
---
# <a name="create-rules-for-optimization-advisor"></a>Kārtulu izveide optimizācijas padomniekam

[!include [banner](../includes/banner.md)]

Šajā tēmā ir izskaidrots, kā izveidot jaunas kārtulas darbvietai **Optimizācijas padomnieks**. Piemēram, varat izveidot jaunu kārtulu, kas nosaka, kuriem piedāvājuma pieprasījuma (PP) gadījumiem ir tukšs nosaukums. Gadījumiem izmantojot nosaukumus, tie ir viegli identificējami un meklējami. Šajā piemērā vienkāršoti parādīts, ko var panākt, izmantojot optimizācijas kārtulas. 

*Kārtula* ir atzīme programmas datos. Ja tiek izpildīts nosacījums, ko novērtē kārtula, tiek izveidotas iespējas optimizēt procesus vai uzlabot datus. Šīs iespējas var izmantot, un papildus var mērīt veikto darbību ietekmi. 

Lai izveidotu jaunu darbvietas **Optimizācijas padomnieks** kārtulu, pievienojiet jaunu klasi, kas paplašina abstrakto klasi **SelfHealingRule**, ievieš interfeisu **IDiagnosticsRule** un kurai ir piešķirts atribūts **DiagnosticRule**. Šai klasei ir arī jābūt metodei, kam piešķirts atribūts **DiagnosticsRuleSubscription**. Parasti tiek izmantota metode **opportunityTitle**, ko aplūkosim vēlāk. Šo jauno klasi var pievienot pielāgotam modelim, kam ir atkarība no modeļa **SelfHealingRules**. Tālāk sniegtajā piemērā ieviesto kārtulu dēvē par **RFQTitleSelfHealingRule**.

```xpp
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

Abstraktajai klasei **SelfHealingRule** ir abstraktas metodes, kas ir jāievieš pārmantošanas klasēs. Pamats ir metode **Novērtēt**, kas atgriež kārtulas identificēto iespēju sarakstu. Iespējas var attiekties uz katru juridisko personu vai arī visu sistēmu.

```xpp
protected List evaluate() 
{ 
    List results = new List(Types::Record); 
    
    DataArea dataArea; 

    while select id from dataArea 
        where !dataArea.isVirtual 
    { 
        changecompany(dataArea.id) 
        { 
            container result = this.findRFQCasesWithEmptyTitle(); 

            if (conLen(result) > 0) 
            { 
                SelfHealingOpportunity opportunity = this.getOpportunityForCompany(dataArea.Id); 
                opportunity.EvaluationState = SelfHealingEvaluationState::Evaluated; 
                opportunity.Data = result; 
                opportunity.OpportunityDate = DateTimeUtil::utcNow(); 
                
                results.addEnd(opportunity); 
            } 
        } 
    } 
    
    return results; 
} 
```

Iepriekš parādītā metode caurskata uzņēmumus un atlasa PP gadījumus ar tukšiem nosaukumiem metodē **findRFQCasesWithEmptyTitle**. Ja tiek atrasts vismaz viens šāds gadījums, tiek izveidota uzņēmuma iespēja ar metodi **getOpportunityForCompany**. Ņemiet vērā, ka tabulas **SelfHealingOpportunity** lauka **Dati** tips ir **Konteiners**, tādējādi tas var ietvert visus datus, kas attiecas uz šīs kārtulas loģiku. Parametram **OpportunityDate** iestatot pašreizējo laikspiedolu, tiek reģistrēts pēdējā iespējas novērtējuma laiks.  

Iespējas var tikt izveidotas arī kā starpuzņēmumu iespējas. Šajā gadījumā uzņēmumu caurskatīšana nav nepieciešama, un iespēja ir jāizveido, izmantojot metodi **getOpportunityAcrossCompanies**. 

Tālāk norādītajā kodā ir redzama metode **findRFQCasesWithEmptyTitle**, kas atgriež to PP gadījumu ID, kam ir tukšs nosaukums.

```xpp
private container findRFQCasesWithEmptyTitle() 
{ 
    container result; 

    PurchRFQCaseTable rfqCase; 
    while select RFQCaseId from rfqCase 
        where rfqCase.Name == '' 
    { 
        result += rfqCase.RFQCaseId; 
    } 
    
    return result; 
} 
```

Vēl divas metodes, kas jāievieš, ir **opportunityTitle** un **opportunityDetails**. Pirmā no tām atgriež īsu iespējas nosaukumu, savukārt otrā atgriež detalizētu iespējas aprakstu, kas var ietvert arī datus.

Metodes **opportunityTitle** atgrieztais nosaukums tiek parādīts darbvietas **Optimizācijas padomnieks** kolonnā **Optimizācijas iespēja**. Tas ir redzams arī kā galvene sānu rūtī, kurā parādīta papildinformācija par iespēju. Parasti šai metodei tiek piešķirts atribūts **DiagnosticRuleSubscription**, kas izmanto tālāk norādītos argumentus. 

* **Diagnostikas apgabals** — tipa **DiagnosticArea** uzskaitījums, kas norāda, kuram lietojumprogrammas apgabalam pieder kārtula, piemēram, **DiagnosticArea::SCM**. 

* **Kārtulas nosaukums** — virkne ar kārtulas nosaukumu. Tas tiks parādīts formas **Diagnostikas apstiprināšanas kārtula** kolonnā **Kārtulas nosaukums** (**DiagnosticsValidationRuleMaintain**). 

* **Izpildes biežums** — tipa **DiagnosticRunFrequency** uzskaitījums, kas norāda, cik bieži ir jāpalaiž kārtula, piemēram, **DiagnosticRunFrequency::Daily**. 

* **Kārtulas apraksts** — virkne, kas sniedz detalizētāku kārtulas aprakstu. Tas tiks parādīts formas **Diagnostikas apstiprināšanas kārtula** kolonnā **Kārtulas apraksts** (**DiagnosticsValidationRuleMaintain**). 

> [!NOTE]
> Atribūts **DiagnosticRuleSubscription** nepieciešams, lai kārtula darbotos. Parasti tas tiek izmantots metodei **opportunityTitle**, taču to var piešķirt jebkurai klases metodei.

Tālāk sniegts piemērs ar ieviešanu. Vienkāršībai izmantotas neapstrādātas virknes, taču pareizai ieviešanai ir nepieciešamas etiķetes. 

```xpp
[DiagnosticsRuleSubscription(DiagnosticsArea::SCM, 
                             'Assign titles to Request for Quotation cases', 
                             DiagnosticsRunFrequency::Daily,  
                             'This rule detects Requests for Quotation with empty titles.')] 
public str opportunityTitle() 
{ 
    return 'Assign titles to Request for Quotation cases'; 
} 
```

Metodes **opportunityDetails** atgrieztais apraksts ir redzams sānu rūtī, kurā parādīta papildinformācija par iespēju. Tam nepieciešams arguments **SelfHealingOpportunity**, kas ir lauks **Dati**, ko var izmantot papildinformācijas sniegšanai par iespēju. Piemērā metode atgriež to PP gadījumu ID, kam ir tukšs nosaukums. 

```xpp
public str opportunityDetails(SelfHealingOpportunity _opportunity) 
{ 
    str details = ''; 
    container opportunityData = _opportunity.Data; 
    int affectedRFQCasesCount = conLen(opportunityData); 

    if (affectedRFQCasesCount != 0) 
    { 
        details = 'The following Request for Quotation cases have an empty title:\n'; 
        for (int i = 1; i <= affectedRFQCasesCount ; i++) 
        { 
            PurchRFQCaseId rfqCaseId = conPeek(opportunityData, i); 
            details += rfqCaseId + '\n'; 
        } 
    } 

    return details; 
}
```

Divas atlikušās abstraktās metodes, kas jāievieš, ir **provideHealingAction** un **securityMenuItem**. 

**provideHealingAction** atgriež vērtību True, ja ir nodrošināta atjaunošanas darbība, pretējā gadījumā tiek atgriezta vērtība False. Ja tiek atgriezta vērtība True, ir jāievieš metode **performAction**, jo pretējā gadījumā tiks parādīta kļūda. Metode **performAction** izmanto argumentu **SelfHealingOpportunity**, kurā datus var izmantot darbībai. Piemērā darbība manuālai korekcijai atver **PurchRFQCaseTableListPage**. 

```xpp
public boolean providesHealingAction() 
{ 
    return true; 
} 

protected void performAction(SelfHealingOpportunity _opportunity) 
{ 
    new MenuFunction(menuItemDisplayStr(PurchRFQCaseTableListPage), MenuItemType::Display).run(); 
} 
```

Atkarībā no kārtulas specifikas, iespējams, var veikt automātisku darbību, izmantojot iespējas datus. Šajā piemērā sistēma varēja automātiski ģenerēt nosaukumus PP gadījumiem. 

Metode **securityMenuItem** atgriež darbību izvēlnes vienuma nosaukumu tā, lai kārtula būtu redzama tikai tiem lietotājiem, kuri var piekļūt darbību izvēlnes vienumam. Drošības apsvērumu dēļ noteiktas kārtulas un iespējas var būt noteiktas kā pieejamas tikai autorizētiem lietotājiem. Piemērā iespēju var skatīt tikai lietotāji, kuri var piekļūt vienumam **PurchRFQCaseTitleAction**. Ņemiet vērā, ka šis darbību izvēlnes vienums tika izveidots šim piemēram un tika pievienots kā ieejas punkts **PurchRFQCaseTableMaintain** drošības privilēģijai. 

> [!NOTE]
> Drošības apsvērumu dēļ, lai izvēlnes vienums dabotos pareizi, tam ir jābūt darbības izvēlnes vienumam. Citi izvēlnes vienumu tipi, piemēram, **Displeja izvēlnes vienumi**, nedarbosies pareizi.

```xpp
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

Kad kārtula ir kompilēta, izpildiet tālāk norādīto darbu, lai tā tiktu parādīta lietotāja interfeisā (UI).

```xpp
class ScanNewRulesJob 
{         
    public static void main(Args _args) 
    {         
        SysExtensionCache::clearAllScopes(); 
        var controller = new DiagnosticsRuleController(); 
        controller.runOperation(); 
    } 
} 
```

Kārtula tiks parādīta formā **Diagnostikas apstiprināšanas kārtula**, kas pieejama, atverot sadaļas **Sistēmas administrēšana** > **Periodiskie uzdevumi** > **Uzturēt diagnostikas apstiprināšanas kārtulu**. Lai tā tiktu novērtēta, atveriet sadaļas **Sistēmas administrēšana** > **Periodiskie uzdevumi** > **Ieplānot diagnostikas apstiprināšanas kārtulu** un atlasiet kārtulas biežumu, piemēram, **Katru dienu**. Noklikšķiniet uz **Labi**. Lai skatītu jauno iespēju, atveriet sadaļas **Sistēmas administrēšana** > **Optimizācijas padomnieks**. 

Tālāk esošais piemērs ir koda fragments ar kārtulas karkasu, tostarp visām nepieciešamajām metodēm un atribūtiem. Tas palīdz jums sākt rakstīt jaunas kārtulas. Piemēra ietvaros izmantotās etiķetes un darbību izvēlnes vienumi ir izmantoti tikai demonstrācijas nolūkos.

```xpp
[DiagnosticsRuleAttribute]
public final class SkeletonSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule
{
    [DiagnosticsRuleSubscription(DiagnosticsArea::SCM,
                                 "@SkeletonRuleLabels:SkeletonRuleTitle", // Label with the title of the rule
                                 DiagnosticsRunFrequency::Monthly,
                                 "@SkeletonRuleLabels:SkeletonRuleDescription")] // Label with a description of the rule
    public str opportunityTitle()
    {
        // Return a label with the title of the opportunity
        return "@SkeletonRuleLabels:SkeletonOpportunityTitle";
    }

    public str opportunityDetails(SelfHealingOpportunity _opportunity)
    {
        str details = "";

        // Use _opportunity.data to provide details on the opportunity

        return details;
    }

    protected List evaluate()
    {
        List results = new List(Types::Record);

        // Write here the core logic of the rule

        // When creating an opportunity, use:
        //     * this.getOpportunityForCompany() for company specific opportunities
        //     * this.getOpportunityAcrossCompanies() for cross-company opportunities

        return results;
    }

    public boolean providesHealingAction()
    {
        return true;
    }

    protected void performAction(SelfHealingOpportunity _opportunity)
    {
        // Place here the code that performs the healing action

        // To open a form, use the following:
        // new MenuFunction(menuItemDisplayStr(SkeletonRuleDisplayMenuItem), MenuItemType::Display).run();
    }

    public MenuName securityMenuItem()
    {
        return menuItemActionStr(SkeletonRuleActionMenuItem);
    }

}
```

Lai iegūtu papildinformāciju, skatiet īso YouTube video: [Optimizācijas padomnieks programmā Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]