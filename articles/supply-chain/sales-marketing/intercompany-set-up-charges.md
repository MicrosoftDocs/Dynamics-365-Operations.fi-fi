---
title: Konsernin sisäisten tilausten kulujen määrittäminen
description: Tässä aiheessa käsitellään konsernin sisäisten tilausten kulujen määrittämistä
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 3786df5ce185fa8433d7c69bed5bef09b4983b8b
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548245"
---
# <a name="set-up-charges-on-intercompany-orders"></a>Konsernin sisäisten tilausten kulujen määrittäminen

[!include [banner](../../includes/banner.md)]

Konsernin sisäisiin tilauksiin lisättävät kulut voidaan määrittää. Kun konsernin sisäiseen myyntitilaukseen lisätään kulu, se synkronoituu automaattisesti konsernin sisäiseen ostotilaukseen. Näin toimitaan kumpaankin suuntaan eli konsernin sisäisestä myyntitilauksesta ostotilaukseen ja päinvastoin.

Kulujen avulla voidaan konsernin sisäiseen myyntitilaukseen voidaan lisätä voitto määrittämällä kulut konsernin sisäiseksi prosentiksi.

Kun kulut määritetään konsernin sisäisiin tilauksiin, käyttöön otetaan sisäisen voiton laskenta konsernin sisäiselle myyntitilaukselle, joka tehdään myyntitilauksen alkuperäisestä nettosummasta. Tämä kannattaa ehkä tehdä, jos konsernin sisäinen toimittaja myynti on kustannushintaista. Seuraava menettely koskee tämän tekemistä konsernin sisäisille asiakkaille. Samaa menettelyä voidaan käyttää toimittajien osalta.

1. Valitse **Myyntireskontra \> Asetukset \> Kulut \> Asiakkaan kuluryhmät**.
1. Luo kuluryhmä.
1. Siirry kohtaan **Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat**. Valitse asiakastilin linkki. Valitse toimintoruudussa **Asiakkaat**-välilehti ja valitse sitten **Myyntitilaus**-pikaväliehti.
1. Ota muokkaukset käyttöön kentässä valitsemalla toimintoruudussa **Muokkaa**. Valitse **Kuluryhmä**-kentässä vaiheessa 2 määritetty konsernin sisäinen kuluryhmä.
1. Valitse **Myyntireskontra \> Asetukset \> Kulut \> Automaattiset kulut**.
1. Määritä kulut täyttämällä soveltuvat kentät.
1. Valitse **Asiakassuhde**-kentässä vaiheessa 2 määritetty konsernin sisäinen kuluryhmä.
1. Valitse **Rivit**-pikavälilehden **Luokka**-kentässä **Konsernin sisäinen prosentti**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
