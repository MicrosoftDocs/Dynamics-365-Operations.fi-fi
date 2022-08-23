---
title: Määritysten lopettaminen RCS:n yleisessä säilössä
description: Tässä artikkelissa kuvataan määritysten lopettaminen RCS:n yleisessä säilössä.
author: gionoder
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2021-02-02
ms.dyn365.ops.version: AX 10.0.14
ms.custom: 97423
ms.assetid: ''
ms.search.form: ERSolutionTable, ERWorkspace
ms.openlocfilehash: b0605f56058e3c93ea088ee8386ba26c4ce2b65a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272333"
---
# <a name="discontinue-configurations-in-the-rcs-global-repository"></a>Määritysten lopettaminen RCS:n yleisessä säilössä

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan määrityksen lopettaminen RCS:n yleisessä säilössä. Aiemmin vain ne konfiguraatiot, joita ei enää tarvita, oli mahdollista poistaa. Nyt voit kuitenkin merkitä vapautetun konfiguraation **Lopetettu**-arvolla RCS:n yleisessä tietovarastossa. Tämän toiminnallisuuden avulla voit myös hallita seuraavia: 
 
 - Toimita etukäteisilmoitukset, kun konfiguraatio on tarkoitus lopettaa.
 - Sisällytä korvaavaa konfiguraatiota koskevat soveltuvat tiedot.
 - Määritä tietyn konfiguraation **Tuen päättymispäivämäärä**, joka ilmoittaa käyttäjälle, milloin se lopetetaan.

Kun lopetat konfigurointiversion, voit määrittää seuraavat valinnaiset tiedot:

  - **Korvauskonfiguraatio**
  - **Korvaava konfigurointiversio**
  - **Vapaatekstihuomautus**: Tämän kentän avulla voit antaa dokumentaatiolinkkejä tai viitteitä
  - **Tuen päättymispäivämäärä**: Tämä kenttä sisältää ehdotetun päivämäärän, johon saakka nykyistä konfiguraatiota/versiota tuetaan. Tämä päivämäärä on päivitettävä manuaalisesti.
  
Lopeta konfiguraatio noudattamalla seuraavia ohjeita. 

1. Valitse, haluatko lopettaa yhden version vai kaikki versiot, joilla on samat asetukset, yhdessä vaiheessa, määrittämällä **Kaikki versiot** -asetukseksi **Kyllä**. 
2. Määritä **Lopeta**-parametriksi **Kyllä**.
3. Lopeta konfiguraatiot valitsemalla **OK**. **Lopetuspäivämäärä**-kenttä täytetään, kun tallennat muutokset.

![Konfiguraation lopettamisen tiedot.](media/Discontinue-details-2.png)
  
Voit palauttaa konfiguraation takaisin **jaetuksi** tai muokata lopetuksen tietoja milloin tahansa. Jos jaat konfiguraation, määritä **Tuen päättymispäivämäärä** ja kaikki muut muut lopettamiseen liittyvät tiedot, jotka osoittavat suunnitelmasi tulevasta lopettamisesta.

Jos haluat jakaa suunniteltua lopettamista koskevat tiedot ennen varsinaista konfiguratiion lopettamista, käyttäjä voi täydentää korvaamiseen liittyvät kentät, mutta jättää **Lopetus**-parametrin arvoksi **Ei**.

> [!NOTE]
> Lopettaminen ei rajoita työvaiheita konfiguraatioiden avulla. Konfiguraatioita voi edelleen tuoda, suorittaa tai johtaa – nämä kentät vain tiedoksi.

## <a name="finance-supports-displaying-this-information-starting-in-version-10014"></a>Finance tukee tämän tiedon näyttämista versiosta 10.0.14 alkaen

Dynamics 365 Finance tukee lopetustietojen näyttämistä versiosta 10.0.14 alkaen. **Yleinen tietovarasto** -sivulla voit tarkastella lopettamiseen liittyviä ajantasaisia tietoja. Oletusarvoisesti lopetetut konfiguraatiot suodatetaan pois.
  
**Tuodut konfiguraatiot** (ERSolutionTable) -sivulla näkyvät konfiguraatiot, jotka on jo lopetettu tuomisen aikana. Jos konfiguraatiot on lopetettu tuonnin jälkeen, lopetustiedot voi synkronoida suorittamalla **Tuo konfiguraatioiden päivitykset** -työn.


