---
title: "Täydennys"
description: "Tässä artikkelissa käsitellään täydennysstrategioita, joita voi käyttää varastonhallinnan toimintoja käyttävissä varastoissa."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSReplenishmentTemplates
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 90043
ms.assetid: 49fa97eb-8e10-49a5-9261-1e393159f178
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 77b895e7f7edd6f22ee960ba2ec4bdd2931c29f8
ms.lasthandoff: 03/31/2017


---

# <a name="replenishment"></a>Täydennys

Tässä artikkelissa käsitellään täydennysstrategioita, joita voi käyttää varastonhallinnan toimintoja käyttävissä varastoissa.

Tässä artikkelissa käsitellään täydennysstrategioita, joita voi käyttää varastonhallinnan toimintoja käyttävissä varastoissa. Tiedot eivät koske Inventoinnin- ja varastonhallinnassa käytettävissä olevaa varastoratkaisua. Käytettävissä on kolmen täydennysstrategiaa:

-   **Aallon kysynnän täydennys** – Tämä strategia luo lähteville tilausten tai kuormien täydennystyön, jos varasto ei ole käytettävissä, kun aalto luo työt. Täydennystyö voidaan esimerkiksi luoda, jos myyntitilaukseen vaadittava määrä ei ole käytettävissä, kun aalto käsitellään.
-   **Vähimmäis- tai enimmäistäydennys** – Tässä strategiassa varastoinnin vähimmäis-ja enimmäisrajoilla määritetään, milloin sijainnit on täydennettävä. Nimike ja sijaintiehto määrittävät varaston, joka arvioidaan täydennystä varten. Vähimmäis- tai enimmäistäydennykset malli ovat ensisijainen mekanismi optimaalisten tasojen ylläpitämiseksi keräilysijainneissa. Voit kysynnän täydennyksen avulla varmistaa, että varastoa riittää aallon kysyntään vastaamiseen. Tämä toimii vähimmäis- ja enimmäistäydennysjaksojen välisenä täydennyksenä:
-   **Kuorman kysynnän täydennys** – Tässä strategiassa summataan useiden kuormien kysyntä ja luodaan täydennystyö, jota tarvitaan varaston täyttämiseen liittyvissä keräilysijainneissa. Tämä strategia auttaa varmistamaan, että luodut kuormat voidaan kerätä varastosta vapauttamisen jälkeen.

Täydennystyö luodaan täydennysmallin perusteella kaikissa kolmessa strategiassa.

## <a name="wave-demand-replenishment"></a>Aallon kysynnän täydennys
Aallon kysynnän täydennys luo kysynnän mukaan täydennystyön, jos lähtevien tilausten tai kuormien määrä ei ole käytettävissä, kun aalto luo työn. Täydennysmallissa on tietoja nimikkeen ehdoista, mittayksiköstä, kysynnän lisäyksestä ja sijainnista. 

Sijaintidirektiiveillä määritetään, mitä sijaintia on täydennettävä. Nämä sijaintidirektiivit linkitetään täydennysmalliin **Direktiivikoodi**-kentässä. Jos **Direktiivikoodi**-kenttää ei ole määritetty, käytettävä suuntadirektiivi määritetään kyselyillä. Huomaa, että jos direktiivikoodia ei ole määritetty täydennysmallissa ja sijaintidirektiivillä on direktiivikoodi, sijaintidirektiivi ohitetaan, vaikka sijaintidirektiivikysely olisi oikein. Keräilysijaintidirektiivillä määritetään, mistä varaston täydennys hankitaan. 

Mallin luonnin lisäksi voit määrittää joitakin täydennysasetuksia aaltomallissa. Aaltomallissa on oltava täydennysaaltovaihe, joka suoritetaan vain, jos nimikkeen kohdistus ei onnistunut. Täydennysaaltovaihe käyttää aaltovaihekoodia käytettävän täydennysmallin määrittämiseen. Täydennysaaltovaiheen lisäksi on varmistettava, että aaltomallin **Menetelmät**-kohdassa on valittu **täydennä**. 

