---
title: Maksutunnuksen käytön rajoittaminen
description: Tässä artikkelissa kerrotaan ominaisuudesta, joka rajoittaa maksutunnusten käyttämistä Microsoft Dynamics 365 Commercessa.
author: BrianShook
ms.date: 10/20/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-09-20
ms.openlocfilehash: 8092ab0724f33f21759aa84d25e0bdcb5b2ad5dd
ms.sourcegitcommit: 6bd8822f7aa781d596b70956bead834117cf302c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709649"
---
# <a name="limit-payment-token-usage"></a>Maksutunnuksen käytön rajoittaminen

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Tässä artikkelissa kerrotaan ominaisuudesta, joka rajoittaa maksutunnusten käyttämistä Microsoft Dynamics 365 Commercessa. Tunnuksen käyttöä rajoitetaan myyntitilausten yhteydessä tai se tallennetaan korttina tiedostoon, jos asiakas antaa suostumuksen tähän.

## <a name="key-terms"></a>Tärkeimmät termit

| Kausi | Kuvaus |
|---|---|
| Tunnus | Viitattu XML-blob-objekti Dynamics 365 -järjestelmässä tallentaa maksuviitteet tapahtumia varten. |
| Kortti tiedostossa | Tallennettu korttiviitetunnus, jota voi käyttää tulevaisuudessa Dynamics 365 -järjestelmässä tai maksuyhdyskäytävässä. Se on asiakastilikohtainen. |

Maksutunnuksen käytön rajoitukset koskevat kaikkia ympäristöjä, joissa käytetään maksuyhdyskäytäväpalvelua, jossa käytetään toistuvia tunnuksia. Valmis [Dynamics 365 Payment Connector Adyenia varten](adyen-connector.md) käyttää toistuvia maksutunnuksia suorittaessaan seuraavia tilaustoimintoja, kuten valtuutusten oikaisuja ja uudelleenvaltuutuksia.

Näitä koko järjestelmässä käytettäviä toistuvia maksutunnuksia voi hallita **Rajoita maksutunnuksen käyttö tilauksen kontekstiin** -ominaisuuden avulla. Se rajoittaa toistuvan tunnuksen käyttöä järjestelmän myyntitilausten yhteydessä. Kun ominaisuus on otettu käyttöön, se muokkaa Commerce headquartersin käyttöliittymää päivittämällä maksun syötön sivut ja rajoittamalla aiempien asiakasmaksujen viitteiden valintaa uusissa tapahtumissa käytettäviksi.

