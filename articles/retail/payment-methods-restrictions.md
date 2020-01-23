---
title: Maksutapojen rajoittaminen kuitittomille palautuksille
description: Tässä ohjeaiheessa käsitellään, miten tiettyjä palautusten maksutapoja voidaan rajoittaa, jos palautus tehdään ilman kuittia.
author: rapraj
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: 22e675fd9b7ee33c89f52ac4c8c15807580b86a7
ms.sourcegitcommit: b806f0c94d703bec39680fead827733361d47045
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/07/2020
ms.locfileid: "2935849"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Maksutapojen rajoittaminen kuitittomille palautuksille


[!include [banner](includes/banner.md)]

Jokainen vähittäismyyjän hyväksymä maksutapa on määritettävä, kun järjestelmä on määritetty. Tässä ohjeaiheessa käsitellään, miten tiettyjä palautusten maksutapoja voidaan rajoittaa, jos palautus tehdään ilman kuittia.

## <a name="set-up-payment-methods"></a>Maksutapojen määrittäminen

Maksutapojen määrittämistä varten on suoritettava seuraavat tehtävät.
1. Luo maksutavat, jotka hyväksytään koko organisaatiossa.
2. Organisaation laajuisten korttityyppien ja korttien numeroiden luominen. Jos luottokortit tai pankkikortit hyväksytään, luo ensin yksi korttimaksuvälinetyyppi ja luo sitten organisaation laajuiset korttityypit ja korttien numerot.
3. Määritä myymälän maksutavat. Liitä maksutavat kuhunkin myymälään ja määritä sitten myymäläkohtaiset asetukset kullekin myymälän maksutavalle.
4. Aseta liikkeille korttimaksutavat. Suorita korttimaksujen määritys loppuun kaikille korttimaksutavoille, jotka hyväksyt liikkeessä.

![Retail POS -asetukset](media/NoReceiptReturns1.png "Retail POS -asetukset") 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Maksutapojen rajoittaminen kuitittomille palautuksille

Määritä kullekin myymälän maksutavalle **Vähittäismyymälän hallinta** -sivun **Kuitittomat palautukset** -kohdan **Rajoitus kuitittomille palautuksille** -asetukseksi **Kyllä**. 

Vaihtokytkimen oletusarvo on **Ei**, mikä varmistaa, että maksutapa sallitaan palautuksille. 

Kun **Rajoitus kuitittomille palautuksille** -asetukseksi on valittu **Kyllä**, valittua maksutapaa ei sallita palautuksille. 

![Vähittäismyymälän maksutapa](media/NoReceiptReturns3.png "Vähittäismyymälän maksutapa") 

> [!NOTE]
> Kun kassa valitsee kuitittomien palautusten rajoitetun maksutavan, avautuva sanoma pyytää varmistamaan hyväksytyt maksutavat.

![Hyväksyttävät maksutavat](media/NoReceiptReturns4.png "Hyväksyttävät maksutavat") 

Jos tapahtuma on sekä kuitillinen että kuititon palautus, rajoitusehtojen noudattamista ei pakoteta, koska tapahtuma palautetaan työnkulkuun kuitillisena. 

