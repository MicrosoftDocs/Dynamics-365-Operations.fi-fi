---
title: Tarjoustenhallinnan määrittäminen
description: Tässä ohjeaiheessa käsitellään tarjousten määrittämistä Talentissa.
author: josaw
manager: AnnBe
ms.date: 02/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43cf13d96e345747e06541267d820e17de7c1763
ms.sourcegitcommit: ea17d2e35c24a141c20ab429897eebf9fa186f61
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/26/2019
ms.locfileid: "768879"
---
# <a name="set-up-offer-management"></a>Tarjoustenhallinnan määrittäminen 

[!include [banner](includes/banner.md)]

Kun hakija siirretään Dynamics 365 for Talent: Attractissa tarjousvaiheeseen, sinun on varmistettava, että tarjoukset luodaan nopeasti hakijalle, hyväksytään tarvittaessa ja lähetetään hakijalle. Koska useimmat tarjoukset ovat vakiomuotoisia, ne voidaan luoda uudelleenkäytettävistä malleista. Attractissa kaikki tarjoukset kerätään tarjouspaketiksi. Se on kokoelma, jossa on vähintään yksi tarjousasiakirja. 

Tässä ohjeaiheessa käsitellään kaikki vaiheet, joita noudattamalla Attractin järjestelmä määrittää erilaisia tarjouspakettimalleja Attractin tarjousten hallintatoiminnossa. Jos käyttäjällä ei ole järjestelmänvalvojan rooli, hänellä ei ole näiden toimintojen käyttöoikeuksia.

>[!NOTE]
> Tarjouksen hallintatoiminnot ovat saatavana kattavan työhönottolaajennuksen osana.

## <a name="offer-data"></a>Tarjouksen tiedot 

Tarjouksen tiedot on tarjouspakettimallin pienin yksikkö. Tyypillinen tarjous koostuu vakiotekstistä ja arvojoukosta. Arvojoukko on ainoa osa, joka voi vaihdella tarjouksen mukaan. Tarjouksen luonnissa on tärkeintä, että tarjouksen luoja keskittyy tarjouspakettimallissa olevaan tarjouksen tietojen paikkamerkkiluetteloon. Määritä tarjouksen tiedot seuraavasti:

1.  Valitse **Tarjousten hallinta**.

1.  Laajenna **Kirjasto**-osa vasemmassa siirtymisruudussa ja valitse sitten **Tarjouksen tiedot**.

    >[!NOTE]
    > **Tarjouksen tiedot** -sivulla on **Ehdokkaan tiedot**- ja **Työn tiedot** -osat. Attractissa on muutamia valmiita tarjouksen tietojen paikkamerkkejä.
    
    > Sivulla on osia, joissa tarjouksen tietojen erilaiset paikkamerkit voidaan järjestää loogisiksi ryhmiksi. Nämä osat helpottavat tarjouksen tietojen ylläpitoa ja tietojen täyttämistä tarjouksen luontiprosessin aikana.

1.  Voit luoda uuden tarjoustieto-osan valitsemalla **Lisää osa** ja antamalla sille yksilöivä nimen.

1.  Voit lisätä tarjoustietojen paikkamerkin johonkin osaan valitsemalla **Lisää tarjouksen tiedot** ja antamalla paikkamerkille yksilöivän nimen.

1.  Voit muokata minkä tahansa osan nimeä pitämällä osoitinta osan päällä ja päivittämällä nimen.

1.  Voit kyllä muokata aiemmin luodun tarjoustietojen paikkamerkin nimeä, mutta varmista ensin, että paikkamerkkiä ei käytetä missään mallissa. Siirrä sitten osoitin tarjoustietojen paikkamerkin nimen päälle ja päivitä nimi tarpeen mukaan.

1. Voit kyllä poistaa aiemmin luodun tarjoustietojen paikkamerkin, mutta varmista ensin, että paikkamerkkiä ei käytetä missään muussa mallissa. Siirrä sen jälkeen osoitin paikkamerkin päälle. Kun roskakorikuvake tulee näkyviin, poista tarjoustietojen paikkamerkki kuvaketta napsauttamalla.
    >[!NOTE]
    > Jokaisen tarjouksen tiedon vieressä on numero, joka ilmaisee, kuinka monessa mallissa tarjoustietojen paikkamerkki on käytössä. 

