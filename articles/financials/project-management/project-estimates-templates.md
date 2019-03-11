---
title: Projektiarvioiden synkronointi suoraan Project Service Automationista Finance and Operationsin projektitoimintoihin
description: Tässä ohjeaiheessa käsitellään malleja ja tehtäviä, joilla projektin tunti- ja kuluarviot synkronoidaan suoraan Microsoft Dynamics 365 for Project Service Automationista Microsoft Dynamics 365 for Finance and Operationsiin.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 21338b889e0377dbfd5adfd461ea81b39a75baf8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "353951"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Projektiarvioiden synkronointi suoraan Project Service Automationista Finance and Operationsin projektitoimintoihin

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään malleja ja tehtäviä, joilla projektin tunti- ja kuluarviot synkronoidaan suoraan Microsoft Dynamics 365 for Project Service Automationista Dynamics 365 for Finance and Operationsiin.

> [!NOTE]
> - Projektitehtävän integrointi, kulutapahtumaluokat, tuntiarviot, kuluarviot ja toiminnon lukitseminen ovat käytössä Microsoft Dynamics 365 for Finance and Operationsin versiossa 8.0.
> - Todellisten tietojen integrointi on mahdollista Microsoft Dynamics 365 for Finance and Operationsin versiossa 8.0.1 tai sitä uudemmassa versiossa.
> - Jos käytössä on Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0 ja KB 4132657 ja KB 4132660 on asennettu, voit integroida projektitehtäviä, kulutapahtumaluokkia, tuntiarvioita, kuluarvioita ja todellisia tietoja sekä määrittää toimintojen lukituksen. Jos kirjanpidollinen jako on palautettava alkuperäisasetuksiin, myös KB 4131710 kannattaa asentaa.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Tiedonkulku Project Service Automationista Finance and Operationsiin

Project Service Automationin ja Finance and Operationsin välinen integrointiratkaisu synkronoi Project Service Automationin ja Finance and Operationsin esiintymien tiedot tietojen integrointiominaisuudella. Tietojen integrointiominaisuudessa käytettävissä olevat integrointimallit mahdollistavat projektin tunti- ja kuluarviointeja koskevan tiedonkulun Project Service Automationista ja Finance and Operationsiin.

Seuraava kuva ilmaisee, miten tiedot synkronoidaan Project Service Automationin ja Finance and Operationsin välillä.

