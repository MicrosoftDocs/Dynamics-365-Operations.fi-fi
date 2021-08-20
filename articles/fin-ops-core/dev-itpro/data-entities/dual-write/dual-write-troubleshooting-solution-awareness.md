---
title: Ratkaisujen käyttäjien osaamistasoon liittyvien ongelmien vianmääritys
description: Tässä ohjeaiheessa on vianmääritys tietoja, joiden avulla voit korjata ratkaisutietoisuuteen liittyviä ongelmia.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: aa5ba0cfb127f20012237774fe948c23731eb56f8680d9fa23309e189683dbf3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736347"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>Ratkaisujen käyttäjien osaamistasoon liittyvien ongelmien vianmääritys

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Tässä artikkelissa on vianetsintätietoja kaksoiskirjoituksen integroinnista Finance and Operations -sovellusten ja Dataversen välillä. Erityisesti se tarjoaa tietoja, joiden avulla voit korjata ratkaisutietoisuuteen liittyviä ongelmia.

> [!IMPORTANT]
> Jotkin tämän ohjeaiheen osoitteet saattavat edellyttää joko järjestelmänvalvojan roolia tai Microsoftin Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia. Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tunnistetietoja.

## <a name="error-on-the-dual-write-page"></a>Virhe kaksoiskirjoitussivulla

**Kaksoiskirjoitussivulla** näyttöön saattaa tulla seuraavan kaltainen virhesanoma:

*Yksikköä, jonka nimi on msdyn\_dualwriteentitymap' with namemapping='Logical', ei löytynyt kohteesta MetadataCache.*

Voit korjata ongelman varmistamalla, että kaksoiskirjoitusydinratkaisu on asennettu Dataverse -järjestelmään. Kaksoiskirjoitusydinratkaisu on ratkaisutietoisuuden edellytys.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]