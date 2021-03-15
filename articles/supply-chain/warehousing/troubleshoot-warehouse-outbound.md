---
title: Lähtevien varaston työvaiheiden vianmääritys
description: Tässä aiheessa käsitellään sellaisten yleisten ongelmien korjaamista, joita voi esiintyä, kun lähteviä varastotoimintoja käytetään Microsoft Dynamics 365 Supply Chain Managementissa.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 165ac8145ad75c2c6619764b9abe855b9d32eb46
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993975"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a>Lähtevien varaston työvaiheiden vianmääritys

[!include [banner](../includes/banner.md)]

Tässä aiheessa käsitellään sellaisten yleisten ongelmien korjaamista, joita voi esiintyä, kun lähteviä varastotoimintoja käytetään Microsoft Dynamics 365 Supply Chain Managementissa.

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a>Seuraava virhesanoma avautuu: Myyntitilausta ei voitu vapauttaa.

### <a name="issue-description"></a>Ongelman kuvaus

Tämä ongelman esiintymiseen voi olla useita syitä. Tilaus on esimerkiksi luotonhallinnan pidossa eikä lähetyksiä voi luoda, ennen kuin kaikille myyntitilaukseen liitetyille myyntiriveille on annettu kelvollinen postiosoite. Vaihtoehtoisesti kyse voi olla tilauksen pidosta, joka on käsiteltävä, ennen kuin tilaus voidaan vapauttaa varastoon. Kyseinen pito voi olla tilauskohtainen ja se voi olla asiakastilissä.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Lisää tai päivitä myyntitilauksen tai myyntitilausten osoite ja vapauta tilaus sitten varastoon. Tilaukset voidaan vapauttaa varastoon vain, jos niissä on kelvollinen toimitusosoite (**Organisaation hallinto** -moduulissa määritetyn osoitemuodon mukaisesti).

Selvitä tilauksen pito ja käsittele ongelmat. Poista sitten pito tilauksesta tai asiakkaasta ja vapauta tilaus varastoon.

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a>Seuraava sanoma avautuu: Kuorman 1% lähetys on vahvistettu. Mitään rivejä ei kuitenkaan kirjata.

### <a name="issue-description"></a>Ongelman kuvaus

Kuorman lähetys on vahvistettu mutta lisäkirjauksia ei tehdä.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Lähetyksen vahvistus ei vaikuta kirjaukseen. Se vain päivittää lähetyksen ja kuorman tilan. Kirjaus on tehtävä erillisessä prosessissa.

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a>Seuraava virhesanoma avautuu: Suoratoimitus ei voi käsitellä varastoa 1%, koska varastonhallinta on otettu siinä käyttöön. Määritä toinen varasto, jossa varastonhallintaa ei ole otettu käyttöön.

### <a name="issue-description"></a>Ongelman kuvaus

Nimike lisätään suoratoimituksen myyntiriville varastosta, jossa varastonhallinta on otettu käyttöön. Tämä virhesanoma avautuu, kun myyntirivi on päivitetty. 

### <a name="issue-resolution"></a>Ongelman ratkaisu

Microsoft on arvioinut ongelman ja määrittänyt, että se on ominaisuuden rajoitus. Varastonhallinta ei tue tällä hetkellä suoratoimitusta. Suoratoimituksen käyttämistä varten on sen vuoksi valittava muu kuin varastonhallintanimike ja varasto.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]