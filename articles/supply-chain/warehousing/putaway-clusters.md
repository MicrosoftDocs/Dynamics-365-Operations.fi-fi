---
title: Hyllytysklusterit
description: Hyllytysklusterit ovat tapa, jolla voi kerätä samanaikaisesti useita rekisterikilpiä viedä sitten hyllytettäviksi eri sijainteihin. Ne voivat olla erittäin käteviä vähittäismyynnissä, jossa rekisterikilvet eivät yleensä ole täysiä kuormalavoja.
author: Mirzaab
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: c2b12798a6ef9c2d4aa022e0c270d8191b2cf4e7fc844042ed88c4eb9f5b98a5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741905"
---
# <a name="putaway-clusters"></a>Hyllytysklusterit

[!include [banner](../includes/banner.md)]

Hyllytysklusterit ovat tapa, jolla voi kerätä samanaikaisesti useita rekisterikilpiä viedä sitten hyllytettäviksi eri sijainteihin. Tätä prosessi on kuin *jakelureitti*. Hyllytysklusterit voivat olla erittäin käteviä vähittäismyynnissä, jossa rekisterikilvet eivät yleensä ole täysiä kuormalavoja. 

## <a name="turn-on-the-cluster-putaway-feature"></a>Klusterihyllytystoiminnon ottaminen käyttöön

Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi. Järjestelmänvalvojat voivat käyttää [Toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) työtilaa tarkistaakseen toiminnon tilan sekä laittaa sen päälle, jos sitä vaaditaan. Tässä tapauksessa toiminto näkyy seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Toiminnon nimi:** *Klusterihyllytystoiminto*

## <a name="setup-for-the-example-scenario"></a>Esimerkkiskenaarion määrittäminen

### <a name="cluster-profiles"></a>Klusteriprofiilit

Hyllytyksen klusteriprofiili määrittää, mihin nimike sijoitetaan, sen sijainnin perusteella, joka nimikkeelle määritettiin vastaanoton yhteydessä. Jos tarvitaan eri klustereita, kullekin mobiililaitteen valikkonimikkeelle on luotava yksi erillinen hyllytysklusteri.

1. Valitse **Varastonhallinta \> Asetukset \> Mobiililaite \> Klusteriprofiilit**.
1. Valitse toimintoruudussa **Uusi**.
1. Määritä **Otsikko**-näkymässä seuraavat arvot:

    - **Hyllytyksen klusteriprofiilin tunnus:** *Klusterihyllytys*
    - **Hyllytyksen klusteriprofiilin nimi:** *Klusterihyllytys*
    - **Klusterityyppi:** *Hyllytys*
    - **Järjestysnumero:** Hyväksy oletusarvo.

1. Valitsemalla **Tallenna** voit ottaa pakolliset kentät käyttöön **Yleinen**-pikavälilehdessä.
1. Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:

    - **Klusterimäärityksen ajoitus:** *Vastaanotossa*

        Tämä kenttää määrittää, määritetäänkö hyllytysklusteri heti, kun varasto vastaanotetaan, vai lajitellaanko se myöhemmin.

    - **Klusterin määrityssääntö:** *Manuaalinen*

        Tämä kenttä määrittää, onko järjestelmän määritettävä klusterimääritys automaattisesti vai määrittääkö käyttäjä sen manuaalisesti.

    - **Direktiivikoodi:** Jätä tämä kenttä tyhjäksi.
    - **Hyllytysklusterin paikannus:** *Vastaanotto*

        Käytettävissä ovat seuraavat arvot:

        - **Vastaanotto** – sijainti löydetään heti vastaanoton aikana.
        - **Klusteria suljettaessa** – sijainti löydetään klusteria suljettaessa.
        - **Käyttäjäohjattu** – Sijainti löydetään, kun rekisterikilpi kerätään klusterista hyllytettäväksi. Tässä tapauksessa sijaintia ei määritetä, kun hyllytystyö luodaan. Käyttäjän on käynnistettävä sijoitusvaihe skannaamalla rekisterikilpi tai työtunnus hyllytyksen aikana. Järjestelmä etsii sitten hyllytyssijainnin ja kertoo käyttäjälle, mihin kerätty määrä asetetaan.

    - **Käyttäjäkohtainen hyllytysklusteri:** *Ei*

        Tämä kenttä määrittää, onko kukin klusteri käyttäjäkohtainen, kun klustereita määritetään automaattisesti. Se on käytettävissä vain, kun **Klusterin määrityssääntö** -kentän asetuksena on *Automaattinen*.

    - **Yksikkörajoitus:** jätä kenttä tyhjäksi.

        Tämä kenttä määrittää yksikön, joka on vastaanotettava, jotta profiili on kelvollinen. Jos jätetään tyhjäksi, kaikki yksiköt ovat kelvollisia.

    - **Työyksikön vaihto:** *Yksittäinen*

        Tämä kenttä määrittää, konsolidoidaanko koko varasto (käyttämällä klusterin tunnusta ja rekisterikilpeä) yhteen rekisterikilpeen, kun klusteri suljetaan, ja hyllytetäänkö se yhtenä rekisterikilpenä vai erikseen vastaanotettuina rekisterikilpinä. Tämä kenttä ei ole käytettävissä, kun **Hyllytysklusterin paikannus** -kentän asetuksena on *Vastaanotto*.

    - **Klusteri säilyy päärekisterikilpenä:** *Ei*

        Jos tässä on asetuksena *Kyllä*, asetusvaiheen suorittamisen jälkeen klusterin tunnuksesta tulee päärekisterikilpi ja kaikki klusteritunnuksen nimikkeet linkitetään kyseiseen päärekisterikilpeen.

