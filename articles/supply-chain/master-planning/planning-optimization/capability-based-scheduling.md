---
title: Aikataulutus resurssien valinnalla kykyjen perusteella
description: Tässä artikkelissa kuvataan resurssin valintaa rajattoman kapasiteetin ajoituksen aikana, kun toimintoja määritetään operaation resurssitarpeiksi.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
ms.search.form: RouteInventProd, WrkCtrTable, WrkCtrCapability
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4a3c8236183b81ad015b43d7dbf869c177eafd44
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335402"
---
# <a name="scheduling-with-resource-selection-based-on-capability"></a>Ajoitus resurssivalintojen avulla toiminnon perusteella

[!include [banner](../../includes/banner.md)]

Määrittämällä tuotantoreitityksen operaation resurssitarpeet voit määrittää, mitä operaation suorittamiseen tarvitaan. Operaatio voi esimerkiksi edellyttää tiettyä resurssia, resurssiryhmää tai taitojen tai toimintojen yhdistelmää. Tässä artikkelissa kuvataan resurssin valintaa rajattoman kapasiteetin ajoituksen aikana, kun toimintoja määritetään operaation resurssitarpeiksi.

## <a name="turn-the-capability-based-scheduling-feature-on-or-off"></a>Toimintopohjainen ajoitus -toiminnon käyttöönotto tai käytöstäpoisto

