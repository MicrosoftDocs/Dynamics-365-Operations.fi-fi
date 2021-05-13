---
title: Luo tuotenumeroiden nimikkeistö määritetyille tuotevarianteille
description: Tässä aiheessa kuvataan, miten tuotenumeroiden nimikkeistö määritetään konfiguroiduille tuotevarianteille ja miten se voidaan liittää konfiguroitavaan päätuotteeseen.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ea30dc107213b1a2c6b2a109188066a6ea82159
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921008"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a>Luo tuotenumeroiden nimikkeistö määritetyille tuotevarianteille

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kuvataan, miten tuotenumeroiden nimikkeistö määritetään konfiguroiduille tuotevarianteille ja miten se voidaan liittää konfiguroitavaan päätuotteeseen. Tässä ohjeaiheessa kerrotaan myös, miten tuotteen kokoonpanomallin osan konfiguraationimikkeistö rakennetaan. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Uusi tuotenumeroiden nimikkeistö on määritetty päätuotteelle D0004. Tuotesuunnittelija tekee yleensä tämän tehtävän.

## <a name="create-a-product-number-nomenclature"></a>Tuotenumeroiden nimikkeistön luominen

1. Valitse **Tuotetietojen hallinta \> Asetukset \> Tuotenimikkeistö**.
1. Valitse **Uusi**.
1. Kirjoita arvo **Nimi**-kenttään.
1. Kirjoita **Kuvaus**-kenttään arvo.
1. Valitse **Lisää**.
1. Valitse **Päätuotteen numero**.
1. Valitse **Lisää**.
1. Valitse **Tekstivakio**.
1. Merkitse valittu rivi luettelossa.
1. Kirjoita arvo **Teksti**-kenttään.
1. Valitse **Lisää**.
1. Valitse **Määritys**.
1. Sulje sivu.

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a>Tuotenumeroiden nimikkeistön määrittäminen päätuotteelle

1. Valitse **Tuotetietojen hallinta \> Tuotteet \> Päätuotteet**.
1. Käytä pikasuodatinta tietueiden etsimiseen. Voit esimerkiksi suodattaa **Tuotenumero**-kenttää arvolla D.
1. Valitse luettelossa valitulla rivillä oleva linkki.
1. Valitse **Muokkaa**.
1. Valitse **Käytä nimikkeistöä** -kentässä *Kyllä*.
1. Syötä tai valitse arvo **Tuotevariantin numeron nimikkeistö** -kentässä.
1. Sulje sivu.
1. Sulje sivu.

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a>Nimikkeistön luominen tuotemääritysmallin osalle

1. Valitse **Tuotetietojen hallinta \> Tuotteet \> Tuotekonfiguraation mallit**.
1. Etsi haluamasi tietue luettelosta ja valitse se.
1. Valitse luettelossa valitulla rivillä oleva linkki.
1. Valitse **Muokkaa**.
1. Valitse **Käytä konfiguraationimikkeistöä** -kentässä *Kyllä*.
1. Valitse **Lisää**.
1. Valitse **Määritteen arvo**.
1. Merkitse valittu rivi luettelossa.
1. Syötä tai valitse arvo kentässä **Määrite**.
1. Valitse **Lisää**.
1. Valitse **Tekstivakio**.
1. Merkitse valittu rivi luettelossa.
1. Kirjoita arvo **Teksti**-kenttään.
1. Valitse **Lisää**.
1. Valitse **Määritteen arvo**.
1. Merkitse valittu rivi luettelossa.
1. Syötä tai valitse arvo kentässä **Määrite**.
1. Valitse **Lisää**.
1. Valitse **Tekstivakio**.
1. Merkitse valittu rivi luettelossa.
1. Kirjoita arvo **Teksti**-kenttään.
1. Valitse **Lisää**.
1. Valitse **Määritteen arvo**.
1. Merkitse valittu rivi luettelossa.
1. Syötä tai valitse arvo kentässä **Määrite**.
1. Valitse **Lisää**.
1. Valitse **Tekstivakio**.
1. Merkitse valittu rivi luettelossa.
1. Kirjoita arvo **Teksti**-kenttään.
1. Valitse **Lisää**.
1. Valitse **Määritteen arvo**.
1. Merkitse valittu rivi luettelossa.
1. Syötä tai valitse arvo kentässä **Määrite**.
1. Valitse **Lisää**.
1. Valitse **Tekstivakio**.
1. Merkitse valittu rivi luettelossa.
1. Kirjoita arvo **Teksti**-kenttään.
1. Valitse **Lisää**.
1. Valitse **Numerosarjan arvo**.
1. Merkitse valittu rivi luettelossa.
1. Anna tai valitse **Numerosarja**-kentässä arvo.
1. Sulje sivu.
1. Sulje sivu.
1. Sulje sivu.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]