---
title: Saapuvien sähköisten tiedostojen käsitteleminen
description: Tämä artikkeli esittelee yleiskatsauksen saapuvien sähköisten asiakirjojen käsittelystä.
author: dkalyuzh
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: dec4c16c8ba9f0ba55f30f3944eff172cf9db724
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910005"
---
# <a name="processing-of-incoming-electronic-documents"></a>Saapuvien sähköisten tiedostojen käsitteleminen

[!include [banner](../includes/banner.md)]

Saapuvat sähköiset tiedostot, kuten sähköiset toimittajalaskut, voidaan tuoda ja käsitellä kahdella tavalla:

- Tiedostot noudetaan ulkoisista kanavista ja välitetään suoraan liitettyyn sovellukseesi. Siinä muunnetaan lisämuunnoksella ja tuodaan tietokantaan.
- Tiedostot esiprosessoidaan sähköisen laskutuksen palvelussa, jonka jälkeen tiedostot siirretään liitettyyn sovellukseesi.

Sähköinen laskutus tukee saapuville asiakirjoille kahta kanavaa: sähköposti- ja Microsoft SharePoint -kansiot.

Kaksi asetustyyppiä määrittävät, suoritetaanko asiakirjoille esiprosessointi vai siirretäänkö ne suoraan liitettyyn sovellukseesi:

- **Tietokanava** – Järjestelmä siirtää asiakirjan suoraan liitettyyn sovellukseen.
- **Tietokanava ja käsittelyputki** – Voit määrittää muita toimenpiteitä, jotka suoritetaan, ennen kuin tiedosto siirretään liitettyyn sovellukseen.

Lisätietoja saapuvien sähköisten tiedostojen käsittelyn skenaarioiden määrittämisestä eri kanavien osalta on kohdassa [Sähköpostikanavan konfiguroiminen](e-invoicing-configure-email.md) ja [SharePoint-kanavan konfiguroiminen](e-invoicing-configure-sharepoint-channel.md).
