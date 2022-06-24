---
title: Warehouse Management ‑mobiilisovelluksen vaiheiden otsikoiden ja ohjeiden mukauttaminen
description: Tässä artikkelissa käsitellään kunkin Warehouse Management -mobiilisovelluksen määritetyn tehtävätyönkulun kunkin vaiheen mukautettujen ohjeiden luontia ja näyttämistä.
author: Mirzaab
ms.date: 08/11/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-11
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 289a3735133919ae7dbad05c40ba9ccf0e8f57ca
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895493"
---
# <a name="customize-step-titles-and-instructions-for-the-warehouse-management-mobile-app"></a>Warehouse Management ‑mobiilisovelluksen vaiheiden otsikoiden ja ohjeiden mukauttaminen

> [!IMPORTANT]
> Tässä artikkelissa käsitellyt toiminnot koskevat vain uutta Warehouse Management -mobiilisovellusta. Niillä ei ole vaikutusta vanhaan varastosovellukseen, joka on nyt vanhentunut.

Tässä artikkelissa käsitellään jokaisen Warehouse Management -mobiilisovellukseen määritetyn tehtävätyönkulun jokaisen vaiheen mukautettujen ohjeiden luontia ja näyttämistä. Kun varastotyöntekijöiden käytössä on hyvin kirjoitettuja ohjeita, he voivat aloittaa heti uusien työnkulkujen käyttämisen ilman edeltävää koulutusta. Tämän toiminnon edut:

- **Työntekijät pääsevät alkuun entistä nopeammin, sillä he voivat toimia selkeiden ohjeiden mukaan tehtävän jokaisessa vaiheessa.** Työnkulun jokaisessa vaiheessa annetaan ohjeita, joiden avulla kenttätyöntekijät ymmärtävät, mistä tehtävässä on kyse.
- **Ohjeet vastaavat omia prosesseja.** Omat ohjeet kirjoitetaan omien liiketoiminta- ja varastoprosessien mukaisesti. Terminologia voi esimerkiksi perustua käytössä olevaan fyysiseen tilaan ja paikallisiin lyhenteisiin.

