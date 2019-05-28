---
title: Vähittäismyyntikanavien kirjanpidon integroinnin määrittäminen
description: Tässä ohjeaiheessa on ohjeet vähittäismyyntikanavien kirjanpidon integrointitoiminnon määrittämiseen.
author: josaw
manager: annbe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 060075757dec64e83c46498380a920d580ac09e4
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2019
ms.locfileid: "1525322"
---
# <a name="set-up-the-fiscal-integration-for-retail-channels"></a>Vähittäismyyntikanavien kirjanpidon integroinnin määrittäminen

[!include [banner](../includes/banner.md)]

## <a name="introduction"></a>Johdanto

Tässä ohjeaiheessa on ohjeet vähittäismyyntikanavien kirjanpidon integrointitoiminnon määrittämiseen. Lisätietoja kirjanpidon integroinnista on kohdassa [Vähittäismyyntikanavan kirjanpidon integroinnin yleiskatsaus](fiscal-integration-for-retail-channel.md).

Kirjanpidon integroinnin määritysprosessi sisältää seuraavat tehtävät:

1. Määritä ne kirjanpidon yhdistimet, jotka edustavat kirjanpidon rekisteröinnissä käytettäviä kirjanpidon laitteita tai palveluja, kuten kuittitulostimia.
2. Määritä tiedostopalvelut, jotka muodostavat kirjanpidon yhdistimien kirjanpidon laitteissa tai palveluissa rekisteröitävät kirjanpitoasiakirjat.
3. Määritä kirjanpidon rekisteröintiprosessi, joka määrittää kirjanpidon rekisteröintivaiheiden järjestyksen sekä kussakin vaiheessa käytettävät kirjanpidon yhdistimet ja kirjanpitoasiakirjojen toimittajat.
4. Määritä kirjanpidon rekisteröintiprosessi myyntipisteen toimintaprofiileihin.
5. Määritä yhdistimen tekniset profiilit laiteprofiileihin.

## <a name="set-up-a-fiscal-registration-process"></a>Kirjanpidon rekisteröintiprosessin määrittäminen

Määritä seuraavat asetukset ennen kirjanpidon integrointitoiminnon käyttämistä.

1. Päivitä vähittäismyynnin parametrit.

    1. Valitse **Vähittäismyynnin yhteiset parametrit** -sivun **Yleiset**-välilehden **Ota kirjanpidon integrointi käyttöön** -asetukseksi **Kyllä**. Määritä seuraavien viitteiden numerosarjat **Numerosarjat**-välilehdessä:

        - Kirjanpidon teknisen profiilin numero
        - Kirjanpidon yhdistinryhmän numero
        - Rekisteröintiprosessin numero

    2. Määritä kirjanpidon toimintaprofiilinumeron numerosarja **Vähittäismyynnin parametrit** -sivulla.

    > [!NOTE]
    > Numerosarjat ovat valinnaisia. Kaikki kirjanpidon integrointiyksiköt voidaan luoda joko numerosarjoista tai manuaalisesti.

