---
title: "Tietojen tuonti- ja vientityöt"
description: "Tietojenhallinnan työtilan avulla voit luoda ja hallita tietojen tuonti- ja vientitehtäviä."
author: Sunil-Garg
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: 68cafc167c178e2feeb0a5af764a491ea6b3c60b
ms.contentlocale: fi-fi
ms.lasthandoff: 08/13/2018

---

# <a name="data-import-and-export-jobs"></a>Tietojen tuonti- ja vientityöt

[!include [banner](../includes/banner.md)]

Voit luoda ja hallita tietojen tuonti- ja vientitehtäviä Microsoft Dynamics 365 for Finance and Operationsin **Tietojenhallinta**-työtilassa. Oletusarvon mukaan tietojen tuonti- ja vientiprosessi luo väliaikaisen taulun kullekin yksikölle kohdetietokantaan. Väliaikaisten taulujen avulla voit tarkistaa, puhdistaa tai muuntaa tiedot ennen niiden siirtämistä.

> [!NOTE]
> Tässä ohjeaiheessa oletetaan, että tunnet [tietoyksiköt](data-entities.md).

## <a name="data-importexport-process"></a>Tietojen tuonti- ja vientiprosessi
Nämä ovat ohjeet tietojen tuontiin tai viemiseen.

1. Luo tuonti- tai vientityö, jossa suoritetaan seuraavat tehtävät:

    - Määritä projektin luokka.
    - Tunnista tuotavat tai vietävät yksiköt.
    - Määritä työn tietojen muoto.
    - Aseta yksiköt mielekkääseen järjestykseen niin, että ne käsitellään loogisissa ryhmissä.
    - Määritä, käytetäänkö väliaikaisia tauluja.

2. Vahvista, että lähde- ja kohdetiedot liitetään oikein.
3. Tarkista tuonti- tai vientityön turvallisuus.
4. Suorita tuonti- tai vientityö.
5. Vahvista, että työ suoritettiin odotetulla tavalla tarkastamalla työhistoria.
6. Tyhjennä väliaikaiset taulut.

Loput tämän ohjeaiheen osat sisältävät tarkempia tietoja kustakin prosessin vaiheesta.

> [!NOTE]
> Saat uusimmat edistymistiedot näkyviin päivittämällä tietojen tuonti- ja vientilomakkeen päivityskuvakkeella. Selaintason päivitystä ei suositella, koska se keskeyttää mahdolliset erien ulkopuoliset tuonti- ja vientityöt.

## <a name="create-an-import-or-export-job"></a>Luo tuonti- tai vientityö
Tietojen tuonti- tai vientityön voi suorittaa useita kertoja.

### <a name="define-the-project-category"></a>Määritä projektin luokka
Suosittelemme, että valitset tuonti- tai vientityölle haluamasi projektiluokan huolella. Voit hallita liittyviä töitä projektiluokkien avulla.

### <a name="identify-the-entities-to-import-or-export"></a>Tunnista tuotavat tai vietävät yksiköt
Voit lisätä tiettyjä yksiköitä tuonti- tai vientityöhön tai käyttää mallia. Mallit täyttävät työn yksikköluettelolla. **Käytä mallia** -vaihtoehtoa voi käyttää, kun työlle on annettu nimi ja se on tallennettu.

### <a name="set-the-data-format-for-the-job"></a>Määritä työn tietojen muoto
Valitse yksikölle tuonnin tai viennin tietomuoto sitä valitessasi. Muodot määritetään **Lähdeasetukset**-ruudussa. Lähdetietojen muodossa yhdistyy **Tyyppi**, **Tiedostomuoto**, **Rivin erotin** ja **Sarakkeen erotin**. Vaikka määritteitä on muitenkin, näiden ymmärtäminen on olennaista. Seuraava taulukko sisältää kelvolliset yhdistelmät.

| Tiedostomuoto            | Rivin tai sarakkeen erotin                       | XML-tyyli                 |
|------------------------|--------------------------------------------|---------------------------|
| Excel                  | Excel                                      | \-–                     |
| XML                    | \-–                                      | XML-elementin XML-määrite |
| Erotin, kiinteä leveys | Pilkku, puolipiste, sarkain, pystyviiva, kaksoispiste | \-–                     |

### <a name="sequence-the-entities"></a>Aseta yksiköt sarjaan
Yksiköt voi järjestää tietomallissa tai tuonti- ja vientitöissä. Kun suoritat työn, joka sisältää useamman tietoyksikön, varmista, että yksiköt on järjestetty oikein. Yksiköt järjestetään ensisijaisesti siten, että voit käsitellä kaikki yksiköiden väliset toiminnalliset riippuvuudet. Jos yksiköillä ei ole toiminnallisia riippuvuuksia, ne voidaan ajoittaa tuotavaksi tai vietäväksi rinnakkain.

#### <a name="execution-units-levels-and-sequences"></a>Suoritusyksiköt, -tasot ja -sarjat
Yksiköiden tuonti- tai vientijärjestystä valvovat ensin suoritusyksikön arvot, sitten suoritusyksikön taso ja lopulta sarja.

