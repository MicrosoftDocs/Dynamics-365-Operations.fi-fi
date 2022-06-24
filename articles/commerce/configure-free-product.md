---
title: Tuotteen määrittäminen ostettavaksi ilmaiseksi
description: Tässä artikkelissa kuvataan, miten tuote määritetään siten, että sen voi hankkia maksutta Microsoft Dynamics 365 Commercessa.
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
ms.openlocfilehash: 4bd7e4f7a7873e471f1aee94f15e7932e8d9eecd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890352"
---
# <a name="configure-a-product-to-be-purchased-for-free"></a>Tuotteen määrittäminen ostettavaksi ilmaiseksi

[!include [banner](includes/banner.md)]


Tässä artikkelissa kuvataan, miten tuote määritetään siten, että sen voi hankkia maksutta Microsoft Dynamics 365 Commercessa.

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
