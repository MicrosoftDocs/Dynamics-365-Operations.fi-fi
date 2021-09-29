---
title: Ota aiemmin luotujen tuotteiden muutostenhallinta käyttöön
description: Tässä ohjeaiheessa kerrotaan, miten voit ottaa muutostenhallinta käyttöön aiemmin luoduille tuotteille. Siinä kuvataan myös tapauksia, joissa muutostenhallinnan käyttöönottoa on rajoitettu.
author: t-benebo
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-05-02
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 45c5774ac1f6db5845d6be6bf2f5d8f99063ea07
ms.sourcegitcommit: 7a2001e4d01b252f5231d94b50945fd31562b2bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/15/2021
ms.locfileid: "7488199"
---
# <a name="enable-change-management-on-existing-products"></a>Ota aiemmin luotujen tuotteiden muutostenhallinta käyttöön

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten voit ottaa muutostenhallinta käyttöön aiemmin luoduille tuotteille. Siinä kuvataan myös tapauksia, joissa muutostenhallinnan käyttöönottoa on rajoitettu.

Kun otat muutostenhallinnan käyttöön aiemmin luodulle tuotteelle, voit luoda tuotteesta eri versioita ja seurata siihen tehtyjä muutoksia sen koko elinkaaren ajalta. Näin voit seurata näitä muutoksia käyttämällä muutostilauksia. Sinun täytyy muuntaa tuotteet *suunnittelunimikkeiksi* (joita kutsutaan myös suunnittelutuotteiksi) ottaaksesi muutostenhallinnan niille käyttöön. Suunnittelutuotteet ovat tuotteita, jotka on versioitu ja joita hallitaan muutostenhallinnan avulla. Ohjattu toiminto opastaa sinua muuntoprosessissa.

## <a name="turn-on-the-feature-in-your-system"></a>Toiminnon ottaminen käyttöön järjestelmässä

Sinun täytyy suorittaa seuraavat toimet käyttääksesi tätä ominaisuutta:

