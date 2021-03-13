---
title: Tietokannan lokikirjauksen määrittäminen ja hallinta
description: Voit seurata Dynamics 365 Human Resourcesin taulukoiden ja kenttien muutoksia tietokantakirjausten avulla.
author: andreabichsel
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 50346cc495fe08f49137dba59dbcbb3f7f838c7b
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/06/2021
ms.locfileid: "5129276"
---
# <a name="configure-and-manage-database-logging"></a>Tietokannan lokikirjauksen määrittäminen ja hallinta

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
2. Suorita ohjattu toiminto loppuun.

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