- Eri suoritusyksiköissä olevat yksiköt käsitellään rinnakkain.
- Saman suoritusyksikön yksiköt käsitellään rinnakkain, jos ne ovat samalla tasolla.
- Kunkin tason yksiköt käsitellään tason mukaisen järjestysnumeron perusteella.
- Kun yksi taso on käsitelty, käsitellään seuraava taso.

#### <a name="resequencing"></a>Uudelleenjärjestys
Voit halutessasi järjestellä yksiköt uudelleen seuraavissa tilanteissa:

- Jos kaikkiin muutoksiin käytetään yksittäistä tietotyötä, voit käyttää uudelleenjärjestysvaihtoehtoja ja optimoida siten koko työn suoritusajan. Tällöin voit käyttää suoritusyksikköä moduulin edustajana, tasoa moduulin toimintoalueen edustajana ja sarjaa yksikön edustajana. Käyttämällä tätä menetelmää voit käyttää kaikkia moduuleja samanaikaisesti, mutta voit silti käyttää moduulin järjestystä. Jos haluat varmistaa, että rinnakkaiset vaiheet onnistuvat, kaikki riippuvuudet on otettava huomioon.
- Jos käytössä on useita tietotöitä (esimerkiksi yksi työ kullekin moduulille), voit optimoida työtä muuttamalla järjestelytoiminnolla yksiköiden tasoa ja järjestystä.
- Jos riippuvuussuhteita ei ole, voidaan yksiköt järjestellä optimaalisesti eri suoritusyksiköihin.

**Uudelleenjärjestely**-valikko on käytettävissä, kun useita yksiköitä on valittuna. Voit järjestellä yksiköitä uudelleen suoritusyksikön, -tason tai -sarjan perusteella. Voit määrittää lisäyksen valittujen yksiköiden uudelleenjärjestelylle. Kunkin yksikön valittu yksikkö-, taso- ja/tai järjestysnumero päivitetään lisäyksen mukaisesti.

#### <a name="sorting"></a>Lajittelu
Voit käyttää **Lajitteluperuste**-vaihtoehtoa, jos haluat tarkastella yksikköluetteloa järjestyksessä.

### <a name="truncating"></a>Katkaiseminen
Tuontiprojekteissa voit katkaista entiteettien tietueet ennen tuontia. Tästä on hyötyä, jos tietueet on tuotava tyhjiin tauluihin. Oletusarvon mukaan tämä asetus ei ole käytössä.

## <a name="validate-that-the-source-data-and-target-data-are-mapped-correctly"></a>Vahvista, että lähde- ja kohdetiedot liitetään oikein
Määritys on toiminto, jota käytetään sekä tuonti-, että vientitöissä.

- Tuontityössä määrityksellä kuvataan, mistä lähdetiedoston sarakkeista tehdään sarakkeita väliaikaisessa taulukossa. Järjestelmä voi siten määrittää, mitkä lähdetiedoston sarakkeet tulee kopioida mihinkin väliaikaisen taulukon sarakkeisiin.
- Vientityössä määrityksellä kuvataan, mistä väliaikaisen taulukon (eli lähteen) sarakkeista tehdään sarakkeita kohdetiedostossa.

Jos väliaikaisen taulukon ja kohdetiedoston sarakenimet vastaavat, järjestelmä luo määrityksen automaattisesti nimien perusteella. Jos nimet eivät vastaa, sarakkeita ei määritetä automaattisesti. Tällöin sinun on tehtävä määritys valitsemalla **Näytä yhdistämismääritykset** -vaihtoehto tietotyön yksikössä.

Järjestelmässä on kaksi määritysnäkymää: **Yhdistämismääritysten visualisointi**, joka on oletusnäkymä, ja **Yhdistämistiedot**. Punainen tähti (\*) osoittaa kohteen kaikki pakolliset kentät. Nämä kentät on yhdistettävä, ennen kuin voit käsitellä yksikköä. Muiden kenttien yhdistämisen voi poistaa tarvittaessa, kun käsittelet yksikköä. Voit poistaa kentän yhdistämisen valitsemalla sen joko **Yksikkö**- tai **Lähde**-sarakkeessa ja valitsemalla sitten **Poista valinta**. Tallenna muutokset **Tallenna**-painikkeella ja sulje sivun palataksesi projektiin. Voit käyttää samaa prosessia muokataksesi kenttien yhdistämismäärityksiä lähteen ja väliaikaisen taulukon välillä tuonnin jälkeen.

Voit luoda yhdistämismäärityksen sivulla valitsemalla **Luo lähteen yhdistämismääritys**. Luotu määritys toimii kuin automaattinen määritys. Tämän vuoksi yhdistämättömät kentät on yhdistettävä manuaalisesti.

![Tietotyypin yhdistämismääritys](./media/dixf-map.png)

