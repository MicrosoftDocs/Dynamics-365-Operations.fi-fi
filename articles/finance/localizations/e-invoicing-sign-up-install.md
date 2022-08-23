---
title: Sähköisen laskutuspalvelun rekisteröityminen ja asentaminen
description: Tässä artikkelissa on tietoja sähköisen laskutuspalvelun rekisteröimisestä ja asentamisesta.
author: gionoder
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 99f484e5ab8821c78fde776a9d3195dade2a09d5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283954"
---
# <a name="sign-up-for-and-install-the-electronic-invoicing-service"></a>Sähköisen laskutuspalvelun rekisteröityminen ja asentaminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja sähköisen laskutuspalvelun rekisteröimisestä ja asentamisesta. Tässä prosessissa on neljä vaihetta. Vaiheet 1–3 ovat pakollisia, ja vaihe 4 on valinnainen.

### <a name="step-1-sign-up-for-regulatory-configuration-service"></a>Vaihe 1: Rekisteröidy Regulatory Configuration Service -palveluun

Regulatory Configuration Services (RCS) tarjoaa määritys- ja suunnittelukokemuksen, jota käytetään sähköisen laskutuksen määrittämisessä. Resursseja, kuten ympäristöjä ja sähköistä laskutusta, luodaan, ylläpidetään ja hallitaan RCS:ssä. Kun resurssit ovat valmiita, ne julkaistaan sähköisen laskutuksen palvelussa.

Lisätietoja RCS:stä: [Regulatory Configuration Services (RCS) – globalisointitoiminnot](rcs-globalization-feature.md).

Voit rekisteröityä RCS-palveluun [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/) -sivulla.

### <a name="step-2-install-the-add-in-for-microservices-in-microsoft-dynamics-lifecycle-services"></a>Vaihe 2: Microservices-lisäosan asentaminen Microsoft Dynamics Lifecycle Servicesissa

Sähköinen laskutuspalvelu on joukko mikropalveluja, jotka sijaitsevat Microsoftin palvelinkeskuksissa. Oletusarvoisesti Dynamics 365 Financen ja Dynamics 365 Supply Chain Managementin asiakkailla ei ole sähköisen laskutuksen palvelun käyttöoikeutta. Se on asennettava lisäosana Microsoft Dynamics Lifecycle Services (LCS) -palvelussa. Kun asennat lisäosan, Finance- tai Supply Chain Management -ympäristö rekisteröidään sovellusrekisteriin, jotka saavat muodostaa yhteyden sähköisen laskutuksen palveluun.

Lisätietoja tästä vaiheesta: [Microservices-lisäosan asentaminen Lifecycle Servicesissa](e-invoicing-install-add-in-microservices-lcs.md).

### <a name="step-3-set-up-rcs"></a>Vaihe 3: RCS:n määrittäminen

On määritettävä integrointi RCS:n ja sähköisen laskutuksen palvelun välillä. Pääkomponentit on myös määritettävä.

Tämän vaiheen ohjeet ovat kohdassa [Regulatory Configuration Servicen (RCS) määrittäminen](e-invoicing-set-up-rcs.md).

### <a name="step-4-microsoft-power-platform-plug-in-admin-reference"></a>Vaihe 4: Microsoft Power Platform -laajennuksen järjestelmänvalvojan viitetiedot

Jotkin skenaariot edellyttävät integrointia Dataversen kanssa Microsoft Power Platformiin liittyen.

Tämä asetus on tällä hetkellä pakollinen, jos käytät sähköisen laskutuksen ratkaisuja Indonesian sähköisen laskutuksen skenaarioihin. Se on kuitenkin valinnainen Saudi-Arabian sähköisen laskutuksen skenaariossa. Lisätietoja on kohdassa [Sähköisten laskutusominaisuuksien saatavuus maittain tai alueittain](e-invoicing-country-specific-availability.md).

Lisätietoja tämän vaiheen suorittamisesta on ohjeissa [Microsoft Power Platform -laajennuksen järjestelmänvalvojan viitetiedot](e-invoicing-power-platform-plug-in.md).
