---
title: Kiertoteiden määritys mobiililaitteiden valikkokohteiden vaiheille
description: Tässä artikkelissa kuvataan, miten voidaan määrittää kiertoteitä valikkokohteille, jotta työntekijät voivat pysäyttää kulloisenkin tehtävän, suorittaa toisen tehtävän ja palata alkuperäiseen tehtävään tietoja menettämättä.
author: Mirzaab
ms.date: 09/01/2022
ms.topic: article
ms.search.form: WHSMobileAppFlowStepListPage, WHSMobileAppFlowStepAddDetour, WHSMobileAppFlowStepDetourSelectFields, WHSMobileAppFlowStepSelectPromotedFields
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 2e387dd4e6499912f2d53dddc17ccc053f1ca699
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689307"
---
# <a name="configure-detours-for-steps-in-mobile-device-menu-items"></a>Kiertoteiden määritys mobiililaitteiden valikkokohteiden vaiheille

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 10.0.31 GA -->

> [!IMPORTANT]
> Tässä artikkelissa käsitellyt toiminnot koskevat vain uutta Warehouse Management -mobiilisovellusta. Niillä ei ole vaikutusta vanhaan varastosovellukseen, joka on nyt vanhentunut.

Tässä artikkelissa kuvataan, miten voidaan määrittää kiertoteitä valikkokohteille, jotta työntekijät voivat pysäyttää kulloisenkin tehtävän, suorittaa toisen tehtävän ja palata alkuperäiseen tehtävään tietoja menettämättä.

Kiertotie on erillinen valikkokohde, joka voidaan avata päätehtävän vaiheesta. Kiertotien päätyessä työntekijä palautetaan paikkaan, jossa hän poistui päätehtävästä. Määrityksen aikana määritetään valikkokohde, joka toimii kiertotienä. Siinä valitaan myös, mitkä päätehtävän kenttäarvot lähetetään automaattisesti eteenpäin (kopioidaan) kiertotiehen ja lisätään siihen. Siksi on ymmärrettävä, missä kohdassa tehtävänkulkua kiertotien on tarkoitus olla työntekijöiden käytettävissä. Sinun on myös varmistettava, että tiedot, jotka on kopioitava kiertotiehen, ovat käytettävissä tehtävänkulun kyseisessä vaiheessa.

## <a name="enable-detours-in-your-system"></a>Kiertoteiden käyttöönotto järjestelmässä

Ennen kuin voit määrittää mobiililaitteiden valikkokohteiden vaiheiden kiertoteitä, sinun suoritettava seuraava menettely, jolla otetaan käyttöön tarvittavat ominaisuudet ja luodaan tarvittavat kenttänimet Warehouse Management -mobiilisovelluksessa.

1. Valitse **Järjestelmänvalvoja \> Työtilat \> Ominaisuuksien hallinta**.
1. Varmista, että *Varastosovelluksen vaiheohjeet* -ominaisuus on käytössä järjestelmässäsi. Supply Chain Managementin versiosta 10.0.29 alkaen tämä ominaisuus on poistettu oletusarvoisesti käytöstä. Lisätietoja *Varastosovelluksen vaiheohjeet*-toiminnosta: [Vaiheotsikkojen ja ohjeiden mukauttaminen Warehouse Management -mobiilisovelluksessa](mobile-app-titles-instructions.md). Tämä ominaisuus on edellytys *Warehouse Management -sovelluksen kiertotiet* -ominaisuudelle.
1. Ota käyttöön seuraavat toiminnot, jotka sisältävät tässä artikkelissa kuvattuja toimintoja:
    - *Warehouse Management -sovelluksen kiertotie*<br>(Supply Chain Managementin versiosta 10.0.29 alkaen tämä ominaisuus on poistettu oletusarvoisesti käytöstä.)
    - *Monitasoiset kiertotiet Warehouse Management ‑mobiilisovelluksessa*
    - *Lähetä Warehouse Management ‑mobiilisovelluksen kiertotievaiheet automaattisesti*
