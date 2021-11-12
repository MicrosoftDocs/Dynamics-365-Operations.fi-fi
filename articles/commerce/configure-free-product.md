---
title: Tuotteen määrittäminen ostettavaksi ilmaiseksi
description: Tässä aiheessa kuvataan, miten tuote määritetään siten, että sen voi hankkia maksutta Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2ad96a3dde93a48694aee418ecfbbd33dc9830d6
ms.sourcegitcommit: 6bf9e18989e6d77497a9dda1c362f324b3c2fbf2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/27/2021
ms.locfileid: "7713882"
---
# <a name="configure-a-product-to-be-purchased-for-free"></a>Tuotteen määrittäminen ostettavaksi ilmaiseksi

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tässä aiheessa kuvataan, miten tuote määritetään siten, että sen voi hankkia maksutta Microsoft Dynamics 365 Commercessa.

## <a name="configure-the-product"></a>Tuotteen määrittäminen

Jos haluat myydä tuotteen maksutta Dynamics 365 Commercessa, määritä sen hinnaksi 0 (nolla). Lisäksi sinun on määritettävä tuotteen **Nollahinta sallittu** -asetus.

**Nollahinta sallittu** -asetus määritetään Commerce-pääkonttorisovelluksessa seuraavasti.

1. Siirry kohtaan **Retail ja Commerce \> Tuotteet ja luokat \> Vapautetut tuotteet luokittain**.
1. Siirry tuotteeseen, jonka haluat myydä maksutta. 
1. Määritä tuotesivun **Commerce**-osassa **Nollahinta sallittu** -asetuksen arvoksi **Kyllä**.

Seuraavassa kuvassa esitetään esimerkki tuotteesta, jonka **Nollahinta sallittu** -asetuksen arvoksi on määritetty **Kyllä**.

![Esimerkki tuotteesta, jossa Nollahinta sallittu -asetukseksi on määritetty Kyllä.](./media/Zero-price.png)

## <a name="configure-the-online-stores-functionality-profile"></a>Verkkokaupan toimintoprofiilin määritys

Ennen kuin voit käsitellä maksuttomia tapahtumia, määritä verkkokauppasi toimintoprofiilin **Salli uloskuittaus ilman maksua** -asetus, jotta tapahtumat ilman maksuja ovat sallittuja. Tietoja toimintoprofiilien luomisesta: [Verkkotoimintoprofiilin luominen](online-functionality-profile.md).

**Salli uloskuittaus ilman maksua** -asetus määritetään Commerce-pääkonttorisovelluksessa seuraavasti.

1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Verkkokaupan asetukset**.
1. Määritä kauppasi toimintoprofiilin **Uloskuittaus**-kohdassa **Salli uloskuittaus ilman maksua** -asetuksen arvoksi **Kyllä**.

Seuraavassa kuvassa on esimerkki verkkokauppaprofiilista, jossa **Salli uloskuittaus ilman maksua** -asetuksen arvoksi on määritetty **Kyllä**.

![Esimerkki verkkokauppaprofiilista, jossa Salli uloskuittaus ilman maksua -asetuksen arvoksi on määritetty Kyllä.](./media/Zero-price-profile.png)

## <a name="additional-resources"></a>Lisäresurssit

[Vähittäismyyntihintojen hallinta](price-management.md)

[Luo online-toimintoprofiili](online-functionality-profile.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
