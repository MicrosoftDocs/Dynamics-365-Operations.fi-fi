---
title: Laskun päivitysten suorittaminen palautuksille
description: Tämä toiminto tukee myös liiketoimintaprosesseja organisaatioissa, joissa palautustilaukset ja myyntitilauksen on päätetty laskuttaa samanaikaisesti ja laskutuksen suorittaa sama henkilö.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f962641f7fdae18a360567d6f37348fabbfc302
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "364370"
---
# <a name="perform-invoice-updates-for-returns"></a>Laskun päivitysten suorittaminen palautuksille 

[!include [banner](../includes/banner.md)]


Palautustilaus on sellaisen myyntitilauksen tyyppi, joka on merkitty palautetuksi tilaukseksi. Siksi palautustilausten laskut luodaan **Kaikki myyntitilaukset**-luettelosivulla **Palautustilaukset** -lomakkeen sijaan. Tämä toiminto tukee myös liiketoimintaprosesseja organisaatioissa, joissa palautustilaukset ja myyntitilauksen on päätetty laskuttaa samanaikaisesti ja laskutuksen suorittaa sama henkilö.

Koska palautettavan nimikkeen laskussa on negatiivinen summa, sitä kutsutaan hyvityslaskuksi.

Kun määrität laskupäivityksen eräkäsittelyä varten, **Palautettu tilaus** -tyypin myyntitilauksen palautusrivin tilan pitää olla **Vastaanotettu**. Tämä tila ilmaisee, että tilauksen pakkausluettelo on päivitetty.

## <a name="post-an-invoice-for-a-return-order"></a>Palautustilauksen laskun kirjaus

1.  Napsauta **Myyntireskontra** \> **Yleinen** \> **Myyntitilaukset** \> **Kaikki myyntitilaukset**.

2.  Valitse myyntitilaus, jossa **Palautettu tilaus** näkyy **Tilauksen tyyppi** -kentässä.

3.  Valitse Toimintoruudun **Laskutus**-välilehden **Luo**-ryhmässä **Lasku**.

4.  Valitse **Parametrit**-välilehdellä **Kirjaus**-valintaruutu.

5.  Tarkista lomakkeen tiedot ja tee tarvittavat muutokset.

6.  Napsauta **OK**. Hyvityslasku kirjataan.

## <a name="see-also"></a>Lisätietoja

[Palautusten pakkausluettelopäivitykset](packing-slip-updates-returns.md)

  


