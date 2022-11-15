---
title: Suunnittelun optimoinnin ja vanhentuneen pääsuunnittelumoduulin erot
description: Tässä artikkelissa on luettelo ominaisuuksista, joita suunnittelun optimointi ei vielä tue ja joita ei mainita suunnittelun optimoinnin sopivuusanalyysisivulla.
author: t-benebo
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 6e1671a508b85a94ac9687af15e898d885ea94c1
ms.sourcegitcommit: 55e440e30490b2d36d86b22aa1263d5da97633aa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/04/2022
ms.locfileid: "9745358"
---
# <a name="differences-between-planning-optimization-and-the-deprecated-master-planning-engine"></a>Suunnittelun optimoinnin ja vanhentuneen pääsuunnittelumoduulin erot

[!include [banner](../../includes/banner.md)]

Suunnittelun optimoinnin tulokset voivat olla erilaiset kuin vanhentuneen pääsuunnittelumoduulin tulokset. Erot voivat johtua odottavista ominaisuuksista. Tässä artikkelissa on luettelo ominaisuuksista, joita suunnittelun optimointi ei vielä tue ja joita ei mainita **[Suunnittelun optimoinnin sopivuusanalyysi](planning-optimization-fit-analysis.md)** -sivulla.

| Ominaisuus | Nykyinen suunnittelun optimoinnin toiminta |
|---|---|
| Todellisen painon tuotteet | Todellisen painon tuotteita pidetään tavallisina tuotteina.|
| Laajennettavat dimensiot | Suunnittelun optimointi ei tue laajennettavia dimensioita. Suunnittelun optimoinnin käyttämisen aikana laajennettavat dimensiot ovat tyhjiä suunnitelluissa tilauksissa, vaikka **Kattavuussuunnitelma dimension mukaan** -valintaruutu olisi valittu **Varastodimensioryhmät** tai **Seurantadimensioryhmät**-sivulla. |
| Suodatetut tuotantoajot | Lisätietoja on kohdassa [Tuotannon suunnittelu – suodattimet](production-planning.md#filters). |
| Ennusteen suunnittelu | Ennusteen suunnittelua ei tueta. Pääsuunnittelua kannattaa käyttää, jos ennustemalli on määritetty pääsuunnitelmaan. |
| Suunniteltujen tilausten numerosarjat | Suunniteltujen tilausten numerosarjoja ei tueta. Suunnitellut tilausnumerot luodaan palvelupuolelle. Suunnitellussa tilausnumerossa näkyy tavallisesti 10 numeroa, mutta numerosarja perustuu todellisuudessa 20 merkkiin, joista suunnittelusuorituksen laskentaan kohdistetaan 10 numeroa ja suunniteltujen tilausten laskentaan 10 muuta numeroa. |
| Suunnitelman kopiointi, suunnittelun poistaminen ja suunnitteluversion tyhjennys | <p>Seuraavat nimikkeet on poistettu käytöstä siirtymisruudun kohdassa **Pääsuunnittelu \> Pääsuunnittelu \> Suunnittelun ylläpito**:</p><ul><li>Suunnitelman kopio</li><li>Poista suunnitelma</li><li>Suunnitelmaversion siivous</li></ul> |
| Palautustilaukset | Palautustilauksia ei ole oteta huomioon. |
| Liittyvien ominaisuuksien aikatauluttaminen | Lisätietoja on kohdassa [Ajoittaminen rajattoman kapasiteetin avulla](infinite-capacity-planning.md#limitations). |
| Varmuusvaraston täyttäminen | Suunnittelun optimointi käyttää aina *Tämän päivän päivämäärä + hankinta-aika* -vaihtoehtoa **Täytä vähimmäisarvo** -kentälle **Nimikkeen kattavuus** -sivulla. Tämä helpottaa tahattoman suunnitellun tilauksen ja muiden ongelmien estämistä, sillä jos toimitusaika ei sisälly varmuusvarastoon, nykyiselle alhaiselle käytettävissä olevalle varastolle luodut suunnitellut tilaukset viivästyvät aina läpimenoajan vuoksi. |
| Varmuusvaraston tarvekohdistus ja nettotarpeet | *Varmuusvarasto*-vaatimustyyppi ei kuulu **Nettotarpeet**-sivuun eikä se näy kyseisellä sivulla. Varmuusvarasto ei edusta kysyntää eikä siihen liity tarvepäivämäärää. Sen sijaan se asettaa rajoituksen sille, kuinka paljon varastoa on oltava aina käytettävissä. **Pienin arvo**-kenttä otetaan silti huomioon, kun suunniteltuja tilauksia lasketaan pääsuunnittelun aikana. On suositeltavaa tarkistaa **Kertynyt määrä** -sarake **Nettotarpeet**-sivulla, jotta nähdään, että tämä arvo otettiin huomioon. Koska tarvekohdistus on erilaista, saatetaan ehdottaa erilaisia toimintoja. |
| Kuljetuskalenteri | **Toimitustavat**-sivun **Kuljetuskalenteri**-sarakkeen arvo ohitetaan. |
| Kattavuuden vähimmäis-/enimmäiskoodi ilman arvoja| Kun käytössä on vanhentunut pääsuunnittelumoduuli ja käyttämälläsi vähimmäis-/enimmäiskattavuuskoodille ei ole määritetty vähimmäis- tai enimmäisarvoja, suunnittelumoduuli käsittelee kattavuuskoodia vaatimuksena ja luo yhden tilauksen kutakin tarvetta varten. Suunnittelun optimointia käytetään, kun järjestelmä luo yhden tilauksen päivää kohden, jotta se kattaa päivän koko summan.  |
| Nettotarpeet ja manuaalisesti luodut suunnitellut tilaukset | Vanhentuneen pääsuunnittelumoduulin avulla nimikkeelle luodut manuaalisesti luodut toimitustilaukset näkyvät automaattisesti nimikkeen nettotarpeiden joukossa. Kun esimerkiksi luot ostotilauksen myyntitilauksesta, ostotilaus näkyy **Nettotarpeet**-sivulla ilman, että aiempia toimenpiteitä tarvitaan. Tämä johtuu siitä, että vanhentunut pääsuunnittelumoduuli kirjaa varastotapahtumat `inventLogTTS`-taulukkoon ja näyttää muutokset dynaamisten suunnitelmien **Nettotarpeet**-sivulla. Suunnittelun optimointia käytettäessä manuaalisesti luodut tilaukset eivät kuitenkaan näy nimikkeen nettotarpeissa, ennen kuin suunnittelun optimointi suoritetaan (käyttäen suunnitelmaa, joka sisältää nimikkeen) tai ennen kuin valitset **Nettotarpeet**-sivun toimintoruudussa **Päivitä \> Pääsuunnittelu**, mikä suorittaa nimikkeen pääsuunnittelun. Lisätietoja **Nettotarpeet**-sivun käytöstä on kohdassa [Nettotarpeet ja tarvekohdistustiedot](net-requirements.md). |
| Resurssimääritys | Kun käytössä on rajaton kapasiteetti, vanhentunut pääsuunnittelumoduuli delegoi kaikki suunnitellut tilaukset määritetyn resurssiryhmän samalle resurssille. Suunnittelun optimointi parantaa tätä valitsemalla resurssit satunnaisessa järjestyksessä, jotta eri tuotantotilaukset voivat käyttää eri resursseja. Jos haluat käyttää samaa resurssia kaikissa suunnitelluissa tilauksissa, sinun on määritettävä tämä resurssi reitille. |
| Laajennetut tietotyypit (EDT:t) | Suunnittelun optimointi ei tue EDT:n tarkkuuden muutoksia. Tämä tarkoittaa, että prosessia ei tueta virallisesti, eikä sen voida taata toimivan. |
| Varmuusvaraston täyttäminen | Suunnittelun optimointi käyttää aina *Tämän päivän päivämäärä + hankinta-aika* -parametrin **Täytä vähimmäisarvo** -arvoa. Tämä valmistelee järjestelmän käyttämään yksinkertaistettuja suunnitteluasetuksia tulevaisuudessa ja tarjoaa tuloksen, jonka perusteella toimia. Jos toimitusaika ei sisälly varmuusvarastoon, alhaiselle käytettävissä olevalle varastolle luodut suunnitellut tilaukset viivästyvät aina läpimenoajan vuoksi. Tämä voi aiheuttaa merkittäviä meluongelmia ja ei-toivottuja suunniteltuja tilauksia. Paras käytäntö on muuttaa asetusta käyttämään *Tämän päivän päivämäärä + hankinta-aika* -arvoa. Päivitä päätiedot ja varoitusten välttämiseksi. |
| Kopioi staattinen dynaamiseen suunnitelmaan | Suunnittelun optimointi ei kopioi staattisia suunnitelmia dynaamisiin suunnitelmiin riippumatta **Pääsuunnittelun parametrit** -asetuksesta. Tavallisesti tämä toiminto ei ole kovin merkityksellinen suunnittelun optimoinnin nopeuden ja täydellisen uudistamisen ansiosta. Jos käytössä on vähintään kaksi suunnitelmaa, pääsuunnittelu on käynnistettävä kunkin suunnitelman osalta. |

## <a name="additional-resources"></a>Lisäresurssit

- [Suunnittelun optimoinnin sopivuusanalyysi](planning-optimization-fit-analysis.md)
- [Parametrit, joita ei käytetä suunnittelun optimoinnissa](not-used-parameters.md)
- [Suunnittelun optimoinnissa käytetyt päivämäärä- ja aikaparametrit](date-time-used.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
