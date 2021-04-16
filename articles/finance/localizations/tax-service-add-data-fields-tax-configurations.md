---
title: Tietokenttien lisääminen verokonfiguraatioihin
description: Tässä ohjeaiheessa kerrotaan, miten veromäärityksiä mukautetaan lisäämällä tietokenttiä.
author: kailiang
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b9d9fce81151ad70d57c69e389e238a6f9137d56
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819421"
---
# <a name="add-data-fields-in-tax-configurations"></a>Tietokenttien lisääminen verokonfiguraatioihin

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Tässä ohjeaiheessa kerrotaan, miten verokonfiguraatioita mukautetaan [käyttämällä verointegraatioon lisättyjä tietokenttiä](tax-service-add-data-fields-tax-integration-by-extension.md).

## <a name="customize-the-tax-data-model"></a>Veron tietomallin mukauttaminen

1. Siirry Microsoft Dynamics 365 Financessa kohtaan **Sähköinen raportointi** \> **Verokonfiguraatiot**.
2. Valitse määrityspuussa **Verotietomalli – Eurooppa**. Valitse siten toimintoruudussa **Luo konfigurointi**.
3. Valitse avattavasta valintaikkunasta **Verotettavan asiakirjan malli, johdettu nimestä: Verotietomalli – Eurooppa, Microsoft** -vaihtoehto, kirjoita uuden verotietomallin nimi ja valitse sitten **Luo konfiguraatio**.
4. Valitse juuri luomasi verotietomalli ja valitse sitten toimintoruudussa **Suunnitteluohjelma**.
5. Laajenna tietomallipuu, valitse **Rivit** ja valitse sitten **Uusi**.
6. Kirjoita **Luo solmu** -valintaikkunaan nimi, määritä kohteen tyyppi ja valitse sitten **Lisää**.
7. Lisää tarvittavat sarakkeet.
8. Valitse toimintoruudussa ensin **Tallenna** ja sitten **Valmis**.
9. Sulje sivu ja tarkastele verotietomallin valmista versiota.

## <a name="customize-the-tax-configuration"></a>Veromäärityksen mukauttaminen

1. Siirry Financessa kohtaan **Sähköinen raportointi** \> **Verokonfiguraatiot**.
2. Valitse määrityspuussa **Veromääritys – Eurooppa**. Valitse siten toimintoruudussa **Luo konfigurointi**.
3. Valitse avattavasta valintaikkunasta **Veropalvelun määritys, johdettu nimestä: Veromääritys – Eurooppa, Microsoft** -vaihtoehto, kirjoita uuden veromäärityksen nimi ja valitse sitten **Luo konfiguraatio**.
4. Valitse juuri luomasi veromääritys ja valitse sitten toimintoruudussa **Suunnitteluohjelma**.
5. Valitse **Ominaisuudet**-osan **Tietomalli**-kentästä aiemmin luomasi mukautettu verotietomalli.
6. Valitse **Tietomallin versio** -kentästä verotietomallin valmis versio.
7. Valitse **Lisää** ja lisää tarvittavat veromitat.
8. Valitse toimintoruudussa ensin **Tallenna** ja sitten **Valmis**.
9. Sulje sivu ja tarkastele veromäärityksen valmista versiota.

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a>Vero-ominaisuuksien toteuttaminen mukautetussa veromäärityksessä

1. Siirry Regulatory Configuration Servicesissä (RCS) kohtaan **Globalisointiominaisuudet** \> **Vero**.
2. Valitse **Lisää**, kirjoita uuden ominaisuuden tiedot ja valitse sitten **Luo ominaisuus**.
3. Valitse ominaisuus **Versiot**-välilehdessä ja valitse sitten **Muokkaa**.
4. Valitse **Yleiset**-välilehden **Konfiguraatioversio**-kentästä mukautettu veromääritys ja -versio.
5. Valitse **Sarakkeiden hallinta** -valintaikkunassa otsikko- ja rivisarakkeet, jotka haluat sisällyttää mukautettuun veromittaan, ja lisää ne sitten **Valitut sarakkeet** -luetteloon valitsemalla oikea nuolipainike.
