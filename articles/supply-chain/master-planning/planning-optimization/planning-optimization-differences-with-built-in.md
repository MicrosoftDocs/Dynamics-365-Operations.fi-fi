---
title: Sisäisen pääsuunnittelun ja suunnittelun optimoinnin erot
description: Tässä aiheessa on luettelo ominaisuuksista, joita suunnittelun optimointi ei vielä tue ja joita ei mainita suunnittelun optimoinnin sopivuusanalyysisivulla.
author: crytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a102f1d77362f650c060ce5d0aee5b62d2102532
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344951"
---
# <a name="differences-between-built-in-master-planning-and-planning-optimization"></a>Sisäisen pääsuunnittelun ja suunnittelun optimoinnin erot

[!include [banner](../../includes/banner.md)]

Suunnittelun optimoinnin tulokset voivat olla erilaiset kuin sisäisen pääsuunnittelumoduulin tulokset. Erot voivat johtua odottavista ominaisuuksista. Tässä aiheessa on luettelo ominaisuuksista, joita suunnittelun optimointi ei vielä tue ja joita ei mainita **[Suunnittelun optimoinnin sopivuusanalyysi](planning-optimization-fit-analysis.md)** -sivulla.

| Ominaisuus | Nykyinen suunnittelun optimoinnin toiminta |
|---|---|
| Todellisen painon tuotteet | Todellisen painon tuotteita pidetään tavallisina tuotteina.|
| Laajennettavat dimensiot | Laajennettavat dimensiot ovat tyhjiä suunnitelluissa tilauksissa, vaikka **Kattavuussuunnitelma dimension mukaan** -valintaruutu olisi valittu **Varastodimensioryhmät** tai **Seurantadimensioryhmät**-sivulla. |
| Suodatetut tuotantoajot | Lisätietoja on kohdassa [Tuotannon suunnittelu – suodattimet](production-planning.md#filters). |
| Ennusteen suunnittelu | Ennusteen suunnittelua ei tueta. Pääsuunnittelua kannattaa käyttää, jos ennustemalli on määritetty pääsuunnitelmaan. |
| Suunniteltujen tilausten numerosarjat | Suunniteltujen tilausten numerosarjoja ei tueta. Suunnitellut tilausnumerot luodaan palvelupuolelle. |
| Suunnitelman kopiointi, suunnittelun poistaminen ja suunnitteluversion tyhjennys | <p>Seuraavat nimikkeet on poistettu käytöstä siirtymisruudun kohdassa **Pääsuunnittelu \> Pääsuunnittelu \> Suunnittelun ylläpito**:</p><ul><li>Suunnitelman kopio</li><li>Poista suunnitelma</li><li>Suunnitelmaversion siivous</li></ul> |
| Palautustilaukset | Palautustilauksia ei ole oteta huomioon. |
| Liittyvien ominaisuuksien aikatauluttaminen | Lisätietoja on kohdassa [Ajoittaminen rajattoman kapasiteetin avulla](infinite-capacity-planning.md#limitations). |
| Kuljetuskalenteri | **Toimitustavat**-sivun **Kuljetuskalenteri**-sarakkeen arvo ohitetaan. |

## <a name="additional-resources"></a>Lisäresurssit

- [Suunnittelun optimoinnin sopivuusanalyysi](planning-optimization-fit-analysis.md)
- [Parametrit, joita ei käytetä suunnittelun optimoinnissa](not-used-parameters.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
