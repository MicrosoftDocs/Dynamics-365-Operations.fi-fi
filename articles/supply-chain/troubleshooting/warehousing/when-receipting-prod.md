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
ms.openlocfilehash: cf307964a07c2b69eb5e4ef2cf9dc094482736d0970e333e84f674c9be6331c7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740524"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a>Yhdelle kuitille tulostetaan vain yksi etiketti useille työotsikoille

Tietopankin numero: 4614667

## <a name="symptoms"></a>Oireet

Samalle kohderekisterikilvelle luodaan useita työotsikkoja, jotka ovat osa yhtä varastosovelluksen vastaanottotapahtumaa. Kun tuote vastaanotetaan, tulostetaan kuitenkin vain yksi rekisterikilven etiketti.

## <a name="resolution"></a>Ratkaisu

Järjestelmä käyttäytyy suunnitellulla tavalla.

Nykyisessä suunnittelussa luodaan aina vain yksi rekisterikilven etiketti, riippumatta siitä, kuinka monta työotsikon ja työrivin yhdistelmää on olemassa. Luotu otsikko sisältää vain yhden yhdistelmän tiedot.

Voit ratkaista tämän ongelman varmistamalla, että työotsikon luonti on aina yhdistetty vain yhteen kohderekisterikilpeen.
