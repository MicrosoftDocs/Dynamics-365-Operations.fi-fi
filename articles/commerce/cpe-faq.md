---
title: Dynamics 365 Commerce -arviointiympäristön usein kysytyt kysymykset
description: Tässä aiheessa on vastauksia Microsoft Dynamics 365 Commercen arviointiympäristön usein kysyttyihin kysymyksiin.
author: v-chgri
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 637714e28b9f8f4aa66e251e709d8f78bff2739d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411869"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a>Dynamics 365 Commerce -arviointiympäristön usein kysytyt kysymykset

[!include [banner](includes/banner.md)]

Tässä aiheessa on vastauksia Microsoft Dynamics 365 Commercen arviointiympäristön usein kysyttyihin kysymyksiin.

**Voiko Commercen arviointiympäristöä käyttää sähköisen kaupankäynnin kaupassa asiakkaille, jotka tällä hetkellä käyttävät Retailia?**

Nro Commercen arviointiympäristö on tarkoitettu vain arviointiin. Jos tarvitset ympäristöä asiakkaalle, joka toteuttaa vähittäismyynnin, ota yhteyttä Microsoftiin.

**Voiko Commercen arviointiympäristöä käyttää sähköisen kaupankäynnin ominaisuuksien valmisteluun nykyisen Retailin toteutuksessa käytetyn sovelluksen tai ympäristön ohella?**

Ei (yleensä). Commercen arviointiosat ovat saatavana vain ympäristöissä, jotka vastaavat edellytyksissä ja valmisteluoppaassa mainittuja määrityksiä. Lisäksi vaadittuja perusesittelytietoja ei ole ympäristöissä, jotka otettiin käyttöön alkuperäisessä julkaisussa, joka on aikaisempi kuin versio 10.0.8. 

**Mitä kustannuksia liittyy Commercen arviointiympäristön käyttöönottoon Microsoft Azuressa Microsoft Dynamics Lifecycle Servicesin (LCS) kautta?**

Perinteistä Dynamics 365 Financen, Dynamics 365 Supply Chain Managementin ja Dynamics 365 Commercen pääkonttorin esittely-ympäristöä (virtuaalikone \[VM\]) isännöidään Azure-tilauksessa. Voit käyttää [Azure hinnoittelulaskuria](https://azure.microsoft.com/pricing/calculator/) tämän kustannuksen arvioimiseen.

Muut osat, kuten Commerce Scale Unit, Commercen sivustonmuodostin ja sähköinen kaupankäyntisivusto, ovat saatavana Microsoftin isännöimänä ohjelmisto palveluna (SaaS) -vaihtoehtona.

**Mitkä Azure-maita tuetaan tällä hetkellä Commercen arviointiympäristössä?**

Commercen arviointiympäristö voidaan ottaa käyttöön vain Pohjois-Amerikan maantieteellisellä alueella.

**Onko olemassa ladattava virtuaalinen kovalevy (VHD), jolla on täydellinen OneBox Virtual Machinen (VM) vaihtoehto?**

Dynamics 365 Commerce ja Commerce Scale Unit ovat saatavana pilvessä käytettävänä ohjelmisto palveluna (SaaS) -versiona.

**Kuinka kauan Commerce arviointiympäristöä voi käyttää?**

Commerce arviointiympäristöllä on 30 päivän aikaraja siitä päivästä, jolloin SaaS-osat, kuten Commerce Scale Unit, Commercen sivustonmuodostin ja oma sähköinen kaupankäyntisivusto, on valmisteltu.

**Voinko pidentää Commercen arviointiympäristön aikarajaa?**

Aikarajan pidennys on poikkeus, jota harkitaan tapauskohtaisesti. Ota tässä tapauksessa yhteys Microsoft-kumppaniin.

## <a name="additional-resources"></a>Lisäresurssit

[Dynamics 365 Commerce -arviointiympäristön yleiskuvaus](cpe-overview.md)

[Dynamics 365 Commerce -arviointiympäristön valmisteleminen](provisioning-guide.md)

[Dynamics 365 Commerce -arviointiympäristön määritykset](cpe-post-provisioning.md)

[BOPIS:n määritykset Dynamics 365 Commerce -arviointiympäristössä](cpe-bopis.md)

[Dynamics 365 Commerce -arviointiympäristön valinnaisten ominaisuuksien määritykset](cpe-optional-features.md)
