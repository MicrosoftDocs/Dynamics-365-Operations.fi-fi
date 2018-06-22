---
title: "Esiversio-ominaisuuksien käyttö - Dynamics 365 for Talent"
description: "Tässä aiheessa kuvataan, kuinka järjestelmänvalvoja voi ottaa käyttöön esiversio-ominaisuudet. Siinä listataan myös ominaisuudet, jotka ovat tällä hetkellä käytössä esikatselua varten."
author: rschloma
manager: AnnBe
ms.date: 04/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.translationtype: HT
ms.sourcegitcommit: dc2ab66bf6e3195e1ebf394f99182f59c3ee2125
ms.openlocfilehash: 63e0a52919e12c1f497e6809244939c6047826a7
ms.contentlocale: fi-fi
ms.lasthandoff: 05/15/2018

---

# <a name="access-preview-features-in-dynamics-365-for-talent"></a>Esiversio-ominaisuuksien käyttö - Dynamics 365 for Talent 

[!include[banner](../includes/banner.md)]

Parannamme jatkuvasti tuotteidemme ominaisuuksia ja haluamme tarjota ne asiakkaillemme mahdollisimman pian. Järjestelmänvalvojat voivat tarkastella ja käyttää esiversio-ominaisuuksia ympäristöissään. Nämä ominaisuudet ovat lähes valmiita yleiseen käyttöön ja ne ovat läpäisseet laajan testauksen. Haluamme saada vielä viimeisen asiakaspalautekierroksen, ennen kuin hyväksymme ominaisuudet yleiseen käyttöön.

Tässä aiheessa kuvataan, kuinka järjestelmänvalvoja voi ottaa käyttöön esiversio-ominaisuudet. Siinä listataan myös ominaisuudet, jotka ovat tällä hetkellä saatavilla esikatselua varten. Tätä luetteloa päivitetään sitä mukaa, kun ominaisuuksia julkaistaan yleiseen käyttöön ja uusia ominaisuuksia tuodaan esikatseltavaksi. Erillistä ilmoitusta ei anneta, kun uusia ominaisuuksia julkaistaan esikatseluun. Ominaisuudet tuodaan vain käyttäjien saataville.

## <a name="enable-or-disable-preview-features"></a>Esiversio-ominaisuuksien ottaminen käyttöön tai poistaminen käytöstä

Voit käyttää Microsoft Dynamics 365 for Talentin hallintakeskuksen **Esiversio-ominaisuudet**-asetusta ottaaksesi esiversio-ominaisuudet käyttöön tai pois käytöstä. Asetus on oletusarvon mukaan poissa käytöstä. Esiversio-ominaisuuksien käyttöönottoasetus on ympäristökohtainen.

> [!IMPORTANT]
> Ottamalla **Esiversio-ominaisuudet**-asetuksen käyttöön sallit esiversio-ominaisuudet organisaation kaikille käyttäjille kyseisessä ympäristössä. Jos poistat asetuksen käytöstä, esiversio-ominaisuudet eivät ole käyttäjien käytettävissä. Esiversio-ominaisuuksilla on Talentissa rajoitettu tuki. Niissä voi olla tavallista vähemmän tietosuoja- ja suojausominaisuuksia, eivätkä ne sisälly Talentin palvelutasosopimuksen. Älä käytä esiversio-ominaisuuksia henkilötietojen (eli henkilökohtaisesti tunnistettavien tietojen) käsittelyyn tai muiden sellaisten tietojen käsittelyyn, jotka edellyttävät lain- tai säädöstenmukaista suojelua.

### <a name="enable-or-disable-preview-features-for-your-organization"></a>Esiversio-ominaisuuksien ottaminen käyttöön tai poistaminen käytöstä organisaatiossasi

#### <a name="attract"></a>Attract

1. Kirjaudu sisään Microsoft Dynamics 365 for Talent: Attract -ohjelmaan.
2. Valitse **Asetukset**-valikossa (hammasrataskuvake) oikeassa alakulmassa **Järjestelmänvalvojan asetukset**.
3. Valitse **Ominaisuuksien hallinta** -välilehdestä kohdan **Esiversio-ominaisuudet** vieressä oleva vaihtoehto siten, että muuttuu siniseksi.
4. Päivitä selaimesi ikkuna nähdäksesi uudet ominaisuudet. (Käyttäjät, jotka ovat jo kirjautuneet sisään, näkevät ominaisuudet seuraavan sisäänkirjautumiskerran yhteydessä tai päivittäessään selaimen ikkunan.)

#### <a name="core-hr"></a>Henkilöstöhallinnon perusversio

1. Kirjaudu sisään Talentiin. Näyttöön avautuu Henkilöstöhallinnan perusversion työtila, jossa suoritat loput vaiheet. 
2. Valitse **Järjestelmän hallinta \> Linkit ja Järjestelmäparametrit**.
3. **Järjestelmäparametrit-sivulla** **Esiversio-ominaisuudet** -välilehdessä aseta **Ota esiversiotila käyttöön kaikille käyttäjille** -asetukseksi **Kyllä** tuodaksesi esiversio-ominaisuudet saataville.

