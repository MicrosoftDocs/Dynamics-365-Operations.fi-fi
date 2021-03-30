---
title: Kaksikäyttötuotteet
description: Tässä ohjeaiheessa käsitellään kaksikäyttötuotteiden jäljittämistä, kunkin tällaisen tuotteen varmennenumeroiden ja kohdemaan tallennusta sekä kelpaavien varmennenumeroiden tulostamista liittyviin laskuihin, pakkausluetteloihin ja/tai myyntitilauksiin.
author: dasani-madipalli
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: COODualUseCerts, COORules, COODualUseCountries
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: a6cc730f8d672d906072a9b97b737dbdea9faf2d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243198"
---
# <a name="dual-use-goods"></a>Kaksikäyttötuotteet

[!include [banner](../includes/banner.md)]

Kaksikäyttötuotteet ovat tyypillisesti nimikkeitä, joilla on sekä siviilikäyttötarkoitus että sotilaallinen käyttötarkoitus. Esimerkiksi kemikaalia voidaan käyttää joko lannoitteena tai räjähteenä. Monissa maissa on erityissäädöksiä, jotka koskevat kaksikäyttötuotteiden vientiä, tuontia ja kuljetusta. Tämän vuoksi on tärkeää, että kaksikäyttötuotteiden kansainväliseen kauppaan osallistuvat yritykset seuraavat käytäntöjä ja varmenteita.

Kaksikäyttötoiminto auttaa yrityksiä jäljittämään kaksikäyttötuotteiksi määritettyjä tuotteita, tallentamaan kunkin tällaisen tuotteen varmennenumerot ja kohdemaan sekä tulostamaan kelvolliset varmennenumerot liittyviin laskuihin, pakkausluetteloihin ja/tai myyntitilauksiin. Tämä auttaa varmistamaan, että lähetetyt tuotteet sisältävät aina ajan tasalla olevat todistukset.

Esimerkkiskenaarioita:

1. Järjestelmän **Kaksikäytön maa-asetukset** -sivu ilmaisee, että Ranskaan menevissä lähetyksissä tarvitaan sertifiointi.
2. Tuotteen X-100 **Vapautetun tuotteen tiedot** -sivu ilmaisee, että kyse on kaksikäyttötuotteesta. Koodi, luokka, ryhmä ja hallintotapa ilmaisevat yhdessä, mihin vientivalvontaluokitukseen tuote kuuluu.
3. **Kaksikäyttötodistukset**-sivu sisältää tuotteen X-100 todistuksen, kun se lähetetään Ranskaan. Tämä todistus vanhenee 1. tammikuuta 2020.
4. Luot 17. kesäkuuta 2020 myyntitilauksen ranskalaiselle asiakasyritykselle, ja tilaus sisältää tuotteen X-100.
5. Kun tallennat myyntitilauksen, järjestelmää määrittää seuraavat tiedot:

    1. Sisältääkö tilaus kaksikäyttötuotteita?
    2. Jos tilaus sisältää kaksikäyttötuotteita, edellyttääkö kohdemaa kaksikäyttötodistuksia?
    3. Ja maa edellyttää kaksikäyttötodistuksia, onko kullekin kohdemaan tuotteelle voimassaoleva todistus?

6. Tilaus sisältää tuotteen X-100, tuote lähetetään Ranskaan ja tuotteella on ranskalainen varmenne. Varmenne on kuitenkin vanhentunut. Niinpä näyttöön tulevaa varoitus, jonka mukaan vähintään yhden tämän myyntitilauksen kaksikäyttönimikkeen kaksikäyttövarmenne ei ole voimassa. Haluatko jatkaa vahvistamista?

Tässä ohjeaiheessa kaikkien niiden asetusten määrittämistä, jotka tarvitaan kaksikäyttötuotteiden määrittämiseen ja tämän skenaarion tukemiseen.

## <a name="define-dual-use-requirements-for-each-relevant-country"></a>Kaksikäyttöedellytysten määrittäminen kullekin liittyvälle maalle

Eri maissa on erilaisia kaksikäyttötuotteita koskevia vaatimuksia. Voit seurata **Maakohtaiset kaksikäyttöasetukset** -sivun avulla, missä maissa todistus tarvitaan ja missä ei. Tässä määritetyt tiedot tarkistetaan myyntitilausten luonnin yhteydessä, ja sinua muistutetaan tarvittavien todistusten antamisesta.

Eri maiden kaksikäyttövaatimuksia koskevat tiedot määritetään seuraavasti:

1. Valitse **Tuotetietojen hallinta \> Asetukset \> Tuotteen yhteensopivuus \> Kaksikäyttötuotteet \> Maakohtaiset kaksikäyttöasetukset**.
2. Valitse aiemmin luodun maan asetukset muokattavaksi tai luo uudet maa-asetukset valitsemalla toimintoruudussa **Uusi**.
3. Määritä seuraavat valittujen tai uusien maa-asetusten arvot:

    | Kenttä | kuvaus |
    |---|---|
    | Maa/alue | Valitse maa, jonka vaatimuksia seurataan. |
    | Varmenne tarvitaan | Valitse tämä valintaruutu niiden maisen osalta, jotka edellyttävät kaksikäyttötuotteiden varmenteen. Poista sen valinta niiden maiden osalta, joissa varmennetta ei tarvita. |

