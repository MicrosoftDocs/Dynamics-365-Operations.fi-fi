---
title: Dynamics 365 Commerce -arviointiympäristön usein kysytyt kysymykset
description: Tässä aiheessa on vastauksia Microsoft Dynamics 365 Commercen arviointiympäristön usein kysyttyihin kysymyksiin.
author: v-chgri
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e8a3e760353b351d42aff82c0d372d2aca350cd2
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343555"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a>Dynamics 365 Commerce -arviointiympäristön usein kysytyt kysymykset

[!include [banner](includes/banner.md)]

Tässä aiheessa on vastauksia Microsoft Dynamics 365 Commercen arviointiympäristön usein kysyttyihin kysymyksiin.

## <a name="can-we-use-the-commerce-evaluation-environment-as-an-e-commerce-storefront-for-customers-that-currently-implement-retail"></a>Voiko Commercen arviointiympäristöä käyttää sähköisen kaupankäynnin kaupassa asiakkaille, jotka tällä hetkellä käyttävät Retailia?

Nro Commercen arviointiympäristö on tarkoitettu vain arviointiin. Jos tarvitset ympäristöä asiakkaalle, joka toteuttaa vähittäismyynnin, ota yhteyttä Microsoftiin.

## <a name="can-the-commerce-evaluation-environment-be-used-to-provision-the-e-commerce-features-on-top-of-an-existing-applicationenvironment-that-implements-retail"></a>Voiko Commercen arviointiympäristöä käyttää sähköisen kaupankäynnin ominaisuuksien valmisteluun nykyisen Retailin toteutuksessa käytetyn sovelluksen tai ympäristön ohella?

Ei (yleensä). Commercen arviointiosat ovat saatavana vain ympäristöissä, jotka vastaavat edellytyksissä ja valmisteluoppaassa mainittuja määrityksiä. Lisäksi vaadittuja perusesittelytietoja ei ole ympäristöissä, jotka otettiin käyttöön alkuperäisessä julkaisussa, joka on aikaisempi kuin versio 10.0.8. 

## <a name="what-costs-are-involved-in-deploying-the-commerce-evaluation-environment-on-microsoft-azure-via-microsoft-dynamics-lifecycle-services-lcs"></a>Mitä kustannuksia liittyy Commercen arviointiympäristön käyttöönottoon Microsoft Azuressa Microsoft Dynamics Lifecycle Servicesin (LCS) kautta?

Perinteistä Dynamics 365 Financen, Dynamics 365 Supply Chain Managementin ja Dynamics 365 Commercen pääkonttorin esittely-ympäristöä (virtuaalikone \[VM\]) isännöidään Azure-tilauksessa. Voit käyttää [Azure hinnoittelulaskuria](https://azure.microsoft.com/pricing/calculator/) tämän kustannuksen arvioimiseen.

Muut osat, kuten Commerce Scale Unit, Commercen sivustonmuodostin ja sähköinen kaupankäyntisivusto, ovat saatavana Microsoftin isännöimänä ohjelmisto palveluna (SaaS) -vaihtoehtona.

## <a name="which-azure-geographies-are-currently-supported-for-the-commerce-evaluation-environment"></a>Mitkä Azure-maita tuetaan tällä hetkellä Commercen arviointiympäristössä?

Commercen arviointiympäristö voidaan ottaa käyttöön vain Pohjois-Amerikan maantieteellisellä alueella.

## <a name="is-there-a-downloadable-virtual-hard-disk-vhd-that-has-the-complete-onebox-virtual-machine-vm-option"></a>Onko olemassa ladattava virtuaalinen kovalevy (VHD), jolla on täydellinen OneBox Virtual Machinen (VM) vaihtoehto?

Dynamics 365 Commerce ja Commerce Scale Unit ovat saatavana pilvessä käytettävänä ohjelmisto palveluna (SaaS) -versiona.

## <a name="how-long-can-the-commerce-evaluation-environment-be-used"></a>Kuinka kauan Commerce arviointiympäristöä voi käyttää?

Commerce arviointiympäristöllä on 30 päivän aikaraja siitä päivästä, jolloin SaaS-osat, kuten Commerce Scale Unit, Commercen sivustonmuodostin ja oma sähköinen kaupankäyntisivusto, on valmisteltu.

## <a name="can-i-extend-the-time-limit-for-my-commerce-evaluation-environment"></a>Voinko pidentää Commercen arviointiympäristön aikarajaa?

Aikarajan pidennys on poikkeus, jota harkitaan tapauskohtaisesti. Ota tässä tapauksessa yhteys Microsoft-kumppaniin.

## <a name="additional-resources"></a>Lisäresurssit

[Dynamics 365 Commerce -arviointiympäristön yleiskuvaus](cpe-overview.md)

[Dynamics 365 Commerce -arviointiympäristön valmisteleminen](provisioning-guide.md)

[Dynamics 365 Commerce -arviointiympäristön määritykset](cpe-post-provisioning.md)

[BOPIS:n määritykset Dynamics 365 Commerce -arviointiympäristössä](cpe-bopis.md)

[Dynamics 365 Commerce -arviointiympäristön valinnaisten ominaisuuksien määritykset](cpe-optional-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
