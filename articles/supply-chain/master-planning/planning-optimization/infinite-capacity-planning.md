---
title: Äärettömän kapasiteetin aikatauluttaminen
description: Tässä artikkelissa on tietoja rajoittamattoman kapasiteetin ajoittamisesta. Lisäksi siinä kuvataan ominaisuuden tämänhetkiset rajoitukset.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
ms.search.form: RouteInventProd
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 7249734e5d2644145a36276dbc818a40b5962805
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740002"
---
# <a name="scheduling-with-infinite-capacity"></a>Aikatauluttaminen äärettömällä kapasiteetilla

[!include [banner](../../includes/banner.md)]

*Rajattoman kapasiteetin ajoitus suunnittelun optimoinnille* -ominaisuus sallii reittitietoihin perustuvan ajoituksen. Se sallii sinun ajoittaa töitä monen eri reititysasetuksen perusteella. Ajoitus kattaa usein käytetyt reititysasetukset, kuten reitityksen työvaiheiden järjestyksen tai reitityksen työvaiheiden resurssien vaatimukset.

## <a name="turn-the-infinite-capacity-scheduling-feature-on-or-off"></a>Rajattoman kapasiteetin ajoitus -toiminnon käyttöönotto tai käytöstäpoisto

Jos haluat käyttää tätä ominaisuutta, se on otettava käyttöön järjestelmässä. Supply Chain Managementin versiosta 10.0.29 alkaen tämä ominaisuus on oletusarvoisesti käytössä. Järjestelmänvalvojat voivat ottaa tämän toiminnon käyttöön tai pois käytöstä hakemalla *Suunnittelun optimoinnin ääretön kapasiteetin ajoitus* -toimintoa [Toimintojen hallinta](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilasta.

Lisätietoja tästä ominaisuudesta on kohdassa [Ajoitus resurssin valinnan avulla ja ominaisuuden perusteella](capability-based-scheduling.md).

## <a name="added-functionality"></a>Lisätoiminnot

*Rajattoman kapasiteetin ajoitus suunnittelun optimoinnille* -ominaisuus sallii töiden ajoituksen reittitietojen perusteella. Näin ollen tuotantoprosessien ajoittaiseen voidaan käyttää reititysasetusta. Vaikka tällä ominaisuudella on rajoituksia, joita vanhentuneella pääsuunnittelumoduulilla ei ole, se tukee yleisimpiä valmistusskenaarioiden vaatimia toimintoja.

Ominaisuus ottaa huomioon sekä *yksinkertaiset reitit* että *reittiverkostot*. Käyttämällä reittitoiminnon **Seuraava**-kenttää voit määrittää monimutkaisia reittejä, joilla on useita lähtöpaikkoja ja useita rinnakkain suoritettavia työvaiheita. Järjestelmä ottaa huomioon tämäntyyppiset monimutkaisten reittien rakenteet ajoituksen aikana.

Lisäksi ominaisuus tukee *rinnakkaisia työvaiheita* reitityksissä. Käyttämällä reitityksen työvaiheiden **Prioriteetti**-kentän *Ensisijainen*- ja *Toissijainen*-vaihtoehtoja voit määrittää reittirakenteen, jossa yksi reitin työvaihe on ensisijainen työvaihe ja toinen on työvaihe on toissijainen. Tällöin järjestelmä ottaa huomioon reittien rakenteen ajoituksen aikana.

Järjestelmä huomioi ajoitusprosessin aikana myös työvaihetta koskevat *resurssivaatimukset*. Järjestelmä käyttää resurssivaatimuksia määrittääkseen työvaiheen suorittamiseen tarvittavat resurssit. *Rajattoman kapasiteetin ajoitus suunnittelun optiminnoille* -ominaisuus tukee tällä hetkellä seuraavantyyppisiä resurssivaatimuksia:

- Resurssityyppi
- Resurssi
- Resurssiryhmä
- Ominaisuus (Lisätietoja on kohdassa [Ajoitus resurssin valinnan avulla ja ominaisuuden perusteella](capability-based-scheduling.md).)

> [!NOTE]
>
> - Jos resurssi ja/tai resurssiryhmä on asetettu rajattoman kapasiteetin arvoksi, pääsuunnittelu pitää niitä rajattomana kapasiteetina.
> - Henkilöstöhallintoon liittyviä vaatimuksia, kuten osaamisalueita tai todistusvaatimuksia, ei tueta vielä.

Ominaisuus tukee myös operatiivisia **Asetusaika**- ja **Ajoaika**-ominaisuuksia. Kun määrität nämä ominaisuudet reitityksen työvaiheelle, ajoitusprosessi luo asianmukaiset asetus- ja prosessityöt.

Yhteenvetona todettakoon, että ajoitus tukee useimmin käytettyjä skenaarioita. Voit luoda reitin, lisätä ensisijaisia ja toissijaisia työvaiheita, määrittää seuraavat työvaiheet, lisätä resurssivaatimuksia sekä lisätä asetus- ja ajoajan. Tällöin järjestelmä ottaa nämä tiedot huomioon ajoituksen aikana.

## <a name="limitations"></a>Rajoitukset

Seuraavat rajoitukset ovat voimassa, kun käytät *Suunnittelun optimoinnin ääretön kapasiteetin ajoitus* -ominaisuutta:

- Ominaisuus tukee vain rajatonta kapasiteettia.
- Ominaisuus ei tue resurssien kuormitustoimintoja.
- Ominaisuus ei ota huomioon reitityksen hävikkiä.
- Ominaisuus tukee *Kesto*-vaihtoehtoa vain ensisijaisen resurssin valintana.
