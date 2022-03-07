---
title: Power Apps-hallintakeskuksessa ei voi luoda ympäristöä
description: Tässä ohjeaiheessa kerrotaan, mitä voidaan tehdä, jos järjestelmänvalvoja ei voi luoda ympäristöä Microsoft Power Appsin hallintakeskuksessa.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 937b372fa95c8076666aed14c2b34b12e8029c4d
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067701"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Power Apps-hallintakeskuksessa ei voi luoda ympäristöä


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Lähetä**

- Vuokraajan tai ympäristön järjestelmänvalvoja ei voi luoda ympäristöä Microsoft Power Appsin hallintakeskuksessa.
- Käyttäjällä ei ole käyttöoikeutta luoda ympäristöjä.

**Ratkaisu**

Varmista, että vuokraajan järjestelmänvalvoja on määrittänyt ympäristöä luovalle käyttäjälle kelvollisen Power Apps P2 -käyttöoikeuden. Seuraavissa Microsoft Dynamics -palvelusuunnitelmissa on mukana oikeudet luoda ympäristöjä:

| Tuotteen varastointiyksikkö (SKU)       | Power Apps P2 -huoltosuunnitelma  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | Power Apps for Dynamics 365 |
| Microsoft Dynamics 365 Enterprise Edition -palvelupaketti | Power Apps for Dynamics 365 |

Huomaa, että myös monet Microsoft Officen varastointiyksiköt sisältävät tämän oikeuden itsenäisen Power Apps-palvelupaketin 2 varastointiyksiköiden lisäksi. Olennaista on, että jokin näistä varastointiyksiköistä on käytössä.

1. Siirry osoitteeseen [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Luo ympäristöjä noudattamalla ohjeita kohdassa [Human Resourcesin valmistelu](/dynamics365/unified-operations/talent/provisioning-talent).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
