---
title: Kirjattujen vuokratapahtumien palauttaminen
description: Tässä ohjeaiheessa kerrotaan, miten kirjattu vuokratapahtuma palautetaan. Kaikki resurssien vuokrauksen kautta luodut tapahtumat voidaan palauttaa.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3e4908ddab2650e5ff7e4a28bf916604d165d08c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969525"
---
# <a name="reverse-posted-lease-transactions"></a>Kirjattujen vuokratapahtumien palauttaminen

[!include [banner](../includes/banner.md)]

Kaikki resurssien vuokrauksen kautta luodut tapahtumat voidaan palauttaa. Resurssin vuokrauksen kautta palautetut tapahtumat päivittävät vuokratietoja. Näin ollen ne myös päivittävät vuokrasopimusvelan kirjanpitoarvot ja käyttöoikeusomaisuuserän.

Voit luoda vuokraukselle palautustapahtuman seuraavasti.

1. Valitse **Vuokratapahtumat**- tai **Velkatapahtumat**-sivulla tapahtuma ja valitse sitten **Palauta tapahtuma**.
2. Näyttöön tulevassa valintaikkunassa voit muokata päivämäärää, jolloin palautuskirjaus kirjataan. Oletusarvoisesti **Päivämäärä**-kenttään määritetään valitun tapahtuman kirjauspäivämäärä. Palautusvientiä ei voi kirjata valitun tapahtuman alkuperäinen kirjauspäivämäärää aiemmin.
3. Valitse **OK**. Kirjataan kirjauskansiovienti, joka palauttaa valitun viennin. Palautus näkyy **Resurssitapahtumat**- tai **Velkatapahtumat**-sivulla. Sivulla näkyvä nykyisen saldon netto yhteensä päivitetään.

Kun valitset **Käänteinen jäljitys**, näkyviin tulee valintaikkuna, jossa näkyvät sekä alkuperäiset tapahtumat että palautetut tapahtumat ja linkitetty numero, joka näkyy *jäljitysnumerona*. Jos haluat helpottaa palautusten ymmärtämistä ja parantaa näkyvyyttä, voit jäljittää myös palautuksia käyttämällä vuokra-aikatauluja.

**Viimeisin kirjauskansion numero** -kentässä **Aikataulu**-sivulla on tapahtumien kirjauskansioiden numerot. Kun tapahtuma palautetaan, tähän kenttään päivittyy palautustapahtuman kirjauskansionumero. Lisäksi valitaan **Palautettu**-valintaruutu. Se osoittaa, että tapahtuma on palautettu. **Kirjattu**-kenttä valitaan.

## <a name="revoke-a-reversed-transaction"></a>Palautetun tapahtuman peruuttaminen

Voit peruuttaa palautetun tapahtuman seuraavasti.

1. Valitse **Aikataulu**-sivulla tai **Tapahtumat**-sivulla alkuperäinen tapahtuma.
2. Noudata seuraavia ohjeita:

    - Jos olet valinnut tapahtuman **Aikataulu**-sivulla, tee seuraavat vaiheet ja luo kirjauskansio kohdassa [Kuukausittaisten kirjauskansiovientien luominen eränä](create-monthly-journals-batch.md). Kirjauskansio on kirjattava manuaalisesti.
    - Jos valitsit tapahtuman **Tapahtumat**-sivulla, valitse **Palauta tapahtuma**. Näyttöön tulee sanoma, jossa kerrotaan tämän peruutuksen olevan aiemman palautuksen peruutus, ja että voit muokata tämän peruutuksen kirjauspäivämäärää. Yleiset yrityksen tarkistukset, jotka vaikuttavat päivämääriin, voidaan kuitenkin syöttää **Päivämäärä**-kenttään. 

3. Valitse **OK**. Kirjataan kirjauskansiovienti, joka palauttaa valitun viennin. Palautus näkyy **Tapahtumat**-sivulla. Nykyisen saldon netto yhteensä palautetaan ensimmäistä palautusta edeltäväksi arvoksi. Näin peruutuksen vaikutus saldoihin vältetään.

Kun valitset **Käänteinen jäljitys**, näyttöön tulee valintaruutu, jossa näkyvät sekä alkuperäiset tapahtumat että palautetut tapahtumat linkitetyn jäljitysnumeron kanssa.

Voit myös jäljittää peruutuksia käyttämällä soveltuvaa **Aikataulut**-sivua. **Käänteinen**-kenttä tyhjennetään, kun taas **Kirjauskansio kirjattu** -kenttä valitaan. Lisäksi **Viimeisin kirjauskansionumero** -kenttään päivitetään peruutustapahtuman kirjauskansionumero ja **Kirjauskansionumero**-kenttään päivitetään palautuskirjauskansionumero.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]