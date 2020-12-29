---
title: Edistyneeseen varastonhallintaan päivittämisen ja siirtymisen vianmääritys
description: Tässä aiheessa käsitellään yleisten edistyneeseen varastonhallintaan päivittämisen ja siirtymisen ongelmien korjaamista.
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
ms.openlocfilehash: d50c6d75ec7cc98109cf81c38ff42b4d2b105b0c
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645814"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a>Edistyneeseen varastonhallintaan päivittämisen ja siirtymisen vianmääritys

[!include [banner](../includes/banner.md)]

Tässä aiheessa käsitellään yleisten edistyneeseen varastonhallintaan päivittämisen ja siirtymisen ongelmien korjaamista.

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a>Seuraava virhesanoma avautuu: java.security.cert.certPathValidatorException: Sertifiointipolun luottamusankkuria ei löytynyt.

### <a name="issue-description"></a>Ongelman kuvaus

Tämä virhesanoma avautuu varastointisovelluksessa, koska itse allekirjoitettuihin varmenteisiin ei tueta paikallisissa Android 8+ -ympäristöissä.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Käytä ulkoista (julkista) varmenteiden myöntäjää. Tämän varastointisovelluksen ongelman korjaus on saatavana versiossa 1.9.0.0. Lisätietoja tästä ongelmasta ja sen korjaamisesta on kohdassa [Varastosovelluksen yhteysongelmien vianmääritys](troubleshoot-warehouse-app-connection.md).

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a>Mikä on hyväksytty prosessi siirryttäessä perusvarastoinnista edistyneeseen varastointiin?

### <a name="issue-description"></a>Ongelman kuvaus

Tällä hetkellä käytössä on erilaisten varastojen hallinta ja perusvarastotoiminnot, ja haluat siirtyä edistyneeseen varastointiin, jossa hyödynnetään mobiililaitteita, aaltoja ja työtä. Tätä siirtoa yritettäessä on kuitenkin ongelmia. Tuotteita ei voi esimerkiksi muuttaa niin, että ne käyttävät varastodimensioita (toimipaikkaa, varastoa ja sijaintia), koska tuotteisiin kohdistuu tapahtumia. Tämän vuoksi on opittava hyväksytty prosessi siirryttäessä perusvarastoinnista edistyneeseen varastointiin.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Lisätietoja perusvarastoinnista edistyneeseen varastointiin siirtymisestä on seuraavissa blogikirjoituksissa ja asiakirjoissa:

- [Aiemmin luotujen nimikkeiden ja varastojen varastonhallintaprosessin ottaminen käyttöön](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [Microsoft Dynamics AX WMS:n siirto uuteen R3-varastointi- ja kuljetustoimintoon](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [WMSI-/WMS2-nimikkeen siirto](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [Varastonhallinnan päivittäminen Microsoft Dynamics AX 2012:sta Supply Chain Managementiin](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/upgrade-migration-warehouse-management-processes)
