---
title: Ennustemallin parantaminen (esiversio)
description: Tässä ohjeaiheessa kuvataan toimintoja, joiden avulla voit parantaa ennustemallien suorituskykyä.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 184a1cb5d3851e26b41340b711c51ef38e06eb53
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186639"
---
# <a name="improve-the-prediction-model-preview"></a>Ennustemallin parantaminen (esiversio)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä ohjeaiheessa kuvataan toimintoja, joiden avulla voit parantaa ennustemallien suorituskykyä. Aloita mallin parantaminen **Asiakkaan maksuennusteet** -työtilassa Microsoft Dynamics 365 Financessa. Parannusvaiheet tehdään AI Builderissa.

## <a name="select-historical-outcomes"></a>Aiempien tulosten valitseminen

Valitse vähintään yksi kolmesta laskun mahdollisesta lopputuloksesta: **Ajoissa**, **Myöhässä** ja **Erittäin paljon myöhässä**. Valitse kaikki kolme tulosta. Jos poistat jonkin tuloksen valinnan, laskut suodatetaan pois koulutusprosessista ja ennusteen tarkkuus vähenee.

[![Tulosten vahvistaminen](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)

Jos organisaatio vaatii vain kaksi tulosta, muuta **Myöhässä**- ja **Erittäin paljon myöhässä** -kohtien rajoiksi 0 (nolla) päivää. Näin voit tehokkaasti kutistaa ennusteen binaariseen **Ajoissa**- tai **Myöhässä**-tilaan.

## <a name="select-fields"></a>Valitse kentät

Kun valitset malliin sisällytettävät kentät, huomaa, että luettelossa ovat kaikki Azure Data Lakeen yhdistettyjen tietojen Microsoft Dataverse -taulukon käytettävissä olevat kentät. Joitakin näistä kentistä **ei** tule valita. Kentät, joita ei tule valita, kuuluvat yhteen kolmesta luokasta:

- Kenttä on pakollinen Dataverse-taulukolle, mutta Data Lakessa ei ole sen varmuuskopioita.
- Kenttä on tunnus, eikä sen vuoksi ole järkevää käyttää sitä koneoppimistoiminnossa.
- Kenttä edustaa tietoja, jotka eivät ole käytettävissä ennusteen aikana.

Seuraavissa osissa näkyvät laskussa ja asiakasentiteeteissä käytettävissä olevat kentät ja kentät, joita **ei** tule valita koulutukseen. Luokka, joka on määritetty kullekin näistä kentistä, viittaa edellä olevan luettelon luokkiin.
 
### <a name="invoice-dataverse-table"></a>Laskun Dataverse-taulu

Seuraavassa kuvassa ovat laskutaulukolle käytettävissä olevat kentät.

[![Laskutaulukon käytettävissä olevat kentät](./media/available-fields.png)](./media/available-fields.png)

Seuraavia kenttiä ei saa valita koulutukselle:

- **Laskutili** (luokka 2)
- **On suljettu** (luokka 3) – Tämän kentän avulla suodatetaan laskut koulutusta (suljettu) ja ennustetta (ei suljettu) varten.
- **Nimi** (luokka 1)
- **Lähteen tunnus** (luokka 2)
- **Lähdetietue** (luokka 2)
- **Lähdetaulukko** (luokka 2)

### <a name="customer-dataverse-table"></a>Asiakkaan Dataverse-taulu

Seuraavassa kuvassa ovat asiakastaulukolle käytettävissä olevat kentät.

[![Asiakastaulukon käytettävissä olevat kentät](./media/related-entities.png)](./media/related-entities.png)

Seuraavaa kenttää ei saa valita koulutukselle:

- **Rivin yksilöivä avain** (luokka 2)

## <a name="filters"></a>Suodattimet

Suodattimet eivät tällä hetkellä tue asiakkaan maksuennusteen skenaariota. Valitse tämän vuoksi **Ohita tämä vaihe** ja jatka Yhteenveto-sivulle.

[![Kohdistusmalli ja suodattimet](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
