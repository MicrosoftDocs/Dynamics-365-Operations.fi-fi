---
title: Projektiarvioiden synkronointi suoraan Project Service Automationista Finance and Operationsin projektitoimintoihin
description: Tässä ohjeaiheessa käsitellään malleja ja tehtäviä, joilla projektin tunti- ja kuluarviot synkronoidaan suoraan Microsoft Dynamics 365 Project Service Automationista Dynamics 365 Financeen.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: ebf0fce60ad006e798aa4f404fbffcf10a0b31f9
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770286"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Projektiarvioiden synkronointi suoraan Project Service Automationista Finance and Operationsin projektitoimintoihin

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään malleja ja tehtäviä, joilla projektin tunti- ja kuluarviot synkronoidaan suoraan Dynamics 365 Project Service Automationista Dynamics 365 Financeiin.

> [!NOTE]
> - Projektitehtävän integrointi, kulutapahtumaluokat, tuntiarviot, kuluarviot ja toiminnon lukitseminen ovat käytössä versiossa 8.0.
> - Todellisten tietojen integrointi on käytettävissä versiossa 8.0.1 tai sitä uudemmassa.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Tiedonkulku Project Service Automationista Financeen

Project Service Automationin ja Financen välinen integrointiratkaisu synkronoi Project Service Automation- ja Finance-esiintymien tiedot tietojen integrointiominaisuudella. Tietojen integrointiominaisuudessa käytettävissä olevat integrointimallit mahdollistavat projektin tunti- ja kuluarviointeja koskevan tiedonkulun Project Service Automationista ja Financeen.

Seuraava kuva ilmaisee, miten tiedot synkronoidaan Project Service Automationin ja Financen välillä.

[![Project Service Automationin ja Financen välisen integroinnin tiedonkulku](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Projektien tuntiarvioita

### <a name="template-and-tasks"></a>Malli ja tehtävät

Saat käytettävissä olevat mallit käyttöösi valitsemalla Microsoft Power Appsin hallintakeskuksessa **Projektit**. Valitse sitten julkiset mallit valitsemalla oikeassa yläkulmassa **Uusi projekti**.

Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoimaan projektin tuntiarviot Project Service Automationista Financeen:

- **Mallin nimi tietojen integroinnissa:** Projektin tuntiarviot (PSA:sta Fin and Opsiin)
- **Projektin tehtävien nimi:**

    - Tapahtumasuhteet
    - Kuluarviot

### <a name="entity-set"></a>Yksikköjoukko

| Project Service Automation | Myyntitiedot                                       |
|----------------------------|-----------------------------------------------|
| Projektitehtävät              | Projektin tuntiarvioiden integrointiyksikkö |

### <a name="entity-flow"></a>Yksikön työnkulku

Projektin tuntiarvioita hallitaan Project Service Automationissa ja ne synkronoidaan Financen projektin tuntiennusteisiin.

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

Kaikki tyhjiä tapahtumaluokkia sisältävät rivit poistava suodatin on lisättävä. Tämä tehtävä vaaditaan riippumatta siitä, käytätkö oletusmallia vai luotko oman mallin. Tämä suodatin poistaa kaikki Project Service Automationin yhteenvetorivit, joiden vuoksi Financen tuntiennusteet voisivat olla virheellisiä. Valitse **Advanced Query and Filtering** -linkki poissuodattaaksesi tyhjäarvoiset tietueet **msdyn\_transactioncategory\_value** -sarakkeessa.

### <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

Seuraavassa kuvassa on esimerkki mallitehtävän yhdistämisestä tietojen integroinnin yhteydessä. Yhdistämismääritys näyttää Project Service Automationista Financeen synkronoitavien kenttien tiedot.

[![Mallin yhdistäminen](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Projektin kustannusarviot

### <a name="template-and-tasks"></a>Malli ja tehtävät

Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoimaan projektin kuluarviot Project Service Automationista Financeen:

- **Mallin nimi tietojen integroinnissa:** Projektin kuluarviot (PSA:sta Fin and Opsiin)
- **Projektin tehtävien nimi:**

    - Tapahtumasuhteet 
    - Kuluarviot

### <a name="entity-set"></a>Yksikköjoukko

| Project Service Automation | Myyntitiedot                                                  |
|----------------------------|----------------------------------------------------------|
| Tapahtumayhteydet    | Projektin tapahtumasuhteiden integrointiyksikkö |
| Arviorivit             | Projektin kuluarvioiden integrointiyksikkö         |

### <a name="entity-flow"></a>Yksikön työnkulku

Projektin kuluarvioita hallitaan Project Service Automationissa ja ne synkronoidaan Financen projektin kuluennusteisiin.

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

Seuraavissa kuvissa on esimerkkejä mallitehtävän yhdistämisistä tietojen integroinnin yhteydessä. Yhdistämismääritys näyttää Project Service Automationista Financeen synkronoitavien kenttien tiedot.

[![Mallin yhdistäminen](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Mallin yhdistäminen](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)