1. Voit poistaa minkä tahansa osan, siirtämällä osoittimin nimen päälle. Jos mitään osan tarjoustietojen paikkamerkkiä ei käytetä missään mallissa, voit poistaa sen roskakorikuvaketta napsauttamalla. 
    >[!NOTE]
    > Osan poistaminen poistaa myös kaikki tarjoustietojen paikkamerkit kyseisestä osasta.

Kun tarjoustietojen paikkamerkit on määritetty, voit käyttää niitä missä tahansa asiakirjamallissa. Tarjoustietojen paikkamerkkien käyttöä ei ole rajoitettu tiettyyn malliin, vaan samaa joukkoa voidaan käytätä kaikissa malleissa.

## <a name="offer-data-rules"></a>Tarjouksen tietojen säännöt

Useimmissa organisaatioissa on tarjousten luontisäännöt. Organisaatio voi esimerkiksi edellyttää, että tietyn toimipaikan ja tietyn ikälisän yhdistelmänä muodostuva vuosipalkka saa olla enintään tietyn suuruinen tai että uudelle työntekijälle on käytettävissä vain muutamia tarjoustason arvoja. Attract tukee tällä hetkellä kaikkia tällaisia CSV-tiedostoa käyttäviä tietosääntöjä.

Valmistele tietosääntöjen CSV-tiedosto seuraavasti:

1.  Määritä sääntöjoukon tarjoustietojen paikkamerkki. Esimerkki: **Vuosipalkka**.

1.  Määritä riippuvaiset tarjouksen tietojen paikkamerkkiarvot. Esimerkki: **Työn sijainti** ja **Taso**.

1.  Määritä sarakkeiksi 1 ja 2 **Työn sijainti** ja **Taso**.

1.  Lataa alueen arvo määrittämällä sarakkeiksi 3 ja 4 **Vuosipalkka**. Jos haluat ladata tietyn arvon arvoalueen sijaan, määritä vain sarakkeeksi 3 **Vuosipalkka**.

1.  Täytä Microsoft Excel -tiedoston tiedot tarvittavien roolien perusteella.

1.  Varmista, että jokainen rivi on yksilöllinen yhdistelmä kaikista arvoista.

1.  Tallenna tiedosto CSV-muodossa.

Lataa tarjouksen tietosääntötiedosto seuraavasti:

1.  Valitse **Tarjousten hallinta**.

1.  Laajenna **Kirjasto**-osa vasemmassa siirtymisruudussa ja valitse sitten **Tarjouksen tietojen säännöt**.

1.  Valitse **Uusi tietojoukko**, jolloin **Lataa palvelimeen** -valintaikkuna avautuu.

1.  Määritä sääntöjoukolle yksilöivä nimi ja lataa tallennettu CSV-tiedosto sitten palvelimeen.

1.  Valitse **Lisää**.
    Sääntöjoukko käsitellään taustalla, ja kun se valmistuu, saat siitä ilmoituksen sovelluksessa ja sähköpostitse.

    Saat ilmoituksen, jos latauksen käsittelyssä esiintyi virheitä. Voit sitten ladata virhelokin, korjata tiedoston ja ladata sen uudelleen palvelimeen.

1.  Käytä ellipsipainiketta (**…**), jos haluat ladata sääntöjoukon ja päivittää arvojoukon. Lataa tiedosto päivittämisen jälkeen uudelleen palvelimeen.

1.  Voit poistaa palvelimeen ladatun aiemmin luodun sääntöjoukon, jos määritettävää paikkamerkkiä ei käytetä toisessa asiakirjamallissa.

>[!NOTE]
> - Kullakin paikkamerkillä voi olla vain yksi yksilöllinen sarakejoukko, josta se on riippuvainen. Jos esimerkki **vuosipalkka** on riippuvainen **työn sijainnista** ja **tasosta**, et voi ladata palvelimeen toista sääntöjoukkoa, jossa **vuosipalkka** on riippuvainen toisenlaisesta sarakejoukosta.

> - Voit ladata tarjouksen tietojen näytesääntöjoukot **Tarjouksen tietojen säännöt** -sivun **Mallit**-välilehdessä.

