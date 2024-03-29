---
title: Microservices-lisäosan asentaminen Lifecycle Servicesissa
description: Tässä artikkelissa käsitellään sähköisen laskutuksen lisäosan asentamista Microsoft Dynamics Lifecycle Servicesiin (LCS).
author: gionoder
ms.date: 02/11/2022
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
ms.openlocfilehash: 938b00192acc0ff5534239f2f280792471181fad
ms.sourcegitcommit: 1ecfc1d8afb2201ab895ae6f93304ba2b120f14b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/21/2022
ms.locfileid: "9710805"
---
# <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>Microservices-lisäosan asentaminen Lifecycle Servicesissa

[!include [banner](../includes/banner.md)]

Sähköisen laskutuksen palvelun todennus edellyttää, että Microsoft Dynamics 365 Finance- tai Dynamics 365 Supply Chain Management -ympäristö rekisteröidään palvelualustalle asentamalla ympäristöösi lisäosa Microsoft Dynamics Lifecycle Services (LCS) -palveluissa.

Rekisteröi ympäristö näiden ohjeiden avulla.

1. Kirjaudu LCS-tilille.
2. Valitse projektikoontinäytössä LCS-projekti.
2. Valitse projektissa **Ympäristö**-koontinäytössä valitse käyttöön otettu ympäristö. Valitun ympäristön on oltava käynnissä.
3. Valitse **Power Platform -integrointi** -välilehden **Ympäristön lisäosat** -osassa **Asenna uusi lisäosa**.
4. Valitse **Sähköinen laskutus**.
5. Syötä **AAD-sovelluksen tunnus** -kenttään kiinteä arvo **091c98b0-a1c9-4b02-b62c-7753395ccabe**. Tämä arvo on aina kiinteä. Varmista, että syötät vain yleisen yksilöivän tunnuksen (GUID). Älä sisällytä muita symboleja, kuten välilyöntejä, pilkkuja, pisteitä tai lainausmerkkejä.
6. Syötä **AAD-vuokraajatunnus**-kenttään Azure-tilaustilisi vuokraajan tunnus. Määrittämäsi Azure Active Directory (Azure AD) -vuokraajan on oltava sama kuin Regulatory Configuration Service (RCS) -palvelua varten käytetyn vuokraajan.
7. Lue ehdot ja valitse valintaruutu.
8. Valitse **Asenna**. Muutaman minuutin kuluttua tilan pitäisi muuttua tilasta **Asennetaan** tilaan **Asennettu**. Sivu on ehkä päivitettävä, ennen kuin muutos tulee näkyviin.

Sähköinen laskutus on nyt valmis käytettäväksi.

> [!NOTE]
> Yrityksillä on yleensä useita Finance- tai Supply Chain Management -ympäristöjä. Näitä ympäristöjä ovat tuotantoympäristöt, käyttäjän hyväksynnän testiympäristöt (UAT) sekä kehitysympäristöt (eristysympäristöt). Edellinen prosessi on suoritettava kaikille ympäristöille, jotka haluat yhdistää sähköiseen laskutukseen.
