---
title: Rajoittamattoman kapasiteetin ajoitus
description: Tässä aiheessa on tietoja rajattoman kapasiteetin ajoituksesta suunnittelun optimointia varten. Lisäksi siinä kuvataan ominaisuuden tämänhetkiset rajoitukset.
author: crytt
ms.date: 6/9/2021
ms.topic: article
ms.search.form: RouteInventProd
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8c493522ea55dd7e69c0133aceef43a3e59021c3
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6361333"
---
# <a name="scheduling-with-infinite-capacity"></a>Rajoittamattoman kapasiteetin ajoitus

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

*Rajattoman kapasiteetin ajoitus suunnittelun optimoinnille* -ominaisuus sallii reittitietoihin perustuvan ajoituksen. Se sallii sinun ajoittaa töitä monen eri reititysasetuksen perusteella. Suunnittelun optimoinnin ajoitus kattaa usein käytetyt reititysasetukset, kuten reitityksen työvaiheiden järjestyksen tai reitityksen työvaiheiden resurssien vaatimukset.

## <a name="turn-on-the-infinite-capacity-scheduling-feature"></a>Rajattoman kapasiteetin ajoitus -ominaisuuden ottaminen käyttöön

Jos järjestelmäsi ei vielä sisällä tässä aiheessa kuvattua ominaisuutta, avaa [Ominaisuuksien hallinta](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtila ja ota *Rajattoman kapasiteetin ajoitus suunnittelun optimoinnille* -ominaisuus käyttöön.

## <a name="added-functionality"></a>Lisätoiminnot

*Rajattoman kapasiteetin ajoitus suunnittelun optimoinnille* -ominaisuus sallii töiden ajoituksen reittitietojen perusteella. Näin ollen tuotantoprosessien ajoittaiseen voidaan käyttää reititysasetusta. Vaikka tällä ominaisuudella on rajoituksia, joita sisäisellä pääsuunnittelumoduulilla ei ole, se tukee yleisimpiä valmistusskenaarioiden vaatimia toimintoja.

Ominaisuus ottaa huomioon sekä *yksinkertaiset reitit* että *reittiverkostot*. Käyttämällä reittitoiminnon **Seuraava**-kenttää voit määrittää monimutkaisia reittejä, joilla on useita lähtöpaikkoja ja useita rinnakkain suoritettavia työvaiheita. Järjestelmä ottaa huomioon tämäntyyppiset monimutkaisten reittien rakenteet ajoituksen aikana.

Lisäksi ominaisuus tukee *rinnakkaisia työvaiheita* reitityksissä. Käyttämällä reitityksen työvaiheiden **Prioriteetti**-kentän *Ensisijainen*- ja *Toissijainen*-vaihtoehtoja voit määrittää reittirakenteen, jossa yksi reitin työvaihe on ensisijainen työvaihe ja toinen on työvaihe on toissijainen. Tällöin järjestelmä ottaa huomioon reittien rakenteen ajoituksen aikana.

Järjestelmä huomioi ajoitusprosessin aikana myös työvaihetta koskevat *resurssivaatimukset*. Järjestelmä käyttää resurssivaatimuksia määrittääkseen työvaiheen suorittamiseen tarvittavat resurssit. *Rajattoman kapasiteetin ajoitus suunnittelun optiminnoille* -ominaisuus tukee tällä hetkellä seuraavantyyppisiä resurssivaatimuksia:

- Resurssityyppi
- Resurssi
- Resurssiryhmä
- Ominaisuus

> [!NOTE]
> Henkilöstöhallintoon liittyviä vaatimuksia, kuten osaamisalueita tai todistusvaatimuksia, ei tueta vielä.

Ominaisuus tukee myös operatiivisia **Asetusaika**- ja **Ajoaika**-ominaisuuksia. Kun määrität nämä ominaisuudet reitityksen työvaiheelle, ajoitusprosessi luo asianmukaiset asetus- ja prosessityöt.

Yhteenvetona todettakoot, että suunnittelun optimoinnin ajoitus tukee useimmin käytettyjä skenaarioita. Voit luoda reitin, lisätä ensisijaisia ja toissijaisia työvaiheita, määrittää seuraavat työvaiheet, lisätä resurssivaatimuksia sekä lisätä asetus- ja ajoajan. Tällöin järjestelmä ottaa nämä tiedot huomioon ajoituksen aikana.

## <a name="limitations"></a>Rajoitukset

Seuraavat rajoitukset ovat voimassa, kun käytät suunnittelun optimoinnin ajoitusta:

- Ominaisuus tukee vain töiden ajoittamista. Työvaiheiden ajoitukseen liittyviä asetuksia ei ottaa huomioon ajoituksen aikana, riippumatta pääsuunnitelmien ajoitusmenetelmästä.
- Ominaisuus tukee vain rajatonta kapasiteettia.
- Ominaisuus ei tue resurssien kuormitustoimintoja.
- Ominaisuus ei ota huomioon reitityksen hävikkiä.
- Ominaisuus tukee *Kesto*-vaihtoehtoa vain ensisijaisen resurssin valintana.

Huomaa, että *Rajattoman kapasiteetin ajoitus suunnittelun optimoinnille* -ominaisuutta parannetaan jatkuvasti. Microsoft pyrkii tukemaan muita ajoitusasetuksia tulevissa versioissa.