1. Jos *Warehouse Management -sovelluksen kiertotiet*- ja/tai *Monitasoiset kiertotiet Warehouse Management ‑mobiilisovelluksessa* -ominaisuus ei ole vielä käytössä, päivitä kenttien nimet Warehouse Management -mobiilisovelluksessa valitsemalla **Varastonhallinta \> Asetukset \> Mobiililaite \> Varastosovelluksen kenttien nimet** ja valitsemalla **Luo oletusasetus**. Lisätietoja: [Varastonhallinnan mobiilisovelluksen kenttien konfigurointi](configure-app-field-names-priorities-warehouse.md).
1. Toista edellinen vaihe kullekin yritykselle, jossa käytät Warehouse Management -mobiilisovellusta.

## <a name="configure-a-detour-from-a-menu-specific-override"></a>Valikkokohtaisen ohituksen kiertotien määrittäminen

Seuraavalla menettelyllä voit määrittää valikkokohtaisen ohituksen kertotien.

1. Luo valikkokohtainen ohitus kulloisellekin valikolle ja vaiheelle kohdan [Warehouse Management ‑mobiilisovelluksen vaiheiden otsikoiden ja ohjeiden mukauttaminen](mobile-app-titles-instructions.md) ohjeiden mukaisesti.
1. Etsi muokattavat **Vaiheen tunnus**- ja **Valikkovaihtoehdon nimi** -arvot ja valitse sitten arvo **Vaiheen tunnus** -sarakkeessa.
1. Valitse näkyviin tulevan sivun **Käytettävissä olevat kiertotiet (valikkokohteet)** -pikavälilehdellä voit määrittää valikkokohteen, joka toimii kiertotienä. Voit valita myös, mitkä päätehtävän kenttäarvot kopioidaan automaattisesti kiertotiehen ja kiertotieltä. Esimerkkejä näiden asetusten käytöstä on skenaarioissa myöhemmin tässä artikkelissa.

## <a name="sample-scenario-1-sales-picking-where-a-location-inquiry-acts-as-a-detour"></a><a name="scenario-1"></a>Esimerkkiskenaario 1: Myynnin keräily, jossa sijaintikysely toimii kiertotienä

Tässä skenaariossa esitetään, miten sijaintikysely määritetään kiertotieksi työntekijän ohjaamassa myynnin keräilyn tehtävänkulussa. Tämän kiertotien avulla työntekijät voivat etsiä kaikki rekisterikilvet sijainnista, jossa he suorittavat keräilyä, ja valita rekisterikilven, jota he haluavat käyttää keräilyn loppuun suorittamisessa. Tällainen kiertotie voi olla hyödyllinen, jos viivakoodi on vahingoittunut ja skanneri ei voi lukea sitä. Vaihtoehtoisesti se voi olla hyödyllinen silloin, kun työntekijän on saatava tietää, mitä järjestelmässä todella on käytettävissä. Huomaa, että tämä skenaario toimii vain, jos keräily suoritetaan rekisterikilpiin perustuvissa sijainnissa.

### <a name="enable-sample-data"></a>Mallitietojen ottaminen käyttöön

Jos haluat suorittaa tämän skenaarion käyttämällä määritettyjä esimerkkitietueita ja -arvoja, sinun täytyy käyttää järjestelmää, johon vakiomuotoiset [demotiedot](../../fin-ops-core/fin-ops/get-started/demo-data.md) on asennettu. Sinun on myös valittava **USMF**-yritys ennen aloittamista.

### <a name="create-a-menu-specific-override-and-configure-the-detour-for-scenario-1"></a>Valikkokohteisen ohituksen luominen ja skenaarion 1 kiertotien määrittäminen

Tässä menettelyssä määrität kiertotien **Myynnin keräily** -valikkokohteelle rekisterikilpivaiheessa.

