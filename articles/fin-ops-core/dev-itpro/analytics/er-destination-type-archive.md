---
title: ER-kohteen arkistotyyppi
description: Tässä ohjeaiheessa annetaan tietoja siitä, miten kullekin lähteviä asiakirjoja luomaan määritetty sähköisen raportoinnin (ER) muodon KANSIO- tai TIEDOSTO-komponentin arkistokohde määritetään.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8797a68507a5116c6adbf1f2d805838fa507958c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745582"
---
# <a name="archive-destination"></a>Arkistokohde

[!include [banner](../includes/banner.md)]

Voit määrittää arkistokohteen kullekin lähteviä asiakirjoja luomaan määritetylle sähköisen raportoinnin (ER) muodon KANSIO- tai TIEDOSTO-komponentille. Luotu asiakirja tallennetaan ER-työluettelon tietueen liitteenä kohdeasetuksen perusteella.

Voit lähettää tällä asetuksella luodun tulosteen Microsoft SharePoint -kansion tai Microsoft Azuren tallennustilaan. Lähetä tuloste valitun asiakirjatyypin mukaan määritettyyn kohteeseen valitsemalla **Käytössä**-asetukseksi **Kyllä**. Valittavana on vain asiakirjatyyppejä, joiden ryhmäksi on valittu **Tiedosto**. Asiakirjojen [tyypit](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) määritetään valitsemalla **Organisaation hallinta** \> **Tiedoston hallinta** \> **Tiedostotyypit**. ER-kohteiden määritys on sama kuin tiedostonhallintajärjestelmän määritys.

[![Tiedostotyypit-sivu](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)

Sijainti määrittää, mihin tiedosto tallennetaan. Kun **Arkisto**-kohde on otettu käyttöön, tulokset voidaan tallentaa työarkistoon. Voit tarkastella tuloksia kohteessa **Organisaation hallinta** \> **Sähköinen raportointi** \> **Sähköisen raportoinnin arkistoidut työt**.

> [!NOTE]
> Valitse työarkiston tiedostotyyppi kohdassa **Organisaation hallinta** \> **Työtilat** \> **Sähköinen raportointi** \> **Sähköisen raportoinnin parametrit**. Lisätietoja on kohdassa [Sähköisen raportoinnin (ER) kehyksen määrittäminen](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup)

## <a name="sharepoint"></a>SharePoint

Voit tallentaa tiedoston määritettyyn SharePoint-kansioon. SharePoint-oletuspalvelimen määritetään valitsemalla **Organisaation hallinto** \> **Tiedoston hallinta** \> **Tiedostonhallintaparametrit**. Määritä SharePoint-kansio **SharePoint**-välilehdessä. Tämän jälkeen voit valita sen kansioksi, johon ER-tuloste tallennetaan. **SharePoint**-sijainnin on oltava valittuna tässä asiakirjatyypissä.

[![SharePoint-kansion valitseminen](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)

## <a name="azure-storage"></a>Azuren tallennustila

Kun asiakirjatyypin sijainniksi on määritetty **Azure-tallennustila**, voit tallentaa tiedoston Azuren tallennustilaan.

## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisen raportoinnin (ER) yleiskatsaus](general-electronic-reporting.md)
- [Sähköisen raportoinnin (ER) kohteet](electronic-reporting-destinations.md)
- [Asiakirjanhallinnan määrittäminen](../../fin-ops/organization-administration/configure-document-management.md)
