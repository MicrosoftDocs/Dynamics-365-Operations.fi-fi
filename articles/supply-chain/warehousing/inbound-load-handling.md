---
title: Ostotilausten saapuvien kuormien varastokäsittely
description: Tässä artikkelissa kuvataan ostotilausten saapuvien kuormien fyysisen varastoinnin käsittelyprosessi.
author: Mirzaab
ms.date: 03/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadTable, WHSLoadPlanningListPage, WHSLoadPlanningWorkbench, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-03-21
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 100b1972801f117560a5caf338a1ac640737ccdf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855929"
---
# <a name="warehouse-handling-of-inbound-loads-for-purchase-orders"></a>Ostotilausten saapuvien kuormien varastokäsittely

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan ostotilausten saapuvien kuormien fyysisen varastoinnin käsittelyprosessi.

Jokaisessa saapuvassa kuormassa järjestelmässä on jo oltava liittyvä myyntitilaus, ja se voi sisältää myös liittyvän kuormamäärityksen ja/tai kuljetussuunnitelman. Lisätietoja saapuvien kuormien luomisesta ja hallinnasta on kohdassa [Liiketoimintaprosessi: saapuvien kuormien kuljetusten suunnitteleminen](/dynamicsax-2012/appuser-itpro/business-process-planning-transportation-for-inbound-loads).

## <a name="overview-how-inbound-loads-are-created-registered-and-received"></a>Yleiskatsaus: miten saapuvat kuormat luodaan, kirjataan ja vastaanotetaan

Seuraavassa kuvassa näkyy tyypillinen kulku, jolla käsitellään saapuvia kuormia, joilla on ostotilausmääriä, kun ne saapuvat varastoosi.

![Saapuvan kuorman käsittelyprosessi.](media/inbound-process.png "Saapuvan kuorman käsittelyprosessi")

1. **Toimittaja vahvistaa ostotilauksen.**

    Prosessi alkaa, kun ostotilaus syötetään järjestelmään ja toimitetaan sitten toimittajalle, joka vahvistaa tilauksen. Ostotilauksen on oltava olemassa, ennen kuin voit luoda saapuvan kuorman tietueen. Voit kuitenkin luoda saapuvan kuorman, vaikka tilausta ei olisikaan vahvistettu. Lisätietoja on kohdassa [Hyväksy ja vahvista ostotilaukset](../procurement/purchase-order-approval-confirmation.md).

1. **Saapuvan kuorman tietue luodaan, jotta saapuminen ja sen sisältö voidaan suunnitella.**

    Saapuva kuormatietue edustaa yhden tai usean ostotilauksen toimittajan toimitusta. Kuorman odotetaan saapuvan varastoon yhtenä fyysisenä kuljetusyksikkönä (kuten rekkakuorma). Saapuvan kuorman tietuetta käytetään suunnittelutarkoituksiin, ja sen avulla logistiikkakoordinaattori voi seurata kuorman edistymistä toimittajalta. Sitä käytetään myös tilausrivimäärien rekisteröimiseen ja edistymisen hallintaan varaston työvaiheiden, kuten saapumisen ja hyllytyksen, kautta. Kuormat voidaan luoda joko automaattisesti tai manuaalisesti, ja ne voivat perustua joko ostotilaukseen tai toimittajan lähetysilmoitus (ASN) -lähetykseen. Lisätietoja on kohdassa [Saapuvan kuorman luominen tai muokkaaminen](/dynamicsax-2012/appuser-itpro/create-or-modify-an-inbound-load).

1. **Toimittaja vahvistaa kuorman lähetyksen.**

    Kun toimittaja lähettää kuorman, vastaanottavan varaston logistiikkakoordinaattori vahvistaa kuorman lähetyksen. Jos vastaanottava yritys käyttää **Kuljetuksen hallinta** -moduulia, saapuvien lähetysten vahvistus käynnistää muita saapuvaan kuormaan liittyviä kuormanhallintaprosesseja. Lisätietoja on kohdassa [Kuorman lähetyksen vahvistaminen](/dynamicsax-2012/appuser-itpro/confirm-a-load-for-shipping).

