---
title: Tietokannan lokikirjauksen määrittäminen ja hallinta
description: Voit seurata Dynamics 365 Human Resourcesin taulukoiden ja kenttien muutoksia tietokantakirjausten avulla.
author: twheeloc
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8faf0be5f094f18b75f2263fa622c9b7f3983274
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899760"
---
# <a name="configure-and-manage-database-logging"></a>Tietokannan lokikirjauksen määrittäminen ja hallinta


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Voit seurata Dynamics 365 Human Resourcesin taulukoiden ja kenttien muutoksia tietokantakirjausten avulla. Tässä artikkelissa käsitellään seuraavia:

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
2. Valitse **Suodatus** **Sisällytettävät tietueet** -osassa.
3. Valitse poistettavien lokien valitsemismenetelmä. Valitse jompikumpi seuraavista vaihtoehdoista:

   - Taulun ID-tunnus
   - Lokin tyyppi
   - Luonnin päivämäärä ja aika

4. Määritä lokin tyhjentämistehtävän suorittamisen ajankohta **Tietokantalokin tyhjentäminen** -välilehdessä. Tietokantalokit ovat oletusarvoisesti käytettävissä 30 päivää.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
