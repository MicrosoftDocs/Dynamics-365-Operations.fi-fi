---
title: Project Service Automationin integrointiparametrit
description: Tässä ohjeaiheessa kerrotaan, miten oletustiedot kirjataan, kun integroit Microsoft Dynamics 365 for Project Service Automationin Microsoft Dynamics 365 for Finance and Operationsin kanssa.
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
ms.openlocfilehash: b58d2de323395db97d1f8ea146da55bba4e0f9c6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838980"
---
# <a name="project-service-automation-integration-parameters"></a>Project Service Automation -integrointiparametrit

[!include[banner](../includes/banner.md)]

Voit määrittää **Project Service Automation -integrointiparametrit** -sivulla, miten oletustiedot lisätään, kun integroit Microsoft Dynamics 365 for Project Service Automationin Microsoft Dynamics 365 for Finance and Operationsin kanssa. Seuraavat on kentät perustettava, jotta projektit voidaan synkronoida Project Service Automationista Finance and Operationsiin.

> [!NOTE]
> - Projektitehtävän integrointi, kulutapahtumaluokat, tuntiarviot, kuluarviot ja toiminnon lukitseminen ovat käytössä Microsoft Dynamics 365 for Finance and Operationsin versiossa 8.0.
> - Todellisten tietojen integrointi on mahdollista Microsoft Dynamics 365 for Finance and Operationsin versiossa 8.0.1 tai sitä uudemmassa versiossa.
> - Jos käytössä on Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0 ja KB 4132657 ja KB 4132660 on asennettu, voit integroida projektitehtäviä, kulutapahtumaluokkia, tuntiarvioita, kuluarvioita ja todellisia tietoja sekä määrittää toimintojen lukituksen. Jos kirjanpidollinen jako on palautettava alkuperäisasetuksiin, myös KB 4131710 kannattaa asentaa.

| Välilehti                    | Kenttä                | kuvaus |
|------------------------|----------------------|-------------|
| Yleiset                | Oletusprojektityyppi | Valitse oletusprojektityyppi. Tätä arvoa käytetään projekteja synkronoidessa, jos Project Service Automationista synkronoitaville projekteille ei ole annettu oletusarvoa integrointimallissa. Synkronoinnin aikana uusien projektien **Projektityyppi**-kenttään määritetään tämä arvo. Arvoa voi kuitenkaan päivitetä, kun projektin sopimusrivejä synkronoidaan Project Service Automationista. |
|                        | Aikaluokka        | Valitse oletusaikaluokka. Tätä arvoa käytetään, kun tuntiarvioita synkronoidaan Project Service Automationista. Kun tuntiennustet ja toteutuneet tunnit synkronoidaan Project Service Automationista, **Luokka**-kentän uudet projektien tuntiennusteet Finance and Operationsissa on asetettu tähän arvoon. |
|                        | Maksuluokka         | Valitse oletusmaksuluokka. Tätä arvoa käytetään, kun toteutuneita maksuja synkronoidaan Project Service Automationista. Kun toteutuneet maksut synkronisoidaan Project Service Automationista, **Luokka**-kentässä on tämä arvo, kun uudet maksutiedot synkronoidaan Finance and Operationsissa. |
| Projektiryhmän oletusarvot | Projektityyppi         | Lisää uusi rivi valitsemalla **Uusi**. Tällä tavoin lisätyllä rivillä voi valita projektityypin, jolle oletusprojektiryhmä määritetään. Tietyn projektityypin voi valita vain yhden kerran kussakin määrityksessä. |
|                        | Projektiryhmä        | Valitse oletusprojektiryhmä valitulle projektityypille. Kun uusia projekteja synkronoidaan Project Service Automationissa, **projektiryhmä** -kentässä on projektityyppiin perustuva oletusarvo, jos oletusarvoa ei ole annettu integrointimallissa. |
| Laskutustyypin oletusarvot  | Laskutustyyppi         | Lisää uusi rivi valitsemalla **Uusi**. Tällä tavoin lisätyllä rivillä voi valita laskutustyypin, johon oletusriviominaisuus määritetään. Tietyn laskutustyypin voi valita vain yhden kerran kussakin määrityksessä. |
|                        | Rivin ominaisuus        | Valitse oletusriviominaisuus valitulle laskutustyypille. Kun uudet tuntiarviot, kuluarviot tai uudet todelliset tiedot synkronoidaan Project Service Automationista, **Riviominaisuus**-kenttä on laskutustyyppiin perustuva oletusarvo. |
| Toimintojen lukitus  | Ei käytettävissä       | Valitse toiminto, jolla Finance and Operations poistetaan käytöstä Project Service Automationista peräisin olevissa projekteissa ja sopimuksissa. Voit esimerkiksi poistaa käytöstä mahdollisuuden muokata sopimuksia ja projekteja, luoda työrakenteita ja kirjata aikaraportteja Finance and Operationsissa. Kirjanpitoon liittyvät kentät ovat edelleen käytössä, vaikka parametriasetus on poistanut ne käytöstä. Kaikki toiminnot on oletusarvoisesti otettu käyttöön. |
