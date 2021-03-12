---
title: Varaston asetusten vianmääritys
description: Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun varastoja määritetään Microsoft Dynamics 365 Supply Chain Managementissa.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6f26144b03fb4d2130c1ed7fe3db2411384b9ff6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970178"
---
# <a name="troubleshoot-warehouse-setup"></a>Varaston asetusten vianmääritys

[!include [banner](../includes/banner.md)]

Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun varastoja määritetään Microsoft Dynamics 365 Supply Chain Managementissa.

## <a name="i-cant-use-any-role-except-administrator-to-access-the-mobile-device-app-emulator"></a>Mobiililaitteen sovelluksen emulaattoria voi käyttää vain, kun roolina on järjestelmänvalvoja.

### <a name="issue-description"></a>Ongelman kuvaus

Järjestelmänvalvojan rooli on ainoa, jolla mobiililaitteen sovelluksen emulaattoria voi käyttää.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Mobiililaitteen sovelluksen emulaattori on määritetty käytettäväksi vain järjestelmänvalvojan tilillä. Testausta ja julkistamisprosessia varten kannattaa käyttää varsinaista varastosovellusta.
