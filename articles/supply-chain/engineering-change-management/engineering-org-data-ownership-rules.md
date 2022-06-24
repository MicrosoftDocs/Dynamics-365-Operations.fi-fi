---
title: Suunnitteluyritykset ja tietojen omistussäännöt
description: Tässä artikkelissa käsitellään, miten yhden tai usean suunnitteluyrityksen avulla voidaan varmistaa, että tuotteiden päätiedot luodaan ja että niitä ylläpidetään keskitetysti. Suunnitteluyritys on yritys, joka omistaa suunnittelutuotteet ja sen suunnitteluun liittyvät tiedot.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgEngineeringOrganization
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 47662203669d5dd466990be397c9a4aaf1dd9932
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875536"
---
# <a name="engineering-companies-and-data-ownership-rules"></a>Suunnitteluyritykset ja tietojen omistussäännöt

[!include [banner](../includes/banner.md)]

## <a name="engineering-companies-and-operational-companies"></a>Suunnitteluyritykset ja operatiiviset yritykset

Tuotteiden päätietojen keskitetty luonti ja ylläpito voidaan varmistaa luomalla vähintään yksi *suunnitteluyritys*. Suunnitteluyritys omistaa suunnittelutuotteet ja niiden suunnitteluun liittyvät tiedot. Se on aina yhdistetty (perustuu) aiemmin luotuun *yritykseen*. Järjestelmä luo tämän yhteyden kautta keskitetyn aloituskohdan kaikille suunnitteluyrityksen suunnittelutuotteiden suunnitteluun liittyville tiedoille. Suunnittelutuotteet luodaan ja suunnitteluun liittyviä tietoja ylläpidetään tässä keskitetyssä aloituskohdassa. Suunnittelutuotteet ja suunnitteluun liittyvät tiedot vapautetaan siitä *operatiivisiin yrityksiin*. (Lisätietoja vapautuksen hallinnasta on kohdassa [Tuoterakenteiden vapauttaminen](release-product-structure.md).) Nämä operatiiviset yritykset käyttävät suunnittelutietoja suunnitteluyrityksen suunnittelemalla tavalla. Mahdollisia logistiikkatietoja ylläpidetään paikallisesti kussakin suunnitteluyrityksessä ja operatiivisessa yrityksessä.

Suunnitteluyritys luodaan valitsemalla **Suunnittelun muutostenhallinta \> Määritys \> Suunnitteluorganisaatiot**. Valitse **Uusi**, anna suunnitteluyritykselle nimi ja valitse aiemmin luotu yritys, johon se perustuu.

Jos ulkoinen tuotteen elinkaaren hallintajärjestelmä ollaan integroimassa, on luotava liiketoimintoyksikkö (yritystyyppi), josta tulee ulkoinen yritys.

## <a name="engineering-product-categories-and-engineering-companies"></a>Suunnittelun tuoteluokat ja suunnitteluyritykset

*Suunnittelun tuoteluokkien* avulla voidaan varmistaa, että suunnittelutuotteet luodaan yrityksen liiketoimintasääntöjen mukaisesti ja että toimivat edellytetyllä tavalla. Lisätietoja suunnittelun tuoteluokista on kohdassa [Suunnitteluversiot ja suunnittelun tuoteluokat](engineering-versions-product-category.md).

Kukin suunnittelun tuoteluokka kuuluu tiettyyn suunnitteluyritykseen, ja se voi luoda vain kyseiseen yritykseen kuuluvia tuotteita. Samalla tavoin myös oikeus ylläpitää suunnittelutuotetta kuuluu yritykselle, joka on liitetty kyseisen tuotteen suunnittelun tuoteluokkaan.

## <a name="data-that-is-owned-by-the-engineering-company"></a>Suunnitteluyrityksen omistamat tiedot

Koska suunnitteluyritys omistaa suunnitteluun liittyvät tiedot, se hallitsee seuraavia prosesseja:

