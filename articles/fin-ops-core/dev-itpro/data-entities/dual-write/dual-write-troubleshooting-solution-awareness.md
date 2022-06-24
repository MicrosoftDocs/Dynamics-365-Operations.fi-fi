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
ms.openlocfilehash: c280eef995664c640e382817dda9d6e1cde154c6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871492"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>Ratkaisujen käyttäjien osaamistasoon liittyvien ongelmien vianmääritys

[!include [banner](../../includes/banner.md)]





Tässä artikkelissa on vianetsintätietoja kaksoiskirjoituksen integroinnista talous- ja toimintosovellusten ja Dataversen välillä. Erityisesti se tarjoaa tietoja, joiden avulla voit korjata ratkaisutietoisuuteen liittyviä ongelmia.

> [!IMPORTANT]
> Jotkin tämän artikkelin osoitteet saattavat edellyttää joko järjestelmänvalvojan roolia tai Microsoft Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia. Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tunnistetietoja.

## <a name="error-on-the-dual-write-page"></a>Virhe kaksoiskirjoitussivulla

**Kaksoiskirjoitussivulla** näyttöön saattaa tulla seuraavan kaltainen virhesanoma:

*Yksikköä, jonka nimi on msdyn\_dualwriteentitymap' with namemapping='Logical', ei löytynyt kohteesta MetadataCache.*

Voit korjata ongelman varmistamalla, että kaksoiskirjoitusydinratkaisu on asennettu Dataverse -järjestelmään. Kaksoiskirjoitusydinratkaisu on ratkaisutietoisuuden edellytys.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]