## <a name="create-dual-use-categories"></a>Kaksikäyttöluokkien luominen

Kaksikäyttötuotteet on usein luokiteltava niiden ECCN (Export Control Classification Number) -numeron mukaan. ECCN on aakkosnumeerinen koodi, joka luokittelee nimikkeet tekijöiden, kuten kauppatavara ja teknologia, perusteella. **Kaksikäyttöluokat**-sivu auttaa luomaan raportointia varten luettelon käytetyistä luokista.

Kaksikäyttöluokat määritetään seuraavasti:

1. Valitse **Tuotetietojen hallinta \> Asetukset \> Tuotteen yhteensopivuus \> Kaksikäyttötuotteet \> Kaksikäyttöluokat**.
2. Valitse aiemmin luotu luokka muokattavaksi tai luo uusi luokka valitsemalla toimintoruudussa **Uusi**.
3. Määritä seuraavat valitun tai uuden luokan arvot:

    | Kentät | kuvaus |
    |---|---|
    | Kaksoiskäyttökoodi | Anna koko ECCN-koodi (kuten *3A001*).|
    | Kaksoiskäyttöluokka | Anna ECCN-koodin CCL (Commerce Control List) -luokkaosa. Esimerkiksi ECCN-koodissa *3A001* tämä arvo on *3*. |
    | Kaksoiskäyttöryhmä | Anna ECCN-koodin tuoteryhmäosa. Esimerkiksi ECCN-koodissa *3A001* tämä arvo on *A*. |
    | Kaksoiskäyttötuotteiden hallinta | Anna nimikkeen hallintakoodi. Tämä koodi ilmaisee syyn, minkä vuoksi nimike on luokiteltu kaksikäyttötuotteeksi. Esimerkiksi ECCN-koodissa *3A001* tämä arvo on *001*. |

## <a name="apply-dual-use-categories-to-products"></a>Kaksikäyttöluokkien käyttäminen tuotteissa

Tuote määritetään kaksikäyttötuotteeksi ja kaksikäyttöluokka otetaan siinä käyttöön seuraavasti:

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Avaa tuotteen **Vapautetun tuotteen tiedot** -sivu valitsemalla tai luomalla tuote.
1. Määritä **Ulkomaankauppa**-pikavälilehden **Kaksoiskäyttötuotteet**-asetukseksi **Kyllä**, jolloin kyseessä oleva tuote tunnistetaan kaksikäyttötuotteeksi.
1. Määritä **Kaksikäyttökoodi**-kenttään nykyistä tuotetta koskeva koodi. (Tämä koodi määritettiin **Kaksikäyttöluokat**-sivulla.)

Tämä asetus tarkistetaan myyntitilauksen luonnin yhteydessä.

## <a name="set-up-dual-use-certificates"></a>Kaksikäyttövarmenteiden määrittäminen

**Kaksikäyttövarmenteet**-sivulla määritetään ja hallitaan kunkin tuotteen ja kunkin maan pakollisia kaksikäyttövarmenteita. Kunkin varmenteen tietoja, kuten maata ja voimassaolopäiviä, voidaan seurata. Voit lisäksi määrittää vaihtoehtoja, jotka määrittävät, mihin nämä tiedot tulostetaan. Tiedot voidaan tulostaa esimerkiksi laskuun, pakkausluetteloon ja/tai myyntitilaukseen. Tämä asetus tarkistetaan myyntitilauksen luonnin yhteydessä.

1. Valitse **Tuotetietojen hallinta \> Asetukset \> Tuotteen yhteensopivuus \> Kaksikäyttötuotteet \> Kaksikäyttövarmenteet**.
2. Valitse aiemmin luotu varmenne muokattavaksi tai luo uusi varmenne valitsemalla toimintoruudussa **Uusi**.
3. Määritä seuraavat valitun tai uuden varmenteen arvot:

    | Kenttä | kuvaus |
    |---|---|
    | Nimiketunnus | Valitse sen kaksikäyttötuotteen nimiketunnus, jota tämä varmenne koskee. |
    | Maa/alue | Kohdemaa tai -alue, jossa tätä varmennetta on käytettävä. |
    | Varmenteen numero | Numero joka näkyy toimittajalle tai asiakkaalle myönnetyssä varmenteessa. |
    | Voimassa | Valitse ensimmäinen päivämäärä, jolloin nykyinen varmenne on voimassa.|
    | Vanhentumisaika | Valitse viimeinen päivämäärä, jolloin nykyinen varmenne on voimassa. |
    | Tulosta laskulle | Valitse tämä valintaruutu, kun varmennenumero tulostetaan laskuihin, joiden osoitteena on määritetty maa määritetyllä päivämääräalueella. |
    | Tulosta pakkausluettelossa | Valitse tämä valintaruutu, kun varmennenumero tulostetaan pakkausluetteloihin, joiden osoitteena on määritetty maa määritetyllä päivämääräalueella. |
    | Tulosta myyntitilauksessa | Valitse tämä valintaruutu, kun varmennenumero tulostetaan myyntitilauksiin, joiden osoitteena on määritetty maa määritetyllä päivämääräalueella. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]