1. **Kuorma saapuu varastoon ja työntekijät rekisteröivät määriä.**

    Kun kuormalava saapuu varastoon vastaanottolaituriin, varastotyöntekijät rekisteröivät kuormamäärät. Kun **Varastonhallinta**-moduulia käytetään, työntekijät tekevät rekisteröitymisen käyttämällä mobiililaitteita. Lisätietoja on kohdassa [Tuotteen vastaanotto ostotilauksia vastaan - rekisteröinti](../procurement/product-receipt-against-purchase-orders.md#registration) ja [saapuvalle kuormalle saapuvien tuotemäärien rekisteröinti](#register-item-quantities-arriving) .

1. **Kirjatut kuormamäärät kirjataan ostotilauksiin.**

    Kun kuormamäärät on rekisteröity saapuneiksi, näiden määrien on oltava tuotteen vastaanotto, joka on kirjattava yrityksen varastokirjanpitoon fyysisen varaston lisäyksen kirjaamista varten. Lisätietoja on kohdassa [Tuotteen vastaanotto ostotilauksilla - tuotteen vastaanotto](../procurement/product-receipt-against-purchase-orders.md#product-receipt) ja [Kirjattujen tuotemäärien kirjaaminen ostotilauksiin](#post-registered-quantities).

## <a name="register-item-quantities-that-arrive-on-an-inbound-load"></a><a name="register-item-quantities-arriving"></a>Saapuvaan kuormaan saapuvien nimikemäärien rekisteröiminen

Microsoft Dynamics 365 Supply Chain Management tukee useita toiminnallisia lähestymistapoja tilattujen tuotteiden saapumisen kirjaamiseen. Tämän vuoksi voit määrittää järjestelmän vastaamaan tiettyjä liiketoiminnan vaatimuksia. Tässä osassa kuvataan saapuvien nimikkeiden määrien rekisteröiminen matkaviestimen avulla, kun järjestelmän laajennettu varastonhallinta on otettu käyttöön. On kuitenkin olemassa vaihtoehtoinen kulku, joka perustuu nimikkeen saapumisen kirjauskansioon mobiililaitteen asemesta. Lue lisätietoja tästä kulusta kohdasta [Rekisteröi nimikkeet erikoisvarastointikäyttöön tarkoitetuksi nimikkeiksi käyttäen nimikkeen saapumisen kirjauskansiota](tasks/register-items-advanced-warehousing.md).

Kun saapuva kuorma saapuu varastoon ensimmäisen kerran, varastotyöntekijöiden on rekisteröitävä lähetykseen sisältyvät nimikemäärät. Yleensä he käyttävät käsiskannereita. Tämä työnkulku on käytettävissä vain, jos järjestelmässä on seuraavat nimikkeet:

- **Saapuva kuormatietue, joka kuvaa lähetyksen odotettuja nimikemääriä**

    Yleensä toimittaja vahvistaa saapuvan kuorman tietueen, ennen kuin lähetys saapuu varastoon. Tämän vuoksi kuorman tila on _Toimitettu_. Varastotyöntekijät voivat kuitenkin myös rekisteröidä nimikkeiden määrän sellaisia kuormia varten, joiden tila on _Avoin_ tai _Vastaanotettu_.

- **Mobiililaitteen valikko, joka on määritetty tukemaan kuorman vastaanottoa**

    Mobiililaitteiden [varastonhallinnan mobiilisovellus](../warehousing/install-configure-warehouse-management-app.md) tukee seuraavia työn luomisprosesseja:

    - Kuorman nimikkeen vastaanotto
    - Kuorman nimikkeen vastaanotto ja poispano
    - Yhdistelmärekisterikilven vastaanotto, jossa **Lähdeasiakirjan rivin tunnistustapa** -kentän valikkonimikkeeksi mobiililaitteessa on määritetty _Lataa nimikkeen vastaanotto_. Lisätietoja on kohdassa [Yhdistelmärekisterikilven vastaanotto](mixed-license-plate-receiving.md).
    - Yhdistelmärekisterikilven vastaanotto ja hyllytys, jossa **Lähdeasiakirjan rivin tunnistustapa** -kentän valikkonimikkeeksi mobiililaitteessa on määritetty _Lataa nimikkeen vastaanotto_. Lisätietoja on kohdassa [Yhdistelmärekisterikilven vastaanotto](mixed-license-plate-receiving.md).

    > [!NOTE]
    > Prosessista riippumatta järjestelmä luo työn, joka ottaa vastaanottavaan sijaintiin kirjatut määrät ja hyllyttää ne tavalliseen tallennussijaintiin. Kun _kuormakohteen vastaanottoa ja hyllytystä_ tai _Yhdistelmärekisterikilven vastaanotto- ja hyllytys_ -prosessia käytetään, kuormamäärää rekisteröinyt työntekijä myös ohjaa laitteen suorittamaan laskutyön osana rekisteröintitehtävää. Sen sijaan _kuormanimikkeen vastaanotto_- ja _yhdistetyn rekisterikilven vastaanotto_ -prosesseille oletetaan, että hyllytystyöt tehdään erillään rekisteröitymistehtävästä.

- **Työmalli, jossa määritetään saapuvien kuormien keräilyyn ja käyttöön liittyvät työt**

    Tämä nimike liittyy edellisiin nimikkeisiin. _Ostotilauksen_ työtilaustyypille on oltava vähintään yksi työmalli, ja siinä on oltava joukko poiminnan/hyllytyksen työtyyppejä.

Mobiililaite ohjaa varaston vastaanottavan työntekijän kulun läpi kuorman määrän rekisteröintiä varten. Tämä kulku sisältää vähintään seuraavat vaiheet kullekin kuorman tunnukselle:

1. Syötä kuorman tunnus.
2. Kirjoittaa nimiketunnus saapuneelle nimikkeelle.
3. Kirjoita vastaanotetun nimiketunnuksen määrä.
4. Kirjoita nimikkeen alkusijainnin rekisterinumero, jos järjestelmää ei ole määritetty luomaan tätä numeroa automaattisesti.
5. Napauta **OK**.

Kun työntekijä on suorittanut nämä vaiheet, järjestelmä tekee seuraavat päivitykset asianmukaisiin yksiköihin edellyttäen, että ostotilausrivin määrä saapui yhteen kuormaan ja kaikki kuormamäärät on rekisteröity:

| Yksikkö | Päivitykset | Seteli |
|---|---|---|
| Kuorma | **Työn luontimäärä** -kenttä kuormarivillä päivitetään siten, että rekisteröity määrä näkyy. | **Kuorman tilan** arvona pysyy _toimitettu_ tai _avoin_, jos kuormalle ei ole suoritettu lähetyksen vahvistusta. Jos vähintään yksi hyllytystyön rivi on aloitettu, se muutetaan _työn alla_ -tilaksi. |
| Ostotilauksen varastotapahtuma, johon liittyvät kuormamäärät on rekisteröity |<p>Seuraavat kentät päivitetään:</p><ul><li><b>Vastaanotto</b>-kentän arvoksi määritetään <i>Rekisteröity.</i>.</li><li><b>Sijainti</b>-kenttään päivitetään vastaanottavan laiturin sijaintikoodi. (Tämä koodi määritetään kunkin varaston <b>oletusvastaanottosijainti</b> -kentässä.)</li><li><b>Rekisterikilpi</b>-kenttään lisätään rekisteröinnissä määritetty tai luotu rekisterinumero.</li><li><b>Kuorman tunnus</b> -kenttään päivitetään sen kuorman numero, johon määrä on rekisteröity. (Katso huomautus.)</li></ul> | Ostotilauksen varastotapahtuman ja kuormaa vasten rekisteröitävien määrien välinen yhteys otettiin käyttöön versiossa 10.0.9 valinnaisena ominaisuutena, jonka nimi oli _liitä ostotilauksen varastotapahtumat kuormaan_. Tämä ominaisuus on erityisen hyödyllinen operatiivisille kuluille, joissa yksi ostettujen tuotteiden tilaus toimitetaan useana kuormana, tai kun kuorma sisältää useiden ostotilausten määriä. |
| Varaston hyllytys | Työ luodaan työmallin perusteella, jotta työntekijä voi siirtää kirjatut määrät vastaanottosijainnista tavalliseen tallennussijaintiin. | Tallennuspaikan valintaa ohjataan hyllytyssijaintidirektiivissä. Jos sijaintidirektiiviä ei ole määritetty, työn hyllytyssijainti on tyhjä. |

Huomaa, että varastotyöntekijät voivat rekisteröidä ostotilauksen vastaanoton yhdellä tai useammalla siihen liitetyllä kuormalla käyttämättä _Lataa nimikkeen vastaanotto_ -prosessia. Käytettävissä ovat seuraavat menetelmät:

- **Mobiililaitteessa:** Käytä _ostotilausrivin vastaanotto_- ja _ostotilausrivin vastaanotto- ja hyllytys_ -prosesseja. (Jos ostotilausrivin määrälle on useampi kuin yksi kuorma, työntekijä ei voi käyttää _ostotilausrivin vastaanotto_ -prosessia. Sen sijaan työntekijää neuvotaan käyttämään laitetoimintoa, joka liittyy _kuorman kohteen vastaanotto_ -prosessiin.)
- **Asiakasohjelmassa:** Käytä nimikkeen saapumisen kirjauskansiota.
- **Asiakasohjelmassa:** Käytä **kirjaus** toimintoa, jota voi käyttää ostotilausriviltä.

> [!NOTE]
> Jos ostotilauksen vastaanotto rekisteröidään jollakin edellä olevista menetelmistä, ostotilauksen varastotapahtuman ja kuorman välille ei luoda linkkiä, vaikka _Liitä ostotilauksen varastotapahtumat, joissa on kuorma_ -ominaisuus on otettu käyttöön. Yksi poikkeus tähän sääntöön on, kun käytät **Ostotilausrivin vastaanotto** -vaihtoehtoa ja vain yhden kuorman tila tilausrivillä on muu kuin _Vastaanotettu_.

### <a name="handle-discrepancies-during-registration-of-inbound-load-quantities"></a>Käsittele ristiriidat saapuvien kuormamäärien rekisteröimisen aikana

Varastotyöntekijät voivat suorittaa osittaisen kuorman määrän vastaanoton rekisteröimisen. Kukin osittainen kuorman määrän kuitti luo sitten erillisen varastotapahtuman, jonka vastaanottotila on _rekisteröity_ rekisteröidylle määrälle, ja erätunnus viittaa alkuperäiseen ostotilausriviin.

#### <a name="load-under-receiving"></a>Kuorman alivastaanotto

Kun kuorma saapuu ja jos nimikemäärät ovat pienempiä kuin kuormatietueessa ilmoitettu määrä, varaston vastaanottohenkilökunta voi työskennellä suoraan asiakasohjelmassa ja kuitata tämän eron vähentämällä kuormarivien määrää siten, että se vastaa todellista ja rekisteröintiä varten määritettyä määrää.

#### <a name="load-over-receiving"></a><a name="load-over-receiving"></a>Kuorman ylivastaanotto

Ylivastaanotto tapahtuu kuorman saapuessa, ja nimikkeen määrät ylittävät odotetun kuormarivin määrän. Voit määrittää, onko ja missä määrin ylivastaanotto on sallittu kuorman rekisteröinnissä.

Voit määrittää, mitä tapahtuu, kun varastotyöntekijä yrittää rekisteröidä ylitoimituksen, käyttämällä kyseisen mobiililaitteen valikkovaihtoehtojen **kuorman ylivastaanotto** -kenttää. Tämä kenttä on käytettävissä mobiililaitteiden valikkokohteille, jotka käyttävät seuraavia työn luomisprosesseja:

- Kuorman nimikkeen vastaanotto
- Kuorman nimikkeen vastaanotto ja poispano
- Yhdistelmärekisterikilven vastaanotto, (kun **Lähdeasiakirjan rivin tunnistustapa** -kentän arvoksi on määritetty _Lataa nimikkeen vastaanotto_)
- Yhdistelmärekisterikilven vastaanotto ja hyllytys, (kun **Lähdeasiakirjan rivin tunnistustapa** -kentän arvoksi on määritetty _Lataa nimikkeen vastaanotto_)

Seuraavassa taulukossa kerrotaan **Kuorman ylivastaanotto** -kentän käytettävissä olevista vaihtoehdoista.

| Arvo | kuvaus |
|---|---|
| Salli | Työntekijät voivat rekisteröidä sellaisten määrien vastaanoton, jotka ylittävät valitun kuorman jäljellä olevan rekisteröimättömän määrän, mutta vain, jos rekisteröity kokonaismäärä ei ylitä kuormaan liittyvän ostotilausrivin määrää (ylitoimitusprosentti osuuden oikaisun jälkeen). |
| Esto | <p>Työntekijät eivät voi rekisteröidä sellaisten määrien vastaanottoa, jotka ylittävät jäljellä olevan rekisteröimättömän määrän valitulle kuormalle (ylioikaisuprosentin mukauttamisen jälkeen). Työntekijä, joka yrittää kirjata vastaanotot, saa virheilmoituksen eikä voi jatkaa, ennen kuin hän rekisteröi määrän, joka on yhtä suuri tai pienempi kuin jäljellä oleva rekisteröimätön kuormamäärä.</p><p>Oletusarvon mukaan kuormarivin ylitoimitusprosenttirivi kopioidaan siihen liittyvästä ostotilausrivistä. Kun <b>kuorman ylivastaanotto</b> -kentän arvoksi on asetettu <i>Estä</i>, järjestelmä käyttää ylitoimituksen prosenttiarvoa laskiessaan kokonaismäärän, joka voidaan kirjata kuormariville. Tämä arvo voidaan kuitenkin korvata yksittäisillä kuormilla tarpeen mukaan. Tämä toiminta on olennaista vastaanottokulkujen aikana, jolloin osa tai koko tilausrivin ylitoimitusprosenttia edustavasta ylimääräisestä määrästä jaetaan suhteessa useisiin kuormiin. Tässä on esimerkkiskenaario:</p><ul><li>Yhdelle ostotilausriville on useita kuormia.</li><li>Ostotilausrivin ylitoimitusprosentti on suurempi kuin 0 (nolla).</li><li>Määrät on jo rekisteröity yhtä tai useampaa kuormaa vasten ottamatta huomioon ylitoimituksen prosenttiosuutta.</li><li>Ylitoimitusmäärä saapuu viimeiseen kuormaan.</li></ul><p>Tässä skenaariossa mobiililaitteiden avulla voidaan rekisteröidä ylimääräkuorma vain, jos varastonvalvoja lisää asianmukaisen kuormarivin ylitoimitusprosentin oletusarvosta arvoon, joka on riittävän suuri, jotta koko ylitoimitus voidaan rekisteröidä lopullisessa kuormassa.</p> |
| Vain suljettujen kuormien esto | Työntekijät voivat vastaanottaa kuorman rivimääriä avokuormille, mutta ei kuormille, joiden tila on _vastaanotettu_. |

> [!NOTE]
> **Kuorman ylikuittaus** -kentän oletusarvo on _Salli_. Kun tätä arvoa käytetään, käyttäytyminen vastaa normaalia toimintaa, joka oli käytettävissä ennen _Kuorman määrien ylivastaanottaminen_ -ominaisuuden käyttöön ottamista versiossa 10.0.11.

### <a name="put-away-the-registered-quantities"></a>Kirjattujen määrien hyllytys

Kun mobiililaitteiden rekisteröiminen on valmis, _määrän vastaanoton kirjaus_ -toiminto päivittää varaston ja varastotietueiden määrän siten, että määrät ovat nyt vastaanottolaiturin sijainnissa ja käytettävissä varauksia varten. Yrityksen varastotoiminnot edellyttävät kuitenkin yleensä, että määrät siirretään vastaanottolaiturilta tavalliseen varastosäilöön, jotta seuraavat poimintaprosessit voivat toteutua. Hyllytyksen ohjeet siepataan hyllytystyössä, joka luodaan automaattisesti, kun saapuva kuorma kirjataan vastaanotetuksi.

Kun varastotyöntekijä on lopettanut hyllytystyön, järjestelmä kirjaa ja seuraa tulosta päivittämällä päivityksen useille yksiköille seuraavan taulukon yhteenvedon mukaisesti.

| Yksikkö | Päivitykset | Seteli |
|---|---|---|
| Kuorma | <p>Seuraavat kentät päivitetään:</p><ul><li><b>Kuorman tila</b> -arvo muutetaan <i>työn alla</i> -tilaksi.</li><li><b>Työn tilan</b> arvoksi muutetaan <i>100,00 % työstä valmiina</i>.</li></ul> | **Kuorman tilan arvo** muutetaan _Työn alla_ -tilaan, kun työntekijä käynnistää hyllytystehtävän vähintään yhdelle hyllytystyön riville. |
| Varastotapahtumat, joihin liittyvät määrät on hyllytetty | **Vastaanotto**- ja **Sijainti** -kentät sekä muut tarvittavat kentät päivitetään vastaamaan vastaanottosijainnin siirtoa tallennussijaintiin. | **Vastaanottotilan** ostotilauksen varastotapahtuman arvo säilyy tilassa _Rekisteröitynyt_. |
| Varaston hyllytys | **Työn tilan** arvoksi vaihtuu _Suljettu_. | |

## <a name="post-registered-product-quantities-against-purchase-orders"></a><a name="post-registered-quantities"></a>Lähetä kirjatut tuotemäärät ostotilauksia vastaan

Kun saapuvat tuotemäärät on rekisteröity järjestelmään, ne ovat käytettävissä varauksen yhteydessä myynnin ja muiden lähtevien ja sisäisten toimintojen yhteydessä. Järjestelmä ei kuitenkaan vielä päivitä varaston (väliaikaisia) tilejä. Tämä päivitys voi tapahtua vain, kun työryhmä kirjaa kirjatut tuotteen vastaanotot.

Jos haluat avata sivun, jossa he voivat kirjata tuotteen vastaanoton, työryhmän jäsenet voivat suorittaa _jonkin_ seuraavista vaiheista:

- Avaa haluamasi kuormatietue ja valitse sitten **Tuotteen vastaanotto** -toiminto.
- Siirry kohtaan **Varaston hallinta \> Kausittaiset tehtävät \> Päivitä tuotteen vastaanotot** ja määritä sitten **Kuorman tunnus** -kenttään kirjattava kuorma.
- Avaa haluamasi ostotilaus ja valitse sitten **Tuotteen vastaanotto** -toiminto.
- Mene kohtaan **Hankinta ja alihankinta \> Ostotilaukset \> Tuotteiden vastaanotto \> Lähetetään tuotteen vastaanottotyö**.

**Tuotteen vastaanotto** -toiminto, joka on käytettävissä **Kuorma** -sivulla (ja päivitystyön vastaavalla sivulla, **Päivitä tuotteen vastaanotot** -sivu), voi päivittää tuotteen vastaanottomäärät vain niiden ostotilausmäärien osalta, joiden tila on _rekisteröity_. **Tuotteen vastaanotto** -toiminto, joka on saatavilla **Ostotilaus**-sivulla voi kuitenkin käsittää sekä käsittelytilojen (_Tilattu_ ja _Rekisteröity_) määrät. Se voi myös ohjata tuotteen vastaanoton kirjauksen laajuutta lisäparametrien avulla, kuten _Vastaanota nyt määrä_ ja _Rekisteröity määrä ja palvelut_.

Ainoastaan tilaukset, joiden tila on _Vahvistettu_, voivat olla tuotteen vastaanotto -kirjattuja. Ei-vahvistettujen ostotilausten osalta **Tuotteen vastaanotto** -toimenpide ei ole käytettävissä.

### <a name="post-registered-quantities-from-the-load-page"></a>Kirjattujen määrien kirjaaminen kuormasivulta

Tuotteen vastaanottamiseen – kirjaa rekisteröidyt määrät **Kuorma**-sivulta, seuraavat edellytykset on otettava käyttöön:

- Kuormalla on oltava vähintään yksi määräyksikkö, jonka tila on _Rekisteröity_.
- Kuorman tilan tulee olla _Lähetetty_.
- Kuormaan liittyvän ostotilauksen tilan on oltava _Vahvistettu_.

> [!NOTE]
> Jos kuorman tilaksi ei ole määritetty _Lähetetty_, järjestelmä vahvistaa automaattisesti kuorman, ennen kuin se suorittaa tuotteen vastaanoton päivityksen. (Kuorman tilaksi asetetaan _Lähetetty_, kun käyttäjä rekisteröi kuorman saapuvan toimituksen.)

Tuotteen vastaanottoon – Kirjaa valittuun kuormaan liittyvät saapumisrekisteröinnit, työntekijä valitsee **Tuotteen vastaanotto** -toimenpiteen **Kuorma**-sivulta. Avatussa sivussa on seuraavat keskeiset tiedot:

- **Määrä**-kentän **Parametrit**-osan **Asetukset**-välilehdellä näkyy _Rekisteröity määrä_. Muita vaihtoehtoja ei ole käytettävissä tässä.
- **Yhteenveto**-pikavälilehden ruudukko sisältää kaikki valittuun kuormaan sisältyvät ostotilaukset.
- **Rivit**-pikavälilehden ruudukossa näkyvät kaikki tilausrivit, joilla on rekisteröity määrä.

> [!NOTE]
> **Rivi**-välilehdessä näkyvien tilausrivien määrät lasketaan eri tavalla sen mukaan, onko _Salli useiden tuotteiden vastaanotto kuorman mukaan_ -ominaisuus käytettävissä ja onko se otettu käyttöön Supply Chain Managementin omassa versiossa.
>
> | Versio | Laskenta |
> |---|---|
> | Versiot ennen versiota 10.0.10 ja uudemmat versiot, joissa _Usean tuotteen vastaanoton salliminen kuormatoimintoa kohden_ ei ole käytössä | Rivimäärä on _kyseisen ostotilausrivin_ kaikkien kirjattujen määrien kokonaissumma riippumatta siitä, tehdäänkö rekisteröinti useasta kuormasta, erillään kuormasta, mobiililaitteesta vai asiakkaan luota. |
> | Versio 10.0.10 ja uudemmat, joissa _Usean tuotteen vastaanoton salliminen kuormatoimintoa kohden_ on käytössä | Rivimäärä on kaikkien niiden _kuorma-tietueen_ kirjattujen määrien kokonaissumma, joista **Tuotteen vastaanoton kirjaus** -toimenpide aloitettiin. |

Kun käyttäjä valitsee **OK** vahvistaakseen tuotteen vastaanoton kirjauksen, järjestelmä tekee seuraavat avainpäivitykset asianmukaisille yksiköille.

| Yksikkö | Päivitykset |
|---|---|
| Sen ostotilauksen varastotapahtuma, jonka rivimäärät on sisällytetty kirjausalueeseen | <p>Seuraavat kentät päivitetään (mutta huomaa, että käytettävissä on myös useita muita päivityksiä):</p><ul><li><b>Vastaanotto</b>-kentän arvoksi määritetään <i>Vastaanotettu</i>.</li><li><b>Fyysinen päivämäärä</b> -kenttään päivitetään kirjauspäivämäärä.</li></ul> |
| Kuorma, josta käyttäjä on kirjannut tuotteen vastaanoton | Kuormien päivitykset määräytyvät käytettävän version ja **Salli usean tuotteen vastaanotto per kuorma** -kentän asetuksen mukaan. Säännöt on kuvattu jäljempänä tässä osassa näkyvässä taulukossa. |

**Salli useiden tuotteiden vastaanotto per kuorma** -kenttä antaa yritysten valita saapuvan kuorman vastaanottokäytännön. Yritykset voivat niiden operatiivisten kulkujen mukaan sallia tai estää usean tuotteen vastaanottokirjauksen lähettämisen samalle kuormalle. Suosittelemme, että logistiikkapäällikkö asettaa **Salli useiden tuotteiden vastaanotto per kuorma** -kentän arvoksi jonkin seuraavista arvoista:

- **Ei** – Valitse tämä arvo, jos varaston vastaanottotyöntekijät rekisteröivät aina kaikki tilausmäärät, jotka saapuvat kunkin kuorman mukana määritetyn aikajakson aikana. Jos yhtään kuormamäärää ei ole rekisteröity, järjestelmä olettaa, etteivät ne saavu perille tai että niitä ei ole ladattu, joten niitä ei tulisi pitää osana kuormaa. Kuormasta suoritettava tuotteen vastaanoton kirjaus käyttää samaa oletusta. Tuotteen vastaanoton lisäksi – kaikkien kirjattujen määrien päivittäminen (sen päätoiminto) se ilmoittaa, että kuorma on valmis ja suljettu lisäkäsittelyä varten. Tällöin kaikki kuorman rivimäärät päivitetään automaattisesti rekisteröidyille määrille, kuormariveille, joilla ei ole kirjattuja määriä, poistetaan ja kuorman tilaksi tulee _Vastaanotettu_.
- **Kyllä** – Valitse tämä arvo, jos varaston vastaanottohenkilöt vaativat enemmän aikaa rekisteröidäkseen kaikki saapuneen kuorman määrät, mutta sillä välin sinun on toimitettava tuotteen kuittaus määristä, jotka on jo rekisteröity. Tässä tapauksessa logistiikkapäällikkö haluaa pitää kuorman avoimena myös tuotteen vastaanoton kirjaustyön suorittamisen jälkeen, jolloin jäljellä olevat kuormamäärät voidaan kirjata ja tuotteen vastaanotto päivittää kirjanpitoon jatkuvasti.
- **Kehote** – Valitse tämä arvo, jos kuorman vastaanottokäytännöt sekoitetaan ja päätös on pakollinen aina, kun tuotteen vastaanoton kirjaus suoritetaan.

Seuraavassa taulukossa on yhteenveto **Salli usean tuotteen vastaanottaminen kuormaa kohti** -asetuksesta.

| Usean tuotteen vastaanoton salliminen kuormaa kohden | Kuorman määrä | Kuorman tila | Seteli |
|---|---|---|---|
| Kun tämä kenttä ei ole käytettävissä (vanhemmat versiot kuin 10.0.10) | <p>Kuorman määrä määritetään siten, että se on sama kuin rekisteröity määrä.</p><p>Jos kuorman määräksi on päivitetty 0 (nolla), mikä tarkoittaa, että rekisteröintiä ei ole tehty, kuormarivi poistetaan.</p><p>Jos kuormassa ei ole kuormalinjoja, kuorma poistetaan.</p> | _Vastaanotettu_ | Jos tilausrivin rekisteröidylle määrälle on useita kuormia, vain sen kuorman tila, josta vastaanotto kirjattiin, on päivitetty _vastaanotetuksi_. |
| Ei | <p>Kuorman määrä määritetään siten, että se on sama kuin kuorman tunnukseen liittyvä rekisteröity määrä.</p><p>Jos varastotapahtumalle ei ole rekisteröity kuormatunnusta, käyttäytyminen vastaa versioita ennen versiota 10.0.10.</p> | _Vastaanotettu_ | |
| Kyllä | Ei päivityksiä | _Vastaanotettu_, jos rekisteröity kokonaiskuormamäärä on yhtä suuri tai suurempi kuin kuormamäärä | |
| Kyllä | Ei päivityksiä | _Lähetetty_ tai _työn alla_, jos rekisteröity kokonaiskuormamäärä on vähemmän kuin kuormamäärä | |

Kun **Kuorman tila** -kentän arvoksi on määritetty _vastaanotettu_, kyseistä kuormaa varten ei voi tehdä enempää tuotteen vastaanoton kirjauksia. Työntekijä voi kuitenkin rekisteröidä jäljellä olevan tilausmäärän vastaanotetuksi kuormalle seuraavien ehtojen mukaisesti. (Lisätietoja on tämän artikkelin edellä olevassa osassa [Kuorman ylivastaanotto](#load-over-receiving).)

- Supply Chain Managementin versio on vanhempi kuin versio 10.0.11.
- _Kuormamäärien ylivastaanotto_ -toiminto on käytössä ja **kuorman määrän ylivastaanotto** -kentän mobiililaitteen valikkokohteen kuormakohteen vastaanottotoiminnoksi on asetettu _Salli_.

Tuotteen vastaanottokirjaus lisää rekisteröimiä kuormamääriä suhteessa kuormaan, jonka tila on _vastaanotettu_. käyttäjän on suoritettava kirjaustoimenpide liittyvästä ostotilauksesta.

### <a name="post-registered-quantities-from-the-purchase-order-page"></a>Kirjattujen määrien kirjaaminen ostotilaussivulta

Tuotteen vastaanottokirjauksen kirjatut määrät **Ostotilaus** -sivulta, käyttäjä suorittaa seuraavat tehtävät ennen **tuotteen vastaanotto** -toimenpiteen valitsemistoimintoa:

- Aseta **Määrä**-kentän **Parametrit**-osan **Asetukset**-välilehdellä arvoksi _Rekisteröity määrä_.
- Syötä **Tuotteen vastaanotto** -kenttään kirjaukseen sisältyvien ostotilausten numerot.

> [!NOTE]
> Rivimäärä, joka sisällytetään kirjausten tekoon on kyseisen ostotilausrivin kaikkien kirjattujen määrien kokonaissumma riippumatta siitä, tehdäänkö määrän rekisteröinti useasta kuormasta, erillään kuormasta, mobiililaitteesta vai asiakkaan luota. Sama sääntö pätee, kun tuotteen vastaanoton kirjaus suoritetaan kuormasta, jos se on valmis, jos **salli useiden tuotteiden vastaanotto per kuorma** -kenttä ei ole käytettävissä tai sitä ei ole otettu käyttöön.

Kun käyttäjä valitsee **OK** vahvistaakseen tuotteen vastaanoton kirjauksen, järjestelmä tekee seuraavat avainpäivitykset asianmukaisille yksiköille.

| Yksikkö | Päivitykset |
|---|---|
| Sen ostotilauksen varastotapahtuma, jonka rivimäärät on sisällytetty kirjausalueeseen | <p>Seuraavat kentät päivitetään (mutta huomaa, että käytettävissä on myös useita muita päivityksiä):</p><ul><li><b>Vastaanotto</b>-kentän arvoksi määritetään <i>Vastaanotettu</i>.</li><li><b>Fyysinen päivämäärä</b> -kenttä päivitetään päivämäärällä, jolloin tuotteen vastaanottopäivämäärä lähetetään.</li></ul> |
| Kuorma | Kuormien päivitykset riippuvat siitä, onko **Salli usean tuotteen vastaanotto kuormaa kohti** -kenttä käytettävissä ja käytössä. Säännöt on kuvattu seuraavassa taulukossa. |

Seuraavassa taulukossa on yhteenveto **Salli usean tuotteen vastaanottaminen kuormaa kohti** -asetuksesta.

| Salli useita tuotteen vastaanottoja kuormaa kohden | Kuorman määrä | Kuorman tila | Seteli |
|---|---|---|---|
| Kun tämä kenttä on joko poistettu käytöstä tai se ei ole käytettävissä (versioissa ennen 10.0.10) | Ei päivityksiä | Päivityksiä ei tehdä. ( Tila pysyy _avoimena_, _toimitettuna_ tai _käsittelyssä_.) | Koska tuotteen vastaanoton kirjaus aloitetaan ostotilauksesta, päivityslogiikalla ei ole tietoja sen vaikutusalueella olevien kirjattujen määrien välisestä liitosta eikä kuormista, joihin rekisteröinti on kirjattu. Näin ollen se ei voi valita kuormaa tilapäivitykseen. |
| Käytössä | Ei päivityksiä | <p>Yksi seuraavista toiminnoista tapahtuu:</p><ul><li>Tila vaihdetaan <i>vastaanotetuksi</i>, jos ostotilauksen varastotapahtumien saadut ja ostetut kokonaismäärät ovat suurempia tai yhtä suuret kuin niihin liittyvän kuorman määrä.</li><li>Tila pysyy <i>avoimena</i>, <i>toimitettuna</i> tai <i>käynnissä</i>, jos edellinen ehto ei täyty kaikkien kuorman rivien osalta.</li></ul> | |

### <a name="select-the-appropriate-product-receipt-posting-option-for-your-logistics-operations"></a>Valitse sopiva tuotteen vastaanoton kirjausvaihtoehto logistiikkatoimintojasi varten

Kuten aiemmin on kuvattu, järjestelmä tarjoaa kaksi tuotteen vastaanoton kirjausvaihtoehtoa. Vaihtoehtoja voi käyttää seuraavissa paikoissa:

- **Kuorma**-sivulla tai **Varaston hallinta \> Kausittaiset tehtävät** -valikosta päivitystyönä
- **Ostotilaus**-sivulla tai **Hankinta ja alihankinta \> ostotilaukset \>vastaanottavat tuotteet** -valikossa päivitystyönä

Yrityksiä, jotka käyttävät kuormia saapuvien tilausten kuljetusten ja varastonkäsittelyn suunnitteluun ja hallintaan, kehotetaan käyttämään seuraavia toimintoja, jotka on suunniteltu toimimaan kuormien kanssa:

- **Lataa nimikkeen vastaanottavat** toimenpiteet niiden fyysisen varastoinnin mobiililaitteisiin, rekisteröi tuotemäärän saapuminen kuormaa vastaan
- Kuormasta käynnistetyt **Tuotteen vastaanoton kirjaus** -toimenpiteet varastokirjanpidon päivittämiseksi

> [!NOTE]
> Muita määrän rekisteröimistä ja tuotteen vastaanoton kirjaustoimintoja voidaan käyttää vastaavien saapuvien operatiivisten prosessien tukemiseen. Jos kuitenkin käytät niitä muiden kuin erillisten kuormaan kohdistettujen toimintojen kanssa tai niiden asemesta, saatat vaarantaa kuormatietojen tarkkuuden ja näin ollen kuorman hallintakulun sopimattomuudet.

## <a name="example-scenarios"></a>Esimerkkiskenaariot

### <a name="prepare-your-system-to-run-the-sample-scenarios"></a>Valmistele järjestelmä malliskenaarioiden suorittamista varten

Jos haluat käsitellä tässä osassa kuvattuja esimerkkiskenaarioita, sinun on ensin varmistettava, että kaikki vaaditut ominaisuudet ovat käytössä järjestelmässä. Tarvittavien demotietojen on myös oltava käytettävissä järjestelmässä.

#### <a name="turn-on-the-required-features"></a>Tarvittavien ominaisuuksien ottaminen käyttöön

Nämä skenaariot edellyttävät _Useita tuotteen vastaanoton kirjauksia kuormaa kohti_ -ominaisuutta ja sen edellytysominaisuutta. Järjestelmänvalvojat voivat ottaa nämä ominaisuudet käyttöön noudattamalla näitä ohjeita.

1. Avaa **Ominaisuuksien hallinta** -työtila. (Lisätietoja tämän työtilan määrittämisestä ja käyttämisestä on kohdassa [Ominaisuuksien hallinnan yleiskuvaus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).)

1. Varmista, että _Ostotilauksen varastotapahtumien liittäminen kuormaan_ -ominaisuus on otettu käyttöön. Supply Chain Managementin versiosta 10.0.21 alkaen tämä ominaisuus on pakollinen, joten se on oletusarvoisesti otettu käyttöön eikä sitä poistaa uudelleen käytöstä. Ominaisuus on kuitenkin edelleen mainittu [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) seuraavasti:

    - **Moduuli:** _Varastonhallinta_
    - **Ominaisuuden nimi:** _Ostotilauksen varastotapahtumien yhdistäminen kuormalla_

1. Ota käyttöön _Useita tuotteen vastaanoton kirjauksia kuormaan_ -ominaisuutta kohden, joka on lueteltu seuraavalla tavalla:

    - **Moduuli:** _Varastonhallinta_
    - **Ominaisuuden nimi:**_Useita tuotteen vastaanoton kirjauksia kuormaa kohden_

#### <a name="enable-sample-data"></a>Mallitietojen ottaminen käyttöön

Näiden skenaarioiden käyttäminen määritettyjen mallitietojen ja -arvojen avulla edellyttää, että käytössä on järjestelmä, johon vakiodemotiedot on asennettu. Sinun on myös valittava **USMF**-yritys ennen aloittamista.

#### <a name="add-a-menu-item-for-receiving-load-items-when-a-mobile-device-is-used"></a>Valikon vaihtoehdon lisääminen kuormakohteiden vastaanottamista varten käytettäessä mobiililaitetta

Ennen kuin varaston vastaanottohenkilöt voivat käyttää mobiililaitetta, joka rekisteröi kuormaan linkitetyn saapuvan varaston, sinun on luotava tähän tarkoitukseen mobiililaitteen valikkovaihtoehto.

Tässä osassa luodaan mobiililaitteen valikkovaihtoehto ja lisätään se aiemmin luotuun valikkoon. Varastotyöntekijä voi sitten valita valikkovaihtoehdon varastonhallinnan mobiilisovelluksesta.

1. Siirry kohtaan **Varaston hallinta \>Asetukset \>Mobiililaite \> Mobiililaitteiden valikkokohteet** ja varmista, että mobiililaitteesi valikossa on valikkovaihtoehto, jolla on seuraavat asetukset:

    - **Tila:** _Työ_
    - **Työn luomisprosessi:**_Lataa nimikkeen vastaanotto_
    - **Luo rekisterikilpi:** _Kyllä_

    Voit jättää kaikki muut asetukset oletusarvoihinsa.

    ![Mobiililaitteen valikkovaihtoehtoasetukset.](media/inbound-mobile-menu-items.png "Mobiililaitteen valikkovaihtoehtoasetukset")

    Lisätietoja mobiililaitteiden valikkokohteiden määrittämisestä on kohdassa [Mobiililaitteiden määrittäminen varastotyötä varten](configure-mobile-devices-warehouse.md).

2. Kun olet määrittänyt valikkokohteen, siirry kohtaan **Varaston hallinta \> Asetukset \> Mobiililaite \> Mobiililaitteiden valikkokohteet** ja lisää se mobiililaitteesi valikkorakenteeseen.

### <a name="example-scenario-1-register-a-load-where-some-items-are-missing"></a>Esimerkkiskenaario 1: Rekisteröi kuorma, josta puuttuu nimikkeitä

Tämä skenaario näyttää, miten määrät rekisteröidään saapuvaan kuormaan, jossa kaikki odotetut määrät eivät ole käytettävissä. Sen jälkeen se näyttää, miten ostotilauksen tuotteen vastaanotto kirjataan.

#### <a name="create-a-load-to-plan-receipt-of-a-purchase-order"></a>Kuorman luominen ostotilauksen vastaanottoa varten

Tässä menettelyssä luodaan manuaalisesti ostotilaus ja siihen liittyvä kuorma. Tämän jälkeen voit päivittää kuorman simuloimaan, että se on lähetetty toimittajalta (joka päivittää kuorman tilan). Varastosuunnittelijat voivat suodattaa kuormat **kuorman tilan** mukaan ja etsiä odotettavissa olevat saapuvat kuormat.

1. Siirry kohtaan **Hankinta ja alihankinta \> Ostotilaukset \> Kaikki ostotilaukset**.
1. Valitse **Uusi**.
1. Määritä **luo ostotilaus** -valintaikkunassa **Toimittajatili**-kentän arvoksi _1001_.
1. Valitse **OK** sulkeaksesi valintaikkunan ja luodaksesi ostotilauksen.
1. Uusi ostotilaus sisältää jo **Ostotilausrivien** mukaisen rivin. Määritä seuraavat tämän rivin arvot:

    - **Nimiketunnus:** _A0001_
    - **Varasto**: _24_
    - **Määrä** _10_

1. Valitse toimintoruudun **Osto**-välilehdessä **Toiminnot \> Vahvista**. Tilauksen tila on nyt _Vahvistettu_.
1. Valitse toimintoruudun **Varasto**-välilehdessä **Toiminnot \> Kuormasuunnittelun työtila**.
1. Valitse **Kuormasuunnittelun työtila** -sivun toimintoruudun **Tarjonta ja kysyntä** -välilehdestä **Lisää \> Uuteen kuormaan**.
1. Määritä **Lataa mallin määritys** -valintaikkunassa **Lataa mallin tunnus** -kentän arvoksi _20 kontti_.
1. Valitse **OK** sulkeaksesi valintaikkunan ja palataksesi työtilaan.
1. Avaa juuri luotu kuorma valitsemalla **Kuormat**-osassa **Kuorman tunnus**.
1. Tarkista kuorman otsikko ja rivin tiedot ja huomaa seuraavat seikat:

    - **Kuorma**-pikavälilehden **Kuorman tila** -kentän arvoksi tulee _Avoin_.
    - **Kuormarivit**-osassa on yksi rivi, jolla **Määrä** -kentän arvoksi on asetettu _10_ ja **Työn luontimäärä** -kentän arvoksi on määritetty _0_ (nolla).

    ![Kuorman tiedot.](media/inbound-load-details.png "Kuorman tiedot")

1. Valitse toimintoruudun **Lähetä ja vastaanota** -välilehdellä **Vahvista \> Saapuva lähetys**. Huomaa, että **Kuorman tilaksi** on vaihdettu _Toimitettu_.
1. Merkitse **Kuorman tunnuksen** arvo muistiin, jotta voit käyttää sitä seuraavassa menettelyssä.

#### <a name="register-receipt-of-the-quantities-that-arrived-on-the-load"></a>Kuormassa varastoon saapuneiden määrien rekisteröiminen

Kun kuorma saapuu varastoon vastaanottolaiturilla, vastaanottava työntekijä rekisteröi mobiililaitteella kuorman määrät.

1. Kirjaudu varastoon 24 käyttämällä mobiililaitettasi. (Kirjaudu standardidemotiedoissa sisään käyttämällä numeroa _24_ käyttäjätunnuksena ja numeroa _1_ salasanana.)
1. Valitse tätä skenaariota varten luomasi _Kuormanimikkeen vastaanotto_ -valikkovaihtoehto.
1. Syötä seuraavat arvot noudattamalla näyttöön tulevia tietojen syöttöohjeita. (Järjestys voi vaihdella käyttämästäsi mobiililaitteesta tai emulaattorista riippuen.)

    - **Kuorma** – Anna edellisessä menettelyssä luomasi kuorman tunnus.
    - **Nimike** – Syötä _A0001_, joka on tähän kuormaan odotettu nimike.
    - **Määrä** – Kirjoita _9_ kuorman todellisena määränä. Huomaa, että tämä määrä on pienempi kuin odotettu määrä.

1. Jatka työnkulkua ja jätä kaikki muut kentät tyhjiksi tai aseta ne oletusarvoihin, kunnes laite ilmoittaa, että työ on päättynyt.

Kuorman vastaanottotehtävä on nyt saatu valmiiksi, ja vastaanottava työntekijä voi siirtyä seuraavaan tehtävään. Varaston vastaanottohenkilökunta tarkistaa kuitenkin kuormatietueen ja näkee, että vastaanotettu määrä oli odotettua pienempi. Tämän jälkeen he voivat tehdä seuraavat toimet verkkoasiakasohjelman avulla.

1. Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.
1. Etsi luettelosta juuri saamasi kuorma. (Sinun on ehkä valittava **Näytä suljettu** -valintaruutu, jos haluat sisällyttää saapuvat kuormat, joiden kuormatila on _Toimitettu_.) Avaa sitten kuorma valitsemalla linkki **Kuorman tunnus** -sarakkeesta.
1. Huomaa kuormatietueessa, että **Kuorman tilan** arvona pysyy _Toimitettu_, mutta kuormarivin **Työn luoma määrä** -arvo on muutettu arvoksi _9_.
1. Siirry kohtaan **Hankinta ja alihankinta \> Ostotilaukset \> Kaikki ostotilaukset**.
1. Etsi luettelosta juuri saamasi ostotilaus ja avaa sitten tilaus valitsemalla linkki **Ostotilaus**-sarakkeesta.
\
1. Valitse **Ostotilausrivit** -pikavälilehdessä **Varasto \> Näkymä \> Tapahtumat**.
1. Tarkista kahden ostotilaustapahtuman tiedot. (Sinun on ehkä mukautettava **Varasto tapahtumat** -sivua, jotta ruudukon **Kuorman tunnus** -kenttä tulee näkyviin.) Sinun pitäisi nähdä kaksi tapahtumaa:

    - Tapahtuma, jonka vastaanotto on _Rekisteröity_-tilassa, vastaa tiettyä kuormaa koskevaa määrää _9_ mobiililaitteen avulla. **Kuorman tunnus** liittyy kyseiseen tapahtumaan.
    - Tapahtuma, jolla on vastaanotto _Tilattu_ -tilassa, vastaa jäljellä olevaa rekisteröimätöntä tilausrivin määrää _1_.

#### <a name="product-receiptpost-the-registered-load-quantities-against-purchase-orders"></a>Tuotteen vastaanotto - Lähetä kirjatut kuormamäärät ostotilauksia vastaan.

Tässä menetelmässä lähetät tuotteen vastaanoton – kirjaa luettelo, jonka olet rekisteröinyt kuormaan. Näin ollen vastaanotettu varasto ja siihen liittyvät kustannukset lisätään yrityksen kirjanpitoon.

1. Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.
1. Etsi luettelosta saamasi kuorma. (Sinun on ehkä valittava **Näytä suljettu** -valintaruutu, jos haluat sisällyttää saapuvat kuormat, joiden kuormatila on _Toimitettu_.) Avaa sitten kuorma valitsemalla linkki **Kuorman tunnus** -sarakkeesta.
1. Valitse toimintoruudun **Lähetä ja vastaanota** -välilehdellä **Vastaanota \> Tuotteen kuittaus**. Jos järjestelmä pyytää vahvistamaan valinnan, valitse **Kyllä**.
1. Tarkista ruudukko **Tuotteen vastaanottokirjaus** -valintaikkunan **Rivit** -pikavälilehdessä. Sinun pitäisi nähdä ostotilausrivi, jolle määrä on rekisteröity valittua kuormaa vasten.

    > [!NOTE]
    > Sellaisissa versioissa, joissa _Useita tuotteen vastaanoton kirjauksia kuormaa kohden_ -toiminto ei ole käytettävissä tai ei ole käytössä, **Kuormarivien** ruudukossa näkyvä oletusmäärä on kaikkien ostotilausriviin liittyvien kuormien mukainen kokonaismäärä.

1. Tarkista ruudukko **Yleiskatsaus**-pikavälilehden **Tuotteen vastaanottokirjaus** -kentässä. Huomaa, että sen arvoksi määritetään numero, joka sisältää valitun kuorman tunnuksen.
1. Valitse **OK**, kun haluat kirjata tuotteen vastaanoton ja sulkea **Tuotteen vastaanoton kirjaus** -valintaikkunan.
1. Palaat kuormatietoihin. Huomaa seuraavat seikat:

    - **Kuorman tila** -kentän arvoksi on nyt määritetty _Vastaanotettu_.
    - Kuormarivillä **Määrä**-arvo on muuttunut _10_:stä _9_:ään kappaleeseen vastaamaan rekisteröityä määrää, mutta **Työn luoman määrän** arvo säilyy lukuna _9_.

Jos ostoryhmä ei odota, että toimittaja toimittaa jäljellä olevan tilauksen määrän 1, se voi lopettaa tilauksen päivittämällä rivin toimituksen jäljellä olevaksi arvoksi _0_. Jos kuitenkin havaitaan, että puuttuva kappale saapui alkuperäiseen kuormaan, varaston henkilöstö voi tehdä jonkin seuraavista toimista:

- Rekisteröi määrä samalle kuormalle. Tässä tapauksessa **Kuorman tila** -kentän arvo palautetaan _Toimitetuksi_ ja **Työn luoman määrän** arvoksi päivittyy _10_. Tämä valinta on käytettävissä vain seuraavissa tilanteissa:

    - _Kuormamäärien ylivastaanottaminen_ -toiminto ei ole käytettävissä, tai se ei ole käytössä.
    - _Kuormamäärien ylivastaanottaminen_ -ominaisuus on käytettävissä ja käytössä **Kuormarivin määrän ylivastaanotto** -kentän arvoksi on määritetty _Salli_.

- Lisää määrä uuteen tai olemassa olevaan kuormaan ja käsittele se tavalliseen tapaan.
- Rekisteröi ja/tai vastaanota määrä tavalla, johon ei liity kuorman käsittelyä.

### <a name="example-scenario-2-register-quantities-that-arrive-on-multiple-inbound-loads-where-some-items-are-missing"></a>Esimerkkiskenaario 2: useiden saapuviin kuormiin saapuvien määrien rekisteröiminen, kun nimikkeitä puuttuu

Tässä skenaariossa yksittäiseen ostotilausriviin liittyvä saapuva toimitus jaetaan kahteen kuormaan. Esimerkiksi ostotilausrivi voidaan jakaa useaan kuormaan painon ja/tai tilavuuden fyysisten kuormarajoitusten vuoksi.

Tämä skenaario osoittaa myös, miten useita tuotteen vastaanoton kirjauksia käsitellään samalle kuormille. Useille saapuville kuormille saapuvat määrät rekisteröidään, mutta määrät eivät vastaa odotettuja määriä. Tuotteen vastaanoton kirjauksen kautta tapahtuvat kustannuspäivitykset tehdään samaan kuormaan useita kertoja.

#### <a name="set-up-load-receiving-policies"></a>Kuorman vastaanottokäytäntöjen määrittäminen

Tässä menettelyssä otetaan käyttöön useita tuotteen vastaanoton kirjauksia samasta kuormasta.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Varastonhallinnan parametrit**.
1. Määritä **Kuormat**-välilehdessä **Salli useiden tuotteiden vastaanotto per kuorma** -kentän arvoksi _Kyllä_.

#### <a name="create-two-loads-to-plan-receipt-of-a-purchase-order"></a>Kahden kuorman luominen ostotilauksen vastaanottoa varten

Tässä menettelyssä luodaan ostotilaus ja kaksi kuormaa. Tämän jälkeen voit manuaalisesti päivittää kunkin kuorman simuloimaan, että sen on lähettänyt toimittaja (joka päivittää kuorman tilan). Varastosuunnittelijat voivat suodattaa kuormat **kuorman tilan** mukaan ja etsiä odotettavissa olevat saapuvat kuormat.

Opit myös määrittämään ostotilausrivin, jotta voit vastaanottaa määrän, joka on 20 prosenttia suurempi kuin riville määritetty määrä.

1. Siirry kohtaan **Hankinta ja alihankinta \> Ostotilaukset \> Kaikki ostotilaukset**.
1. Valitse **Uusi**.
1. Määritä **Toimittaja**-pikavälilehdessä **Toimittajatili**-kentän arvoksi _1001_ ja valitse sitten **OK**.
1. Uusi ostotilaus avataan ja se sisältää tyhjän rivin **Ostotilausrivien** ruudukossa. Määritä seuraavat tämän tilausrivin arvot:

    - **Nimiketunnus:** _A0001_
    - **Varasto**: _24_
    - **Määrä** _10_

1. Määritä **Rivitiedot** -pikavälilehden **Toimitus**-välilehdessä **Ylitoimitus**-kentän arvoksi _20_.
1. Valitse toimintoruudun **Osto**-välilehdessä **Toiminnot \> Vahvista**. Tilauksen tila on nyt _Vahvistettu_.
1. Valitse toimintoruudun **Varasto**-välilehdessä **Toiminnot \> Kuormasuunnittelun työtila**.
1. Valitse **Kuormasuunnittelun työtila** -sivun toimintoruudun **Tarjonta ja kysyntä** -välilehdestä **Lisää \> Uuteen kuormaan**.
1. Määritä **Lataa mallin määritys** -valintaikkunassa **Lataa mallin tunnus** -kentän arvoksi _20 kontti_. Muuta **Tiedot**-välilehdessä **Määrä**-arvoa _10_ - _5_, jos haluat osittain lisätä ostotilausrivin määrän.
1. Ota asetukset käyttöön valitsemalla **OK** ja sulje valintaikkuna.
1. Luo toinen kuorma toistamalla vaiheet 8 - 10. Tällä kertaa **Määrä**-kentän arvoksi on jo asetettu _5_.
1. Valitse **Kuormien suunnittelu -työtila** -sivun **Kuormat**-ruudukosta ensimmäisen luomasi **Kuorman tunnus**. **Lataa tiedot** -sivu tulee näkyviin ja näyttää valitun kuorman. Noudata näitä ohjeita:

    1. Valitse toimintoruudun **Lähetä ja vastaanota** -välilehdellä **Vahvista \> Saapuva lähetys**.
    1. Huomaa, että **Kuorman tilan** arvo on vaihdettu arvoksi _Toimitettu_.
    1. Palaa **Kuormasuunnittelun työtila** -sivulle valitsemalla sulkemispainike.

1. Toista edellinen vaihe luomasi toisen kuorman osalta.
1. Merkitse muistiin kaksi **Kuorman tunnus** arvoa, jotka näkyvät **Kuormat**-ruudukossa.

#### <a name="register-partial-receipt-of-the-quantities-that-arrived-on-the-first-load-and-post-the-registered-load-quantities"></a>Rekisteröi ensimmäiseen kuormaan saapuneiden määrien osittainen vastaanotto ja kirjaa rekisteröidyt kuormamäärät

Kun kuormat saapuvat varastoon vastaanottolaiturilla, vastaanottava työntekijä rekisteröi mobiililaitteella kuorman määrät. Kuormaan linkitetty rekisteröity varasto on sitten kustannuspäivitys yrityksen kirjanpidossa kirjaamalla ostotilauksen tuotteen vastaanoton kuorman perusteella.

Tämä menettely osoittaa, miten vastaanottava työntekijä rekisteröi kuormamäärät mobiililaitteeseen.

1. Kirjaudu varastoon 24 käyttämällä mobiililaitettasi. (Kirjaudu standardidemotiedoissa sisään käyttämällä numeroa _24_ käyttäjätunnuksena ja numeroa _1_ salasanana.)
1. Valitse tätä skenaariota varten luomasi _Kuormanimikkeen vastaanotto_ -valikkovaihtoehto.
1. Syötä seuraavat arvot noudattamalla näyttöön tulevia tietojen syöttöohjeita. (Järjestys voi vaihdella käyttämästäsi mobiililaitteesta tai emulaattorista riippuen.)

    - **Kuorma** – Anna edellisessä menettelyssä luomasi ensimmäinen kuorman tunnus.
    - **Nimike** – Syötä _A0001_, joka on tähän kuormaan odotettu nimike.
    - **Määrä** – Syötä _3_. Huomaa, että tämä määrä on pienempi kuin odotettu määrä. Tässä skenaariossa oletetaan, että sinulla ei ole aikaa rekisteröidä kaikkia tämän kuorman määriä. Myöhemmin tässä menettelyssä muut kappaleet rekisteröidään toistamalla tämä vaihe ja määrittämällä **Määrä** -kentän arvoksi _2_.

1. Jatka työnkulkua ja jätä kaikki muut kentät tyhjiksi tai aseta ne oletusarvoihin, kunnes laite ilmoittaa, että työ on päättynyt.
1. Siirry verkkoasiakasohjelmassa kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.
1. Etsi juuri saamasi kuorma luettelosta ja valitse **Kuorman tunnus** -arvo, joka avaa kuorman. Huomaa, että **Kuorman tilan** arvona pysyy _Toimitettu_, mutta kuormarivin **Työn luoma määrä** -arvo on muutettu arvoksi _3_.
1. Valitse toimintoruudun **Lähetä ja vastaanota** -välilehdellä **Vastaanota \> Tuotteen kuittaus**. Jos järjestelmä pyytää vahvistamaan valinnan, valitse **Kyllä**.
1. Tarkista, ettet muuta näkyvissä olevia arvoja **Kirjaustuotteen vastaanotto** -valintaikkunassa, ja valitse sitten **OK**.
1. Palaat **Kuorman tiedot** -sivulle valittua kuormaa varten. Huomaa seuraavat seikat:

    - **Kuorman tila** -kentän arvona pysyy määritetty _Lähetetty_.
    - Kuormarivillä kuorman **Määrän** arvo on _5_ kpl, mikä on alkuperäinen kuormamäärä, ja **työn luoman määrän** arvo säilyy lukuna _3_.

1. Viimeistele tämän kuorman jäljellä olevan määrän rekisteröiminen toistamalla tämä menettely. Määritä kuitenkin vaiheessa 3 **Määrä**-kentän arvoksi _2_.

Ensimmäisen kuorman vastaanottava tehtävä on nyt saatu valmiiksi. Kaksi tuotteen vastaanottokirjauskansiota on luotu, toinen kutakin suorittamiasi tuotteen vastaanoton päivityksiä varten.

#### <a name="register-receipt-of-the-quantities-that-arrived-on-the-second-load-and-account-for-the-overdelivered-quantity"></a>Rekisteröi toiseen kuormaan saapuneiden määrien vastaanotto ja ylitoimitetun määrän tili

Tässä skenaariossa vastaanottava virkailija rekisteröi määrän, joka on suurempi kuin kuorman määrä. Ylivastaanotto sallitaan, koska järjestelmä on määritetty sallimaan ylitoimitus.

1. Kirjaudu varastoon 24 käyttämällä mobiililaitettasi. (Kirjaudu standardidemotiedoissa sisään käyttämällä numeroa _24_ käyttäjätunnuksena ja numeroa _1_ salasanana.)
1. Valitse tätä skenaariota varten luomasi _Kuormanimikkeen vastaanotto_ -valikkovaihtoehto.
1. Syötä seuraavat arvot noudattamalla näyttöön tulevia tietojen syöttöohjeita. (Järjestys voi vaihdella käyttämästäsi mobiililaitteesta tai emulaattorista riippuen.)

    - **Kuorma** – Anna toinen aiemmin luomasi kuormatunnus.
    - **Nimike** – Syötä _A0001_, joka on tähän kuormaan odotettu nimike.
    - **Määrä** – Syötä _7_, joka on jäljellä oleva määrä, jonka toimittaja on valtuutettu toimittamaan osana ostotilauksen kokonaismäärää 12 (jossa 10 on alkuperäisen tilauksen määrä ja 2 on 20 prosentin sallittu ylitoimitusmäärä). Muista, että viisi kpl:tta on jo rekisteröity ensimmäistä kuormaa vasten.

Toinen kuorma on nyt päivitetty määrällä 7 ja se voi olla tuotteen vastaanotto-päivitetty tämän määrän perusteella.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]