> - Kun tarjouksen luoja korvaa tarjouksen tietojen sääntöjen suosittelemat arvot, tarjous merkitään muuksi kuin vakiotarjoukseksi ja tarjouksen hyväksyntätyönkulun käyttö on pakollista.

## <a name="document-templates"></a>Tiedostomallit

Tarjouksen asiakirjamalli voi auttaa järjestelmänvalvojia luomaan tarjouskirjeitä. Tarjouksen asiakirjamalli koostuu tekstistä, joka on osa tarjousta, ja määritetyistä tarjoustietojen paikkamerkeistä. 

Luo tarjouksen asiakirjamalli seuraavasti:

1.  Valitse **Tarjousten hallinta**.

1.  Laajenna **Kirjasto**-osa vasemmassa siirtymisruudussa ja valitse sitten **Mallit**.

    Avautuvalla **Mallit**-sivulla on luettelo asiakirjamalleista, jotka on jo määritetty.

1.  Luo uusi asiakirjamalli valitsemalla **Uusi malli**.

1.  Anna mallille yksilöivä nimi ja valitse **Luo**.

1.  Voit lisätä tai muokata tarjousasiakirjan sisältöä RTF-editorissa. Voit lisätä tauluja, kuvia ja hyperlinkkejä käyttämällä tekstieditorin yläosassa olevia vaihtoehtoja.

1.  Voit lisätä tarjoustietojen paikkamerkkien tarjouksen malliasiakirjaan

    - vetämällä ja pudottamalla oikeasta ruudusta

    - sijoittamalla tarjoustietojen paikkamerkin suoraan työpaikkaan tunnisteen avulla. Kirjoita ensin **\#** ja aloita sitten tarjoustietojen paikkamerkin nimen kirjoittaminen. Vaihtoehdot tulevaa näkyviin avattavana luettelon. Lisää tarjoustietojen paikkamerkki napsauttamalla sitä tai painamalla **Enter**-näppäintä.

    >[!NOTE]
    > - Voit liittää paikkamerkin tarjouksen asiakirjamalliin ilman, että hakija näkee sen arvon, siirtämällä osoittimen tarjoustietojen paikkamerkin päälle ja napsauttamalla **Kiinnitä**-kuvaketta. Paikkamerkki siirretään nyt tarjouksen asiakirjamallin **Kiinnitetyn tarjouksen tiedot** -osaan. Voit poistaa kiinnityksen toimimalla samalla tavoin mutta valitsemalla **Poista kiinnity** tarjoustietojen paikkamerkkiluettelossa.

    > - Voit tarkastella aktiivisia tarjoustietojen paikkamerkkejä siirtymällä oikeassa ruudussa **Aktiiviset**-välilehteen.

    > - Jos lisää tarjoustietojen sääntöjoukkoa noudattavan paikkamerkin, näet kyseisen tarjoustietojen paikkamerkin riippuvuuden muista arvoista.

    > - Vaihtoehtoisesti voit **tuoda** sisällön paikallisen tiedoston .docx-tiedostosta ja muokata sitä tarpeen mukaan. Tässä tapauksessa sinun ei tarvitsee kirjoittaa kaikkea sisältöä editorissa.

1. Voit esikatsella tarjousasiakirjaa valitsemalla sivun yläosassa**Esikatselu**-vaihtoehdon.

1. Voit hallita, saako tarjouksen luoja muokata tarjousasiakirjan sisältöä valitsemalla sivun yläosassa **Hallitse käyttöoikeutta**. Jos haluat, että tarjouksen luoja voi vain lisätä paikkamerkin arvot tekstin muokkaamisen sijaan, määritä käyttöoikeuden arvoksi **Ei**.

1. Tallenna eteneminen valitsemalla **Tallenna**. Malli tallennetaan luonnoksena.

1. Viimeistele asiakirja ja merkitse se julkaistuksi valitsemalla **Valmis**.

1. Näet asiakirjamallikirjaston saapumissivulla, mitkä asiakirjamallit ovat aktiivisia, mitkä luonnostilassa ja mitkä on arkistoitu eikä enää käytettävissä.

>[!NOTE]
> Voit poistaa tarjousasiakirjamallit, jotka eivät sisälly nykyiseen tarjouspakettimalliin.


