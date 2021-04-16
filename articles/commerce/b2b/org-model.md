---
title: Organisaation mallinnushierarkioiden luominen B2B-organisaatioille
description: Tässä aiheessa kuvataan, miten luodaan organisaation mallinnushierarkioita B2B-organisaatioille.
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 487af939f92ece8bc3e543b3beeffa239baa1863
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799826"
---
# <a name="create-org-modeling-hierarchies-for-b2b-organizations"></a>Organisaation mallinnushierarkioiden luominen B2B-organisaatioille

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kuvataan, miten luodaan organisaation mallinnushierarkioita B2B-organisaatioille Microsoft Dynamics 365 Commercessa.

Commerce headquarters -sovelluksessa liikekumppaniorganisaatioita edustavat asiakas- ja asiakashierarkiayksiköt. Liikekumppaniorganisaatio ja sen käyttäjät esitetään asiakkaina, ja asiakashierarkioiden avulla nämä asiakkaat liitetään toisiinsa.

Kun liikekumppanin pyyntö liittyä B2B-verkkokauppasivustoon hyväksytään, suoritetaan seuraavat toimenpiteet:

- Järjestelmään luodaan kaksi uutta asiakastietuetta: liikekumppaniorganisaation **Tyyppi – organisaatio** -asiakastietue ja pyytäjän (eli liikekumppanin käyttäjä, joka lähetti pyynnön) **Tyyppi – henkilö** -asiakastietue.
- Luodaan uusi asiakashierarkiatietue kohdassa **Asiakas \> Asiakashierarkia**. Tietueella on seuraavat otsikko-ominaisuudet:

    - **Asiakashierarkian tunnus** – Asiakashierarkian yksilöivä tunnus. Tämä tunnus käyttää Commerce headquarters -parametrien Commercen jaetuissa parametreissa määritettyä numerosarjaa.
    - **Nimi** – Liikekumppanin organisaationimi, joka on määritetty rekisteröintipyynnössä.
    - **Tarkoitus** – Tämä ominaisuus on määritetty ennalta määritetylle arvolle **B2B-organisaatio**.
    - **Organisaatio** – Liikekumppanin asiakastunnus.

Seuraavassa on asiakashierarkiatietueen tiedot:

- Pyytäjän asiakastietue on liitetty asiakashierarkiaan.
- Järjestelmänvalvojan rooli on liitetty pyytäjään.

Kun järjestelmänvalvoja lisää käyttäjiä B2B-sivuston liikekumppaniorganisaatioon, kullekin käyttäjälle luodaan uusi asiakastietue Commerce headquarters -sovelluksessa. Tämä asiakastietue lisätään myös liikekumppanin asiakashierarkiatietueeseen, ja sen rooli on "käyttäjä".

> [!NOTE]
> Useimmissa tapauksissa hierarkian kaikkien asiakastietueiden vastaavat ominaisuuksien arvot pitäisi vastata toisiaan. Esimerkiksi koska kaikkien liikekumppanien käyttäjien tulisi saada samanlaisia hintoja tuotteille, hintaryhmän ja siihen liittyvien konfiguraatioiden tulisi täsmätä. Järjestelmä ei kuitenkaan pakota tämän yhdenmukaisuuden noudattamista. Siksi relevantit Commerce headquarters -käyttäjät ovat vastuussa siitä, että ominaisuusarvot ja konfiguroinnit vastaavat toisiaan annetun hierarkian kaikille asiakkaille.

Commerce headquarters -käyttäjät voivat tarkastella hierarkian kaikkien asiakastietueiden ominaisuusarvoja vierekkäisessä näkymässä. Valitse asianmukaisen asiakastietueen ominaisuudet valitsemalla välilehtien nimet avattavasta valikosta. Käyttäjät voivat tarkastella ja muokata ominaisuusarvoja suoraan tässä näkymässä. Vaihtoehtoisesti voit ottaa järjestelmänvalvojan asiakastietueen kaikki arvot käyttöön kaikissa käyttäjäasiakastietueissa valitsemalla **Ohita**-vaihtoehdon asiakashierarkian tiedoissa.

## <a name="additional-resources"></a>Lisäresurssit

[B2B-verkkokauppasivuston määrittäminen](set-up-b2b-site.md)

[Liikekumppanikäyttäjien hallinta B2B-verkkokauppasivustoissa](manage-b2b-users.md)

[Asiakastilin maksutavan määrittäminen B2B-verkkokauppasivustoille](payment-method.md)

[Tuotemäärän rajojen asettaminen B2B-verkkokauppasivustoille](quantity-limits.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]