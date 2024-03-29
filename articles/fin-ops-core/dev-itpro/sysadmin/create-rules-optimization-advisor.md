---
title: Optimointityökalun sääntöjen luominen
description: Tässä artikkelissa käsitellään uusien sääntöjen lisäämistä optimointityökaluun.
author: kamaybac
ms.date: 02/04/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: global
ms.author: kamaybac
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.search.form: SelfHealingWorkspace
ms.openlocfilehash: a4addc98e3d5496bc8d2fafb3918931da876739f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273914"
---
# <a name="create-rules-for-optimization-advisor"></a>Optimointityökalun sääntöjen luominen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa selitetään, miten **optimointityökalun** uusia sääntöjä luodaan. Voit esimerkiksi luoda uuden säännön, joka määrittää millä tarjouspyyntötapauksilla on tyhjä otsikko. Kun tapauksissa käytetään otsikoita, ne on helppo tunnistaa ja niissä on helppo tehdä hakuja. Tämä melko yksinkertainen esimerkki osoittaa, mitä optimointisäännöillä voi saavuttaa. 

*Sääntö* tarkoittaa sovellustietojen tarkistusta. Jos säännön arvioima ehto täyttyy, luodaan mahdollisuuksia prosessien optimointiin ja tietojen parannukseen. Mahdollisuuksiin voidaan reagoida ja, valinnaisesti, toimintojen vaikutus voidaan mitata. 

Voit luoda uuden säännön **optimointityökaluun** lisäämällä **DiagnosticRule**-määritteellä varustetun **SelfHealingRule**-abstraktiluokkaa laajentavan uuden luokan ja **IDiagnosticsRule**-liittymän toteutuksen. Luokalla on myös **DiagnosticsRuleSubscription**-määritteellä varustettu menetelmä. Yleensä se tehdään **opportunityTitle**-menetelmällä, joka käsitellään myöhemmin. Tämä uusi luokka voidaan lisätä mukautettuun malliin, joka on riippuvainen **SelfHealingRules**-mallista. Seuraavassa esimerkissä toteutetaan **RFQTitleSelfHealingRule**-niminen sääntö.

