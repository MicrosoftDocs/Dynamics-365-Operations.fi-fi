---
title: Dynamics 365 Human Resources -infrastruktuurin yhdistämisen tunnetut ongelmat
description: Tässä artikkelissa kuvataan ongelmia, joita Microsoft Dynamics 365 Human Resources -infrastruktuurin yhdistämisen aikana voi ilmetä.
author: twheeloc
ms.date: 10/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 28c2c10a9293d00e26dfcc80ab08b89a122a6135
ms.sourcegitcommit: 088a7b5eb9a3b68710dfe012abf4c24776978750
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2022
ms.locfileid: "9733453"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-known-issues"></a>Dynamics 365 Human Resources -infrastruktuurin yhdistämisen tunnetut ongelmat

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="shared-dataverse-environments"></a>Jaetut Dataverse-ympäristöt

Kaksoiskirjoituksen kehys ei tue kahden talous- ja toimintosovellusympäristön linkittämistä samaan Dataverse-ympäristöön. Jos sinulla on Dataverse-ympäristö, joka on jaettu molemmille seuraaville kohteille, sinun täytyy joko kopioida Dataverse-ympäristö tai jakaa se osiin:

- Talous- ja toimintosovellukset
- Tämänhetkinen Human Resources -ympäristö

## <a name="environment-type-requirements"></a>Vaaditut ympäristötyypit

Tarvitset seuraavat ympäristötyypit ennen kuin voit suorittaa siirron:

- Jos sinulla ei ole yhtään erillistä eristysympäristöä, sinun täytyy luoda sellainen siirron vahvistusta varten.
- Jos sinulla on useita erillisiä tuotantoympäristöjä, yksi niistä voidaan siirtää. Ota yhteyttä Microsoft-tukeen merkitäksesi muut ympäristöt eristysympäristöiksi.

## <a name="teams-integration"></a>Teams-integrointi

Teamsin nykyistä Human Resoures -sovellusta siirretään tällä hetkellä Microsoft Power Platform -ratkaisuun. Lisätietoja on kohdassa [Human Resources -sovellus Teamsissa](hr-admin-teams-leave-app.md).

## <a name="licensing"></a>Käyttöoikeudet

Dynamics 365 Human Resources -lisensseihin ei tehdä muutoksia seuraavien osa-alueiden osalta: 

- **Ostettujen lisenssien vaadittu vähimmäismäärä**
- **Tuotantoympäristön ja eristysympäristön käyttöoikeudet** – Jos sinulla on itsenäisiä Human Resources -lisenssejä, jotka sisältävät yhden tuotantoympäristön ja yhden eristysympäristön, talous- ja toimintosovellusinfrastruktuurissa on saatavilla sama määrä lisenssejä.
- **Eristysympäristöjen lisälisenssit** – Jos olet ostanut eristysympäristöjen lisälisenssejä erilliselle Human Resources -sovellukselle, eristysympäristöille on saatavilla sama määrä lisenssejä talous- ja toimintosovellusinfrastruktuurissa. 
