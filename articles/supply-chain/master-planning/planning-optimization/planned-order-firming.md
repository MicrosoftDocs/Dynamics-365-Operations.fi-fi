---
title: Vahvista suunnitellut tilaukset
description: Tässä ohjeaiheessa kerrotaan, miten suunnitellut tilaukset voidaan vahvistaa. Kun suunnitellut tilaukset vahvistetaan, ne muunnetaan varsinaisiksi osto-, siirto- tai tuotantotilauksiksi.
author: ChristianRytt
ms.date: 04/22/2021
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 7e3a86e2aa0e7182f7f9e853b9e8667e677a8ad6
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/09/2022
ms.locfileid: "8102710"
---
# <a name="firm-planned-orders"></a>Vahvista suunnitellut tilaukset

[!include [banner](../../includes/banner.md)]

Suunnitellut tilaukset on *vahvistettava* (vapauttava) pääsuunnitteluprosessin osana. Kun suunnitellut tilaukset vahvistetaan, ne muunnetaan varsinaisiksi osto-, siirto- tai tuotantotilauksiksi. Nämä tilaukset tunnetaan myös nimellä *vapautetut tilaukset* tai *avoimet tilaukset*.

Suunniteltuja tilauksia voi vahvistaa kolmella tavalla:

- **Manuaalinen vahvistaminen** – Valitse tietyt suunnitellut tilaukset luettelosta ja aloita prosessi manuaalisesti.
- **Automaattinen vahvistus** – Määritä kattavuusryhmien, yksittäisten nimikkeiden ja nimike- ja pääsuunnitelmien yhdistelmien vahvistamisen oletusaikaraja. Tällöin pääsuunnittelun ajon aikana suunnitellut tilaukset vahvistetaan automaattisesti, jos tilauspäivä on määritetyn vahvistamisen aikarajan sisällä.
- **Kyselypohjainen vahvistaminen** – Määritä kysely, jossa valitaan suunnitellut tilaukset niiden ominaisuuksien mukaan. Voit määrittää erätyön, joka suorittaa kyselyn ja vahvistaa täsmäytystilaukset säännöllisesti.

Tässä aiheessa kuvataan kutakin menetelmää yksityiskohtaisesti.

## <a name="enable-the-features-that-are-described-in-this-topic"></a><a name="enable-features"></a>Tässä ohjeaiheessa kuvattujen ominaisuuksien ottaminen käyttöön

Useimmat suunnitellut tilaustoiminnot ovat käytettävissä kaikissa Microsoft Dynamics 365 Supply Chain Managementin vakioasennuksissa, joissa käytetään suunnittelun optimointia. Joitakin tässä ohjeaiheessa kuvatuista ominaisuuksista on kuitenkin otettava käyttöön ominaisuuksien hallinnassa, ennen kuin niitä voi käyttää.

### <a name="turn-parallelized-firming-of-planned-orders-on-or-off"></a>Suunniteltujen tilausten rinnakkaisen vahvistuksen ottaminen käyttöön tai käytöstä poistaminen

Rinnakkainen vahvistus nopeuttaa vahvistusprosessia rinnakkaistamalla sen useissa säikeissä. Tämä menetelmä voi olla hyödyllinen, kun useita suunniteltuja tilauksia vahvistetaan. Tämän toiminnon käyttö edellyttää, että järjestelmässä on käytössä *Suunniteltujen tilausten rinnakkainen vahvistaminen* -toiminto. Supply Chain Managementin versiosta 10.0.21 alkaen tämä ominaisuus on poistettu oletusarvoisesti käytöstä. Supply Chain Managementin versiosta 10.0.25 alkaen tämä toiminto on pakollinen, eikä sitä voi poistaa käytöstä. Jos käytät vanhempaa versiota kuin 10.0.25, voit ottaa tämän toiminnon käyttöön tai pois käytöstä hakemalla [Toimintojen hallinnasta](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) toimintoa *Suunniteltujen tilausten rinnakkainen vahvistaminen*.

### <a name="enable-planned-order-firming-with-filtering"></a>Ota suunniteltujen tilausten vahvistaminen käyttöön suodatuksen avulla

