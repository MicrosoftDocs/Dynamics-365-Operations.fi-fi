---
title: Ympäristöä ei voi luoda PowerAppsin hallintakeskuksessa
description: Tässä ohjeaiheessa kerrotaan, mitä voidaan tehdä, jos järjestelmänvalvoja ei voi luoda ympäristöä Microsoft PowerAppsin hallintakeskuksessa.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6f9b7ceef6895b295e6ae5a50d8ac7970497efe5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "304265"
---
# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a>PowerApps-hallintakeskuksessa ei voi luoda ympäristöä

[!include [banner](includes/banner.md)]

**Ongelma**

- Vuokraajan tai ympäristön järjestelmänvalvoja ei voi luoda ympäristöä Microsoft PowerAppsin hallintakeskuksessa.
- Tätä vaihetta suorittavalle käyttäjälle ei ole määritetty suoraan käyttöoikeutta, jonka antaa käyttäjille oikeuden suorittaa ympäristön luontivaiheen.

**Ratkaisu**

Varmista, että vuokraajan järjestelmänvalvoja on määrittänyt kelvollisen PowerApps P2 -käyttöoikeuden käyttäjälle, joka suorittaa ympäristön luontivaiheen. Tämä oikeus on seuraavissa Microsoft Dynamics -palvelusopimuksissa.

| Tuotteen varastointiyksikkö (SKU)       | PowerApps P2 -palvelusopimus  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | PowerApps for Dynamics 365 |
| Microsoft Dynamics 365 Enterprise Edition -palvelupaketti | PowerApps for Dynamics 365 |

Huomaa, että myös monet Microsoft Officen varastointiyksiköt sisältävät tämän oikeuden itsenäisen PowerApps-palvelupaketin 2 varastointiyksiköiden lisäksi. Olennaista on, että jokin näistä varastointiyksiköistä on käytössä.

1. Siirry osoitteeseen [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Luo ympäristöjä noudattamalla ohjeita kohdassa [Talentin valmistelu](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).