1. Valitse **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen vaiheet**.
1. Etsi vaihetunnus nimeltä *LicensePlateId* ja valitse se.
1. Valitse toimintoruudussa **Luo vaiheen määritys**.
1. Käytä avattavassa valintaikkunassa kenttää **Valikkokohde** etsiäksesi ja valitaksesi *Myynnin keräily*.
1. Valitse **OK**.
1. Luomasi ohituksen tietosivu tulee näkyviin. Valitse **Käytettävissä olevat kiertotiet (valikkokohteet)**-pikavälilehden työkalupalkista **Lisää**.
1. Valitse **Lisää kiertotie** -valintaikkunassa **Sijaintikysely** kiertotieksi, joka asetetaan saataville Warehouse Management -mobiilisovelluksessa.
1. Valitse **OK**.
1. Valitse **Käytettävissä olevat kiertotiet (valikkokohteet)**-pikavälilehdessä juuri lisäämäsi kiertotie ja valitse sitten työkalupalkista **Valitse lähetettävät kentät**.
1. Määritä **Valitse lähetettävät kentät** -valintaikkunassa ne tiedot, jotka lähetetään kiertotiestä ja kiertotiehen. Tässä skenaariossa annat työntekijöiden käyttää sijaintia, josta heidän on tarkoitus suorittaa keräily, sijaintikyselykiertotien syötteenä. Valitse siksi **Lähetä myynnin keräilystä** -osan työkalupalkista **Lisää** lisätäksesi rivin ruudukkoon. Määritä sitten uudelle rivillä seuraavat arvot:

    - **Kopioi myynnin keräilystä:** *Sijainti*
    - **Liitä sijaintikyselyyn:** *Sijainti*
    - **Automaattinen lähetys:** *Valittu* (sivu päivitetään liitetyllä *sijainnin* arvolla)

1. Koska tämän skenaarion kiertotie määritetään rekisterikilpivaiheessa, olisi hyödyllistä, että työntekijät voisivat tuoda rekisterikilven kyselystä takaisin päätyönkulkuun. Valitse siksi **Tuo takaisin sijaintikyselystä** -osan työkalupalkista **Lisää** lisätäksesi rivin ruudukkoon. Määritä sitten uudelle rivillä seuraavat arvot:

    - **Kopioi sijaintikyselystä:** *Rekisterikilpi*
    - **Liitä myynnin keräilyyn:** *Rekisterikilpi*
    - **Automaattinen lähetys:** *Tyhjennetty* (automaattista päivitystä ei tehdä, kun kiertotieltä palataan *rekisterikilven* arvon kanssa)

1. Valitse **OK**.

Kiertotie on nyt määritetty kokonaan. **Sijaintikysely**-kiertotien käynnistävä painike tulee nyt näkyviin rekisterikilpivaiheeseen **Myynnin keräily** -valikkokohteen osalta.

### <a name="complete-a-sales-pick-on-a-mobile-device-and-use-the-detour"></a>Myynnin keräilyn suorittaminen mobiililaitteella ja kiertotien käyttö

Tässä menettelyssä suoritetaan myynnin keräily Warehouse Management -mobiilisovelluksella. Käytät juuri määrittämääsi kiertotietä sen rekisterikilven etsimiseen, jota käytät keräilyvaiheen suorittamiseen.

1. Luo Microsoft Dynamics 365 Supply Chain Managementissa myyntitilaus, joka edellyttää keräilyvaihetta sijainnissa, jota seurataan rekisterikilvillä. Vapauta myyntitilaus sitten varastoon. Kirjoita luotu työn tunnus muistiin.
1. Avaa Warehouse Management -mobiilisovellus ja kirjaudu sisään varastoon 24. (Kirjaudu standardidemotiedoissa sisään käyttämällä numeroa *24* käyttäjätunnuksena ja numeroa *1* salasanana.)
1. Valitse **Lähtevät**-valikko ja valitse sitten **Myynnin keräily** -valikkokohde.
1. Noudata näytön tiedonsyöttöohjeita ja syötä vaiheessa 1 luotu työn tunnus.
1. Avaa toimintovalikko vaiheessa, joka sisältää tekstin **Skannaa rekisterikilpi**. Tällöin näkyviin pitäisi tulla uusi painike nimeltään **Sijaintikysely**. Vasemmassa yläkulmassa oleva nuoli ilmaisee, että painike käynnistää kiertotien. Valitse **Sijaintikysely**.
1. Kiertotie käynnistetään. Vahvista seuraavalla sivulla sijainti, joka on kopioitu päätyönkulusta.
1. Napauta sijainnissa käytettävissä olevien rekisterikilpien luettelossa rekisterikilpeä, jonka haluat kopioida takaisin päätyönkulkuun. Valitse sitten **Takaisin**-painike.
1. Sinut palautetaan myynnin keräilyn päätyönkulkuun, ja rekisterikilpi on kopioitu kiertotiestä takaisin siihen. Vahvista arvo, jotta voit jatkaa seuraavaan vaiheeseen.
1. Voit nyt suorittaa loput vakiotyönkulusta syöttämällä vaaditut tiedonsyöttöohjeet.

