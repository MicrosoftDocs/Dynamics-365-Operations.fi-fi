---
title: Projektiarvioiden synkronointi Project Service Automationista suoraan Finance and Operationsin projektiennusteisiin
description: "Tässä ohjeaiheessa käsitellään malleja ja tehtäviä, joilla projektin tunti- ja kuluarviot synkronoidaan suoraan Microsoft Dynamics 365 for Project Service Automationista Dynamics 365 for Finance and Operationsiin."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 90501f40da0fdc66ad087b3bd746c908cc25711b
ms.contentlocale: fi-fi
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-estimates-from-project-service-automation-directly-to-project-forecasts-in-finance-and-operations"></a>Projektiarvioiden synkronointi Project Service Automationista suoraan Finance and Operationsin projektiennusteisiin

Tässä ohjeaiheessa käsitellään malleja ja tehtäviä, joilla projektin tunti- ja kuluarviot synkronoidaan suoraan Microsoft Dynamics 365 for Project Service Automationista Dynamics 365 for Finance and Operationsiin.

> [!NOTE]
> Projektitehtävien integrointi, kulutapahtumaluokat, tuntiarviot, kuluarviot ja toiminnon lukitseminen ovat käytössä Dynamics 365 for Finance and Operationsin versiossa 8.0.


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Tiedonkulku Project Service Automationista Finance and Operationsiin

Project Service Automationin ja Finance and Operationsin välinen integrointiratkaisu synkronoi Project Service Automationin ja Finance and Operationsin esiintymien tiedot tietojen integrointiominaisuudella. Tietojen integrointiominaisuudessa käytettävissä olevat integrointimallit mahdollistavat projektin tunti- ja kuluarviointeja koskevan tiedonkulun Project Service Automationista ja Finance and Operationsiin.

Seuraava kuva ilmaisee, miten tiedot synkronoidaan Project Service Automationin ja Finance and Operationsin välillä.