```xpp
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

**SelfHealingRule**-abstraktiluokassa on abstraktimenetelmiä, jotka on toteutettava perivissä luokissa. Ytimenä on **arviointimenetelmä**, joka palauttaa luettelon säännön tunnistamia mahdollisuuksia. Mahdollisuudet voivat olla yritys- tai järjestelmäkohtaisia.

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

Edellä oleva menetelmä hakee ja valitsee yrityksistä **findRFQCasesWithEmptyTitle**-menetelmällä tarjouspyyntötapauksia, joissa on tyhjiä otsikoita. Jos vähintään yksi kyseinen tapaus löytyy, yrityskohtainen mahdollisuus luodaan **getOpportunityForCompany**-menetelmällä. Huomaa, että **SelfHealingOpportunity**-taulun **Tiedot**-kenttä on **Säilö**-tyyppinen ja siinä voi siksi olla tämän säännön logiikkaan liittyviä tietoja. Kun **OpportunityDate** määritetään kuluvan hetken aikaleimalla, mahdollisuuden viimeisin arviointi rekisteröidään.  

Mahdollisuudet voivat olla myös yritysten välisiä. Siinä tapauksessa yritykset kattava haku ei ole välttämätöntä ja mahdollisuus on luotava **getOpportunityAcrossCompanies**-menetelmällä. 

Seuraava koodi näyttää **findRFQCasesWithEmptyTitle**-menetelmän, joka palauttaa tyhjiä otsikoita sisältävien tarjouspyyntötapausten tunnukset.

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

**opportunityTitle** ja **opportunityDetails** ovat kaksi muuta toteutettavaa menetelmää. Edellinen palauttaa mahdollisuuden lyhyen otsikon, kun taas jälkimmäinen palauttaa mahdollisuuden tarkan kuvauksen, joka voi sisältää myös tietoja.

**opportunityTitle**-menetelmän palauttava otsikko näkyy **Optimointityökalu**-työtilan **Optimointimahdollisuus**-sarakkeessa. Se näkyy myös sivuruudun otsikossa, jossa on lisätietoja mahdollisuudesta. Yleensä tämä menetelmä on varustettu **DiagnosticRuleSubscription**-määritteellä, joka käyttää seuraavia argumentteja: 

* **Diagnosointialue** – Valintaluettelotyyppi **DiagnosticArea** kuvaa, mihin sovellusalueeseen sääntö kuuluu. Esimerkki: **DiagnosticArea::SCM**. 

* **Säännön nimi** – Merkkijono, jossa on säännön nimi. Se näkyy **Säännön nimi** -sarakkeessa **Diagnostiikan vahvistussääntö** -lomakkeessa (**DiagnosticsValidationRuleMaintain**). 

* **Suoritustiheys** – Valintaluettelotyyppi **DiagnosticRunFrequency** kuvaa, miten usein sääntö suoritetaan. Esimerkki: **DiagnosticRunFrequency::Daily**. 

* **Säännön kuvaus** – Merkkijono, jossa on säännön yksityiskohtainen kuvaus. Se näkyy **Säännön kuvaus** -sarakkeessa **Diagnostiikan vahvistussääntö** -lomakkeessa (**DiagnosticsValidationRuleMaintain**). 

> [!NOTE]
> **DiagnosticRuleSubscription**-määrite on välttämätön säännön toiminnan kannalta. Sitä käytetään yleensä **opportunityTitle**-menetelmässä, mutta se voi olla luokan minkä tahansa menetelmän varusteena.

Seuraavassa on esimerkkitoteutus. Käsittelemättömiä merkkijonoja käytetään yksinkertaisuuden vuoksi, mutta oikea toteutus edellyttää otsikoita. 

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

**opportunityDetails**-menetelmän palauttama kuvaus näkyy sivuruudussa ja siinä on lisätietoja mahdollisuudesta. Se käyttää **SelfHealingOpportunity**-argumenttia, joka on **Tiedot**-kenttä ja jolla voi antaa lisätietoja mahdollisuudesta. Esimerkissä menetelmä palauttaa tyhjän otsikon sisältävien tarjouspyyntötapausten tunnukset. 

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

Jäljellä olevat kaksi toteutettavaa menetelmää ovat **provideHealingAction** ja **securityMenuItem**. 

**provideHealingAction** palauttaa tosi-arvon, jos korjaustoiminto annetaan. Muussa tapauksessa palautetaan epätosi. Jos tosi palautetaan, menetelmä **performAction** on toteutettava tai tapahtuu virhe. **performAction**-menetelmä käyttää **SelfHealingOpportunity**-argumenttia, jossa tietoja voi käyttää toimintaan. Esimerkiksi toiminto avaa kohteen **PurchRFQCaseTableListPage** manuaalisesti korjattavaksi. 

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

Säännön tietojen mukaan automaattinen toiminto voi olla mahdollista mahdollisuuden tietojen avulla. Tässä esimerkissä järjestelmä voi luoda muodostaa tarjouspyyntötapausten otsikot automaattisesti. 

**securityMenuItem** palauttaa toimintovalikkovaihtoehdon nimen siten, että sääntö näkyy vain käyttäjille, jotka voivat käyttää toiminnon valikkovaihtoehtoa. Suojaus voi edellyttää, että tietyt säännöt ja mahdollisuudet ovat vain valtuutettujen käyttäjien käytettävissä. Esimerkissä mahdollisuuden näkevät vain käyttäjät, joilla on **PurchRFQCaseTitleAction**-käyttöoikeus. Huomaa, että tämä toimintovalikkovaihtoehto luotiin tässä esimerkissä ja lisättiin **PurchRFQCaseTableMaintain**-suojausoikeuden aloituspisteeksi. 

> [!NOTE]
> Suojauksen oikea toiminta edellyttää, että valikkovaihtoehto on toimintovalikon vaihtoehto. Muut valikkovaihtoehtotyypit, kuten **Näyttövalikon vaihtoehdot** eivät toimi oikein.

```xpp
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

Kun sääntö on käännetty, saat sen näkyviin käyttöliittymään suorittamalla seuraava työ.

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

Sääntö näkyy **Diagnostiikan vahvistussääntö** -lomakkeessa, jonka voi avata valitsemalla **Järjestelmän hallinta** > **Kausittaiset tehtävät** > **Ylläpidä diagnostiikan vahvistussääntöä**. Voit arvioida sen valitsemalla ensin **Järjestelmän hallinta** > **Kausittaiset tehtävät** > **Aikatauluta diagnostiikan vahvistussääntö** ja sitten säännön tiheyden, kuten **Päivittäin**. Napsauta **OK**. Voit tarkastella uutta mahdollisuutta valitsemalla **Järjestelmän hallinta** > **Optimointityökalu**. 

Seuraavassa esimerkissä on koodikatkelma, jossa on kaikki tarvittavat menetelmät ja määritteet sisältävä sääntörunko. Se auttaa aloittamaan uusien sääntöjen kirjoittamisen. Esimerkissä käytettyjä otsikoita ja toimintovalikon vaihtoehtoja käytetään vain esittelytarkoituksessa.

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

Lisätietoja on lyhyessä YouTube-videossa: [Dynamics 365 Financen optimointineuvoja](https://www.youtube.com/watch?v=MRsAzgFCUSQ)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