Varastotyö on nyt valmis. Työntekijä avasi kiertotien onnistuneesti suorittaakseen toissijaisen tehtävän (sijaintikysely) kadottamatta paikkaansa päätehtävässä ja toi takaisin tiedot, jotka tarvittiin päätehtävän suorittamiseen.

## <a name="sample-scenario-2-item-inquiry-with-movement-and-adjustment-detours"></a>Esimerkkiskenaario 2: Nimikekysely siirto- ja oikaisukiertoteillä

Tässä skenaariossa kuvataan, miten siirto ja oikaisut määritetään useiksi kiertoteiksi sijaintikyselyn tehtävänkulussa. Tämä ominaisuus voi olla hyödyllinen tilanteissa, joissa työntekijä saapuu sijaintiin ja havaitsee, että sijainnin varasto poikkeaa järjestelmään rekisteröidystä, minkä vuoksi hänen on oikaistava tai siirrettävä tuotteita.

Voit korvata sijaintikyselyn tarvittaessa rekisterikilpikyselyllä tai nimikekyselyllä.

### <a name="enable-sample-data"></a>Mallitietojen ottaminen käyttöön

Jos haluat suorittaa tämän skenaarion käyttämällä määritettyjä esimerkkitietueita ja -arvoja, sinun täytyy käyttää järjestelmää, johon vakiomuotoiset [demotiedot](../../fin-ops-core/fin-ops/get-started/demo-data.md) on asennettu. Sinun on myös valittava **USMF**-yritys ennen aloittamista.

### <a name="create-a-menu-specific-override-and-configure-the-detour-for-scenario-2"></a>Valikkokohteisen ohituksen luominen ja skenaarion 2 kiertotien määrittäminen

Tässä menettelyssä määrität kiertotien **Myynnin keräily** -valikkokohteelle rekisterikilpivaiheessa.

1. Valitse **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen vaiheet**.
1. Etsi ja valitse vaihetunnus nimeltään *LocationInquiryList*.

    > [!NOTE]
    > Jos haluat käyttää nimikekyselyä sijaintikyselyn sijaan, valitse rivi, jossa vaihetunnuksen nimi on *ItemInquiryList*. Jos taas haluat käyttää rekisterikilpikyselyä, valitse rivi, jolla vaihetunnuksen nimi on *LPInquiryList*.

1. Valitse toimintoruudussa **Luo vaiheen määritys**.
1. Käytä avattavassa valintaikkunassa kenttää **Valikkokohde** etsiäksesi ja valitaksesi *Sijaintikysely*.
1. Valitse **OK**.
1. Luomasi ohituksen tietosivu tulee näkyviin. Valitse **Käytettävissä olevat kiertotiet (valikkokohteet)**-pikavälilehden työkalupalkista **Lisää**.
1. Valitse **Lisää kiertotie** -valintaikkunassa **Siirto** kiertotieksi, joka asetetaan saataville Warehouse Management -mobiilisovelluksessa.
1. Valitse **OK**.
1. Valitse **Käytettävissä olevat kiertotiet (valikkokohteet)**-pikavälilehdessä juuri lisäämäsi kiertotie ja valitse sitten työkalupalkista **Valitse lähetettävät kentät**.
1. Määritä **Valitse lähetettävät kentät** -valintaikkunassa ne tiedot, jotka lähetetään kiertotiestä ja kiertotiehen. Tässä skenaariossa oletat, että työntekijät etsivät rekisterikilpiohjattuja sijainteja. Sen vuoksi on hyödyllistä kopioida kyselyn rekisterikilpi **Siirto**-kiertotiehen. Valitse **Lähetä myynnin keräilystä** -osan työkalupalkista **Lisää** lisätäksesi rivin ruudukkoon. Määritä sitten uudelle rivillä seuraavat arvot:

    - **Kopioi sijaintikyselystä:** *Sijainti*
    - **Liitä siirtoon:** *Loc / LP*
    - **Automaattinen lähetys:** *Tyhjennetty* (automaattista päivitystä ei tehdä)

    Tässä kiertotiessä ei oleteta, että tietoja kopioidaan takaisin, koska päätyönkulku oli kysely, jossa ei tarvita lisävaiheita.

