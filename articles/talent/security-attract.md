---
title: Käyttöoikeuksien ja roolien hallinta Attractissa
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talent - Attractin käyttöoikeusrooleja.
author: andreabichsel
manager: AnnBe
ms.date: 03/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: ad94a7511afef0c68fb8f2a70402babb80b0f9ad
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024191"
---
# <a name="set-user-permissions"></a>Aseta käyttöoikeudet

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 Talent: Attract käyttää rooleihin perustuvia käyttöoikeuksia. Käyttöoikeuksia ei siis myönnetä yksittäisille käyttäjille vaan käyttöoikeusrooleille, joita määritetään käyttäjille. Käyttäjä, jolle on määritetty käyttöoikeusrooli, saa kyseiseen rooliin liitetyt käyttöoikeudet.

Attractissa viisi peruskäyttäjäroolia:

- Järjestelmänvalvoja
- Työhön ottava esimies
- Työhönottaja
- Haastattelija
- Vain luku

Ainoastaan järjestelmänvalvojan rooliin sisältyy oikeus lisätä muita käyttäjiä ja muuttaa heidän käyttöoikeuksiaan.

- **Lisää** – valitse hallintakeskuksessa **Käyttöoikeudet**-välilehdessä **Määritä rooleja**, etsi lisättävä käyttäjä ja määritä sitten käyttöoikeudet kyseiselle käyttäjälle.
- **Muokkaa** – tee käyttäjähaku tai etsi käyttäjä luettelosta ja valitse sitten **Muokkaa**, jonka jälkeen voit muuttaa kyseisen käyttäjän oikeuksia.
- **Poista** – Käyttäjää ei poisteta järjestelmästä, vaikka hänen käyttöoikeutensa poistetaan. Voit kuitenkin rajoittaa käyttäjän oikeuksia Attractissa. Esimerkki: Hildalle on määritetty työhön ottavan esimiehen rooli ja hänet on lisätty työhön työhön ottavana esimiehenä. Jos Hilda poistetaan myöhemmin työhön ottavan esimiehen roolista, hän on edelleen työn työhön ottava esimies ja hän voi edelleen käyttää kyseistä työtä. Hilda ei kuitenkaan voi luoda muita töitä.

Seuraavissa osissa kutakin roolia käsitellään yleistasolla. Ohjeaiheessa jäljempinä olevissa taulukoissa on niistä lisätietoja.

> [!NOTE]
> Joitakin ominaisuuksia voi käyttää vain Attractin kattavan työhönottolaajennuksen kanssa.

## <a name="administrator"></a>Järjestelmänvalvoja

Käyttäjät, joille on määritetty järjestelmänvalvojan rooli, voivat käyttää ja muuttaa kaikkia Attractin tietoja. Järjestelmänvalvojat voit luoda, lukea, päivittää ja poistaa tietoja. Heillä on myös pääsy hallintakeskukseen, josta he voivat muokata Attract-asetuksia ja määrittää käyttäjätietoja. On suositeltavaa, että ainakin yhdelle henkilölle määritettään järjestelmänvalvojan rooli. Microsoft PowerAppsin ympäristön järjestelmänvalvoja määritetään oletusarvoisesti Attractin järjestelmänvalvojaksi. Jos rekisteröidyit Attractin kokeiluversioon, sinulle on määritetty järjestelmänvalvojan rooli automaattisesti. Tällä hetkellä töiden luontia varten järjestelmänvalvojan roolin lisäksi käyttäjällä on oltava joko työhönottajan tai työhön ottavan esimiehen rooli.

## <a name="hiring-manager"></a>Työhön ottava esimies

Käyttäjät, jolle on määritetty työhön ottavan esimiehen rooli, voivat luoda töitä ja päivittää aiemmin luomiaan töitä. Työhön ottavat esimiehet voivat suorittaa vain muutamia toimenpiteitä työssä ja siihen liitetyissä hakemuksissa. Vain käyttäjät, joille on määritetty työhön ottavan esimiehen rooli, voidaan lisätä työhönottoryhmään työhön ottavina esimiehinä.

## <a name="recruiter-role"></a>Työhönottajan rooli

Käyttäjillä, joille on määritetty työhönottajan rooli, on luomiensa töiden täydet luku-, luonti-, päivitys- ja poisto-oikeudet. Heillä on myös heidän omistamiin töihin liitettyjen hakemusten täydet luonti-, luku-, päivitys- ja poisto-oikeudet. Vain käyttäjät, joille on määritetty työhönottajan rooli, voidaan lisätä työhönottoryhmään työhönottajina.

## <a name="interviewer"></a>Haastattelija

Jokainen käyttäjä, jolla on organisaatiossa Microsoft Azure Active Directory (Azure AD) -tili, voidaan lisätä työhönottoryhmään haastattelijana. Käyttäjät, joille on määritetty haastattelijan rooli, voivat tarkastella oman työhönottoryhmänsä työn ja työn hakijan tietoja. Haastattelijat voivat myös tehdä kyseisissä töissä työhönottosuosituksia ja antaa palautetta hakijoista. He eivät kuitenkaan voi päivittää työn tai hakijan tietoja.

