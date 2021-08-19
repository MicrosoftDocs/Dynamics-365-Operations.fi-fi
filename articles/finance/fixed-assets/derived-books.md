---
title: Johdetut kirjat
description: Tässä artikkelissa on yleiskuvaus johdetun kirjan toiminnoista.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9e3bb4d5ac566ef361ff0b7e34823e11eeb6c979d058130c50a4618997fd50a3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712434"
---
# <a name="derived-books"></a>Johdetut kirjat

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on yleiskuvaus johdetun kirjan toiminnoista.

Johdettujen kirjojen avulla voidaan yksinkertaistaa säännöllisesti ajoitettujen käyttöomaisuuden kirjatapahtumien kirjaamista.  Voit valita yhden kirjan ensisijaiseksi kirjaksi. Valinta on yleensä kirjanpidon poistossa käytettävä kirja. Tämän jälkeen se liitetään muihin kirjoihin, jotka on määritetty kirjaamaan tapahtumat samoille aikaväleille kuin ensisijainen kirja. Verotuksen poistojen kirjat määritetään usein johdettuina kirjoina. 

Yleisimmät johdettuihin kirjoihin kirjattavaksi määritettävät tapahtumat ovat hankinnat, hankintaoikaisut ja luovutukset. 

## <a name="example"></a>Esimerkki

Hankinta-tapahtumatyypin kirjan A johdetuiksi kirjoiksi on määritetty kirjat B ja C. Kirjalle A syötetään käyttöomaisuuserän 123 hankintatapahtuma, jonka summa on 1 500,00. 

Kun tapahtuma kirjataan, hankintatapahtuma luodaan ja kirjataan käyttöomaisuuserälle 123 sekä kirjaan B että kirjaan C summalla 1 500,00. Kun valmistelet ensisijaisen kirjan tapahtumia käyttöomaisuuden kirjauskansioon kirjaamista varten, voit tarkastella ja muokata myös johdettujen kirjojen tapahtumia. Jos valmistelet ensisijaisen kirjan tapahtumia toisessa kirjauskansiossa, et voi tarkastella johdettujen arvojen tapahtumia. Ne kirjataan määritetyille tileille ja määritettyihin kirjanpitotasoihin, kun ensisijaisen kirjan tapahtumat kirjataan.

> [!NOTE]                                                                                                                               
> Kirjat, joihin on määritetty tapahtumien kirjaus jollakin muulla aikavälillä kuin ensisijaisessa kirjassa, on liitettävä käyttöomaisuuserään erillisinä kirjoina, ei johdettuina kirjoina.  

Lisätietoja on kohdassa [Kirjaaminen johdetuissa kirjoissa](post-derived-value-models.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]