1. Valitse **OK**.

Kiertotie on nyt määritetty kokonaan. **Siirto**-kiertotien käynnistävä painike tulee nyt näkyviin rekisterikilpivaiheeseen **Sijaintikysely**-valikkokohteen osalta.

### <a name="do-a-location-inquiry-on-a-mobile-device-and-use-the-detour"></a>Sijaintikyselyn tekeminen mobiililaitteella ja kiertoien käyttö

Tässä menettelyssä suoritetaan sijaintikysely Warehouse Management -mobiilisovelluksella. Tämän jälkeen kiertotietä käytetään tuotteiden siirron suorittamiseen.

1. Avaa Warehouse Management -mobiilisovellus ja kirjaudu sisään varastoon 24. (Kirjaudu standardidemotiedoissa sisään käyttämällä numeroa *24* käyttäjätunnuksena ja numeroa *1* salasanana.)
1. Valitse **Varasto**-valikko ja valitse sitten **Sijaintikysely**-valikkokohde.
1. Syötä sijainti kyselyn kohteeksi, kuten *FL-001*.
1. Kun luettelo tulee näkyviin, napauta ja pidä napautettuna yhtä siinä olevista korteista, jotta näet käytettävissä olevat kiertotiet.
1. Valitse **Siirto**.
1. Huomaa, että rekisterikilpi on kopioitu valitsemastasi kortista. Vahvista arvo.
1. Voit nyt suorittaa siirron noudattamalla vakiotehtävänkulkua. Kun työ on valmis, avaa toimintovalikko ja valitse **Peruuta**.
1. Palaat **Sijaintikysely**-sivulle. Huomaa, että arvoja ei päivitetä automaattisesti. Näin ollen sivu on päivitettävä manuaalisesti, jotta näet siirtokiertotien muutokset.

> [!NOTE]
> *Monitasoiset kiertotiet Warehouse Management ‑mobiilisovelluksessa* -ominaisuuden avulla voit määrittää monitasoisia kiertoteitä (kiertoteitä kiertoteiden sisällä), joiden avulla työntekijät voivat siirtyä olemassa olevalta kiertotieltä hetkessä toiselle ja taas takaisin. Ominaisuus tukee valmiiden kiertoteiden kahta tasoa. Tarvittaessa voit mukauttaa järjestelmää niin, että se tukee kolmea tai useampaa kiertoteiden tasoa luomalla koodilaajennukset tauluun `WHSWorkUserSessionState`.
>
> *Lähetä Warehouse Management ‑mobiilisovelluksen kiertotievaiheet automaattisesti* -ominaisuuden avulla työntekijät voivat tehdä kiertotietyönkulkuja aiempaa nopeammin ja helpommin Warehouse Management -mobiilisovelluksessa. Näin joitakin työnkulun vaiheita voidaan ohittaa, kun sovellus täyttää kiertotietiedot taustalla ja siirtyy sitten automaattisesti seuraavaan vaiheeseen lähettämällä sivun automaattisesti [*Esimerkkiskenaario 1: Myynnin keräily, jossa sijaintikysely toimii kiertotienä*](#scenario-1) -kohdassa näytetyllä tavalla.