## <a name="verify-the-security-for-your-import-or-export-job"></a>Tarkista tuonti- tai vientityön turvallisuus
Voit rajoittaa **Tietojenhallinta**-työtilan käyttöoikeutta, jotta muut kuin järjestelmänvalvojat voivat käyttää vain tiettyjä töitä. Käyttöoikeus tietotyöhön tarkoittaa täyttä käyttöoikeutta kyseisen työn suoritushistoriaan sekä väliaikaisiin tauluihin. Sinun on siis varmistettava, että käyttöoikeudet on asetettu asianmukaisesti, kun luot tietotyön.

### <a name="secure-a-job-by-roles-and-users"></a>Työn suojaaminen roolien ja käyttäjien perusteella
**Soveltuvat roolit** -valikkoa voidaan käyttää työn rajoittamiseen tietyille käyttöoikeusrooleille. Vain kyseisiin rooleihin kuuluvat käyttäjät voivat käyttää työtä.

Voit myös rajoittaa työn tietyille käyttäjille. Kun suojaat työn käyttäjien perusteella roolien sijaan, voit hallita käyttöoikeuksia tarkemmin, jos roolilla on useita käyttäjiä.

### <a name="secure-a-job-by-legal-entity"></a>Työn suojaaminen yrityksen perusteella
Tietotyöt ovat yleisiä. Näin ollen, jos tietotyö on luotu ja käytössä yrityksessä, työ on näkyvissä kaikissa muissakin järjestelmän yrityksissä. Tämän oletustoiminta voi olla haluttua tietyissä sovelluksen skenaarioissa. Organisaatio voi esimerkiksi tuoda laskujen tietoja tietoyksiköiden ja tarjota keskitetyn laskujen käsittelyryhmä, joka vastaa organisaation kaikkien osastojen laskuvirheiden käsittelystä. Tällöin on hyvä antaa kaikkien keskitetyn laskujen käsittelyryhmän jäsenten käyttää kaikkien yritysten laskujen tuontitöitä. Oletusasetus täyttää täten tarpeen yrityksen näkökulmasta.

Organisaatio voi kuitenkin haluta yrityskohtaiset laskujen käsittelyryhmät. Tässä tapauksessa yrityksen ryhmällä tulee olla käyttöoikeus ainoastaan oman yrityksensä laskujen tuontityöhön. Nämä vaatimukset täytetään määrittämällä tietotöille yrityspohjaiset käyttöoikeudet työn sisäisestä **Soveltuvat yritykset** -valikosta. Kun määritykset on tehty, käyttäjät näkevät vain työt, jotka ovat käytettävissä yrityksessä, johon he ovat kirjautuneena. Nähdäkseen toisen yrityksen työt, käyttäjien on vaihdettava kyseiseen yritykseen.

Työ voidaan suojata samaan aikaan rooli-, käyttäjä- ja yritysperusteisesti.

## <a name="run-the-import-or-export-job"></a>Suorita tuonti- tai vientityö
Voit suorittaa työn kerran valitsemalla **Tuo**- tai **Vie**-painikkeen, kun olet määrittänyt työn. Voit määrittää toistuvan työn valitsemalla **Luo toistuva tietotyö**.

## <a name="validate-that-the-job-ran-as-expected"></a>Vahvista, että työ suoritettiin odotetulla tavalla
Työhistoria on käytettävissä tuonti- ja vientitöiden ongelmanratkaisuun ja tutkintaan. Historian työt on järjestetty aikajaksoille.

![Työhistorian jaksot](./media/dixf-job-history.md.png)

Kukin ajettu työ sisältää seuraavat tiedot:

- Suorituksen tiedot
- Suoritusloki

Suorituksen tiedoissa näkyy kunkin työn käsittelemän tietoyksikön tila. Näin löydät nopeasti seuraavat tiedot:

- Käsitellyt yksiköt
- Yksiköstä käsitellyt tietueet ja epäonnistuneiden tietueiden määrä
- Kunkin yksikön väliaikaiset tietueet

Voit ladata vientitöiden väliaikaiset tiedot tiedostona, tai voit ladata ne pakettina tuonti- ja vientitöitä varten.

Voit avata suoritustiedoista suorituslokin.

## <a name="clean-up-the-staging-tables"></a>Tyhjennä väliaikaiset taulut
Väliaikaiset taulut voi tyhjentää **Tietojenhallinta**-työtilan **Tyhjennä väliaikaiset taulut** -ominaisuuden avulla. Voit valita kustakin väliaikaisesta taulusta poistettavat tietueet seuraavilla asetuksilla:

- **Yksikkö** – jos tarjottuna on vain yksikkö, kaikki kyseisen yksikön väliaikaisen taulun tietueet poistetaan. Valitsemalla tämän voit tyhjentää kaikki yksikön tietoprojektien ja -töiden tiedot.
- **Työn tunnus** – jos vain työn tunnus on annettu, kaikki valitun työn yksiköiden tietueet poistetaan asianmukaisista väliaikaisista tauluista.
- **Tietoprojektit** – jos valittuna on vain tietoprojekti, kaikki valitun projektin kaikkien töiden yksiköihin kuuluvat kaikki tietueet poistetaan.

Poistettavaa tietojoukkoa voi myös rajoittaa yhdistämällä asetuksia.

