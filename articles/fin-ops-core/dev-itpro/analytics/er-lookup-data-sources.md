---
title: Haun tietolähteiden määrittäminen ER-sovelluskohtaisten parametrien käyttämiseksi
description: Tässä artikkelissa kerrotaan, kuinka voit määrittää hakutietolähteet sähköisen raportoinnin (ER) muodoissa käyttämään ER-sovelluskohtaisia parametreja.
author: kfend
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.custom: ''
ms.assetid: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
ms.openlocfilehash: f3ce5837b1d20860588848a1b518b3d801a05db4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285118"
---
# <a name="configure-lookup-data-sources-to-use-er-application-specific-parameters"></a>Haun tietolähteiden määrittäminen ER-sovelluskohtaisten parametrien käyttämiseksi 

[!include[banner](../includes/banner.md)]

Sovelluskohtaisten [ER-parametrien](general-electronic-reporting.md) avulla voit määrittää ER-muodon tietojen suodattamisen abstraktin sääntöjoukon perusteella. Tämä sääntöjoukko voidaan määrittää käyttämään **Haku**-tyypin ER-muodossa käytettävissä olevaa tietolähdettä. Tämän jälkeen voit määrittää todelliset säännöt ER-komponenttien suunnittelijoiden ulkopuolella käyttämällä käyttöliittymää (UI), joka luodaan automaattisesti vastaavan ER-muodon **haku** tietolähteen asetusten ja nykyisten oikeushenkilötietojen perusteella. Lopulta määritettyjä sääntöjä käytetään ER-muodon **Haku** tietolähde-kentässä, kun ER-muoto suoritetaan.

> [!NOTE]
> Muokkaatavissa ER-muodon konfiguroitujen tietolähteiden avulla voit määrittää, mitä sovellustietoja käytetään reaalisääntöjen määrityksessä.

[ER-toimintojen suunnittelutoiminto](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base) tuo **haku**-tyypin tietolähteen ER-muotoon. Tietolähteen asetukset on määritettävä niin, että ne kuvaavat, miltä abstraktit säännöt näyttävät. Näitä ovat esimerkiksi seuraavat:

   - Tietyn tietotyypin parametrijoukko, jonka arvoa annetaan yksittäisen säännön määrittämiseksi.
   - Tietyn tietotyypin arvotyyppi, jonka yksittäinen sääntö palauttaa, kun sääntöä pidetään muun muassa sopivina.

Voit konfiguroida seuraavantyyppisiä **haku** tietolähteitä sen mukaan, minkä tyyppisen arvon mikä tahansa konfiguroitu sääntö palauttaa:

   - Käytä **Tietomalli\Haku**-tyyppiä, kun mallin valintalista-arvo on palautettava.
   - Käytä **Dynamics 365 Operations\Lookup** -tyyppiä, kun sovelluksen valintalistan arvo tai sovelluksen [laajennettu tietotyypin](../extensibility/extensible-edts.md) arvo on palautettava.
   - Käytä **Muotoile luettelo\Haku**-tyyppiä, kun muodon valintalista-arvo on palautettava.

Seuraavassa kuvassa esitetään, miten muodon valintalista voidaan konfiguroida ER-mallimuodossa.

   ![Muodon valintalistan näyttäminen konfiguroitujen hakutietojen lähteen pohjana.](./media/er-lookup-data-sources-img1.gif)

Seuraavassa kuvassa esitetään muodon komponentit, jotka on konfiguroitu raportoimaan erityyppiset verot luodun raportin eri osassa.

   ![Erilaisten verojen erityyppisten verojen erillisen raportin näyttäminen muotoilun osissa.](./media/er-lookup-data-sources-img2.png)

Seuraavassa kuvassa havainnollistaa, kuinka ER Operations -suunnittelu sallii **muotoile luettelo\haku** -tyypin tietolähteen lisäyksen.  Lisätty tietolähde on määritetty palauttamaan `List of taxation levels`- muodon valintalistan arvo.

   ![Muotoile luettelo\haku-tyypin ER-tietolähteen lisääminen.](./media/er-lookup-data-sources-img3.gif)

Seuraavassa kuvassa havainnollistetaan, miten lisätty tietolähde on konfiguroitu käyttämään mallitietolähteen **Koodi**-kenttää. **Mallin** tietolähteen **Model.Data.Tax**-tietue on määritetty parametriksi jokaista konfiguroitua sääntöä varten.

![Muotoile luettelo\haku-tyypin lisätyn tietolähteen parametrien konfiguroiminen.](./media/er-lookup-data-sources-img4.gif)

Lisätty `Model.Data.Tax`-tietolähde määritetään määrittämään verokoodi jokaiselle konfiguroitulle säännölle käyttämällä **TaxTable**-sovellustaulun tietueita.

   ![Mallin muokkaaminen\haku-tyypin yhden yrityksen hakutietolähteen tarkastelu.](./media/er-lookup-data-sources-img5.gif)

Voit määrittää valitun ER-muodon hakusäännöt käyttämällä käyttöliittymää, joka on automaattisesti kohdistettu konfiguroidun valitun tietolähteen rakenteen kanssa. Tämä käyttöliittymä edellyttää, että jokaiselle säännölle on määritettävä palautusarvo `List of taxation levels`-muodon valintalista-arvoksi sekä verokoodi parametriksi.

   ![Konfiguroidun tietolähteen sääntöjen määrittäminen.](./media/er-lookup-data-sources-img6.gif)

