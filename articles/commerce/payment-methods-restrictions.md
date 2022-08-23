---
title: Maksutapojen rajoittaminen kuitittomille palautuksille
description: Tässä artikkelissa käsitellään, miten tiettyjä palautusten maksutapoja voidaan rajoittaa, jos palautus tehdään ilman kuittia.
author: josaw1
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.industry: Retail
ms.search.form: RetailTenderTypeTable
ms.openlocfilehash: 9b14d7d8f6a2d9209ad6a12cd53bce4a9b50178d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281393"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Maksutapojen rajoittaminen kuitittomille palautuksille


[!include [banner](includes/banner.md)]

Jokainen vähittäismyyjän hyväksymä maksutapa on määritettävä, kun järjestelmä on määritetty. Tässä artikkelissa käsitellään, miten tiettyjä palautusten maksutapoja voidaan rajoittaa, jos palautus tehdään ilman kuittia.

## <a name="set-up-payment-methods"></a>Maksutapojen määrittäminen

Maksutapojen määrittämistä varten on suoritettava seuraavat tehtävät.
1. Luo maksutavat, jotka hyväksytään koko organisaatiossa.
2. Organisaation laajuisten korttityyppien ja korttien numeroiden luominen. Jos luottokortit tai pankkikortit hyväksytään, luo ensin yksi korttimaksuvälinetyyppi ja luo sitten organisaation laajuiset korttityypit ja korttien numerot.
3. Määritä myymälän maksutavat. Liitä maksutavat kuhunkin myymälään ja määritä sitten myymäläkohtaiset asetukset kullekin myymälän maksutavalle.
4. Aseta liikkeille korttimaksutavat. Suorita korttimaksujen määritys loppuun kaikille korttimaksutavoille, jotka hyväksyt liikkeessä.

![Myymälän asetukset.](media/NoReceiptReturns1.png "Retail POS -asetukset") 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Maksutapojen rajoittaminen kuitittomille palautuksille

Määritä kullekin myymälän maksutavalle **Myymälän hallinta** -sivun **Kuitittomat palautukset** -kohdan **Rajoitus kuitittomille palautuksille** -asetukseksi **Kyllä**. 

Vaihtokytkimen oletusarvo on **Ei**, mikä varmistaa, että maksutapa sallitaan palautuksille. 

Kun **Rajoitus kuitittomille palautuksille** -asetukseksi on valittu **Kyllä**, valittua maksutapaa ei sallita palautuksille. 

![Myymälän maksutapa.](media/NoReceiptReturns3.png "Vähittäismyymälän maksutapa") 

> [!NOTE]
> Kun kassa valitsee kuitittomien palautusten rajoitetun maksutavan, avautuva sanoma pyytää varmistamaan hyväksytyt maksutavat.

![Hyväksyttävät maksutavat.](media/NoReceiptReturns4.png "Hyväksyttävät maksutavat") 

Jos tapahtuma on sekä kuitillinen että kuititon palautus, rajoitusehtojen noudattamista ei pakoteta, koska tapahtuma palautetaan työnkulkuun kuitillisena. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
