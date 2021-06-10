---
title: Aallon etikettien uudelleentulostus ja mitätöinti
description: Tässä ohjeaiheessa käsitellään aiemmin luotujen aallon etikettien mitätöintiä ja uudelleentulostusta.
author: perlynne
ms.date: 07/09/2020
ms.topic: article
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSWaveTableListPage, WHSWorkException, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelLayout, WHSWaveLabelType, WHSWaveLabelTemplateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-07-09
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: caba37d3e7bb5d2f08a8c10ff0f0e1bc886e5648
ms.sourcegitcommit: 0cc89dd42c1924ca0ec735c6566bc56b39cc5f7d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/26/2021
ms.locfileid: "6102755"
---
# <a name="reprint-and-void-wave-labels"></a>Aallon etikettien uudelleentulostus ja mitätöinti

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään aaltokäsittelyn luomien etikettien hallintaa. (Tarkka kuvaus ja määritysohjeet ovat kohdassa [Aallon etikettitulostuksen määrittäminen](../warehousing/configure-wave-label-printing.md).)

Aallon etikettejä voi tulostaa uudelleen koska tahansa. Yksittäin etiketti voidaan esimerkiksi tulostaa siinä tapauksessa, että nykyinen on kadonnut tai vaurioitunut. Tai sitten varaston työntekijä tai työnjohtaja voi haluta tulostaa koko etikettirullan, jos aallon etikettisarjan numero ja/tai koostumus on muuttunut (esimerkiksi puuttuvan varaston tai jonkin muun syyn vuoksi). Usein koko rulla on tulostettava uudelleen, vaikka vain laatikoiden määrä olisi muuttunut, jotta kokonaismäärä pysyy oikeana kunkin etiketin Laatikko X/Y -osassa.

Aallon etiketin uudelleentulostustoiminto tukee seuraavia toimintoja:

- Etikettien uudelleentulostus sekä varastointisovelluksesta että raskaasta asiakkaasta.
- Etikettien mitätöinti ja uudelleentulostus samanaikaisesti. (Etikettien mitätöintimahdollisuus on upotettu esimerkiksi lyhyisiin keräilyskenaarioihin.)
- Aallon etikettihistorian tyhjentäminen.

Tämä ohjeaihe sisältää skenaariokokoelman, jotka näyttävät esimerkkien avulla, miten kutakin aallon etikettien uudelleentulostustoimintoa käytetään.

> [!IMPORTANT]
> Ohjeaiheen skenaarioiden käyttäminen edellyttää, että kyseiset aallon tulostustoiminnot otetaan käyttöön ja määritetään kohdassa [Aallon etikettitulostuksen määrittäminen](../warehousing/configure-wave-label-printing.md) kuvatulla tavalla. Useissa skenaarioissa lisäksi edellytetään aiheen skenaarioiden suorittamista, jotta tarvittavat näytetiedot ovat käytettävissä.

## <a name="scenario-1-reprint-labels-from-the-web-client"></a>Skenaario 1: Etikettien uudelleentulostus verkkoasiakasohjelmasta

Voit tarkastella aallon etikettejä ja tulostaa niitä uudelleen seuraavilta sivuilta. Valitse kunkin sivun toimintoruudun **Lähetykset**-välilehden **Aiheeseen liittyvät tiedot**-ryhmässä **Aallon etiketit**.

- Kaikki lähetykset \> Lähetyksen tiedot
- Kaikki kuormat \> Kuorman tiedot
- Kaikki aallot
- Aalto-otsikot
- Aallon etikettihistoria

Aallon etiketti tulostetaan verkkoasiakasohjelmasta seuraavasti:

1. Valitse **Varastonhallinta \> Lähtevät aallot \> Lähetysaallot \> Kaikki aallot**.
1. Valitse aalto, jonka etiketit tulostetaan uudelleen.
1. Valitse toimintoruudun **Aalto**-välilehden **Tulosta**-ryhmässä **Aallon etiketit**.
1. Tee sitten jompikumpi tai molemmat seuraavista:

    - Tulosta etiketti uudelleen valitsemalla tulostin **Tulostimen nimi** -kentässä. (Jätä tämä kenttä tyhjäksi, jos haluat vain päivittää aallon etikettitiedot muttet tulostaa etikettiä uudelleen.)
    - Päivitä etiketti valitsemalla **Päivitä aallon etikettitiedot** -valintaruutu. (Älä valitse tätä valintaruutua, jos haluat voin tulostaa aiemman etiketin uudelleen.)

    > [!NOTE]
    > Aina kun aallon etiketti tulostetaan tai uudelleentulostetaan, sen tiedot muunnetaan soveltuvan aallon etiketin asettelun kautta ja kaikki paikkamerkit korvataan varsinaisilla arvoilla. Kyseinen merkkijono tallennetaan sitten tietueena aallon etikettihistoriassa. Jos **Päivitä aallon etikettitiedot** -valintaruudun valinta poistetaan, tallennettuja ZPL (Zebra Programming Language) -tietoja käytetään, kun etiketti tulostetaan uudelleen. Jos **Päivitä aallon etikettitiedot** -valintaruutu valitaan, uusi merkkijono luodaan. Myös aiemmin luodut etiketit lasketaan uudelleen ja mahdolliset ylimääräiset etiketit (jos esimerkiksi liittyvät työrivit on peruutettu tai niitä on muokattu) merkitään **mitätöidyiksi** eikä niitä tulosteta uudelleen.