Tämän ominaisuuden avulla voit täyttää joidenkin maksujen myöntäjien, kuten Visan, käyttöä koskevat säännöt. Visa määrittää [Visan perussäännöissä ja Visan tuote- ja palvelusäännöissä](https://usa.visa.com/content/dam/VCOM/download/about-visa/visa-rules-public.pdf) niiden maksutunnusten käytön, joita tulee rajoittaa tapahtumissa, jos kortinhaltija ei määritä toisin.

**Rajoita maksutunnuksen käyttö tilauksen kontekstiin** -ominaisuus on olennainen vain, jos käytössä on toistuvia maksutunnusten viitteitä käyttävä maksuyhdyskäytäväpalvelu.

## <a name="enable-the-feature"></a>Toiminnon käyttöönotto

Jos haluat ottaa **Rajoita maksutunnuksen käyttö tilauksen kontekstiin** -ominaisuuden käyttöön, siirry ympäristön Commerce headquartersissa kohtaan **Työtilat \> Ominaisuuksien hallinta**, etsi **Rajoita maksutunnuksen käyttö tilauksen kontekstiin** -kohta luettelosta ja valitse se. Valitse lopuksi **Ota käyttöön nyt**.

## <a name="limit-payment-token-usage"></a>Maksutunnuksen käytön rajoittaminen

Kun ominaisuus on käytössä, maksutavan sieppaamisessa käytettäville Commerce headquartersin sivuille päivitetään tapa, jolla tallennettuihin asiakkaan maksutapoihin viitataan. Tämä päivitys vaikuttaa pääasiassa seuraaviin kahteen toimintoalueeseen:

- tallennetun asiakaskortin syöttäminen asiakkaan puolesta
- maksutietojen tallentaminen asiakkaalle tulevia myyntitilauksen maksutapahtumia varten.

Kun asiakas käyttää Commerce-kanavia, maksutiedot tallennetaan myyntitilauksen kontekstiin. Myyntitilauksen konteksti rajoittaa maksutunnuksen käyttöä niin, että sitä ei käytetä maksuviitteenä asiakastietueessa maksusivuilla uusissa tai muokatuissa myyntitilauksen maksuissa Commerce headquartersissa.

### <a name="payment-form-changes"></a>Maksulomakkeen muutokset

Kun puhelinkeskuksen tai Commerce headquartersin käyttäjä maksaa asiakkaan puolesta myyntitilauksesta, maksusivulla näkyy maksutavan valinnan tiedot. Kun **Rajoita maksutunnuksen käyttö tilauksen kontekstiin** -ominaisuus on käytössä ja käyttäjä valitsee plusmerkin (**+**) maksusivulla, vain Tallennettu kortti -tietueet näytetään. Muutokset edellyttävät puhelinkeskuksen tai Commerce headquartersin käyttäjän asiakkaan **Syötä asiakkaan maksutiedot** -sivulle uuden myyntitilaustapahtuman yhteydessä täyttäneiden kaikkien maksutietojen syöttämistä.

**Numero**-kentän arvoluettelo sisältää vain korttiviitteet, jotka liittyvät tallennetun kortin omaavaan asiakkaaseen. Se suodattaa pois kaikki aiemmat maksuviitteet, jotka eivät kuulu myyntitilaukseen.

Plusmerkki (**+**) **Numero**-kentässä säilytetään. Sitä voi käyttää niiden maksutietojen syöttämisessä, jotka asiakas antaa käsittelyssä olevaan myyntitilaukseen liittyvää tapahtumaa varten.

### <a name="how-cards-on-file-work"></a>Tallennettujen korttien käsitteleminen

Kun **Rajoita maksutunnuksen käyttö tilauksen kontekstiin** -ominaisuus on otettu käyttöön, tallennettu kortti on toistuva maksutunnus, joka tallennetaan asiakastietueeseen. Sitä ei rajoiteta myyntitilauksen kontekstissa. Tallennettu kortti mahdollistaa nopean viittauksen Commerce headquartersiin, kun käyttäjät täyttävät maksusivulla uuden myyntitilauksen maksua. Tämä tunnusviite on käytettävissä vain Dynamics 365 -ympäristössä. Maksuyhdyskäytävää käyttävissä online-kanavissa, joissa käyttäjät tallentavat maksutavan tulevaa käyttöä varten maksun iFrame-moduulissa, maksuyhdyskäytävä tallentaa turvallisesti nämä viitteet erillisenä viitteenä tallennettavaan Dynamics 365 -korttiin.

Jos esimerkiksi Dynamics 365 Commerce Payment Connector Adyenia varten on käytössä online-kanavassa, luottokorttitiedot maksun iFrame-moduuliin syöttävät asiakkaat näkevät vain yhdyskäytäväpalvelun korttiviitteet seuraavaa verkko-ostoa varten todentamisen yhteydessä. He eivät näe Dynamics 365 -ympäristöön tallennettua korttia maksun iFrame-moduulin vaihtoehtona. Samoin ostajien tehdessä tilausta puhelinkeskuksen kautta heidän online-tilassa tallennettuja korttiviitteitään ei näytetä vaihtoehtoina puhelinkeskuksen käyttäjälle. Puhelinkeskuksen käyttäjät näkevät vain edelliset tallennetut kortin viitteet Dynamics 365-järjestelmästä (asiakkaan kanssa sovitulla tavalla) tulevissa tilauksissa käytettäviksi.

Commerce headquartersin käyttäjät voivat tallentaa kortin asiakkaalle siirtymällä kohtaan **Retail ja Commerce \> Asiakkaat** ja valitsemalla asiakastilitietueen. Jos käyttäjällä on maksusivujen käyttöoikeus, he voivat käyttää **Asiakas \> Määritys** -osassa **Luottokortit**-syöttösivua syöttäessään maksukortin, joka tallennetaan tulevia tapahtumia varten. Tämä toiminto säästää aikaa, kun asiakkaan tulevia myyntitilausmaksuja käsitellään. Puhelinkeskuksen ja Commerce headquartersin käyttäjien on syötettävä tallennetun kortin tiedot vain, jos asiakas suostuu kortin viitteen käyttöön tulevissa tapahtumissa.

Commerce headquartersin maksusivujen alaosassa olevan **Tallenna tulevaa käyttöä varten** -valintaruudun avulla käyttäjät voivat tallentaa kortin tiedot. Tätä valintaruutua tulee käyttää vain, jos asiakas suostuu tallennetun kortin käyttöön tulevissa tapahtumissa. Voit näyttää **Tallenna tulevaa käyttöä varten** -valintaruudun tai rajoittaa sen näyttämistä **Salli asiakaskortti tiedostossa** -vaihtoehdon avulla **Maksu**-välilehdessä **Puhelinkeskuksen parametrit** -sivulla Commerce headquartersissa. Kun tämän vaihtoehdon arvoksi määritetään **Kyllä**, Commerce headquartersin käyttäjä, jolla on maksusivujen käsittelyn käyttöoikeus, voi tallentaa kortin käyttämällä **Tallenna tulevaa käyttöä varten** -valintaruutua. Kun vaihtoehdon arvoksi on määritetty **Ei**, valintaruutu ei ole käytettävissä Commerce headquartersin käyttäjille, joilla on maksusivujen käsittelyn käyttöoikeus. **Salli asiakaskortti tiedostossa** -vaihtoehtoa voi käyttää, jos yritys haluaa rajoittaa toistuvien tunnusten käyttämistä Commerce headquartersissa, mutta ei silti halua sallia kortin tallentamista ilman, että asiakkaan suostumuksen antaminen varmistetaan.

### <a name="commerce-headquarters-pages-where-the-recurring-token-restrictions-are-enforced"></a>Commerce headquartersin sivut, joissa toistuvan tunnuksen rajoitukset otetaan käyttöön

Tunnusten rajoittamisen laajuus vaikuttaa Commerce headquartersin seuraavilla alueilla, kun ominaisuus otetaan käyttöön:

- Asiakasmaksun tiedot kohdassa **Myyntitilaus \> Maksut \> Syötä asiakasmaksu**
- Jatkuvuustilaukset
- Maksuerämaksut
- Myyntireskontran luottokorttimaksut

### <a name="manage-payment-tokens-archiving-or-removal"></a>Maksutunnusten hallinta (arkistoiminen tai poistaminen)

Maksutunnukset, jotka luotiin ennen kuin **Rajoita maksutunnuksen käyttö tilauksen kontekstiin** -ominaisuuden merkintä otettiin käyttöön (tai kun ominaisuus poistettiin käytöstä), jäävät määrittämättömiksi järjestelmässä. Niihin voi viitata Commerce headquartersin maksusivun valintaluetteloissa. Nämä tunnukset voidaan poistaa Commerce headquartersissa säännöllisesti kahdella eri tavalla:

- Määritä **Arkistoi luottokorttitapahtumatiedot** -sivulla työ, joka säännöllisesti tyhjentää maksutunnukset tai arkistoi ne. Jos määrität **Poista tiedot ennen arkistointia** -vaihtoehdon arvoksi **Kyllä**, **Tapahtuman vähimmäisikä (päivinä)** -asetusta vastaavat tunnukset poistetaan. Lisätietoja on kohdassa [Arkistoi luottokorttitapahtumatiedot](archive-cc-data.md).
- Käytä uutta **Tyhjennä luottokortin tunnukset** -sivua (**Myyntireskontra \> Kyselyt ja raportit \> Puhdista \> Tyhjennä luottokortin tunnukset**), jonka avulla voit suorittaa tai määrittää erätyön, joka poistaa maksutunnukset. Määritä seuraavat parametrit:

    - **Tunnuksen vähimmäisikä päivinä** -arvon on oltava 90 päivää tai suurempi.
    - **Suorita taustalla** -asetuksen avulla voi määrittää **Toistuvuus**- tai **Hälytykset**-asetukset.
    - Eräryhmä voidaan määrittää suorittamaan tietyn ryhmän tehtävä.
    - Jos **Yksityinen**-vaihtoehdon arvoksi on määritetty **Kyllä**, vain työn tekijä voi suorittaa sen.
    - Jos **Kriittinen työ** -vaihtoehdon arvoksi on määritetty **Kyllä**, järjestelmä seuraa työn tilaa aktiivisesti.

Poistettuja tunnuksia ei voi noutaa. Määritä **Tunnuksen vähimmäisikä päivinä** -kenttään väli, joka sopii pisimpään suoritettavan tapahtuman elinkaareen ympäristössä (valtuutuksesta sieppaukseen tai hyvitykseen).

## <a name="additional-resources"></a>Lisäresurssit

[Maksut – usein kysytyt kysymykset](payments-retail.md)

[Kassamoduuli](../add-checkout-module.md)

[Maksumoduuli](../payment-module.md)
