---
title: Laskun päivitysten suorittaminen palautuksille
description: Tämä toiminto tukee myös liiketoimintaprosesseja organisaatioissa, joissa palautustilaukset ja myyntitilauksen on päätetty laskuttaa samanaikaisesti ja laskutuksen suorittaa sama henkilö.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 32a108694c11a2ebd922a71d5c82691584bbb397
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014746"
---
# <a name="perform-invoice-updates-for-returns"></a>Laskun päivitysten suorittaminen palautuksille 

[!include [banner](../includes/banner.md)]


Palautustilaus on sellaisen myyntitilauksen tyyppi, joka on merkitty palautetuksi tilaukseksi. Siksi palautustilausten laskut luodaan **Kaikki myyntitilaukset**-luettelosivulla **Palautustilaukset** -lomakkeen sijaan. Tämä toiminto tukee myös liiketoimintaprosesseja organisaatioissa, joissa palautustilaukset ja myyntitilauksen on päätetty laskuttaa samanaikaisesti ja laskutuksen suorittaa sama henkilö.

Koska palautettavan nimikkeen laskussa on negatiivinen summa, sitä kutsutaan hyvityslaskuksi.

Kun määrität laskupäivityksen eräkäsittelyä varten, **Palautettu tilaus** -tyypin myyntitilauksen palautusrivin tilan pitää olla **Vastaanotettu**. Tämä tila ilmaisee, että tilauksen pakkausluettelo on päivitetty.

## <a name="post-an-invoice-for-a-return-order"></a>Palautustilauksen laskun kirjaus

1.  Valitse **Myyntireskontra** \>  **Tilaukset** \> **Kaikki myyntitilaukset**.

2.  Valitse myyntitilaus, jossa **Palautettu tilaus** näkyy **Tilauksen tyyppi** -kentässä.

3.  Valitse Toimintoruudun **Laskutus**-välilehden **Luo**-ryhmässä **Lasku**.

4.  Valitse **Parametrit**-välilehdellä **Kirjaus**-valintaruutu.

5.  Tarkista lomakkeen tiedot ja tee tarvittavat muutokset.

6.  Napsauta **OK**. Hyvityslasku kirjataan.

## <a name="see-also"></a>Lisätietoja

[Palautusten pakkausluettelopäivitykset](packing-slip-updates-returns.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]