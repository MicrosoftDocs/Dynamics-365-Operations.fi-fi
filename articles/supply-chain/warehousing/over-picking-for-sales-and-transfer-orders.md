---
title: Myyntitilausten ja siirtotilausten ylikeräily
description: Tässä ohjeaiheessa kerrotaan, miten ylikeräily otetaan käyttöön myynti- ja siirtotilauksille.
author: GalynaFedorova
ms.date: 07/06/2021
ms.topic: article
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-07-06
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 52a4225efa88a7b9303dd611d5652f59da1612a4
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678405"
---
# <a name="over-picking-for-sales-orders-and-transfer-orders"></a>Myyntitilausten ja siirtotilausten ylikeräily

[!include [banner](../includes/banner.md)]

Tämä aihe esittelee skenaarion, joka osoittaa, miten joko tietty työntekijä tai kaikki työntekijät voivat valita ylikeräilyn. Ylikeräilyprosessi mahdollistaa valvotun ylikeräilyn keräilyn aikana.

Varaston ylikeräily on yksinkertainen käsite. Järjestelmän avulla työntekijät voivat poimia tilaukseen määritettyä enemmän nimikkeitä. Se kuitenkin ottaa huomioon ylitoimitusrajan, joka on määritetty siirtotilauksen tai myyntitilauksen rivitasolla. Jos raja ylittyy, Warehouse Management -sovellus ilmoittaa työntekijöille, että he ylittävät ylitoimitusrajan.

Ylitoiminto auttaa pienentämään ylläpitoa ja auttaa myös asetusten joustavassa määrityksessä. Voit määrittää yhden tai useita mobiililaitteen valikkokohteita ja ottaa käyttöön yli keräilyn vain osalle niistä. Voit myös estää valittuja työntekijöitä keräämästä myyntitilauksia ja/tai siirtotilauksia liian helposti ilman, että valikkokohteita tarvitsee muuttaa. Sen sijaan voit poistaa yhden tai molemmat näistä ominaisuuksista käytöstä asiaankuuluvissa työntekijäasetuksissa.

Ylipoimintatoiminto auttaa työntekijöitä säästämään aikaa ja työtä nimikkeiden keräämisessä ja lähetyksessä. Ominaisuuden avulla työntekijät voivat esimerkiksi suorittaa seuraavia tehtäviä:

- Kutistuminen keräilyn tai lähetyksen aikana.
- Vältä pakkausmateriaalin purkamista keräilyprosessin aikana.
- Nimikevahinkojen korvaaminen kuljetuksen aikana.
- Lähetä määrä tai mittayksikön varianssi.
- Minimoi rekisterikilvissä olevien määrien rikkoutuminen.
- Vältä materiaalihävikkiä ja kalliiden materiaalien vähyyttä.
- Mittaa kerätty määrä keräilyn jälkeen (esimerkiksi kuorma-autojen punnitsemisen avulla).

> [!IMPORTANT]
> Ylipoimintatoiminto koskee vain myyntitilausta ja siirtotilauksen keräilyä ja käsittelyä. Täydennys ei tue ylikeräilyä. Kun täydennystyö suoritetaan, käyttäjät eivät voi suorittaa ylipoimintaa.

Tässä aiheessa näytetään esimerkkitilanne tämän toiminnon määrittämisestä ja ylipoimintaominaisuuden käytöstä.

## <a name="scenario-prerequisite-make-demo-data-available"></a>Skenaarion edellytykset: Esittelytietojen käyttö

Ohjeaiheen skenaariossa viitataan arvoihin ja tietueisiin, jotka sisältyvät Microsoft Dynamics 365 Supply Chain Managementin vakiodemotietoihin. Jos haluat käyttää harjoituksissa näitä annettuja arvoja, varmista, että demotiedot on asennettu työskentely-ympäristöön ja että yritykseksi on valittu *USMF* ennen aloittamista.

## <a name="scenario-setup"></a>Skenaarion määrittäminen

Ennen kuin käyt läpi esimerkkiskenaarion, sinun on otettava käyttöön ylikeräily sekä työntekijälle että asianmukainen valikkokohde.

