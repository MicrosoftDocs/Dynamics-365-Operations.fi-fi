---
title: "Esiversio-ominaisuuksien käyttö Talentissa"
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
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: cd738cafc97477182e574ee0f363fdcf1df7da7a
ms.contentlocale: fi-fi
ms.lasthandoff: 10/22/2018

---

# <a name="access-preview-features-in-talent"></a>Esiversio-ominaisuuksien käyttö Talentissa

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
4. Vaihtoehtoisesti voit hallita yksittäisiä ominaisuuksia ottamalla kyseiset ominaisuudet käyttöön tai poistamalla ne käytöstä tällä sivulla.
5. Päivitä selaimesi ikkuna nähdäksesi uudet ominaisuudet. (Käyttäjät, jotka ovat jo kirjautuneet sisään, näkevät ominaisuudet seuraavan sisäänkirjautumiskerran yhteydessä tai päivittäessään selaimen ikkunan.)

#### <a name="core-hr"></a>Henkilöstöhallinnon perusversio

1. Kirjaudu sisään Talentiin. Näyttöön avautuu Henkilöstöhallinnan perusversion työtila, jossa suoritat loput vaiheet. 
2. Valitse **Järjestelmän hallinta \> Linkit ja Järjestelmäparametrit**.
3. **Järjestelmäparametrit-sivulla** **Esiversio-ominaisuudet** -välilehdessä aseta **Ota esiversiotila käyttöön kaikille käyttäjille** -asetukseksi **Kyllä** tuodaksesi esiversio-ominaisuudet saataville.

> [!NOTE]
> Voit poista esiversio-ominaisuudet käytöstä samalla tavalla. Kun esiversio-ominaisuudet poistetaan käytöstä, käyttäjät eivät voi käyttää niitä ja kyseisiin ominaisuuksiin liittyvissä prosesseissa voi esiintyä virheitä.

## <a name="features-that-are-currently-in-preview"></a>Tämänhetkiset esiversio-ominaisuudet

### <a name="attract"></a>Kerätä

- **Työhön sopivat ehdokkaat** – Työhönottajat ja rekrytointipäälliköt näkevät kätevästi kaikista hakijoista, kuka ehdokkaista soveltuu parhaiten työhön. Viisi parasta hakijaa näytetään sen perusteella, miten hyvin heidän ansioluettelonsa tai profiilinsa vastaa työnkuvausta.
- **Liittyvät työt** – Ehdokkaat näkevät luettelon muista heille soveltuvista töistä ansioluettelon tai profiilin ja työnkuvauksen perusteella.  Tällä hetkellä ehdokkaat näkevät tämän vaihtoehdon, kun he hakevat ehdotuksia muista mahdollisuuksista.
- **EEO-/OFCCP-tuki** – Uudet tehtävätyypit mahdollistavat valmiiksi täytetyn lomakkeen käytön, jolla kerätään ehdokkaan EEO (Equal Employment Opportunity)- ja OFCCP (Office of Federal Contract Compliance Program) -tiedot.  Lomake on määritetty ennalta, eikä sitä voi muokata.

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

