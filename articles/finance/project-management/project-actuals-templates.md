---
title: Projektin todellisten tietojen synkronointi Project Service Automationista suoraan projektin integroinnin kirjauskansioon Finance and Operationsiin kirjaamista varten
description: Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla projektin todelliset tiedot synkronoidaan suoraan Dynamics 365 Project Service Automationista Finance and Operationsiin.
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
ms.openlocfilehash: 302ac0f456dd8a24dc02948ee657e359f5a9c844
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770332"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Projektin todellisten tietojen synkronointi Project Service Automationista suoraan projektin integroinnin kirjauskansioon Finance and Operationsiin kirjaamista varten

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään malleja ja taustatehtäviä, joilla projektin todelliset tiedot synkronoidaan suoraan Dynamics 365 Project Service Automationista Dynamics 365 Financeiin.

Malli synkronoi tapahtumat Project Service Automationista Financen valmistelutaulukkoon. Synkronoinnin jälkeen tiedot **täytyy** viedä valmistelutaulukosta integroinnin kirjauskansioon.

> [!NOTE]
> - Projektin todellisten tietojen integrointi on mahdollista versioista 8.0.1 alkaen.
> - Jos käytät Enterprise edition -versiota 7.3.0 sen jälkeen, kun KB 4132657 ja KB 4132660 on asennettu, voit käyttää malleja integroidaksesi projektitehtäviä, kulutapahtumaluokkia, tuntiarvioita, kuluarvioita ja todellisia tietoja sekä määrittääksesi toimintojen lukituksen. Jos kirjanpidollinen jako on palautettava alkuperäisasetuksiin, myös KB 4131710 kannattaa asentaa.
> - Jos käytät versiota 7.3.0 ja tuot maksutapahtumia Project Service Automationista, sinun on asennettava KB 4345320, jotta maksut sisällytetään projektin laskuun.
> - Jos kirjaat arvolisäverosummia aika- tai kulutapahtumia Project Service Automationissa, sinun on asennettava Project Service Automationin päivitys 7. Muussa tapauksessa todellisia verotietoja ei linkitetä liitettyihin todellisiin aika- tai kuluarvoihin eikä niitä synkronoida Financeen. Pyydä lisätietoja tuesta.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Tiedonkulku Project Service Automationista Financeen

Project Service Automationin ja Financen välinen integrointiratkaisu synkronoi Project Service Automation- ja Finance-esiintymien tiedot tietojen integrointiominaisuudella. Tietojen integrointiominaisuudessa käytettävissä olevat integrointimallit mahdollistavat projektin todellisia tietoja koskevan tiedonkulun Project Service Automationista Financeen.

Seuraava kuva ilmaisee, miten tiedot synkronoidaan Project Service Automationin ja Financen välillä.