[![Project Service Automationin ja Finance and Operationsin välisen integroinnin tiedonkulku](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)


## <a name="templates-and-tasks"></a>Mallit ja tehtävät

Saat käytettävissä olevat mallit käyttöösi valitsemalla Microsoft PowerAppsin hallintakeskuksessa **Projektit**. Valitse sitten julkaiset mallit valitsemalla oikeassa yläkulmassa **Uusi projekti**.

Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoimaan projektin tuntiarviot Project Service Automationista Finance and Operationsiin:

-  **Mallin nimi tietojen integroinnissa:** Projektin tuntiarviot (PSA:sta Fin and Opsiin)

-  **Projektin tehtävien nimi:** 
    - Tapahtumasuhteet 
    - Kuluarviot

## <a name="entity-set"></a>Yksikköjoukko

| Project Service Automation      | Finance and Operations                          |
|---------------------------------|-------------------------------------------------|
| Projektitehtävät                   | Projektin tuntiarvioiden integrointiyksikkö   |

## <a name="entity-flow"></a>Yksikön työnkulku

Projektin tuntiarvioita hallitaan Project Service Automationissa ja ne synkronoidaan Finance and Operationsiin projektin tuntiennusteisiin.

## <a name="preconditions"></a>Ennakkoehdot

Projektin, projektitehtävien ja projektin kuluarvion tapahtumaluokat on synkronoitava, ennen kuin projektin tuntiarviot voidaan synkronoida.

## <a name="power-query"></a>Power Query

Projektin tuntiarviomallissa on käytettävä Microsoft Power Queryä. Sen avulla voidaan päivittää seuraavat toiminnot:
- Määritettävää **ennustemallin tunnusta** käytetään, kun integrointi luo uusi tuntiennusteita.
- Sellaisten tehtävän resurssikohteisten tietueiden suodattaminen pois, jotka aiheuttavat tuntiennusteisiin tapahtuvan integroinnin epäonnistumisen.
- Tyhjien tapahtumaluokkarivien suodattaminen pois. Jos suodatusta ei tehdä, tuloksena voi olla virheellisiä tuntiennusteita

### <a name="forecast-model-id"></a>Ennustemallin tunnus
Voit päivittää malliin oletusennustemallin tunnuksen avaamalla määrityksen napsauttamalla **Yhdistä**-nuolta. Avaa kyselyn ja suodatuksen lisäasetukset valitsemalla.
- Jos käytät Microsoft Projectin tuntiarviot (PSA:sta Fin and Opsiin) -oletusmallia, valitse **Lisätty ehto** **Käytetyt vaiheet** -osassa. Vaihda **Toiminto**-merkinnän **O_forecast** tilalle sen **ennustemallin tunnuksen** nimi, jota käytetään integraatiossa. Oletusmallin ennustemalli tunnus on saatu esittelytiedoista.
- Jos luot uuden mallin, sinun on lisättävä tämä sarake. Valitse **Lisää ehtosarake** ja anna sarakkeelle nimi, kuten Mallitunnus. Anna sarakkeelle ehto, jonka mukaan jos Projektitehtävä ei ole tyhjäarvo, niin <enter the forecast model ID>; muuten tyhjäarvo.

### <a name="filter-out-resource-specific-records"></a>Resurssikohtaisten tietueiden suodattaminen
Projektin tuntiarviot (PSA:sta Fin and Opsiin) -mallissa on oletussuodatin, joka poistaa kaikki resurssikohtaiset tietueet. Jos luot oman mallin, tämä suodatin on lisättävä. Valitse kyselyn ja suodatuksen lisäasetuslomakkeen **msdyn_islinetask**-sarakkeessa suodatin, joka sisällyttää vain **Epätosi**-tietueet.

### <a name="filter-out-empty-transaction-category-rows"></a>Tyhjien tapahtumaluokkarivien suodattaminen
Kaikki tyhjiä tapahtumaluokkia sisältävät rivit poistava suodatin on lisättävä. Tämä on tehtävä riippumatta siitä, käytätkö oletusmallia vai luotko oman mallin. Tämä suodatin poistaa kaikki Project Service Automationin yhteenvetorivit, joiden vuoksi Finance and Operationsin tuntiennusteet voisivat olla virheellisiä. Valitse kyselyn ja suodatuksen lisäasetuslomakkeen **msdyn_transactioncategory_value**-sarakkeen tyhjäarvoisten tietueiden poissuodatus.

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

Seuraavassa kuvassa on esimerkki mallitehtävän yhdistämisestä tietojen integroinnin yhteydessä. Yhdistämismääritys näyttää Project Service Automationista Finance and Operationsiin synkronoitavan kentän tiedot.

[![Mallin yhdistäminen](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

Seuraavaa mallia ja sen taustalla olevaa tehtävää käytetään synkronoimaan projektin kuluarviot Project Service Automationista Finance and Operationsiin:

-  **Mallin nimi tietojen integroinnissa:** Projektin kuluarviot (PSA:sta Fin and Opsiin)
-  **Projektin tehtävien nimi:** 
     - Tapahtumasuhteet 
     - Kuluarviot

## <a name="entity-set"></a>Yksikköjoukko

| Project Service Automation      | Finance and Operations                                     |
|---------------------------------|------------------------------------------------------------|
| Tapahtumayhteydet         | Projektin tapahtumasuhteiden integrointiyksikkö.   |
| Arviorivit                  | Projektin kuluarvioiden integrointiyksikkö.           |

## <a name="entity-flow"></a>Yksikön työnkulku

Projektin kuluarvioita hallitaan Project Service Automationissa ja ne synkronoidaan Finance and Operationsiin projektin kuluennusteisiin.

## <a name="prerequisites"></a>Edellytykset

Projektin, projektitehtävien ja projektin kuluarvion tapahtumaluokat on synkronoitava, ennen kuin projektin kuluarviot voidaan synkronoida.

## <a name="power-query"></a>Power Query

Projektin kuluarviomallissa on käytettävä Microsoft Power Queryä. Sen avulla voidaan päivittää seuraavat toiminnot:
- Vain kuluarviorivien tietueet sisällyttävä suodatus
- Määritettävää **ennustemallin tunnusta** käytetään, kun integrointi luo uusi tuntiennusteita.
- Laskutustyyppien muuntaminen.
- Tapahtumatyyppien muuntaminen.

### <a name="filter-to-include-only-expense-estimate-lines"></a>Vain kuluarviorivit sisällyttävä suodatus
Projektin kuluarviot (PSA:sta Fin and Opsiin) -mallissa oletussuodatin, joka sisällyttää integraatioon vain kulurivit. Jos luot oman mallin, tämä suodatin on lisättävä. Valitse tapahtumasuhdetehtävä ja napsauta **Yhdistä**-nuolta. Valitse **Kyselyn ja suodatuksen lisäasetukset**. Suodata **msdyn_transactiontype1**-sarake sisältävään vain **msdyn_estimateline**.

### <a name="forecast-model-id"></a>Ennustemallin tunnus
Voit päivittää malliin oletusennustemallin tunnuksen avaamalla kuluarviotehtävän määrityksen napsauttamalla **Yhdistä**-nuolta. Avaa kyselyn ja suodatuksen lisäasetukset valitsemalla.
- Jos käytät Microsoft Projectin kuluarviot (PSA:sta Fin and Opsiin) -oletusmallia, valitse ensin **Lisätty ehto** **Käytetyt vaiheet** -osassa. Vaihda **Toiminto**-merkinnän **O_forecast** tilalle sen **ennustemallin tunnuksen** nimi, jota käytetään integraatiossa. Oletusmallin ennustemalli tunnus on saatu esittelytiedoista.
- Jos luot uuden mallin, sinun on lisättävä tämä sarake. Valitse **Lisää ehtosarake** ja anna sarakkeelle nimi, kuten Mallitunnus. Anna sarakkeelle ehto, jonka mukaan jos arviorivin tunnus ei ole tyhjäarvo, niin <anna ennustemallin tunnus>; muutoin tyhjäarvo.

### <a name="transform-the-billing-types"></a>Laskutustyyppien muuntaminen
Projektin kuluarviot (PSA to Fin and Ops) -malliin on lisätty ehtosarake, joka muuntaa Project Service Automationista vastaanotetut laskutustyypit integroinnin aikana.
- Jos luot oman mallin, tämä ehtosarake on lisättävä. Valitse kyselyn ja suodatuksen lisäasetuslomakkeessa **Lisää ehtosarake**. Anna sarakkeelle uusi nimi, kuten Laskutustyyppi. Anna ehto seuraavasti:

    Jos **msdyn_billingtype** = 192350000, niin **Ei-veloitettava** muutoin jos **msdyn_billingtype** = 192350001, niin **Veloitettava** muutoin jos **msdyn_billingtype** = 192350002, niin **Täydentävä** muutoin **Ei-käytettävissä**

### <a name="transform-the-transaction-types"></a>Tapahtumatyyppien muuntaminen
Projektin kuluarviot (PSA to Fin and Ops) -malliin on lisätty ehtosarake, joka muuntaa Project Service Automationista vastaanotetut tapahtumatyypit integroinnin aikana.
- Jos luot oman mallin, tämä ehtosarake on lisättävä. Valitse kyselyn ja suodatuksen lisäasetuslomakkeessa **Lisää ehtosarake**. Anna sarakkeelle uusi nimi, kuten Tapahtumatyyppi. Anna seuraava ehto: Jos **msdyn_transactiontypecode** = 192350000, niin **Kustannus** muutoin jos **msdyn_transactiontypecode** = 192350005, niin **Sales** muutoin **tyhjäarvo**

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

Seuraavissa kuvissa on esimerkkejä mallitehtävän yhdistämisistä tietojen integroinnin yhteydessä. Yhdistämismääritys näyttää Project Service Automationista Finance and Operationsiin synkronoitavan kentän tiedot.

[![Mallin yhdistäminen](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Mallin yhdistäminen](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)




