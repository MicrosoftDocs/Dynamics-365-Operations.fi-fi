---
title: Työtunnusten yhdistetty numerosarja
description: Tämä ominaisuus tarjoaa yhden yhdistetyn numerosarjan, joka luo työn tunnukset tuotannon hallinnassa, valmistuksen suorittamisen sekä aika- ja läsnäolomoduulissa.
author: johanhoffmann
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8ff8fae0bb20b11b15c7520fbb14727ff0372ca0255adc82599c6680a64671af
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748712"
---
# <a name="unified-number-sequence-for-job-ids"></a>Työtunnusten yhdistetty numerosarja

[!include [banner](../includes/banner.md)]

Tämä ominaisuus tarjoaa yhden yhdistetyn numerosarjan, joka luo työn tunnukset tuotannon hallinnassa, valmistuksen suorittamisen sekä aika- ja läsnäolomoduulissa. Aiemmin voit valita kullekin moduulille eri numerosarjan, mikä saattaa aiheuttaa ristiriidan työtunnuksissa, jos vähintään kaksi näistä sarjoista käyttää samaa muotoa. Tällainen ristiriita voi aiheuttaa tietojen vaurioitumista.

## <a name="turn-on-this-feature-for-your-system"></a>Tämän ominaisuuden ottaminen käyttöön järjestelmällesi

Jos järjestelmäsi ei vielä sisällä tässä aiheessa kuvattua ominaisuutta, avaa [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja ota *Työtunnusten yhdistetty numerosarja* -ominaisuus käyttöön.

## <a name="set-up-the-unified-number-sequence-for-job-ids"></a>Määritä työtunnusten yhdistetty numerosarja

Kun tämä ominaisuus on käytössä, tuotannonohjauksen, valmistuksen suorittamisen ja aika- ja läsnäolomoduulien parametrisivuilla olevat **Työtunnus**- numerosarjan asetukset vanhentuvat ja uusi **Yhdistetty työtunnus** -kenttä lisätään. Kaikki kolme moduulia jakavat **Yhdistetty työtunnus** -arvon, mikä varmistaa, että kaikissa moduuleissa viitataan samaan numerosarjaan. Tämän vuoksi työtunnukset ovat yksilöllisiä kaikissa kolmessa moduulissa, eikä ristiriitoja tule koskaan.

Määritä työtunnusten yhdistetty numerosarja seuraavasti:

1. Ota toiminto käyttöön edellisessä osassa kuvatulla tavalla.
1. Määritä yhdistettyjä työtunnuksia varten käytettävä numerosarja tai luo uusi numerosarja. Lisätietoja on kohdassa [Numerosarjojen yleiskatsaus](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).
1. Siirry **Tuotannonhallinnan parametrit**-, **Tuotannon suoritusparametrit**- tai **Aika ja läsnäolo -parametrit** -sivulle. Valinnalla ei ole merkitystä, sillä kun teet tämän asetuksen jollain sivulla, kaikki muut sivut päivittyvät automaattisesti.
1. Avaa valittujen parametrien sivun **Numerosarjat**-välilehti.
1. Määritä aiemmin määritetty **Numerosarjakoodi** ruudukon **Yhdistetty työtunnus** -riville.
