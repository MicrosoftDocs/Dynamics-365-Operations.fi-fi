---
title: Sähköisen laskutuksen määritys
description: Tämä artikkeli sisältää yhteenvedon sähköisen laskutuksen määritys- ja konfigurointiprosessista.
author: dkalyuzh
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8e2aa89119530a0ba00a8561d94006285d67a71b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883116"
---
# <a name="electronic-invoicing-setup"></a>Sähköisen laskutuksen määritys

[!include [banner](../includes/banner.md)]

Tämä artikkeli sisältää yhteenvedon sähköisen laskutuksen määritys- ja konfigurointiprosessista. Asennusvaiheet on suoritettava tässä määritetyssä järjestyksessä. Jos vaihe on pakollinen, mutta ohitat sen, toiminto ei toimi oikein, ja useita virheitä tapahtuu seuraavien vaiheiden aikana tai toimintoa käytettäessä. 

Varmista ennen aloittamista, että kaikki pääkomponentit on määritetty oikein, että olet rekisteröitynyt Regulatory Configuration Serviceen (RCS) ja että sinulla on RCS-esiintymä ja että sähköisen laskutuksen lisäosa on asennettu Microsoft Dynamics 365 Finance- tai Dynamics 365 Supply Chain Management -ympäristöäsi varten. Lisätietoja: [Sähköisen laskutuksen rekisteröiminen ja asennus](e-invoicing-install-add-in-microservices-lcs.md).

Määritä seuraavaksi Azure-resurssit, joita sähköinen laskutus edellyttää toimiakseen. Lisätietoja on kohdassa [Sähköisen laskutuksen Azure-resurssien määrittäminen](e-invoicing-set-up-azure-resources.md).

Kun pääkomponentit on konfiguroitu, määritä sähköisen laskutuksen loogiset pääkomponentit RCS:n avulla. Määritä ensin ylläpidettävien palveluympäristöjen määrä. Näin voit määrittää loogiset tiedot ja konfiguraation osioinnin, jotta kehitys- tai testiympäristön ja tuotantoympäristön välillä on raja. Jotta voit määrittää kehitysprosessin joustavasti, saatat tarvita useita erillisiä kehitys- ja testiympäristöjä. Palveluympäristöjen määrittämisen lisäksi voit luoda linkin liiketoimintasovelluksiin, kuten Financeen tai Supply Chain Managementiin, suoraan RCS:stä ja määrittää parametrit, joita tarvitaan sähköisen laskutuksen oikean käytön yhteydessä. Lisätietoja ympäristöistä on kohdassa [Palveluympäristöt](e-invoicing-service-environments.md).

Kun kaikki on määritetty, voit luoda omia globalisointitoimintoja, jotka määrittävät sähköisten tiedostojen käsittely- ja muuntoskenaariot sekä tiedostojen tuonnin yleisestä tietovarastosta. Lisätietoja globalisaatio-ominaisuuksien käyttämisestä: [Globalisaatio-ominaisuuksien käyttäminen](e-invoicing-working-globalization-features.md).

Jos skenaariosi edellyttävät sähköpostin tai SharePointin integrointia tai saapuvien sähköisten tiedostojen käsittelyyn, katso lisätietoja näiden kanavien määrittämisestä ja käyttämisestä kohdasta [Saapuvien sähköisten tiedostojen käsitteleminen](e-invoicing-process-incoming-electronic-documents.md) .
