---
title: Konsernin sisäisten myyntilaskujen maksujen rekisteröiminen automaattisesti
description: Tässä artikkelissa käsitellään konsernin sisäisten myyntilaskujen maksujen automaattista rekisteröintiä
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 4e8f784cd310026f0a647a0f509999e11ab26ce5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878784"
---
# <a name="register-payments-automatically-for-intercompany-customer-invoices"></a>Konsernin sisäisten myyntilaskujen maksujen rekisteröiminen automaattisesti

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management luo asiakastapahtuman, kun konsernin sisäinen myyntilasku kirjataan. Tämä asiakastapahtuma jää avoimeksi siihen saakka, että se selvitetään eli maksetaan. Kun vastaavan konsernin sisäisen ostotilauksen lasku päivitetään, asiakastapahtumaa vastaava toimittajatapahtuma luodaan. Myös tämä toimittajatapahtuma jää avoimeksi siihen saakka, että se selvitetään. Erojen välttämiseksi myyntireskontran maksukirjauskansio voidaan luoda ja kirjata automaattisesti, kun myyntireskontran maksukirjauskansio kirjataan.

1. Valitse **Myynti ja markkinointi \> Asiakkaat \> Kaikki asiakkaat**.
1. Valitse toimintoruudun **Yleiset**-välilehdessä **Konsernin sisäinen**.
1. Konsernin sisäiset myyntireskontramaksut määritetään myyntitilausten **Konsernin sisäinen** -sivulla, valitsemalla **Myyntitilauskäytännöt**-linkki.
1. **Maksukirjauskansio**-kentässä valitaan se myyntireskontran maksukirjauskansio, johon konsernin sisäiset toimittajamaksut halutaan rekisteröidä. Se määritetään **Myyntireskontran parametrit** -sivulla.
1. Jos kirjaus tähän kirjauskansioon halutaan tehdä automaattisesti, **Kirjaa kirjauskansioon automaattisesti** -valintaruutu on valittava.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
