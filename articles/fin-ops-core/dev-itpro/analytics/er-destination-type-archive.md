---
title: ER-kohteen arkistotyyppi
description: Tässä aiheessa on tietoja kunkin sähköisen raportoinnin (ER) muodon KANSIO- tai TIEDOSTO-osan arkistokohteen määrittämisestä.
author: NickSelin
ms.date: 11/30/2020
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
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 18c662fee0cedaa55f63ffeb25b0d61ee7baffda
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753525"
---
# <a name="archive-er-destination-type"></a>ER-kohteen arkistotyyppi

[!include [banner](../includes/banner.md)]

Voit määrittää arkistokohteen kullekin lähteviä asiakirjoja luomaan määritetylle sähköisen raportoinnin (ER) muodon **Kansio**- tai **Tiedosto**-komponentille. Luotu asiakirja tallennetaan ER-työluettelon tietueen liitteenä kohdeasetuksen perusteella. Voit tarkastella tuloksia kohteessa **Organisaation hallinta** \> **Sähköinen raportointi** \> **Sähköisen raportoinnin työt**.

Voit lähettää tällä asetuksella luodun tulosteen Microsoft SharePoint -kansion tai Microsoft Azuren tallennustilaan. Lähetä tuloste valitun asiakirjatyypin mukaan määritettyyn kohteeseen valitsemalla **Käytössä**-asetukseksi **Kyllä**. Valittavana on vain asiakirjatyyppejä, joiden ryhmäksi on valittu **Tiedosto**. Asiakirjojen [tyypit](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) määritetään valitsemalla **Organisaation hallinta** \> **Tiedoston hallinta** \> **Tiedostotyypit**. ER-kohteiden määritys on sama kuin tiedostonhallintajärjestelmän määritys.

[![Tiedostotyypit-sivu](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)

Sijainti määrittää, mihin tiedosto tallennetaan. Kun **Arkisto**-kohde on otettu käyttöön, tulokset voidaan tallentaa työarkistoon. Voit tarkastella tuloksia kohteessa **Organisaation hallinta** \> **Sähköinen raportointi** \> **Sähköisen raportoinnin arkistoidut työt**.

> [!NOTE]
> Valitse työarkiston tiedostotyyppi kohdassa **Organisaation hallinta** \> **Työtilat** \> **Sähköinen raportointi** \> **Sähköisen raportoinnin parametrit**. Lisätietoja on kohdassa [Sähköisen raportoinnin (ER) kehyksen määrittäminen](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).

## <a name="sharepoint"></a>SharePoint

Voit tallentaa tiedoston määritettyyn SharePoint-kansioon. SharePoint-oletuspalvelimen määritetään valitsemalla **Organisaation hallinto** \> **Tiedoston hallinta** \> **Tiedostonhallintaparametrit**. Määritä SharePoint-kansio **SharePoint**-välilehdessä. Tämän jälkeen voit valita sen kansioksi, johon ER-tuloste tallennetaan. **SharePoint**-sijainnin on oltava valittuna tässä asiakirjatyypissä.

[![SharePoint-kansion valitseminen](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)

## <a name="azure-storage"></a>Azuren tallennustila

Kun asiakirjatyypin sijainniksi on määritetty **Azure-tallennustila**, voit tallentaa tiedoston Azuren tallennustilaan.

> [!NOTE] 
> ER-kehys tallentaa tiedostot pysyvästi Azure Blob -tallennustilaan toisin kuin tietojenhallintakehys, jolla on seitsemän päivän säilytyskäytäntö asiakirjoille, jotka on käsiteltävä. Lisätietoja on kohdissa [Ohjelmointirajapinta viestin tilan hakemiselle](../data-entities/recurring-integrations.md#api-for-getting-message-status) ja [Tilan tarkistuksen ohjelmointirajapinta](../data-entities/data-management-api.md#status-check-api). ER:ään liittyvät tiedostot tallennetaan Azure Blob -tallennustilaan sovellustaulun tietueiden liitteinä niin pitkäksi aikaa kuin on tarpeellista. Yksittäinen tiedosto poistetaan Azure Blob -tallennustilasta yhdessä sen sovellustaulun tietueen kanssa, johon tiedosto on liitetty.

## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisen raportoinnin (ER) yleiskatsaus](general-electronic-reporting.md)
- [Sähköisen raportoinnin (ER) kohteet](electronic-reporting-destinations.md)
- [Asiakirjanhallinnan määrittäminen](../../fin-ops/organization-administration/configure-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]