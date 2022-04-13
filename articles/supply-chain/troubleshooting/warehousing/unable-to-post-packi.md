---
title: Pysäytetyn myyntitilausrivin pakkausluetteloa ei voi kirjata
description: Et voi kirjata pysäytetyn myyntitilausrivin pakkausluetteloa
author: smithanataraj
ms.date: 03/07/2022
ms.topic: article
ms.search.form: WHSLoadTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2022-03-07
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 115cfe79e075eb36f73203818acdbb5e31fc0bad
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462849"
---
# <a name="cant-post-packing-slip-for-a-stopped-a-sales-order-line"></a>Pysäytetyn myyntitilausrivin pakkausluetteloa ei voi kirjata

Virhekoodi: SYS13203

## <a name="symptoms"></a>Oireet

Kun yrität kirjata kuorman lähetysluetteloa, järjestelmä näyttää seuraavan virhesanoman:

> Pakkausluetteloa ei voida kirjata, kun myyntitilausrivi pysäytetään lähtevän lähetyksen vahvistamisen jälkeen. Määrää ei voida poimia.

## <a name="cause"></a>Syy

Voit pysäyttää yhden tai useamman liittyvän myyntitilausrivin, mikä tarkoittaa, että järjestelmä estää myyntitilauksen jatkokäsittelyn. Tämä merkitsee muun muassa, että järjestelmä ei kirjaa tilaukselle pakkausluetteloa.

Käyttäjä on esimerkiksi päättänyt pysäyttää yhden tai useampia tilausrivejä, koska asiakas on ottanut yhteyttä ja peruuttanut tilauksensa. Jos lähtevä lähetys on kuitenkin jo vahvistettu, myyntitilauksen sisältävä lähetys olisi jo fyysisesti poistunut varastosta, mikä tarkoittaa, että myyntitilausrivien pysäyttämisellä ei ole vaikutusta. Koska lähetyksen fyysinen pysäyttäminen ei ole enää mahdollista, voit yhtä hyvin avata rivit pakkausluettelon kirjaamista varten. Tämän jälkeen sinun on käsiteltävä peruutettua tilausta palautuksena.

## <a name="resolution"></a>Ratkaisu

Voit kirjata pakkausluettelon varmistamalla, että kaikkia asiaankuuluvia myyntitilausrivejä ei ole pysäytetty, tekemällä seuraavat vaiheet.

1. Valitse **Kaikki myyntitilaukset \> Myynti ja markkinointi \> Kaikki myyntitilaukset**.
1. Voit etsiä ja avata myyntitilauksen, jonka kanssa sinulla on ongelmia.
1. Valitse **Myyntitilausrivit**-pikavälilehdessä myyntitilausrivi.
1. Avaa **Rivin tiedot** -pikavälilehdessä **Yleiset**-välilehti ja varmista, että **Pysäytetty**-kentän arvoksi on määritetty *Ei*.
1. Jatka työskentelyä, kunnes kaikki asiaankuuluvat myyntirivit eivät enää ole pysäytettyjä.
1. Yritä uudelleen kirjata kuorman tai myyntitilauksen pakkausluettelo.
