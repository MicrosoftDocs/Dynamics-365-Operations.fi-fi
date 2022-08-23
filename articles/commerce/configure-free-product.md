---
title: Tuotteen määrittäminen ostettavaksi ilmaiseksi
description: Tässä artikkelissa kuvataan, miten tuote määritetään siten, että sen voi hankkia maksutta Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 88370085de047a5e0be773dde218770cfa242d14
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280361"
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
