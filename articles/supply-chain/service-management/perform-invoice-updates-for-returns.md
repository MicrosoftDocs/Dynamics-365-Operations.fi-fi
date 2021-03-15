---
title: Laskun päivitysten suorittaminen palautuksille
description: Tämä toiminto tukee myös liiketoimintaprosesseja organisaatioissa, joissa palautustilaukset ja myyntitilauksen on päätetty laskuttaa samanaikaisesti ja laskutuksen suorittaa sama henkilö.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d99f067e93de57b5b13787f128f450f736660351
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006670"
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

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]