Jos haluat käyttää tätä ominaisuutta, se on otettava käyttöön järjestelmässä. Supply Chain Managementin versiosta 10.0.29 alkaen tämä ominaisuus on oletusarvoisesti käytössä. Järjestelmänvalvojat voivat ottaa tämän toiminnon käyttöön tai pois käytöstä hakemalla *Suunnittelun optimoinnin ääretön kapasiteetin ajoitus* -toimintoa [Toimintojen hallinta](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilasta.

Lisätietoja tästä ominaisuudesta on kohdassa [Ajoittaminen rajattoman kapasiteetin avulla](infinite-capacity-planning.md).

## <a name="capability-based-scheduling"></a>Toimintopohjainen ajoitus

Toiminto on operaatioresurssin kyky suorittaa tietty aktiviteetti. Yksittäiselle operaatioresurssille voidaan delegoida enemmän kuin yksi toiminto, ja yksittäinen toiminto voidaan delegoida enemmän kuin yhdelle resurssille. Toimintoja voi delegoida kaikentyyppisille resursseille: työkaluille, toimittajille, koneille, toimipaikoille, toimitiloille ja henkilöstölle.

Kun määrität toimintoja resurssitarpeiksi, voit siirtää resurssien varaamista, kunnes tilaukset ajoitetaan. Sen sijaan, että delegoisit tiettyjä resursseja tai resurssiryhmiä reititysoperaatioon, voit määrittää kussakin reititysoperaatiossa tarvittavat toiminnot. Ajoituksen aikana järjestelmä yhdistää sitten pakolliset toiminnot toimintoihin, jotka resursseille on määritetty. Järjestelmä valitsee vain vaatimukset täyttävät resurssit.

Jos haluat delegoida toimintoja operaatioresurssille, käytä **Toiminnot**-pikavälilehteä **Resurssit**-sivulla. Jos haluat delegoida resursseja toiminnolle, käytä **Resurssit**-pikavälilehteä **Resurssitoiminnot**-sivulla. Molemmat sivut ovat käytössä siirtymisruudun kohdassa **Tuotannon hallinta \> Määritys \> Resurssit**. Molemmat pikavälilehdet sisältävät ruudukon, joka sisältää valittuun resurssiin tai toimintoon liittyvät resurssit. Molemmissa pikavälilehdissä on myös työkalurivi, jonka avulla voit lisätä, poistaa ja muokata ruudukon rivejä. Ruudukko sisältää seuraavat sarakkeet:

- **Resurssi** tai **Toiminto** – Valitse resurssi tai toiminto, jota rivi delegoi.
- **Kuvaus** – Syötä lyhyt kuvaus resurssille tai toiminnolle.
- **Voimaantulopäivä** – Määritä ensimmäinen päivämäärä, jolloin resurssin tai toiminnon määritys on voimassa. Ajoituksen aikana järjestelmä ei käytä resurssia tai toimintoa, johon on tehty vanhentunut kapasiteettimääritys, vaikka resurssi muutoin täyttää vaatimukset.
- **Päättyminen** – Määritä viimeinen päivämäärä, jolloin resurssin tai toiminnon määritys on voimassa. Ajoituksen aikana järjestelmä ei käytä resurssia tai toimintoa, johon on tehty vanhentunut kapasiteettimääritys, vaikka resurssi muutoin täyttää vaatimukset.
- **Taso** – Määritä pätevyystaso, joka resurssilla on oltava toiminnossa. Jos määrität **Vaadittu vähimmäistaso** -arvon resurssi- tai toimitotarpeelle, ajoitusydin ottaa huomioon pätevyystason resurssin valinnan aikana. Järjestelmä valitsee sitten vain ne resurssit, joilla on tarvittavat ominaisuudet tasolla, joka vastaa resurssivaatimuksessa määriteltyä vähimmäistasoa tai on sitä suurempi.
- **Prioriteetti** – Suunnittelun optimointi ei vielä tue tätä kenttää. Jos kuitenkin käytät sisäistä suunnitteluydintä, voit määrittää **Prioriteetti**-kentän resurssi- tai toimintomäärityksessä määrittääksesi resurssin prioriteetin. Jos *Prioriteetti* on valittu **Ensisijaisen resurssin valinta** -kentässä **Ajoitusparametrit** -sivulla, järjestelmä valitsee ajoituksen aikana ensimmäiseksi resurssin, jolla on korkein prioriteetti (alhaisin numeerinen arvo **Prioriteetti**-kentässä).

## <a name="example"></a>Esimerkki

Tässä esimerkissä kerrotaan, miten ajoitusydin valitsee resurssit toiminnon perusteella.

Tuotantoreititys sisältää viisi operaatiota: *10*, *20*, *30*, *40* ja *50*. Kukin reitityksen operaatio vaatii resurssin, jolla on eri toiminnot. Esimerkiksi reititysvaihe *10* vaatii resurssin, jolla on kaiuttimen kokoamistoiminto (*0050 Spkr Assembly*) ja puutyötoiminto (*1010 Wood capabilities*). Reititysoperaatio *50* vaatii resurssin, jolla on tuotteen pakkaamistoiminto (*0070 Packing capability*).

![Ajoitukseen käytettävä toiminto.](media/capability-based-scheduling.png "Ajoitukseen käytettävä toiminto.")

Ydin etsii ajoituksen aikana resurssit, jotka täyttävät operaation vaatimukset. Ajoitusydin valitsee esimerkiksi resurssin *00101* suorittamaan operaation *10*, koska kyseinen resurssi on ensimmäinen löydetty resurssi, jolla on molemmat vaaditut toiminnot. Ajoitusydin valitsee esimerkiksi resurssin *00301* suorittamaan operaation *50*, koska kyseinen resurssi on ainoa löydetty resurssi, jolla on pakkaustoiminto.

Mieti seuraavaksi, miten tämä esimerkki muuttuu, kun käytetään pätevyystasoja:

- Operaatio *10* vaatii pätevyyden vähimmäistason *7* *0059 Assembly* -toiminnossa.
- Resurssilla *00101* on pätevyystaso *5* *0059 Assembly* -toiminnossa.
- Resurssilla *00102* on pätevyystaso *10* *0059 Assembly* -toiminnossa.

Tässä tapauksessa äärettömän kapasiteetin ajoituksen aikana ajoitusydin valitsee resurssin *00102* suorittamaan operaation *10*, koska tällä resurssilla, toisin kuin resurssilla *00101*, on vaadittu pätevyystaso kyseisessä toiminnossa.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
