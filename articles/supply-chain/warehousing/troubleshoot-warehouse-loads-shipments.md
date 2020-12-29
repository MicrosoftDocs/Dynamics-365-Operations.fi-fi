---
title: Kuormituksen luomisen ja lähetysten vianmääritys
description: Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun kuormituksen luontia ja lähetyksiä käytetään Microsoft Dynamics 365 Supply Chain Managementissa.
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
ms.openlocfilehash: 2933bcfd2cc526e39a4e1343cd472334a5b95607
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645329"
---
# <a name="troubleshoot-load-building-and-shipments"></a>Kuormituksen luomisen ja lähetysten vianmääritys

[!include [banner](../includes/banner.md)]

Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun kuormituksen luontia ja lähetyksiä käytetään Microsoft Dynamics 365 Supply Chain Managementissa.

## <a name="i-receive-the-following-error-message-you-cant-create-a-load-line-for-this-order-line-because-it-contains-inventory-dimensions-that-are-invalid"></a>Seuraava virhesanoma avautuu: Et voi luoda tälle tilausriville kuormariviä, koska se sisältää virheellisiä varastodimensioita...

### <a name="issue-description"></a>Ongelman kuvaus

Seuraava virhesanoma avautuu, kun yrität vapauttaa myyntitilauksen palautuksen varastoon:

> Et voi luoda tälle tilausriville kuormariviä, koska se sisältää virheellisiä varastodimensioita. Et voi viitata varastodimensioihin, jotka sijaitsevat varaushierarkiassa sijaintidimension alla. Poista virheelliset dimensiot tilausriviltä.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Tuote ei valitettavasti tue myynnin palautusprosessin kuorman käsittelyä. Niinpä myyntitilauksen palautusta ei voi vapauttaa varastoon.

Myyntitilaustapahtumissa ei voi viitata varastodimensioihin, jotka sijaitsevat varaushierarkiassa **Sijainti**-dimension alla. Ongelman ratkaisu on virheellisten dimensioiden poistaminen tilausriviltä.

## <a name="i-receive-the-following-error-message-one-of-the-lines-is-already-on-a-load-unable-to-release-to-warehouse"></a>Seuraava virhesanoma avautuu: Yksi riveistä on jo kuormassa. Vapautus varastoon ei onnistu.

### <a name="issue-description"></a>Ongelman kuvaus

Jos kuormat luodaan manuaalisesti tai jos prosessi määritetään siten, että kuormat on jo luotu ennen myyntitilausrivin kirjaamista, oletuksena on, että seuraava vapautus tehdään manuaalisesti ja että käytössä on kuorman reititys ja hinnoittelu.

Mahdollinen on myös skenaario, jossa varastoon yritetään tehdä automaattinen vapautus mutta aaltoprosessi ei luo työtä. Tämän vuoksi luodaan kuitenkin avoin lähetys tai kuorma. Tämä avoin lähetys tai kuorma estää seuraavat yritykset vapauttaa tilaus automaattisesti siihen asti, että avoin lähetys tai kuorma poistetaan tai aalto käsitellään uudelleen manuaalisesti.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Vapautus voidaan tehdä myyntitilaussivulta tai automaattinen vapautus myyntitilauksen vapautussivulta vain siinä tapauksessa, että yhtään kuormaa ei ole ennen vapautusta varastoon. Kuorma luodaan automaattisesti aallon käsittelyn jälkeen.

## <a name="i-receive-the-following-error-message-the-delivery-note-correction-cant-be-processed-the-delivery-note-only-contains-items-that-are-subject-to-warehouse-management-processes-as-these-are-not-supported-by-delivery-note-correction"></a>Seuraava virhesanoma avautuu: Toimitusilmoituksen korjausta ei voitu käsitellä. Toimitusilmoitus sisältää vain nimikkeet, jotka liittyvät varastonhallintaprosesseihin, koska toimitusilmoituksen korjaus ei tue niitä.

### <a name="issue-description"></a>Ongelman kuvaus

Kirjattua toimitusilmoitusta ei voi peruuttaa, koska **Peruuta**-painike ei ole käytettävissä. Toimitusilmoitusta ei voi myöskään korjata. Jos yrität sitä, kyseinen virhesanoma avautuu.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Varastonhallintajärjestelmää käyttävien nimikkeiden kirjattujen pakkausluetteloiden korjaaminen edellyttää, että kirjaaminen tehdään kuormasta eikä suoraan tilauksesta.

## <a name="how-can-i-create-work-from-outbound-loads-instead-of-waves"></a>Miten työ luodaan lähtevistä kuormista ei aalloista?

### <a name="issue-description"></a>Ongelman kuvaus

Ongelman voi toisintaa esimerkiksi seuraavasti.

1. Luo lähtevä kuorma käyttämällä myyntitilausta tai siirtotilausta.
2. Vapauta kuorma varastoon.
3. Huomaa, että keräilytyötä ei ole vielä luotu.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Jos työ on luotava heti, kun kuorma vapautetaan, aaltomalli on määritettävä vastaavasti. Määritä aaltomallin seuraavissa asetuksissa *Kyllä*:

- Automatisoi aallon luonti
- Käsittele aalto, kun se vapautetaan varastoon
- Automatisoi aallon vapautus

## <a name="i-cant-re-release-a-partially-shipped-load"></a>Osittain lähetettyä kuormaa ei voi vapauttaa uudelleen

### <a name="issue-description"></a>Ongelman kuvaus

Osittain lähetettyä kuormaa ei voi vapauttaa varastoon. Kun vapautus varastoon tehdään, Toiminto valmis -sanoma avautuu mutta mitään ei tapahdu eikä jäljellä olevalle määrälle luoda työtä. Tämä ongelma esiintyy käytettäessä kuljetuskuormatoimintoa ja varaus on keskeneräinen.

### <a name="issue-resolution"></a>Ongelman ratkaisu

[KB 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) (Osittain lähetetyt kuormat voidaan uudelleenaallottaa ja -käsitellä) on korjattu [versiossa 10.0.15](../get-started/whats-new-scm-10-0-15.md).
