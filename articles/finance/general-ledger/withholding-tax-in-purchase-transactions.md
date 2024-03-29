---
title: Ennakonpidätys ostotapahtumissa
description: Ennakonpidätyksen alaisille toimittajille voit määrittää **ennakonpidätysryhmän** oletusarvon **Kaikki toimittajat** -sivulla.
author: kailiang
ms.date: 01/12/2021
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
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: c2220159cef31bf3343bcf39325c7a0ff3e0cf47
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727199"
---
# <a name="withholding-tax-in-purchase-transactions"></a>Ennakonpidätys ostotapahtumissa

Ennakonpidätyksen alaisille toimittajille voit määrittää **ennakonpidätysryhmän** oletusarvon **Kaikki toimittajat** -sivulla.

1. Siirry kohtaan **Siirtymisruutu > Moduulit > Ostoreskontra > Toimittajat > Kaikki toimittajat**.

2. Valitse haluttu toimittajatili ja valitse **Muokkaa**.

3. Määritä **Lasku ja toimitus** -välilehdessä **Laske ennakonpidätys** -kentän arvoksi **Kyllä**.

   > [!NOTE] 
   > Ennakonpidätystä ei lasketa, jos tämän toimittajan **Laske ennakonpidätys** -asetusta ei ole otettu käyttöön tiedoissa.

4. Valitse ennakonpidätysryhmä kohdassa **Ennakonpidätysryhmä**.

5. Valitse **Tallenna**.

Voit määrittää ennakonpidätyksen alaisille nimikkeille/palveluille oletusarvoisen **Nimikkeen ennakonpidätysryhmän** kohdassa **Julkaistut tuotteet**.

1. Valitse **Siirtymisruutu > Moduulit > Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet**.

2. Valitse haluttu nimikenumero ja valitse **Muokkaa**.

3. Valitse **Osto**-välilehdestä **Laske ennakonpidätys**.

   > [!NOTE] 
   > Ennakonpidätystä ei lasketa, jos **Laske ennakonpidätys** -asetuksena ei ole **Kyllä** tälle nimikkeelle **Julkaistu tuote** -sivun **Osto**-välilehdessä.

4. Valitse nimikkeen ennakonpidätysryhmä **Nimikkeen ennakonpidätysryhmä** -luettelossa.

5. Valitse **Tallenna**.

Ennakonpidätysryhmät ja nimikkeen ennakonpidätysryhmät voidaan sivuilla. 

- **Ostotilaus**
- **Toimittajan lasku**
- **Laskukirjauskansio**

Ennakonpidätysryhmän ja nimikkeen ennakonpidätysryhmän oletusarvo tulee riveille, kun luot **ostotilauksia** ja/tai **odottavia toimittajan laskuja**. Voit ottaa **toimittajan laskukirjauskansion** osalta käyttöön **Laske ennakonpidätys** -asetuksen ja valita kirjauskansion **Yleiset**-välilehdestä **Nimikkeen ennakonpidätysryhmän**.

Ennakonpidätyksen väliaikainen summa on käytettävissä **Ostotilaus**-sivun **Summat**-välilehden **Oikaistu ennakonpidätys** -kentässä.

![Ennakonpidätys sisältyy ostotilaukseen.](media/withholding-tax-adjusted.png)

Ennakonpidätys lasketaan **toimittajan maksukirjauskansiossa**. Voit oikaista sovellettavia ennakonpidätyskoodeja sekä todellisia ennakonpidätyksen summia manuaalisesti **Ennakonpidätys** -välilehdessä **Tapahtumien selvitys** -sivulla.

![Ennakonpidätyksen voi muuttaa manuaalisesti Tapahtumien selvitys -sivulla.](media/withholding-tax-vendor-payment-tab.png)

Johdettu ennakonpidätyksen summa vähennetään toimittajan maksusta ja kirjataan **ennakonpidätystilille** liittyvässä tositteessa.

![Ennakonpidätystili, jossa näkyy liittyvä tosite.](media/withholding-tax-adjusted.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
