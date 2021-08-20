---
title: Siirtotilausten luominen varastosovelluksessa
description: Tässä ohjeaiheessa käsitellään siirtotilausten luontia ja käsittelyä varastonhallinnan mobiilisovelluksessa
author: perlynne
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 986abfaef81474571de7db179253c4d76f65d4bec180fa9f355f3218ddbb96ba
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746816"
---
# <a name="create-transfer-orders-from-the-warehouse-app"></a>Siirtotilausten luominen varastosovelluksesta

[!include [banner](../includes/banner.md)]

Varastotyöntekijät voivat luoda ja käsitellä tällä ominaisuudella siirtotilauksia suoraan varastonhallinnan mobiilisovelluksessa. Työntekijä aloittaa valitsemalla kohdevaraston. Tämän jälkeen lisäävät rekisterikilvet siirtotilaukseen lukemalla vähintään yhden rekisterikilven. Kun varastotyöntekijä valitsee **Suorita tilaus**, erätyö luo tarvittavan siirtotilauksen ja tarvittavat tilausrivit kyseisille rekisterikilville rekisteröidyn käytettävissä olevan varaston perusteella.

## <a name="enable-the-create-transfer-orders-from-the-warehouse-app-feature"></a><a name="enable-create-transfer-order-from-warehouse-app"></a>Siirtotilausten luonnin ottaminen käyttöön varastosovellustoiminnossa

Ennen kuin tätä toimintoa voidaan käyttää, se on otettava edellytyksineen käyttöön järjestelmässä. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sivua ja tarkistaa toiminnon tilan sekä ottaa sen käyttöön tarvittaessa.

1. Ota ensimmäiseksi käyttöön [Käsittele varastosovelluksen tapahtumat](warehouse-app-events.md) -toiminto, joka näkyy [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) seuraavasti:
    - **Moduuli** - Varastonhallinta
    - **Toiminnon nimi** – Käsittele varastosovelluksen tapahtumia
1. Ota seuraavaksi käyttöön *Luo siirtotilauksia varastosovelluksessa* -ominaisuus, joka näkyy seuraavasti:
    - **Moduuli** - Varastonhallinta
    - **Ominaisuuden nimi** – Luo ja käsittele siirtotilauksia varastosovelluksessa
1. Jos lähtevien lähetysten käsittely halutaan automatisoida, myös [Vahvista lähtevät lähetykset erätöissä](confirm-outbound-shipments-from-batch-jobs.md) -ominaisuus on otettava käyttöön. Tämä ominaisuus näkyy seuraavasti:
    - **Moduuli** - Varastonhallinta
    - **Ominaisuuden nimi** – Vahvista lähtevät lähetykset erätöissä

## <a name="set-up-a-mobile-device-menu-item-to-create-transfer-orders"></a><a name="setup-warehouse-app-menu"></a>Mobiililaitteen valikkokohteen määrittäminen luomaan siirtotilauksia

Seuraavaksi käsitellään yleisiä ohjeita mobiililaitteen siirtotilauksen luontiin käytettävän valikkokohteen määrittämisestä. Liiketoimintatarpeet määrittävät, millainen automaatiotaso määritetään, kun käyttäjät luovat siirtotilauksia varastossa, ja niiden mukaan otetaan käyttöön erilaisia määrityksiä. Tässä asiakirjassa on skenaario, jossa käsitellään yhtä näistä määrityksistä.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.
1. Lisää uusi valikkokohde valitsemalla **Uusi**. Voit aloittaa, kun olet määrittänyt seuraavat asetukset:

    - **Valikon vaihtoehdon nimi** – anna nimi siinä muodossa, kun sen halutaan näkyvän Supply Chain Managementissa.
    - **Otsikko** - anna valikkovaihtoehdon nimi siinä muodossa, kun työntekijät näkevät sen varastonhallinnan mobiilisovelluksessa.
    - **Tila** – määritä tilaksi *Epäsuora* (tämä valikkokohde ei luo työtä).
    - **Tehtäväkoodi** – Määritä asetukseksi *Luo siirtotilaus rekisterikilvistä*, jolloin varastotyöntekijät voivat luoda siirtotilauksen vähintään yhden skannatun rekisterikilven perusteella.