1. Vahvista valinta valitsemalla **OK**.

## <a name="scenario-2-reprint-labels-from-the-warehousing-app"></a>Skenaario 2: Etikettien uudelleentulostus varastointisovelluksesta

Tämä skenaario koskee tyypillisesti tilanteita,joissa etikettirulla kadonnut tai vaurioitunut. Siihen sisältä esimerkki näyttää, miten mobiililaitteen valikkovaihtoehdot määritetään siten, että työntekijät voivat tulostaa yksittäisiä tai useita etikettejä. Sen jälkeen näytetään, miten kyseisiä valikkovaihtoja käytetään mobiililaitteella.

### <a name="set-up-the-required-menu-items-and-menu-for-the-mobile-device"></a>Mobiililaitteen valikkovaihtoehtojen ja valikon määrittäminen

Ennen kuin työntekijät voivat uudelleentulostaa etikettejä mobiililaitteesta, kyseisten toimintojen valikkovaihtoehdot on määritettävä ja lisättävä varastointisovelluksen valikkoon.

#### <a name="create-new-mobile-device-menu-items"></a>Mobiililaitteen uusien valikkovaihtoehtojen luominen

Luo varastointisovelluksesta uudelleentulostettavien etikettien uusi valikkovaihtoehtokokoelma seuraavasti:

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.
1. Luo valikkovaihtoehto ja määritä sille seuraavat arvot:

    - **Valikkovaihtoehdon nimi:** *Tulosta yksi aallon etiketti uudelleen*
    - **Otsikko:** *Tulosta yksi aallon etiketti uudelleen*
    - **Tila:** *Epäsuora*
    - **Tehtäväkoodi:** *Tulosta yksi aallon etiketti uudelleen*

1. Luo toinen valikkovaihtoehto ja määritä sille seuraavat arvot:

    - **Valikkovaihtoehdon nimi:** *Tulosta etiketit uudelleen (nimike)*
    - **Otsikko:** *Tulosta aallon etiketit (nimike)*
    - **Tila:** *Epäsuora*
    - **Tehtäväkoodi:** *Tulosta useita aallon etikettejä uudelleen*
    - **Näytä työluettelon ryhmittelysuodatin:** *Kyllä*
    - **Järjestelmän ryhmittelykenttä:** *ShipmentID*
    - **Järjestelmän ryhmittelykentän etiketti:** *Lähetystunnus*
    - **Tulostustila:** *Tuote*

1. Valitse toimintoruudussa **Kenttäluettelo**. Voit sitten valita avautuvalla sivulla kentät, joiden näyttäminen auttaa työntekijöitä tunnistamaan oikean etikettirullan.
1. Näytettäviä kenttiä on enintään seitsemän. Kunkin käytettävissä olevan paikan kenttä valitaan avattavasta luettelosta. Jos kenttää ei tarvita, jätä se tyhjäksi. 

    Tässä on esimerkki:

    - **Näyttökenttä:** *LabelItemId*
    - **Näyttökenttä 2:** *LabelItemName*
    - **Näyttökenttä 3:** *InventQty*
    - **Näyttökenttä 4:** *LabelUnitId*

1. Sulje sivu.
1. Luo kolmas valikkovaihtoehto ja määritä sille seuraavat arvot:

    - **Valikkovaihtoehdon nimi:** *Tulosta etiketit uudelleen (valintalista)*
    - **Otsikko:** *Tulosta aallon etiketit (valintalista)*
    - **Tila:** *Epäsuora**
    - **Tehtäväkoodi:** *Tulosta useita aallon etikettejä uudelleen*
    - **Näytä työluettelon ryhmittelysuodatin:** *Kyllä*
    - **Järjestelmän ryhmittelykenttä:** *ShipmentID*
    - **Järjestelmän ryhmittelykentän etiketti:** *Lähetystunnus*
    - **Tulostustila:** *Luettelointi*