## <a name="offer-package-templates"></a>Tarjouspakettimallit

Tarjouspaketit ovat hakijan kanssa jaettavia tarjouksen tietoja, ja ne koostuvat vähintään yhdestä tarjousasiakirjamallista. Luo tarjouspaketti seuraavasti:

1.  Valitse **Tarjousten hallinta**.

1.  Valitse vasemmassa siirtymisruudussa **Paketit**.

    Näkyviin tulee luettelo aktiivisista pakettimalleista, jotka ovat tarjouksen luojien käytettävissä.

1.  Luo uusi tarjouspaketti valitsemalla **Uusi paketti**.

1.  Anna yksilöivä nimi ja valitse **Luo**.

1.  Valitse **Lisää malli**.

    >[!NOTE]
    > - Voit joko luoda uuden mallin tai valita aiemmin luodun mallin.

    > - Jos päätät lisätä aiemmin luodun mallin, sinun on varmistettava, että tarjousasiakirjamalli on tallennettu, viimeistelty ja merkitty aktiiviseksi.
    
    > - Voit valita niin monta asiakirjamallia kuin haluat. 
    
1.  Valitse **Valmis**, jonka jälkeen palaat **paketin hallintaan**.

    Voit määrittää asiakirjojen järjestyksen sekä merkitä, mitä tiettyä tarjousasiakirjaa on käytettävä tarjousta luotaessa. Tarjouksen luojalla on mahdollisuus poistaa asiakirjat, joissa on merkintä **Ei pakollinen**.

1. Tallenna tarjouspakettimalli, jotta se on myös kaikkien muiden tarjouksen luojien käytettävissä, valitsemalla **Tallenna ja julkaise**.

   Voit tarkastella tarjouspakettimallien luonnoksi valitsemalla **Luonnokset**-välilehden. Jos tarjouspakettimalliin tehdään muutoksia, se on tallennettava ja julkaistava uudelleen.

## <a name="configure-an-offer-process"></a>Tarjousprosessin asetusten määrittäminen

Tarjouksen luontiprosessissa on useita osia, joita Attractin järjestelmänvalvoja voi määrittää.

- **Tarjouksen hyväksynnät** – Valitse, onko tarjoukset hyväksyttävä, ennen kuin tarjous voidaan lähettää hakijalle. Voit järjestelmänvalvojana päättää, tehdäänkö kaikki tarjouksen hyväksynnät peräkkäisessä tai rinnakkaisessa hyväksyntätyönkulussa. Voit myös määrittää, onko tarjouksen hyväksyjien liitettävä hyväksyntään kommentti. Tarjouksen hyväksyntä on pakollista kaikissa ei vakiomuotoisissa tarjouksissa.

- **Hakijan tarjouskokemus** – Järjestelmänvalvojana voi määrittää, onko kaikille tarjouksilla vanhentumispäivä ja jos on, mikä on vanhentumispäivämäärän oletussiirtymä. Voit myös määrittää, voiko hakija hylätä tarjouksen.

- **Sähköiset allekirjoitukset** – Voit järjestelmänvalvojana valita menetelmä, jolla ehdokkaat allekirjoittavat tarjoukset.
    - Adobe Sign – Kaikki tarjouspaketit lähetetään ja allekirjoitetaan Adobe Signin kautta. Jokaisella tarjouksen julkaisevalla tekijällä on oltava oma Attractiin yhdistetty Adobe Sign -tili. Lisätietoja Adobe Sign -käyttöoikeuksista ja maksuttomasta kokeilusta on tässä [linkissä](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).

    - DocuSign – Kaikki tarjouspaketit lähetetään ja allekirjoitetaan DocuSignin kautta. Jokaisella tarjouksen julkaisevalla tekijällä on oltava oma Attractiin yhdistetty DocuSign-tili. 
    
    - ESign – Tämä oletusasetus on heti käyttövalmis, ja käyttäjä voi allekirjoittaa tarjouksen kirjoittamalla nimensä ja nimikirjaimensa.


Lisätietoja tarjouksen luontiprosessista on kohdassa [Tarjousten luominen, hyväksyminen ja allekirjoittaminen](./creating-offers.md).