[![Project Service Automationin ja Finance and Operationsin välisen integroinnin tiedonkulku](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Projektin toteutuneet arvot Project Service Automationista

### <a name="template-and-tasks"></a>Malli ja tehtävät

Saat käytettävissä olevat mallit käyttöösi valitsemalla Microsoft Power Appsin hallintakeskuksessa **Projektit**. Valitse sitten julkiset mallit valitsemalla oikeassa yläkulmassa **Uusi projekti**.

Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoimaan projektin todelliset tiedot Project Service Automationista Financeen:

- **Mallin nimi tietojen integroinnissa:** projektin todelliset tiedot (PSA:sta Fin and Opsiin)
- **Projektin tehtävien nimi:**

    - Todelliset
    - Tapahtumayhteydet

### <a name="entity-set"></a>Yksikköjoukko

| Project Service Automation | Myyntitiedot                                   |
|----------------------------|----------------------------------------------------------|
| Todelliset                    | Projektin todellisten tietojen integrointiyksikkö                   |
| Tapahtumayhteydet    | Projektin tapahtumasuhteiden integrointiyksikkö |

### <a name="entity-flow"></a>Yksikön työnkulku

Projektin todellisia tietoja hallitaan Project Service Automationissa ja ne synkronoidaan Financen projektin integroinnin kirjauskansioon. Kirjanpitoa sovelletaan taloushallinnon oletusdimensioiden ja kirjausasetusten perusteella.

### <a name="prerequisites"></a>Edellytykset

Ennen todelliset tiedot voidaan synkronoida, Project Service Automationin integrointiparametrit on määritettävä sekä projektit, projektitehtävät ja projektin kulutapahtumaluokat synkronoitava.

### <a name="power-query"></a>Power Query

Projektin todellisten tietojen mallissa on käytettävä Microsoft Power Query for Exceliä seuraavien toimintojen päivittämiseen:

- Muunna Project Service Automationin tapahtumatyyppi oikeaksi tapahtumatyypiksi Financessa. Projektin todellisten tietojen mallissa (PSA:sta Fin and Opsiin) tämä muunnos on määritetty valmiiksi.
- Muunna Project Service Automationin laskutustyyppi oikeaksi laskutustyypiksi Financessa. Projektin todellisten tietojen mallissa (PSA:sta Fin and Opsiin) tämä muunnos on määritetty valmiiksi. Laskutustyyppi yhdistetään sitten rivin ominaisuuteen **Project Service Automationin integrointiparametrisivun** määrityksen mukaisesti.
- Suodata esiin tällä mallilla synkronoitavat resurssin organisaatioyksiköt.
- Jos konsernin sisäisen todellisen ajan tai konsernin sisäisten todellisten kulujen tiedot synkronoidaan Financeen, sopimuksen organisaatioyksikkö on muunnettava oikeaksi yritykseksi Financessa. Projektin todellisten tietojen mallissa (PSA:sta Fin and Opsiin) on esittelytietojen perusteella määritetty ehtosarake. Viimeksi lisätty ehdollinen sarake on päivitettävä oikeiksi yrityksiksi. Muuten tuloksena voi olla integrointivirhe tai Financeen tuotavat tapahtumien todelliset tiedot ovat virheellisiä.
- Jos konsernin sisäisen todellista aikaa tai konsernin sisäisten todellisten kulujen tietoja ei synkronoida Financeen, viimeksi lisätty ehdollinen sarake on poistettava mallista. Muuten tuloksena voi olla integrointivirhe tai Financeen tuotavat tapahtumien todelliset tiedot ovat virheellisiä.

#### <a name="contract-organizational-unit"></a>Sopimuksen organisaatioyksikkö
Voit päivittää malliin lisätyn ehdollisen sarakkeen, avaamalla määrityksen napsauttamalla **Yhdistä**-nuolta. Valitse **Kyselyn ja suodatuksen lisäasetukset** avataksesi Power Queryn.

- Jos käytät projektin todellisten tietojen oletusmallia (PSA:sta Fin and Opsiin), Power Queryssä, valitse viimeinen **Lisätty ehto** **Käytetyt vaiheet** -osassa. Vaihda **Toiminto**-merkinnän **USSI** tilalle sen yrityksen nimi, jota käytetään integraatiossa. Lisää tarvittaessa lisäehtoja **Toiminto**-merkintään ja päivitä **else**-ehto **USMF** oikeaksi yritykseksi.
- Jos olet luomassa uutta mallia, tämä sarake on lisättävä tukemaan konsernin sisäistä aikaa ja kuluja. Valitse **Lisää ehtosarake** ja anna sarakkeelle nimi, kuten **Yritys**. Määritä ehto sarakkeelle, jossa **msdyn\_contractorganizationalunitid.msdyn\_nimi** on \<organisaatioyksikkö\>, sitten \<lisää yritys\>; muuten null.

### <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

Seuraavissa kuvissa on esimerkki mallitehtävän yhdistämisestä tietojen integroinnin yhteydessä. Yhdistämismääritys näyttää Project Service Automationista Financeen synkronoitavien kenttien tiedot.

[![Mallin yhdistäminen](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Mallin yhdistäminen](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Tuo väliaikaisesta taulusta Project Service Automationin integroinnin jälkeen

Säännöllinen valmistelutaulukon tuontiprosessi on suoritettava sen jälkeen, kun todelliset tiedot on synkronoitu Project Service Automationista Financeen. Tämä prosessi tuo projektitapahtumat valmistelutaulukosta Project Service Automationin integroinnin kirjauskansioon, jossa käytetään kirjanpitoa ja tuodut tapahtumat voidaan kirjata. Tämä prosessi kannattaa suorittaa erätilassa, ja se voidaan määrittää toistuvana eränä suoritettavaksi.

## <a name="update-actuals-from-finance"></a>Päivitä todelliset tiedot Financesta

### <a name="template-and-tasks"></a>Malli ja tehtävät

Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoimaan kirjattujen projektitapahtumien tositenumero ja arvonlisäverot Financesta Project Service Automationiin:

- **Mallin nimi tietojen integroinnissa:** projektin todellisten tietojen päivitys (Fin and Opsista PSA:han)
- **Projektin tehtävien nimi:**

    - Todelliset 
    - Tapahtumayhteydet

### <a name="entity-set"></a>Yksikköjoukko

| Myyntitiedot                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Projektin todellisten tietojen integrointiyksikkö                   | Todelliset                    |
| Projektin tapahtumasuhteiden integrointiyksikkö | Tapahtumayhteydet    |

### <a name="entity-flow"></a>Yksikön työnkulku

Projektin todellisia tietoja hallitaan Project Service Automationissa ja ne synkronoidaan Financen projektin integroinnin kirjauskansioon. Kun todelliset tiedot on kirjattu Financeen, ne päivitetään Project Service Automationissa Financesta saadulla tositenumerolla. Jos arvonlisäverot lisättiin Financessa, verojen uudet todelliset tiedot luodaan Project Service Automationissa.

### <a name="power-query"></a>Power Query

Projektin todellisten tietojen päivitysmallissa on käytettävä Power Query for Exceliä seuraavien toimintojen päivittämiseen:

- Muunna Financen tapahtumatyyppi oikeaksi tapahtumatyypiksi Project Service Automationissa. Projektin todellisten tietojen päivitysmallissa (Fin Opsista PSA:han) tämä muunnos on määritetty valmiiksi.
- Muunna Financen laskutustyyppi oikeaksi laskutustyypiksi Project Service Automationissa. Projektin todellisten tietojen päivitysmallissa (Fin Opsista PSA:han) tämä muunnos on määritetty valmiiksi.

### <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

Seuraavissa kuvissa on esimerkkejä mallitehtävän yhdistämisistä tietojen integroinnin yhteydessä. Yhdistämismääritys näyttää Financesta Project Service Automationiin synkronoitavien kenttien tiedot.

[![Mallin yhdistäminen](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Mallin yhdistäminen](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)