1. Valitse toimintoruudussa **Kenttäluettelo**. Valitse sitten avattavissa luetteloissa kentät, joiden avulla työntekijät tunnistavat oikean etikettirullan (esimerkiksi *LabelItemId*, *LabelItemName*, *InventQty*, *LabelUnitId* ja *NumberOfLabels*).
1. Sulje sivu.
1. Luo neljäs valikkovaihtoehto ja määritä sille seuraavat arvot:

    - **Valikkovaihtoehdon nimi:** *Tulosta etiketit uudelleen (viimeisen mukaan)*
    - **Otsikko:** *Tulosta aallon etiketit (viimeisen mukaan)*
    - **Tila:** *Epäsuora*
    - **Tehtäväkoodi:** *Tulosta useita aallon etikettejä uudelleen*
    - **Näytä työluettelon ryhmittelysuodatin:** *Kyllä*
    - **Järjestelmän ryhmittelykenttä:** *ShipmentID*
    - **Järjestelmän ryhmittelykentän etiketti:** *Lähetystunnus*
    - **Tulostustila:** *Viimeisen hyväksyttävän aallon etiketin tunnus*

1. Valitse toimintoruudussa **Kenttäluettelo**. Valitse sitten avattavissa luetteloissa kentät, joiden avulla työntekijät tunnistavat oikean etikettirullan (esimerkiksi *LabelItemId*, *LabelItemName*, *InventQty*, *LabelUnitId* ja *NumberOfLabels*).
1. Sulje sivu.

#### <a name="set-up-the-mobile-device-menu"></a>Mobiililaitteen valikon määrittäminen

Lisää uudet valikkovaihtoehdot varastointisovelluksen valikkoon seuraavasti:

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikko**.
1. Valitse aiemmin luotu **Lähtevät**-valikko.
1. Etsi vasemmasta luettelosta juuri luodut uudelleentulostuksen valikkovaihtoehdot ja lisää ne oikealla olevaan luetteloon oikealla nuolipainikkeella.
1. Sulje sivu.

### <a name="use-cases"></a>Käyttötapaukset

Annetut käyttötapaukset ovat esimerkkejä, jotka osoittavat, miten työntekijät voivat käyttää määritettyjä mobiililaitteen valikkovaihtoehtoja aallon etikettien uudelleentulostuksessa.

Varmista ennen käyttötapauksiin siirtymistä, että seuraavat edellytykset täyttyvät:

- Esittelytiedot on asennettu ja **USMF**-yritys on valittu.
- Aallon etikettitulostus on määritetty ja etikettejä on luotu kohdassa [Aallon etikettitulostuksen määrittäminen](../warehousing/configure-wave-label-printing.md) kuvatulla tavalla.

#### <a name="use-case-21-a-single-wave-label-is-scratched-and-must-be-reprinted"></a>Käyttötapaus 2.1: Yksi aallon etiketti on repaleinen ja tulostettava uudelleen.

1. Kirjaudu varastointisovellukseen varaston *62* käyttäjänä. (Kirjaudu vakioesittelytiedoissa sisään käyttäjätunnuksella *62* ja salasanalla *1*.)
1. Valitse **Lähtevät \> Tulosta yksi aallon etiketti uudelleen**.
1. Anna aallon etiketin tunnus tai skannaa se.
1. Valitse uudelleentulostuksen tulostin.
1. Vahvista tehtävä valitsemalla **OK**.

#### <a name="use-case-22-several-labels-for-boxes-of-the-same-item-were-damaged-and-must-be-reprinted-each-label-has-a-product-bar-code-but-no-enumeration-or-sscc-number"></a>Käyttötapaus 2.2: Useita saman nimikkeen pakkauksen etikettejä vaurioitui, ja ne on tulostettava uudelleen. Kussakin etiketissä on tuotteen viivakoodi mutta ei luettelointi- tai SSCC-numeroa.

1. Kirjaudu varastointisovellukseen varaston *62* käyttäjänä. (Kirjaudu vakioesittelytiedoissa sisään käyttäjätunnuksella *62* ja salasanalla *1*.)
1. Valitse **Lähtevät \> Tulosta etiketit uudelleen (nimike)**.
1. Anna lähetyksen tunnus tai skannaa se.
1. Valitse uudelleentulostusta varten ruutu, jossa on oikea etikettirulla.
1. Lukemalla tuotteen viivakoodin aiemmin luodussa etiketissä voit vahvistaa, että oikea rivi on valittu.
1. Anna uudelleentulostettavien etikettien määrä.
1. Valitse uudelleentulostuksen tulostin.
1. Vahvista tehtävä valitsemalla **OK**.

#### <a name="use-case-23-several-labels-for-boxes-werent-printed-because-of-a-printer-jam-because-the-labels-have-enumeration-you-can-define-the-carton-range-to-reprint"></a>Käyttötapaus 2.3: Useita pakkausten etikettejä ei tulostettu tulostimen tukoksen vuoksi. Koska etiketti käyttää luettelointia, voit määrittää uudelleentulostettavan laatikkoalueen.

