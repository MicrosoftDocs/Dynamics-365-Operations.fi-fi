---
title: Varastonhallinnan varausten vianmääritys
description: Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun varastovarauksia käytetään Microsoft Dynamics 365 Supply Chain Managementissa.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6151797001b1ccdb7e371c70b90c304a5ab422d8
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645116"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a>Varastonhallinnan varausten vianmääritys

[!include [banner](../includes/banner.md)]

Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun varastovarauksia käytetään Microsoft Dynamics 365 Supply Chain Managementissa.

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a>Seuraava virhesanoma avautuu: Varauksia ei voi poistaa, koska on luotu töitä, jotka ovat riippuvaisia niistä.

### <a name="issue-description"></a>Ongelman kuvaus

Myyntirivin varastoin varausta ei voi poistaa, koska rivillä on avoin työ.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Selvitä, onko kyse avoimesta pakkausryhmän työstä ja siirrä nimike pakkausasemalta toiseen sijaintiin (kuten *lastausovelle*). Selvitä **Työn luontihistorian loki**- ja **Työn tiedot** -sivuilta, mikä fyysisesti varaa varastoa, ja vapauta varaus sitten suorittamalla tai poistamalla työ.

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a>Näytössä on seuraava virhesanoma: Varastomäärää -%1 ei voi päivittää, sillä varastotapahtumia on liian vähän nimikkeelle %2....

### <a name="issue-description"></a>Ongelman kuvaus

Tämä ongelma voi esiintyä, jos järjestelmä ei voi päivittää varastomäärää, koska varastotapahtumia, joilla on määritetyt dimensiot, ei ole tarpeeksi. Virhesanoman koko teksti:

> Varastomäärää -%1 ei voi päivittää, sillä varastotapahtumia on liian vähän nimikkeelle %2 dimensioilla Koko=%3, Väri=%4, Lisäykset=%5, Toimipaikka=%6, Varasto=%7, Varasto=%8, Varaston tila=Käytettävissä, Rekisterikilpi=%9, Eränumero=%10 viitetunnusta %11 varten erätunnuksessa %12.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Varmista, että määrää ei ole varattu fyysisesti millään varastotapahtumalla. Nämä tapahtumat voivat esimerkiksi avata laatutilauksia, varastoestotilauksia tai toimitustilauksia.

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a>Seuraava virhesanoma avautuu: Fyysinen varastosaldo...ei voi varata, koska varastossa on vain 0,00 saatavana.

### <a name="issue-description"></a>Ongelman kuvaus

Tämä ongelma voi esiintyä, jos järjestelmä ei voi päivittää varastomäärää, koska varastotapahtumia, joilla on määritetyt dimensiot, ei ole tarpeeksi. Virhesanoman koko teksti:

> Fyysinen varastosaldo Toimipaikka=%1, Varasto=%2, Varaston tila=käytettävissä, Eränumero=%3, Omistaja=%4: %5 ei voi varata, koska varastossa on vain 0,00 saatavana.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Tämä ongelman syy on todennäköisesti avoin työ. Voit joko suorittaa työn tai vastaanottaa ilman työn luontia. Varmista, että määrää ei ole varattu fyysisesti millään varastotapahtumalla. Nämä tapahtumat voivat esimerkiksi avata laatutilauksia, varastoestotilauksia tai toimitustilauksia.

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a>Seuraava virhesanoma avautuu: Jotta kuormituksen rivit voidaan määrittää aaltoon, niiden on määritettävä dimensiot sijainnin yläpuolelle. Voit määrittää nämä dimensiot varaamalla kuormituksen rivin ja luomalla sen uudelleen.

### <a name="issue-description"></a>Ongelman kuvaus

Jos käytät nimikettä, jossa käytetään erän yläpuolella olevaa varaushierarkiaa (eli **Eränumero**-dimensio on sijoitettu **Sijainti**-dimension *yläpuolelle*), osittaisen määrän **Kuormasuunnittelun työtila** -sivun **Vapauta varastoon** -komento ei toimi. Sait tämän virhesanoma eikä osittaiselle määrälle luoda yhtään työtä.

Jos käytät kuitenkin nimikettä, jossa käytetään erän alapuolella olevaa varaushierarkiaa (eli **Eränumero**-dimensio on sijoitettu **Sijainti**-dimension *alapuolelle*), voit vapauttaa kuorman osittaisen määrän **Kuormasuunnittelun työtila** -sivulta.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Tämä on suunniteltu ominaisuus. Jos sijoitat dimension **Sijainti**-dimension yläpuolelle varaushierarkiassa, se on määritettävä ennen vapautusta varastoon. Microsoft on arvioinut tämän ongelman ja määrittänyt sen toimintorajoitukseksi, joka koskee vapautuksia varastoon kuormasuunnittelun työtilasta. Osittaisia määriä ei voi vapauttaa, jos vähintään yhtä **Sijainti**-dimension yläpuolella olevaa dimensiota ei ole määritetty.

Lisätietoja on kohdassa [Joustava varastotason dimensioiden varauskäytäntö](flexible-warehouse-level-dimension-reservation.md).
