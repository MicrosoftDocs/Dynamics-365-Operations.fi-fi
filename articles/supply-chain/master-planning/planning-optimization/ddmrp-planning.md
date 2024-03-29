---
title: Kysyntäperustainen suunnittelu
description: Tässä artikkelissa käsitellään suunniteltujen tilausten luontia nimikkeille, jotka on määritetty erotuspisteiksi.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 8ba9a6d24923b66259bc8b6cc688ec667cb000de
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740299"
---
# <a name="demand-driven-planning"></a>Kysyntäperustainen suunnittelu

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Tässä artikkelissa käsitellään suunniteltujen tilausten luontia nimikkeille, jotka on määritetty erotuspisteiksi.

## <a name="net-flow-and-qualified-demand"></a>Nettovirta ja hyväksytty kysyntä

Pääsuunnittelun aikana järjestelmä muodostaa *nettovirta*-käsitteen avulla voimassa olevan käytettävissä olevan määrän sen perusteella, mikä on todellinen käytettävissä oleva määrä sekä siihen lisätty tilattu määrä (toimitustilaukset, joita ei ole vielä vastaanotettu) ja siitä vähennetty *hyväksytty kysyntä* (hyväksytty tuleva myynti). Tämän esitetään seuraavassa kuvassa. Kun järjestelmä määrittää, mihin puskurivyöhykkeeseen nimike kuuluu ja mikä tilattavan määrän on oltava, kyse on nettovirran eikä todellisen käytettävissä olevan varaston arvioinnista.

![Esimerkki nettovirran laskentakaaviosta](media/ddmrp-net-flow-example.png "Esimerkki nettovirran laskentakaaviosta")

Kun suunniteltu tilaus käynnistyy suunnittelun suorittamisen aikana, tilattu määrä on enimmäismäärä, josta on vähennetty nettovirta. Järjestelmä käyttää tilauksen prioriteetin määrittämiseen [prioriteettipohjaista suunnittelutoimintoa](priority-based-planning.md) eikä tarvepäiviä. DDMRP (kysyntäperustainen materiaalitarvesuunnittelu) määrittää suunnitellun tilauksen prioriteetin sen perusteella, mikä on tilatun määrän prosenttiosuus enimmäisvarastosta. Edellisessä kuvassa tilattu määrä on 53 prosenttia enimmäisvarastosta. Niinpä tilauksen prioriteetti täydennyksen osalta on 53. (Mainittakoon, että 0 on korkein prioriteetti ja 100 alhaisin prioriteetti.)

*Hyväksytty kysyntä* on erääntynyt kysyntä, johon on lisätty kuluvan päivän kysyntä ja hyväksytyt tilauspiikit tulevaisuudessa. Seuraavassa kuvassa on esimerkki kuluvan päivän (12. kesäkuuta) ja kolmen seuraavan päivän kysyntätasoista. DDMRP:n avulla voidaan määrittää tilauspiikin raja-arvo ilmaisemaan normaalisti odotettavissa olevan kysynnän ylittävän kysynnän. Jos raja-arvoksi on määritetty 25 kappaletta, kuvassa olevista tulevista päivistä kaksi on tilauspiikkejä. Tilauspiikin raja-arvo on määritettävä kullekin tuotteelle erikseen tuotteen **Nimikkeen kattavuus** -sivulla, mistä on lisätietoja kohdassa [Erotuspistenimikkeen puskurien määrittäminen](ddmrp-buffer-profile-and-levels.md#set-up-buffers).

![Esimerkki hyväksytyn kysynnän laskentakaaviosta](media/ddmrp-net-qualified-demand-example.png "Esimerkki hyväksytyn kysynnän laskentakaaviosta")

Mikäli erääntynyttä kysyntää ei ole, kuluvan päivän kysyntä (18) voidaan nyt lisätä kahden tilauspiikin (29 ja 26) määrään, jolloin hyväksyttävän kysynnän tulokseksi saadaan 73. Vaikka 23. kesäkuuta on kysyntää, kannattaa huomata, että sitä ei sisällytetä nettovirtalaskelmaan, sillä DDMRP käynnistää suunnitellun tilauksen eri tavalla kuin perinteiset suunnittelun kattavuusryhmät.

## <a name="generating-planned-orders-with-ddmrp"></a>Suunniteltujen tilausten luominen DDMRP:n avulla

Järjestelmä luo suunnitteluajon aikana uuden suunnitellun tilauksen, jos nimikkeen nettovirta alittaa uudelleentilauspisteen. DDMRP:tä käytettäessä suunnitteluajo tehdään yleensä joka päivä. Käytännössä siis varastotasot tarkistetaan kerran päivässä, ja tarkistuksen perusteella määritetään, mitä nimikkeitä on täydennettävä.

Seuraavassa kuvassa on esimerkki tilanteesta, josta tilauksen koko on 20. kesäkuuta 18 kappaletta, 21. kesäkuuta 29 kappaletta, 22. kesäkuuta 26 kappaletta ja 23. kesäkuuta 20 kappaletta. Koska tilauspiikin raja-arvoksi on määritetty 25 kappaletta, kaksi tilausta merkitään piikeiksi. Kyseistä nimikettä on käytettävissä 220 kappaletta.

![Suunnitteluesimerkki 1](media/ddmrp-planning-example-1.png "Suunnitteluesimerkki 1")

Jos pääsuunnittelu suoritetaan nyt, se luo suunnittelun tilauksen, jos nettovirran havaitaan alittavan uudelleentilauspisteen (tässä esimerkissä 219 kappaletta).

![Suunnitteluesimerkki 2](media/ddmrp-planning-example-2.png "Suunnitteluesimerkki 2")

Tässä esimerkissä luodaan 130 kappaleen suunniteltu ostotilaus. Tämä luku on yhtä suuri kuin enimmäistaso, josta on vähennetty nettovirta. Suunnitellun tilauksen prioriteetiksi määritetään 53,07, ja tämä arvo perustuu prosenttiosuuteen enimmäismäärästä. Koska nämä arvot havaittiin 20. kesäkuuta, järjestelmä luo 20. kesäkuuta päivätyn suunnitellun tilauksen ja lisää siihen nimikkeen erotetun läpimenoajan (tässä esimerkissä viisi arkipäivää). Koska viisiarkipäivää on viikko kuluvasta päivästä, suunnitellun tilauksen päivämääräksi merkitään 27. kesäkuuta.

> [!NOTE]
> Pääsuunnittelu laskee vain erotetut nimikkeet DDMRP:n avulla. Kaikki muut nimikkeet lasketaan käyttämällä vakiotarvelaskentaa (MRP).