1. Määritä **Siirtotilauksen rivin luontikäytäntö** -asetuksen avulla, miten tämä valikkovaihtoehto luo siirtotilauksen rivejä. Rivit luodaan tai päivitetään skannatuille rekisterikilville rekisteröidyn käyttävissä olevan varaston perusteella. Valitse jokin seuraavista arvoista:

    - **Ei varausta** – siirtotilauksen rivejä ei varata.
    - **Rekisterikilpiopastus rivivarauksessa** – Siirtotilauksen rivit varataan ja niissä käytetään rekisterikilpiopastuksen strategiaa tallentamaan tilausriveihin liittyvät rekisterikilpitunnukset. Niinpä paikannettuja rekisterikilpitunnuksen arvoja voidaan käyttää siirtotilausrivien työnluontiprosessin osana.

1. Voit lisätä **Lähtevien lähetyskäytäntö** -asetuksella tarvittaessa enemmän automaatiota lähtevien siirtotilausten lähetysprosessiin. Kun työntekijä valitsee **Suorita tilaus** -painikkeen, sovellus luo *Suorita tilaus* -varastosovellustapahtuman, joka tallentaa tässä valitun arvon **Lähtevien lähetyskäytäntö** -kenttään jokaisella valittuna olevan siirtotilauksen rivillä. Kun erätyö myöhemmin luo siirtotilauksen käsittelemällä tapahtumajonon, erätyö voi lukea tähän kenttään tallennetun arvon ja voi siten hallita, miten työ käsittelee kunkin rivin. Valitse yksi seuraavista:

    - **Ei mitään** – prosessia ei automatisoida lainkaan.
    - **Vapauta varastoon** – automatisoi varastoon vapautusprosessin.
    - **Lähetyksen vahvistus** – automatisoi lähetyksen vahvistusprosessin.
    - **Vapautus ja lähetyksen vahvistus** – automatisoi sekä varastoon vapautus- että lähetyksen vahvistusprosessit.

## <a name="add-the-mobile-device-menu-item-to-a-menu"></a>Mobiililaitteen valikkovaihtoehdon lisääminen valikkoon

1. Valitse **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikko**.
1. Valitse **Muokkaa**.
1. Valitse ensin aiemmin luotu valikko ja sitten uusi valikkovaihtoehto **Käytettävissä olevat valikot ja valikkovaihtoehdot** -kohdassa. Lisää valikkovaihtoehto valitsemalla oikea nuolipainike.

## <a name="create-a-transfer-order-based-on-license-plates"></a>Rekisterikilpiin perustuvan siirtotilauksen luominen

Varastonhallinnan mobiilisovelluksessa on yksinkertainen prosessi rekisterikilpiin perustuvien siirtotilausten luomiseen. Työntekijä luo siirtotilauksen toimimalla seuraavasti varastonhallinnan mobiilisovelluksessa:

1. Luo siirtotilaus ja määritä kohdevarasto.
1. Määritä jokainen lähetettävä rekisterikilpi.
1. Valitse **Suorita tilaus**.

