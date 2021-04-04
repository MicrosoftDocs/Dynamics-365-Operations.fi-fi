---
title: Tulostimen ER-kohteen tyyppi
description: Tässä aiheessa käsitellään tulostinkohteen määrittämistä sähköisen raportoinnin (ER) muodon KANSIO- tai TIEDOSTO-osalla.
author: NickSelin
manager: AnnBe
ms.date: 02/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 19613d9dfba21d591d96a2df45bedb80c043b3a7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561947"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a>Tulostinkohde

[!include [banner](../includes/banner.md)]

Voit lähettää luodun asiakirjan suoraan verkkotulostimeen suoraa tulostusta varten.

## <a name="prerequisites"></a>Edellytykset

Ennen aloittamista sinun on asennettava ja määritettävä asiakirjan reititysagentti ja rekisteröitävä sitten verkkotulostimet. Lisätietoja on kohdassa [Verkkotulostuksen käyttöönotto asentamalla asiakirjan reititysagentti](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent)

## <a name="make-the-printer-destination-available"></a>Tulostinkohteen käytettäväksi asettaminen

Jos haluat, että **Tulostin**-kohde on käytettävissä Microsoftin Dynamics 365 Financen kulloisessakin esiintymässä, siirry **Ominaisuuksien hallinta** -työtilaan ja ota seuraavat ominaisuudet käyttöön tässä järjestyksessä:

1. Muunna sähköisen raportoinnin lähtevät asiakirjat Microsoft Office -muodoista PDF-muotoon
2. Asiakirjareitityksen agentti lähtevien asiakirjojen sähköisen raportoinnin kohteena

[![ER-tulostinkohteen toiminnon käyttöönotto ominaisuuksien hallinnassa](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>Soveltuvuus

**Tulostin**-kohde voidaan määrittää vain tiedostokomponenteille, joita käytetään tulosteen luomiseen joko tulostettavassa PDF-muodossa (PDF Mergerin tai PDF-tiedoston muotoelementit) tai Microsoft Office Excel/Word -muodossa (Excel-tiedosto). Kun tuloste luodaan PDF-muodossa, se lähetetään tulostimeen. Kun tuloste luodaan Microsoft Office -muodossa, se muunnetaan automaattisesti PDF-muotoon ja lähetetään sitten tulostimeen.

### <a name="limitations"></a>Rajoitukset

**Tulostin**-kohdetta käytetään vain pilvikäyttöönotoissa.

### <a name="use-the-printer-destination"></a>Käytä tulostinkohdetta

1. Määritä **Käytössä** -asetuksen arvoksi **Kyllä**, jos haluat lähettää luodun tiedoston tulostimeen.
2. Valitse **Tulostimen nimi** -kentässä asianmukainen verkkotulostin.
3. Aseta **Tallenna tulostusarkistoon?** -asetuksen arvoksi **Kyllä**, jos haluat tallentaa luodun tulosteen tulostusarkistoon, jotta se voidaan tulostaa myös myöhemmin. Arkistoitu tuloste on myöhemmin käytettävissä kohdassa **Organisaation hallinta** \> **Kyselyt ja raportit** \> **Raporttiarkisto**.

[![Tulostinkohteen käyttö](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> **Muunna PDF-muotoon** -asetuksen ei tarvitse olla käytössä, kun määrität **Tulostin**-kohteen. PDF-muunnos tulostusta varten tapahtuu, vaikka asetus ei olisi käytössä.

Jos haluat käyttää tiettyä [sivun suuntaa](electronic-reporting-destinations.md#SelectPdfPageOrientation), kun tulostat lähtevän asiakirjan Excel-muodossa, **Muunna PDF-muotoon** -asetus on otettava käyttöön. Kun määrität **Muunna PDF:ksi** -asetukseksi **Kyllä**, **Sivun suunta** -kenttä on käytettävissä. **Sivun suunta** -kentästä voit valita haluamasi sivun suunnan.

## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisen raportoinnin (ER) yleiskatsaus](general-electronic-reporting.md)
- [Sähköisen raportoinnin (ER) kohteet](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
