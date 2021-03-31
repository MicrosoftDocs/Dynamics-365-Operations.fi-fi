---
title: Pääsuunnittelun vianmääritys
description: Tässä aiheessa käsitellään sellaisten ongelmien korjaamista, joita pääsuunnittelun käytössä voi esiintyä.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: db336946873fa1b5cc3f669823541af8cab4115b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216102"
---
# <a name="troubleshoot-master-planning"></a>Pääsuunnittelun vianmääritys

Tässä aiheessa käsitellään sellaisten ongelmien korjaamista, joita pääsuunnittelun käytössä voi esiintyä.

## <a name="bill-of-materials-explosion-behaves-differently-for-firmed-production-orders-and-for-estimated-production-orders-for-manually-created-work"></a>Tuoterakenteen hajotus toimii eri tavalla vahvistetuissa tuotantotilauksissa ja manuaalisesti luodun työn ennakkolasketuissa tuotantotilauksissa

### <a name="issue-description"></a>Ongelman kuvaus

Kun tuotantotilaus vahvistetaan, nimikkeitä ei hajoteta, kun tuoterakenne hajotetaan. Kun työtilaus kuitenkin luodaan manuaalisesti ja tuotantotilaukselle tehdään ennakkolaskenta, nimikkeet hajotetaan.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Järjestelmä toimii odotetusti. Tuotantotilausta vahvistettaessa tapahtuva hajotus osoittaa suunniteltuun tilaukseen, mutta ei vaikuta siltä, että suunniteltu tilaus on tällä hetkellä vahvistettu tässä tapauksessa. Jos tuotantotilaus on kuitenkin ennakkolaskettu, hajotus käynnistetään vapautetusta tuotantotilauksesta, kun suunniteltua tilausta ei ole.

## <a name="the-delay-value-isnt-updated-when-i-reschedule-a-planned-order"></a>Viivearvo ei päivitetä, kun suunniteltu tilaus ajoitetaan uudelleen

Päivitä suunniteltujen tilausten viive avaamalla suunnitellun tilauksen **Ajoitetaan uudelleen** -valintaikkuna. Varmista **Hajotus**-pikavälilehdessä, että **Suorita hajotus uudelleenajoittamisen jälkeen** -vaihtoehdon asetuksena on *Kyllä*.

## <a name="production-scheduling-doesnt-consider-the-safety-margins-that-are-set-on-the-item-coverage-for-pegged-supply"></a>Tuotannon ajoitus ei ota huomioon varmuusmarginaaleja, jotka on määritetty tarvekohdistetun nimikkeen kattavuudessa

### <a name="issue-description"></a>Ongelman kuvaus

Pääsuunnittelu ottaa varmuusmarginaalit huomioon. Varmuusmarginaalit kuitenkin ohitetaan, kun suunnittelut tuotantotilaukset ajoitetaan.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Marginaalit otetaan huomioon vain pääsuunnittelun aikana mutta ei manuaalisen ajoituksen aikana. Marginaalit suunnitellaan toimimaan puskureina suunnitteluvaiheen aikana tuomaan varsinaiseen prosessiin pelivaraa.

Halutun tuloksen saa poistamalla marginaalin. Reititys on päivitettävä sisältämään toivottu aika (esimerkiksi jonotusaikana): Pääsuunnittelun ja manuaalisen ajoituksen tuloksen pitäisi sitten olla sama.

## <a name="planned-orders-are-generated-even-though-we-have-items-in-stock-and-production-orders-already-exist-for-them"></a>Suunnitellut tilaukset luodaan, vaikka nimikkeitä on varastossa ja niillä on jo tuotantotilaukset.

Tämä ongelma on ehkä mahdollista korjata lisäämällä soveltuvien ryhmien **Positiiviset päivät** -arvoa **Kattavuusryhmä**-sivulla. Tämä muutos saa järjestelmän määrittää, voiko käytettävissä olevaa varastoa käyttää kysyntään. Silloin uutta suunniteltua tilausta ei luoda varastossa oleville nimikkeille.

## <a name="master-planning-doesnt-seem-to-respect-capacity-limitations-and-is-scheduling-more-than-the-available-capacity"></a>Pääsuunnittelu ei näytä noudattavan kapasiteettirajoituksia ja sen aikataulutus ylittää käytettävissä olevan kapasiteetin

### <a name="issue-description"></a>Ongelman kuvaus

Jos käytettävässä toiminnon aikatauluttamisessa on rajallinen kapasiteetti ja reititys määrittää yhdistelmätarpeet sekä resurssiryhmälle että yksittäisille resursseille, on olemassa pieni ylivarauksen mahdollisuus, joka johtuu algoritmin tavasta tarkistaa kapasiteettiristiriidat. Tämä ylivaraus voi esiintyä, kun pääsuunnittelun suorittamiseen käytetään lisätyöasemia. Se tapahtuu todennäköisimmin siinä tapauksessa, että useilla töillä on suhteellisen lyhyt suoritusaika.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Jos on ylivarauksia ei saa missään tapauksessa esiintyä toimintojen ajoittamisessa, voit tehdä pääsuunnittelun ajoituksesta yksisäikeisen ottamalla **Tarkka rajallinen kapasiteetti toimintojen ajoituksessa** -asetuksen käyttöön **Pääsuunnittelun parametrit** -sivulla. Tämä asetus ei ole oletusarvoisesti käytettävissä. Se on lisättävä manuaalisesti sivulle mukautustoimintojen avulla. Tätä asetusta käytettäessä ajoitus hidastuu, koska rinnakkainen käsittely ei ole käytössä.

## <a name="planned-orders-take-a-long-time-to-update"></a>Suunniteltujen tilausten päivittäminen kestää kauan

### <a name="issue-description"></a>Ongelman kuvaus

Suunnittelun tilauksen tarpeen määrää ja/tai toimituspäivää päivitettäessä päivityksen tallentaminen kestää tilauskohtaisesti tyypillisesti vähintään 30 sekuntia.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Tämä on tunnettu sisäisen pääsuunnittelumoduulin ongelma. Se johtuu taustalla olevasta tuoterakenteen automaattisesta hajotuksesta muokkausten aikana. Tämä ongelma korjataan suunnittelun optimoinnissa, jossa suunnittelija voi päivittää ja hyväksyä tilauksia ja sitten halutessaan käynnistää suunnitteluajon, joka päivittää taustatuoterakenteen suunnittelutilaukset.

Sisäisen pääsuunnittelumoduulin suorituskykyä voi parantaa seuraavasti:

1. Siirry kohtaan **Pääsuunnittelu \> Määritykset \> Suunnitelmat \> Pääsuunnitelmat**.
1. Valitse suunnitelma.
1. Laajenna **Aikarajat päivissä** -pikavälilehti.
1. Määritä **Hajotus**-asetukseksi *Kyllä* ja määritä tämän asetuksen alla olevaan kenttään 0 (nolla).

> [!NOTE]
> Tämä rajoittaa kyseisessä pääsuunnitelmassa suoritetut hajotukset yhteen päivään.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]