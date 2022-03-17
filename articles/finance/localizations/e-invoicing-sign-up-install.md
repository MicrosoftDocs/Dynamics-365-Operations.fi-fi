---
title: Sähköisen laskutuspalvelun rekisteröityminen ja asentaminen
description: Tässä aiheessa on tietoja sähköisen laskutuspalvelun rekisteröimisestä ja asentamisesta.
author: dkalyuzh
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4ab16652e4a50dd71a5d0b2b49b4dd79e327f7a8
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371645"
---
# <a name="sign-up-for-and-install-the-electronic-invoicing-service"></a>Sähköisen laskutuspalvelun rekisteröityminen ja asentaminen

[!include [banner](../includes/banner.md)]

Tässä aiheessa on tietoja sähköisen laskutuspalvelun rekisteröimisestä ja asentamisesta. Tässä prosessissa on neljä vaihetta. Vaiheet 1–3 ovat pakollisia, ja vaihe 4 on valinnainen.

### <a name="step-1-sign-up-for-regulatory-configuration-service"></a>Vaihe 1: Rekisteröidy Regulatory Configuration Service -palveluun

Regulatory Configuration Services (RCS) tarjoaa määritys- ja suunnittelukokemuksen, jota käytetään sähköisen laskutuksen määrittämisessä. Resursseja, kuten ympäristöjä ja sähköistä laskutusta, luodaan, ylläpidetään ja hallitaan RCS:ssä. Kun resurssit ovat valmiita, ne julkaistaan sähköisen laskutuksen palvelussa.

Lisätietoja RCS:stä: [Regulatory Configuration Services (RCS) – globalisointitoiminnot](rcs-globalization-feature.md).

Voit rekisteröityä RCS-palveluun [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/) -sivulla.

### <a name="step-2-install-the-add-in-for-microservices-in-microsoft-dynamics-lifecycle-services"></a>Vaihe 2: Microservices-lisäosan asentaminen Microsoft Dynamics Lifecycle Servicesissa

Sähköinen laskutuspalvelu on joukko mikropalveluja, jotka sijaitsevat Microsoftin palvelinkeskuksissa. Oletusarvon mukaan Dynamics 365 Finance- ja Dynamics 365 Supply Chain Management -asiakkailla ei ole sähköisen laskutuksen palvelun käyttöoikeutta. Se on asennettava lisäosana Microsoft Dynamics Lifecycle Services (LCS) -palvelussa. Kun asennat lisäosan, Finance- tai Supply Chain Management -ympäristö rekisteröidään sovellusrekisteriin, jotka saavat muodostaa yhteyden sähköisen laskutuksen palveluun.

Lisätietoja tästä vaiheesta: [Microservices-lisäosan asentaminen Lifecycle Servicesissa](e-invoicing-install-add-in-microservices-lcs.md).

### <a name="step-3-set-up-rcs"></a>Vaihe 3: RCS:n määrittäminen

On määritettävä integrointi RCS:n ja sähköisen laskutuksen palvelun välillä. Pääkomponentit on myös määritettävä.

Tämän vaiheen ohjeet ovat kohdassa [Regulatory Configuration Servicen (RCS) määrittäminen](e-invoicing-set-up-rcs.md).

### <a name="step-4-microsoft-power-platform-plug-in-admin-reference"></a>Vaihe 4: Microsoft Power Platform -laajennuksen järjestelmänvalvojan viitetiedot

Jotkin skenaariot edellyttävät integrointia Dataversen kanssa Microsoft Power Platformiin liittyen.

Tämä asetus on tällä hetkellä pakollinen, jos käytät sähköisen laskutuksen ratkaisuja Indonesian sähköisen laskutuksen skenaarioihin. Se on kuitenkin valinnainen Saudi-Arabian sähköisen laskutuksen skenaariossa. Lisätietoja on kohdassa [Sähköisten laskutusominaisuuksien saatavuus maittain tai alueittain](e-invoicing-country-specific-availability.md).

Lisätietoja tämän vaiheen suorittamisesta on ohjeissa [Microsoft Power Platform -laajennuksen järjestelmänvalvojan viitetiedot](e-invoicing-power-platform-plug-in.md).