> [!NOTE]
> Voit poista esiversio-ominaisuudet käytöstä samalla tavalla. Kun esiversio-ominaisuudet poistetaan käytöstä, käyttäjät eivät voi käyttää niitä ja kyseisiin ominaisuuksiin liittyvissä prosesseissa voi esiintyä virheitä.

## <a name="features-that-are-currently-in-preview"></a>Tämänhetkiset esiversio-ominaisuudet

### <a name="attract"></a>Attract

- **Työmallit** – Voit nyt luoda työhönoton prosessimalleja. Käyttäjät voivat jo mukauttaa työkohtaista työhönottoprosessia. Nyt he voivat kuitenkin luoda prosessimalleja ja valita sitten sopivan mallin, kun työ luodaan. Tämä ominaisuus auttaa siten nopeuttamaan työhönottoprosessia.
- **Urasivusto** – Urasivuston nykyinen versio ainoastaan listaa kaikki avoimet työt. Enemmän ominaisuuksia lisätään sivustoon myöhemmin. Työt voidaan merkitä sisäisiksi tai ulkoisiksi. Sisäiset käyttäjät, jotka kirjautuvat sivustoon, näkevät sekä sisäiset että ulkoiset työt. Käyttäjät, jotka eivät ole sisäisiä ja kirjautuneet sisään, näkevät vain ulkoiset työt.
- **Työpaikkailmoitus** – Voit nyt laatia työpaikkailmoituksia urasivustolle.
- **LinkedIn-työpaikkailmoitus** – Voit nyt laatia työpaikkailmoituksia LinkedIniin.

    > [!NOTE]
    > Ilmoitukset näkyvät vain asiakkaille, jotka tilaavat vähintään yhtä LinkedIn-työpaikkailmoitustuotetta. Muussa tapauksessa asiakkaat näkevät työn vain, jos he hakevat sitä erikseen. LinkedIn-työpaikkailmoitukset tulevat näkyviin viiveellä. Työ voi tulla näkyviin vasta useiden tuntien kuluttua siitä, kun se julkaistaan Attractista.

- **Hakeminen** – Sekä sisäiset että ulkoiset hakijat voivat nyt hakea työtä suoraan työn sivulta urasivustossa.
- **Tarjousten hallinta** – Käyttäjät voivat nyt luoda tarjouksia malleista, jotka sisältävät paikkamerkkejä. Kun hakijat pääsevät Tarjous-vaiheeseen, työhönottajat voivat käyttää tarjoustyökalua valmistellakseen ehdokkaan virallisen tarjouksen mallien perusteella, lähettääkseen tarjouksen sisäiseen hyväksyntään ja lopulta lähettääkseen tarjouksen hakijalle allekirjoitettavaksi. Tarjoustyökaluun lisätään ominaisuuksia ajan mittaan, ja esiversio-ominaisuus päivitetään näillä ominaisuuksilla kun ne ovat valmiita julkaistavaksi esikatseluun.

### <a name="core-hr"></a>Henkilöstöhallinnon perusversio

- **Avoin rekisteröinti** – Etujen avoin rekisteröinti tarjoaa työntekijöille yksinkertaisen, itsepalveluna toimivan tavan etujen valitsemiseksi. Henkilöstöhallinnon järjestelmänvalvojat voivat määrittää etujen avoimen rekisteröintiprosessin organisaatiolleen, ja työntekijöiden rekisteröintitavan, helposti ohjatulla ratkaisulla.

## <a name="feedback"></a>Palaute

Riippumatta siitä, onko palaute positiivinen vai negatiivinen, haluamme kuulla mielipiteesi esiversio-ominaisuuksista. Kannustamme sinua antamaan säännöllisesti palautetta, kun käytät näitä sivustoja tai muita ominaisuuksia.

- [Yhteisö](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – Tämä sivusto on erinomainen resurssi, jossa käyttäjät voivat keskustella tapauksista, esittää kysymyksiä ja saada ohjeita yhteisöltä.
- Käytä seuraavia sivustoja tuoteideoiden ehdottamiseksi. Ilmoita meille, mitä ominaisuuksia haluaisit tuotteeseen ja mitä muutoksia nykyisiin ominaisuuksiin pitäisi mielestäsi tehdä.

    - [Attract-ideat](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [Henkilöstöhallinnon perusversio](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)

Älä sisällytä mitään henkilötietoja (eli henkilökohtaisesti tunnistettavia tietoja) palautteeseesi tai tuotearvioihisi. Kerättyjä tietoja voidaan analysoida tarkemmin, eikä niitä käytetä pyyntöihin vastaamiseen tietosuojalakien mukaisesti. Henkilökohtaisiin tietoihin, jotka kerätään erillään näistä ohjelmista, sovelletaan [Microsoftin tietosuojalausuntoa](https://privacy.microsoft.com/privacystatement).

> [!TIP]
> Lisää kirjanmerkki tähän aiheeseen ja käy säännöllisesti katsomassa tietoa uusista julkaistuista esiversio-ominaisuuksista.