Suunniteltujen tilausten vahvistaminen suodatuksella mahdollistaa loogisten ehtojen määrittämisen sen valitsemiseksi, mitkä suunnitellut tilaukset haluat vahvistaa. Voit myös esikatsella valittuja suunniteltuja tilauksia, suorittaa prosessin taustalla ja/tai ajoittaa sen erätyönä.

Supply Chain Managementin versiosta 10.0.25 alkaen tämä ominaisuus on poistettu oletusarvoisesti käytöstä. Järjestelmänvalvojat voivat ottaa tämän toiminnon käyttöön tai pois käytöstä hakemalla *Suunnitellun tilauksen vahvistaminen suodatuksen kanssa* -toimintoa [Toimintojen hallinta](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilassa.

### <a name="enable-auto-firming-for-planning-optimization"></a>Ota käyttöön automaattinen vahvistus suunnittelun optimoinnille

Automaattisen vahvistuksen avulla voit vahvistaa suunnitellut tilaukset pääsuunnitteluprosessin osana vahvistuksen aikarajan aikana. Automaattista vahvistamista tuetaan aina suunnittelumoduulissa, joka on integroitu Supply Chain Managementiin. Kuitenkin jos sitä käytetään myös suunnittelun optimointiin, ominaisuus on otettava käyttöön.

Voit ottaa tämän toiminnon käyttöön järjestelmässäsi valitsemalla [Ominaisuuksien hallinta](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja ottamalla *Suunnittelun optimoinnin automaattinen vahvistus* -ominaisuuden käyttöön. (Supply Chain Managementin versiosta 10.0.21 alkaen tämä ominaisuus on poistettu oletusarvoisesti käytöstä.)

## <a name="manually-firm-planned-orders"></a>Vahvista suunnitellut tilaukset manuaalisesti

Voit vahvistaa suunnitellut tilaukset manuaalisesti etsimällä ja valitsemalla ne suunnitellut tilaukset, jotka haluat vahvistaa, ja käynnistämällä sitten vahvistamisprosessin manuaalisesti.

1. [Avaa jokin suunniteltujen tilausten luettelosivu](approved-planned-order.md#view-planned-orders)
1. **Suodata**-kentän, **Suunnittelu**-kentän ja sarakeotsikoiden avulla voit suodattaa ja lajitella luettelon niin, että voit etsiä haluamiasi suunniteltuja tilauksia.
1. Valitse jokaisen vahvistettavan suunnitellun tilauksen valintaruutu. Jos haluat vahvistaa kaikki sivulla luetteloituna olevat suunnitellut tilaukset (käytössä olevien suodattimien perusteella), ohita tämä vaihe.
1. Valitse toimintoruudussa yksi seuraavista painikkeista:

    - **Vahvista** – Vahvista vain valitut suunnitellut tilaukset.
    - **Vahvista kaikki** – Vahvista kaikki sivulla luetteloidut suunnitellut tilaukset (käytössä olevien suodattimien perusteella) riippumatta valituista valintaruuduista. Tämä vaihtoehto voi olla hyödyllinen, jos olet vahvistamassa useaa suunniteltua tilausta.

1. Määritä **Vahvistus**-valintaikkunan **Parametrit**-pikavälilehdessä seuraavat kentät. (Monet näistä kentistä ottavat oletusarvonsa **Vakiopäivitys**-välilehdeltä **Pääsuunnittelun parametrit** -sivulla.)

    - **Päivitä merkintä** – Valitse käytettävä varaston merkintämenettely vahvistettaessa suunniteltuja tilauksia.
    - **Lopeta vahvistus virhetilanteessa** – Määritä tämän asetuksen arvoksi *Kyllä*, jos haluat lopettaa kaikkien valittujen suunniteltujen tilausten vahvistamisen, jos jossakin niistä on virheitä. Asetuksen arvona on oltava *Ei*, jos **Rinnakkainen vahvistus** -asetuksena on *Kyllä*.
    - **Rinnakkainen vahvistus** – Tämä vaihtoehto on käytettävissä vain, jos [*Suunniteltujen tilausten rinnakkainen vahvistus* -ominaisuus](#enable-features) on käytössä järjestelmässä ja jos olet valinnut vähintään kaksi suunniteltua tilausta vahvistusta varten. Määritä arvoksi *Kyllä*, jos haluat suorittaa vahvistusprosessit rinnakkain. Rinnakkainen vahvistus voi parantaa suorituskykyä.
    - **Säikeiden määrä** – Tämä vaihtoehto on käytettävissä vain, jos [*Suunniteltujen tilausten rinnakkainen vahvistus* -ominaisuus](#enable-features) on käytössä järjestelmässä ja jos **Rinnakkainen vahvistus** -vaihtoehdon arvona on *Kyllä*. Määritä vahvistusprosessin rinnakkaistamisessa käytettävien säikeiden määrä. Ohjeita tämän vaihtoehdon käytöstä pääsuunnittelussa on kohdassa [Pääsuunnittelun suorituskyvyn parantaminen](../master-planning-performance.md#number-of-threads).

        > [!NOTE]
        > **Säikeiden määrä** -kentän arvo *0* (nolla) pidentää pääsuunnittelun ajoaikaa. Tämän vuoksi tämän kentän arvo kannattaa määrittää suuremmaksi kuin 0.

    - **Ryhmittely toimittajan mukaan** – Määritä tämän asetuksen arvoksi *Kyllä* , jos haluat ryhmitellä suunnitellut ostotilaukset ja luoda yhden ostotilauksen toimittajaa kohti vahvistuksen aikana. Voit vaihtoehtoisesti luoda uuden ostotilauksen, jossa on yksi rivi kullekin suunnitellulle tilaukselle.
    - **Ryhmittely ostajaryhmän mukaan** – Määritä tämän asetuksen arvoksi *Kyllä*, kun haluat ryhmitellä suunnitellut ostotilaukset j luoda yhden ostotilauksen, jossa yhdistetään toimittaja- ja ostajaryhmät. Jos haluat käyttää tätä asetusta, sinun täytyy asettaa myös **Ryhmittely toimittajan mukaan** -vaihtoehdon arvoksi *Kyllä*.
    - **Ryhmittele ostosopimuksen mukaan** – Määritä tämän asetuksen arvoksi *Kyllä*, jos haluat ryhmitellä suunnitellut ostotilaukset, joissa on sama toimittaja kuin aiemmin luoduilla ostosopimuksilla ja luo yksi ostotilaus ostosopimusta kohden. Tämä vaihtoehto on automaattisesti käytössä, kun **Ryhmittele toimittajan mukaan** on käytössä. Jos haluat käyttää **Ostosopimus-ryhmittelyä**, **Etsi ostosopimus** -asetus on määritettävä *Kyllä* **pääsuunnittelun parametrit** -sivulla.
    - **Ryhmittely kauden mukaan** (**Ostotilaukset**-osassa) – Valitse kausi, jonka mukaan suunnitellut ostotilaukset ryhmitellään. Jos haluat käyttää tätä asetusta, sinun täytyy valita myös **Ryhmittely toimittajan mukaan** -vaihtoehto.
    - **Ryhmittely kauden mukaan** (**Siirrot**-osassa) – Valitse kausi, jonka mukaan suunnitellut siirtotilaukset ryhmitellään. Tilaukset ryhmitellään **Varastosta**- ja **Varastoon**-arvojen mukaan.

    > [!NOTE]
    > Kukin Group by -asetus aiheuttaa sen, että järjestelmä muuntaa kunkin suunnitellun tilauksen ryhmittelyn perusteella yhden ostotilauksen riviksi.

    ![Parametrit-pikavälilehti Vahvistus-valintaikkunassa.](./media/manual-firming.png "Parametrit-pikavälilehti Vahvistus-valintaikkunassa")

1. **Suorita taustalla**-pikavälilehdessä määritä työ niin, että se suoritetaan erätilassa. Ei kuitenkaan ole järkevää määrittää toistuvaa aikataulua, kun vahvistat ajoituksen manuaalisesti. Kentät toimivat samalla tavalla kuin muissakin [taustatöissä](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) Supply Chain Managementissa. Manuaalisessa vahvistuksessa erätyö käsittelee kuitenkin vain valittuna olevat suunnitellut tilaukset. Se ei käsittele tilauksia, jotka sopivat sivulla sillä hetkellä käytettäviin suodattimiin.
1. Ota asetukset käyttöön valitsemalla **OK** ja luo vahvistetut tilaukset.

## <a name="auto-firm-planned-orders"></a>Suunniteltujen tilausten automaattinen vahvistaminen

Automaattisen vahvistuksen avulla voit vahvistaa suunnitellut tilaukset pääsuunnitteluprosessin osana. Voit määrittää kattavuusryhmien, yksittäisten nimikkeiden ja nimike- ja pääsuunnitelmien yhdistelmien vahvistamisen oletusaikarajan. Tällöin pääsuunnittelun ajon aikana suunnitellut tilaukset vahvistetaan automaattisesti, jos tilauspäivä on määritetyn vahvistamisen aikarajan sisällä. Suunnittelun optimoinnin avulla luodut suunnitellut tilaukset ja sisäinen pääsuunnittelutoiminto käsittelevät tilauspäivää (alkamispäivämäärää) eri tavalla.

> [!NOTE]
> Suunniteltujen ostotilausten automaattinen vahvistus on mahdollista vain, jos nimike on liitetty toimittajaan.
> 
> Vahvistetuissa johdetuissa tilauksissa (alihankintaostotilauksissa) näkyy *Tarkistettavana*-tila, kun muutosten seuranta on otettu käyttöön.

> [!IMPORTANT]
> Ennen kuin tässä osassa kuvattua ominaisuutta voi käyttää suunnittelun optimoinnissa, [*Suunnittelun optimoinnin automaattinen vahvistus* -ominaisuus](#enable-features) on otettava käyttöön järjestelmässä tämän ohjeaiheen alussa kuvatulla tavalla. Automaattista vahvistusta voidaan käyttää aina sisäänrakennetun pääsuunnittelumoduulin kanssa.

### <a name="auto-firming-with-planning-optimization-vs-the-built-in-planning-engine"></a>Automaattinen vahvistus suunnittelun optimoinnilla vs. sisäänrakennettu suunnittelumoduuli

Sekä suunnittelun optimointia että sisäistä suunnittelumoduulia voi käyttää suunniteltujen tilausten automaattiseen vahvistamiseen. Niillä on kuitenkin tärkeitä eroavaisuuksiakin. Esimerkiksi siinä missä suunnittelun optimointi käyttää tilauspäivää (eli aloituspäivää) määrittämään, mitkä suunnitellut tilaukset vahvistetaan, sisäinen suunnittelumoduuli käyttää tarvepäivää (eli päättymispäivää). Seuraavassa taulukossa on erojen yhteenveto.

| Ominaisuus | Suunnittelun optimointi | Sisäinen suunnittelumoduuli |
|---|---|---|
| **Päivämäärän peruste** | Automaattinen vahvistus perustuu tilauspäivään (aloituspäivään). | Automaattinen vahvistus perustuu tarvepäivään (päättymispäivään). |
| **Läpimenoaika** | Koska tilauspäivä (aloituspäivä) käynnistää vahvistuksen, läpimenoaikaa ei tarvitse sisällyttää vahvistuksen aikarajaan. | Vahvistuksen aikarajan on oltava pidempi kuin läpimenoajan, jotta voidaan varmistaa, että tilaukset vahvistetaan ajoissa. |
| **Nykyisen viikon tilaukset** | Jos haluat vahvistaa kaikki tilaukset, joiden on käynnistyttävä kuluvana viikkona, vahvistuksen aikarajan on oltava yksi viikko. | Jos haluat vahvistaa kaikki tilaukset, joiden on käynnistyttävä kuluvana viikkona, vahvistuksen aikarajan on oltava läpimenoaika plus yksi viikko. |

### <a name="set-up-auto-firming-and-the-firming-time-fence"></a>Automaattisen vahvistuksen ja vahvistuksen aikarajan määrittäminen

Voit ottaa automaattisen vahvistuksen käyttöön määrittämällä kattavuuden asetuksille automaattisen vahvistuksen aikarajan, joka on myöhemmin kuvattu tässä osassa. Jos kattavuusasetusten automaattista vahvistamista ei ole otettu käyttöön tai jos suunnittelu aloitetaan tietyltä sivulta, kuten vapautetun tuotteen **Nettotarpeet**-sivulta , automaattisen vahvistuksen prosessi ohitetaan.

Automaattisen vahvistuksen ryhmittely- ja merkintäasetukset ottavat arvonsa **Vakiopäivitys**-välilehdeltä **Pääsuunnittelun parametrit** -sivulla.

Automaattisen vahvistuksen aikaraja määritetään niiden päivien määrän mukaan, jonka syötät liittyville kattavuusasetuksille. Automaattinen vahvistus voidaan ottaa käyttöön ja vahvistuksen aikarajaa hallita seuraavilla tavoilla:

- Voit määrittää kattavuusryhmän vahvistuksen oletusaikarajan valitsemalla ensin **Pääsuunnittelu \> Asetukset \> Kattavuus \> Kattavuusryhmät** ja valitsemalla sitten kattavuusryhmän. Anna sitten päivien määrä **Muu**-pikavälilehden **Automaattisen vahvistuksen aikaraja (päivää)** -kentässä.
- Jos haluat korvata tietyn nimikkeen kattavuusryhmälle määritetyn vahvistuksen aikarajan, valitse **Tuotetietojen hallinta \> Vapautetut tuotteet**. Valitse toimintoruudusta **Suunnitelma** ja valitse sitten **Nimikekattavuus**. Valitse tämän jälkeen **Yleiset**-välilehdessä **Ohita aikarajat** ja anna päivien määrä **Automaattisen vahvistuksen aikaraja (päivää)** -kentässä.
- Voit ohittaa tietylle kattavuusryhmälle määritetyn aikarajan ja tietyn pääsuunnitelman nimikkeen kattavuuden valitsemalla ensin **Pääsuunnittelu \> Asetukset \> Pääsuunnitelmat** ja valitsemalla sitten pääsuunnitelman. Anna sitten päivien määrä valitsemalla **Aikarajat päivinä** -pikavälilehdessä **Vahvistus**-asetukseksi *Kyllä*.

Jos määrität kaikkien aiemmin mainittujen aikarajojen arvoksi *0* (nolla), liittyvien katettujen nimikkeiden automaattinen vahvistus poistetaan käytöstä.

## <a name="firm-planned-orders-by-using-a-query"></a>Vahvista suunnitellut tilaukset kyselyn avulla.

Kyselypohjaisen vahvistamisen avulla voit suunnitella vahvistuksen etukäteen määritettyjen ehtojen mukaan. Toisin kuin automaattinen vahvistus, kyselypohjainen vahvistus mahdollistaa tilausten eri osajoukkojen automaattisen vahvistamisen eri aikoina. Lisäksi voit käyttää manuaalisia tai automaattisia toimintoja vahvistaaksesi erityyppisiä suunniteltuja tilauksia. Voit myös esikatsella, mitkä vahvistetut tilaukset valitaan asetusten mukaan. Voit siis vahvistaa, että valinta vastaa odotuksiasi.

Voit yhdistää automaattisen vahvistuksen kyselypohjaiseen vahvistukseen. Kyselypohjaisessa vahvistustyössä on esimerkiksi eteenpäin toimitettava aikaraja, joka on pidempi kuin täsmäyttävän automaattisen vahvistuksen kattavuuskonfiguraation aikaraja. Siksi kyselypohjainen vahvistustyö käsittelee suunnitellut tilaukset ennen automaattisen vahvistuksen käynnistämistä. Voit käyttää hyväksesi tätä toimintatapaa, kun haluat ajoittaa tiettyjen toimittajien tilaukset eri tavalla kuin muiden toimittajien samankaltaisten tuotteiden tilaukset.

> [!IMPORTANT]
> Ennen kuin tässä osassa kuvattua ominaisuutta voi käyttää, [*Suunniteltujen tilausten vahvistaminen suodatuksen avulla* -ominaisuus](#enable-features) on otettava käyttöön järjestelmässä tämän ohjeaiheen alussa kuvatulla tavalla.

Toimi seuraavasti, kun haluat vahvistaa suunnitellun tilauksen käyttämällä kyselyyn perustuvaa vahvistamisprosessia.

1. Valitse **Pääsuunnittelu \> Pääsuunnittelu \> Suorita \> Suunniteltujen tilausten vahvistaminen**.
1. Määritä **Suunniteltujen tilausten vahvistaminen** -valintaikkunassa **Parametrit**-pikavälilehdessä peruskäsittelyn, merkinnän ja ryhmittelyn asetukset. Nämä vaihtoehdot toimivat samoin kuin **Vahvistus**-valintaikkunassa. (Kuvaukset ovat edellisessä osassa.) Määritä sitten **Suunnitelma**-osassa seuraavat kentät, jotka ovat yksilöiviä suunnitellun **Suunniteltujen tilausten vahvistaminen** -valintaikkunassa:

    - **Suunnitelma** – Valitse pääsuunnitelma, jota on käytettävä tämän kyselyn löytämien suunniteltujen tilausten vahvistamisen aikana.
    - **Vahvistuksen aikarajapäivät eteenpäin** – Valitse, kuinka pitkälle tulevaisuuteen pääsuunnittelun on laskettava erilaiset tarpeet ja muut huomionarvoiset seikat.
    - **Vahvistuksen aikarajapäivät taaksepäin** – Valitse, kuinka pitkälle menneeseen pääsuunnittelun on laskettava erilaiset tarpeet ja muut huomionarvoiset seikat.

    ![Parametrit-pikavälilehti Suunniteltujen tilausten vahvistaminen -valintaikkunassa.](./media/planned-order-firming-main-1.png "Parametrit-pikavälilehti Suunniteltujen tilausten vahvistaminen -valintaikkunassa")

1. Voit määrittää tilaukseen sisällytettävät tietueet valitsemalla **Suodata**-painikkeen **Sisällytettävät tietueet** -pikavälilehdeltä. Näyttöön tulee vakiokyselyvalintaikkuna, jossa voit määrittää valintaehtoja, lajitteluehtoja ja liitoksia. Kentät toimivat samalla tavalla kuin muissakin kyselyissä Supply Chain Managementissa. Tämän lomakkeen kentät ovat vain luku -kenttiä, ja ne näyttävät kyselyyn liittyviä arvoja.

    ![Sisällytettävät tietueet -pikavälilehti Suunniteltujen tilausten vahvistaminen -valintaikkunassa.](./media/planned-order-firming-main-2.png "Sisällytettävät tietueet -pikavälilehti Suunniteltujen tilausten vahvistaminen -valintaikkunassa")

1. Valitse **Esiversio**, jos haluat esikatsella vahvistetun tilauksen sisältöä asetusten mukaan. Luettelo suunnitelluista tilauksista, jotka on tarkoitus vahvistaa, näytetään sanomana. Voit sitten tarvittaessa muuttaa asetuksia, kunnes esikatselussa näkyy vahvistettu tilaus halutunlaisena.

    ![Esimerkki vahvistetun tilauksen esikatselusta.](./media/planned-order-firming-preview.png "Esimerkki vahvistetun tilauksen esikatselusta")

    > [!WARNING]
    > Tämä ominaisuus vahvistaa kaikki suodatusehtoja vastaavat suunnitellut tilaukset. Suunniteltujen tilausten kritiikitön vahvistus voi aiheuttaa sen, että luodaan runsaasti ei-toivottuja osto-, siirto- ja tuotantotilauksia. Ennen jatkamista voit vahvistaa sisällytettävät tietueet **Esiversio**-painikkeen avulla.

1. **Suorita taustalla** -pikavälilehdessä määritä työ niin, että se suoritetaan erätilassa ja/tai määritä toistuva aikataulu. Kentät toimivat samalla tavalla kuin muissakin [taustatöissä](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) Supply Chain Managementissa.
1. Ota asetukset käyttöön valitsemalla **OK** ja luo vahvistetut tilaukset.

## <a name="track-firmed-orders"></a>Vahvistettujen tilausten seuraaminen

Noudattamalla seuraavia ohjeita voit seurata suunniteltua tilausta, joka on vahvistettu.

1. [Avaa jokin suunniteltujen tilausten luettelosivu](approved-planned-order.md#view-planned-orders)
1. Avaa tai valitse suunniteltu tilaus, jota haluat seurata.
1. Valitse sitten toimintoruudussa **Näytä**-välilehden **Näytä**-ryhmässä **Vahvistushistoria**.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
