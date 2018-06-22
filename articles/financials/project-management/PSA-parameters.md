---
title: Project Service Automationin integrointiparametrit
description: "Voit määrittää, mitkä ovat tietojen oletusarvot, kun Project Service Automation integroidaan Dynamics 365 for Finance and Operationsin kanssa."
author: KimANelson
manager: AnnBe
ms.date: 12/13/2017
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
ms.openlocfilehash: 32f7f70c5b1071cef5a3360ccc09fa2d95fbf9a9
ms.contentlocale: fi-fi
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation-integration-parameters"></a>Project Service Automationin integrointiparametrit

Voit määrittää **Project Service Automationin integrointiparametrit** -sivulla, mitkä ovat tietojen oletusarvoja, kun Project Service Automation integroidaan Finance and Operationsin kanssa. Seuraavat on määritettävä, jotta projektien voidaan synkronoida Project Service Automationista Finance and Operationsissa.

> [!NOTE]
> Projektitehtävien integrointi, kulutapahtumaluokat, tuntiarviot, kuluarviot ja toiminnon lukitseminen ovat käytössä Dynamics 365 for Finance and Operationsin versiossa 8.0.




| **Välilehti**                      | **Kenttä**                          | **Kuvaus**                    |
|------------------------------|------------------------------------|--------------------------------|
| **Yleiset**                  | **Oletusprojektityyppi**               | Valitse **projektityypin** oletusarvo. Tätä arvoa käytetään, kun Project Service Automationista synkronoitaville projekteille ei ole annettu oletusarvoa integrointimallissa. Synkronoinnin aikana uusien projektien **projektityypiksi** on määritetty tämä arvo, ja se voidaan päivittää, kun projektin sopimusrivit synkronoidaan Project Service Automationista.               |
| **Yleiset**                  | **Aikaluokka**                      | Valitse **aikaluokan** oletusarvo, jota käytetään, kun tuntiarviot synkronoidaan Project Service Automationista. Synkronoinnin aikana Finance and Operationsin uusien projektien tuntiennusteiden **Luokka**-arvona on tämä arvo, kun tuntiarviot ja todelliset tuntitiedot synkronoidaan Project Service Automationista.   |
| **Yleiset**                  | **Maksuluokka**                       | Valitse **maksuluokan** oletusarvo, jota käytetään, kun todelliset maksutiedot synkronoidaan Project Service Automationista. Synkronoinnin aikana Finance and Operationsin uusien maksutapahtumien **Luokka**-arvona on tämä arvo, kun todelliset maksutiedot synkronoidaan Project Service Automationista.          |
| **Projektiryhmän oletusarvot**   | **Projektityyppi** | Lisää uusi rivi valitsemalla **Uusi**. Tällä tavoin lisätyllä rivillä voi valita projektityypin, jonka mukaan oletusprojektiryhmä määritetään. Tietyn projektityypin voi valita vain kerran kussakin määrityksessä.              
|                              | **Projektiryhmä**          | Valitse oletusprojektiryhmä tietylle projektityypille. Kun uusia projekteja synkronoidaan Project Service Automationissa, **projektiryhmä** on projektityyppiin perustuva oletusarvo, jos oletusarvoa ei ole annettu integrointimallissa.  |
| **Laskutustyypin oletusarvot**    | **Laskutustyyppi** | Lisää uusi rivi valitsemalla **Uusi**. Tällä tavoin lisätyllä rivillä voi valita laskutustyypin, jonka mukaan oletusriviominaisuus määritetään. Tietyn laskutustyypin voi valita vain kerran kussakin määrityksessä.          |
|                              | **Rivin ominaisuus**| Valitse oletusriviominaisuus tietylle laskutustyypille. Kun uudet tuntiarviot, kuluarviot tai uudet todelliset tiedot synkronoidaan Project Service Automationista, **Riviominaisuus** on laskutustyyppiin perustuva oletusarvo.          |
| **Toimintojen lukitus**    |                   | Valitse toiminto, jolla Finance and Operations poistetaan käytöstä Project Service Automationista peräisin olevissa projekteissa ja sopimuksissa. Voit esimerkiksi poistaa käytöstä mahdollisuuden muokata sopimuksia ja projekteja, luoda työrakenteita ja kirjata aikaraportteja Finance and Operationsissa. Kirjanpitoon liittyvät kentät ovat edelleen käytössä, vaikka parametriasetus on poistanut ne käytöstä. Kaikki toiminnot on oletusarvoisesti otettu käyttöön.           |

