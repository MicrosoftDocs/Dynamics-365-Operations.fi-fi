---
title: Hanki osaajia kykypoolien avulla Attractissa
description: Tässä ohjeaiheessa käsitellään kykypoolien luontia ja määrittämistä Microsoft Dynamics 365 Talent – Attractissa.
author: andreabichsel
manager: AnnBe
ms.date: 06/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 97385da9d258cc169a9976be7c7798faa41661c3
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527690"
---
# <a name="source-candidates-with-talent-pools-in-attract"></a>Hanki osaajia kykypoolien avulla Attractissa

[!include [banner](includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Rekrytoijat ja työhönottopäälliköt voivat järjestää hakijat Attractin kykypoolitoiminnolla. Kykypoolien avulla voi seurata kaikkia hakijoita, jotka hakevat työpaikkaa yrityksessä, sekä viestiä heidän kanssaan.

## <a name="create-and-share-a-talent-pool"></a>Kykypoolin luominen ja jakaminen

Kaikki käyttäjät, joilla on työhönottajan, työhönottopäällikön tai Attractin järjestelmänvalvojan rooli, voivat luoda kykypooleja. Kykypoolin omistaja voi myös jakaa poolin muiden käyttäjien kanssa, joten käyttäjäryhmä, etenkin rekrytoijat, voivat tarkastella jaettua hakijapoolia.

Kykypoolin osallistujat voivat tarkastella kyseisen pooli hakijaluetteloa. He voivat myös lisätä hakijoita pooliin tai poistaa heitä poolista.

Luo ja jaa kykypooleja seuraavien ohjeiden mukaisesti.

1. Valitse Attractin aloitussivun vasemmassa siirtymisruudussa **Kykypoolit**.

    **Omat kykypoolit** -välilehdessä on näkyvissä kaikki kykypoolit, joiden käyttöoikeus sinulla on, sekä tietoja kustakin poolista. Näitä tietoja ovat esimerkiksi poolin omistaja ja siinä olevien hakijoiden määrä.

1. Valitse sivun oikeassa yläkulmassa oleva **Uusi** ja avaa **Luo kykypooli** -valintaikkuna.
1. Anna kykypoolille yksilöivä nimi.
1. Voit lisätä osallistujia kykypooliin, etsimällä nimet henkilövalitsimella ja lisäämällä heidät sitten luetteloon. Voit jakaa kykypoolin käyttäjien kanssa, joiden rooli on työhönottaja, työhönottopäällikkö tai Attractin järjestelmänvalvoja.
1. Luo uusi kykypooli valitsemalla **Lisää**.
     > [!NOTE]
     > Voit lisätä osallistujia kykypooliin myös sen jälkeen, kun olet luonut sen. Voit hallita kykypoolin käyttöoikeuksia. Voit esimerkiksi peruuttaa jonkun käyttäjän kykypoolin käyttöoikeuden.
     > - Voit lisätä osallistujia omistamaasi aiemmin luotuun kykypoolin valitsemalla **Omat kykypoolit** -välilehden kykypoolikortin oikeassa yläkulmassa ensin ellipsipainikkeen (**…**) ja sitten **Muokkaa**. Etsi henkilöitä henkilövalitsimella ja lisää heidät sitten luetteloon. 
     > - Voit peruttaa käyttäjän kykypoolin käyttöoikeuden valitsemalla kykypoolikortin oikeassa yläkulmassa ensin ellipsipainikkeen (**…**) ja sitten **Muokkaa**. Valitse **Käytön hallinta** -välilehdessä käyttäjän vieressä oleva roskakoripainike.

6. Viimeistele ja tallenna toiminto valitsemalla **Päivitä**.

> [!NOTE]
> Jos haluat luoda useita kykypooleja, organisaatiossa on oltava kattava työhönottolaajennus.

## <a name="add-and-remove-candidates"></a>Hakijoiden lisääminen ja poistaminen

Kykypoolin omistaja ja sen osallistujat voivat lisätä hakijoita pooliin, tarkastella siinä olevia hakijoita ja poistaa hakijoita siitä.

1. Avaa kykypooli valitsemalla se **Omat kykypoolit** -välilehdessä.

    Luettelo kykypooliin kuuluvista hakijoista tulee näkyviin.

1. Voit lisätä hakijoita kykypooliin avaamalla **Lisää ehdokas** -valintaikkunalla valitsemalla oikeassa yläkulmassa **+ Uusi**. Tee sitten jokin seuraavista:

    - Voit lisätä sisäisen hakijan hakemalla henkilön sähköpostiosoitteen avulla. Jos haku onnistuu, hakijan sähköpostiosoite, etunimi ja sukunimi lisätään kenttiin. Jos hakijan ansioluettelo tai muut hakijaa koskevat asiakirjat ovat saatavana, voit ladata ne tässä vaiheessa. Lisää hakija sitten kykypooliin valitsemalla **Lisää**.
    - Voit lisätä ulkoisen hakijan antamalla hän sähköpostiosoitteen, etunimen ja sukunimen manuaalisesti. Jos hakijan ansioluettelo tai muut liittyvät asiakirjat ovat saatavana, voit ladata ne tässä vaiheessa. Lisää hakija sitten kykypooliin valitsemalla **Lisää**.
    - Voit lisätä useita hakijoita valitsemalla **Excelistä**-välilehden. Voit sitten ladata sopivan Microsoft Excel -mallin, antaa hakijoiden tiedot, tallentaa Excel-laskentataulukon ja ladata sen sovellukseen.

        Jos laskentataulukossa on virheitä, saat niistä ilmoituksen. Voit sitten korjata virheet ja yrittää ladata laskentataulukon uudelleen. Kun virheitä ei enää löydy, lataa laskentataulukko valitsemalla **Lisää**. Laskentataulukko käsitellään taustalla ja saat ilmoituksen, kun kaikki hakijat on lisätty kykypooliin.

1. Voit poistaa hakijoita kykypoolista valitsemalla **Toiminto**-sarakkeessa kyseisen hakijan roskakorikuvakkeen.

## <a name="search-and-view-candidate-profiles"></a>Hakijaprofiilien hakeminen ja tarkasteleminen

> [!NOTE] 
> Tämä ominaisuus on tällä hetkellä vain esiversiossa. Voit halutessasi kokeilla sitä [ottamalla sen käyttöön Attractin järjestelmänvalvojan asetuksissa](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature). 

Kykypoolien avulla voit tarkastella ehdokkaan profiilia, LinkedIn-tietoja, liittyviä asiakirjoja ja sovellushistoriaa. Voit tehdä haun mihin tahansa kykypooliin lisätystä ehdokkaiden tietokannasta, mukaan lukien suljetut ja aktiiviset hakijat.

>[!NOTE]
> Kun lisäät uusia ehdokkaita, uusien lisäysten indeksoiminen hakua varten voi kestää 15 minuuttia.

Parannetun hakukokemuksen avulla voit tehdä haun kaikista ehdokkaiden asiakirjoista ja suodattaa esimerkiksi hopeamitalistien, lähteiden, taitojen ja koulutuksen perusteella. Edellisissä versioissa sinun oli määritettävä koko entiteetti, josta haku tehtiin. Attract voi nyt hakea kaikista ehdokkaaseen liittyvistä kentistä ja lajitella tulokset.

1. Voit aloittaa uuden haun ehdokkaan tietokannassa kirjoittamalla haettavan tekstin **Kykypoolit**-välilehden hakuruutuun. 

Voit kirjoittaa ehdokkaan nimen tai jonkin muun haettavan määritteen. Erottele määritteet välilyönnillä.

Voit tarkentaa hakutuloksia muuttamalla hakukyselyä tai käyttämällä sivun oikealla puolella olevia älykkäitä suodattimia.

Hakutuloksissa näkyvät eri määritteiden tärkeimmät hakukyselyä vastaavat osumat. Valitse mikä tahansa ehdokas, jonka profiilin haluat nähdä.

### <a name="syntax-highlights"></a>Syntaksin tärkeimmät kohdat 

| Käyttäjä | Käyttö                                                      | Esimerkki              |
|----------|------------------------------------------------------------|----------------------|
| \*       | Hakee alimerkkijonoja, tätä voi käyttää kaikkien tietueiden palauttamisessa | Syöte: Mi\* <br></br> Tulos: Kaikki tietueet, jotka sisältävät Mi-alkuisia kenttiä, esimerkiksi Microsoft, Micro systems, Midtown Enterprises ja Middleton <br></br>Syöttö: \* <br></br> Tulos: Kaikki tietokannan tietueet |
| “”       | Hakee tarkan vastineen                                | Syöttö: ”Microsoft” <br></br> Tulos: Kaikki tietueet, joissa on Microsoft                    |

>[!WARNING]
> Älä poista käytöstä Common Data Service -ilmentymän osuvuushakua. Se estää haun käytön Attractissa.

Kaikilla käyttäjillä on sama hakijaprofiilien näkymä. **Profiili**-välilehdessä on ne tiedot taidoista, työkokemuksesta ja koulutuksesta, jotka hakija on antanut uraportaalin avulla osana hakemuksia.

- Voit tarkastella hakijan yhteystietoja. Voit myös muokata tai päivittää tietoja tarpeen mukaan **Muokkaa**-painikkeella.

- Voit tarkastella hakijan koko hakemushistoriaa. Näet kaikki työpaikat, joita hakija on organisaatiossa hakenut sekä kyseisten hakemusten tilan. Jos kuulut työpaikan työhönottoryhmään, voit tarkastella hakemuksen tietoja tarkemmin valitsemalla **Näytä**.

- **Asiakirjat**-välilehdessä näkyy kaikki asiakirjat, jotka hakija on lisännyt profiilistaan tai työnhakuprosessien aikana. Voit hallita tässä välilehdessä esimerkiksi hakijan ansioluetteloita, saatekirjeitä ja portfoliotöitä. Tässä välilehdessä voi myös lisätä asiakirjoja.

    Valitse tarkastelevan asiakirjan nimi asiakirjaluettelossa. Voit tarkastella Microsoft Word -asiakirjoja sovelluksessa Microsoft 365:n avulla. Voit myös ladata asiakirjat paikalliseen tietokoneeseen käyttämällä kussakin asiakirjassa olevaa **Lataa**-asetusta.

- Hakijan LinkedIn-tiedot ovat **LinkedIn**-välilehdessä. Jos haluat käyttää tätä välilehteä, sinun on muodostettava käyttäjän asetuksissa yhteys LinkedIn-tiliin. Lisäksi ympäristössä on oltava LinkedIn Recruiter-yhteys. Lisätietoja on kohdassa [Ehdokkaiden rekrytointi LinkedIn Recruiterilla Microsoft Dynamics 365 Talent – Attractissa](./attract-linkedin-recruiter.md).

> [!NOTE]
> Vain ehdokkaat voivat päivittää osaamisalueensa, koulutushistoriansa ja työkokemuksensa.

## <a name="add-candidates-from-a-talent-pool-to-a-job"></a>Hakijoiden lisääminen kykypoolista työpaikkaan

Voit siirtää hakijan hakutuloksista tai kykypoolista mihin tahansa aktiiviseen työ, jonka työhönotossa olet mukana. Siirrä hakija tiettyyn työpaikkaan seuraavien ohjeiden mukaisesti.

1. Etsi hakija käyttämällä hakuasetusta ja avaa sitten hänen profiilinsa. Voit myös avata kykypoolin **Omat kykypoolit** -välilehdessä, hakea hakijan kykypoolista ja avata sitten hänen profiilinsa.

1. Valitse hakijan profiilisivun oikeassa yläkulmassa **Lisää työhön**. 
     
     Näkyvissä on niiden työpaikkojen luettelo, joiden työhönottoryhmään kuulut joko työhönottajana tai työhönottopäällikkönä.

1. Valitse ensin työpaikka, johon hakija lisätään, ja sitten **Lisää**. Voit hakea työpaikkaa myös käyttämällä **Lisää ehdokas työlle** -valintaikkunan yläosan hakukenttää.

    Jos tiedustelu oli otettu työssä käyttöön, hakija lisätään **Potentiaalinen ehdokas** -vaiheessa.

    Jos tiedustelua ei ole otettu työssä käyttöön, hakija lisätään **Haku**-vaiheessa. Työn määritysten mukaan hakija voi myös saada sähköpostiviestin, jossa he voivat tarkastella hakemustaan.

## <a name="add-candidates-from-a-job-to-a-talent-pool"></a>Hakijoiden lisääminen työpaikasta kykypooliin

Jos yhteen työpaikkaan liittyy useita hyviä hakijoita, joita ei valita mutta joita haluat seurata. Haluat ehkä siinä tapauksessa lisätä hakijat kykypoolin, jotta voit kutsua heidät myöhemmin hakemaan muita työpaikkoja.

1. Siirry työhön, josta haluat lisätä hakijan.

1. Valitse hakija ja avaan hänen hakemuksensa.

1. Valitse hakemussivulla **Lisää kykypooliin**. Näkyviin tulee luettelo kykypooleista, joiden käyttöoikeus sinulla on.

1. Valitse tai hae kykypooli ja lisää sitten hakija kyseiseen pooliin valitsemalla **Lisää**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]