2. Lataa kirjanpidon yhdistimien ja kirjanpitoasiakirjan toimittajien määritykset.

    Kirjanpitoasiakirjan toimittaja vastaa niiden kirjanpitoasiakirjojen luomisesta, jotka vastaavat myyntipisteessä rekisteröityjä vähittäismyyntitransaktioita ja -tapahtumia. Rekisteröinnissä käytetään samaa muotoa, jota käytetään myös kirjanpidon laitetta tai palvelua käytettäessä. Kirjanpitoasiakirjan toimittaja voi esimerkiksi luoda verokuitin XML-muodossa.

    Kirjanpidon yhdistin vastaa kirjanpidon laitteen tai palvelun kanssa tapahtuvasta tietoliikenteestä. Kirjanpidon yhdistin voi esimerkiksi lähettää kirjanpitoasiakirjan toimittajan XML-muodossa luoman verokuitin kuittitulostimeen. Lisätietoja kirjanpidon integroinnin osista on kohdassa [Kirjanpidon rekisteröintiprosessi ja kirjanpidon laitteiden kirjanpidon integrointimallit](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices).

    1. Lataa **Kirjanpidon yhdistimet** -sivulla (**Vähittäismyynti \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpidon yhdistimet**) kunkin sellaisen laitteen tai palvelun XML-määritys, jota aiot käyttää kirjanpidon integroinnissa.

        > [!TIP]
        > Valitsemalla **Näytä** voit tarkastella kaikkia nykyisiin kirjanpidon yhdistimeen liittyviä toimintaprofiileja ja teknisiä profiileja.

    2. Lataa **Kirjanpitoasiakirjan toimittajat** -sivulla (**Vähittäismyynti \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpitoasiakirjan toimittajat**) kunkin sellaisen laitteen tai palvelun XML-määritys, jota aiot käyttää.

        > [!TIP]
        > Valitsemalla **Näytä** voit tarkastella kaikkia nykyiseen kirjanpitoasiakirjan toimittajaan liittyviä toimintaprofiileja.

    Esimerkkejä kirjanpidon yhdistimien ja kirjanpitoasiakirjojen toimittajien määrityksistä on kohdassa [Retail SDK:n kirjanpidon integrointimallit](fiscal-integration-for-retail-channel.md#fiscal-integration-samples-in-the-retail-sdk).

    > [!NOTE]
    > Tietojen yhdistämisen katsotaan olevan osa kirjainpitoasiakirjan toimittajaa. Jos haluat määrittää samalle yhdistimelle erilaisia tietojen yhdistämisiä (kuten osavaltiokohtaisia säädöksiä), sinun on luotava erillisiä kirjainpitoasiakirjan toimittajia.

3. Luo yhdistimen toiminnalliset ja tekniset profiilit.

    1. Luo **Yhdistimen toiminnalliset profiilit** -sivulla (**Vähittäismyynti \> Kanavan asetukset \> Kirjanpidon integrointi \> Yhdistimen toiminnalliset profiilit**) yhdistimen toiminnallinen profiili jokaiselle kirjanpidon yhdistimen ja siihen liittyvän kirjanpitoasiakirjan toimittajan yhdistelmälle.

        1. Valitse yhdistimen nimi.
        2. Valitse asiakirjan toimittaja.

        Voit muuttaa tietojen yhdistämisparametreja yhdistimen toiminnallisessa profiilissa. Voit palauttaa kirjanpitoasiakirjan toimittajan määrityksessä määritetyt oletusparametrit valitsemalla **Päivitys**.

        **Esimerkkejä**
    
        |   | Muoto | Esimerkki |
        |---|--------|---------|
        | **ALV-prosenttiasetukset** | arvo: VATrate | 1 : 2000, 2 : 1800 |
        | **ALV-koodien yhdistäminen** | VATcode : arvo | vat20 : 1, vat18 : 2 |
        | **Maksuvälinetyyppien yhdistäminen** | TenderType : arvo | Käteinen : 1, Kortti : 2 |

        > [!NOTE]
        > Yhdistimen toiminnalliset profiilit ovat yrityskohtaisia. Jos aiot käyttää samaa kirjanpidon yhdistimen ja kirjanpitoasiakirjan toimittajan yhdistelmää eri yrityksissä, kullekin yritykselle on luotava yhdistimen toiminnallinen profiili.

    2. Luo kunkin kirjanpidon yhdistimen toiminnallinen profiili **Yhdistimen tekniset profiilit** -sivulla (**Vähittäismyynti \> Kanavan asetukset \> Kirjanpidon integrointi \>Yhdistimen tekniset profiilit**).

        1. Valitse yhdistimen nimi.
        2. Valitse yhdistimen tyyppi. Valitse laiteasemaan liitetyissä laitteissa **Paikallinen**.

            > [!NOTE]
            > Vain paikallisia yhdistimiä tuetaan.

        Yhdistimen teknisen profiilin **Laite**- ja **Asetukset**-välilehtien parametreja voi muuttaa. Voit palauttaa kirjanpidon yhdistimen määrityksessä määritetyt oletusparametrit valitsemalla **Päivitys**. Kun XML-määrityksen uutta versiota ladataan, saat ilmoituksen, jonka mukaan nykyistä kirjanpidon yhdistintä tai kirjanpitoasiakirjan toimittaja on jo käytössä. Tämä menettely ei ohita yhdistimen toiminnallisiin tai teknisiin profiileihin aiemmin tehtyjä manuaalisia muutoksia. Voit käyttää uuden määrityksen oletusparametrijoukkoa valitsemalla **Päivitä** **Yhdistimen toiminnalliset profiilit**- tai **Yhdistimen tekniset profiilit** -sivulla.

4. Luo kirjanpidon yhdistinryhmiä.

    Kirjanpidon yhdistinryhmä yhdistää ne kirjanpidon yhdistimien toiminnalliset profiilit, jotka suorittavat samoja toimintoja ja joita käytetään samassa kirjanpidon rekisteröintiprosessin vaiheessa. Jos esimerkiksi myymälässä käytetään useita kuittitulostinmalleja, kyseisten kuittitulostimien kirjanpidon yhdistimet voidaan yhdistää kirjanpidon yhdistinryhmäksi.
    
    1. Luo uusi kirjanpidon yhdistinryhmä **Kirjanpidon yhdistinryhmä** -sivulla (**Vähittäismyynti \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpidon yhdistinryhmä**).
    2. Lisää toiminnalliset profiilit yhdistinryhmään. Valitse ensin **Toiminnalliset profiilit** -sivulla **Lisää** ja valitse sitten profiilin numero. Kullakin yhdistinryhmän kirjanpidon yhdistimellä voi olla vain yksi toiminnallinen profiili.
    3. Voit keskeyttää toiminnallisen profiilin käytön valitsemalla **Poista käytöstä** -asetukseksi **Kyllä**. Muutos koskee vain nykyistä yhdistinryhmää. Voit jatkaa saman toiminnallisen profiilin käyttöä muissa yhdistinryhmissä.

5. Luo kirjanpidon rekisteröintiprosessi.

    Rekisteröintivaiheiden järjestys ja kussakin vaiheessa käytetty yhdistinryhmä määrittävät kirjanpidon rekisteröintiprosessin.
    
    1. Luo uusi tietue kirjanpidon rekisteröinnin kullekin yksilölliselle prosessille **Kirjanpidon rekisteröintiprosessi** -sivulla (**Vähittäismyynti \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpidon rekisteröintiprosessi**).
    2. Lisää rekisteröintivaiheet prosessiin:

        1. Valitse **Lisää**.
        2. Valitse kirjanpidon yhdistimen tyyppi.
        3. Valitse sopiva kirjanpidon yhdistinryhmä **Ryhmän numero** -kentässä.

6. Määritä kirjanpidon rekisteröintiprosessiyksiköt myyntipisteen profiileihin.

    1. Määritä kirjanpidon rekisteröintiprosessi myyntipisteen toimintoprofiiliin **Myyntipisteen toimintoprofiilit** -sivulla (**Vähittäismyynti \> Kanavan asetukset \> POS-asetukset \> POS-profiilit \> Toimintoprofiilit**). Valitse ensin **Muokkaa** ja sitten prosessi **Kirjanpidon rekisteröintiprosessi** -välilehden **Prosessin numero** -kentässä.
    2. Määritä yhdistimen tekniset profiilit laiteprofiiliin **POS-laiteprofiili** -sivulla (**Vähittäismyynti \> Kanavan asetukset \> POS-asetukset \> POS-profiilit \> Laite profiilit**). Valitse **Muokkaa**, lisää rivit **Kirjanpidon oheislaitteet** -välilehdessä ja valitse sitten yhdistimen tekninen profiili **Profiilin numero** -kentässä.

    > [!NOTE]
    > Voit lisätä useita teknisiä profiileja samaan laiteprofiiliin. Laiteprofiilia tai myyntipisteen toimintoprofiilia voi kuitenkin käyttää vain kerran samassa kirjanpidon yhdistinryhmässä.

    Kirjanpidon rekisteröinnin työnkulun määrittää kirjanpidon rekisteröintiprosessi sekä tietyt kirjanpidon integrointiosien osat: kirjanpitoasiakirjan toimittajan Commerce Runtime -laajennus ja kirjanpidon yhdistimen Hardware station -laajennus.

    - Kirjanpidon rekisteröinnin tapahtumien ja transaktioiden tilaus määritetään valmiiksi kirjanpitoasiakirjan toimittajassa.
    - Kirjanpitoasiakirjan toimittaja vastaa myös kirjanpidon rekisteröinnissä käytettävän kirjanpidon yhdistimen tunnistamisesta. Se yhdistää siihen kirjanpidon yhdistinryhmään sisältyvät yhdistimen toiminnalliset profiilit, joka on määritetty kirjanpidon rekisteröintiprosessin nykyiselle vaiheelle, siihen yhdistimen tekniseen profiilin, joka on määritetty myyntipisteeseen pariliitoksen muodostaneen laiteaseman laiteprofiiliin.
    - Kirjanpitoasiakirjan toimittaja käyttää kirjanpitoasiakirjan toimittajan määrityksen tietojen yhdistämisasetuksia transaktio- tai tapahtumatietojen, kuten verojen ja maksujen, muuntamiseen kirjanpitoasiakirjaa luotaessa.
    - Kun kirjanpitoasiakirjan toimittaja luo kirjanpitoasiakirjan, kirjanpidon yhdistin voi joko lähettää sen sellaisenaan kirjanpidon laitteeseen tai muuntaa sen sarjaksi laitteen ohjelmointirajapinnan komentoja. Valittu vaihtoehto perustuu siihen, miten tietoliikennettä käsitellään.

7. Vahvista kirjanpidon rekisteröintiprosessi **Kirjanpidon rekisteröintiprosessi** -sivulla (**Vähittäismyynti \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpidon rekisteröintiprosessit**) valitsemalla **Vahvista**.

    Tämän tyyppinen vahvistus kannattaa tehdä seuraavissa tapauksissa:
    
    - Uudessa rekisteröintiprosessissa sen jälkeen, kun kaikki asetukset ovat valmiita – myös silloin kun rekisteröintiprosessit määritetään myyntipisteen toiminnallisiin profiileihin ja laitteistoprofiileihin.
    - Aiemmin luodussa kirjanpidon rekisteröintiprosessissa tehtyjen muutosten jälkeen, kun kyseiset muutokset voivat aiheuttaa toisen kirjanpidon yhdistimen valinnan suorituksen aikana. (Näin voi tapahtua esimerkiksi silloin, kun kirjanpidon rekisteröintiprosessivaiheen yhdistinryhmä vaihdetaan, yhdistimen toiminnallinen profiili otetaan käyttöön yhdistinryhmässä tai yhdistimen uusi toiminnallinen profiili lisätään yhdistinryhmään.)
    - Yhdistimen teknisten profiilien laiteprofiileihin määrittämisessä tehtyjen muutosten jälkeen.

8. Siirrä tiedot kanavatietokantaan suorittamalla **Jakeluaikataulu** -sivulla **1070**- ja **1090**-työt.

## <a name="set-up-fiscal-texts-for-discounts"></a>Alennusten kirjanpitotekstien määrittäminen

Alennusta käytettäessä verokuittiin on joissakin tapauksissa tulostettava erityinen teksti. Voit määrittää alennusten kirjanpitotekstit **Kirjanpidon yhdistinryhmä** -sivulla (**Vähittäismyynti \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpidon yhdistinryhmä**).

- Jos kyse on manuaalisesti myyntipisteessä lisättävistä alennuksista, tietokoodin tai tietokoodiryhmän kirjanpitoteksti on määritettävä. Tämä tietokoodi määritetään myyntipisteen toimintaprofiilissa **Tuotealennus**-tietokoodina.

    1. Valitse **Kirjanpidon yhdistinryhmä** -sivulla **Verokuitin teksti**.
    2. Valitse **Tietokoodit**-välilehdessä ensin **Lisää** ja sitten tietokoodi tai tietokoodiryhmä.
    3. Valitse **Tietokoodin numero** -kohdassa arvo.
    4. Valitse **Alikoodin numero** -kentässä arvo, jos valittu tietokoodi edellyttää alikoodia.
    5. Määritä **Verokuitin teksti** -kentässä verokuittiin tulostettava kirjanpitoteksti.
    6. Valitse **Tulosta käyttäjän syöte verokuittiin** -asetukseksi **Kyllä**, jolloin verokuitin teksti korvataan käyttäjän myyntipisteessä manuaalisesti antamilla tiedoilla. Tämä asetus koskee vain tietokoodeja, joiden syötetyyppi on **Teksti**.

    > [!NOTE]
    > Voit määrittää kirjanpitotekstin useisiin tietokoodeihin sellaisia skenaarioita varten, joissa käytetään tietokoodiryhmiä. linkitettyjä tietokoodeja ja käynnistettyjä tietokoodeja. Näissä skenaarioissa verokuitissa on kirjanpitotekstiä kaikista siihen tapahtumariviin linkitetyistä tietokoodeista, jossa alennusta käytettiin.

- Kanavakohtaisissa alennuksissa alennustunnukselle on määritettävä kirjanpitoteksti.

    1. Valitse **Kirjanpidon yhdistinryhmä** -sivulla **Verokuitin teksti**.
    2. Valitse **Alennukset**-välilehdessä ensin **Lisää** ja sitten alennustunnus.
    3. Määritä **Verokuitin teksti** -kentässä verokuittiin tulostettava kirjanpitoteksti.

    > [!NOTE]
    > Jos samalle tapahtumariville käytetään useita alennuksia, verokuitissa on kirjanpitotekstiä kaikista kyseiseen tapahtumariviin linkitetyistä alennuksista.

## <a name="set-error-handling-settings"></a>Virheen käsittelyasetusten määrittäminen

Kirjanpidon integroinnissa käytettävissä olevat virheen käsittelyasetukset määritetään kirjanpidon rekisteröintiprosessissa. Lisätietoja virheen käsittelystä kirjanpidon integroinnissa on kohdassa [Virheen käsittely](fiscal-integration-for-retail-channel.md#error-handling).

1. Voit määrittää seuraavat parametrit kirjanpidon rekisteröinnin kullekin vaiheelle **Kirjanpidon rekisteröintiprosessi** -sivulla (**Vähittäismyynti \> Kanavan asetukset \> Kirjanpidon integrointi \> Kirjanpidon rekisteröintiprosessi**):

    - **Salli ohitus** – tämä parametri ottaa **Ohita**-asetuksen käyttöön virheen käsittelyn valintaikkunassa.
    - **Salli rekisteröidyksi merkitseminen** – tämä parametri ottaa **Merkitse rekisteröidyksi** -asetuksen käyttöön virheen käsittelyn valintaikkunassa.
    - **Jatka virheen ilmetessä** – Jos tämä parametri on käytössä, kirjanpidon rekisteröintiprosessi voi jatkua POS-rekisterissä, jos transaktion tai tapahtuman tilikausirekisteröinti epäonnistuu. Muussa tapauksessa operaattorin on suoritettava epäonnistunut tilikausirekisteröinti uudelleen, ohitettava se tai merkittävä transaktio tai tapahtuma rekisteröidyksi, jos haluaa suorittaa seuraavan transaktion tai tapahtuman tilikausirekisteröinnin. Lisätietoja on kohdassa [valinnainen tilikausirekisteröinti](fiscal-integration-for-retail-channel.md#optional-fiscal-registration).

    > [!NOTE]
    > Jos **Jatka virheen ilmetessä** -parametri on käytössä, **Salli Ohita**- ja **Salli Merkitse rekisteröidyksi** -parametrit ovat automaattisesti poissa käytöstä.

2. Virheen käsittelyn valintaikkunan **Ohita**- ja **Merkitse rekisteröidyksi** -asetukset edellyttävät **Salli rekisteröinnin ohitus tai rekisteröidyksi merkitseminen** -käyttöoikeuden. Ota tämän vuoksi **Salli ohita rekisteröinti tai rekisteröidyksi merkitseminen** -käyttöoikeus käyttöön **Käyttöoikeusryhmät** -sivulla (**Vähittäismyynti \> Työntekijät \> Käyttöoikeusryhmät**).
3. Käyttäjät voivat antaa **Ohita**- ja **Merkitse rekisteröidyksi** -asetuksilla lisätietoja siitä, milloin kirjanpidon rekisteröinti epäonnistuu. Voit ottaa tämän toiminnon käyttöön määrittämällä **Ohita**- ja **Merkitse rekisteröidyksi** -tietokoodit kirjanpidon yhdistinryhmässä. Käyttäjien antamat tiedot tallennetaan sitten kirjanpitotapahtumaan linkitettyjä tietokooditapahtumana. Lisätietoja tietokoodeista on kohdassa [Tietokoodit ja tietokoodiryhmät](../info-codes-retail.md).

    > [!NOTE]
    > **Tuotteen** käynnistintoimintoa ei tueta tietokoodeissa, joita käytetään **Ohita**- ja **Merkitse rekisteröidyksi** -asetuksina kirjanpidon yhdistinryhmissä.

    - Valitse **Kirjanpidon yhdistinryhmä**-sivun **Tietokoodit**-välilehdessä tietokoodit tai tietokooditryhmät **Ohita**- ja **Merkitse rekisteröidyksi** -kenttinä.

    > [!NOTE]
    > Kirjanpidon rekisteröintiprosessin missä tahansa vaiheessa voidaan luoda yksi kirjanpitoasiakirja ja yksi muu kuin kirjanpitoasiakirja. Kirjanpitoasiakirjan toimittajalaajennus tunnistaa jokaisen transaktio- tai tapahtumatyypin kirjanpitoasiakirjaan tai muuhun kuin kirjanpitoasiakirjaan liittyväksi. Virheen käsittelytoiminto koskee vain kirjanpitoasiakirjoja.
    >
    > - **Kirjanpitoasiakirja** – pakollinen asiakirja, jonka rekisteröitymisen on onnistuttava (esimerkiksi verokuitti).
    > - **Muu kuin kirjanpitoasiakirja** – transaktion tai tapahtuman täydentävä asiakirja (esimerkiksi lahjakortti).

4. Jos operaattorin on voitava jatkaa nykyisen toiminnan käsittelyä (esimerkiksi tapahtuman luominen tai viimeistely) kuntotarkastuksen virheen jälkeen, sen on otettava käyttöön **Salli kuntotarkistuksen virheen ohitus** -käyttöoikeudet **Käyttöoikeusryhmät** -sivulla (**Retail \> työntekijät \> käyttöoikeusryhmät**). Saat lisätietoja kuntotarkastusmenettelystä kohdasta [Tilikausirekisteröinnin kuntotarkastus](fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

## <a name="set-up-fiscal-xz-reports-from-the-pos"></a>Kirjanpidon X/Z-raporttien määrittäminen myyntipisteessä

Kirjanpidon X/Z-raporttien suorittaminen myyntipisteestä edellyttää, että myyntipisteen asetteluun lisätään uusia painikkeita.

- Asenna suunnitteluohjelma ja päivitä myyntipisteen asettelu **Painikeruudukot**-sivulla noudattamalla kohdan [Mukautetun toimintopainikkeen lisääminen myyntipisteen asetteluun Retail Headquarters -sovelluksessa](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) ohjeita.

    1. Valitse päivitettävä asettelu. 
    2. Lisää uusi painike, määritä **Tulosta kuitti X** -painikeominaisuus.
    3. Lisää uusi painike ja määritä **Tulosta kuitti Z** -painikeominaisuus.
    4. Siirrä muutokset kanavatietokantaan suorittamalla työ **1090** **Ajastuksen jakelu** -sivulla.

## <a name="enable-manual-execution-of-postponed-fiscal-registration"></a>Ota käyttöön lykätyn tilikausirekisteröinnin manuaalinen käyttö

Jos haluat ottaa käyttöön lykätyn tilikausirekisteröinnin manuaalisen käytön, lisää uusi painike POS-asetteluun.

- Asenna suunnitteluohjelma ja päivitä myyntipisteen asettelu **Painikeruudukot**-sivulla noudattamalla kohdan [Mukautetun toimintopainikkeen lisääminen myyntipisteen asetteluun Retail Headquarters -sovelluksessa](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) ohjeita.

    1. Valitse päivitettävä asettelu.
    2. Lisää uusi painike, määritä **Viimeistele tilikausirekisteröintiprosessi** -painikeominaisuus.
    3. Siirrä tekemäsi muutokset kanavatietokantaan suorittamalla työ **1090** **Ajastuksen jakelu** -sivulla.
