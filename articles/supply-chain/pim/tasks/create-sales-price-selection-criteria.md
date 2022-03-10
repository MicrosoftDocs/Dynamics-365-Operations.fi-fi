---
title: Luo myyntihinnan valintaperusteet
description: Tässä toimintaohjeessa kuvataan, miten voit luoda myyntihinnan valintaehdon määriteperustaiselle myyntihintamallille.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ed7083f289948033782f74dd9ed1b3c2d2a73aea
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568444"
---
# <a name="create-sales-price-selection-criteria"></a>Luo myyntihinnan valintaperusteet

[!include [banner](../../includes/banner.md)]

Tässä toimintaohjeessa kuvataan, miten voit luoda myyntihinnan valintaehdon määriteperustaiselle myyntihintamallille. Tämän menettelyn suorittaminen edellyttää, että ainakin yksi myyntihintamalli on käytettävissä. Tässä esimerkissä käytetään hintamallia esittelytietojen USMF-yrityksen Kaiutinratkaisu-hintamallissa. Tämän tehtävän suorittaa yleensä tuotepäällikkö.

## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>Uuden ehdon lisääminen vanhalle myyntihintamallille

1. Valitse **Tuotetietojen hallinta \> Tuotteet \> Tuotekonfiguraation mallit**.
1. Valitse luettelosta kaiutinratkaisun tuotemalli, mutta älä valitse mallinimen linkkiä.
1. Valitse toimintoruudussa **Malli**.
1. Valitse **Hintamalliehdot**.
1. Valitse **Uusi**.
1. Syötä **Nimi**-kenttään "Asiakasryhmä 10".
    * Valinnan ehdot tunnistetaan hinnoittelumallin ehdon nimen avulla.  
1. Syötä tai valitse arvo kentässä **Hintamalli**.
1. Valitse **Tilaustyyppi**-kenttään *Myyntitilaus*.
    * Tilauksen tyyppi määrittää tietokannan kentät, jotka ovat saatavilla valintakyselyssä.  
1. Kirjoita päivämäärä **Voimassaolo alkaa** -kenttään.
1. Syötä päivämäärä **Vanhentuu**-kenttään.
1. Valitse **Tallenna**.

## <a name="create-the-query-for-the-selection-criteria"></a>Luo kysely valintaperusteilla

1. Valitse **Muokkaa**.
2. Valitse *Asiakkaat* **Taulukko**-kentässä.
3. Valitse **Kenttä**-kentässä *Asiakasryhmä*.
    * Tässä esimerkissä tiettyä asiakasryhmää valintakriteerinä.  
4. Valitse **Ehto**-kentässä *Asiakasryhmä 10*.
5. Valitse **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]