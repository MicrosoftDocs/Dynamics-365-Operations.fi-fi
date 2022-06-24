---
title: Jaetun laskun toiminnot
description: Tässä artikkelissa kuvataan asetuksia ja toimintoja laskujen jakamiseen toimitusosoitteen ja verotilinumeron (TAN) mukaan.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 7bbeb94429c2c69b7b8ea3089390db676a021b80
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874429"
---
# <a name="split-invoice-functionality"></a>Jaetun laskun toiminnot

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan asetuksia ja toimintoja laskujen jakamiseen toimitusosoitteen ja verotilinumeron (TAN) mukaan.

Valitse **Ostoreskontran parametrit** -sivun **Yleiset**-välilehdestä **Tuotevastaanotto**- tai **Lasku**-valintaruutu, kun haluat kirjata ja jakaa **Ostotilaus**-sivulla tuotteen vastaanoton tai laskun, jolla on eri toimitusosoitteet ja TAN-numerot. Kirjattu lasku jaetaan tämän jälkeen toimitusosoitteen ja TAN-numeron perusteella.

**Yhteenvedon päivitys** -välilehdessä **Jaon peruste** -pikavälilehden **Toimitustiedot**-rivillä määritä **Vahvistus**-, **Keräysluettelo**-, **Pakkausluettelo**- tai **Lasku**-vaihtoehdon arvoksi **Kyllä**, jos haluat kirjata ja jakaa vahvistuksen, keräysluettelon, pakkausluettelon tai laskun, jossa eri toimitusosoitteet ja TAN-numerot on määritetty eri laskuriveille **Myyntitilaus**-sivulla. Lasku jaetaan ensin toimitusosoitteen ja sitten TAN-numeron perusteella.

> [!IMPORTANT]
> - Jos **Toimitustiedot**-vaihtoehtojen asetuksena ei ole **Kyllä**, lasku kirjataan yhtenä laskuna. Laskun jakoa ei tapahdu.
> - Jos haluat jakaa ja kirjata pakkausluettelon, jossa laskuriveillä on eri toimitusosoitteet ja TAN-numerot, määritä **Pakkausluettelo**-asetuksen arvoksi **Toimitustiedot**-kohdassa **Kyllä**.
> - Jos haluat jakaa ja kirjata laskun, jossa laskuriveillä on eri toimitusosoitteet ja TAN-numerot, määritä **Lasku**-asetuksen arvoksi **Toimitustiedot**-kohdassa **Kyllä**.
> - Jos haluat kirjata laskun, jossa laskuriveillä on eri toimitusosoitteet mutta samat TAN-numerot, määritä **Lasku**-asetuksen arvoksi **Toimitustiedot**-kohdassa **Ei**. Lasku jaetaan toimitusosoitteen perusteella.

## <a name="example"></a>Esimerkki

Tässä esimerkissä **Lasku**-asetus on **Toimitustiedot**-kohdassa **Kyllä** **Ostoreskontran parametrit** -sivun **Yhteenvedon päivitys** -välilehdessä. Ostolasku kirjataan, ja sen riveillä on seuraavat toimitusosoitteiden ja TAN-numeroiden asetukset:

- **Nimikerivi 1:** Toimitusosoite 1, TAN-ABCD12345A
- **Nimikerivi 2:** Toimitusosoite 1, TAN-ABCD12345A
- **Nimikerivi 3:** Toimitusosoite 2, TAN-ABCE12345B
- **Nimikerivi 4:** Toimitusosoite 3, TAN-ABCD12345A

Tällöin alkuperäinen lasku jaetaan kahteen laskuun ja kirjataan seuraavasti:

- Lasku 1 kirjataan nimikeriville 1 ja nimikeriville 2, koska molemmilla riveillä on sama toimitusosoite ja TAN.
- Lasku 2 kirjataan nimikeriville 3.
- Lasku 3 kirjataan nimikeriville 4.
