--- 
title: Ostotilauksen tuotteiden vastaanoton kirjaaminen
description: "Seuraavassa menettelyssä kuvataan, miten kirjaat tavaroiden vastaanoton suoraan ostotilaukseen."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9b2300a593c9e153ee598fa72e29907c82f2b79e
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a>Ostotilauksen tuotteiden vastaanoton kirjaaminen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Seuraavassa menettelyssä kuvataan, miten kirjaat tavaroiden vastaanoton suoraan ostotilaukseen. On myös mahdollista rekisteröidä tuotteiden vastaanotto varastoon ja kirjata ne myöhemmin ostotilaukseen. Tämän tehtävän suorittaa yleensä ostoedustaja tai ostoreskontran koordinaattori. Tämän oppaan esimerkissä käytetään esittely-yritys USMF:n tietoja. Esimerkki sisältää yksinkertaisen ostotilauksen luomisvaiheet siten, että voit toistaa menettelyn tehtäväoppaana. Jos käytät menettelyä omilla tiedoilla, aloita Tavaran vastaanoton kirjaaminen -alitehtävästä.


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a>Valmistele uusi ostotilaus tavaroiden vastaanottoa varten
1. Valitse Hankinta > Ostotilaukset > Kaikki ostotilaukset.
2. Valitse Uusi.
3. Kirjoita Toimittajan tili -kenttään arvoksi US-101.
4. Valitse OK.
5. Kirjoita Nimiketunnus-kenttään arvo M0001.
6. Kirjoita 5 Määrä-kenttään.
7. Valitse toimintoruudussa Osta.
8. Valitse Vahvista.

## <a name="record-receipt-of-goods"></a>Tavaran vastaanoton kirjaaminen
1. Valitse toimintoruudussa Vastaanota.
2. Valitse Tuotteen vastaanotto.
    * Määrä-kentän avulla voit valita haluamasi vastaanotettavan määrän. Jos määrä on esimerkiksi jo rekisteröity varastossa, voit valita rekisteröidyn määrän.  Tässä esimerkissä käytetään tilattua määrää.   
3. Kirjoita mikä tahansa arvo Tuotteen vastaanotto -kenttään.
    * Tätä kenttää käytetään syöttämään viite, jota käytetään tositteena tuotteen vastaanoton kirjauskansiossa.  
4. Laajenna Rivit-osa.
5. Valitse määräksi 4.
    * Tähän pystyt määrittämään manuaalisesti vastaanotettavan määrän kullekin tilauksen riville.  
6. Tiivistä Rivit-osa.
7. Valitse OK.
    * Tavarat nyt tallennettuja vastaanotetuiksi ostotilauksella, ja sitä vastaava tuotteen vastaanoton kirjauskansioasiakirja on luotu. Voit käyttää Tuotteen vastaanotto -toimintoa ostotilauksesta luotujen kirjauskansioiden tarkasteluun selvittääksesi mitä on vastaanotettu ja milloin.  


