---
title: Määritä cross-kurssi
description: Tässä ohjeaiheessa on tietoja Microsoft Dynamics 365 Financen ristikursseista.
author: abruer
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 146794557a3a6ba1801598fe6b814e209d9f5fc6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177600"
---
# <a name="specify-the-cross-rate"></a>Määritä cross-kurssi

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kuvataan ristikurssin tarkoitus ja kuinka ristikurssi määritetään, kun täsmäytät maksun laskun kanssa. Käytä ristikurssia, kun kaikki seuraavat kriteerit täyttyvät: 
-   Selvität maksua laskun kanssa. 
-   Maksurivi ja laskurivi käyttävät eri valuuttoja. 
-   Kumpikaan valuutta ei ole kirjanpitovaluuttaa. 

Ristikursseja ei käytetä laskettaessa maksutapahtuman valuutan muuntamista maksun kirjanpitovaluuttaan. Sen sijaan vaihtokurssitaulusta noudetaan vaihtokurssit, joilla lasketaan maksutapahtuman valuuttasumman ja maksun kirjanpitovaluuttasumman arvo. 

Esimerkiksi kirjanpitovaluutta on USD, laskutusvaluutta on CAD ja maksuvaluutta on EUR. Ristikurssin avulla voit kirjoittaa vaihtokurssin, jonka avulla voit muuntaa suoraan Kanadan dollarit euroiksi, eikä sinun tarvitse muuntaa Yhdysvaltain dollareiden kautta. Kun valitset laskun ja ensisijaisen maksun, voit syöttää ristikurssin laskuriville. Ristikurssi on näiden tapahtumien valuuttojen vaihtokurssi selvityspäivänä.

1.  Valitse jokin seuraavista sivuista:
- **Myyntireskontra > Yleinen > Asiakkaat > Kaikki asiakkaat.** 
- **Ostoreskontra > Yleiset > Toimittajat > Kaikki toimittajat.** 
- **Hankinta > Yleinen > Toimittajat > Kaikki toimittajat**
2.  Valitse asiakas tai toimittaja, jonka avoimia tapahtumia selvität. 
3.  Jos kyse on asiakkaasta, valitse **Kaikki asiakkaat** -luettelosivulla **Perintä > Tilitä avoimet tapahtumat**. Jos kyse on toimittajasta, valitse **Kaikki toimittajat** -luettelosivulla **Lasku > Tilitä avoimet tapahtumat**. 
4.  Valitse tapahtuma, joka on ensisijainen maksu, ja valitse sitten **Merkitse maksu**. **Merkitse**-sarakkeen valintaruutu on valittu ja tietokuvake näkyy **Ensisijainen maksu** -sarakkeessa. 
5.  Anna **Ristikurssi**-kentässä laskun valuutan ja maksun valuutan vaihtokurssi selvityspäivänä. 