**Täydennysmalli**-sivulla on **Salli aallon kysynnän käyttää varaamattomia määriä** -valintaruutu. Valitse tämä valintaruutu, jos haluat, että kysynnän täydennys vähentää varaamattomia määriä valitusta täydennysmallista luodusta työstä. Tämä valintaruutu on valittava jokaisessa aiemmin luodussa täydennysmallissa, jotta kysynnän täydennysmallit voisivat käyttää tätä logiikkaa. Kun kysynnän täydennys käynnistyy varastossa, se vähentää kysyntää nykyiseltä täydennystyöltä, jolla on varaamattomia määriä, jos työn alkuperä on täydennysmalleissa, joissa **Salli aallon kysynnän käyttää varaamattomia määriä** -valintaruutu on valittuna.

## <a name="minmax-replenishment"></a>Vähimmäis- tai enimmäistäydennys
Vähimmäis- tai enimmäistäydennyksessä varastoa täydennetään niin, että on määritettyjen vähimmäis- ja enimmäisrajojen välillä. Yleensä tämä prosessi tapahtuu kerran päivässä, mikä auttaa varmistamaan, että kaikki keräilysijainnit on täytetty enimmäistasolle ennen keräilyn aloittamista. 

Vähimmäis- ja enimmäissummat määritetään täydennysmallissa. Monet muut mallin asetukset muistuttavat aallon kysynnän täydennyksessä käytettäviä malleja. Mallissa on oltava yksi rivi kullekin nimikkeelle ja sijainnille. Kun täydennys suoritetaan käyttämällä erätyötä, Microsoft Dynamics 365 for Operations tarkistaa täydennyksen tarpeen siinä järjestyksessä, johon rivit on järjestetty. 

Huomaa, vähimmäis- ja enimmäistäydennysstrategia ei voi täydentää tyhjää sijaintia, ellei sijaintia ole määritetty nimikkeen kiinteästi sijainniksi. Jos täydennettävä sijainti ei ole kiinteä sijainti, Dynamics 365 for Operations ei voi määrittää täydennettävää nimikettä. Niinpä ennen täydennystä tarvitaan ainakin varastosaldo.

## <a name="load-demand-replenishment"></a>Kuorman kysynnän täydennys
Kuorman kysynnän täydennys summaa useiden kuormien kysynnän ja luo täydennystyön, jota tarvitaan varaston täyttämiseen liittyvissä keräilysijainneissa. Kuorman kysynnän täydennys muistuttaa monin tavoin aallon kysynnän täydennystä. Suurin on siinä, miten ja milloin kuorman kysynnän täydennys ja aallon kysynnän täydennys suoritetaan. Vähimmäis- tai enimmäistäydennyksen tavoin kuorman kysynnän täydennys suoritetaan käyttämällä erätyötä. Voit määrittää erätyön valitsemalla **Kuorman kysynnän täydennys** -sivulla käytettävän täydennysmallin ja määrittämällä suodatinkyselyn, joka määrittää kysynnän määrittämisessä käytettävät kuormat. Sijaintikysely määrittää sijainnit, joista käytettävissä olevat määrät vähennetään kuormien koottuun kysyntään vastaamiseksi.

## <a name="replenishment-prerequisites"></a>Täydennyksen edellytykset
| Edellytys            | Kuvaus                                                                                                                                                                                                                                        |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nimike                    | Nimike on otettava käyttöön varastonhallintaprosesseille.                                                                                                                                                                                       |
| Varasto               | Varastossa on oltava käytössä varastonhallintaprosessit. Valitse **Varastot**-sivulta varasto ja sitten **Käytä varastonhallintaprosesseja** -vaihtoehto, jos haluat aktivoida varaston varastonhallintaprosesseja varten. |
| Täydennysmallit | Vähimmäis- tai enimmäistäydennykselle, aallon kysynnän täydennykselle tai kuorman kysynnän täydennykselle on määritettävä vähintään yksi täydennysmalli.                                                                                                             |
| Sijainnit               | Sijainnit on luotava ja liitettävä sijaintiprofiiliin.                                                                                                                                                                                     |
| Sijaintiprofiilit       | Sijaintiprofiilit tarvitaan sijaintien luontiin.                                                                                                                                                                                       |
| Sijaintidirektiivit     | Sijaintidirektiivejä tarvitaan ohjaamaan työ sijainteihin, joissa täydennystä tarvitaan, ja sijainteihin, jotka ovat varaston lähteenä.                                                                                     |
| Työmallit          | **Täydennys** tyyppisiä työmalleja tarvitaan luomaan täydennystyö, jolla varasto voidaan siirtää haluttuun sijaintiin.                                                                                           |




