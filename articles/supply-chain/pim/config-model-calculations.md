---
title: Tuotekonfiguraatiomallin laskelmat
description: Tässä aiheessa kuvataan, miten tuotekonfiguraatiomallissa määritteiden laskelmat
author: t-benebo
ms.date: 03/18/2021
ms.topic: article
ms.search.form: PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-18
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 349fed3ca75b94db2f421a1ff3c3553c96c202c37d59857a3d973f3de8f995ad
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755248"
---
# <a name="product-configuration-model-calculations"></a>Tuotekonfiguraatiomallin laskelmat

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, miten tuotekonfiguraatiomallissa määritteiden laskelmat.

## <a name="prerequisites"></a>Edellytykset

Laskentaa käytetään tuotteen kokoonpanomallissa laskettaessa tuotteelle kokoonpanoarvoja. Ennen kuin laskelmien määritys aloitetaan, liittyvä tuotekonfiguraatiomalli on oltava olemassa. Yhteenveto konfigurointimallien määritysprosessista ja niihin liittyvistä tehtävistä on kohdassa [Tuotekonfiguraatiomallin määrittäminen](set-up-maintain-product-configuration-model.md).

## <a name="create-a-calculation"></a>Luo laskenta

Laskenta koostuu kaavasta ja kohdemääritteestä. Lisätietoja: [Tuotekonfiguraatiomallin laskelmat – usein kysytyt kysymykset](calculate-product-configuration-models.md).

Voit luoda laskelman aiemmin luotua tuotemallia varten noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Tuotetietojen hallinta \> Yleinen \> Tuotekonfiguraation mallit**.
1. Avaa tuotekonfiguraation malli ja valitse sitten **Muokkaa**.
1. Lisää laskelma valitsemalla **Laskelmat** -pikavälilehdessä **Lisää** ja määritä sitten seuraavat kentät:

    - **Nimi** – Anna laskelman nimi.
    - **Kuvaus** – anna laskelman kuvaus.
    - **Kohdemäärite** – Valitse määrite, jota varten laskenta tehdään.

1. Valitse **Muokkaa lauseketta**.
1. Lisää lausekkeeseen pakolliset määritteet, operaattorit ja arvot **Syötä laskenta** -valintaikkunassa. Lisätietoja näiden elementtien käsittelystä on kohdassa [Tuotteen määritysmallien lausekerajoitukset ja taulukkorajoitukset](expression-constraints-table-constraints-product-configuration-models.md).
1. Kun lauseke on valmis, valitse **OK**.

## <a name="calculation-examples"></a>Esimerkkejä laskutoimituksista

Tässä osassa on muutamia esimerkkejä, jotka osoittavat, kuinka laskelmat toimivat.

### <a name="example-1"></a>Esimerkki 1

Kohdemääritteen tyyppi on Boolean ja laskenta käyttää seuraavaa ehtolauseketta:

`If[(decimalAttribute1 / decimalAttribute2) < 1, True, False]`

Tämä lauseke palauttaa kohdemääritteeseen *Tosi*, jos `decimalAttribute2` on suurempi tai yhtä suuri kuin `decimalAttribute1`. Muussa tapauksessa se palauttaa totuusarvon *Epätosi*.

### <a name="example-2"></a>Esimerkki 2

Tässä esimerkissä kohdemääritteenä käytetään tekstimääritettä `textFixedList`. Tämä määrite sisältää seuraavan kiinteän luettelon.

| Arvo | Selvityksen arvo |
|---|---|
| A | 1a |
| D | 2b |
| K | 2c |

Seuraavassa näyttökuvassa näkyy, miltä tämän määritteen asetukset voivat näyttää järjestelmässäsi.

![Määritteen tyypin asetukset esimerkissä 2.](media/model-calculations-example2.png "Määritteen tyypin asetukset esimerkissä 2")

Määritettä käytetään seuraavassa ehtolausekkeessa:

`If[integerAttribute < 150, 0, 2]`

Jos `integerAttribute` on pienempi kuin 150, tämä lauseke palauttaa kiinteän luettelon ensimmäisen tietueen tekstin arvon *A*. Muussa tapauksessa se palauttaa kiinteän luettelon kolmannen tietueen tekstiarvon *C*.

> [!NOTE]
> Kiinteä luettelo vastaa nollaan perustuvaa valintalista (enum), ja sen arvoja voidaan käyttää sopivalla kokonaislukuarvolla. Siksi ensimmäisen kiinteän luettelon arvo (*A*) vastaa arvoa numeroa *0*, toinen arvo (*B*) vastaa numeroa *1* ja kolmas arvo (*C*) vastaa numeroa *2*.

### <a name="example-3"></a>Esimerkki 3

Tässä esimerkissä `textFixedList`-kohdemääritettä edellisestä esimerkistä. Se käyttää myös toista `textAttribute`-tekstimääritettä, joka sisältää seuraavan kiinteän luettelon.

| Arvo | Selvityksen arvo |
|---|---|
| AA | 1aa |
| BB | 2bb |

Seuraavassa näyttökuvassa näkyy, miltä tämän määritteen asetukset voivat näyttää järjestelmässäsi.

![Määritteen tyypin asetukset esimerkissä 3.](media/model-calculations-example3.png "Määritteen tyypin asetukset esimerkissä 3")

Määritteen `textFixedList` arvo lasketaan seuraavan ehtolausekkeen avulla:

`If[textAttribute == "1aa", 0, 2]`

Jos `textAttribute`-palautusarvo on yhtä kuin *1aa*, tämä lauseke palauttaa kiinteän `textFixedList`-luettelon ensimmäisen tietueen tekstin arvon *A*. Muussa tapauksessa se palauttaa kiinteän `textFixedList`-luettelon kolmannen tietueen tekstiarvon *C*.

> [!NOTE]
> - Ehdollisen laskelman on käytettävä määritteen palautusarvoa.
> - Laskelmissa voidaan käyttää vain kiinteän luettelon tekstimääritteitä.

## <a name="see-also"></a>Lisätietoja

- [Tuotemääritysmallien laskelmat – usein kysytyt kysymykset](calculate-product-configuration-models.md)
- [Lisää rajoituslauseke tuotemääritysmalliin](tasks/add-expression-constraint-product-configuration-model.md)
- [Tuotekonfiguraatiomallien yleiskatsaus](product-configuration-models.md)
