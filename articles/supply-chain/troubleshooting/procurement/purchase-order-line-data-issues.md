---
title: Ostotilausrivin tietoristiriidat
description: Ostotilausriveillä on tietojen ristiriitoja tai vioittuneita tietoja.
author: SmithaNataraj
ms.date: 12/07/2021
ms.topic: troubleshooting
ms.search.form: PurchLineManualCorrection, PurchTable, PurchLine, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-12-07
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: ee2cb9a07c8a00a92c71e3e99d8ec20aa27fb20e
ms.sourcegitcommit: b9799a58d6ec221df86788bc37c4fbd28b435e89
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/08/2022
ms.locfileid: "8100800"
---
# <a name="purchase-order-line-data-discrepancies"></a>Ostotilausrivin tietoristiriidat

## <a name="symptoms"></a>Oireet

Kun tarkistat ostotilauksen rivejä, huomaat yhden tai useampia seuraavista ongelmista:

- Ostotilausrivien jäljellä olevan summan (toimitus tai laskutus) tiedoissa on ristiriitoja tai ne ovat vioittuneet.
- Ostotilausrivi tai otsikon tila on vioittunut.
- Et voi laskuttaa ostotilausta esimerkiksi, koska näyttöön tulee vähintään yksi seuraavista virhesanomista:

    - "Pysäytettiin (virhe): Tapahtuma on jo kirjattu."
    - "Määrää ei voi laskuttaa, koska varastotapahtumat, joiden tila on Vastaanotettu, eivät riitä."
    - "Riittämätön määrä varastotapahtumia, joiden tila on Ostettu nimikkeen %0 määrälle %1."

- Et voi viimeistellä tai sulkea ostotilausta esimerkiksi jonkin seuraavan ongelman vuoksi:

    - **Viimeistele**-painike ei ole käytettävissä.
    - Et voi peruuttaa vahvistetussa ja vastaanotetussa tilassa olevan ostotilauksen ostotilausrivin tilattua määrää.

## <a name="cause"></a>Syy

Nämä ongelmat johtuvat yleensä tietojen vioittumiseen tai ristiriitaisuuteen yhden tai useamman ostotilausrivin jäljellä olevassa määrässä.

## <a name="resolution"></a>Ratkaisu

Nämä ongelmat voi yleensä korjata päivittämällä asianosaisten ostotilausrivien tila, toimituksen jäljellä oleva määrä ja/tai laskutuksen jäljellä oleva määrä seuraavassa menettelyssä kuvatulla tavalla.

1. Siirry kohtaan **Hankinta \> Kausittaiset tehtävät \> Puhdistus \> Korjaa ostotilausrivit manuaalisesti**.
1. Etsi ja valitse ongelmallinen ostotilaus **Ostotilaus**-kentässä.
1. Valitse **Ostotilausrivit**-osassa rivi, jolta olet löytänyt ristiriitaisuuden.
1. Tutki **Varastotapahtumat**-osassa näkyvät tiedot. Jos havaitset epäjohdonmukaisuuksia ostotilausrivin ja sen varastotapahtumien välillä, valitse jokin seuraavista toimintoruudun komennoista sen mukaan, missä näet epäjohdonmukaisuudet:

    - **Laske uudelleen \> Laske toimituksen jäljellä oleva määrä uudelleen** – Päivitä ostotilausrivin ja otsikon tilat automaattisesti. Tämä toiminto toimii vain varastoitujen ostotilausrivien (rivien, joiden nimikettä on varastossa) osalta. Varastoimattomia ja todellisen painikkeiden nimikkeitä ei tällä hetkellä tueta.
    - **Laske uudelleen \> Laske laskutuksen jäljellä oleva määrä uudelleen** – Päivitä ostotilausrivin ja otsikon tilat automaattisesti. Tämä toiminto toimii vain varastoitujen ostotilausrivien (rivien, joiden nimikettä on varastossa) osalta. Varastoimattomia ja todellisen painikkeiden nimikkeitä ei tällä hetkellä tueta.
    - **Laske uudelleen \>Laske tila uudelleen** – Laske valitun rivin tila uudelleen. Tämä laskelma perustuu aiemmin luotuun logiikkaan. Näin ollen ostotilauksen otsikon tila päivitetään tarvittaessa uuden ostotilausrivin tilan perusteella.

1. Jos jäljellä olevissa määrissä on edelleen epäjohdonmukaisuuksia, voit muokata niitä suoraan seuraavien kenttien avulla:

    - Jäljellä oleva määrä
    - Varastotoimitusmuistutus
    - Laskun jäännös
    - Varastolaskumuistutus
