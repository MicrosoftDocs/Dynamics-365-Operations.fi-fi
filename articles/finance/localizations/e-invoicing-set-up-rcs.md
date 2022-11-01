---
title: Määritä Regulatory Configuration Service (RCS)
description: Tässä artikkelissa kuvataan, miten Regulatory Configuration Service (RCS) määritetään.
author: gionoder
ms.date: 10/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 32ced98925ee66e02f0b073b4acbd586666ac20c
ms.sourcegitcommit: 1ecfc1d8afb2201ab895ae6f93304ba2b120f14b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/21/2022
ms.locfileid: "9710778"
---
# <a name="set-up-regulatory-configuration-service-rcs"></a>Määritä Regulatory Configuration Service (RCS)

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan, miten Regulatory Configuration Service (RCS) määritetään.

## <a name="turn-on-globalization-features"></a>Globalisaatio-ominaisuuksien ottaminen käyttöön

1. Kirjaudu RCS-tilille.
2. Valitse **Ominaisuuksien hallinta** -ruutu.
3. **Valitse ominaisuuksien hallinta** -työtilassa luettelosta **globalisaation ominaisuudet** ja valitse sitten **Ota käyttöön nyt**.

**Globalisaatio-ominaisuudet** -työtilan ruudun pitäisi nyt näkyä RCS-päänäytössä.

## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>Määritä RCS-integroinnin parametrit sähköisen laskutuksen avulla

1. Valitse **Globalisaatiotoiminnot**-työtilan **Liittyvät asetukset** -osassa **Sähköisen raportoinnin parametrit**.
2. Kun määrität parametreja ensimmäisen kerran, sinua pyydetään muodostamaan yhteys Life Cycle Services (LCS) -ratkaisuun. Valitse **Muodosta yhteys Lifecycle Servicesiin napsauttamalla tästä** ja valitse yhteyden muodostamisen jälkeen **OK**.

    > [!IMPORTANT]
    > Jos tietojen sijaintia käytetään jossakin maassa tai jollakin alueella ja jos RCS:n valmistelualue on eri kuin LCS:n valmistelualue, saatat saada seuraavan yhteysvirhesanoman RCS:ssä: Pyynnön URI-tunnusta vastaavaa HTTP-resurssia ei löytynyt. Valitse **OK**. Saatat saada toisen virhesanoman RCS:ssä: Dynamics Lifecycle Services -palvelujen käyttäjätunnuksen luominen käyttäjän () puolesta epäonnistui. Ota yhteys järjestelmänvalvojaan.
    >  
    > Näin tapahtuu, koska LCS on yleinen palvelu ja se valmistellaan Yhdysvalloissa. Tietojen sijaintikäytännön vuoksi nykyisen alueen RCS ei voi muodostaa yhteyttä LCS:ään. Tähän on seuraavat 2 mahdollista ratkaisua:
    > - Poista RCS nykyiseltä alueelta ja luo se Yhdysvaltojen alueelle.
    > - Ohita virheet ja jatka sähköisen laskutuksen asetusten määrittämistä. Nämä virheet eivät vaikuta sähköiseen laskutuksen toimintoon.

3. Kirjoita **Sähköinen laskutus** -välilehdessä **Palvelun päätepisteen URI** -kenttään asianmukainen Microsoft Azure -alueen palvelun päätepiste, joka näkyy seuraavassa taulukossa.

    | Konesalin Azure-alue | Palvelun päätepisteen URI-osoite |
    |----------------------------|----------------------|
    | Yhdysvallat              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Eurooppa                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Yhdistynyt kuningaskunta             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Aasia                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Japani                      | <p>`https://gw.jp-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Sveitsi                | <p>`https://gw.ch-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Brasilia                     | <p>`https://gw.br-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.br-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Yhdistyneet arabiemiirikunnat       | <p>`https://gw.ae-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Australia                  | <p>`https://gw.au-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.au-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Kanada                     | <p>`https://gw.ca-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.ca-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Ranska                     | <p>`https://gw.fr-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Intia                      | <p>`https://gw.in-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Norja                     | <p>`https://gw.no-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Etelä-Afrikka               | <p>`https://gw.za-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. Tarkista **Sovelluksen tunnus** -kenttä ja syötä siihen kiinteä arvo **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. Varmista, että kenttään syötetään vain yleinen yksilöivä tunnus (GUID) eikä arvo sisällä muita symboleja, kuten välilyöntejä, pilkkuja, pisteitä tai lainausmerkkejä.