### <a name="set-up-a-worker-to-allow-for-over-picking"></a>Ylikeräilyn salliminen työntekijälle

Seuraavassa on yleinen menettely, jonka mukaan työntekijä määritetään sallimaan myyntitilausten ja siirtotilausten ylikeräily erikseen. Tämä konfigurointi määrittää, kuka keräystyöntekijä voi tehdä ylikeräilyn ja voiko työntekijä tehdä ylikeräilyn sekä siirtotilauksille että myyntitilauksille.

1. Valitse **Varastonhallinta \> Asetukset \> Työntekijä**.
1. Valitse luetteloruudusta **Julia Funderburk**
1. Valitse **Käyttäjät**-pikavälilehdestä rivi, jolla on seuraavat arvot. Jos näillä arvoilla ei ole olemassa olevaa riviä, luo se.

    - **Käyttäjätunnus:** *24*
    - **Käyttäjänimi:** *WH 24*
    - **Oletusvarasto:** *24*
    - **Valikon nimi:** *Pää*

1. Määritä **Työ**-pikavälilehdessä käyttäjälle *24* seuraavat arvot, jos niitä ei ole vielä määritetty:

    - **Salli myynnin ylikeräily:** *Kyllä*
    - **Salli siirtotilaus ylikeräilyn aikana:** *Kyllä*

### <a name="set-up-a-mobile-device-menu-item-to-allow-for-over-picking"></a>Määritä mobiililaitteen valikkonimike, jotta voit sallia ylikeräilyn

Tässä on yleinen menetelmä, jonka avulla määritetään kannettavan laitteen valikkokohde, jotta ylikeräily otetaan käyttöön. Jotkin parametrit voidaan ottaa käyttöön tai poistaa käytöstä sen mukaan, mitä liiketoimintavaatimukset koskevat matkapuhelinvalikon käyttöönottamisen käyttöoikeustasoa.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.
1. Valitse luetteloruudusta tietue, jonka nimi on *Myynnin keräily*. Jos tällä nimellä ei ole aiemmin luotua tietuetta, luo se. Vahvista tai määritä tietueelle seuraavat arvot:

    - **Valikkokohteen nimi:** *Myynnin keräily*
    - **Nimike:** *Myynnin keräily*
    - **Tila:** *Työ*
    - **Käytä aiemmin luotua työtä:** *Kyllä*
    - **Ohjaus:** *Käyttäjän ohjaama*
    - **Ohita kohderekisterikilpi:** *Kyllä*
    - **Ohita rekisterikilpi asetuksen aikana:** *Kyllä*
    - **Pidä työ käyttäjän lukitsemana:** *Kyllä*
    - **Salli ylikeräily:** *Kyllä*

> [!IMPORTANT]
> Kun sekä työntekijän että kannettavan laitteen valikkokohteen parametrit on otettu käyttöön, ylikeräily voidaan käsitellä vain mobiililaitteen kautta.

## <a name="example-scenario"></a>Esimerkkiskenaario

Kun edellytykset, työntekijän asetukset ja valikkokohteen asetukset ovat valmiina, voit käyttää toimintoa.

### <a name="create-a-sales-order-that-allows-for-overdelivery"></a>Ylitoimitusta tukevan myyntitilauksen luominen

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Luo uusi myyntitilaus valitsemalla **Uusi**.
1. Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:

    - **Asiakastili:** *US-001*
    - **Varasto**: *24*

1. Valitse **OK**.
1. Uusi myyntitilaus avataan. Lisää **Myyntitilausrivit**-pikavälilehdessä rivi, jossa on seuraavat asetukset:

    - **Nimiketunnus:** *A0001*
    - **Määrä** *10*

1. Määritä **Rivitiedot** -pikavälilehden **Toimitus**-välilehdessä **Ylitoimitus**-kentän arvoksi *10*.
1. Valitse **Myyntitilausrivit**-pikavälilehdessä **Varasto \> Varaus**.
1. Varaa varasto **Varaus**-sivun toimintoruudussa valitsemalla **Varaa erä**.
1. Sulje **Varaus**-sivu.
1. Valitse toimintoruudussa **Varasto**-välilehdellä **Vapauta varastoon**.

