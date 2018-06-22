---
title: Projektin todellisten tietojen synkronointi Project Service Automationista suoraan projektin integroinnin kirjauskansioon Finance and Operationsiin kirjaamista varten
description: "Tässä ohjeaiheessa käsitellään malleja ja tehtäviä, joilla projektin todelliset tiedot synkronoidaan suoraan Microsoft Dynamics 365 for Project Service Automationista Dynamics 365 for Finance and Operationsiin."
author: KimANelson
manager: AnnBe
ms.date: 05/21/2018
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
ms.openlocfilehash: 85ff049852e0b00623f47a12fb66e2c9bb9c4151
ms.contentlocale: fi-fi
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-actuals-from-project-service-automation-directly-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Projektin todellisten tietojen synkronointi Project Service Automationista suoraan projektin integroinnin kirjauskansioon Finance and Operationsiin kirjaamista varten

Tässä ohjeaiheessa käsitellään malleja ja tehtäviä, joilla projektin todelliset tiedot synkronoidaan suoraan Microsoft Dynamics 365 for Project Service Automationista Dynamics 365 for Finance and Operationsiin.

Malli synkronoin tapahtumat Project Service Automationista Finance and Operationsin valmistelutaulukkoon. Synkronoinnin jälkeen tiedot on vietävä valmistelutaulukosta integroinnin kirjauskansioon.

> [!NOTE]
> Projektin todellisten tietojen integrointi on käytettävissä Dynamics 365 for Finance and Operationsin versiossa 8.01.

> [!NOTE]
> Jos kirjaat arvolisäverosummia aika- tai kulutapahtumia Project Service Automationissa, sinun on asennettava Project Service Automationin päivitys 7. Jos tätä päivitystä ei ole asennettu, todellisia verotietoja ei linkitetä liitettyihin todellisiin aika- tai kuluarvoihin eikä niitä synkronoida Finance and Operationsiin. Pyydä lisätietoja tuesta.


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Tiedonkulku Project Service Automationista Finance and Operationsiin

Project Service Automationin ja Finance and Operationsin välinen integrointiratkaisu synkronoi Project Service Automationin ja Finance and Operationsin esiintymien tiedot tietojen integrointiominaisuudella. Tietojen integrointiominaisuudessa käytettävissä olevat integrointimallit mahdollistavat projektin todellisia tietoja koskevan tiedonkulun Project Service Automationista Finance and Operationsiin.

Seuraava kuva ilmaisee, miten tiedot synkronoidaan Project Service Automationin ja Finance and Operationsin välillä.