1. Hyllytyksen lajitteluehdot määritetään **Klusterin lajittelu** -pikavälilehdessä. Lisää rivi valitsemalla työkalurivillä **Uusi** ja määritä sitten seuraavat arvot:

    - **Järjestysnumero:** Hyväksy oletusarvo.
    - **Kentän nimi:** *WMSLocationId*

        Tämä kenttä määrittää kentän, jota tämän rivin on käytettävä lajitteluehtona.

    - **Lajittelu:** *Nouseva*

        Tässä kentässä määritetään, tehdäänkö lajittelu nousevassa vai laskevassa järjestyksessä.

1. Lisää rivi valitsemalla **Klusterin työmalli** -pikavälilehden työkalurivillä **Uusi** ja määritä sitten seuraavat arvot:

    - **Työtilaustyyppi:** *Ostotilaukset*
    - **Työmalli:** *61 - ostotilaus, suora*

1. Valitse toimintoruudussa ensin **Tallenna** ja sitten **Muokkaa kyselyä**.
1. Lisää kyselyyn toinen rivi valitsemalla **Klusterihyllytys**-valintaikkunan **Alue**-välilehdessä **Lisää**. Päivitä sitten kyselyn rivit seuraavan taulukon mukaisesti.

    | Taulu | Johdettu taulu | Kenttä | Kriteeri |
    |---|---|---|---|
    | Työ | Työ | Varasto | *61* |
    | Työ | Työ | Työ tunnus | Jätä tämä kenttä tyhjäksi. |

1. Tallenna kysely ja sulje valintaikkuna valitsemalla **OK**.
1. Valitse toimintoruudussa **Tallenna** ja sulje sivu.

> [!IMPORTANT]
> Klusteriprofiilissa himmennettyinä näkyvät kentät, kun **Luo klusterin tunnus** -asetuksena on *Kyllä*, eivät ole käytettävissä eikä niitä oteta huomioon tätä ominaisuutta käytettäessä.

### <a name="mobile-device-menu-items"></a>Mobiililaitteen valikkovaihtoehdot

Tässä toiminnossa on kaksi uutta mobiililaitteen valikkovaihtoehtoa. **Vastaanotto ja klusterilajittelu** -valikkovaihtoehdolla lajitellaan vastaanotettu varasto hyllytysklusteriin vastaanotettaessa. **Klusterihyllytys**-valikkovaihtoehdolla klusteri hyllytetään määrityksen jälkeen.

#### <a name="receive-and-sort-cluster"></a>Vastaanotto ja klusterilajittelu

Luo uusi mobiililaitteen valikkovaihtoehto varaston vastaanottamiseen ja lajitteluun klusteriin. Tämä valikkovaihtoehto luo saapuvan työn varaston vastaanoton jälkeen, ja se ilmaisee, että vastaanoton valikkovaihtoehtoja käytetään hyllytysklustereissa.

> [!NOTE]
> **Vastaanotto ja klusterilajittelu** -valikkovaihtoehtoa voidaan käyttää vastaanoton seuraavien valikkovaihtoehtojen kanssa:
>
> - Ostotilausrivin vastaanotto
> - Ostotilausnimikkeen vastaanotto
> - Kuorman nimikkeen vastaanotto

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.
1. Valitse toimintoruudussa **Uusi**.
1. Määritä **Otsikko**-näkymässä seuraavat arvot:

    - **Valikkovaihtoehdon nimi:** *Vastaanotto ja klusterilajittelu*
    - **Otsikko:** *Vastaanotto ja klusterilajittelu*
    - **Tila:** *Työ*
    - **Käytä aiemmin luotua työtä:** *Ei*

1. Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:

    - **Työn luontiprosessi:** *Ostotilausnimikkeen vastaanotto*
    - **Luo rekisterikilpi:** *Kyllä*
    - **Määritä hyllytysklusteri:** *Kyllä*

        > [!NOTE]
        > **Määritä hyllytysklusteri** -asetus on käytettävissä vain vastaanoton yksivaiheisessa *Työn luontiprosessi* -tehtävässä.

    Hyväksy jäljellä olevien kenttien oletusarvot.

1. Valitse toimintoruudussa **Tallenna**.

#### <a name="cluster-putaway"></a>Klusterin varastointi

Luo uusi mobiililaitteen valikkovaihto klusterin hyllytykseen sen jälkeen, kun se on määritetty.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.
1. Valitse toimintoruudussa **Uusi**.
1. Määritä **Otsikko**-näkymässä seuraavat arvot:

    - **Valikkovaihtoehdon nimi:** *Klusterihyllytys*
    - **Otsikko:** *Klusterihyllytys*
    - **Tila:** *Työ*
    - **Käytä aiemmin luotua työtä:** *Kyllä*

1. Määritä **Yleinen**-pikavälilehden **Ohjaus**-kentän arvoksi *Klusterihyllytys*. Hyväksy jäljellä olevien kenttien oletusarvot.
1. Määritä **Työluokat**-pikavälilehdessä kelvollinen työluokka tälle mobiililaitteen valikkovaihtoehdolle:

    - **Työluokan tunnus:** *Osto*
    - **Työtilaustyyppi:** *Ostotilaukset*

1. Valitse toimintoruudussa **Tallenna**.

### <a name="mobile-device-menu"></a>Mobiililaitevalikko

Lisää juuri luodut valikkovaihtoehdot mobiilisovelluksen saapuvien valikkoon.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikko**.
1. Valitse toimintoruudussa **Muokkaa**.
1. Valitse valikkoluettelossa **Saapuvat**.
1. Etsi ja valitse **Käytettävissä olevat valikot ja valikkovaihtoehdot** -luettelossa **Vastaanotto ja klusterilajittelu**.
1. Siirrä valittu valikkovaihtoehto **Valikkorakenne**-luetteloon valitsemalla oikea nuolipainike.
1. Siirrä valikkovaihtoehto haluttuun kohtaan valikossa ylä- tai alanuolipainikkeella.
1. Valitse toimintoruudussa **Tallenna**.
1. Lisää loput valikkovaihtoehdot toistamalla vaiheet 4–7:

    - Määritä klusteri
    - Klusterin varastointi

## <a name="example-scenario"></a>Esimerkkiskenaario

Tämä skenaario simuloi hyllytysklusterin käsittelyä.

### <a name="create-a-purchase-order"></a>Ostotilauksen luominen

1. Valitse **Ostoreskontra \> Ostotilaukset \> Kaikki ostotilaukset**.
1. Valitse toimintoruudussa **Uusi**.
1. Aseta **Luo ostotilaus** -valintaikkunassa seuraavat arvot:

    - **Toimittajan tili:** *1001*
    - **Varasto**: *61*

1. Valitse **OK**.

    **Kaikki ostotilaukset** -sivu avautuu.

1. Lisää **Kaikki ostotilaukset** -sivun **Ostotilausrivit**-pikavälilehdessä **Lisää rivi** -painikkeella seuraavat rivit:

    - Ostotilausrivi 1:

        - **Nimiketunnus:** *A0001*
        - **Määrä** *10*

    - Ostotilausrivi 2:

        - **Nimiketunnus:** *A0002*
        - **Määrä** *20*

    - Ostotilausrivi 3:

        - **Nimiketunnus:** *M9215*
        - **Määrä** *30*

1. Valitse toimintoruudussa **Tallenna**.
1. Kirjoita ostotilauksen numero muistiin.

### <a name="receive-inventory-and-put-it-away-from-the-mobile-device"></a>Varaston vastaanotto ja hyllytys mobiililaitteella

#### <a name="receive-and-sort-the-inventory-into-a-cluster"></a>Varaston vastaanotto ja lajittelu klusteriin

