---
title: (ER) Konfiguraatioiden tuonti RCS:stä
description: Tässä ohjeaiheessa on tietoja tavasta, jolla käyttäjä voi tuoda ER-konfiguraation uuden version RCS:stä.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 799abeafe5f0929e6dd2f8a5f437f3c10b3b06d9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570533"
---
# <a name="er-import-configurations-from-rcs"></a>(ER) Konfiguraatioiden tuonti RCS:stä

[!include [banner](../../includes/banner.md)]

Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi tuoda uuden sähköisen raportoinnin (ER) konfiguraation version Microsoft Regulatory Configuration Servicesista (RCS). Tässä esimerkissä voit valita RCS-esiintymässä määritetyn ER-konfiguraation version ja tuoda sen malliyrityksen Litware, Inc:n nykyiseen esiintymään. Nämä vaiheet voidaan suorittaa mille tahansa yritykselle, koska yritykset jakavat ER-konfiguraatiot. Näitä vaiheita varten on ensin suoritettava ohjeaiheessa [Konfigurointipalvelujen luominen ja merkitseminen aktiivisiksi](er-configuration-provider-mark-it-active-2016-11.md) käsitellyt vaiheet. Näiden vaiheiden suorittamista varten tarvitset sen RCS-esiintymän käyttöoikeuden, jossa on vähintään yksi ER-konfiguraatio joko **Valmis**- tai **Jaettu**-tilassa.

1. Valitse **Organisaation hallinto** > **Työtilat** > **Sähköinen raportointi**. 
2. Varmista, että Litware, Inc. -malliyrityksen konfiguraation lähde on käytettävissä ja merkitty **aktiiviseksi**. Jos konfiguraation lähde ei ole näkyvissä, suorita ohjeaiheen [Konfiguraation lähteiden luominen ja merkitseminen aktiivisiksi](er-configuration-provider-mark-it-active-2016-11.md) vaiheet. 
3. Jos yritykseen ei ole valmisteltu RCS-ympäristöä, valitse ulkoinen **Regulatory Services – määritys** -linkki ja valmistele RCS-ympäristö ohjeiden mukaisesti. 
4. Valitse **Sähköisen raportoinnin parametrit**. 
5. Valitse **RCS**-välilehti. 
6. Jos yrityksessä on jo valmisteltu RCS-ympäristö, käytä sitä sivun URL-osoitteiden avulla. 
7. Sulje sivu. 

## <a name="register-a-new-er-repository"></a>Rekisteröi uusi ER-säilö. 
1. Merkitse valittu rivi luettelossa. 
2. Valitse lähteeksi Litware, Inc. 
3. Valitse Säilöt. 
4. Avaa valintaikkuna valitsemalla Lisää. 
5. Syötä Konfiguraatiosäilön tyyppi -kentän arvoksi RCS. 
6. Valitse Luo säilö. 
7. Anna tai valitse arvo RCS-ympäristön näyttönimen kentässä. 
8. Valitse haluamasi RCS-esiintymä. Niitä voi olla useita. 
9. Valitse OK. 

## <a name="import-er-configurations-from-rcs-based-repository"></a>ER-konfiguraatioiden tuominen RCS-pohjaisesta säiliöstä
1. Valitse **Näytä suodattimet**. 
2. Anna **Nimi**-kenttään suodatusarvoksi RCS käyttämällä **sisältää**-suodatinoperaattoria. 
3. Kun avaat valitun säilön, valitse **Yhdistä Regulatory Configuration Servicesiin** -sivulla **Muodosta yhteys Regulatory Configuration Servicesiin valitsemalla tämä** -linkki. 
4. Valitse **Avaa**. 
5. Valitse **Sulje**. 
6. Valitse sopiva ER-konfiguraation versio ja tuo se nykyiseen esiintymään valitsemalla **Tuo**.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]