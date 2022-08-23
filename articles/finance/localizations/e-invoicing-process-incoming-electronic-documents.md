---
title: Saapuvien sähköisten tiedostojen käsitteleminen
description: Tämä artikkeli esittelee yleiskatsauksen saapuvien sähköisten asiakirjojen käsittelystä.
author: gionoder
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 554bc8fde3b2135eb878d885541c76ecd6d66493
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277298"
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