1. Kirjaudu varastointisovellukseen varaston *62* käyttäjänä. (Kirjaudu vakioesittelytiedoissa sisään käyttäjätunnuksella *62* ja salasanalla *1*.)
1. Valitse **Lähtevät \> Tulosta etiketit uudelleen (valintalista)**.
1. Anna lähetyksen tunnus tai skannaa se.
1. Valitse uudelleentulostusta varten ruutu, jossa on oikea etikettirulla.
1. Anna ensimmäinen pakkaus, jonka etiketti tulostetaan uudelleen.
1. Anna viimeinen pakkaus, jonka etiketti tulostetaan uudelleen. Vaihtoehtoisesti tämä kenttä voidaan jättää tyhjäksi, jolloin kaikki määritetyn ensimmäisen pakkauksen jälkeisten pakkausten etiketit tulostetaan uudelleen.
1. Valitse uudelleentulostuksen tulostin.
1. Vahvista tehtävä valitsemalla **OK**.

#### <a name="use-case-24-several-labels-for-boxes-werent-printed-because-of-a-printer-jam-the-last-good-label-has-a-wave-label-id-that-is-printed-as-a-bar-code"></a>Käyttötapaus 2.4: Useita pakkausten etikettejä ei tulostettu tulostimen tukoksen vuoksi. Viimeisessä hyväksyttävässä etiketissä on aallon etiketin tunnus, joka on tulostettu viivakoodina.

1. Kirjaudu varastointisovellukseen varaston *62* käyttäjänä. (Kirjaudu vakioesittelytiedoissa sisään käyttäjätunnuksella *62* ja salasanalla *1*.)
1. Valitse **Lähtevät \> Tulosta etiketit uudelleen (viimeisen mukaan)**.
1. Anna lähetyksen tunnus tai skannaa se.
1. Valitse uudelleentulostusta varten ruutu, jossa on oikea etikettirulla.
1. Anna tai skannaa viimeisen hyväksyttävän aallon etiketin tunnus. Sovellus määrittää sarjan seuraavan etiketin ensimmäiseksi pakkaukseksi, jolle on tulostettava etiketti uudelleen.
1. Anna viimeinen pakkaus, jonka etiketti tulostetaan uudelleen. Vaihtoehtoisesti tämä kenttä voidaan jättää tyhjäksi, jolloin kaikki määritetyn ensimmäisen pakkauksen jälkeisten pakkausten etiketit tulostetaan uudelleen.
1. Valitse uudelleentulostuksen tulostin.
1. Vahvista tehtävä valitsemalla **OK**.

## <a name="scenario-3-short-pick-and-reprint"></a>Skenaario 3: Lyhyt keräily ja uudelleentulostus

Varmista ennen tähän skenaarioon siirtymistä, että seuraavat edellytykset täyttyvät:

- Esittelytiedot on asennettu ja **USMF**-yritys on valittu.
- Aallon etikettitulostus on määritetty ja etikettejä on luotu kohdassa [Aallon etikettitulostuksen määrittäminen](../warehousing/configure-wave-label-printing.md) kuvatulla tavalla.

### <a name="set-up-work-exceptions"></a>Määritä työn poikkeukset

Työn poikkeukset määrittävät lyhyen keräilyn toiminnan. Määritä työn poikkeus seuraavasti:

1. Valitse **Varastonhallinta \> Asetukset \> Työ \> Työn poikkeukset**.
1. Luo tietue, jossa on seuraavat asetukset:

    - **Työn poikkeuksen koodi:** *Lyhyt keräily ja tulostus*
    - **Poikkeuksen tyyppi:** *Lyhyt keräily*
    - **Ehdota aallon etikettien uudelleentulostusta:** *Kyllä*

### <a name="void-and-reprint-after-a-short-pick"></a>Mitätöi ja uudelleentulostus lyhyen keräilyn jälkeen

1. Kirjaudu varastointisovellukseen varaston *62* käyttäjänä. (Kirjaudu vakioesittelytiedoissa sisään käyttäjätunnuksella *62* ja salasanalla *1*.)
1. Avaa sen myyntitilaustyön työn työnkulku, joka luotiin, kun aallon etiketit tulostettiin ensimmäisen kerran.
1. Valitse **Lyhyt keräily**.
1. Valitse tälle skenaariolle luotu työn poikkeuksen koodi.
1. Jos valitsit oikean poikkeuksen, **Mitätöinti ja uudelleentulostus** -valintaruudun pitäisi olla valittavissa. Valitse valitse ruutu ja vahvista. Vahvistetun etikettirullasarjan tunnistaa siitä, että **Etiketin luontitunnus** -kenttä lasketaan uudelleen työrivin muutetun määrän mukaan. Se tulostetaan sitten uudelleen määritetyssä tulostimessa.

## <a name="additional-resources"></a>Lisäresurssit

- [Aallon etiketin tulostus](configure-wave-label-printing.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]