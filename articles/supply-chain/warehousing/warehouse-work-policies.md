---
title: Työkäytännöt
description: Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää työkäytännöt.
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: d3f3a02a369cab34b965b2443bb77053377a190e
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6353369"
---
# <a name="work-policies"></a>Työkäytännöt

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten järjestelmä ja varastonhallinnan mobiilisovellus määritetään niin, että ne tukevat työkäytäntöjä. Tämän toiminnon avulla voit rekisteröidä varaston nopeasti ilman hyllytystyön luomista silloin, kun vastaanotat osto- ja siirtotilauksia ja kun viimeistelet valmistusprosesseja. Tämä ohjeaihe sisältää yleistietoja. Saat yksityiskohtaisia tietoja rekisterikilven vastaanotosta kohdassa [Rekisterikilven vastaanotto varastonhallinnan mobiilisovelluksen kautta](warehousing-mobile-device-app-license-plate-receiving.md).

Työkäytäntö määrittää, luodaanko varastotyö valmistetun nimikkeen valmiiksi raportoinnin yhteydessä vai silloin, kun tavarat vastaanotetaan käyttämällä varastonhallinnan mobiilisovellusta. Voit määrittää kunkin työkäytännön määrittämällä sen ehdot: työtilaustyypit ja -prosessit, varaston sijainnin ja (vaihtoehtoisesti) tuotteet. Esimerkiksi ostotilaus tuotteelle *A0001* on vastaanotettava sijainnissa *RECV* varastossa *24*. Myöhemmin tuotetta kulutetaan toisessa prosessissa sijainnissa *RECV*. Tässä tapauksessa määrität työkäytännön, joka estää hyllytystyön luomisen, kun työntekijä raportoi tuotteen *A0001* vastaanotetuksi sijainnissa *RECV*.

> [!NOTE]
> - Jotta työkäytäntö olisi aktiivinen, määritä sille ensin vähintään yksi sijainti **Varastosijainnit**-pikavälilehdessä **Työkäytännöt**-sivulla. 
> - Et voi määrittää samaa sijaintia useille työkäytännöille.
> - Mobiililaitteen valikon vaihtoehtojen **Tulosta tarra** -asetus ei tulosta rekisterikilven otsikkoa, jos työtä ei ole luotu.

## <a name="activate-the-features-in-your-system"></a>Järjestelmän ominaisuuksien aktivoiminen

