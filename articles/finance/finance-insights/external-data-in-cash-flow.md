---
title: Ulkoiset tiedot kassavirtaennusteissa
description: Tässä artikkelissa käsitellään määritysvaiheita, jotka on suoritettava, jotta ulkoiset tiedot voidaan syöttää tai tuoda kassavirtaennusteisiin.
author: RyanCCarlson2
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f0cb05770dc2fbd4e13af261b5f0a0e117a2f6d7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846941"
---
# <a name="external-data-in-cash-flow-forecasts"></a>Ulkoiset tiedot kassavirtaennusteissa

[!include [banner](../includes/banner.md)]

Ulkoisia tietoja voidaan lisätä tai tuoda kassavirtaennusteisiin. Tässä artikkelissa kuvataan ulkoisten tietojen käyttöön liittyviä määritysvaiheita, jotka mahdollistavat ulkoisten tietojen sisällyttämisen kassavirtaennusteeseen.

## <a name="external-data-setup"></a>ULkoisten tietojen määrittäminen

Anna ulkoisten tietojen käyttämistä kassavirtaennusteissa tukevat asetukset käyttämällä **Ulkoinen lähde** -välilehteä **Kassavirtaennusteen määritykset** -sivulla (**Maksuliikenteen hallinta \> Kassavirran ennustaminen \> Kassavirtaennusteen määritys**).

Ulkoisia tietoja voidaan lisätä tai tuoda kassavirtaennusteisiin. Ulkoiset lähteet on määritettävä ennen ulkoisten tietojen antamista tai tuomista. Määritä ulkoiset kassavirtaluokat **Ulkoinen lähde** -välilehdessä. Luokka voi olla joko **Lähtevä** tai **Saapuva**. Kirjaustyypiksi on valittava **Maksuvalmius**. Valitse **Yrityksen asetukset** -ruudukossa yritykset ja vastaavat päätilit, joita ulkoiset kassavirtaluokat koskevat.

Lisätietoja kassavirtaennusteiden määrittämisestä on kohdassa [Kassavirtaennusteet](../cash-bank-management/cash-flow-forecasting.md).

## <a name="enter-external-data"></a>Ulkoisten tietojen antaminen

Kassavirtaennusteiden ulkoisia tietoja voi antaa ja muokata **Avaa Excelissä** -käyttökokemuksen avulla. Valitse **Ulkoiset tiedot** -painike **Kassavirtaennuste**-työtilasivulla ja valitse sitten joko **Lisää ulkoisia tietoja** tai **Muokkaa aiemmin luotuja ulkoisia tietoja**. Kun Microsoft Excel -tiedosto avataan, voit kirjoittaa tiedot seuraaviin kenttiin:

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
