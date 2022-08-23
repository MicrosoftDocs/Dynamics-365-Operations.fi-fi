---
title: Logon lisääminen
description: Tässä artikkelissa kerrotaan, miten logo lisätään sivustollesi Microsoft Dynamics 365 Commerce -sovelluksessa.
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 4bd47907791edfd0ab81282bd1e465ac54172cdf
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278094"
---
# <a name="add-a-logo"></a>Logon lisääminen

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan, miten logo lisätään sivustollesi Microsoft Dynamics 365 Commerce -sovelluksessa.

Kun rakennat sivustoasi, yksi ensimmäisistä asioista, jonka luultavasti teet, on lisätä yrityksesi tai brändin logo sivuston otsikkoon. Dynamics 365 Commerce -online-moduulikirjasto tarjoaa moduulin, joka tekee tästä tehtävästä helppoa.

Voit lisätä logon suoraan malliin, asetteluun tai sivulle. Tällä tavoin voit helposti muuttaa tietyillä sivuilla tai sivuryhmillä näkyvää logoa. Tämä artikkeli kattaa kuitenkin yleisimmät skenaariot, joissa lisäät logon otsikon osioihin, joita voidaan käyttää uudelleen kaikilla sivustosi sivuilla.

## <a name="prerequisites"></a>Edellytykset

Ennen kuin voit lisätä logon sivustosi kaikille sivuille, sinun on suoritettava nämä tehtävät.

1. Lataa logo mediakirjastoon.
1. Luo otsikko-osa. Lisätietoja osien luomisesta ja käyttämisestä on kohdassa [osien käyttäminen](work-with-fragments.md).
1. Sisällytä otsikon osa malliin, jota sivustosi sivut käyttävät asettelu- ja moduulivaihtoehtoihin. Lisätietoja malleista on osiossa [Mallien avulla työskentely](work-with-templates.md).

## <a name="add-a-logo-to-a-header-fragment"></a>Logon lisääminen otsikko-osaan

Jos haluat lisätä logon sivustosi otsikko-osaan, toimi seuraavasti.

1. Valitse vasemmanpuoleisessa siirtymisruudussa **Osat**.
1. Valitse aiemmin luomasi otsikon osa ja valitse sitten **Muokkaa**.
1. Laajenna otsikkomoduuli.
1. Anna logon kuva ja linkki otsikkomoduulin ominaisuusruudussa. 
1. Tallenna otsikko-osa, lopeta sen muokkaus ja julkaise se.

Kun olet julkaissut päivitetyn otsikon osan, kaikki ylätunnisteosan sisältävää mallia käyttävät sivuston sivut näyttävät logon.

## <a name="additional-resources"></a>Lisäresurssit

[Sivuston teeman valitseminen](select-site-theme.md)

[CSS-ohitustiedostojen parissa työskentely](css-override-files.md)

[Favicon-kuvakkeen lisääminen](add-favicon.md)

[Copyright-ilmoituksen lisääminen](add-copyright-notice.md)

[Kielten lisääminen sivustoon](add-languages-to-site.md)

[Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
