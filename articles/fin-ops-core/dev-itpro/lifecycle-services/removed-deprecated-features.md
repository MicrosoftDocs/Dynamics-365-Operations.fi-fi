---
title: Lifecycle Servicesin (LCS) poistetut tai vanhentuneet ominaisuudet
description: Tässä ohjeaiheessa käsitellään ominaisuuksia, jotka on poistettu tai joiden poistoa suunnitellaan Microsoft Dynamics Lifecycle Servicesistä (LCS).
author: AngelMarshall
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e583ec66f24940f44113433042f5e2340cf0f52c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748436"
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
<td>Vanhentunut: vuokakaavioiden osaa BPM:ssä odotetaan poistettavaksi vuonna 2020. Seuraavat toiminnot eivät ole käytettävissä:
<ul>
<li>Kaikki vuokaaviot ovat vain luku -muotoisia eikä niitä voi muokata. Myöskään vuokaaviotehtäviin liitetyt muodon ominaisuudet eivät ole käytettävissä. Nämä vuokaaviot sisältävät sekä oletusarvoiset vuokaaviot, jotka luodaan automaattisesti, että mukautettuja vuokaavioita, joita muokataan näiden oletusarvoisten vuokaavioiden perusteella.</li>
<li>Prosessivaiheet ovat vain luku -muotoisia eikä niitä voi muokata.</li>     
<li>Vanha sovitus/aukkoanalyysiominaisuus ei ole käytettävissä. Tämän vuoksi väliluetteloa ei luoda automaattisesti eikä se ole käytettävissä vientiä varten.
<p><strong>Huomautus:</strong> Tämä ominaisuus on aiemmin vanhentunut ja korvattu Microsoft Azure DevOps-integraatiolla.</p>
</li>
<li>Vuokaavion versiohistoria ei ole käytettävissä.</li>
</ul>
</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]