1. Ota käyttöön Suunnittelun muutostenhallinta -ominaisuus ja sen konfigurointiavain, niin kuin aiheessa[Suunnittelun muutostenhallinnan yleiskatsaus](product-engineering-overview.md) on kuvattu.
1. Ota käyttöön *Ota aiemmin luotujen tuotteiden muutostenhallinta käyttöön* -ominaisuus toiminnon hallinnasta. Lisätietoja on kohdassa [Toiminnon hallinnan yleiskatsaus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="restrictions-and-limitations"></a>Rajoitukset

Kaikkia tuotetyyppejä ei voi muuntaa kaikiksi muiksi tyypeiksi. Seuraavat rajoitukset ovat voimassa:

- Kun muunnat tuotteen suunnittelutuotteeksi, se pysyy *tuotteena*. Siitä ei tule *päätuotetta*.
- Kun muunnat päätuotteen, jolla on tietty dimensiojoukko, dimensiot säilyvät muutoksen jälkeen. Jos muunnat esimerkiksi päätuotteen, jolla on kokodimensio, se säilyttää kokodimension.

Jos sinulla on siis erillinen tuote, voit muuttaa sen vain suunnittelutuotteeksi, joka ei seuraa tuotedimensiota tapahtumissa (eli versiodimensiota ei käytetä). Katso lisätietoja näistä ongelmista tämän aiheen myöhemmistä osioista.

## <a name="prepare-for-conversion-by-creating-all-required-engineering-product-categories"></a>Valmistaudu muuntamiseen luomalla kaikki tarvittavat suunnittelun tuoteluokat

Jokaiselle suunnittelutuotteelle täytyy kohdistaa *suunnittelun tuoteluokka*. Teet tämän kohdistuksen, kun suoritat ohjatun **Muunna suunnittelutuotteeksi** -toiminnon. Kaikilla asiaankuuluvilla vakiotuotteilla täytyy olla suunnittelun tuoteluokat *ennen* kuin voit muuntaa kyseiset tuotteet.

Suunnittelun tuoteluokka tarjoaa perustan suunnittelutuotteen luomiseksi, ja se määrittää joukon oletusarvoja ja käytäntöjä. Tuloksena syntyvässä suunnittelutuotteessa käytetään myös suunnittelumääritteitä ja niiden (suunnitteluluokalle määritettyjä) oletusarvoja. Voit muokata määritteiden arvoja ja/tai lisätä tuloksena syntyvään tuotteeseen lisää suunnittelumääritteitä tarpeen mukaan.

Suunnittelun tuoteluokan täytyy vastata tuotetta, johon kohdistat sen. Esimerkiksi tuotetyypin ja dimensioryhmän täytyy vastata sekä tuotetta että sen suunnittelun tuoteluokkaa. Lisätietoja on kohdassa [Suunnitteluversiot ja suunnittelun tuoteluokat](engineering-versions-product-category.md).

> [!IMPORTANT]
> Ohjattu **Muunna suunnittelutuotteeksi** -toiminto voi muuntaa tuotteen vain suunnittelutuotteisiksi, joissa versiota ei seurata tapahtumissa. Tästä syystä **Versioiden seuranta tapahtumissa** -vaihtoehdoksi täytyy määrittää *Ei* suunnittelun tuoteluokille, joita luot nykyisten tuotteiden muuntamista varten.

Lisätietoja suunnittelun tuoteluokkien luomisesta on kohdassa [Suunnitteluversiot ja suunnittelun tuoteluokat](engineering-versions-product-category.md).

## <a name="run-the-convert-to-engineering-product-wizard"></a>Ohjatun Muunna suunnittelutuotteeksi -toiminnon käyttäminen

Ohjattu **Muunna suunnittelutuotteeksi** -toiminto auttaa sinua muuntamaan yhden tai useamman nykyisen tuotteen suunnittelutuotteisiksi. Se muuntaa tuotteet suunnittelutuotteiksi (versioiduiksi tuotteiksi), joissa versiota ei seurata tapahtumissa (eli versiodimensiota ei käytetä). Kun muunnos on valmis, voit hallita tuotteita käyttämällä Suunnittelun muutostenhallinta -ominaisuutta.

Muunnos on pysyvä. Et voi siis kumota sitä myöhemmin. 

Muunnetut suunnittelutuotteet vapautetaan jatkossakin samoissa yrityksissä, joissa alkuperäinen tuote vapautettiin. Suunnittelun tuoterakennetta (BOM) tai reittejä ei kuitenkaan vapauteta automaattisesti kyseisille yrityksille.

Noudata näitä ohjeita suorittaaksesi ohjatun **Muunna suunnittelutuotteeksi** -toiminnon ja muuntaaksesi tuotteen suunnittelutuotteeksi.

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Valitse muunnettavien tuotteiden valintaruudut ruudukosta.
1. Avaa ohjattu toiminto valitsemalla toimintoruudun **Suunnittele**-välilehden **Suunnittelun muutostenhallinta** -ryhmästä **Muunna suunnittelutuotteeksi**.
1. Ohjatun toiminnon ensimmäinen sivu on **Tervetuloa**-sivu. Jos muunnosprosessi ei ole sinulle vielä tuttu, lue tällä sivulla olevat tiedot huolellisesti läpi. Kun olet valmis jatkamaan, valitse **Seuraava**.
1. **Valitse muunnettavien tuotteiden tiedot** -sivulla näytetään tuotteet, jotka valitsit ennen ohjatun toiminnon avaamista. Tarkasta luettelo. Käytä työkalurivin **Uusi**- ja **Poista**-painikkeita lisätäksesi tai poistaaksesi tuotteita tarvittaessa.
1. Käytä seuraavia ruudukon ylälaidassa olevia kenttiä määrittääksesi oletusarvoja luettelossa oleville tuotteille. (Voit muuttaa näitä arvoja yksittäisille tuotteille muunnoksen jälkeen). Oletusarvoja ei voi kohdistaa tuotteille, joille on jo määritetty asiaankuuluva arvo.

    - **Oletusarvoinen suunnitteluluokka** – Valitse alustava suunnittelun tuoteluokka, joka kohdistetaan luettelon kaikille tuotteille. Valitsemaasi luokkaa käytetään kaikille tuotteille, jotka ovat yhteensopivia sen kanssa.
    - **Oletusversio** – Määritä alustava tuoteversio, joka kohdistetaan luettelon kaikille tuotteille. Jokaisella suunnittelutuotteella on vähintään yksi suunnitteluversio.
    - **Elinkaaren oletustila** – Valitse alustava tuotteen elinkaaren tila, joka kohdistetaan luettelon kaikille tuotteille.
    - **Nykyistä tuoterakennetta käytetään suunnittelutuotteessa** – Valitse tämä valintaruutu, jos luettelon tuotteiden nykyistä tuoterakennetta tulisi käyttää suunnittelutuotteen tuoterakenteena.

    Katso lisätietoja tuoteasetuksista seuraavasta vaiheesta.

1. Tarkista kaikki ruudukossa olevat tuotteet ja arvioi, kuinka hyvin niille määrittämäsi oletusarvot sopivat niille. Tarkista kultakin riviltä seuraavat tiedot ja määritä tarvittavat kentät:

    - **Tuotenumero** – Tuotenumero.
    - **Tuotteen nimi** – Tuotteen nimi.
    - **Suunnitteluluokka** – Valitse suunnittelun tuoteluokka, johon tuotteen tulisi kuulua sen muuntamisen jälkeen. Jokaiselle tuotteelle täytyy olla sopiva luokka, niin kuin tämän aiheen edellisessä osiossa kuvattiin. Sinun täytyy määrittää luokka jokaiselle tuotteelle.
    - **Versio** – Syötä tuoteversio, joka kohdistetaan tuotteelle sen muuntamisen jälkeen. Voit esimerkiksi valita numeron, joka sopii luokkasi tällä hetkellä käyttämään numerojärjestykseen. Kuhunkin suunnitteluversioon tallennetaan versiokohtaisia suunnitteluun liittyviä tietoja. Lisätietoja on kohdassa [Suunnitteluversiot ja suunnittelun tuoteluokat](engineering-versions-product-category.md).
    - **Tuotteen elinkaaren tila** – Valitse tuotteen elinkaaren tila, jossa tuotteen tulisi olla sen muuntamisen jälkeen. Tuotteen elinkaaren tila sallii sinun hallita, mitkä tapahtumat sallitaan tietylle suunnitteluversiolle. Lisätietoja on kohdassa [Tuotteen elinkaaren tilat ja tapahtumat](product-lifecycle-state-transactions.md).
    - **Sisältää tuoterakenteen** – Valittu valintamerkki osoittaa, että tuotteella on tuoterakenne. Tämän valintaruudun asetuksella voit päättää, miten nykyinen **Nykyistä tuoterakennetta käytetään suunnittelutuotteessa** -valintaruutu määritetään.
    - **Nykyistä tuoterakennetta käytetään suunnittelutuotteessa** – Valitse tämä valintaruutu, jos tuotteen nykyistä tuoterakennetta tulisi käyttää suunnittelutuotteen tuoterakenteena. Tämän jälkeen tuoterakennetta hallitaan Suunnittelun muutostenhallinta -ominaisuudella. Jos tuotteella ei ole tuoterakennetta tai haluat luoda tuoterakenteen muunnetulle tuotteelle myöhemmin manuaalisesti, poista tämän valintaruudun valinta.
    - **Sisältää virheitä** – Valittu valintaruutu osoittaa, että tuoteasetuksissa on yksi tai useampi virhe. Esimerkiksi tuotetyyppi tai dimensioryhmä ei ehkä vastaa luokan tuotetyyppiä tai dimensioryhmää. Virheelliset tuotteet ohitetaan eikä niitä muunneta.

1. Kun olet valmis, vahvista tuoteasetukset valitsemalla työkaluriviltä **Vahvista**. Jokaisen rivi **Sisältää virheitä** -valintaruutu päivitetään osoittamaan tuotteen tila. Säädä arvoja, kunnes tuotteiden asetuksissa ei ole enää virheitä.
1. Kun kaikki tuotteet on määritetty oikein, jatka valitsemalla **Seuraava**.
1. **Vahvista valinta** -sivulla näytetään niiden tuotteiden määrä, joiden asetuksissa ei ole virheitä ja jotka ovat siis valmiita muunnosta varten. Siinä näytetään myös niiden tuotteiden määrä, jotka ohitetaan virheiden vuoksi. Jos haluat suorittaa muunnoksen erätyönä, määritä **Suorita erässä** -vaihtoehdoksi *Kyllä*.
1. Valitse **Valmis**, kun haluat ottaa asetuksesi käyttöön ja aloittaa tuotteiden muuntamisen suunnittelutuotteiksi.

> [!NOTE]
> Jos järjestelmäsi on määritetty hyväksymään tuotteet manuaalisesti ennen niiden vapautusta, sinun täytyy hyväksyä jokainen muunnettu tuote käyttämällä asiaankuuluvien yritysten **Avaa tuotevapautukset** -sivua. Lisätietoja on kohdassa [Tuotteen tarkistaminen ja hyväksyminen ennen vapauttamista paikalliselle yhtiölle](engineering-scenarios.md#accept).