4. Syötä **LCS-ympäristötunnus**-kenttään Microsoft Dynamics Lifecycle Services (LCS) -ympäristösi tunnus. Tätä arvoa käytetään viittauksena Finance- tai Supply Chain Management -ympäristöön, jota käytät sähköisen laskutuksen palvelun kanssa. Voit saada tunnuksesi kirjautumalla sisään [LCS:ään](https://lcs.dynamics.com/), avaamalla projektin ja katsomalla sitten **Ympäristön hallinta** -välilehden **Ympäristön tiedot** -osassa **Ympäristön tunnus** -kentän.

    > [!IMPORTANT]
    > Jos sähköisen laskutuksen lisäosa on asennettu useaan Finance- tai Supply Chain Management -ympäristöön LCS:ssä, käytä aina viimeksi asennetun ympäristön ympäristötunnusta. Jos päätät asentaa lisäosan uuteen ympäristöön sähköisen laskutuksen toiminnon asennuksen ja käytön jälkeen, päivitä RCS:n **LCS-ympäristötunnus** -kenttä uusimpaan arvoon.

5. Valitse **Tallenna** ja sulje sitten sivu.

## <a name="configuration-providers"></a>Konfiguraation tarjoajat

Konfiguraatiopalveluiden avulla voit erottaa toisistaan sähköisessä laskutusprosesseissa ja omistajien globalisaatio-ominaisuuksissa käytettävät sähköisen raportoinnin konfiguraatiot. Kaikkien Microsoftin yleistietovarastossa julkaisemien globalisointiominaisuuksien konfiguraatiopalveluksi on määritetty **Microsoft** (`http://microsoft.com`).

Voit muokata vain aktiiviseen konfiguraatiopalveluun kuuluvia ER-konfiguraatioita ja globalisointiominaisuuksia. Voit käyttää näitä konfiguraatioita ja ominaisuuksia malleina luodaksesi aktiiviseen konfiguraatiopalveluun kuuluvia konfiguraatioita ja toimintoja ja muokata niitä.

Luo ensin määrityspalvelut. Määritä sitten yksi niistä aktiiviseksi. **Microsoft**-konfiguraatiopalvelua ei voi määrittää aktiiviseksi.

### <a name="create-a-configuration-provider"></a>Luo määrityspalvelu

1. Valitse **Sähköisen raportointi** -työtilan **Liittyvät linkit** -osassa **Konfiguraation lähteet**.
2. Valitse **Uusi**.
3. Kirjoita konfiguraatiopalvelun yksilöivä nimi **Nimi**-kenttään.
4. Kirjoita **Internet-osoite**-kenttään konfiguraatiopalvelun yksilöivä URL-osoite.
5. Valitse **Tallenna** ja sulje sitten sivu.

### <a name="select-a-configuration-provider-as-active"></a>Valitse konfiguraatiopalvelu aktiiviseksi

1. Valitse konfigurointipalveluluettelosta konfiguraatiopalvelu, jonka haluat määrittää aktiiviseksi.
2. Valitse **Määritä aktiivinen**.

## <a name="import-er-configurations-from-the-global-repository"></a>Sähköisen raportoinnin konfiguraatioiden tuonti yleisestä tietovarastosta

1. Valitse **Sähköisen raportointi** -työtilan **Liittyvät linkit** -osassa **Konfiguraation lähteet**.
2. Valitse **Microsoft**-määrityspalvelu konfiguraatiopalveluluettelosta ja valitse sitten **Säilöt**.
3. Valitse **Yleiset** ja valitse toimintoruudusta **Avaa**.
4. Tuo seuraavat ER-mallit:

    - **Myyntilaskun kontekstimalli**
    - **Laskumalli**
    - **Kirjanpitoasiakirjat** (Brasilian skenaarioihin, jos tarpeen)
    - **Vastaussanomamalli**

5. Jos **Laskun mallimääritystä** ei tuoda automaattisesti, tuo se.
6. Sulje sivu.
