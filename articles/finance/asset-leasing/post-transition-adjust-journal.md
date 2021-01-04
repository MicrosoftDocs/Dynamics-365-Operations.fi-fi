---
title: Oikaisukirjauskansioviennit siirtymän jälkeen resurssin vuokrauksessa
description: Tässä ohjeaiheessa kerrotaan toiminnoista, joiden avulla vuokrauksen portfolio voidaan siirtää uusiin vuokrauksen kirjanpitostandardeihin, ASC 842:een ja IFRS 16:een.
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
ms.openlocfilehash: 4af7b9dc7a03a6d17ff34ffc726eb87e848dd785
ms.sourcegitcommit: f0f5545a8ff99583e0131f435d91c64bb68a1c38
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/30/2020
ms.locfileid: "4442984"
---
# <a name="post-transition-adjustment-journal-entries-in-asset-leasing"></a>Oikaisukirjauskansioviennit siirtymän jälkeen resurssin vuokrauksessa

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan toiminnoista, joiden avulla vuokrauksen portfolio voidaan siirtää uusiin vuokrauksen kirjanpitostandardeihin: ASC 842 (Accounting Standards Codification Topic 842), joka on US GAAP:n Yhdysvaltojen yleisti hyväksytty kirjanpitostardardi, ja IFRS 16 (International Financial Reporting Standard 16).

Lisätietoja kirjan määrittämisestä uusiin standardeihin siirtymistä varten on kohdassa [Vuokrasopimuskirjojen määrittäminen](set-up-lease-books.md).

Kun luot siirtymän oikaisukirjauskansioviennin, luodaan kirjauskansiovienti. Tämä vienti vaikuttaa taseeseen tallentamalla vuokrauksen tänä päivänä uusien standardien mukaan. Soveltuvaa resurssitiliä veloitetaan kyseisen päivän kirjanpitoarvon mukaan, ja velkatiliä hyvitetään. Ero veloitetaan jäljellä olevista tuotoista tai hyvitetään niille.

Voit kirjata siirtymän oikaisun uusien kirjanpitostandardien mukaan seuraavasti.

1. Valitse **Vuokrasopimusyhteenveto**-sivulla vuokrasopimus ja valitse sitten **Kirjat**.
2. Valitse kirjassa **Maksuaikataulu**.
3. Valitse **Maksuaikataulu**-valintaikkunassa **Vahvista**. Sulje sitten valintaikkuna.
4. Valitse **Siirtymän oikaisu**.

    > [!NOTE]
    > Siirtymän oikaisu voidaan luoda vain vuokrasopimuskirjoissa, jotka on liitetty kirjaan, jossa **Siirtymäkirja**-kenttä on käytettävissä. Jos **Vuokrauksen alkaminen** -kentän arvo on myöhempi kuin siirron päivämäärä, **Siirtymän oikaisu** -kentän arvoa ei päivitetä.

5. Jos haluat tarkastella kirjauskansiovientiä, valitse **Resurssin leasingkirjauskansiot**.
6. Valitse uusi kirjauskansio ja valitse sitten **Kirjaa**.
