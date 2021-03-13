---
title: Power Apps-hallintakeskuksessa ei voi luoda ympäristöä
description: Tässä artikkelissa kerrotaan, mitä voidaan tehdä, jos järjestelmänvalvoja ei voi luoda ympäristöä Microsoft Power Appsin hallintakeskuksessa.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 664c644c9b34e3489b4134040e165d26202dbd38
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112373"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Power Apps-hallintakeskuksessa ei voi luoda ympäristöä

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
2. Luo ympäristöjä noudattamalla ohjeita kohdassa [Human Resourcesin valmistelu](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).
