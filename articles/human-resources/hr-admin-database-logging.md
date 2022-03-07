---
title: Tietokannan lokikirjauksen määrittäminen ja hallinta
description: Voit seurata Dynamics 365 Human Resourcesin taulukoiden ja kenttien muutoksia tietokantakirjausten avulla.
author: andreabichsel
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d22ff9f3ce68c81f37840342c795d7d162eb027b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801332"
---
# <a name="configure-and-manage-database-logging"></a>Tietokannan lokikirjauksen määrittäminen ja hallinta

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Voit seurata Dynamics 365 Human Resourcesin taulukoiden ja kenttien muutoksia tietokantakirjausten avulla. Tässä ohjeaiheessa käsitellään seuraavia:

- Tietokantakirjauksen suojauksen ja suorituskyvyn hallinta
- Määritä tietokantakirjaus
- Tietokantalokien tyhjentäminen

## <a name="overview-of-database-logging"></a>Tietokantakirjauksen yleiskatsaus

Tietokantakirjaus seuraa Microsoft Dynamics 365 Human Resourcesin taulukoiden ja kenttien muutoksia. Lisääminen, päivittäminen tai poistaminen ovat tällaisia muutoksia. Tietokantakirjaus tallentaa tietueen taulukoiden tai kenttien muutoksista tietokantakirjaustaulukkoon.

Tietokantakirjauksen käyttötapoja liiketoiminnassa:

- Arkaluonteisia tietoja sisältäviin taulukoihin tehtyjen muutosten seurantatietueen luominen.
- Yksittäisten tapahtumien seuraaminen. Tietokantakirjausta ei ole tarkoitettu erätöissä suoritettavien automaattisten tapahtumien seuraamiseen.

## <a name="security-for-database-logging"></a>Tietokantakirjauksen suojaus

Tietokantalokeissa voi olla arkaluonteisia tietoja. Lokitietojen käyttöoikeuden voi rajoittaa vain niille käyttöoikeusrooleille, joiden on voitava käyttää näitä tietoja.

## <a name="database-logging-and-performance"></a>Tietokantakirjaus ja suorituskyky

Vaikka tietokantakirjaus voi olla arvokasta liiketoiminnan kannalta, se voi kuluttaa paljon resursseja ja edellyttää paljon hallintaa. Tietokantakirjauksen vaikutukset suorituskykyyn:

- Tietokantalokitaulukon koko voi kasvaa nopeasti, mikä puolestaan voi kasvattaa tietokannan kokoa. Kasvu määräytyy sen mukaan, kuinka paljon lokiin kirjattuja tietoja päätät säilyttää. Tietokantalokitaulukko sisältää oletusarvoisesti vain 30 päivän lokitiedot. 

- Tietokantakirjaus voi heikentää pitkäkestoisia automaattisia prosesseja, kuten pitkään kestäviä tietojen tuontia.

### <a name="best-practices"></a>Parhaat käytännöt

Voit parantaa suorituskykyä rajaamalla lokikirjausten määrää ja valitsemalla lokiin tiettyjä kenttiä koko taulujen sijaan. Kokonaissuorituskykyä ylläpidetään rajoittamalla tietokantakirjaus 20 taulukkoon.

> [!NOTE]
> Yksittäisten kenttien osalta lokiin voidaan kirjata vain päivitykset.

## <a name="set-up-database-logging"></a>Määritä tietokantakirjaus

Tietokantakirjauksen voi määrittää käyttämällä ohjattua **Tietokantamuutosten kirjaaminen lokiin** -toimintoa. Ohjattu toiminto on joustava tapa määrittää taulukoiden tai kenttien lokiin kirjaaminen.

1. Valitse **Järjestelmänvalvoja > Linkit > Tietokanta > Tietokantalokin asetukset**. Käynnistä ohjattu **Tietokantamuutosten kirjaaminen lokiin** -toiminto valitsemalla **Uusi**.
2. Valitse **Seuraava**. 
3. Valitse ohjatun toiminnon **Taulut ja kentät** -sivulla taulut ja kentät, joille tietokannan lokiin kirjaamisen haluat ottaa käyttöön, ja valitse **Seuraava**.

   > [!Note]
   > Tietokannan lokiinkirjaus ei ole käytettävissä kaikissa Human Resources -tietokannan taulukoissa. Jos valitset **Näytä kaikki taulukot** luettelon alapuolella taulujen ja kenttien luettelo laajennetaan näyttämään kaikkien ne tietokantataulut, joiden tietokantaloki on käytettävissä, mutta tämä on kaikkien tietokantataulujen luettelon osajoukko.

4. Valitse ohjatun toiminnon **Muutostyypit**-sivulla tietotoiminnot, joiden muutoksia haluat seurata kullekin taululle ja kentälle, ja valitse sitten **Seuraava**. Alla olevassa taulukossa on lokiin kirjattavissa olevien tietotoimintojen kuvaus.
5. Tarkista tehdyt muutokset **Valmis**-sivulla ja valitse **Valmis**.

| Toiminto | kuvaus |
| -- | -- |
| Seuraa uusia tapahtumia | Luo loki tauluun luoduille uusille tietueille. |
| Päivitys | Luo loki taulutietueiden päivitystä varten tai taulun yksittäisten kenttien päivitykselle. Jos kirjaat lokiin taulun päivitykset, lokitietue luodaan aina, kun taulun mihin tahansa tietueen kenttään tehdään päivitys. Jos kirjaat lokiin tiettyjen kenttien päivitykset, lokitietue luodaan vain, kun taulutietueiden kyseisiin kenttiin tehdään päivityksiä. |
| Delete-näppäin | Luo loki taulusta poistettuja tietueita varten. |
| Nimeä tunnus uudelleen | Luo lokitietue, kun taulun avain nimetään uudelleen. |


## <a name="clean-up-database-logs"></a>Tietokantalokien tyhjentäminen

Voit poistaa kaikki tietokantalokit tai osan niistä seuraavien vaihtoehtojen avulla:

- Valitse kaikki tietyn taulukon lokit.
- Valitse tietyntyyppiset tietokantalokit,
- Valitse päivämäärä ja aika, jolloin loki luotiin.

Tietokantalokin tyhjentäminen määritetään seuraavasti: 

1. Valitse **Järjestelmänvalvoja > Linkit > Tietokanta > Tietokantaloki**. Valitse **Tyhjennä loki**.

2. Valitse poistettavien lokien valintamenetelmä antamalla jokin seuraavista vaihtoehdoista:

   - Taulun tunnus
   - Lokin tyyppi
   - Luonnin päivämäärä ja aika

3. Määritä lokin tyhjentämistehtävän suorittamisen ajankohta **Tietokantalokin tyhjentäminen** -välilehdessä. Tietokantalokit ovat oletusarvoisesti käytettävissä 30 päivää.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
