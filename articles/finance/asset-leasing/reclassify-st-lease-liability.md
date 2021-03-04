---
title: Lyhytaikaisen vuokrasopimusvelan osan uudelleenluokitteleminen
description: Tässä ohjeaiheessa selitetään, miten voit luoda kuukausittaisen kirjauskansion, jonka avulla voit luokitella vuokrasopimusvelan lyhytaikaiseksi.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 46bcd396c93bc1d2944241165d438f8ccc013e20
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442962"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a>Lyhytaikaisen vuokrasopimusvelan osan uudelleenluokitteleminen

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa selitetään, miten voit luoda kuukausittaisen kirjauskansion, jonka avulla voit luokitella vuokrasopimusvelan lyhytaikaiseksi. Kun aikataulu, joka on valittu eräprosessissa, on **Lyhytaikaisen vuokrasopimusvelan uudelleenluokittelu**, kirjauskansiovienti luodaan. Tätä vientiä käytetään kirjattaessa vuokrasopimusvelan nykyinen osa kuukauden viimeisenä päivänä. Samaan aikaan palautusvienti kirjataan seuraavan kuukauden ensimmäisestä päivästä alkaen.

Vuokrasopimusvelan lyhytaikainen osa näkyy velan kuoletusaikataulussa. Kun kirjauskansiovienti kirjataan, **Velan uudelleenluokituskirjauskansio luotu** -sarake tulee käyttöön ja kirjauskansion tunnus täytetään aikataulussa.

Voit luoda ja kirjata lyhytaikaisen velan uudelleenluokituskirjauskansioviennin seuraavasti.

1. Siirry kohtaan **Resurssin vuokraus \> Kausittainen \> Eräkirjauskansion luominen**.
2. Valitse **Eräkirjauskansion luominen** -valintaikkunan **Valitse aikataulu** -kentässä **Lyhytaikaisen vuokrasopimusvelan uudelleenluokittelu**.
3. Valitse **Vuokraryhmä**-kentässä vuokraryhmä. Voit myös valita kirjan tunnuksen **Kirjan tunnus** -kentässä.
4. Ota käyttöön **Kirjaa**-parametri. Vaihtoehtoisesti voit jättää tämän parametrin pois käytöstä, jos vienti luotava mutta ei kirjattava.
5. Ota käyttöön **Esikatselu ennen kirjaamista** -parametri, jos haluat tarkastella vientiä ennen sen kirjaamista.
6. Valitse **OK**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]