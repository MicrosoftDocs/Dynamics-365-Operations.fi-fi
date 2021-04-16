---
title: Varastonhallinnan varausten vianmääritys
description: Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun varastovarauksia käytetään Microsoft Dynamics 365 Supply Chain Managementissa.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: d0d73396772ed9e8397797d6685fb550d911303b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828103"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a>Varastonhallinnan varausten vianmääritys

[!include [banner](../includes/banner.md)]

Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun varastovarauksia käytetään Microsoft Dynamics 365 Supply Chain Managementissa.

Lisätietoja erä- ja sarjanumerorekisteröinnistä: [Varaston erä- ja sarjanumeroiden varaushierarkioiden vianmääritys](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
