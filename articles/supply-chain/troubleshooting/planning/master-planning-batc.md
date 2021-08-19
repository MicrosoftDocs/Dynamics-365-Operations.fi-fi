---
title: Et voi suodattaa pääsuunnittelunimikkeitä niihin liittyvien kattavuusryhmän arvojen mukaan
description: Et voi suodattaa pääsuunnittelunimikkeitä niihin liittyvien kattavuusryhmän arvojen mukaan.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 9750a73f0962179512c5e21a614a276c313ff975b7494f31589ca936886ecf6e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781390"
---
# <a name="you-cant-filter-master-planning-items-by-their-related-coverage-group-values"></a>Et voi suodattaa pääsuunnittelunimikkeitä niihin liittyvien kattavuusryhmän arvojen mukaan

Tietopankin numero: 4612572

## <a name="symptoms"></a>Oireet

Haluat suodattaa kohteet, jotka sisällytetään pääsuunnittelun erätyöhön, aihealuetaulukon liittyvien tietueiden arvojen perusteella. (Haluat esimerkiksi suodattaa nimikkeet niiden **Toimittaja**- ja/tai **Kattavuusryhmä**-arvon mukaan). Erätyön suodatinasetuksissa voit luoda liitoksen **Nimike**-taulusta **Nimikkeen kattavuus** -tauluun ja määrittää sitten kyselyn nimikekattavuustaulun kenttien arvot. Kun nämä asetukset on tehty, järjestelmä luo edelleen suunniteltuja tilauksia koko nimikkeen kattavuutta varten, ei vain niitä nimikkeitä varten, jotka vastaavat nimikkeen kattavuustaulun määritettyjä kenttäarvoja.

## <a name="resolution"></a>Ratkaisu

Erätyön suodatin voi suodattaa vain nimikkeiden perusteella. Vaikka liitoksen voikin lisätä **nimikkeen kattavuustauluun**, tätä taulua vasten muodostetut suodatusasetukset eivät vaikuta kyselyn tulokseen. Ajon aikana järjestelmä suunnittelee kaikkia kattavuusryhmiä ja kaikkia suodatetun nimikkeiden muunnelmia. Kun nimike on jo sisällytetty ajoon, nimikkeen suodattimeen sisältyvät kattavuusryhmät eivät vaikuta suunnittelun tulosteessa.
