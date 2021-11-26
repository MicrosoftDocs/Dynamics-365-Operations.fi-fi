---
title: Käänteinen kirjauskansion kirjaus
description: Tässä aiheessa kuvataan ominaisuuksia, joiden avulla voit muuttaa tositteita käänteisiksi tositetapahtumien luettelosta tai talouskirjauskansioista.
author: kweekley
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: roschloma
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb1615312e9fd1786a5a0050dda3e9e9b20fe710
ms.sourcegitcommit: 408786b164b44bee4e16ae7c3d956034d54c3f80
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/05/2021
ms.locfileid: "7753775"
---
# <a name="reverse-journal-posting"></a>Käänteinen kirjauskansion kirjaus

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan Microsoft Dynamics 365 Finance -ominaisuuksia, joiden avulla voit muuttaa koko kirjauskansion tai yhden tai useamman tositteen käänteiseksi tositetapahtumien luettelosta riippumatta niiden alkuperästä. 

Ennen jonkin tässä aiheessa käsitellyn toiminnon käyttöä se on otettava käyttöön järjestelmässä. Järjestelmänvalvojat voivat käyttää **Toimintojen hallinnan** työtilaa tarkistaakseen toiminnon tilan sekä laittaa sen päälle, jos sitä vaaditaan. Tässä tapauksessa toiminto näkyy seuraavalla tavalla:
 - Moduuli: Kirjanpito
 - Ominaisuuden nimi: **Useiden asiakirjojen joukkoperuutus**

## <a name="reversing-journals"></a>Kirjauskansioiden muuttaminen käänteiseksi

Voit muuttaa kirjauskansion rivejä käänteisiksi yksittäin. Käänteisen kirjauskansion kirjauksen avulla voit myös muuttaa koko talouskirjauskansion käänteiseksi. Kirjauskansion muuttaminen käänteiseksi: 

- Suodata kirjattuja kirjauskansioita ja avaa kirjauskansion **Rivit**-näkymä.
- Valitse **Käänteinen**-valikko sivun ylälaidasta.
- Näet tositteiden ja tositerivien kokonaismäärän sekä käänteiseksi muunnettavien rivien kokonaissumman.
- Valitse **Kyllä** käyttääksesi olemassa olevia tapahtumapäiviä tai **Ei** luodaksesi uuden. Joissakin tapauksissa alkuperäisen tapahtuman ajanjakso voi olla suljettu, ja sinun on syötettävä uusi tapahtumapäivä käänteiseksi muuttamista varten.
- Jos valitsit **Ei**, syötä tapahtumapäivä käänteiseksi muutamista varten. 
- Kirjoita kommentti, jonka haluat lisätä käänteiseksi muuttamisen tapahtumaan.
- Valitse **Käänteinen**-painike.

Tapahtumat muutetaan käänteisiksi. 

Jos tositteessa on yli 100 riviä, käänteiseksi muuttamisen prosessi suoritetaan eräkäsittelyn avulla. Voit tarkistaa tulokset lukemalla erätyön kommentit. Tapahtumat, joita ei voitu muuttaa käänteiseksi, luetellaan erätyön historiassa.

Jos tositteessa on enintään 100 riviä, käänteiseksi muuttamisen prosessi suoritetaan heti. Tulokset esitetään valintaikkunassa. Näet kaikki tositteet, joita ei voi muuttaa käänteiseksi, sekä epäonnistumisen syyn. Sulje valintaikkuna valitsemalla **OK**.

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a>Tositteiden muuttaminen käänteiseksi tositetapahtumien luettelosta. 

Voit muuttaa tositteita käänteisiksi myös minkä tahansa alareskontran **tositetapahtumien luettelosta**. Lisäksi voit muuntaa useita tositteita käänteisiksi kerralla. 

Yhden tai usean tositteen muuttaminen käänteiseksi: 

- Valitse **Peruuta koko kirjauskansio** -pudotusvalikko sivun ylälaidasta.
- Näet tositteiden ja tositerivien kokonaismäärän sekä käänteiseksi muunnettavien rivien kokonaissumman.
- Valitse **Kyllä** käyttääksesi olemassa olevia tapahtumapäiviä tai **Ei** luodaksesi uuden. Joissakin tapauksissa alkuperäisen tapahtuman ajanjakso voi olla suljettu, ja sinun on syötettävä uusi tapahtumapäivä käänteiseksi muuttamista varten.
- Jos valitsit **Ei**, syötä tapahtumapäivä käänteiseksi muutamista varten. 
- Kirjoita kommentti kuvaamaan käänteiseksi muuttamisen tapahtumaa.
- Valitse **Käänteinen**-painike.

Tapahtumat muutetaan käänteisiksi. 

Jos tositerivejä on yli 100, käänteiseksi muuttamisen prosessi suoritetaan eräkäsittelyn avulla. Voit tarkistaa tulokset lukemalla erätyön kommentit. Tapahtumat, joita ei voitu muuttaa käänteiseksi, luetellaan erätyön historiassa.

Jos tositteessa on enintään 100 riviä, käänteiseksi muuttamisen prosessi suoritetaan heti. Tulokset esitetään valintaikkunassa. Näet kaikki tositteet, joita ei voitu muuttaa käänteiseksi, sekä epäonnistumisen syyn. Sulje valintaikkuna valitsemalla **OK**.

Tapahtumia voidaan muuttaa käänteiseksi vain, jos ne täyttävät käänteiseksi muuttamisen liiketoimintasäännöt. Toimittajamaksuja ei voida muuttaa käänteiseksi tässä aiheessa kuvatulla tavalla. Toimittajamaksut on muutettava käänteiseksi kohdassa [Toimittajamaksun käänteiseksi muuttaminen](../accounts-payable/reverse-vendor-payment.md) esitetyllä tavalla.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
