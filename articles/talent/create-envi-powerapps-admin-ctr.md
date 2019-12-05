---
title: Power Apps-hallintakeskuksessa ei voi luoda ympäristöä
description: Tässä ohjeaiheessa kerrotaan, mitä voidaan tehdä, jos järjestelmänvalvoja ei voi luoda ympäristöä Microsoft Power Appsin hallintakeskuksessa.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5923c59ab5dde13fed0483972e76634031404fd8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773216"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Power Apps-hallintakeskuksessa ei voi luoda ympäristöä

[!include [banner](includes/banner.md)]

**Lähetä**

- Vuokraajan tai ympäristön järjestelmänvalvoja ei voi luoda ympäristöä Microsoft Power Appsin hallintakeskuksessa.
- Tätä vaihetta suorittavalle käyttäjälle ei ole määritetty suoraan käyttöoikeutta, jonka antaa käyttäjille oikeuden suorittaa ympäristön luontivaiheen.

**Ratkaisu**

Varmista, että vuokraajan järjestelmänvalvoja on määrittänyt kelvollisen Power Apps P2 -käyttöoikeuden käyttäjälle, joka suorittaa ympäristön luontivaiheen. Tämä oikeus on seuraavissa Microsoft Dynamics -palvelusopimuksissa.

| Tuotteen varastointiyksikkö (SKU)       | Power Apps P2 -huoltosuunnitelma  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | Power Apps for Dynamics 365 |
| Microsoft Dynamics 365 Enterprise Edition -palvelupaketti | Power Apps for Dynamics 365 |

Huomaa, että myös monet Microsoft Officen varastointiyksiköt sisältävät tämän oikeuden itsenäisen Power Apps-palvelupaketin 2 varastointiyksiköiden lisäksi. Olennaista on, että jokin näistä varastointiyksiköistä on käytössä.

1. Siirry osoitteeseen [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Luo ympäristöjä noudattamalla ohjeita kohdassa [Talentin valmistelu](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).
