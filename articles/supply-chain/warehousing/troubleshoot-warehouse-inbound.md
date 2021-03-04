---
title: Saapuvien varastotoimintojen vianmääritys
description: Tässä aiheessa käsitellään sellaisten yleisten ongelmien korjaamista, joita voi esiintyä, kun saapuvia varastotoimintoja käytetään Microsoft Dynamics 365 Supply Chain Managementissa.
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
ms.openlocfilehash: 60b6e37ec9d716f635c2d25374ac25a82286660e
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645969"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a>Saapuvien varastotoimintojen vianmääritys

[!include [banner](../includes/banner.md)]

Tässä aiheessa käsitellään sellaisten yleisten ongelmien korjaamista, joita voi esiintyä, kun saapuvia varastotoimintoja käytetään Microsoft Dynamics 365 Supply Chain Managementissa.

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a>Seuraava virhesanoma avautui: Laatutilaus %1 on luotu. Klusteriprofiilia ei löytynyt. Tarkista konfiguraatio.

### <a name="issue-description"></a>Ongelman kuvaus

Tämä virhesanoma liittyy vastaanottoprosessiin, jossa laadunhallinta on otettu käyttöön. Ympäristön määritysten mukaan virhesanoman luovan tapahtuman lisätiedot voivat auttaa korjaamaan ongelman.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Tarkista ensimmäiseksi [klusterikeräilyn](set-up-cluster-picking.md) määritys ja varmista, että klusteriprofiilit on määritetty oikein. Et voi käyttää mobiililaitteen klusterikeräilyn valikkokohdetta, ellei klusteriprofiileja ole määritetty. Ympäristön mukaan on ehkä tarkistettava myös liittyvät määritykset.

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a>Yhdistelmärekisterikilven vastaanottoa ei voi käyttää muussa kuin hyvityksen jakelukoodissa.

### <a name="issue-description"></a>Ongelman kuvaus

Kun jakelukoodin **Toiminto**-kentän määrityksenä on *Hyvitys* tai *Hävikki*, voit käyttää [Yhdistelmärekisterikilven vastaanotto](mixed-license-plate-receiving.md) -valikkovaihtoehtoa palautettujen nimikkeiden käsittelemiseen.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Microsoft on arvioinut ongelman ja määrittänyt, että se on ominaisuuden rajoitus. Tällä hetkellä yhdistelmärekisterikilven vastaanotossa tuetaan vain [jakelukoodeja](../service-management/set-up-disposition-codes.md), joissa **Toiminto**-kentän asetuksena on *Hyvitys* tai *Hävikki*.

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a>Kun kausittainen tuotteen vastaanottojen päivitystehtävä suoritetaan, vahvistamattomat ostotilaukset vahvistetaan.

### <a name="issue-description"></a>Ongelman kuvaus

Kun olet suorittanut kausittaisen *Päivitä tuotteen vastaanotot* -tehtävän, järjestelmä vahvistaa automaattisesti vahvistamattomat ostotilaukset, joiden varastotapahtuman tila on *Rekisteröity*.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Uusi saapuvan kuorman käsittelyominaisuus *Kuormamäärien ylivastaanottaminen* korjaa tämän ongelman. Ota tämä ominaisuus käyttöön siirtymällä [ominaisuuksien hallintaan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja ottamalla seuraavat ominaisuudet käyttöön (alla olevassa järjestyksessä):

1. Liitä ostotilauksen varastotapahtumat kuorman kanssa
1. Kuormamääriä vastaanotettu liikaa

Lisätietoja on kohdassa [Kirjattujen tuotemäärien kirjaaminen ostotilauksiin](inbound-load-handling.md#post-registered-quantities).