>[!NOTE]
> Useat työntekijät voivat määrittää samaan siirtotilaukseen tarkoitettuja rekisterikilpiä valitsemalla **Valitse siirtotilaus** -painikkeella varastosovelluksen tapahtumajonossa aiemmin luodun, käsittelemättömän siirtotilausnumeron. Lisätietoja siirtotilauksen numeroarvojen etsimisestä on kohdassa [Varastosovellustapahtumien kysely](#inquire-the-warehouse-app-events).

## <a name="example-scenario"></a>Esimerkkiskenaario

Tämä skenaario on yleiskatsaus siirtotilausten luontiprosessiin ja automatisoituun käsittelyyn valittuihin rekisterikilpiin rekisteröidyn käytettävissä olevan varaston perusteella.

Eteneminen tässä skenaariossa käyttämällä ehdotettuja arvoja edellyttää asennettujen esittelytietojen käsittelyä ja *USMF*-yrityksen valintaa ennen aloittamista.

Tässä skenaariossa oletetaan, että [Luo ja käsittele siirtotilauksia varastosovelluksessa -ominaisuus](#enable-create-transfer-order-from-warehouse-app) ja [varastosovelluksen tapahtumakäsittely](warehouse-app-events.md) on otettu käyttöön.

Sen lisäksi, että siirtotilauksen luonnin mobiililaitteen valikkovaihtoehdot on määritetty, myös lisämallit, sijaintidirektiivit ja erätyöt on määritettävä ja otettava käyttöön.

### <a name="example-scenario-blueprint"></a>Esimerkkiskenaarion sisältö

Käyttäjä on vähittäismyyjä, jolla on useita rekisterikilpiä. Kukin rekisterikilpi sisältää nimikevalikoiman, joka on sijoitettu tiettyyn paikkaan yhdessä varastossa (*Varasto 51*). Käyttäjä haluaa ottaa käyttöön prosessin, jolla työntekijät voivat luoda siirtotilauksen toiseen varastoon (*Varasto 61*) skannattua rekisterikilpikokoelmaa varten. Siirtotilauksen lähetys ja päivitys tapahtuu automaattisesti heti, kun tilauksen viimeinen rekisterikilpi on määritetty.

![Esimerkki automatisoidusta siirtotilausprosessista.](media/create-transfer-order-from-app-example.png "Esimerkki automatisoidusta siirtotilausprosessista")

### <a name="create-a-mobile-device-menu-item-for-creating-transfer-orders"></a>Mobiililaitteen valikkokohteen luominen siirtotilausten luontia varten

Tässä osassa käsitellään uuden mobiililaitteen valikkovaihtoehdon luomista siirtotilausten luontia varten. Määritä **Tila**-asetukseksi *Epäsuora* ja **Tehtäväkoodi**-asetukseksi *Luo siirtotilaus rekisterikilvistä*.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.
1. Valitse **Uusi**.
1. Anna **Valikkovaihtoehdon nimi** -kentässä nimeksi *Luo ST*.
1. Anna **Otsikko**-kentässä kuvaus *Luo ST*.
1. Valitse **Tila**-kentässä *Epäsuora*.
1. Valitse **Tehtäväkoodi**-asetukseksi *Luo siirtotilaus rekisterikilvistä*.
1. Valitse **Tilausrivin luontikäytäntö** -asetukseksi *Rekisterikilpiopastus rivivarauksessa*.
1. Vallitse **Lähtevien lähetyskäytäntö** -asetukseksi *Vapautus ja lähetyksen vahvistus*.
1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikko**.
1. Valitse **Muokkaa**.
1. Valitse aiemmin luotu **Varasto**-valikko ja valitse sitten uusi valikkovaihtoehto **Käytettävissä olevat valikot ja valikkovaihtoehdot** -kohdassa. Lisää valikkovaihtoehto **Varasto**-valikkoon valitsemalla oikea nuolipainike.

### <a name="set-up-work-templates-to-auto-process-and-break-work-by-located-license-plate"></a>Työmallien määrittäminen käsittelemään ja keskeyttämään työ automaattisesti paikannetun rekisterikilven perusteella

Tässä osassa käsitellään työmallin ottamista käyttöön siten, että se käsittelee automaattisesti mallin luoman työn sen jälkeen, kun aalto vapautetaan.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työmallit**.
1. Valitse **Työtilaustyyppi**-kentässä *Siirtovarasto-otto*.
1. Luo uusi työmalli valitsemalla **Uusi**.
1. Kirjoita **Työmalli**-kenttään *51 RK-automaattikäsittely*.
1. Kirjoita **Työmallin kuvaus** -kenttään *51 RK-automaattikäsittely*.
1. Valitse **Käsittele automaattisesti** -valintaruutu. Automaattivaiheiden käsittely edellyttää, että tämä asetus on valittu.
1. Esittelytiedoissa on jo työmalli *51 Siirto*. Muokkaa **Järjestysnumero**-kenttää siten, että uuden työmallin järjestysnumero on pienempi kuin valmiin *51 Siirto* -työmallin järjestysnumero.
1. Ota **Työmallin tiedot** -pikavälilehti käyttöön valitsemalla työkalurivillä **Tallenna**.
1. Valitse **Työmallin tiedot** -pikavälilehden työkalurivillä **Uusi**. Kaksi riviä lisätään.
1. Valitse **Työtyyppi**-kentässä *Keräilyt*.
1. Valitse **Työluokan tunnus** -kentässä *TransfOut*.
1. Valitse **Työmallin tiedot** -työkalurivillä **Uusi**.
1. Valitse **Työtyyppi**-kentässä *Määritä*.
1. Valitse **Työluokan tunnus** -kentässä *TransfOut*.
1. Ota **Direktiivikoodi** käyttöön valitsemalla **Tallenna**.
1. Valitse **Työtyyppi**-kohdan *Määritä*-rivillä **Direktiivikoodi** *Lastausovi*. Varmista, että uuden työmallin **järjestysnumero** on pienin.
1. Avaa kyselyeditori valitsemalla työkalurivillä **Muokkaa kyselyä**.
1. Valitse **Alue**-välilehdessä **Lisää**.
1. Valitse lisätyn rivin **Kenttä**-kohdassa *Varasto*.
1. Valitse **Ehdot**-kentässä *51*.
1. Valitse **Lajittelu**-välilehti.
1. Valitse **Lisää** ja määritä **Kenttä**-asetukseksi *Paikannettu rekisterikilven tunnus*. Tämän kentän määrittäminen ottaa käyttöön työkalurivin **Työn otsikoiden katkaisut** -painikkeen.
1. Valitsemalla **OK** ja sitten **Kyllä** voit palauttaa ryhmittelyn ja palata **Työmallit**-sivulle.
1. Valitse **Työn otsikoiden katkaisu**, ota käyttöön **Ryhmittele tämän kentän mukaan** **Paikannettu rekisterikilven tunnus** -asetuksena ja sulje.

> [!NOTE]
> Kaikkia asetuksia ei voida käsitellä automaattisesti. Sellaisia ovat esimerkiksi todellisen painon vaihtoehdot ja seurantadimensioyhdistelmän käyttäminen.

### <a name="set-up-location-directives-for-the-license-plate-guided-strategy"></a>Rekisterikilpiopastetun strategian sijaintidirektiivien määrittäminen

Tässä osassa käsitellään sijaintidirektiivien poimintaprosessin määrittämistä käyttämään **Rekisterikilpiopastus**-strategiaa.

1. Valitse **Varastonhallinta \> Asetukset \> Sijaintidirektiivit**.
1. Valitse **Muokkaa**.
1. Valitse siirtymisluettelon otsikossa **Työtilaustyyppi**-kohdassa *Siirtovarasto-otto*.
1. Valitse siirtymisluettelossa aiemmin luotu sijaintidirektiivi **51 ST poiminta**.
1. Valitse **Rivit**-pikavälilehdessä **Salli jakaminen** -valintaruutu.
1. Lisää uusi toimintorivi valitsemalla **Sijaintidirektiivin toiminnot** -pikavälilehdessä **Uusi**.
1. Kirjoita **Nimi**-kenttään *RK-opastus*.
1. Valitse **Strategia**-kentässä *Rekisterikilpiopastus*. Tällä toiminnolla on oltava pienin järjestysnumero.
1. Valitse työkalurivillä **Tallenna**.
1. Valitse työkalurivillä **Päivitä**-sivukuvake.
1. Valitse **Sijaintidirektiivin toiminnot** -pikavälilehdessä rivi *ST poiminta*.
1. Muuta järjestysnumero suuremmaksi kuin juuri luodun *RK-opastus*-toiminnon järjestysnumero valitsemalla **Sijaintidirektiivin toiminnot** -työkalurivillä **Siirrä alas**.

> [!NOTE]
> Rekisterikilpiopastus-strategia yrittää varata ja luoda poimintatöitä sijainneissa, joissa on pyydettyjä siirtotilausriveihin liitettyjä rekisterikilpiä. Mutta jos tämä ei ole mahdollista ja haluat silti luoda poimintatyön, ota käyttöön toinen sijaintidirektiivin toimintastrategia. Vaihtoehtoisesti voi myös hakea varastoa muualta fyysisessä varastossa. Toimintatavan valinta määräytyy liiketoimintaprosessin tarpeiden mukaan.

### <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Erätyön määrittäminen käsittelemään varastosovelluksen tapahtumia

Tässä osassa käsitellään aikataulutetun erätyön määrittämistä käsittelemään varastosovellustapahtumia.

1. Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Käsittele varastosovelluksen tapahtumat**.
2. Ota **Eräkäsittely** käyttöön valintaikkunan **Suorita taustalla** -kohdassa.
3. Valitse **Toistuminen** ja määritä erätyön käsitteleminen liiketoiminnassa tarvittavan aikavälin perusteella.
4. Palaa pääikkunaan valitsemalla **OK**.
5. Lisää työ eräjonoon valitsemalla **OK** pääikkunassa.

### <a name="set-up-a-batch-job-to-release-transfer-orders-automatically"></a>Erätyön määrittäminen vapauttamaan siirtotilaukset automaattisesti

Tässä osassa käsitellään aikataulutetun erätyön määrittämistä vapauttamaan siirtotilaukset, joissa on Valmis vapautettavaksi -merkintä.

1. Valitse **Varastonhallinta \> Vapauta varastoon \> Siirtotilausten automaattinen vapautus**.
1. Laajenna valintaikkunassa **Sisällytettävät tietuet** -osa.
1. Valitse **Suodatus** **Sisällytettävät tietueet** -osassa.
1. Lisää kyselyyn uusi rivi valitsemalla **WHSTransferAutoRTWQuery**-kyselysivun **Alue**-välilehdessä **Lisää**.
1. Valitse uuden rivin **Taulukko**-kentässä avattava valikko ja valitse taulukko **Varastoon vapautettava siirtorivi**.
1. Valitse avattavassa **Kenttä**-valikossa **Lähtevien lähetyskäytäntö**.
1. Vallitse **Ehdot** -kentässä **Vapautus ja lähetyksen vahvistus**.
1. Valitse rivin, jonka **Kenttä**-asetuksena on *Varastosta*, **Ehdot**-kentässä *51*.
1. Palaa pääikkunaan valitsemalla **OK**.
1. Määritä eräkäsittely laajentamalla **Suorita taustalla** -osa.
1. Ota **Eräkäsittely** käyttöön **Suorita taustalla** -kohdassa.
1. Valitse **Toistuminen** ja määritä erätyön käsitteleminen liiketoiminnassa tarvittavan aikavälin perusteella.
1. Palaa pääikkunaan valitsemalla **OK**.
1. Lisää erätyö eräjonoon valitsemalla pääikkunassa **OK**.

### <a name="set-up-the-process-outbound-shipment-batch-job"></a>Käsittele lähtevät lähetykset -erätyön määrittäminen

Tässä osassa käsitellään aikataulutetun erätyön määrittämistä suorittamaan lähtevän lähetyksen vahvistus kuormissa, jotka ovat valmiita lähettäviksi ja jotka liittyvät lähetysvalmiisiin siirtotilausriveihin.

1. Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Käsittele lähtevät lähetykset**.
1. Laajenna **Sisällytettävät tietueet** -osa.
1. Valitse **Suodata**.
1. Valitse **Liitokset**-välilehti **WHSLoadShipConfirm**-kyselyssä.
1. Laajenna taulukkohiearkia siten, että **Kuormat** ja **Kuorman tiedot** laajentuvat.
1. Valitse **Kuorman tiedot** -taulukko.
1. Valitse **Lisää taulukon liitos** -painike.
1. Siirry suodattamalla tai hakemalla taulukkoluettelon **Suhde**-sarakkeessa *Siirtotilausrivit (viite)* -kohtaan.
1. Siirrä kohdistus luettelossa taulukkosuhteeseen ja paina **Valitse**-painiketta.
1. Valitse **Siirtotilausrivit**-taulukko.
1. Valitse **Lisää taulukon liitos** -painike.
1. Siirry suodattamalla tai hakemalla taulukkoluettelon **Suhde**-sarakkeessa *Varaston siirron lisäkentät (tietuetunnus)* -kohtaan.
1. Siirrä kohdistus luettelossa taulukkosuhteeseen ja paina **Valitse**-painiketta.
1. Valitse **Alue**-välilehti.
1. **Alue**-kyselytaulukoissa voidaan määrittää kolme kyselyehtoaluetta. Lisää rivi valitsemalla **Lisää**-painike.
1. Lisää alue taulukon **Kuormat**-kohtaan. Määritä **Kenttä**-asetukseksi *Kuorman tila* ja **Ehdot**-asetukseksi *Ladattu*.
1. Lisää toinen alue taulukon **Varaston siirron lisäkentät** -kohtaan. Määritä **Kenttä**-asetukseksi *Lähtevien lähetyskäytäntö* ja **Ehdot**-asetukseksi *Vapautus ja lähetyksen vahvistus*.
1. Lisää toinen alue taulukon **Kuorman tiedot** -kohtaan. Määritä **Kenttä**-asetukseksi *Viite* ja **Ehdot**-asetukseksi *Siirtotilauksen lähetys*.
1. Palaa pääikkunaan valitsemalla **OK**.
1. Laajenna **Suorita taustalla** -osa.
1. Ota **Eräkäsittely** käyttöön.
1. Valitse **Toistuminen** ja määritä erätyön käsitteleminen liiketoiminnassa tarvittavan aikavälin perusteella.
1. Palaa pääikkunaan valitsemalla **OK**.
1. Lisää erätyö eräjonoon valitsemalla pääikkunassa **OK**.

> [!NOTE]
> Lisätietoja on kohdassa [Lähtevien lähetysten vahvistaminen erätöistä](confirm-outbound-shipments-from-batch-jobs.md).

## <a name="processing-the-example-for-create-transfer-order-from-the-warehouse-app"></a>Käsittelyesimerkki Luo siirtotilauksia varastosovelluksessa -toiminnossa

### <a name="add-on-hand-on-a-license-plate"></a>Rekisterikilven käytettävissä olevan varaston lisääminen

Tämän skenaariossa alussa on oltava rekisterikilpi, joka sisältää fyysisen käytettävissä olevan varaston.

| Nimike | Varasto | Varaston tila | Toimipaikka | Rekisterikilpi | Määrä |
| --- | --- | --- | --- | --- | --- |
| A0001 | 51 | Saatavilla | RK-010 | RK10 | 1 |
| A0002 | 51 | Saatavilla | RK-010 | RK10 | 2 |

Lisää fyysisen käytettävissä olevan varaston määrätä käyttämällä seuraavia arvoja:

> [!NOTE]
> Tätä varten on luotava rekisterikilpi ja käytettävissä sijainnissa on voitava käyttää yhdistettyjä nimikkeitä, kuten RK-010.

### <a name="create-and-process-transfer-orders-from-the-warehouse-app"></a>Luo ja käsittele siirtotilauksia varastosovelluksesta

1. Avaa sovellus ja kirjaudu sisään käyttäjänä *51*. Nykyisen käyttäjän varasto on 51.
1. Valitse valikkovaihtoehto **Luo ST** siitä valikkosijainnista, johon vaihtoehto lisättiin määrityksiä tehtäessä.
1. Aloita siirtotilauksen luonti antamalla kohdevarasto (Varastoon) **Varasto**-kentässä *61*. Uusi siirtotilaus kulkee nykyisestä varastosta 51 (Varastosta) kohdevarastoon *61*.
1. Valitse **OK**.
1. Lue **Rekisterikilpi**-kentässä rekisterikilven tunnus. Anna aiemmassa vaiheessa lisätyn varaston rekisterikilpi *RK10*.
1. Valitse **OK**.
1. Viimeistele varastosovelluksen siirtotilauksen luonti valitsemalla ensin valikkopainike ja sitten **Suorita tilaus**.

Tässä esimerkissä käytetään kahta **varastosovellustapahtumaa** (*Luo siirtotilaus* ja *Suorita siirtotilaus*).

### <a name="inquire-the-warehouse-app-events"></a><a name="#inquire-the-warehouse-app-events"></a>Varastosovellustapahtumien kysely

Voit näyttää varastonhallinnan mobiilisovelluksen luoman tapahtumajonon ja tapahtumasanomat valitsemalla **Varastonhallinta \> Kyselyt ja raportit \> Mobiililaitteen lokit \> Varastosovelluksen tapahtumat**.

*Luo siirtotilaus* -tapahtuman sanomille annetaan *Odottaa*-tila, jolloin **Käsittele varastosovelluksen tapahtumat** -erätyö ei poimi ja käsittele tapahtumasanomia. Erätyö käsittelee tapahtumat heti, kun tapahtumasanaoman tilaksi päivitetään *Asetettu jonoon*. Tämä tapahtuu samanaikaisesti *Suorita siirtotilaus* -tapahtuman luonnin kanssa. (Työntekijä valitsee silloin **Suorita tilaus** painikkeen varastonhallinnan mobiilisovelluksessa.) Kun *Luo siirtotilaus* -tapahtuman sanomat on käsitelty, tilaksi päivitetään *Valmis* tai *Epäonnistui*. Kun *Suorita siirtotilaus* -tilaksi päivitetään *Valmis*, kaikki liittyvät tapahtumat poistetaan jonosta.

Koska erätyö ei käsittele siirtotilauksen tietojen luonnin **varastosovelluksen tapahtumia**, ennen kuin sanomien tilaksi on päivitetty *Asetettu jonoon*, pyydetyt siirtotilauksen numerot on haettava **Tunniste**-kentän osana. **Tunniste**-kenttä on **Varastosovelluksen tapahtumat** -sivun otsikko.

Siirtotilausrivin luonti voi epäonnistua varastotapahtuman käsittelyn osana. Siinä tapauksessa tapahtumasanoman tilaksi päivitetään *Epäonnistui*, ja voit selvittää **Erän loki** -tietojen avulla, miksi näin tapahtui, ja korjata mahdolliset ongelmat.

Tyypillisiä ovat prosessin puuttuviin vaiheisiin liittyvät ongelmat, kuten puuttuva siirtovarasto *Luo siirtotilaus*-tapahtumassa. Tällaisessa esimerkissä siirtovarasto lisätään lähetysvarastoon ja **Palauta**-asetuksella muutetaan kaikkien varastosovelluksen tapahtumasanomien tila *Epäonnistui* tilaksi *Asetettu jonoon*, jolloin erätyö käsittelee tapahtumasanomat uudelleen määritystietojen korjaamisen jälkeen.

Tuotantoympäristöissä poikkeukset voivat liittyä ennemminkin prosesseihin: esimerkiksi pyydetty rekisterikilpi voi olla erätyön käsittelyajankohtana tyhjä, jolloin mitään siirtotilausrivejä ei luoda. Tämä sanoma epäonnistuneesta tapahtumasta voidaan joko poistaa **Poista**-vaihtoehdolla tai tarvittava fyysinen käyttävissä oleva varasto voidaan lisätä rekisterikilpeen ja kaikissa liittyvissä tapahtumasanomissa käytetään **Palauta**-vaihtoehtoa.

Lisätietoja on kohdassa [Varastosovellustapahtuman käsittely](warehouse-app-events.md).

### <a name="follow-up-on-the-example-scenario-processing"></a>Esimerkkiskenaarion käsittelyn seuranta

Seuraavat tapahtuivat tämän skenaarion aikana:

1. Varastonhallinnan mobiilisovelluksella valittiin valikkovaihtoehto, joka käyttää tehtäväkoodia **Luo siirtotilaus rekisterikilvistä**.
1. Sovellus pyysi valitsemaan siirtotilauksen kohdevaraston. Lähdevarasto on aina se varasto, johon on kirjauduttu työntekijänä.
1. Kohdevarastoa valittaessa järjestelmä varasi tulevalle siirtotulokselle ID-numeron (järjestelmän määrittämän siirtotilauksen numerosarjan perusteella) muttei luonut siirtotilausta vielä.
1. Kun uuteen varastoon siirrettävän käytettävissä olevan varaston sisältävä rekisterikilpi *RK10* skannattiin, **varastosovellustapahtuma** lisättiin tapahtumajonoon myöhemmin käsiteltäväksi. Varastotapahtuman sanomassa oli tietoja skannauksesta, mukaan lukien aiotusta siirtotilauksen numerosta.
1. Kun **Suorita tilaus** valitaan varastonhallinnan mobiilisovelluksessa, uusi varastosovellustapahtuma, **Suorita siirtotilaus**, luodaan ja liittyvän aiemman luodun tapauksen, **Suorita siirtotilaus**, tila muuttui tilaksi **Asetettu jonoon**.
1. **Käsittele varastosovelluksen tapahtumia -erätyö** poimi taustalla **Asetettu jonoon** -tapahtuman ja keräsi skannattuun rekisterikilpeen liittyvän käytettävissä olevan varaston. Käytettävissä olevan varaston perusteella luotiin varsinainen siirtotilaustietue ja siihen liitetyt rivit. Työ täytti myös siirtotilauksen **Lähtevien lähetyskäytäntö** -kenttään arvon määritetyn *Vapautus ja lähetyksen vahvistus* -kohdan perusteella ja linkitti rekisterikilven **Rekisterikilpiopastus**-strategian rivien perusteella.
1. Siirtotilausrivin **Lähtevien lähetyskäytäntö** -kentän arvon perusteella **Siirtotilausten automaattinen vapauttaminen -erätyö** -kyselyn tuloksena oli siirtotilauksen vapauttaminen lähetysvarastoon. Käytettyjen **Aaltomalli**-, **Työmalli**- ja **Sijaintidirektiivit** -määritysten vuoksi työt käsiteltiin automaattisesti, jolloin **Kuorman tila** päivitettiin tilaan *Kuormattu*.
1. Kuormalle suoritettiin **Käsittele lähtevät lähetykset -erätyö**, jonka tuloksena siirtotilaus lähetettiin ja lähetysilmoitus (ASN) luotiin.
1. Näiden tapahtumien ajoitus on riippuvainen erätöille luoduista **Toistuminen**-asetuksista.

## <a name="frequently-asked-questions"></a>Usein kysytyt kysymykset

### <a name="mobile-device-menu-item-setup"></a>Mobiililaitteen valikkovaihtoehdon määrittäminen

#### <a name="why-cant-i-see-create-transfer-order-from-license-plate-in-the-menu-item-work-activity-drop-down-list"></a>Miksi Luo siirtotilaus rekisterikilvestä ei näy valikkovaihtoehdon avattava työtehtäväluettelossa?

*Luo ja käsittele siirtotilauksia varastosovelluksessa* -ominaisuus on otettava käyttöön. Lisätietoja on kohdassa [Siirtotilausten luonnin ottaminen käyttöön varastosovelluksessa](#enable-create-transfer-order-from-warehouse-app).

### <a name="warehouse-management-mobile-app-processes"></a>Varastonhallinnan mobiilisovelluksen prosessit

#### <a name="why-cant-i-see-the-menu-button-complete-order"></a>Miksi valikon Suorita tilaus -painike ei ole näkyvissä?

Siirtotilauksen on oltava määritettynä vähintään yksi rekisterikilpi.

#### <a name="can-several-warehouse-management-mobile-app-users-add-license-plates-to-the-same-transfer-order-at-the-same-time"></a>Voivatko useat varastonhallinnan mobiilisovelluksen käyttäjät lisätä rekisterikilpiä samaan siirtotilaukseen samanaikaisesti?

Kyllä. Useat varastotyöntekijät voivat skannata rekisterikilpiä samaan siirtotilaukseen.

#### <a name="can-the-same-license-plate-be-added-to-different-transfer-orders"></a>Voidaanko sama rekisterikilpi lisätä eri siirtotilauksiin?

Ei. Rekisterikilpi voidaan lisätä kerralla vain yhteen siirtotilaukseen.

#### <a name="after-having-selected-the-complete-order-button-can-i-then-add-more-license-plates-for-that-transfer-order"></a>Voiko siirtotilaukseen lisätä vielä rekisterikilpiä sen jälkeen, kun Suorita tilaus -painike on valittu?

Ei. Siirtotilaukseen, jossa on **Suorita siirtotilaus** -varastosovellustapahtuma, ei voi lisätä enää rekisterikilpiä.

#### <a name="how-can-i-find-existing-transfer-orders-to-be-used-via-the-select-transfer-order-button-in-the-warehouse-management-mobile-app-if-the-order-has-not-yet-been-created-in-the-backend-system"></a>Miten käytettävä aiemmin luotu siirtotilaus löydetään varastonhallinnan mobiilisovelluksen Valitse siirtotilaus -painikkeella, jos tilausta ei ole vielä luotu taustajärjestelmässä?

Vaikka tilauksia ei voi tällä hetkellä hakea sovelluksessa, siirtotilauksen numeroita voi etsiä **Varastosovellustapahtumat**-sivulla. Lisätietoja on kohdassa [Varastosovellustapahtumien kysely](#inquire-the-warehouse-app-events).

#### <a name="can-i-manually-select-the-transfer-order-number-to-be-used-from-the-warehouse-management-mobile-app"></a>Voidaanko varastonhallinnan mobiilisovelluksessa käytettävä siirtotilauksen numero valita manuaalisesti?

Vain automaattisesti numerojärjestystä käyttävää siirtotilauksen numeroiden luontia tuetaan.

### <a name="background-processing"></a>Taustaprosessi

#### <a name="how-should-i-clean-up-records-in-my-warehouse-app-events-queue-message-tables"></a>Miten tietoja tyhjennetään varastosovelluksen tapahtumajonon sanomataulukoista?

Niitä voi tarkastella ja ylläpitää **Varastosovellustapahtumat**-sivulla. Lisätietoja on kohdassa [Varastosovellustapahtumien kysely](#inquire-the-warehouse-app-events).

#### <a name="why-is-the-transfer-order-receipt-date-not-updated-according-to-my-delivery-date-control-setup"></a>Miksi siirtotilauksen vastaanottopäivä ei päivity toimituspäivämäärän tarkistusmääritysten mukaisesti?

Siirtotilauksen luodaan ilman **Toimituspäivän tarkistus** -ominaisuuksia.

#### <a name="can-i-use-a-license-plate-having-physical-negative-inventory-on-hand"></a>Voiko sellaista rekisterikilpeä käyttää, jonka fyysinen käytettävissä oleva varasto on negatiivinen?

Ominaisuus tukee vain positiivisia fyysisiä käytettävissä olevan varaston määriä rekisterikilpitasolla, mutta voi olla fyysisiä negatiivisia käytettävissä olevia varastoja korkeammalla fyysisen varaston ja varastotilan tasolla, kun määrität siirtotilauksille rekisterikilpiä.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]