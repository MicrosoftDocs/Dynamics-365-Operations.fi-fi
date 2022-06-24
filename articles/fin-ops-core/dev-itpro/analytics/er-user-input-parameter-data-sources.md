---
title: USER INPUT PARAMETER -tietolähteiden avulla voit määrittää raportin parametrit.
description: Tässä artikkelissa kerrotaan, miten USER INPUT PARAMETER -tietolähteiden avulla määritetään luotujen raporttien parametreja.
author: NickSelin
ms.date: 04/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Version 10.0.27
ms.openlocfilehash: 62b7a8173416a1d36a2985823d186a7a0e6a7e60
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872969"
---
# <a name="use-user-input-parameter-data-sources-to-specify-parameters-for-a-report"></a>USER INPUT PARAMETER -tietolähteiden avulla voit määrittää raportin parametrit.

[!include[banner](../includes/banner.md)]

Kun suunnittelet [sähköisen raportoinnin](general-electronic-reporting.md) (ER) [mallimääritystä](er-overview-components.md#model-mapping-component) ja [ER-muotoja](er-overview-components.md#format-component) osia, voit käyttää *USER INPUT PARAMETER* -tyypin tietolähteitä niiden arvojen hakemiseen, jotka voidaan määrittää valintaikkunan tietojen syöttökentissä ajon aikana, ennen kuin ER-muodon suorittaminen alkaa. Tässä artikkelissa kuvataan *USER INPUT PARAMETER* -tietolähteitä, joita tuetaan tällä hetkellä.

## <a name="mandatory-properties"></a><a name="mandatory-properties"></a>Pakolliset ominaisuudet

Jokaisen *USER INPUT PARAMETER* -tyypin tietolähteille on määritettävä seuraavat ominaisuudet:

- Syötä **Nimi**-kenttään tietolähteen sisäinen nimi. Voit käyttää tätä nimeä muissa konfiguroitujen mallimääritysten tai muotokomponentin [lausekkeissa](er-formula-language.md) ja sidonnoissa.

## <a name="optional-properties"></a><a name="optional-properties"></a>Valinnaiset ominaisuudet

Jokaisen *USER INPUT PARAMETER* -tyypin tietolähteille voidaan valinnaisesti määrittää seuraavat ominaisuudet:

- Määritä **Otsikko**-kenttään otsikko, jota käytetään liittyvien tietojen syöttökentässä valintaikkunassa ajon aikana. Voit lisätä eri kielikoodeille eri otsikkotekstin aktivoimalla **Otsikko**-kentän ja valitsemalla **Käännä**.
- Määritä **Ohje**-kentässä **Muodon suunnittelu** -sivun tai **Mallin määrityksen suunnittelu** -sivun alaosassa suunnittelun aikana näkyvä ohjeteksti, kun *USER INPUT PARAMETER* -tyypin muokattava tietolähde valitaan. Tämä teksti saattaa sisältää lisätietoja tietolähteestä, jotta käyttäjät voivat konfiguroida muokattavissa olevaa muotoa tai mallimäärityskomponenttia. Voit lisätä eri kielikoodeille eri ohjetekstin valitsemalla **Käännä**.

    > [!NOTE]
    > **Käännä**-painike , jonka avulla voit lisätä [kielikohtaisia otsikoita ja tekstiä](er-design-multilingual-reports.md#format-component), on käytettävissä vasta kun olet, lisännyt tietolähteen, tallentanut muutokset ja avannut sitten tietolähteen uudelleen muokkausta varten.

- Määritä **Vain luku** - kentässä lauseke, joka palauttaa *[Boolean](er-formula-supported-data-types-primitive.md#boolean)*-arvon.

    - Jos konfiguroitu lauseke palauttaa arvon **Tosi** ajon aikana, liittyvä tietojen syöttökenttä näkyy himmennettynä valintaikkunassa etkä voi muuttaa sen arvoa.
    - Jos konfiguroitu lauseke palauttaa arvon **Epätosi** ajon aikana tai jos lauseketta ei ole määritetty, liittyvä tietojen syöttökenttä on käytettävissä valintaikkunassa ja voit muuttaa sen arvoa.

- Määritä **Oletusarvo**-kentässä lauseke, joka palauttaa viitatun parametrityypin arvon. Tämän arvon avulla voidaan täyttää valintaikkunan liittyvän tietosyöttökentän oletusarvo ajon aikana.

    Kun suoritat ER-muodon, liittyvään tietosyöttökenttään suorituksen aikana syötetyt arvot tallennetaan muistiin aiemmin käytettynä arvona. Aiemmin käytetyt arvot tallennetaan yksitellen kutakin kenttää, suoritettava ER-muotoa, nykyistä käyttäjää ja nykyistä organisaatiota (yritystä) varten.

    - Määritä **Palauta aina oletusarvo**-kentän arvoksi **Kyllä**, jos **Oletusarvo**-lausekkeen palauttamaa arvoa käytetään aina oletusarvona aiemmin käytetystä arvosta riippumatta.
    - Määritä **Palauta aina oletusarvo**-kentän arvoksi **Ei**, jos **Oletusarvo**-lausekkeen palauttamaa arvoa pitäisi käyttää oletusarvona vain, kun aiemmin käytetty arvo puuttuu.

    > [!NOTE]
    > Jos määrität **Palauta aina oletusarvo** -asetukseksi **Kyllä**, lauseke on määritettävä **Oletusarvo**-kentässä.

- Jos määrität **Salli monivalinta** -asetukseksi **Kyllä**, voit valita konfiguroidulle parametrille useita arvoja ajon aikana. Jos määrität arvoksi **Ei**, voit valita vain yhden arvon.

    > [!NOTE]
    > Tämä vaihtoehto ei koske kaikkia *USER INPUT PARAMETER* -tyyppejä. Suunnittelun aikana heitetään poikkeus, joka ilmoittaa käyttäjälle, että konfiguroitu käyttäjän syöteparametri ei tue monivalintaa ja että vain yksi arvo voidaan valita tai syöttää.
    >
    > Jos Määrität **Salli monivalinta** -asetuksen arvoksi **Kyllä** ja olet määrittänyt lausekkeen **Oletusarvo**-kenttään, lausekkeen avulla voidaan määrittää vain yksi oletusarvo.

- Valitse **Muokkaa näkyvyyttä** -vaihtoehto määrittääksesi, näytetäänkö konfiguroitu parametri valintaikkunassa ajon aikana.

    > [!NOTE]
    > *USER INPUT PARAMETER* -tyypin tietolähteiden oletusnäkyvyys määräytyy sen ER-komponentin mukaan, joka sisältää ne.
    >
    > - Jos tietolähde on määritetty muotokomponentissa, se on oletusarvoisesti näkyvissä.
    > - Jos tietolähde on konfiguroitu mallimäärityskomponentissa, se näkyy vain, jos tietolähteen arvo vaikuttaa tulokseen, kun ER-komponentti suoritetaan. Olet esimerkiksi lisännyt tietolähteen, mutta et ole käyttänyt sitä nykyisen mallimäärityskomponentin lausekkeissa ja sidonnoissa. Tällöin oletusarvon mukaan asianmukainen tietojen syöttökenttä ei näy valintaikkunassa ajon aikana. 

    Määritä **Kaavan suunnittelu** -sivun **Kaava**-kenttään lauseke, joka palauttaa *totuusarvon*

    - Jos konfiguroitu lauseke palauttaa arvon **Tosi** ajon aikana tai jos lauseketta ei ole määritetty, liittyvä tietojen syöttökenttä on näkyvissä valintaikkunassa ajon aikana.
    - Jos konfiguroitu lauseke palauttaa arvon **Epätosi**, liittyvien tietosyöttökenttä piilotetaan valintaikkunassa ajon aikana. Kun muut lausekkeet kutsuvat sitä ajon aikana, se palauttaa oletusarvon, aiemmin käytetyn arvon tai nykyisen tietotyyppiarvon oletusarvon muiden asetusten mukaan.

## <a name="type-specific-properties"></a>Tyyppikohtaiset ominaisuudet

### <a name="application-dependent-user-input-parameter"></a>Sovelluksesta riippuvainen käyttäjän syöteparametri

Käytä **Yleiset** \> **User input parameter** -tyypin tietolähdettä, kun haluat hakea Microsoft Dynamics 365 Finance -sovelluksen nykyiselle esiintymälle määritetyn tietotyypin pakolliset arvot.. Kun lisäät tämäntyyppisen tietolähteen ER-komponenttiin, määritä seuraavat ominaisuudet:

- Valitse **Operations-tietotyypin nimi (EDT, valintalista)** -kentästä sovelluksen [laajennettu tietotyyppi (EDT)](../extensibility/extensible-edts.md) tai sovelluksen valintalista.

> [!NOTE]
> On suositeltavaa tarkistaa lausekkeet, jotka on konfiguroitu **Vain luku** - ja **Oletusarvo**-kentissä, kun muutat **Operations-tietotyypin nimi (EDT, valintalista)** -viitettä muokattavassa tietolähteessä, jonka on tätä *USER INPUT PARAMETER* -tyyppiä.

Seuraavassa kuvassa esitetään **Instat XML (DE)** -ER-muotomäärityksessä määritetyn `$TaxRegNum`-tietolähteen ominaisuudet. Tämä tietolähde on määritetty niin, että se tarjoaa *Kuvaus*-EDT-kohteen avulla **Verorekisteröintinumero**-tietokentän valintaikkunassa ajon aikana.

![USER INPUT PARAMETER -tyypin tietolähteen ominaisuudet, jotka ovat Muodon suunnittelu -sivun valintaikkunassa.](./media/er-user-input-parameter-data-sources-01.png)

Seuraavassa kuvassa näkyy valintaikkuna, joka näkyy ajon aikana, kun **Instat XML (DE)** -ER-muotokonfiguraatio suoritetaan Intrastat-ilmoituksen [luontia](../../../finance/localizations/tasks/eur-00002-eu-intrastat-declaration.md) varten. Huomaa, että määritetty **Verorekisteröintinumero**-kenttä on käytettävissä tietojen syöttöä varten.

![Suoritettavan ER-muodon Intrastat-raporttivalintaikkuna Intrastat-sivulla.](./media/er-user-input-parameter-data-sources-02.png)

### <a name="data-model-enumeration-user-input-parameter"></a>Tietomallin luetteloinnin käyttäjän syöttöparametri

Hae yksittäisen tietomallin [valintalistan](er-formula-supported-data-types-primitive.md#enumeration) arvo(t) käyttämällä **Tietomalli** \> **Luetteloinnin käyttäjän syöttöparametri** -tyypin tietolähdettä. Kun lisäät tämäntyyppisen tietolähteen ER-komponenttiin, määritä seuraavat ominaisuudet:

- Määritä **Malli**-kenttään viittaus perustietomalliin.
- Määritä **Mallin valintalista** -kentässä viittaus viitatun tietomallin valintalistaan.
- Valitse **Versio**-kentästä sen ER-tietomallikomponentin tarkistusversionumero, joka sisältää viitatun mallin valintalistan.

    > [!TIP]
    > Suunnittelun aikana voit jättää **Versio**-kentän tyhjäksi, jos haluat käyttää viitatun tietomallikomponentin valintalistaluetteloa, joka sijaitsee vastaavan ER-tietomallin konfiguraation luonnosversiossa. Näin voit samalla muokata mallimäärityksen tai muotokomponentin luonnosversiota ja perustietomallin komponentin luonnosversiota.
    >
    > Huomaa kuitenkin, että **Versio**-kentän voi jättää tyhjäksi vain mallimäärityksen tai muotokomponentin luonnosversiossa. Kun muutat ER-mallimäärityksen tai muotomäärityksen tilan **Luonnos**-tilasta **Valmis**-tilaksi, tähän kenttään täytetään automaattisesti nykyisen Finance-instanssin suurin käytettävissä oleva mallin versionumero. Jos otat käyttöön perustietomallin luonnosversiossa uuden valintalistan tai valintalista-arvon ja viittaat siihen muokattavassa mallimäärityksessä tai muotokomponentissa, täydennä se perustietomallin konfiguraation luonnosversio ennen ER-mallimäärityksen tai muodon konfiguraation luonnosversion viimeistelyä. Muussa tapauksessa poikkeus "Polkua ei löydy" tulee, kun muutat mallimäärityksen tai muotomäärityksen tilan **Luonnos**-tilasta **Valmis**-tilaksi. Sanoma ilmoittaa, että viitattu valintalista tai valintalista-arvo puuttuu perustietomallista.

Seuraavassa kuvassa esitetään **Instat XML (DE) Contoso** -ER-muotomäärityksessä määritetyn `$ReportDirection`-tietolähteen ominaisuudet. **Instat XML (DE) Contoso** -määritys on [johdettu](general-electronic-reporting.md#Configuration) **Instat XML (DE)** -määrityksestä. Tämä tietolähde on määritetty niin, että se tarjoaa *ReportDirection*-mallivalintalistan avulla soveltuvan valintakentän valintaikkunassa ajon aikana.

![USER INPUT PARAMETER -tyypin tietolähteen ominaisuudet, jotka ovat Muodon suunnittelu -sivun valintaikkunassa.](./media/er-user-input-parameter-data-sources-03.png)

### <a name="format-enumeration-user-input-parameter"></a>Muodon luetteloinnin käyttäjän syöttöparametri

Hae yksittäisen muodon valintalistan arvo(t) käyttämällä **Muodon valintalista** \> **Luetteloinnin käyttäjän syöttöparametri** -tyypin tietolähdettä. Kun lisäät tämäntyyppisen tietolähteen ER-komponenttiin, määritä seuraavat ominaisuudet:

- Määritä **Muodon valintalista** -kenttään muokattavan muodon valintalista.

> [!NOTE]
> Tämän tyyppiset tietolähteet voidaan konfiguroida vain muokattavan muotokomponentin käyttöalueessa.

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin kaavojen suunnittelutoiminto](general-electronic-reporting-formula-designer.md)

[Tietolähdearvojen käynnistäminen lähdekoodin USER INPUT PARAMETER -tyypistä](er-initiate-uip-data-source-value-from-source-code.md)