## <a name="read-only"></a>Vain luku

Käyttäjille, joille on määritetty vain luku -rooli, on kaikkien Attract-ympäristön tietojen lukuoikeus. He eivät kuitenkaan voi luoda tai muokata mitään tietoja.

## <a name="find-out-which-roles-you-have"></a>Selvitä, mitkä roolit sinulla on

1.  Napsauta kysymysmerkkiä (**?**) Attractissa sivun oikeassa yläkulmassa.

2.  Valitse **tietoja**.

    Näyttöön tulevasta ikkunasta näet, mitkä roolit sinulla on Attractissa:

    ![Näytä Attract-käyttöoikeuden laji](media/attract-license-types.png)
    
## <a name="delegated-roles"></a>Delegoidut roolit

Työhönottajat ja työhön ottavat esimiehet voivat määrittää kunkin työn työhönottoryhmässä itselleen yhden tai usean edustajan. He eivät voi kuitenkaan määrittää edustajia muille työhönottoryhmän jäsenille.

Edustajilla on samat käyttöoikeudet kuin määrityksen tehneellä henkilöllä. Jos esimerkiksi työhön ottava esimies määrittää itselleen työtä varten edustajan, edustajalla on samat käyttöoikeudet kuin kyseisen työn työhön ottavalla esimiehellä. Edustajat eivät voi poistaa muista edustajia työhönottoryhmästä. He eivät voi myöskään poistaa henkilöä, joka määritti heidät edustajaksi.

## <a name="job-details-and-actions"></a>Työn tiedot ja toiminnot

Käyttäjät, joille on määritetty työhönottajan tai työhön ottavan esimiehen rooli, voivat luoda töitä. Seuraavat käyttöoikeudet koskevat työn tietoja ja toimintoja, joita voidaan käyttää töissä.