## <a name="turn-on-the-warehouse-app-step-instructions-feature"></a>Varastosovelluksen vaiheiden ohjetoiminnon ottaminen käyttöön

Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi. Järjestelmänvalvojat voivat tarkistaa toiminnon tilan ja ottaa sen käyttöön [ominaisuuksien hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetusten avulla. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Toiminnon nimi:** *Varastosovelluksen vaiheohjeet*

## <a name="step-titles-and-step-instructions-in-the-app"></a>Vaiheiden otsikot ja ohjeet sovelluksessa

Tehtävätyönkulun jokaisella vaiheella on Warehouse Management -mobiilisovelluksessa vaihetunnus. Lisäksi jokaisella vaiheella on otsikko, kuvake ja ohje. (Lisätietoja on kohdassa [Vaiheiden kuvakkeiden ja otsikoiden määrittäminen Warehouse Management -mobiilisovelluksessa](step-icons-titles.md).)

### <a name="step-titles"></a>Vaiheiden otsikot

*Vaiheen otsikko* on lyhyt kuvaus siitä, mitä työntekijän on tehtävä vaiheen aikana. Se näkyy suurikokoisena tekstinä näytön yläreunassa, kuten seuraavassa kuvassa.

![Esimerkki vaiheen otsikosta Warehouse Management -mobiilisovelluksessa](media/wma-step-title.png "Esimerkki vaiheen otsikosta Warehouse Management -mobiilisovelluksessa")

> [!TIP]
> Koska tekstikoko on suuri, vaiheen otsikko kannattaa pitää mahdollisimman lyhyenä. Muussa tapauksessa teksti voi katketa. Jos otsikko pitkä, työntekijät voivat kuitenkin avata koko tekstin sisältävän valintaikkunan pitämällä otsikko painettuna.

### <a name="step-instructions"></a>Vaiheen ohjeet

*Vaiheen ohje* on pitkä kuvaus, jossa on lisätietoja siitä, mitä työntekijän on vaiheen aikana tehtävä. Se näkyy ponnahdusikkunassa, kuten seuraavassa kuvassa.

![Esimerkki vaiheen ohjeesta Warehouse Management -mobiilisovelluksessa](media/wma-step-instructions.png "Esimerkki vaiheen ohjeesta Warehouse Management -mobiilisovelluksessa")

Vaiheen ohje tulee automaattisesti näkyviin, kun vaihe avataan. Työntekijät voivat hylätä sen napauttamalla jotakin kohtaa ponnahdusikkunan ulkopuolella. Valintaikkunassa on myös **Älä näytä uudelleen** -valintaruutu, jonka valitsemalla työntekijät voivat estää ohjeen avautumisen, kun he suorittavat saman tehtävän seuraavan kerran.

## <a name="load-the-default-setup"></a>Oletusasetusten lataaminen

Kun *Varastosovelluksen vaiheiden ohjeet* -toiminto otetaan käyttöön ensimmäisen kerran, järjestelmässä ei ole mitään mukautettavia vaiheen otsikoita tai ohjeita. Tämän vuoksi ensimmäisenä on ladattava oletusasetukset. Oletusasetukset sisältävä kaikkien käytettävissä olevien vaihetunnusten tekstit kaikilla tuetuilla kielillä. Oletusasetukset ladataan seuraavasti:

1. Valitse **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen vaiheet**.
1. Valitse toimintoruudussa **Luo oletusasetukset**. Vakiovaiheet lisätään sivulle.

## <a name="customize-step-titles-and-instructions"></a>Vaiheiden otsikoiden ja ohjeiden mukauttaminen

Vaiheen otsikkoa ja/tai ohjetta voi mukauttaa valituissa kielissä seuraavasti:

1. Valitse **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen vaiheet**.

    **Mobiililaitteen vaiheet** -sivulla on luettelo, joka sisältää jokaisen järjestelmässä käytettävissä olevan vaiheet. Kukin vaihetunnus voi jakaa rajoituksetta mobiililaitteen valikkovaihtoehtojen kesken. Jos vaihetunnusta käytetään useissa valikkovaihtoehdoissa, sama otsikko ja ohje näytetään kaikissa kyseisissä valikkovaihtoehdoissa. Tiettyjen valikkovaihtoehtojen otsikko ja ohjeita voi kuitenkin mukauttaa ohituksia luomalla. (Lisätietoja on seuraavassa osassa.)

    Ruudukko sisältää seuraavat sarakkeet:

    - **Valikkovaihtoehdon nimi** – Riveillä, joissa tämä sarake on tyhjä, käytetään vaiheen oletusotsikkoa ja -ohjeita, ja ne koskevat kaikkia niitä mobiililaitteen valikkovaihtoehtoja, joille ei ole määritetty ohitusta. Riveillä, joissa tähän sarakkeeseen on määritetty valikkovaihtoehdon nimi, käytetään vain määritettyjä valikkovaihtoehtoa koskevia ohituksia.
    - **Vaiheen tunnus** – vaiheen yksilöivä tunnus.
    - **Syötteen otsikko** – Otsikko, joka näytetään, kun sovellus pyytää uusia tietoja. Sivun kentät ovat yleensä tyhjiä (eli niillä ei ole esimääritettyjä arvoja).
    - **Vahvistuksen otsikko** – Otsikko, joka näytetään, kun sovellus pyytää vahvistamaan järjestelmään jo tallennetun arvon. Sivun kentissä on yleensä esimääritetyt arvot.

1. Etsi muokattavat **Vaiheen tunnus**- ja **Valikkovaihtoehdon nimi** -arvot ja valitse arvo **Vaiheen tunnus** -sarakkeessa. Avautuvalla sivulla on luettelo kaikista valitun vaiheen otsikon ja ohjeen käytettävissä olevista käännöksistä.
1. Mukauta minkä tahansa kielen tekstiä seuraavien ohjeiden mukaan. Kummallakin vaihtoehdolla voi muokata nykyisten kielten tekstiä. Kuitenkin vain ensimmäisellä vaihtoehdolla voi lisätä tekstiä uusiin kieliin, sillä toisella vaihtoehdolla voi tarkastella ja muokata kaikkia valitun kielen aiemmin luotuja valikkokohtaisia ohituksia.

    - Avaa valintaikkuna, jossa voi lisätä tai muokata tekstiä millä tahansa tuetulla kielellä, valitsemalla työkalurivillä **Lisää**. Valitse **Viitekieli**-kentässä kieli, jonka arvoja halutaan tarkastella. Arvot näkyvät vasemmassa sarakkeessa. Valitse **Käännösten kieli** -kentässä lisättävä tai mukautettava kieli. Muokkaa oikeassa sarakkeessa tarpeen mukaan **Syötteen otsikko**-, **Syötteen ohje**-, **Vahvistuksen otsikko**- ja **Vahvistuksen ohje** -kenttien arvoja. Valitse sitten **OK**.
    - Etsi ja valitse ruudukossa rivi, jossa **Kieli**-kentän määrityksenä on muokattava kieli. Valitse työkalurivillä **Näytä tämän vaiheen käännökset: &lt;kieli&gt;**. Avautuvassa valintaikkunassa voi muokata kaikkia valitun kielen ohitustekstejä. Valintaikkunassa on ruudukko, jossa on rivit sekä vakioteksteille (joissa **Valikkovaihtoehdon nimi** -kenttä on tyhjä) että kullekin käytettävissä olevassa ohitustekstille (jossa **Valikkovaihtoehdon nimi** -kentässä sen valikkovaihtoehdon nimi, jota ohitus koskee). Muokkaa tarpeen mukaan **Syötteen otsikko**-, **Syötteen ohje**-, **Vahvistuksen otsikko**- ja **Vahvistuksen ohje** -kenttien arvoja. Valitse sitten **OK**.

1. Toimi vastaavasti siihen saakka, että jokainen tarvittava otsikko ja ohje on määritetty jokaisella tarvittavalla kielellä.

## <a name="add-menu-specific-overrides"></a>Valikkokohtaisten ohitusten lisääminen

Kuten edellisessä osassa mainittiin, kullekin vaiheen tunnukselle voidaan luoda tarvittava määrä valikkokohtaisia ohituksia. Tämän ominaisuuden avulla voidaan muokata ja muuttaa ohjetta siten, että se vastaa paremmin tietyn valikkovaihtoehdon paikallista liiketoimintaprosessia. Jos yritys esimerkiksi yleensä antaa työntekijöille työtunnuksen tulostettuna asiakirjana myynnin keräilyä varten, työntekijöille voidaan antaa vihje, että ensimmäiseksi kannattaa skannata työtunnus.

Kutakin ohitusta käytetään tietyssä mobiililaitteen valikkovaihtoehdossa, eikä sen käännösten määrää ole rajoitettu. Jos valikkovaihtoehdolla ei ole ohitusta, siinä käytetään vakiotekstejä. Jos ohitusta ei ole käännetty jollekin kielelle, käytetään vakiotekstejä myös valikkovaihtoehdoissa, jossa ohitus on määritetty muille kielille.

Ohitus luodaan ja määritetään seuraavasti:

1. Valitse **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen vaiheet**.
1. Etsi ja valitse ruudukossa rivi, jolle ohitus luodaan.
1. Valitse toimintoruudussa **Luo vaiheen määritys**.
1. Määritä avattavassa **Lisää vaiheen määritys** -ikkunassa **Valikkovaihtoehto**-kenttään sen mobiililaitteen valikkovaihtoehdon nimi, jota ohitus koskee. Valitse sitten **OK**.
1. Avautuvalla sivulla näkyy kaikki tekstit, jotka ovat käytettävissä uudessa ohituksessa. Aluksi luodaan vain yksi kieli. Kaikki muut kielet jatkavat vakiotekstien käyttämistä, ellei kyseisiä kieliä lisätä tässä kohdassa. Muokkaa tekstejä ja lisää uusia kieliä tarpeen mukaan edellisessä osassa kuvatulla tavalla.
