---
title: Microservices-lisäosan asentaminen Lifecycle Servicesissa
description: Tässä ohjeaiheessa käsitellään sähköisen laskutuksen lisäosan asentamista Microsoft Dynamics Lifecycle Servicesiin (LCS).
author: dkalyuzh
ms.date: 02/11/2022
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
ms.openlocfilehash: a575f3e26489607dc2143ba05c941240969a0feb
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371718"
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
5. Kirjoita **AAD-sovellustunnus**-kenttään **091c98b0-a1c9-4b02-b62c-7753395ccabe**. Tämä arvo on kiinteä arvo. Varmista, että syötät vain yleisen yksilöivän tunnuksen (GUID). Älä sisällytä muita symboleja, kuten välilyöntejä, pilkkuja, pisteitä tai lainausmerkkejä.
6. Syötä **AAD-vuokraajatunnus**-kenttään Azure-tilaustilisi vuokraajan tunnus. Määrittämäsi Azure Active Directory (Azure AD) -vuokraajan on oltava sama kuin Regulatory Configuration Service (RCS) -palvelua varten käytetyn vuokraajan.
7. Lue ehdot ja valitse valintaruutu.
8. Valitse **Asenna**. Muutaman minuutin kuluttua tilan pitäisi muuttua tilasta **Asennetaan** tilaan **Asennettu**. Sivu on ehkä päivitettävä, ennen kuin muutos tulee näkyviin.

Sähköinen laskutus on nyt valmis käytettäväksi.

> [!NOTE]
> Yrityksillä on yleensä useita Finance- tai Supply Chain Management -ympäristöjä. Näitä ympäristöjä ovat tuotantoympäristöt, käyttäjän hyväksynnän testiympäristöt (UAT) sekä kehitysympäristöt (eristysympäristöt). Edellinen prosessi on suoritettava kaikille ympäristöille, jotka haluat yhdistää sähköiseen laskutukseen.
