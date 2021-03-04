---
title: Varastotyönkulkujen numerosarjojen määrittäminen
description: Tässä ohjeaiheessa käsitellään yleisesti toimintoja, joilla luodaan rekisterikilpien tunnusten, aallon etiketin tunnusten, kontin tunnusten ja rahtikirjojen tunnusten numerosarjalaajennukset.
author: GarmMSFT
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSNumberSequenceExt
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: e6faab834b4c1c514bcc23a59d74e2bd0e069754
ms.sourcegitcommit: a26e4963d40796da21ce6581cfb2f4d9db4f6776
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/27/2020
ms.locfileid: "4427515"
---
# <a name="configure-number-sequences-for-warehouse-flows"></a>Varastotyönkulkujen numerosarjojen määrittäminen

[!include [banner](../includes/banner.md)]

*Numerosarjalaajennukset*-toiminto lisää uuden määrityssivujen numerosarjojen määrittämistä varten. Sen avulla voi luoda joustavasti GS1-säädeltyjä tunnuksia, kuten GS1-etuliitteitä ja -tarkistusnumeroita (modulo 10), minkä lisäksi se valvoo aiemmin luotujen numerosarjojen pituusrajoitusten noudattamista.

Vakionumerosarjasegmentit eivät sovellu GS1-toteutukseen, koska mitään tarkistusnumeroa ei lasketa ja yrityksen GS1-etuliite on päivitettävä manuaalisesti.

Tämä toiminto lisää seuraavat toiminnot:

- Rahtikirjan tunnukset voidaan luoda etukäteen.
- Yksilöivä numerosarja voidaan luoda SSCC (sarjatoimitusyksikkökoodi) -numeroille.
- GS1-yhteensopivat numerosarjat voidaan luoda rahtikirja- ja SSCC-numeroille. Tämä toiminto lisää heti käytössä olevan rekisterikilpien tunnusten, konttien tunnusten, aallon etikettien tunnusten ja rahtikirjan tunnusten tuen.
- Rekisterikilven tunnusnumerot voi määrittää joustavasti. Voit esimerkiksi sisällyttää tai jättää pois sovelluksen tunnisteet (AI), kuten edessä olevat nollat (00).

Toiminto tehostaa laatikoiden etikettitukea ja uusien järjestelmän luomien numeroiden oikaisua.

## <a name="turn-on-the-number-sequence-extensions-feature"></a>Numerosarjalaajennukset-toiminnon ottaminen käyttöön

Ennen kuin käytät toimintoa, se on otettava käyttöön järjestelmässä. Järjestelmänvalvojat voivat käyttää [Toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) työtilaa tarkistaakseen toiminnon tilan sekä laittaa sen päälle, jos sitä vaaditaan. Tässä tapauksessa toiminto näkyy seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Toiminnon nimi:** *Numerosarjalaajennukset*

## <a name="set-up-the-feature"></a>Toiminnon määrittäminen

Numerosarjalaajennukset määritetään järjestelmään seuraavasti:

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Varastonhallinnan parametrit**.
1. Anna yrityksen GS1-etuliite **Yleiset**-välilehden **Yrityksen GS1-etuliite** -kenttään. Tämä arvo koskee kaikkia numerosarjoja, joihin GS1-etuliite sisältyy segmenttinä.
1. Jos haluat luoda aallon etikettien rahtikirjanumeroita valitse **Raportit**-välilehdessä **Luo rahtikirjanumero, kun aallon etikettejä tulostetaan** -valintaruutu.

    > [!NOTE]
    > Tämä valintaruutu on valittavissa vain, jos [aallon etikettitulostuksen](configure-wave-label-printing.md) toiminnot on otettu käyttöön.

1. Valitse **Varastonhallinta** \> **Asetukset** \> **Numerosarjalaajennukset**
1. Valitse toimintoruudussa **Luo oletusasetukset**. GS1-yhteensopiva rahtikirjan numerosarja ja kolme SSCC-numerosarjatyyppiä luodaan. Kaikki nämä numerosarjat ottavat yrityksen GS1-etuliitteen pituuden huomioon.

    Lisätietoja oletusnumerosarjojen mukauttamisesta ja/tai uusien sarjojen lisäämisestä on seuraavassa osassa. Voit myös poistaa minkä tahansa näistä sarjoista, jos et tarvitse niitä.

1. Valitse uudelleen **Varastonhallinta \> Asetukset \> Varastonhallinnan parametrit**.
1. Valitse **Numerosarjat**-välilehdessä numerosarjalaajennus, jolla luodaan rekisterikilpitunnusten, aallon etikettitunnusten, konttitunnusten (siinä tapauksessa valitaan sopiva **SSCC-18-numerosarja**) ja/tai rahtikirjatunnukset (siinä tapauksessa valitaan **Rahtikirja**-sarja). Numerosarjalaajennuksia tuetaan oletusarvoisesti vain näissä neljässä tunnustyypissä.

