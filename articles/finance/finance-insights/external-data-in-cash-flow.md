---
title: Ulkoisten tietojen käyttäminen kassavirta ennusteissa (esiversio)
description: Tässä ohjeaiheessa kuvataan määritysvaiheet, jotka on suoritettava, jotta ulkoiset tiedot voidaan syöttää tai tuoda kassavirtaennusteisiin.
author: rcarlson
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 66bdb8bd638859bb4fc5565e3f12a8f671addcff
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186687"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a>Ulkoisten tietojen käyttäminen kassavirta ennusteissa (esiversio)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Ulkoisia tietoja voidaan lisätä tai tuoda kassavirtaennusteisiin. Tässä ohjeaiheessa kuvataan ulkoisten tietojen käyttöön liittyviä määritysvaiheita, jotka mahdollistavat ulkoisten tietojen sisällyttämisen kassavirtaennusteeseen.

## <a name="external-data-setup"></a>ULkoisten tietojen määrittäminen

Syötä ulkoisten tietojen käyttämistä kassavirtaennusteissa tukevat asetukset käyttämällä **Ulkoinen lähde** -välilehteä **Kassavirtaennusteen määritykset** -sivulla (**Maksuliikenteen hallinta \> Kassavirran ennustaminen**).

Lisätietoja määrityksestä on kohdassa [Kassavirran ennustaminen](../cash-bank-management/cash-flow-forecasting.md).

Jos haluat syöttää ulkoisia tietoja kassavirtaennusteisiin, voit käyttää Avaa Excelissä -käyttökokemusta ulkoisten tietojen syöttämiseen ja muokkaamiseen. Valitse **Ulkoiset tiedot** -painike ja valitse sitten joko **Lisää ulkoisia tietoja** tai **Muokkaa aiemmin luotuja ulkoisia tietoja**. Kun Microsoft Excel -tiedosto avataan, voit kirjoittaa tiedot seuraaviin kenttiin:

- **Kirjaustunnus**
- **Kuvaus** (valinnainen)
- **Ulkoisen lähteen nimi** – Valitse jokin sen luettelon arvoista, jonka määritit Finance Insightsin määrittämisen yhteydessä.
- **Yritys**
- **Päivämäärä**
- **Summa tapahtuman valuuttana**
- **Valuuttakoodi**
- **Oletusdimensio** (valinnainen)
- **Asiakirjanumero** (valinnainen)
- **Tilinumero** (valinnainen)
- **Tilin nimi** (valinnainen)

## <a name="importing-external-data-by-using-the-data-management-framework"></a>Ulkoisten tietojen tuominen käyttämällä tiedonhallinnan kehystä

Voit tuoda kassavirtaennusteiden ulkoisia tietoja käyttämällä **Tiedonhallinta**-työtilaa ja entiteettiä, jonka nimi on **Kassavirtaennusteen ulkoinen lähdemerkintä**.

Jos sinun on siirrettävä asetustiedot ympäristöstä toiseen, tarvittavat asetustaulukot ovat käytettävissä seuraaville entiteeteille:

- Kassavirtaennusteen ulkoisen lähteen asetukset
- Kassavirtaennusteen ulkoisen lähdeyrityksen asetukset

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
