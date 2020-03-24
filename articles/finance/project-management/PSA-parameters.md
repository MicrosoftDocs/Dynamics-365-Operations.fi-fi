---
title: Project Service Automationin integrointiparametrit
description: Tässä ohjeaiheessa kerrotaan, miten oletustiedot kirjataan, kun integroit Microsoft Dynamics 365 for Project Service Automationin Microsoft Dynamics 365 Financen kanssa.
author: KimANelson
manager: AnnBe
ms.date: 03/03/2020
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
ms.openlocfilehash: cd09dad15112fd71bfd386e0072a77a4121c96e0
ms.sourcegitcommit: 236672932ffd0a758012ebb7b2df9bc51249c126
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096248"
---
# <a name="project-service-automation-integration-parameters"></a>Project Service Automation -integrointiparametrit

[!include[banner](../includes/banner.md)]

Voit määrittää **Project Service Automation -integrointiparametrit** -sivulla, miten oletustiedot lisätään, kun integroit Dynamics 365 Project Service Automationin Dynamics 365 Financein kanssa. Sinun on määritettävä seuraavat kentät, jotta projektit voidaan synkronoida onnistuneesti Project Service Automationista Financeen:

Voit avata **Project Service Automation -integrointiparametrit** -sivun siirtymällä **Projektinhallinta ja kirjanpito** \> **Asetukset** \> **Dynamics 365 for Project Service Automation -integrointiparametrit**. 

> [!NOTE]
> - Projektitehtävän integrointi, kulutapahtumaluokat, tuntiarviot, kuluarviot ja toiminnon lukitseminen ovat käytettävissä versiossa 8.0.
> - Todellisten tietojen integrointi on käytettävissä versiossa 8.0.1 tai sitä uudemmassa.


| Välilehti                    | Kenttä                | Kuvaus |
|------------------------|----------------------|-------------|
| Yleiset                | Oletusprojektilaji | Valitse oletusprojektityyppi. Tätä arvoa käytetään projekteja synkronoidessa, jos Project Service Automationista synkronoitaville projekteille ei ole annettu oletusarvoa integrointimallissa. Synkronoinnin aikana uusien projektien **Projektityyppi**-kenttään määritetään tämä arvo. Arvoa voi kuitenkaan päivitetä, kun projektin sopimusrivejä synkronoidaan Project Service Automationista. |
|                        | Aikaluokka        | Valitse oletusaikaluokka. Tätä arvoa käytetään, kun tuntiarvioita synkronoidaan Project Service Automationista. Kun tuntiennusteet ja toteutuneet tunnit synkronoidaan Project Service Automationista, Financen projektin uusien tuntiennusteiden **Luokka**-kenttä asetetaan tähän arvoon. |
|                        | Maksuluokka         | Valitse oletusmaksuluokka. Tätä arvoa käytetään, kun toteutuneita maksuja synkronoidaan Project Service Automationista. Kun toteutuneet maksut synkronisoidaan Project Service Automationista, uusien maksutapahtumien **Luokka**-kenttä asetetaan tähän arvoon. |
| Projektiryhmän oletusarvot | Projektityyppi         | Lisää uusi rivi valitsemalla **Uusi**. Tällä tavoin lisätyllä rivillä voi valita projektityypin, jolle oletusprojektiryhmä määritetään. Tietyn projektityypin voi valita vain yhden kerran kussakin määrityksessä. |
|                        | Projektiryhmä        | Valitse oletusprojektiryhmä valitulle projektityypille. Kun uusia projekteja synkronoidaan Project Service Automationissa, **projektiryhmä** -kentässä on projektityyppiin perustuva oletusarvo, jos oletusarvoa ei ole annettu integrointimallissa. |
| Laskutustyypin oletusarvot  | Laskutustyyppi         | Lisää uusi rivi valitsemalla **Uusi**. Tällä tavoin lisätyllä rivillä voi valita laskutustyypin, johon oletusriviominaisuus määritetään. Tietyn laskutustyypin voi valita vain yhden kerran kussakin määrityksessä. |
|                        | Rivin ominaisuus        | Valitse oletusriviominaisuus valitulle laskutustyypille. Kun uudet tuntiarviot, kuluarviot tai uudet todelliset tiedot synkronoidaan Project Service Automationista, **Riviominaisuus**-kenttä on laskutustyyppiin perustuva oletusarvo. |
| Toimintojen lukitus  | Ei käytettävissä       | Valitse toiminto, jolla Finance poistetaan käytöstä Project Service Automationista peräisin olevissa projekteissa ja sopimuksissa. Voit esimerkiksi poistaa käytöstä mahdollisuuden muokata sopimuksia ja projekteja, luoda työrakenteita ja kirjata aikaraportteja Financessa. Kirjanpitoon liittyvät kentät ovat edelleen käytössä, vaikka parametriasetus on poistanut ne käytöstä. Kaikki toiminnot on oletusarvoisesti otettu käyttöön. |