[![Project Service Automationin ja Finance and Operationsin välisen integroinnin tiedonkulku](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)


## <a name="templates-and-tasks"></a>Mallit ja tehtävät

Saat käytettävissä olevat mallit käyttöösi valitsemalla Microsoft PowerAppsin hallintakeskuksessa **Projektit**. Valitse sitten julkaiset mallit valitsemalla oikeassa yläkulmassa **Uusi projekti**.

Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoimaan projektin todelliset tiedot Project Service Automationista Finance and Operationsiin:

-  **Mallin nimi tietojen integroinnissa:** projektin todelliset tiedot (PSA:sta Fin and Opsiin)

-  **Projektin tehtävien nimi:** 
    - Todelliset 
    - Tapahtumayhteydet

## <a name="entity-set"></a>Yksikköjoukko

| Project Service Automation      | Finance and Operations                                      |
|---------------------------------|-------------------------------------------------------------|
| Todelliset                         | Projektin todellisten tietojen integrointiyksikkö                      |
| Tapahtumayhteydet         | Projektin tapahtumasuhteiden integrointiyksikkö    |

## <a name="entity-flow"></a>Yksikön työnkulku

Projektin todellisia tietoja hallitaan Project Service Automationissa ja ne synkronoidaan Finance and Operationsin projektin integroinnin kirjauskansioon. Kirjanpitoa sovelletaan taloushallinnon oletusdimensioiden ja kirjausasetusten perusteella.

## <a name="preconditions"></a>Ennakkoehdot

Ennen todelliset tiedot voidaan synkronoida, Project Service Automationin integrointiparametrit on määritettävä sekä projektit, projektitehtävät ja projektin kulutapahtumaluokat synkronoitava.

## <a name="power-query"></a>Power Query

Projektin todellisten tietojen mallissa on käytettävä Microsoft Power Queryä. Sen avulla voidaan tehdään seuraavat toiminnot:
- Project Service Automationin **tapahtumatyyppi** muunnetaan oikeaksi Finance and Operationsin **tapahtumatyypiksi**. Projektin todellisten tietojen mallissa (PSA:sta Fin and Opsiin) tämä muunnos on määritetty valmiiksi.
- Project Service Automationin **laskutustyyppi** muunnetaan oikeaksi Finance and Operationsin **laskutustyypiksi**. Projektin todellisten tietojen mallissa (PSA:sta Fin and Opsiin) tämä muunnos on määritetty valmiiksi. Laskutustyyppi yhdistetään sitten **rivin ominaisuuteen** Dynamics 365 for Project Service Automationin integrointiparametrilomakkeen määrityksen mukaisesti.
- Suodata esiin tällä mallilla synkronoitavat **resurssin organisaatioyksiköt**.
- Jos **konsernin sisäisen todellisen ajan tai konsernin sisäisten todellisten kulujen tiedot** synkronoidaan Finance and Operationsiin, **sopimuksen organisaatioyksikkö** on muunnettava oikeaksi **yritykseksi** Finance and Operationsissa. Projektin todellisten tietojen mallissa (PSA:sta Fin and Opsiin) on esittelytietojen perusteella määritetty ehtosarake. Viimeksi lisätty ehtosarake on päivitettävä oikeiksi yrityksiksi. Jos päivitystä ei tehdä, tuloksena voi olla integrointivirhe tai Finance and Operationsiin tuotavat tapahtumien todelliset tiedot ovat virheellisiä.
- Jos **konsernin sisäisen todellista aikaa tai konsernin sisäisten todellisten kulujen tietoja** ei synkronoida Finance and Operationsiin, viimeksi lisätty ehtosarake on poistettava mallista. Jos päivitystä ei tehdä, tuloksena voi olla integrointivirhe tai Finance and Operationsiin tuotavat tapahtumien todelliset tiedot ovat virheellisiä.

### <a name="contract-organizational-unit"></a>Sopimuksen organisaatioyksikkö
Voit päivittää malliin lisätyn ehtosarakkeen, avaa määritys napsauttamalla **Yhdistä**-nuolta. Avaa kyselyn ja suodatuksen lisäasetukset valitsemalla.
- Jos käytät Microsoft Projectin todellisten tietojen oletusmallia (PSA:sta Fin and Opsiin), valitse viimeinen **Lisätty ehto** **Käytetyt vaiheet** -osassa. Vaihda **Toiminto**-merkinnän **USSI** tilalle sen **yrityksen** nimi, jota käytetään integraatiossa. Lisää tarvittaessa lisäehtoja **Toiminto**-merkintään ja päivitä **else**-ehto **USMF** oikeaksi **yritykseksi**.
- Jos olet luomassa uutta mallia, tämä sarake on lisättävä tukemaan konsernin sisäistä aikaa ja kuluja. Valitse **Lisää ehtosarake** ja anna sarakkeelle nimi, kuten Yritys. Anna sarakkeelle ehto, jonka mukaan jos msdyn_contractorganizationalunitid.msdyn_name on <organizational unit>, niin <enter the Legal entity>; muuten tyhjäarvo.

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

Seuraavassa kuvassa on esimerkki mallitehtävän yhdistämisestä tietojen integroinnin yhteydessä. Yhdistämismääritys näyttää Project Service Automationista Finance and Operationsiin synkronoitavan kentän tiedot.

[![Mallin yhdistäminen](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Mallin yhdistäminen](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table"></a>Tuo valmistelutaulukosta

Säännöllinen valmistelutaulukon tuontiprosessi on suoritettava sen jälkeen, kun todelliset tiedot on synkronoitu Project Service Automationista Finance and Operationsiin. Tämä prosessi tuo projektitapahtumat valmistelutaulukosta Project Service Automationin integroinnin kirjauskansioon, jossa käytetään kirjanpitoa ja tuodut tapahtumat voidaan kirjata. Tämä prosessi kannattaa suorittaa erätilassa. Lisäksi sen voi määrittää toistuvana eränä suoritettavaksi.

## <a name="update-actuals"></a>Todellisten tietojen päivittäminen

Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoimaan Finance and Operationsista Project Service Automationiin kirjattujen projektitapahtumien tositenumero ja arvonlisäverot.

-  **Mallin nimi tietojen integroinnissa:** projektin todellisten tietojen päivitys (Fin and Opsista PSA:han)
-  **Projektin tehtävien nimi:** 
     - Todelliset 
     - Tapahtumayhteydet

## <a name="entity-set"></a>Yksikköjoukko

| Finance and Operations                                         | Project Service Automation        |
|----------------------------------------------------------------|-----------------------------------|
| Projektin todellisten tietojen integrointiyksikkö                         | Todelliset                           |
| Projektin tapahtumasuhteiden integrointiyksikkö       | Tapahtumayhteydet           |

## <a name="entity-flow"></a>Yksikön työnkulku

Projektin todellisia tietoja hallitaan Project Service Automationissa ja ne synkronoidaan Finance and Operationsin projektin integroinnin kirjauskansioon. Kun todelliset tiedot on kirjattu Finance and Operationsissa, ne päivitetään Project Service Automationissa Finance and Operationsin tositenumerolla. Jos arvonlisäverot lisättiin Finance and Operationsissa, verojen uudet todelliset tiedot luodaan Project Service Automationissa.

## <a name="power-query"></a>Power Query

Projektin todellisten tietojen mallissa on käytettävä Microsoft Power Queryä. Sen avulla voidaan päivittää seuraavat toiminnot:
- Finance and Operationsin **tapahtumatyyppi** muunnetaan oikeaksi Project Service Automationin **tapahtumatyypiksi**. Projektin todellisten tietojen päivitysmallissa (Fin Opsiin PSA:han) tämä muunnos on määritetty valmiiksi.
- Finance and Operationsin **laskutustyyppi** muunnetaan oikeaksi Project Service Automationin **laskutustyypiksi**. Projektin todellisten tietojen päivitysmallissa (Fin Opsiin PSA:han) tämä muunnos on määritetty valmiiksi.

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

Seuraavissa kuvissa on esimerkkejä mallitehtävän yhdistämisistä tietojen integroinnin yhteydessä. Yhdistämismääritys näyttää Finance and Operationsista Project Service Automationiin synkronoitavan kentän tiedot.

[![Mallin yhdistäminen](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Mallin yhdistäminen](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)




