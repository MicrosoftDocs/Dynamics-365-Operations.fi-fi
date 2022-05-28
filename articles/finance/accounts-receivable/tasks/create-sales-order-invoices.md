---
title: Luo myyntitilauksen laskut
description: Tässä aiheessa käsitellään myyntitilauksen laskuttamista sekä laskujen yhdistämistä ja eräkäsittelyä.
author: ShivamPandey-msft
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7976d310e9c80dfe683359f1157b85e46c758c48
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713441"
---
# <a name="create-sales-order-invoices"></a>Luo myyntitilauksen laskut

[!include [banner](../../includes/banner.md)]

Tässä aiheessa käsitellään myyntitilauksen laskuttamista sekä laskujen yhdistämistä ja eräkäsittelyä. Näissä toimintaohjeissa käytetään esittely-yritystä USMF.


## <a name="create-an-invoice-from-a-sales-order"></a>Laskun luominen myyntitilauksesta
1. Valitse **Siirtymisruutu > Moduulit > Myyntireskontra > Tilaukset > Myyntitilaukset, jotka on lähetetty mutta joita ei ole laskutettu.**
2. Valitse myyntitilaus luettelosta. 
3. Valitse **toimintoruudussa** **Lasku > Luo > Lasku**. Ota huomioon, että tälle myyntitilaukselle on liitetty useita pakkausluetteloita. Näkyvissä on vain sana *useita* pakkausluetteloiden numeroiden sijaan.  
4. Laajenna **Parametrit**-osa.
    - Kirjauksen arvoksi on annettava Kyllä, jotta lasku kirjataan. Voit myös ottaa kirjauksen pois päältä ja vain tulostaa laskun. Saat kuitenkin saman tuloksen, kun luot proformalaskun laskun sijaan.  
    - Tätä vaihtoehtoa käytetään komentojonotöissä. Kysely suoritetaan, kun komentojonotyö suoritetaan.
5. Valitse **Tulosta**-kentässä Jälkeen.
6. Valitse **Tulosta lasku** -kohdassa **Kyllä**. Tulostuksenhallinnan avulla voit tulostaa laskusta useita kopioita ja myös lähettää laskun sähköpostitse PDF-tiedostona.  
7. Valitse **Tulosta kulut** -kentässä Tee yhteenveto.
8. Valitse **Tarkista luottoraja** -kentässä Saldo.
9. Valitse **Peruuta**.

## <a name="combine-orders-into-a-single-invoice"></a>Tilausten yhdistäminen yhdeksi laskuksi
1. Siirry siirtymisruudussa kohtaan **Moduulit > Myyntireskontra > Tilaukset > Kaikki myyntitilaukset**.
2. Etsi asiakas, jolla on useita avoimia laskuja.
3. Valitse useita saman asiakkaan avoimia myyntitilauksia.
4. Valitse **toimintoruudussa** **Lasku > Luo > Lasku**.
5. Laajenna **Parametrit**-osa.
6. Valitse **Määrä**-kentässä Kaikki. Ota huomioon, että yhteenveto-osassa näkyy kaksi laskua. Yhdistetään laskut yhdeksi laskuksi.  
7. Valitse **Yhteenvedon päivitys** -kentässä Laskutustili.
8. Valitse **Järjestä**, kun haluat yhdistää myyntitilaukset yhdeksi laskuksi. Kaksi myyntitilausta on nyt yhdistetty yhdeksi laskuksi.   
9. Valitse **Peruuta**.
10. Valitse **Kyllä**.

## <a name="post-invoices-in-a-batch"></a>Laskujen kirjaaminen eränä
1. Valitse **Siirtymisruutu > Moduulit > Myyntireskontra > Laskut > Erälaskutus > Lasku**.
2. Klikkaa **Valitse**.
3. Valitse **OK**.
4. Valitse **Erä**.
5. Valitse **eräkäsittelyn** arvoksi **Kyllä**.
6. Valitse **Toistuminen**.
7. Valitse **Päivät**,
8. Valitse **OK**.
9. Valitse **OK**.
10. Valitse **Peruuta**.
11. Valitse **Kyllä**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