Seuraavassa kuvassa havainnollistetaan, miten **lasketun kenttä** tyypin `Model.Data.Summary.LevelByLookup`-tietolähteen voi konfiguroida niin, että se kutsui määritettyä **haku** tietolähdettä ja antaa tarvittavat parametrit. Voit käsitellä tätä puhelua ajon aikana ER käy läpi määritetyssä järjestyksessä määritettyjen sääntöjen luettelon ja etsii ensimmäisen säännön, joka täyttää määritetyt ehdot. Tässä esimerkissä sääntö, joka sisältää annettua verokoodia vastaavat verokoodit. Näin saadaan selville, mikä sääntö on sopivin ja mikä on sääntöä varten konfiguroitu valintalista-arvo, jonka tämä tietolähde palauttaa.

> [!NOTE]
> Poikkeus ilmenee, jos sovellettavaa sääntöä ei löydy. Voit estää nämä poikkeukset määrittämällä sääntöluettelon lopussa lisää sääntöjä, jotka käsittelevät tapauksia, joissa annetaan ei-konfiguroitu arvo tai arvoa ei ole. Käytä **\*Ei tyhjä**\*- ja **\*Tyhjä**\*-asetuksia vastaavasti.  
>
> ![Määritetyn hakutietolähteen kutsuminen tietolähteen lisäämiseksi.](./media/er-lookup-data-sources-img7.png)

Kun määrität **Yritysten välinen**-asetuksen arvoksi **Kyllä** muokattavalle hakutietolähteelle, lisäät uuden pakollisen **yritys**-parametrin tämän tietolähteen parametrijoukkoon. **Yritys**-parametrin arvo on määritettävä ajon aikana, kun hakutietolähdettä kutsutaan. Kun yrityskoodi määritetään ajon aikana, ohjelma käyttää tälle yritykselle määritettyjä sääntöjä sopivimman säännön etsimisessä ja vastaava arvo palautetaan. Seuraavassa kuvassa kerrotaan, miten tämä voidaan tehdä ja miten muokattavissa olevia tietolähdettä muutetaan.

   ![Mallin muokkaaminen\haku-tyypin yritysten välisen hakutietolähteen tarkastelu.](./media/er-lookup-data-sources-img8.gif)

> [!NOTE]
> Valitse jokainen yritys erikseen, jos haluat määrittää tämän hakutietolähteen sääntöjoukon muokattavassa ER-muodossa. Poikkeus tulee suorituspalvelussa, kun yritystenvälistä hakua kutsutaan sen yrityksen koodilla, jonka hakuasetusta ei ole tehty loppuun.
>
> Varmista, että myönnät käyttöoikeudet käyttäjälle, joka suorittaa ER-muodon yritystenvälisen **haku**-tietolähteen avulla, jotta voit käyttää kaikkien tämän tietolähteen käyttöalueeseen kuuluvien yritysten tietoja. Muussa tapauksessa tuotetaan poikkeus ajon aikana.

Versiosta 10.0.19 alkaen **haku**-tietolähteiden laajennetut toiminnot ovat käytettävissä. Kun määrität muokattavan hakutietolähteen **Laajennettu**-asetuksen arvoksi **Kyllä**, konfiguroitu hakutietolähde muunnetaan rakenteeksi tietolähteeksi, joka tarjoaa lisätoimintoja konfiguroitujen sääntöjoukon analysoimista varten. Seuraavassa kuvassa näkyy tämä muunnos.

   ![Mallin muokkaaminen\haku-tyypin jäsennellyn hakutietolähteen tarkastelu.](./media/er-lookup-data-sources-img9.gif)

- **Haku**-alinimike on suunniteltu toimintoksi, joka löytää sopivimman säännön parametrijoukon perusteella konfiguroitavien sääntöjen joukkoa joukon perusteella.
- **IsLookupResultSet**-alinimike on suunniteltu toimintoksi, joka hyväksyy peruslistatietolähteen määritetyn arvon ja palauttaa *totuusarvon* **Tosi**, kun sääntöjoukko sisältää vähintään yhden säännön, jolle annettu valintalista-arvo on määritetty palautetuksi arvoksi. Tämä toiminto palauttaa *totuusarvon* **Epätosi**, kun ei ole sääntöjä, jotka palauttavat määritetyn valintalista-arvon.
- **Asetus**-alinimikkeen määrittäminen on toiminto, joka palauttaa konfiguroitujen sääntöjen joukon tietueluettelon tietueista. Palautetut arvot ja konfiguroitujen sääntöjen parametrijoukko näkyvät jokaisessa palautetussa tietueessa tietotyyppien kentissä:

    - Palautetut arvot näytetään **Hakutulos**-kentässä.
    - Konfiguroitu parametri esitetään kentissä parametrien niminä (tässä esimerkissä **koodi**-kenttä).

Lisätietoja **haku** tietolähteen konfiguroinnista on kohdassa [ER-muotojen konfiguroiminen käyttämään yritykselle määritettyjä parametreja](er-app-specific-parameters-configure-format.md). Lisätietoja hakusääntöjen määrittämisestä on kohdassa [ER-muodon parametrien määrittämisestä yritystä kohti](er-app-specific-parameters-set-up.md).

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin muotojen määrittäminen käyttämään yrityskohtaisesti määritettyjä parametreja](er-app-specific-parameters-configure-format.md)

[Sähköisen raportoinnin muodon parametrien määrittäminen yrityskohtaisesti](er-app-specific-parameters-set-up.md)
