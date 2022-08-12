---
title: Ratkaisujen käyttäjien osaamistasoon liittyvien ongelmien vianmääritys
description: Tässä artikkelissa on vianmääritys tietoja, joiden avulla voit korjata ratkaisutietoisuuteen liittyviä ongelmia.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 6866956efcc76a7da6c3aa5fb36058de78d5472e
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111295"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>Ratkaisujen käyttäjien osaamistasoon liittyvien ongelmien vianmääritys

[!include [banner](../../includes/banner.md)]





Tässä artikkelissa on vianmääritystietoja kaksoiskirjoituksen integroinnista talous- ja toimintosovellusten sekä Dataversen välillä. Erityisesti se tarjoaa tietoja, joiden avulla voit korjata ratkaisutietoisuuteen liittyviä ongelmia.

> [!IMPORTANT]
> Jotkin tämän artikkelin osoitteet saattavat edellyttää joko järjestelmänvalvojan roolia tai Microsoft Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia. Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tunnistetietoja.

## <a name="error-on-the-dual-write-page"></a>Virhe kaksoiskirjoitussivulla

**Kaksoiskirjoitussivulla** näyttöön saattaa tulla seuraavan kaltainen virhesanoma:

*Yksikköä, jonka nimi on msdyn\_dualwriteentitymap' with namemapping='Logical', ei löytynyt kohteesta MetadataCache.*

Voit korjata ongelman varmistamalla, että kaksoiskirjoitusydinratkaisu on asennettu Dataverse -järjestelmään. Kaksoiskirjoitusydinratkaisu on ratkaisutietoisuuden edellytys.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
