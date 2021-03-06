---
title: Ennakonpidätys myyntitapahtumissa
description: Tässä ohjeaiheessa on luettelo vaiheista valittujen asiakkaiden ennakonpidätyksen laskennan välttämiseksi. Voit määrittää oletusennakonpidätysryhmän asiakkaille, jotka määrittävät ennakonpidätyksen maksuissaan.
author: roschlom
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 8e11ce10faa9b450b6f36a856b34b06b4ee1838d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842341"
---
# <a name="withholding-tax-in-sales-transactions"></a>Ennakonpidätys myyntitapahtumissa

Tässä ohjeaiheessa on luettelo vaiheista valittujen asiakkaiden ennakonpidätyksen laskennan välttämiseksi. Voit **Asiakkaat**-sivulla määrittää oletusarvoisen **Ennakonpidätysryhmä**-ryhmän asiakkaille, jotka määrittävät ennakonpidätyksen maksuissaan. 

1. Siirry kohtaan **Siirtymisruutu > Moduulit > Myyntireskontra > Asiakkaat > Kaikki asiakkaat**.

2. Valitse haluttu asiakastili ja valitse **Muokkaa**.

3. Määritä **Lasku ja toimitus** -välilehdessä **Laske ennakonpidätys** -kentän arvoksi **Kyllä**.

   > [!NOTE] 
   > Ennakonpidätystä ei lasketa, jos tämän asiakkaan **Laske ennakonpidätys** -asetusta ei ole otettu käyttöön päätiedoissa.

4. Valitse ennakonpidätysryhmä kohdassa **Ennakonpidätysryhmä**.

5. Valitse **Tallenna**.

Voit määrittää nimikkeelle/palvelulle, josta pitää maksaa ennakonpidätys, oletusarvoisen **Nimikkeen ennakonpidätysryhmän** kohdassa **Julkaistut tuotteet**.

1. Valitse **Siirtymisruutu > Moduulit > Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet**.

2. Valitse haluttu nimikenumero ja valitse **Muokkaa**.

3. Valitse **Myynti**-välilehdestä **Laske ennakonpidätys**.

   > [!NOTE] 
   > Ennakonpidätystä ei lasketa, jos **Laske ennakonpidätys** -asetuksena ei ole **Kyllä** tälle nimikkeelle **Julkaistu tuote** -sivun **Myynti**-välilehdessä.

4. Valitse nimikkeen ennakonpidätysryhmä **Nimikkeen ennakonpidätysryhmä** -luettelossa.

5. Valitse **Tallenna**.

Ennakonpidätysryhmät ja nimikkeen ennakonpidätysryhmät voidaan määrittää **Myyntitilaus**-sivulla. 

Kun luot uuden myyntitilauksen, käytetään ennakonpidätysryhmän ja nimikkeen ennakonpidätysryhmän oletusarvoja myyntitilausriveillä.

Ennakonpidätys lasketaan ja kirjataan **asiakkaan maksukirjauskansiossa**. Voit oikaista sovellettavaa ennakonpidätyskoodia sekä todellista ennakonpidätyksen summaa manuaalisesti **Ennakonpidätys** -välilehdessä **Tapahtumien selvitys** -sivulla.

Laskettu ennakonpidätyksen summa vähennetään asiakasmaksusta ja kirjataan **ennakonpidätyksen vastatilille** liittyvässä tositteessa.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]