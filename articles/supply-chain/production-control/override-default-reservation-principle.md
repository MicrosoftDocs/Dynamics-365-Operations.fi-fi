---
title: Tuotannon materiaalien oletusvarausperiaatteen ohittaminen
description: Tässä aiheessa käsitellään kunkin nimikemalliryhmän oletusvarausperiaatteen määrittämistä siten, että kussakin tuotannon tuoterakenteen tai erätilauskaavan nimikkeessä käytetään automaattisesti eri varausperiaatetta.
author: johanhoffmann
ms.date: 12/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-10
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: eb4200deed5407bef6861913cecdad7114ea68cc
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270784"
---
# <a name="override-the-default-reservation-principle-for-materials-in-production"></a>Tuotannon materiaalien oletusvarausperiaatteen ohittaminen

[!include [banner](../includes/banner.md)]

*Ohita tuotannon oletusvaraus* -toiminnolla voidaan määrittää kunkin nimikemalliryhmän oletusvarausperiaate. Niinpä kussakin tuotannon tuoterakenteen tai erätilauskaavan nimikkeessä käytetään automaattisesti eri varausperiaatetta. Voit valita, ohittaako jokainen nimikemalliryhmä tilaukselle määritetyn oletusvarausperiaatteen ja mitä varausperiaatetta käytetään sen tilalla (*manuaalinen*, *arvio*, *aikataulutus*, *vapautus* tai *aloitus*).

Uutta tuotantotilausta tai erätilausta luotaessa pyydetään valitsemaan varausperiaate, jota on käytettävä kyseisessä tilauksessa ja sen kaikilla tuoterakenneriveillä tai kaavariveillä. *Ohita tuotannon oletusvaraus* -toimintoa käytettäessä osa tuoterakenne- tai kaavariveistä tai kaikki kyseiset rivit voivat ohittaa kyseisen varausperiaatteen ja käyttää sen sijaan soveltuvalle nimikemalliryhmälle määritettyä varausperiaatetta.

Jos esimerkiksi raaka-aineet tai ainesosat edellyttävät keräilytyötä, kyseisille tuotteille luodut tuoterakenne- tai kaavarivit edellyttävät fyysistä varausta, koska fyysinen varaus on varastotyön luonnin edellytys. Jos varauksen halutaan tapahtuvan automaattisesti, yleensä valitaan jokin seuraavista varausperiaatteista: *arvio*, *aikataulutus*, *vapautus* tai *aloitus*. Jos materiaalit tai ainesosat eivät kuitenkaan edellytä keräilytyötä, koska ne kulutetaan suojaan sijainnista, *manuaalinen* varausperiaate valitaan yleensä sen vuoksi, että mitään varauksia ei tehdä eikä keräilytöitä luoda.

## <a name="turn-on-the-feature"></a>Toiminnon ottaminen käyttöön

Ennen kuin käytät toimintoa, se on otettava käyttöön järjestelmässä. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Tuotannonhallinta*
- **Toiminnon nimi:** *Ohita tuotannon oletusvaraus*

## <a name="assign-a-production-reservation-policy-to-an-item-model-group"></a>Tuotannon varauskäytännön määrittäminen nimikemalliryhmään

1. Valitse **Kustannusten hallinta \> Varaston kirjanpitokäytäntöjen määrittäminen \> Nimikemalliryhmät**.
1. Luo tai valitse nimikemalliryhmä.
1. Valitse **Varastokäytännöt**-pikavälilehdessä **Ohita nimikkeen tuotantovaraus** -valintaruutu.
1. Valitse **Varaus**-kentässä valittuun malliryhmään kuuluvien nimikkeiden varausperiaate. (Nämä nimikkeet sisältävät tuoterakenne- tai kaavarivillä olevat nimikkeet.)

    - **Manuaalinen** – Malliryhmän nimikkeille ei tehdä automaattisesti tuotannon fyysistä varausta. Ne voidaan kuitenkin varata tarvittaessa manuaalisesti.
    - **Arvio** – malliryhmän nimikkeet varataan fyysisesti tuotantotilauksen arvioinnin aikana.
    - **Aikataulutus** – malliryhmän nimikkeet varataan fyysisesti tuotantotilauksen aikataulutuksen aikana.
    - **Vapautus** – malliryhmän nimikkeet varataan fyysisesti, kun tuotantotilaus vapautetaan.
    - **Aloitus** – malliryhmän nimikkeet varataan fyysisesti tuotantotilausta aloitettaessa.

## <a name="example-using-reservation-principles-in-a-bulkpack-scenario"></a>Esimerkki: varausperiaatteiden käyttäminen bulkki- ja pakkausskenaariossa

Irtotavaravoiteluainetta tuotetaan 1 000 litran miksauslaitteessa. Kun irtotavara on valmis, se pumpataan useisiin täyttöasemiin, joissa erikokoiset pullot täytetään. Kun pullot on täytetty, ne pakataan laatikkoihin. Kyseiset laatikot pakataan sitten kuormalavoille.

Tässä skenaariossa luodaan erätilaus tuottamaan 1 000 litraa irtotavaraa. (Tämä tilaus on irtotavaratilaus.) Kun tämä erätilaus on valmis, se raportoidaan valmiina täyttöasemien materiaalin syöttösijaintiin. Sen jälkeen luodaan erätilaus täyttämään ja pakkaamaan jokainen pullokoko. (Nämä tilaukset ovat pakkaustilauksia.) Pakkaustilauksissa on kaava, joka koostuu irtotavarasta, tyhjästä pullosta, etiketistä ja muista pakkausmateriaaleista. Koska irtotavara siirtyy suoraan miksauslaitteesta täyttöasemiin, tämän ainesosan keräämiseen ei tarvita varastotyötä ja irtotavara kulutetaan suoraan syöttösijainnista. Tämän vuoksi varausperiaatteeksi on määritetty *manuaalinen*. Muut materiaalit on vaiheistettu täyttöasemaan keräilytyön avulla. Niinpä kyseisten rivin varausperiaatteeksi on määritetty esimerkiksi *vapautus*, jolloin varaus tehdään automaattisesti, kun pakkaustilaus vapautetaan.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]