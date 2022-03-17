---
title: Sähköisen laskutuksen määritys
description: Tämä ohjeaihe sisältää yhteenvedon sähköisen laskutuksen määritys- ja konfigurointiprosessista.
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
ms.openlocfilehash: 8138c63e9eff1d2ca934f9d4467e4e3b73dae941
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371646"
---
# <a name="electronic-invoicing-setup"></a>Sähköisen laskutuksen määritys

[!include [banner](../includes/banner.md)]

Tämä ohjeaihe sisältää yhteenvedon sähköisen laskutuksen määritys- ja konfigurointiprosessista. Asennusvaiheet on suoritettava tässä määritetyssä järjestyksessä. Jos vaihe on pakollinen, mutta ohitat sen, toiminto ei toimi oikein, ja useita virheitä tapahtuu seuraavien vaiheiden aikana tai toimintoa käytettäessä. 

Varmista ennen aloittamista, että kaikki pääkomponentit on määritetty oikein, että olet rekisteröitynyt Regulatory Configuration Serviceen (RCS) ja että sinulla on RCS-esiintymä ja että sähköisen laskutuksen lisäosa on asennettu Microsoft Dynamics 365 Finance- tai Dynamics 365 Supply Chain Management -ympäristöäsi varten. Lisätietoja: [Sähköisen laskutuksen rekisteröiminen ja asennus](e-invoicing-install-add-in-microservices-lcs.md).

Määritä seuraavaksi Azure-resurssit, joita sähköinen laskutus edellyttää toimiakseen. Lisätietoja on kohdassa [Sähköisen laskutuksen Azure-resurssien määrittäminen](e-invoicing-set-up-azure-resources.md).

Kun pääkomponentit on konfiguroitu, määritä sähköisen laskutuksen loogiset pääkomponentit RCS:n avulla. Määritä ensin ylläpidettävien palveluympäristöjen määrä. Näin voit määrittää loogiset tiedot ja konfiguraation osioinnin, jotta kehitys- tai testiympäristön ja tuotantoympäristön välillä on raja. Jotta voit määrittää kehitysprosessin joustavasti, saatat tarvita useita erillisiä kehitys- ja testiympäristöjä. Palveluympäristöjen määrittämisen lisäksi voit luoda linkin liiketoimintasovelluksiin, kuten Financeen tai Supply Chain Managementiin, suoraan RCS:stä ja määrittää parametrit, joita tarvitaan sähköisen laskutuksen oikean käytön yhteydessä. Lisätietoja ympäristöistä on kohdassa [Palveluympäristöt](e-invoicing-service-environments.md).

Kun kaikki on määritetty, voit luoda omia globalisointitoimintoja, jotka määrittävät sähköisten tiedostojen käsittely- ja muuntoskenaariot sekä tiedostojen tuonnin yleisestä tietovarastosta. Lisätietoja globalisaatio-ominaisuuksien käyttämisestä: [Globalisaatio-ominaisuuksien käyttäminen](e-invoicing-working-globalization-features.md).

Tietoja toiminnoista käsittelyputkissa, jotka muodostavat globalisaatio-ominaisuuksien luontiprosessin: **[SUORITA!: Tiedoston käsittelyn toiminnot]**.

Jos skenaariosi edellyttävät sähköpostin tai SharePointin integrointia tai saapuvien sähköisten tiedostojen käsittelyyn, katso lisätietoja näiden kanavien määrittämisestä ja käyttämisestä kohdasta [Saapuvien sähköisten tiedostojen käsitteleminen](e-invoicing-process-incoming-electronic-documents.md) .
