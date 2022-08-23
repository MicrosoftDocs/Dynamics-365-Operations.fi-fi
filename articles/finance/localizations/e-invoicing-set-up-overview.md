---
title: Sähköisen laskutuksen määritys
description: Tämä artikkeli sisältää yhteenvedon sähköisen laskutuksen määritys- ja konfigurointiprosessista.
author: gionoder
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: de94843c1e98a8788375bd41def587a64baea07d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272176"
---
# <a name="electronic-invoicing-setup"></a>Sähköisen laskutuksen määritys

[!include [banner](../includes/banner.md)]

Tämä artikkeli sisältää yhteenvedon sähköisen laskutuksen määritys- ja konfigurointiprosessista. Asennusvaiheet on suoritettava tässä määritetyssä järjestyksessä. Jos vaihe on pakollinen, mutta ohitat sen, toiminto ei toimi oikein, ja useita virheitä tapahtuu seuraavien vaiheiden aikana tai toimintoa käytettäessä. 

Varmista ennen aloittamista, että kaikki pääkomponentit on määritetty oikein, että olet rekisteröitynyt Regulatory Configuration Serviceen (RCS) ja että sinulla on RCS-esiintymä ja että sähköisen laskutuksen lisäosa on asennettu Microsoft Dynamics 365 Finance- tai Dynamics 365 Supply Chain Management -ympäristöäsi varten. Lisätietoja: [Sähköisen laskutuksen rekisteröiminen ja asennus](e-invoicing-install-add-in-microservices-lcs.md).

Määritä seuraavaksi Azure-resurssit, joita sähköinen laskutus edellyttää toimiakseen. Lisätietoja on kohdassa [Sähköisen laskutuksen Azure-resurssien määrittäminen](e-invoicing-set-up-azure-resources.md).

Kun pääkomponentit on konfiguroitu, määritä sähköisen laskutuksen loogiset pääkomponentit RCS:n avulla. Määritä ensin ylläpidettävien palveluympäristöjen määrä. Näin voit määrittää loogiset tiedot ja konfiguraation osioinnin, jotta kehitys- tai testiympäristön ja tuotantoympäristön välillä on raja. Jotta voit määrittää kehitysprosessin joustavasti, saatat tarvita useita erillisiä kehitys- ja testiympäristöjä. Palveluympäristöjen määrittämisen lisäksi voit luoda linkin liiketoimintasovelluksiin, kuten Financeen tai Supply Chain Managementiin, suoraan RCS:stä ja määrittää parametrit, joita tarvitaan sähköisen laskutuksen oikean käytön yhteydessä. Lisätietoja ympäristöistä on kohdassa [Palveluympäristöt](e-invoicing-service-environments.md).

Kun kaikki on määritetty, voit luoda omia globalisointitoimintoja, jotka määrittävät sähköisten tiedostojen käsittely- ja muuntoskenaariot sekä tiedostojen tuonnin yleisestä tietovarastosta. Lisätietoja globalisaatio-ominaisuuksien käyttämisestä: [Globalisaatio-ominaisuuksien käyttäminen](e-invoicing-working-globalization-features.md).

Jos skenaariosi edellyttävät sähköpostin tai SharePointin integrointia tai saapuvien sähköisten tiedostojen käsittelyyn, katso lisätietoja näiden kanavien määrittämisestä ja käyttämisestä kohdasta [Saapuvien sähköisten tiedostojen käsitteleminen](e-invoicing-process-incoming-electronic-documents.md) .