- **Suunnittelutuotteiden luonti:** Kukin suunnitteluyritys voi luoda vain omistamaansa suunnittelun tuoteluokkaan perustuvia uusia suunnittelutuotteita. Joissakin tapauksissa operatiiviset yritykset ylläpitävät omia paikallisia kyseisiin tuotteisiin liittyviä tietoja.
- **Suunnitteluversioiden luonti:** Kun yritys luo uuden suunnittelutuotteen, järjestelmä luo automaattisesti sen ensimmäisen suunnitteluversion. Vain omistava suunnitteluyritys voi luoda uusia versioita kyseisestä tuotteesta.
- **Suunnittelumääritteiden luonti ja ylläpito:** Kun yritys luo uuden suunnittelutuotteen, järjestelmä lisää suunnittelumääritteet siihen automaattisesti. Vain omistava suunnitteluyritys voi luoda ja ylläpitää kyseisten määritteiden arvoja. Lisätietoja suunnittelumääritteistä on kohdassa [Suunnittelumääritteet ja suunnittelumääritteiden haku](engineering-attributes-and-search.md).
- **Suunnitteluversioihin yhdistettyjen tuoterakenteiden luonti ja ylläpito:** Omistava yritys voi yhdistää tuoterakenteen suoraan suunnittelutuotteen versioon. Kun nämä tuoterakenteet vapautetaan muihin yrityksiin, tuoterakenteen suunnittelutietojen muutoksissa on seuraavat rajoitukset:

    - Operatiivinen yritys ei saa poistaa vapautettuja tuoterakenteen rivejä.
    - Tuoterakenteen rivien suunnittelukentät ovat vain luku -muotoisia operatiivisessa yrityksessä. Kaikki muut kentät ovat logistisia toteutuskenttiä, joita operatiivinen yritys voi muokata.
    - Operatiivinen yritys voi lisätä tuoterakenteen rivejä samaan tuoterakenteeseen. Tällä tavoin se voi tehdä paikallisia lisäyksiä, kuten pakkausmateriaaleja tai voiteluaineita.
    - Operatiivinen yritys voi lisätä täysin uuden, paikallisen tuoterakenteen. Tämä muutos voi olla välttämätön esimerkiksi tapauksissa, joissa vapautukseen ei sisälly tuoterakennetta. Operatiivinen yritys omistaa nämä paikalliset tuoterakenteet ja ylläpitää niitä. Lisätietoja vapautuksen hallinnasta on kohdassa [Tuoterakenteiden vapauttaminen](release-product-structure.md).
    - Kaikki paikalliset tuoterakenteet ja tuoterakenteen rivit säilytetään, kun suunnitteluyritys päivittää tuoterakenteen.

- **Suunnitteluversioihin yhdistettyjen reititysten luonti ja ylläpito:** Omistava yritys voi yhdistää reitityksen suoraan kuhunkin suunnitteluversioon. Kun nämä reititykset vapautetaan muihin yrityksiin, reititysten suunnittelutietojen muutoksissa on seuraavat rajoitukset:

    - Muut yritykset eivät voi poistaa reititysten suunnittelutietoja.
    - Muut yritykset voivat lisätä toimintoja reititykseen. Tällä tavoin ne voivat lisätä paikallisia reititysvaiheita.
    - Operatiiviset yritykset voivat lisätä täysin uusia, paikallisia reitityksiä. Tämä muutos voi olla välttämätön, jos vapautukseen ei esimerkiksi ole sisällytetty reitityksiä. Operatiiviset yritykset omistavat nämä paikalliset reititykset ja ylläpitävät niitä. Lisätietoja vapautuksen hallinnasta on kohdassa [Tuoterakenteiden vapauttaminen](release-product-structure.md).
    - Kaikki paikallisesti tehdyt muutokset säilytetään, kun suunnitteluyrityksen päivitykset vapautetaan uudelleen reitityksiin.

- **Suunnitteluasiakirjojen luonti ja ylläpito:** Suunnitteluyritys voi liittää suunnitteluasiakirjoja kuhunkin suunnitteluversioon.

    - Kun nämä asiakirjat vapautetaan muihin yrityksiin, asiakirjat on suojattu siten, että operatiivinen yritys ei voi poistaa niitä.
    - Muut yritykset voivat lisätä täysin uusia paikallisia asiakirjoja. Operatiivinen yritys omistaa nämä paikalliset asiakirjat ja ylläpitää niitä.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]