[![Project Service Automationin ja Finance and Operationsin välisen integroinnin tiedonkulku](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Projektien tuntiarvioita

### <a name="template-and-tasks"></a>Malli ja tehtävät

Saat käytettävissä olevat mallit käyttöösi valitsemalla Microsoft PowerAppsin hallintakeskuksessa **Projektit**. Valitse sitten julkiset mallit valitsemalla oikeassa yläkulmassa **Uusi projekti**.

Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoimaan projektin tuntiarviot Project Service Automationista Finance and Operationsiin:

- **Mallin nimi tietojen integroinnissa:** Projektin tuntiarviot (PSA:sta Fin and Opsiin)
- **Projektin tehtävien nimi:**

    - Tapahtumasuhteet
    - Kuluarviot

### <a name="entity-set"></a>Yksikköjoukko

| Project Service Automation | Finance and Operations                        |
|----------------------------|-----------------------------------------------|
| Projektitehtävät              | Projektin tuntiarvioiden integrointiyksikkö |

### <a name="entity-flow"></a>Yksikön työnkulku

Projektin tuntiarvioita hallitaan Project Service Automationissa ja ne synkronoidaan Finance and Operationsiin projektin tuntiennusteisiin.

### <a name="prerequisites"></a>Edellytykset

Projektin, projektitehtävien ja projektin kuluarvion tapahtumaluokat on synkronoitava, ennen kuin projektin tuntiarviot voidaan synkronoida.

### <a name="power-query"></a>Power Query

Projektin tuntiarvioiden mallissa on käytettävä Microsoft Power Query for Exceliä seuraavien toimintojen päivittämiseen:

- Määritettävää oletusennustemallin tunnusta käytetään, kun integrointi luo uusi tuntiennusteita.
- Sellaisten tehtävän resurssikohteisten tietueiden suodattaminen pois, jotka aiheuttavat tuntiennusteisiin tapahtuvan integroinnin epäonnistumisen.
- Tyhjien tapahtumaluokkarivien suodattaminen pois. Jos suodatusta ei tehdä valmiiksi, tuloksena voi olla virheellisiä tuntiennusteita

#### <a name="set-the-default-forecast-model-id"></a>Aseta ennustemallin oletusarvon tunnus.

Voit päivittää malliin oletusennustemallin tunnuksen avaamalla määrityksen napsauttamalla **Yhdistä**-nuolta. Valitse sitten **Kyselyn ja suodatuksen lisäasetukset** -linkki.

- Jos käytät projektin tuntiarvioita (PSA:sta Fin and Opsiin) -oletusmallia, valitse **Lisätty ehto** **Käytetyt vaiheet** -listassa. Vaihda **Toiminto**-merkinnän **O\_forecast** tilalle sen ennustemallin tunnuksen nimi, jota käytetään integraatiossa. Oletusmallin ennustemalli tunnus on saatu esittelytiedoista.
- Jos luot uuden mallin, sinun on lisättävä tämä sarake. Valitse Power Queryssä **Lisää ehtosarake** ja anna uudelle sarakkeelle nimi, kuten **Mallin tunnus**. Anna sarakkeelle ehto, jonka mukaan jos projektitehtävä ei ole tyhjäarvo, niin \<anna ennustemallin tunnus\>; muutoin tyhjäarvo.

#### <a name="filter-out-resource-specific-records"></a>Resurssikohtaisten tietueiden suodattaminen

Projektin tuntiarviot (PSA:sta Fin and Opsiin) -mallissa on oletussuodatin, joka poistaa kaikki resurssikohtaiset tietueet. Jos luot oman mallin, tämä suodatin on lisättävä. Valitse **Advanced Query and Filtering** -linkki suodattaaksesi **msdyn\_islinetask** -sarakkesta niin, että vain **Epätosi** -asiakirjat ovat mukana.

#### <a name="filter-out-empty-transaction-category-rows"></a>Tyhjien tapahtumaluokkarivien suodattaminen

Kaikki tyhjiä tapahtumaluokkia sisältävät rivit poistava suodatin on lisättävä. Tämä tehtävä vaaditaan riippumatta siitä, käytätkö oletusmallia vai luotko oman mallin. Tämä suodatin poistaa kaikki Project Service Automationin yhteenvetorivit, joiden vuoksi Finance and Operationsin tuntiennusteet voisivat olla virheellisiä. Valitse **Advanced Query and Filtering** -linkki poissuodattaaksesi tyhjäarvoiset tietueet **msdyn\_transactioncategory\_value** -sarakkeessa.

### <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

Seuraavassa kuvassa on esimerkki mallitehtävän yhdistämisestä tietojen integroinnin yhteydessä. Yhdistämismääritys näyttää Project Service Automationista Finance and Operationsiin synkronoitavan kentän tiedot.

[![Mallin yhdistäminen](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Projektin kustannusarviot

### <a name="template-and-tasks"></a>Malli ja tehtävät

Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoimaan projektin kuluarviot Project Service Automationista Finance and Operationsiin:

- **Mallin nimi tietojen integroinnissa:** Projektin kuluarviot (PSA:sta Fin and Opsiin)
- **Projektin tehtävien nimi:**

    - Tapahtumasuhteet 
    - Kuluarviot

### <a name="entity-set"></a>Yksikköjoukko

| Project Service Automation | Finance and Operations                                   |
|----------------------------|----------------------------------------------------------|
| Tapahtumayhteydet    | Projektin tapahtumasuhteiden integrointiyksikkö |
| Arviorivit             | Projektin kuluarvioiden integrointiyksikkö         |

### <a name="entity-flow"></a>Yksikön työnkulku

Projektin kuluarvioita hallitaan Project Service Automationissa ja ne synkronoidaan Finance and Operationsiin projektin kuluennusteisiin.

### <a name="prerequisites"></a>Edellytykset

Projektin, projektitehtävien ja projektin kuluarvion tapahtumaluokat on synkronoitava, ennen kuin projektin kuluarviot voidaan synkronoida.

### <a name="power-query"></a>Power Query

Projektin kuluarviomallissa on käytettävä Power Query for Exceliä seuraavien toimintojen päivittämiseen:

- Vain kuluarviorivien tietueet sisällyttävä suodatus.
- Määritettävää oletusennustemallin tunnusta käytetään, kun integrointi luo uusi tuntiennusteita.
- Laskutustyyppien muuntaminen.
- Tapahtumatyyppien muuntaminen.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Vain kuluarviorivit sisällyttävä suodatus

Projektin kuluarviot (PSA:sta Fin and Opsiin) -mallissa oletussuodatin, joka sisällyttää integraatioon vain kulurivit. Jos luot oman mallin, tämä suodatin on lisättävä. Valitse **Tapahtumasuhde**-tehtävä ja napsauta **Yhdistä**-nuolta avataksesi kartoituksen. Valitse **Kyselyn ja suodatuksen lisäasetukset** -linkki. Suodata **msdyn\_transactiontype1** -sarake niin, että se sisältää vain **msdyn\_estimateline** -tiedoston.

#### <a name="set-the-default-forecast-model-id"></a>Aseta ennustemallin oletusarvon tunnus.

Voit päivittää malliin oletusennustemallin tunnuksen avaamalla **Kuluarvio**-tehtävän ja sitten napsauttaa **Yhdistä**-nuolta avataksesi kartoituksen. Valitse **Kyselyn ja suodatuksen lisäasetukset** -linkki.

- Jos käytät projektin kuluarvioiden oletusmallia (PSA:sta Fin and Opsiin), Power Queryssä, valitse ensimmäinen **Lisätty ehto** **Käytetyt vaiheet** -osassa. Vaihda **Toiminto**-merkinnän **O\_forecast** tilalle sen ennustemallin tunnuksen nimi, jota käytetään integraatiossa. Oletusmallin ennustemalli tunnus on saatu esittelytiedoista.
- Jos luot uuden mallin, sinun on lisättävä tämä sarake. Valitse Power Queryssä **Lisää ehtosarake** ja anna uudelle sarakkeelle nimi, kuten **Mallin tunnus**. Anna sarakkeelle ehto, jonka mukaan jos arviorivin tunnus ei ole tyhjäarvo, niin \<anna ennustemallin tunnus\>; muutoin tyhjäarvo.

#### <a name="transform-the-billing-types"></a>Laskutustyyppien muuntaminen

Projektin kuluarviot (PSA to Fin and Ops) -malliin kuuluva ehtosarake, joka muuntaa Project Service Automationista vastaanotetut laskutustyypit integroinnin aikana. Jos luot oman mallin, tämä ehtosarake on lisättävä. Valitse **kyselyn ja suodatuksen** linkki ja valitse sitten **Lisää ehtosarake**. Anna sarakkeelle uusi nimi, kuten **Laskutustyyppi**. Anna sitten seuraava ehto:

Jos **msdyn\_billingtype** = 192350000, silloin **NonChargeable**  
Jos **msdyn\_billingtype** = 192350001, silloin **Chargeable**  
Jos **msdyn\_billingtype** = 192350002, silloin **Complimentary**  
muuta **NotAvailable**

#### <a name="transform-the-transaction-types"></a>Tapahtumatyyppien muuntaminen

Projektin kuluarviot (PSA to Fin and Ops) -malliin kuuluva ehtosarake, joka muuntaa Project Service Automationista vastaanotetut tapahtumatyypit integroinnin aikana. Jos luot oman mallin, tämä ehtosarake on lisättävä. Valitse **kyselyn ja suodatuksen** linkki ja valitse sitten **Lisää ehtosarake**. Anna sarakkeelle uusi nimi, kuten **Tapahtumatyyppi**. Anna sitten seuraava ehto:

Jos **msdyn\_transactiontypecode** = 192350000, silloin **Cost**  
jos **msdyn\_transactiontypecode** = 192350005, then **Sales**  
else **null**

### <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

Seuraavissa kuvissa on esimerkkejä mallitehtävän yhdistämisistä tietojen integroinnin yhteydessä. Yhdistämismääritys näyttää Project Service Automationista Finance and Operationsiin synkronoitavan kentän tiedot.

[![Mallin yhdistäminen](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Mallin yhdistäminen](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)
