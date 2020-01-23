---
title: Lifecycle Servicesin (LCS) poistetut tai vanhentuneet ominaisuudet
description: Tässä ohjeaiheessa käsitellään ominaisuuksia, jotka on poistettu tai joiden poistoa suunnitellaan Microsoft Dynamics Lifecycle Servicesistä (LCS).
author: sericks007
manager: AnnBe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c792d06e9b0aa42919de924bdcc9118358779b72
ms.sourcegitcommit: 75bbcff474cfb8d2f282be2b9d2d7984d1505fa3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/03/2019
ms.locfileid: "2885452"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a>Lifecycle Servicesin (LCS) poistetut tai vanhentuneet ominaisuudet

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään Microsoft Dynamics Lifecycle Servicesin (LCS) ominaisuuksia, jotka on poistettu tai jotka ovat vanhentuneita.

- *Poistettu* ominaisuus ei ole enää käytettävissä palvelussa.
- *Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.

Tämän luettelon avulla voit ottaa huomioon nämä poistuneet ja vanhentuneet ominaisuudet omassa suunnittelussasi.

## <a name="october-2019-announcements"></a>Lokakuu 2019 ilmoitukset

### <a name="flowchart-diagrams-in-business-process-modeler"></a>Liiketoimintaprosessien mallintajan vuokaaviot

<table>
<tbody>
<tr>
<td><strong>Poiston tai vanhentumisen syy</strong></td>
<td>Olemme poistamassa vuokaavioiden komponentin liiketoimintaprosessien mallintaja (BPM)-osassa, koska vanha muotoilu aiheutti vähäisen käytön.</td>
</tr>
<tr>
<td><strong>Onko toinen ominaisuus korvannut?</strong></td>
<td>Ei</td>
</tr>
<tr>
<td><strong>Alueet, joihin avain vaikuttaa</strong></td>
<td>Liiketoimintaprosessien mallintaja</td>
</tr>
<tr>
<td><strong>Tila</strong></td>
<td>Vanhentunut: vuokakaavioiden osaa BPM:ssä odotetaan poistettavaksi helmikuun alussa 2020. Seuraavat toiminnallisuudet poistetaan:
<ul>
<li>Aiemmin luodut vuokaaviot eivät ole käytettävissä tarkastelua tai muokkaamista varten. Myös vuokaaviotoimintoihin liittyvät muodon ominaisuudet eivät ole käytettävissä, koska koko <strong>vuokaavio</strong>-välilehti poistetaan. Nämä vuokaaviot sisältävät sekä oletusarvoiset vuokaaviot, jotka luodaan automaattisesti, että mukautettuja vuokaavioita, joita muokataan näiden oletusarvoisten vuokaavioiden perusteella.</li>
<li>Vanha sovitus/aukkoanalyysiominaisuus ei ole käytettävissä. Tämän vuoksi väliluetteloa ei luoda automaattisesti eikä se ole käytettävissä vientiä varten.
<p><strong>Huomautus:</strong> Tämä ominaisuus on aiemmin vanhentunut ja korvattu Microsoft Azure DevOps-integraatiolla.</p>
</li>
<li>Vuokaavion versiohistoria ei ole käytettävissä.</li>
</ul>
</td>
</tr>
</tbody>
</table>
