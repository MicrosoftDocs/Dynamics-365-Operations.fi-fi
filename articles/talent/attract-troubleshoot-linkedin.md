---
title: LinkedInin ja Microsoft Dynamics 365 Talent – Attractin integroinnin vianmääritys
description: Tässä ohjeaiheessa käsitellään sellaisten ongelmien vianmääritystä, jotka koskevat työpaikkojen julkaisua LinkedIniin Microsoft Dynamics 365 Talent – Attractista.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: b031fd95d2e7fc8405ad96139779091e00bb4d46
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551469"
---
# <a name="troubleshoot-integration-with-linkedin-and-microsoft-dynamics-365-talent---attract"></a>LinkedInin ja Microsoft Dynamics 365 Talent – Attractin integroinnin vianmääritys

[!include [banner](../includes/banner.md)]

Tee seuraavien tietojen avulla sellaisten ongelmien vianmääritys, joita voi esiintyä, kun yrität julkaista työpaikkoja LinkedIniin Microsoft Dynamics 365 Talent: Attractista.

## <a name="you-cant-sign-in-to-linkedin-from-attract"></a>Kirjautuminen LinkedIniin Attractista ei onnistu

Jos kirjautumisessa LinkedIniin Attractista on ongelmia, yritä seuraavia toimenpiteitä:

1. Varmista, että LinkedIn-tunnistetiedot, jotka olet määrittänyt Attractissa, ovat voimassa ja oikeat.
2. Jos tunnistetiedot ovat voimassa ja oikein, ota yhteyttä [LinkedInin tukeen](https://www.linkedin.com/help/linkedin).
3. Jos ongelma ei ratkea, ota yhteyttä [Microsoftin tukeen](./talent-support.md).

## <a name="job-posts-from-attract-dont-appear-on-linkedin"></a>Attractista julkaistut työpaikat eivät näy LinkedInissä

Jos työpaikka ei näy LinkedInissä 24 tunnin jälkeen, kokeile seuraavia toimenpiteitä:

1. Varmista, että LinkedIn-yritystunnus yhdistetään LinkedIn-yrityssivulle ja että se on annettu oikein Attractin hallintakeskukseen. Lisätietoja LinkedIn-asetusten muuttamisesta hallintakeskuksessa on kohdassa [LinkedIn-integraation määrittäminen](attract-admin-linkedin.md). Lisätietoja LinkedIn-yritystunnuksista on kohdassa [LinkedIn-yritystunnuksen liittäminen LinkedIn-työpaikkailmoitussivulle – usein kysyttyjä kysymyksiä](https://www.linkedin.com/help/linkedin/answer/98972).
2. Tarkista työpaikan tiedot LinkedInissä ja varmista, että osoite on täydellinen. Työpaikan onnistunut julkaisu edellyttää, että LinkedInissä on ainakin työpaikan kaupunki ja maa tai alue.
3. Varmista, että työpaikka ei ole toisen LinkedInissä julkaistun työpaikan kaksoiskappale. LinkedIn ei julkaise työpaikkoja, jotka ovat toisen rekrytoijan LinkedInin Premium-työpaikkojen tai rajoitettujen listausten kaksoiskappaleita. Varmista, ettei joku muu yrityksen työntekijä ole jo julkaissut työpaikkaa manuaalisesti.

## <a name="see-also"></a>Lisätietoja

[LinkedInin usein kysytyt kysymykset](./attract-linkedin-faq.md)

[Työpaikkojen julkaiseminen LinkedInissä Attractista](./attract-post-jobs-to-linkedin.md)

[Ehdokkaiden rekrytointi LinkedIn Recruiter -ratkaisulla](./attract-linkedin-recruiter.md)

[Työpaikkojen luominen](./creating-jobs-attract.md)

[LinkedIn-integraation vianmääritys](./attract-troubleshoot-linkedin.md)
