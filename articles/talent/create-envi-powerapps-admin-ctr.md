---
title: "Ympäristöä ei voi luoda PowerAppsin hallintakeskuksessa"
description: "Tässä ohjeaiheessa kerrotaan, mitä voidaan tehdä, jos järjestelmänvalvoja ei voi luoda ympäristöä Microsoft PowerAppsin hallintakeskuksessa."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 6f9b7ceef6895b295e6ae5a50d8ac7970497efe5
ms.contentlocale: fi-fi
ms.lasthandoff: 12/04/2018

---

# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a>Ympäristöä ei voi luoda PowerAppsin hallintakeskuksessa

[!include [banner](includes/banner.md)]

**Ongelma**

- Vuokraajan tai ympäristön järjestelmänvalvoja ei voi luoda ympäristöä Microsoft PowerAppsin hallintakeskuksessa.
- Tätä vaihetta suorittavalle käyttäjälle ei ole määritetty suoraan käyttöoikeutta, jonka antaa käyttäjille oikeuden suorittaa ympäristön luontivaiheen.

**Ratkaisu**

Varmista, että vuokraajan järjestelmänvalvoja on määrittänyt kelvollisen PowerApps P2 -käyttöoikeuden käyttäjälle, joka suorittaa ympäristön luontivaiheen. Tämä oikeus on seuraavissa Microsoft Dynamics -palvelusopimuksissa.

| Tuotteen varastointiyksikkö (SKU)       | PowerApps P2 -palvelusopimus  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | PowerApps for Dynamics 365 |
| Microsoft Dynamics 365 Plan Enterprise Edition | PowerApps for Dynamics 365 |

Huomaa, että myös monet Microsoft Officen varastointiyksikötsisältävät tämän oikeuden itsenäisen PowerApps-palvelupaketin 2 varastointiyksiköiden lisäksi. Olennaista on, että jokin näistä varastointiyksiköistä on käytössä.

1. Siirry osoitteeseen [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Luo ympäristöjä noudattamalla ohjeita kohdassa [Talentin valmistelu](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).