| Tiedot tai toiminto    | Työhönottaja | Työhön ottava esimies | Haastattelija |
|-------------------|-----------|----------------|-------------|
| Työn tiedot       | Niiden töiden luonti, lukeminen, päivitys ja poisto, joiden työhönottoryhmässä käyttäjä on | Niiden töiden luonti, lukeminen, päivitys ja poisto, joiden työhönottoryhmässä käyttäjä on | Vain luku |
| Työhönottoryhmä       | Niiden töiden luonti, lukeminen, päivitys ja poisto, joiden työhönottoryhmässä käyttäjä on | Niiden töiden luonti, lukeminen, päivitys ja poisto, joiden työhönottoryhmässä käyttäjä on | Vain luku |
| Työpaikkailmoitus       | Niiden töiden luonti, lukeminen, päivitys ja poisto, joiden työhönottoryhmässä käyttäjä on | Vain luku | Vain luku |
| Prosessoi           | Niiden töiden luonti, lukeminen, päivitys ja poisto, joiden työhönottoryhmässä käyttäjä on | Niiden töiden luonti, lukeminen, päivitys ja poisto, joiden työhönottoryhmässä käyttäjä on | Vain luku |
| Lisää hakija    | Hakijoiden lisääminen töihin, joiden työhönottoryhmässä käyttäjä on | Hakijoiden lisääminen töihin, joiden työhönottoryhmässä käyttäjä on | Ei sallittu |
| Lisää potentiaalinen ehdokas     | Potentiaalisten ehdokkaiden lisääminen töihin, joiden työhönottoryhmässä käyttäjä on | [Potentiaalinen ehdokas -tehtävän asetusten](./activities-attract.md#prospect-activity) määritysvaihtoehto määrittää, voivatko haastattelijat lisätä ja tarkastella potentiaalisia ehdokkaita | Ei sallittu |
| Aktivoi työ      | Niiden töiden aktivointi, joiden työhönottoryhmässä käyttäjä on | Niiden töiden aktivointi, joiden työhönottoryhmässä käyttäjä on | Ei sallittu |
| Sulje työ         | Niiden töiden sulkeminen, joiden työhönottoryhmässä käyttäjä on | Ei sallittu | Ei sallittu |
| Poista työ        | Niiden töiden poistaminen, joiden työhönottoryhmässä käyttäjä on | Vain jos työhön ei ole lisätty yhtään hakijaa | Ei sallittu |
| Poista hakijoita | Hakijoiden poistaminen, jos käyttäjä on työhönottoryhmässä | Ei sallittu | Ei sallittu |

## <a name="application-details-and-actions"></a>Hakemuksen tiedot ja toiminnot

Seuraavat käyttöoikeudet koskevat hakijoiden työkohtaisia tietoja ja toimintoja, joita voidaan käyttää hakemuksissa.

| Tiedot tai toiminto          | Työhönottaja | Työhön ottava esimies | Haastattelija |
|-------------------------|-----------|----------------|-------------|
| Hakemusasiakirjat   | Niiden töiden luonti, lukeminen, päivitys ja poisto, joiden työhönottoryhmässä käyttäjä on | Niiden töiden luonti, lukeminen, päivitys ja poisto, joiden työhönottoryhmässä käyttäjä on | Vain luku |
| Hakemuksen huomautukset       | Niiden töiden luonti, lukeminen, päivitys ja poisto, joiden työhönottoryhmässä käyttäjä on | Niiden töiden luonti, lukeminen, päivitys ja poisto, joiden työhönottoryhmässä käyttäjä on | Vain luku|
| Hakemus-tehtävä    | Tarkastelu, jos käyttäjä on työhönottoryhmässä | Tarkastelu, jos käyttäjä on työhönottoryhmässä | Vain luku |
| Hakemuksen palaute    | Palautteen lisääminen tai kaiken palautteen katsominen, jos käyttäjä on työhönottoryhmässä | Palautteen lisääminen tai kaiken palautteen katsominen, jos käyttäjä on työhönottoryhmässä | Palautteen lisääminen\*\* |
| Hylkää hakemus      | Hakemuksen hylkääminen, jos käyttäjä on työhönottoryhmässä | Ei sallittu | Ei sallittu |
| Siirrä seuraavaan vaiheeseen           | Hakemuksen hylkääminen, jos käyttäjä on työhönottoryhmässä | Hakemuksen siirtäminen, jos käyttäjä on työhönottoryhmässä | Ei sallittu |
| Käynnistä tarjousten hallinta | Tarjousten hallinnan käynnistäminen | Tarjoustehtävässä on määritysvaihtoehto | Ei sallittu |


\*\* [Palautetehtävän asetusten](./activities-attract.md) määritysvaihtoehto määrittää, näkevätkö haastattelijat toistensa antaman palautteen.


## <a name="process-templates"></a>Prosessimallit

Seuraavat käyttöoikeudet koskevat työhönoton prosessimalleja. Ryhmän jäsenten mahdollisuus luoda ja muokata malleja määritetään hallintakeskuksen **Mallien hallinta** -kohdassa. Jos mallien hallinta on otettu käyttöön, työhönottajat ja työhön ottavat esimiehet voivat luoda omia prosessimalleja ja muokata niitä. Jos mallien hallinta on poistettu käytöstä, vain järjestelmänvalvojat voivat luoda ja muokata prosessimalleja. Seuraavassa taulukossa oletetaan, että mallien hallinta on otettu käyttöön.

| Tiedot              | Työhönottaja                                           | Työhön ottava esimies                                      | Haastattelija |
|-------------------|-----------------------------------------------------|-----------------------------------------------------|-------------|
| Prosessimallit | Täydet käyttöoikeudet käyttäjän luomissa malleissa | Täydet käyttöoikeudet käyttäjän luomissa malleissa | Ei pääsyä   |

## <a name="email-and-email-templates"></a>Sähköposti ja sähköpostimallit

Seuraavat käyttöoikeudet koskevat sähköpostimalleja ja toimintoja, joita sähköposteissa voidaan käyttää. Vain järjestelmänvalvojat voivat luoda ja muokata sähköpostimalleja.

| Tiedot tai toiminto     | Työhönottaja          | Työhön ottava esimies     | Haastattelija |
|--------------------|--------------------|--------------------|-------------|
| Sähköpostimallit    | Vain luku -käyttöoikeus   | Vain luku -käyttöoikeus   | Ei pääsyä   |
| Lähetä sähköposti         | Tehtäväkohtainen lähetys  | Tehtäväkohtainen lähetys  | Ei pääsyä   |
| Muokkaa sähköpostin sisältöä | Sähköpostin sisällön muokkaus | Sähköpostin sisällön muokkaus | Ei pääsyä   |

## <a name="talent-pools"></a>Kykypoolit

Seuraavat käyttöoikeudet kykypooleja. Vain kykypoolin luonut käyttäjä näkee sen, ellei henkilö valitse poolin jakamista. Ehdokashaulla voidaan hakea hakijoita, joita ei ole lisätty nimettyyn pooliin.

| Tiedot tai toiminto   | Työhönottaja                                       | Työhön ottava esimies                                  | Haastattelija |
|------------------|-------------------------------------------------|-------------------------------------------------|-------------|
| Nimetty pooli       | Käyttäjän luomien poolien täydet käyttöoikeudet | Käyttäjän luomien poolien täydet käyttöoikeudet | Ei pääsyä   |
| Jaa pooli       | Vain käyttäjän luomat poolit                | Vain käyttäjän luomat poolit                | Ei pääsyä   |
| Ehdokashaku | Täydet hakutoiminnot                        | Täydet hakutoiminnot                        | Ei pääsyä   |

## <a name="candidates"></a>Ehdokkaat

Ehdokkaat ovat kykypooliin lisättyjä henkilöitä, joita ei ole liitetty työhön.

| Tiedot                        | Työhönottaja                        | Työhön ottava esimies                   | Haastattelija |
|-----------------------------|----------------------------------|----------------------------------|-------------|
| Profiili – ehdokkaan tiedot | Luonti, luku, päivitys ja poisto | Luonti, luku, päivitys ja poisto | Ei pääsyä   |
| Tiedostot                   | Luonti, luku, päivitys ja poisto | Luonti, luku, päivitys ja poisto | Ei pääsyä   |