1. Kirjaudu varastonhallinnan mobiilisovellukseen käyttäjänä, joka on määritetty varastoon *61*.
1. Valitse päävalikossa **Saapuva**.
1. Valitse **Saapuva**-valikossa **Vastaanotto ja klusterilajittelu**.
1. Anna **Ostotilausnro**-kentässä ostotilauksen numero.
1. Valitse **OK** (valintamerkkipainike).
1. Valitse **Nimike**-kenttä ja anna nimiketunnus *A0001* ja valitse sitten **OK**.
1. Valitse **Määrä**-kenttä, anna arvoksi *10* numeronäppäimistöllä ja valitse sitten valintamerkkipainike.
1. Vahvista annettu määrä valitsemalla **Määrä**-tehtäväsivulla **OK** (valintamerkkipainike).
1. Vahvista valitsemalla **Nimike**-tehtäväsivulla **OK**, että nimike *A0001* annettiin.
1. Valitse **Klusterin tunnus** -kenttä ja määritä luotavalle klusterille tunnus antamalla jokin arvo.

    Tässä annettua arvoa käytetään, kun ostotilauksessa jäljellä olevat kaksi nimikettä vastaanotetaan.

1. Valitse **OK**.

    **Ostotilausnro**-kenttä avautuu ja siinä on Työ valmis -sanoma.

    Nimike *A0001* on nyt vastaanotettu *VASTOT*-sijaintiin ja määritetty vaiheessa 10 annettuun klusterin tunnukseen.

1. Toista vaiheet 4–11 ostotilauksessa jäljellä olevien nimikkeiden vastaanottamiseen ja klusterin tunnukseen määrittämiseen:

    - Nimikkeen *A0002* määrä on *20*
    - Nimikkeen *M9215* määrä on *30*

#### <a name="close-the-cluster"></a>Klusterin sulkeminen

Klusteri on suljettava, ennen kuin klusterin nimikkeet voidaan hyllyttää.

1. Valitse Supply Chain Managementissa **Varastonhallinta \> Työ \> Lähtevä \> Työklusterit**.
1. Hae **Työklusterit**-sivun **Työklusteri**-osan **Klusterin tunnus** -kentässä aiemmin annetun klusterin tunnus.
1. Jos klusteri ei ole näkyvissä, se on ehkä jo suljettu. Voit selvittää, onko klusteri suljettu, valitsemalla **Näytä suljettu työ** -valintaruutu ja hakemalla aiemmin annettua klusterin tunnusta. Toimi sitten jonkin seuraavien vaiheiden mukaisesti:

    - Jos klusteri on suljettu, ohita tämän menettely jäljellä olevat vaiheet ja siirry seuraavaan menettelyyn [Klusterin hyllyttäminen](#put-the-cluster-away).
    - Jos klusteria ei ole suljettu, sulje klusteri manuaalisesti tämän menettelyjä jäljellä olevien ohjeiden mukaisesti. Siirry sitten seuraavaan menettelyyn.

1. Valitse **Työklusteri**-osassa aiemmin annettu klusterin tunnus.
1. Valitse toimintoruudussa **Sulje klusteri**.

    Kun klusteri on suljettu, se ei enää näy **Työklusteri**-osassa (ellei **Näytä suljettu työ** -valintaruutua ole valittuna).

#### <a name="put-the-cluster-away"></a>Klusterin hyllyttäminen

1. Kirjaudu varastonhallinnan mobiilisovellukseen käyttäjänä, joka on määritetty varastoon *61*.
1. Valitse päävalikossa **Saapuva**.
1. Valitse **Saapuva**-valikossa **Klusterihyllytys**.
1. Valitse **Klusterin tunnus** ja anna aiemmin annettu suljetun klusterin tunnus.
1. Valitse **OK**.

    **Klusterihyllytys: keräily** -sivu avautuu. Siinä näkyy klusterin tunnus, keräilysijainti, nimikkeet (näkyvissä on arvo *Useita*) ja klusterin kerättävä kokonaismäärä.

1. Valitse **OK**.

    **Klusterihyllytys: aseta** -sivu avautuu. **Aseta**-ohjeet määrittävät klusterin tunnuksen, asetussijainnin, nimikkeet, kokonaismäärän ja klusterissa vastaanotettujen nimikkeiden rekisterikilpitunnukset.

    Voit ohittaa tai hyväksyä tämän vaihtoehdon vakioasetuksilla.

    ![Klusterihyllytys: Aseta-sivu.](media/Cluster_putaway-Put.png "Klusterihyllytys: Aseta-sivu")

1. Vahvista klusterin hyllytys valitsemalla **OK**.

    Klusteri on valmis -sanoma tulee näkyviin.

## <a name="notes-and-tips"></a>Huomautuksia ja vihjeitä

Jos klusterin tunnuksesta tulee upotetun kuormalavan päärekisterikilpi, asetussijainti annetaan automaattisesti, kun klusterin tunnus skannataan. Muita rekisterikilpiä ei tarvitse skannata, vaikka rekisterikilven luonti olisi määritetty manuaaliseksi.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]