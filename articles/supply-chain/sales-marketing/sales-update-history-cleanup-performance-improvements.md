---
title: Myyntihistorian puhdistuksen suorituskyvyn parannukset
description: Tässä aiheessa kuvataan myyntihistorian puhdistuksen suorituskyvyn parannuksiin liittyvä ominaisuus sekä sen ottaminen käyttöön.
author: myvakalo
ms.date: 10/05/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d4eeee3c1228b278fea07464f35946c295c5aea8
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/25/2021
ms.locfileid: "7679052"
---
# <a name="saleshistorycleanupperformanceimprovements"></a>Myyntihistorian puhdistuksen suorituskyvyn parannukset

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)] <!-- GA with 10.0.24 -->

Kausittainen **Myynnin päivityshistorian poistaminen** -erätyövoi kestää kauan, jos sitä ei suoriteta säännöllisesti ympäristöissä, joissa myyntipäivityksiä on paljon. Näissä tilanteissa *Myyntihistorian puhdistuksen suorituskyvyn parannukset* -ominaisuus voi lyhentää ajon kestoa ja parantaa luotettavuutta.

Ominaisuus parantaa olemassa olevaa puhdistustyötä seuraavilla tavoilla:

- Puhdistus jaetaan eriksi (eräkokoa voi muuttaa mukautuksissa).
- Sitä suoritetaan enintään 2 tuntia (kestoa voi muuttaa mukautuksissa).
- Jos mahdollista, se hyödyntää tietokantaominaisuuksia vähentääkseen lukituksia ja välttää tapahtumataulujen liitoksia puhdistuksen aikana.

Kun ominaisuus on otettu käyttöön, **Myynnin päivityshistorian puhdistus** -erätyö (**Myynti ja markkinointi \> Kausittaiset tehtävät \> Puhdistus \> Myynnin päivityshistorian puhdistus**) suoritetaan kuten ennen, mutta suorituskyky on parempi ja se kestää enintään 2 tuntia. Tämä tarkoittaa, että kaikki tietyn säilytysajan tiedot puhdistaakseen on ehkä suoritettava useita kertoja.

## <a name="turn-on-the-saleshistorycleanupperformanceimprovements-feature"></a>Ota käyttöön Myyntihistorian tyhjennyksen suorituskyvyn parannukset -ominaisuus

Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Myynti ja markkinointi*
- **Ominaisuuden nimi:** *Myyntihistorian tyhjennyksen suorituskyvyn parannukset*