Kun vapautus on tehty, näkyviin tulee tietosanomia, jotka sisältävät luodun aallon ja luodut kuormatunnukset.

### <a name="get-the-work-id-and-license-plate-number-for-the-new-order"></a>Hae uuden tilauksen työtunnus ja rekisterinumero

Kun olet vapautenut myyntitilauksen varastoon, järjestelmän olisi luotava uusi työtunnus, jolla on yksi valintarivi. Etsi työtunnus ja rekisterikilven toimeksianto alla olevien ohjeiden avulla.

1. Valitse **Varastonhallinta \> Työ \> Työn tiedot**.
1. Hae **Yleiskatsaus**-ruudukosta juuri luodun myyntitilauksen **Tilausnumero**-sarake. Merkitse muistiin tämän myyntitilauksen vastaava työtunnus.
1. Valitse uuden myyntitilauksen rivi, jos haluat nähdä **Rivit**-ruudukon liittyvät tiedot. Merkitse muistiin nimikkeen keräyssijainti.
1. Siirry kohtaan **Varastonhallinta \> Kyselyt ja raportit \> Käytettävissä olevien luettelo**.
1. Valitse toimintoruudussa **Dimensiot**.
1. Varmista, **Dimensionäyttö**-valintaruudussa, että **Rekisterikilpi**-, **Varasto**- ja **Nimikenumero**-valintaruudut on valittu. Valitse sitten **OK**.
1. Määritä **Suodatin**-ruudussa seuraavat suodattimet:

    - **Nimiketunnus** – **on yksi seuraavista** – *A0001*
    - **Varasto** – **alkaa numerolla** - *24*

1. Valitse **Käytä**.
1. Kirjoita muistiin näkyvissä olevat **rekisterikilven** arvot.

### <a name="over-pick-the-order-by-using-the-warehouse-management-mobile-app"></a>Tilauksen ylikerääminen Warehouse Management -mobiilisovelluksen avulla

1. Kirjaudu varastonhallinnan mobiilisovellukseen käyttäjänä varastossa *24*.
1. Siirry kohtaan **Lähtevät \> Myynnin keräily**.
1. Kirjoita myyntitilausta varten luotu työtunnus **Skannauksen työtunnus- tai rekisterikilpi** -kenttään.
1. Valitse **OK** (valintamerkkisymboli).
1. Valitse **Ylipoiminta**.
1. Aseta **Keräysmäärä**-kentän arvoksi *14*.
1. Valitse **OK** (valintamerkkisymboli).

    **Ylikeräys**-sivulla näytetään seuraava sanoma: "Rivin ylitoimitus on 40,00 prosenttia, mutta sallittu ylitoimitus on vain 10,00 prosenttia." Tämä sanoma ilmaisee, että syötit ylitoimitusrajan ylittävän keräysmäärän. Myyntitilausrivin ylitoimitusraja on 10 prosenttia. Näin ollen määritetylle määrälle 10 voidaan tehdä ylikeräyksiä vain yksi, kun kokonaismäärä on 11.

1. Aseta **Keräysmäärä**-kentän arvoksi *11*.
1. Valitse **OK** (valintamerkkisymboli).
1. Kirjoita **Rekisterikilpi**-kenttään sen käyttöoikeus, jota olet huomauttanut edellisessä osassa.
1. Syötä **Kohderekisterikilpi**-kenttään kohderekisterikilpi. Huomaa, että keräilysijainti (*FLOOR-001*), nimike (*A0001*) ja määrä (*11 kpl*) ovat näkyvissä.
1. Valitse **OK** (valintamerkkisymboli).
1. Tarkista **Myyntitilaukset – poispano** -sivulla olevat tiedot. **Sijainti**-kentän pitäisi ilmaista, että kerätyt nimikkeet ovat menossa *BAYDOOR*-sijaintiin.
1. Valitse **OK** (valintamerkkisymboli).

**Skannaa työn tunnus tai rekisterikilven tunnus** -sivulla on Työ valmis -sanoma. Tämä sanoma ilmaisee, että myyntitilauksen työtunnus on valmis eikä ylitoimitusmäärä ylitä 10 prosentin ylitoimitusrajaa.
