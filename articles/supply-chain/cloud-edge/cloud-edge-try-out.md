---
title: Kokeile Scale Uniteja jaetussa hybriditopologiassa
description: Tässä artikkelissa on lisätietoja valmistuksen ja varastoinnin hallinnan kuormitusten pilvi- ja reunapalvelujen Scale Unitien kokeilemisesta.
author: perlynne
ms.date: 05/02/2022
ms.topic: article
ms.search.form: ScaleUnitWorkloadsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-03-03
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 5645955109e7a942e617b3b90a27065c2a8fe4a3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893581"
---
# <a name="try-out-scale-units-in-a-distributed-hybrid-topology"></a>Kokeile Scale Uniteja jaetussa hybriditopologiassa

[!include [banner](../includes/banner.md)]

Kokeilu jaetussa hybriditopologiassa on yksinkertaista. Ensimmäisen vaiheen aikana mukautukset on vahvistettava, jotta ne toimivat jaetussa topologiassa. Vaihtoehtoja on kaksi.

## <a name="option-1-evaluate-customizations-in-development-environments"></a>Vaihtoehto 1: Mukautusten arvioiminen kehitysympäristöissä

Ennen kuin aloitat eristysympäristön tuomisen, suosittelemme, että tutustut skaalausyksiköihin kehitysasetuksissa, kuten yhden laatikon ympäristössä (eli tier-1-ympäristössä), jotta voit vahvistaa prosessit, mukautukset ja ratkaisut. Tässä vaiheessa tietoja ja mukautuksia käytetään yksiruutuissa ympäristöissä. Voit suorittaa työt yhdessä ympäristössä, joka voi olla sekä yritystoiminto että skaalausyksikkö. Vaihtoehtoisesti voi olla kaksi kehitysympäristöä, joista toisen roolina on voi olla yritystoiminto ja toisen roolina skaalausyksikkö. Nämä asetukset ovat paras tapa tunnistaa ja korjata ongelmia. Myös viimeisintä [esiversiota](../../fin-ops-core/fin-ops/get-started/one-version.md#how-can-i-get-early-access-to-non-released-platform-updates) voi käyttää tämän vaiheen suorittamiseen.

Ympäristöjen asentamiseen ja ylläpitoon on käytettävä [skaalausyksikön käyttöönottotyökaluja yhden ruudun kehitysympäristöissä](https://github.com/microsoft/SCMScaleUnitDevTools). Näiden työkalujen avulla voit konfiguroida skaalausyksiköt yhdessä tai kahdessa yksiruutuisessa ympäristössä. Työkalut toimitetaan sekä binaarijulkaisuna että lähdekoodina GitHubissa. Tutki projektin wikiä, joka sisältää [vaiheittaiset käyttöoppaat](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide), jotka kuvaavat työkalujen käyttöä. Jos [otat käyttöön reunan skaalausyksiköt mukautetussa laitteistossa paikallisen yritystietojen (LBD) avulla](cloud-edge-edge-scale-units-lbd.md), sinun on noudatettava eri prosessia.

## <a name="option-2-acquire-add-ins-and-deploy-in-your-sandbox-environments"></a>Vaihtoehto 2: Apuohjelmien hankkiminen ja käyttöönotto eristysympäristöissäsi

Jos haluat kokeilla jaettua hybriditopologiaa, sinulla on oltava kaksi eristysympäristöä (tier 2), joista toisessa on tiedot (yritystoiminto) ja toisessa skaalausyksikköä ja jossa on "tyhjät tiedot".

Vähintään yhden pilvipalvelun tai reunan skaalausyksikköön on hankittava lisäosa. Vastaavat projekti- ja ympäristöpaikat myönnetään sitten [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/) -palveluissa, jotta skaalausyksikön ympäristöt voidaan ottaa käyttöön [skaalausyksikön hallintaportaalin](https://aka.ms/SCMSUM) avulla.

Ota yhteys Microsoft-tukeen pyytääksesi, että eristysympäristöt otetaan käyttöön.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
