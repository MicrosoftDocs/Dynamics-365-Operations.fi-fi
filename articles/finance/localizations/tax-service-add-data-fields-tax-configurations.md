---
title: Tietokenttien lisääminen veromäärityksiin
description: Tässä artikkelissa kerrotaan, miten veromäärityksiä mukautetaan lisäämällä tietokenttiä.
author: Kai-Cloud
ms.date: 10/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 894c42f444d27b807288b84c7b9c620ad0121fa9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872323"
---
# <a name="add-data-fields-in-tax-configurations"></a>Tietokenttien lisääminen veromäärityksiin

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten verokonfiguraatioita mukautetaan [käyttämällä verointegraatioon lisättyjä tietokenttiä](tax-service-add-data-fields-tax-integration-by-extension.md).

## <a name="customize-the-tax-data-model"></a>Veron tietomallin mukauttaminen

1. Siirry Microsoft Dynamics 365 Financessa kohtaan **Sähköinen raportointi** > **Verokonfiguraatiot**.
2. Valitse määrityspuussa **Verolaskennan tietomalli**. Valitse siten toimintoruudussa **Luo konfigurointi**. 

  > [!NOTE] 
  > Jos käytettävissä ei ole määrityslähdettä, luo sellainen ja ota se käyttöön veronmäärityksessäsi. Lisätietoja on kohdassa [Määrityspalvelujen luonti ja merkitseminen aktiiviseksi](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
  
3. Valitse avattavasta valintaikkunasta **Verotettavan asiakirjan malli, johdettu nimestä: Verolaskentatietomalli, Microsoft**, kirjoita uuden verotietomallin nimi ja valitse sitten **Luo konfiguraatio**.
4. Valitse juuri luomasi verotietomalli ja valitse sitten toimintoruudussa **Suunnitteluohjelma**.
5. Laajenna tietomallipuu, valitse **Rivit** ja valitse sitten **Uusi**.
6. Kirjoita **Luo solmu** -valintaikkunaan nimi, määritä kohteen tyyppi ja valitse sitten **Lisää**.
7. Lisää tarvittavat sarakkeet.
8. Valitse toimintoruudussa ensin **Tallenna** ja sitten **Valmis**.
9. Sulje sivu ja tarkastele verotietomallin valmista versiota.

## <a name="customize-the-tax-configuration"></a>Veromäärityksen mukauttaminen

1. Siirry Financessa kohtaan **Sähköinen raportointi** > **Verokonfiguraatiot**.
2. Valitse määrityspuussa **Verolaskennan tietomallimääritys**. Valitse siten toimintoruudussa **Luo konfigurointi**.
3. Valitse avattavasta valintaikkunasta **Veropalvelun määritys, johdettu nimestä: Veronlaskentamääritys – Eurooppa, Microsoft**, kirjoita uuden veromäärityksen nimi ja valitse sitten **Luo konfiguraatio**.
4. Valitse juuri luomasi veromääritys ja valitse sitten toimintoruudussa **Suunnitteluohjelma**.
5. Valitse **Ominaisuudet**-osan **Tietomalli**-kentästä aiemmin luomasi mukautettu verotietomalli.
6. Valitse **Tietomallin versio** -kentästä verotietomallin valmis versio.
7. Valitse **Lisää** ja lisää tarvittavat veromitat.
8. Valitse toimintoruudussa ensin **Tallenna** ja sitten **Valmis**.
9. Sulje sivu ja tarkastele veromäärityksen valmista versiota.

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a>Vero-ominaisuuksien toteuttaminen mukautetussa veromäärityksessä

1. Siirry In Regulatory Configuration Servicessä (RCS) kohtaan **Globalisointiominaisuudet** > **Vero**.
2. Valitse **Lisää**, kirjoita uuden ominaisuuden tiedot ja valitse sitten **Luo ominaisuus**.
3. Valitse ominaisuus **Versiot**-välilehdessä ja valitse sitten **Muokkaa**.
4. Valitse **Yleiset**-välilehden **Konfiguraatioversio**-kentästä mukautettu veromääritys ja -versio.
5. Valitse **Sarakkeiden hallinta** -valintaikkunassa otsikko- ja rivisarakkeet, jotka haluat sisällyttää mukautettuun veromittaan, ja lisää ne sitten **Valitut sarakkeet** -luetteloon valitsemalla oikea nuolipainike.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
