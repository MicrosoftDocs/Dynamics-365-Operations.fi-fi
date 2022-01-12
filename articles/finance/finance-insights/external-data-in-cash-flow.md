---
title: Ulkoiset tiedot kassavirtaennusteissa
description: Tässä aiheessa käsitellään määritysvaiheita, jotka on suoritettava, jotta ulkoiset tiedot voidaan syöttää tai tuoda kassavirtaennusteisiin.
author: rcarlson
ms.date: 12/21/2021
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
ms.openlocfilehash: 66b097b2936e61c619d45ad103440eddbb983feb
ms.sourcegitcommit: c8dc60bb760553f166409c2e06dd2377f601c006
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/23/2021
ms.locfileid: "7945777"
---
# <a name="external-data-in-cash-flow-forecasts"></a>Ulkoiset tiedot kassavirtaennusteissa

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Ulkoisia tietoja voidaan lisätä tai tuoda kassavirtaennusteisiin. Tässä ohjeaiheessa kuvataan ulkoisten tietojen käyttöön liittyviä määritysvaiheita, jotka mahdollistavat ulkoisten tietojen sisällyttämisen kassavirtaennusteeseen.

## <a name="external-data-setup"></a>ULkoisten tietojen määrittäminen

Anna ulkoisten tietojen käyttämistä kassavirtaennusteissa tukevat asetukset käyttämällä **Ulkoinen lähde** -välilehteä **Kassavirtaennusteen määritykset** -sivulla (**Maksuliikenteen hallinta \> Kassavirran ennustaminen \> Kassavirtaennusteen määritys**).

Ulkoisia tietoja voidaan lisätä tai tuoda kassavirtaennusteisiin. Ulkoiset lähteet on määritettävä ennen ulkoisten tietojen antamista tai tuomista. Määritä ulkoiset kassavirtaluokat **Ulkoinen lähde** -välilehdessä. Luokka voi olla joko **Lähtevä** tai **Saapuva**. Kirjaustyypiksi on valittava **Maksuvalmius**. Valitse **Yrityksen asetukset** -ruudukossa yritykset ja vastaavat päätilit, joita ulkoiset kassavirtaluokat koskevat.

Lisätietoja kassavirtaennusteiden määrittämisestä on kohdassa [Kassavirtaennusteet](../cash-bank-management/cash-flow-forecasting.md).

## <a name="enter-external-data"></a>Ulkoisten tietojen antaminen

Kassavirtaennusteiden ulkoisia tietoja voi antaa ja muokata **Avaa Excelissä** -käyttökokemuksen avulla. Valitse **Ulkoiset tiedot** -painike **Kassavirtaennusteen määritys** -sivulla ja valitse sitten joko **Lisää ulkoisia tietoja** tai **Muokkaa aiemmin luotuja ulkoisia tietoja**. Kun Microsoft Excel -tiedosto avataan, voit kirjoittaa tiedot seuraaviin kenttiin:

- **Kirjaustunnus** (yksilöivä)
- **Kuvaus** (valinnainen)
- **Ulkoisen lähteen nimi** – valitse jokin sen luettelon arvoista, jonka määritit Finance Insightsin määrittämisen yhteydessä.
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
