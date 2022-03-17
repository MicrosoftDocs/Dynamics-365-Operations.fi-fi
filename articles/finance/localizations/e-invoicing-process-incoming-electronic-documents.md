---
title: Saapuvien sähköisten tiedostojen käsitteleminen
description: Tämä aihe esittelee yleiskatsauksen saapuvien sähköisten asiakirjojen käsittelystä.
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
ms.openlocfilehash: 9701367e1ba1f9dbd1e53deb863c10af4213a359
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371609"
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