Voit ottaa tämän ohjeaiheen kaikki toiminnot käyttöön järjestelmässä ottamalla seuraavat kaksi ominaisuutta käyttöön [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- Rekisterikilven vastaanoton parannukset
- Saapuvan työn työkäytäntöjen parannukset

## <a name="the-work-policies-page"></a>Työkäytännöt-sivu

Voit määrittää työkäytännöt siirtymällä kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työkäytännöt**. Määritä sitten kunkin pikavälilehden kentät seuraavien aliosien mukaan.

### <a name="the-work-order-types-fasttab"></a>Työtilaustyypit-pikavälilehti

Lisää **Työtilaustyypit**-pikavälilehteen kaikki työtilaustyypit ja liittyvät työprosessit, joita työkäytäntö koskee. Työkäytännöt tukevat seuraavia työtilaustyyppejä ja liittyviä työprosesseja.

| Työtilaustyyppi | Työprosessi |
|---|---|
| Raaka-aineiden keräily| Kaikki liittyvät prosessit |
| Rinnakkaistuotteen ja sivutuotteen poispano | Kaikki liittyvät prosessit |
| Valmiiden tuotteiden hyllytys | Kaikki liittyvät prosessit |
| Siirron vastaanotto | Rekisterikilven vastaanotto (ja hyllytys) |
| Ostotilaukset | <ul><li>Rekisterikilven vastaanotto (ja hyllytys)</li><li>Kuorman nimikkeen vastaanotto (ja hyllytys)</li><li>Ostotilausrivin vastaanotto (ja hyllytys)</li><li>Ostotilausnimikkeen vastaanotto (ja hyllytys)</li></ul> |

Jos haluat määrittää työkäytännön niin, että se koskee saman työtilaustyypin useita työprosesseja, lisää erillinen rivi jokaiselle ruudukon työprosessille.

Määritä ruudukon jokaisen rivin **Työn luontimenetelmä** -kenttään jokin seuraavista arvoista:

- **Ei koskaan** – Työkäytäntö estää varastotyön luomisen valitulle työtilaustyypille ja liittyvälle työprosessille.
- **Cross-docking** – Työkäytäntö luo cross-docking-työn käyttämällä **Cross-docking-käytännön nimi** -kentässä valittua käytäntöä.

### <a name="the-inventory-locations-fasttab"></a>Varastosijainnit-pikavälilehti

Lisää **Varastosijainnit**-pikavälilehteen kaikki sijainnit, joihin tämä työkäytäntö tulee kohdistaa. Jos sijaintia ei ole liitetty työkäytäntöön, työkäytäntöä ei käytetä missään prosessissa.

Et voi määrittää samaa sijaintia useille työkäytännöille.

Voit käyttää sijaintiprofiiliin määritettyä varastopaikkaa, jonka **rekisterikilven seuranta** on poistettu käytöstä. Tällöin työntekijät rekisteröivät käytettävissä olevan varaston suoraan.

### <a name="the-products-fasttab"></a>Tuotteet-pikavälilehti

Määritä **Tuotteet**-välilehdessä **Tuotevalinta**-kenttä niin, että se ohjaa käytäntöjen kohdistamista tuotteisiin seuraavasti:

- **Kaikki** – Käytäntö kohdistetaan kaikkiin tuotteisiin.
- **Valittu** – Käytäntö kohdistetaan vain tuotteisiin, jotka ovat ruudukossa. Käytä **Tuotteet**-pikavälilehden työkaluriviä, jos haluat lisätä tuotteita ruudukkoon tai poistaa niitä ruudukosta.

## <a name="default-and-custom-to-locations"></a>Oletus- ja mukautetut kohdesijainnit

> [!NOTE]
> Jos haluat määrittää tässä osassa kuvaillun toiminnon käytettäväksi järjestelmässä, ota käyttöön *Rekisterikilven vastaanoton parannukset*- ja *Työkäytännön parannukset saapuvalle työlle* -toiminnot [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -kohdassa.

Aiemmin järjestelmä tuki vain kullekin varastolle määritettyä oletussijaintia. Seuraavia työn luontiprosesseja käyttävät mobiililaitteen valikon vaihtoehdot sisältävät nyt kuitenkin **Käytä oletustietoja** -vaihtoehdon. Tämän vaihtoehdon avulla voit määrittää kohdesijainnin yhdelle tai usealle valikon vaihtoehdolle. (Tämä vaihtoehto on jo käytettävissä joidenkin muun tyyppisten valikkovaihtoehtojen yhteydessä.)

- Rekisterikilven vastaanotto (ja hyllytys)
- Kuorman nimikkeen vastaanotto (ja hyllytys)
- Ostotilausrivin vastaanotto (ja hyllytys)
- Ostotilausnimikkeen vastaanotto (ja hyllytys)

Valikon vaihtoehdon **Kohdesijainti**-asetus korvaa varaston oletusvastaanottosijainnin kaikissa tilauksissa, jotka on käsitelty kyseisen valikon vaihtoehdon avulla.

Voit määrittää mobiililaitteen valikon vaihtoehdon tukemaan vastaanottoa mukautetussa sijainnissa alla olevien vaiheiden avulla.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.
1. Valitse valikon vaihtoehto, joka käyttää jotain aiemmin tässä osassa mainittua työn luontiprosessia, tai luo valikon vaihtoehto.
1. Määritä **Yleinen**-pikavälilehdessä **Käytä oletustietoja** -asetukseksi **Kyllä**.
1. Valitse toimintoruudusta **Oletustiedot**.
1. Määritä **Oletustiedot**-sivulla seuraavat arvot:

    - **Oletustietokenttä:** Määritä tämän kentän arvoksi *Kohdesijainti*.
    - **Varasto:** Valitse tämän valikon vaihtoehdon yhteydessä käytettävä kohdevarasto.
    - **Sijainti:** Tässä kentässä ovat kaikki sijaintien tunnukset, jotka ovat käytettävissä valitussa varastossa. Tämän kentän määrittäminen ei kuitenkaan muuta tilannetta. Tämän vuoksi kenttä voidaan jättää tyhjäksi. Voit silti käyttää luetteloa, jos haluat varmistaa **Kovakoodattu arvo** -kenttään annettavan tunnuksen.
    - **Kovakoodattu arvo:** Anna sijainnin tunnus vastaanottosijainnille, joka koskee tätä valikon vaihtoehtoa.

> [!TIP]
> Työkäytäntö voidaan kohdistaa vain, jos kaikki vastaanottosijainnit on luetteloitu liittyvän työkäytännön asetuksissa. Tämä vaatimus on voimassa siitä huolimatta, onko käytössä varaston oletusvastaanottopaikka vai mukautettu kohdesijainti.

## <a name="example-scenario-warehouse-receiving"></a>Esimerkkiskenaario: Varaston vastaanotto

Kaikki tuotteet, jotka on vastaanotettu *Ostotilausnimikkeen vastaanotto (ja hyllytys)* -prosessin avulla, on rekisteröitävä sijainnissa *FL-001*. Niiden on myös oltava käytettävissä varastossa *24*. Työtä ei kuitenkaan tule luoda. Tuotteet, jotka vastaanotetaan jonkin muun prosessin avulla (käyttämällä muita mobiililaitteen valikon vaihtoehtoja), on rekisteröitävä varaston oletusvastaanottosijaintiin (*RECV*). Työ tulee luoda normaaliin tapaan. (Tässä skenaariossa ei näytetä vastaanoton oletusasetuksia.)

Tämä skenaario edellyttää seuraavia elementtejä:

- *Ostotilausnimikkeen vastaanotto (ja hyllytys)* -prosessin työkäytäntö sijainnissa *FL-001* kaikille tuotteille
- Mobiililaitteen valikon vaihtoehto, jolla on oletustiedot ja joka määrittää **Kohdesijainti**-kentän arvoksi *FL-001*

### <a name="prerequisites"></a>Edellytykset

Jos haluat määrittää tässä skenaariossa kuvaillun toiminnon käytettäväksi järjestelmässä, ota käyttöön *Rekisterikilven vastaanoton parannukset*- ja *Työkäytännön parannukset saapuvalle työlle* -toiminnot [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -kohdassa.

Tässä skenaariossa käytetään vakioesittelytietoja. Jos siis haluat käsitellä tätä skenaariota käyttämällä tässä annettuja arvoja, sinun on työskenneltävä järjestelmässä, johon on asennettu esittelytiedot. Sinun on myös valittava **USMF**-yritys.

### <a name="set-up-a-work-policy"></a>Määritä työkäytäntö

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työkäytännöt**.
1. Valitse **Uusi**.
1. Anna **Työkäytännön nimi** -kenttään *Ei ostonimikkeen hyllytystyötä*.
1. Valitse **Tallenna**.
1. Valitse **Työtilaustyypit**-pikavälilehdessä **Lisää**, jos haluat lisätä rivin ruudukkoon. Määritä sitten uuden rivin seuraavat arvot:

    - **Työtilaustyyppi:** *Ostotilaukset*
    - **Työprosessi:** *Ostotilausnimikkeen vastaanotto (ja hyllytys)*
    - **Työn luontimenetelmä:** *Ei koskaan*
    - **Cross-docking-käytännön nimi:** Jätä tämä kenttä tyhjäksi.

1. Valitse **Varastosijainnit**-pikavälilehdessä **Lisää**, jos haluat lisätä rivin ruudukkoon. Määritä sitten uuden rivin seuraavat arvot:

    - **Varasto**: *24*
    - **Sijainti:** *FL-001*

1. Määritä **Tuotteet**-pikavälilehdessä **Tuotteen valinta** -kentän arvoksi *Kaikki*.
1. Valitse **Tallenna**.

### <a name="set-up-a-mobile-device-menu-item-to-change-the-receiving-location"></a>Määritä mobiililaitteen valikon vaihtoehto, jos haluat muuttaa vastaanottosijaintia

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.
1. Valitse vasemmanpuoleisessa ruudussa olemassa oleva valikon **Oston vastaanotto** -vaihtoehto.
1. Määritä **Yleinen**-pikavälilehdessä **Käytä oletustietoja** -asetukseksi *Kyllä*.
1. Valitse **Tallenna**.
1. Valitse toimintoruudusta **Oletustiedot**.
1. Valitse **Oletustiedot**-sivun toimintoruudussa **Uusi**, jos haluat lisätä rivin ruudukkoon. Määritä sitten uuden rivin seuraavat arvot:

    - **Oletustietokenttä:** *Kohdesijainti*
    - **Varasto**: *24*
    - **SIjainti:** Jätä tämä kenttä tyhjäksi.
    - **Kovakoodattu arvo:** *FL-001*

1. Valitse **Tallenna**.

### <a name="receive-a-purchase-order-without-creating-work"></a>Ostotilauksen vastaanottaminen ilman työn luomista

Tämä osan esimerkki osoittaa, miten ostotilausnimike vastaanotetaan ilman työn luomista sijainnissa, joka on eri kuin tälle varastolle määritetty oletusvastaanottosijainti. Tässä esimerkissä käytetään työkäytäntöä ja mobiililaitenimikettä, jotka luotiin aiemmin tässä skenaariossa.

#### <a name="create-a-purchase-order"></a>Ostotilauksen luominen

1. Siirry kohtaan **Hankinta ja alihankinta \> Ostotilaukset \> Kaikki ostotilaukset**.
1. Valitse **Uusi**.
1. Aseta **Luo ostotilaus** -valintaikkunassa seuraavat arvot:

    - **Toimittajan tili:** *US-101*
    - **Toimipaikka:** *2*
    - **Varasto**: *24*

1. Valitse **OK**, jos haluat sulkea valintaikkunan ja avata uuden ostotilauksen.
1. Määritä **Ostotilausrivit**-pikavälilehdessä seuraavat arvot tyhjälle riville:

    - **Nimiketunnus:** *A0001*
    - **Määrä** *1*

1. Valitse **Tallenna**.
1. Kirjoita ostotilauksen numero muistiin.

#### <a name="receive-a-purchase-order"></a>Ostotilauksen vastaanottaminen

1. Kirjaudu mobiililaitteella varastoon *24* käyttämällä käyttäjätunnusta *24* ja salasanaa *1*.
1. Valitse **Saapuva**.
1. Valitse **Oston vastaanotto**. **Sijainti**-kentän arvoksi tulee määrittää *FL-001*.
1. Anna edellisessä proseduurissa luodun ostotilauksen ostotilausnumero.
1. Anna **Nimiketunnus**-kenttään arvo *A0001*.
1. Valitse **OK**.
1. Kirjoita **Määrä**-kenttään *1*.
1. Valitse **OK**.

Ostotilaus on nyt vastaanotettu, mutta siihen ei ole liitetty työtä. Käytettävissä oleva varasto on päivitetty. Määrä *1* nimikettä *A0001* on nyt käytettävissä sijainnissa *FL-001*.

## <a name="example-scenario-manufacturing"></a>Esimerkkiskenaario: Valmistus

Seuraavassa esimerkissä on kaksi tuotantotilausta, jotka ovat *PRD-001* ja *PRD-002*. Tuotantotilaus *PRD-001* sisältää *Kokoonpano*-työvaiheen, jolla tuote *SC1* raportoidaan valmiiksi sijainnissa *001*. Tuotantotilaus *PRD-002* sisältää *Maalaus*-työvaiheen ja käyttää tuotetta *SC1* sijainnista *001*. Tuotantotilaus *PRD-002* käyttää myös raaka-ainetta *RM1* sijainnissa *001*. Raaka-ainetta *RM1* varastoidaan varastosijaintiin *BULK-001*, josta raaka-ainekeräilyn varastotyö kerää sen sijaintiin *001*. Keräilytyö luodaan, kun tuotanto *PRD-002* vapautetaan.

[![Varaston työkäytännöt.](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)

Kun suunnittelet tämän skenaarion mukaista varastotyön konfigurointia, ota huomioon seuraavat seikat:

- Valmiiden tuotteiden hyllytyksen varastotyötä ei tarvita, kun raportoit tuotteen *SC1* valmiiksi tuotantotilauksesta *PRD-001* sijainnissa *001*. Tämä johtuu siitä, että *Maalaus*-työvaihe tuotantotilauksessa *PRD-002* käyttää *SC1*:n samassa sijainnissa.
- Raaka-aineen keräilyn varastotyö vaaditaan, jotta raaka-aine *RM1* siirretään varastosijainnista *BULK-001* sijaintiin *001*.

Seuraavassa on esimerkki työmenettelystä, jonka voit määrittää näiden havaintojen perusteella:

- **Työkäytännön nimi:** *Ei hyllytystyötä*
- **Työtilaustyypit:** *Valmiiden tuotteiden hyllytys* ja *Rinnakkais- ja sivutuotteen hyllytys*
- **Varastosijainnit:** Varasto *51* ja sijainti *001*
- **Tuotteet:** *SC1*

Seuraavassa esimerkkiskenaariossa on vaiheittaiset ohjeet varastotyökäytännön määrittämiseksi tässä skenaariossa.

## <a name="example-scenario-report-as-finished-to-a-location-that-isnt-license-platecontrolled"></a>Esimerkkiskenaario: Raportoi valmistuneeksi sijaintiin, jossa ei ole varastorekisterinumero-ohjausta

Tässä skenaariossa on esimerkki, jossa tuotantotilaus raportoidaan valmiiksi tiettyyn sijaintiin, jossa ei ole varastorekisterinumero-ohjausta.

Tässä skenaariossa käytetään vakioesittelytietoja. Jos siis haluat käsitellä tätä skenaariota käyttämällä tässä annettuja arvoja, sinun on työskenneltävä järjestelmässä, johon on asennettu esittelytiedot. Sinun on myös valittava **USMF**-yritys.

### <a name="set-up-a-warehouse-work-policy"></a>Määritä varaston työkäytäntö

Varastointiprosessit eivät aina sisällä varastotyötä. Voit määrittää työn käytännön, joka estää raaka-aineen keräilytyön ja valmiiden tuotteiden hyllytystöiden luonnin tietyille tuotejoukoille tietyissä sijainneissa.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työkäytännöt**.
1. Valitse **Uusi**.
1. Anna **Työkäytännön nimi** -kenttään *Ei hyllytystyötä*.
1. Valitse toimintoruudussa **Tallenna**.
1. Valitse **Työtilaustyypit**-pikavälilehdessä **Lisää**, jos haluat lisätä rivin ruudukkoon. Määritä sitten uuden rivin seuraavat arvot:

    - **Työtilaustyyppi:** *Valmiiden tuotteiden hyllytys*
    - **Työprosessi:** *Kaikki liittyvät työprosessit*
    - **Työn luontimenetelmä:** *Ei koskaan*
    - **Cross-docking-käytännön nimi:** Jätä tämä kenttä tyhjäksi.

1. Valitse **Lisää** uudelleen, jos haluat lisätä toisen rivin ruudukkoon. Määritä sitten uuden rivin seuraavat arvot:

    - **Työtilauksen tyyppi:** *Rinnakkais- ja sivutuotteen hyllytys*
    - **Työprosessi:** *Kaikki liittyvät työprosessit*
    - **Työn luontimenetelmä:** *Ei koskaan*
    - **Cross-docking-käytännön nimi:** Jätä tämä kenttä tyhjäksi.

1. Valitse **Varastosijainnit**-pikavälilehdessä **Lisää**, jos haluat lisätä rivin ruudukkoon. Määritä sitten uuden rivin seuraavat arvot:

    - **Varasto**: *51*
    - **Sijainti:** *001*

1. Määritä **Tuotteet**-pikavälilehdessä **Tuotteen valinta** -kentän arvoksi *Valittu*.
1. Valitse **Tuotteet**-pikavälilehdessä **Lisää**, jos haluat lisätä uuden rivin ruudukkoon.
1. Määritä uuden rivin **Nimiketunnus**-kentän arvoksi *L0101*.
1. Valitse toimintoruudussa **Tallenna**.

### <a name="set-up-an-output-location"></a>Määritä tulostussijainti

1. Siirry kohtaan **Organisaation hallinto \> Resurssit \> Resurssiryhmät**.
1. Valitse vasemmasta ruudusta resurssiryhmä **5102**.
1. Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:

    - **Tulostusvarasto:** *51*
    - **Tulostussijainti:** *001*

1. Valitse toimintoruudussa **Tallenna**.

> [!NOTE]
> Sijainti *001* ei ole rekisterikilven mukaan ohjattu sijainti. Voit määrittää rekisterikilven mukaan ohjaamattoman tulostussijainnin ainoastaan, jos sijainnille on olemassa soveltuva työkäytäntö.

### <a name="create-a-production-order-and-report-it-as-finished"></a>Luo tuotantotilaus ja ilmoita se valmiiksi

1. Siirry kohtaan **Tuotannonhallinta \> Tuotantotilaukset \> Kaikki tuotantotilaukset**.
1. Valitse toimintoruudussa **Uusi tuotantotilaus**.
1. Määritä **Luo tuotantotilaus** -valintaikkunassa **Nimiketunnus**-kentän arvoksi *L0101*.
1. Valitse **Luo** luodaksesi tilauksen. Sulje sitten valintaikkuna.

    Uusi tuotantotilaus lisätään ruudukkoon **Kaikki tuotantotilaukset** -sivulla.

    Pidä uusi tuotantotilaus valittuna.

1. Valitse toimintoruudun **Tuotantotilaus**-välilehden **Käsittely**-ryhmässä **Arvio**.
1. Katso arvio **Arvio**-valintaikkunasta ja sulje valintaikkuna valitsemalla **OK**.
1. Valitse toimintoruudun **Tuotantotilaus**-välilehden **Käsittely**-ryhmässä **Käynnistä**.
1. Määritä **Käynnistä**-valintaikkunan **Yleistä**-välilehdessä **Automaattinen tuoterakennekulutus** -kentän arvoksi *Ei koskaan*.
1. Valitse **OK** tallentaaksesi asetuksen. Sulje valintaikkuna.
1. Valitse toimintoruudun **Tuotantotilaus**-välilehden **Käsittely**-ryhmässä **Ilmoita valmistuneeksi**.
1. Määritä **Ilmoita valmistuneeksi** -valintaikkunan **Yleistä**-välilehdessä **Hyväksy virhe** -valinnan arvoksi *Kyllä*.
1. Valitse **OK** tallentaaksesi asetuksen. Sulje valintaikkuna.
1. Valitse toimintoruudun **Varasto**-välilehden **Yleinen**-ryhmässä **Työn tiedot**.

Kun tuotantotilaus on ilmoitettu valmistuneeksi, hyllytystyötä ei luoda. Tämä toiminta johtuu siitä, että määritettynä on työkäytäntö, joka estää töiden luonnin, kun tuote *L0101* ilmoitetaan valmiiksi sijainnissa *001*.

## <a name="more-information"></a>Lisätietoja

Lisätietoja mobiililaitteiden valikkokohteista on kohdassa [Mobiililaitteiden määrittäminen varastotyötä varten](configure-mobile-devices-warehouse.md).

Lisätietoja rekisterikilven vastaanotosta ja työkäytännöistä on kohdassa [Rekisterikilven vastaanotto varastonhallinnan mobiilisovelluksen kautta](warehousing-mobile-device-app-license-plate-receiving.md).

Lisätietoja saapuvien kuormien hallinnasta on kohdassa [Ostotilausten saapuvien kuormien varastokäsittely](inbound-load-handling.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]