Kun uusi numero luodaan seuraavan kerran jollekin näistä numerosarjoista, uusi logiikka on käytössä.

> [!NOTE]
> Jos et valitse rekisterikilpitunnusten numerosarjalaajennusta, nykyisiä rekisterikilpitunnusten luontisääntöjä käytetään. Muussa tapauksessa käytetään valittua numerosarjaa. Muut tunnukset käyttävät yksinkertaista numerosarjaa siihen saakka, että niissä käytetään numerosarjalaajennusta.

## <a name="create-and-edit-number-sequences"></a>Numerosarjojen luominen ja muokkaaminen

Edellisessä osassa luotiin numerosarjojen oletusjoukko. Tässä osassa käsitellään kunkin numerosarjan määrittämistä. Lisäksi käsitellään mukautettujen sarjojen luontia sekä oletusarvoisten tai mukautettujen sarjojen muokkaamista.

Numerosaroja voi luoda ja muokata seuraavasti:

1. Valitse **Varastonhallinta** \> **Asetukset** \> **Numerosarjalaajennukset**.
1. Valitse toimintoruudussa **Uusi**.
1. Anna uuden sarjan nimi **Numerosarjalaajennus**-kenttään. Syötä **Kuvaus**-kenttään kuvaus.
1. Kokoa numerointimuoto lisäämällä, poistamalla ja järjestelmällä segmenttejä **Segmentit**-pikavälilehden painikkeilla. Määritä kun rivin **Segmentti**-kenttään segmenttityyppi, joka määrittää kyseisen segmentin tarkoituksen ja sisällön. Seuraavassa taulukossa käytettävissä olevien segmenttityyppien kuvaukset.

    | Segmenttityyppi | kuvaus |
    |---|---|
    | Vakio | Tämä segmenttityyppi lisää saman vakiotekstin jokaiseen sarjaan luotuun numeroon. Kirjoita **Arvo**-kenttään tarvittava teksti. **Pituus**-kenttä päivitetään automaattisesti **Arvo**-kenttään annetun tekstin pituiseksi. |
    | Numerojärjestys | Anna **Arvo**-kenttään numeromerkki (*\#*) jokaiselle merkille, jonka pitäisi näkyä luodussa sarjassa. Itse numerosarja voi muodostaa pidempiä numeroita, mutta vain oikeanpuolimmaisimmat merkit näytetään. **Pituus**-kenttä päivitetään automaattisesti **Arvo**-kenttään annettujen numeromerkkien määrän mukaiseksi.<p>SSCC-18-lukujen GS1-vaatimukset edellyttävät, että tämän segmentin pituus on 16, josta on vähennetty GS1-etuliitteen pituus. Varmista, että näin on.</p> |
    | GS1-etuliite | Tämä segmenttityyppi lisää arvon, joka on määritetty **Varastonhallinnan parametrit** -sivun **Yrityksen GS1-etuliite** -kentässä. **Arvo**-kenttä näyttää arvon, joka on määritetty **Varastonhallinnan parametrit** -sivulla ja **Pituus**-kenttä näyttää merkkien määrän arvossa. Sekä **Arvo**- että **Pituus**-kenttä ovat vain luku -muotoisia. |
    | Sovellustunnus | Anna **Arvo**-kenttään sovelluksen tunniste niin kuin se on määritetty tämän tyyppisen numerosarjan GS1-käytännössä. Anna esimerkiksi *00* SSCC-kohdassa tai *420* rahtikirjan osalta. **Pituus**-kenttä päivitetään automaattisesti **Arvo**-kenttään annetun tunnisteen pituiseksi. |
    | Pakkaustyyppi | Jos nimike voidaan määrittää selkeästi, tämä segmenttityyppi lisää kentän arvon soveltuvasta yksikön sarjaryhmästä (**Yksikön sarjaryhmät** -sivulta). (Tämä toiminta vastaa rekisterikilpitunnusten nykyistä logiikkaa.) Jos rekisterikilvet sisältävät useita varastointiyksiköitä, tämä segmenttityyppi lisää oletusarvoisesti arvon *0* (nolla). Tässä segmenttityypissä **Arvo**-kentän asetuksena on aina *P* ja **Pituus**-kentän asetuksena on aina *1*.|
    | Tarkistusnumero | Tämä segmenttityyppi lisää tarkistusnumeron, joka on modulo 10 -lasku. (Tämä toiminta vastaa rekisterikilpitunnusten nykyistä logiikkaa.) Tässä segmenttityypissä **Arvo**-asetuksena on aina sirkumfleksi (*^*) ja **Pituus**-kentän asetuksena on aina *1*. |

1. Voit tarkastella lopullisen numeromuodon esimerkki, tarkasta **Muoto**-kenttä **Segmentit**-pikavälilehden alaosassa.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]