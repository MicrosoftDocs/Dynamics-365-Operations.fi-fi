---
title: Yhdelle kuitille tulostetaan vain yksi etiketti useille työotsikoille
description: Yhdelle kuitille tulostetaan vain yksi etiketti useille työotsikoille.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8e11dc918eb3c9085018d15b43819522cc8bebe3
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026472"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a>Yhdelle kuitille tulostetaan vain yksi etiketti useille työotsikoille

Tietopankin numero: 4614667

## <a name="symptoms"></a>Oireet

Samalle kohderekisterikilvelle luodaan useita työotsikkoja, jotka ovat osa yhtä varastosovelluksen vastaanottotapahtumaa. Kun tuote vastaanotetaan, tulostetaan kuitenkin vain yksi rekisterikilven etiketti.

## <a name="resolution"></a>Ratkaisu

Järjestelmä käyttäytyy suunnitellulla tavalla.

Nykyisessä suunnittelussa luodaan aina vain yksi rekisterikilven etiketti, riippumatta siitä, kuinka monta työotsikon ja työrivin yhdistelmää on olemassa. Luotu otsikko sisältää vain yhden yhdistelmän tiedot.

Voit ratkaista tämän ongelman varmistamalla, että työotsikon luonti on aina yhdistetty vain yhteen kohderekisterikilpeen.
