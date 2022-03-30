---
title: Sisäisen pääsuunnittelun ja suunnittelun optimoinnin erot
description: Tässä aiheessa on luettelo ominaisuuksista, joita suunnittelun optimointi ei vielä tue ja joita ei mainita suunnittelun optimoinnin sopivuusanalyysisivulla.
author: ChristianRytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 575aef709a0ac3b0cf8150f1e816dac04c069814
ms.sourcegitcommit: ddcab9726e9dbcf3296cb0988b97a3ae7ccb3dfb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2022
ms.locfileid: "8396496"
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
| Suunniteltujen tilausten numerosarjat | Suunniteltujen tilausten numerosarjoja ei tueta. Suunnitellut tilausnumerot luodaan palvelupuolelle. Suunnitellussa tilausnumerossa näkyy tavallisesti 10 numeroa, mutta numerosarja perustuu todellisuudessa 20 merkkiin, joista suunnittelusuorituksen laskentaan kohdistetaan 10 numeroa ja suunniteltujen tilausten laskentaan 10 muuta numeroa. |
| Suunnitelman kopiointi, suunnittelun poistaminen ja suunnitteluversion tyhjennys | <p>Seuraavat nimikkeet on poistettu käytöstä siirtymisruudun kohdassa **Pääsuunnittelu \> Pääsuunnittelu \> Suunnittelun ylläpito**:</p><ul><li>Suunnitelman kopio</li><li>Poista suunnitelma</li><li>Suunnitelmaversion siivous</li></ul> |
| Palautustilaukset | Palautustilauksia ei ole oteta huomioon. |
| Liittyvien ominaisuuksien aikatauluttaminen | Lisätietoja on kohdassa [Ajoittaminen rajattoman kapasiteetin avulla](infinite-capacity-planning.md#limitations). |
| Varmuusvaraston täyttäminen | Suunnittelun optimointi käyttää aina *Tämän päivän päivämäärä + hankinta-aika* -vaihtoehtoa **Täytä vähimmäisarvo** -kentälle **Nimikkeen kattavuus** -sivulla. Tämä helpottaa tahattoman suunnitellun tilauksen ja muiden ongelmien estämistä, sillä jos toimitusaika ei sisälly varmuusvarastoon, nykyiselle alhaiselle käytettävissä olevalle varastolle luodut suunnitellut tilaukset viivästyvät aina läpimenoajan vuoksi. |
| Varmuusvaraston tarvekohdistus ja nettotarpeet | *Varmuusvarasto*-vaatimustyyppi ei kuulu **Nettotarpeet**-sivuun eikä se näy kyseisellä sivulla. Varmuusvarasto ei edusta kysyntää eikä siihen liity tarvepäivämäärää. Sen sijaan se asettaa rajoituksen sille, kuinka paljon varastoa on oltava aina käytettävissä. **Pienin arvo**-kenttä otetaan silti huomioon, kun suunniteltuja tilauksia lasketaan pääsuunnittelun aikana. On suositeltavaa tarkistaa **Kertynyt määrä** -sarake **Nettotarpeet**-sivulla, jotta nähdään, että tämä arvo otettiin huomioon. |
| Kuljetuskalenteri | **Toimitustavat**-sivun **Kuljetuskalenteri**-sarakkeen arvo ohitetaan. |
| Kattavuuden vähimmäis-/enimmäiskoodi ilman arvoja| Kun käytössä on sisäinen suunnittelumoduuli, jossa käytetään vähimmäis-/enimmäiskattavuuskoodia, jossa ei ole määritetty vähimmäis- tai enimmäisarvoja, suunnittelumoduuli käsittelee kattavuuskoodia vaatimuksena ja luo yhden tilauksen kutakin tarvetta varten. Suunnittelun optimointia käytetään, kun järjestelmä luo yhden tilauksen päivää kohden, jotta se kattaa päivän koko summan.  |

## <a name="additional-resources"></a>Lisäresurssit

- [Suunnittelun optimoinnin sopivuusanalyysi](planning-optimization-fit-analysis.md)
- [Parametrit, joita ei käytetä suunnittelun optimoinnissa](not-used-parameters.md)
- [Suunnittelun optimoinnissa käytetyt päivämäärä- ja aikaparametrit](date-time-used.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
