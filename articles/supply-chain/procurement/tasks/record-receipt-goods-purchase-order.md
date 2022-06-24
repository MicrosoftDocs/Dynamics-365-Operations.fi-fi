---
title: Ostotilauksen tuotteiden vastaanoton kirjaaminen
description: Tässä artikkelissa kuvataan, miten kirjaat tavaroiden vastaanoton suoraan ostotilaukseen.
author: GalynaFedorova
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22baf6d0f6db04b3c6ce3c09ee8cb286e9a1e590
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882457"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a>Ostotilauksen tuotteiden vastaanoton kirjaaminen

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa kuvataan, miten kirjaat tavaroiden vastaanoton suoraan ostotilaukseen. On myös mahdollista rekisteröidä tuotteiden vastaanotto varastoon ja kirjata ne myöhemmin ostotilaukseen. Tämän tehtävän suorittaa yleensä ostoedustaja tai ostoreskontran koordinaattori. Tämän oppaan esimerkissä käytetään esittely-yritys USMF:n tietoja. Esimerkki sisältää yksinkertaisen ostotilauksen luomisvaiheet siten, että voit toistaa menettelyn tehtäväoppaana. Jos käytät menettelyä omilla tiedoilla, aloita **Tavaran vastaanoton kirjaaminen** -alitehtävästä.


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a>Valmistele uusi ostotilaus tavaroiden vastaanottoa varten
1. Siirry siirtymisruudussa kohtaan **Moduulit > Hankinta > Ostotilaukset > Kaikki ostotilaukset**.
2. Valitse **Uusi**.
3. Kirjoita **Toimittajan tili** -kenttään arvoksi `US-101`.
4. Valitse **OK**.
5. Kirjoita **Nimiketunnus**-kenttään arvo `M0001`.
6. Kirjoita **Määrä**-kenttään `5`.
7. Valitse toimintoruudussa **Osto**.
8. Valitse **Vahvista**.

## <a name="record-receipt-of-goods"></a>Tavaran vastaanoton kirjaaminen
1. Valitse toimintoruudussa **Vastaanota**.
2. Valitse **Tuotteen vastaanotto**. **Määrä**-kentän avulla voit valita haluamasi vastaanotettavan määrän. Jos määrä on esimerkiksi jo rekisteröity varastossa, voit valita **Rekisteröity määrä**. Tässä esimerkissä käytetään arvoa **Tilattu määrä**
3. Laajenna **Yleiskatsaus**-osa.
4. Kirjoita mikä tahansa arvo **Tuotteen vastaanotto** -kenttään. Tätä kenttää käytetään syöttämään viite, jota käytetään tositteena tuotteen vastaanoton kirjauskansiossa.  
5. Laajenna **Rivit**-osa.
6. Valitse **määräksi** 4. Tähän pystyt määrittämään manuaalisesti vastaanotettavan määrän kullekin tilauksen riville.  
7. Valitse **OK**. Tavarat nyt tallennettuja vastaanotetuiksi ostotilauksella, ja sitä vastaava tuotteen vastaanoton kirjauskansioasiakirja on luotu. Voit käyttää Tuotteen vastaanotto -toimintoa ostotilauksesta luotujen kirjauskansioiden tarkasteluun selvittääksesi mitä on vastaanotettu ja milloin.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]