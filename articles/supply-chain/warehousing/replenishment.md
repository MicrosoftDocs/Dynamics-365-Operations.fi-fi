---
title: Täydennys – yleiskatsaus
description: Tässä ohjeaiheessa käsitellään täydennysstrategioita, joita voi käyttää varastonhallinnan toimintoja käyttävissä varastoissa.
author: Mirzaab
ms.date: 02/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSReplenishmentTemplates, WHSInventFixedLocation, WHSRequestType
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "90043"
- intro-internal
ms.assetid: 49fa97eb-8e10-49a5-9261-1e393159f178
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e381af433eb3041d92ddfe375e6b4c75c1feb7c2
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/03/2021
ms.locfileid: "6335817"
---
# <a name="replenishment-overview"></a>Täydennys – yleiskatsaus

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään täydennysstrategioita, joita voi käyttää varastonhallinnan toimintoja käyttävissä varastoissa. Tiedot eivät koske Inventoinnin- ja varastonhallinnassa käytettävissä olevaa varastoratkaisua.

Seuraavat täydennysstrategiat ovat käytettävissä:

- **Aallon kysynnän täydennys** – Tämä strategia luo lähteville tilausten tai kuormien täydennystyön, jos varasto ei ole käytettävissä, kun aalto luo työt. Täydennystyö voidaan esimerkiksi luoda, jos myyntitilaukseen vaadittava määrä ei ole käytettävissä, kun aalto käsitellään.
- **Vähimmäis- tai enimmäistäydennys** – Tässä strategiassa varastoinnin vähimmäis-ja enimmäisrajoilla määritetään, milloin sijainnit on täydennettävä. Nimike ja sijaintiehto määrittävät varaston, joka arvioidaan täydennystä varten. Vähimmäis- tai enimmäistäydennykset malli ovat ensisijainen mekanismi optimaalisten tasojen ylläpitämiseksi keräilysijainneissa. Voit kysynnän täydennyksen avulla varmistaa, että varastoa riittää aallon kysyntään vastaamiseen. Tämä toimii vähimmäis- ja enimmäistäydennysjaksojen välisenä täydennyksenä:
- **Kuorman kysynnän täydennys** – Tässä strategiassa summataan useiden kuormien kysyntä ja luodaan täydennystyö, jota tarvitaan varaston täyttämiseen liittyvissä keräilysijainneissa. Tämä strategia auttaa varmistamaan, että luodut kuormat voidaan kerätä varastosta vapauttamisen jälkeen.
- **Välitön täydennys** – tällä menetelmällä varasto täydennetään ennen kuin aalto suoritetaan, jos kohdistus epäonnistuu sijaintidirektiivin riville, jolla on täydennysmalli. 

Täydennystyö luodaan täydennysmallin perusteella kaikissa neljässä strategiassa.

## <a name="wave-demand-replenishment"></a>Aallon kysynnän täydennys
Aallon kysynnän täydennys luo kysynnän mukaan täydennystyön, jos tuotantotilausten, kanbanien, lähtevien tilausten tai kuormien määrä ei ole käytettävissä, kun aalto luo työn. Täydennysmallissa on tietoja nimikkeen ehdoista, mittayksiköstä, kysynnän lisäyksestä ja sijainnista. 

Sijaintidirektiiveillä määritetään, mitä sijaintia on täydennettävä. Nämä sijaintidirektiivit linkitetään täydennysmalliin **Direktiivikoodi**-kentässä. Jos **Direktiivikoodi**-kenttää ei ole määritetty, käytettävä suuntadirektiivi määritetään kyselyillä. Huomaa, että jos direktiivikoodia ei ole määritetty täydennysmallissa ja sijaintidirektiivillä on direktiivikoodi, sijaintidirektiivi ohitetaan, vaikka sijaintidirektiivikysely olisi oikein. Keräilysijaintidirektiivillä määritetään, mistä varaston täydennys hankitaan. 

Mallin luonnin lisäksi voit määrittää joitakin täydennysasetuksia aaltomallissa. Aaltomallissa on oltava täydennysaaltovaihe, joka suoritetaan vain, jos nimikkeen kohdistus ei onnistunut. Täydennysaaltovaihe käyttää aaltovaihekoodia käytettävän täydennysmallin määrittämiseen. Täydennysaaltovaiheen lisäksi on varmistettava, että aaltomallin **Menetelmät**-kohdassa on valittu **Täydennä**. 

**Täydennysmalli**-sivulla on **Salli aallon kysynnän käyttää varaamattomia määriä** -valintaruutu. Valitse tämä valintaruutu, jos haluat, että kysynnän täydennys vähentää varaamattomia määriä valitusta täydennysmallista luodusta työstä. Tämä valintaruutu on valittava jokaisessa aiemmin luodussa täydennysmallissa, jotta kysynnän täydennysmallit voisivat käyttää tätä logiikkaa. Kun kysynnän täydennys käynnistyy varastossa, se vähentää kysyntää nykyiseltä täydennystyöltä, jolla on varaamattomia määriä, jos työn alkuperä on täydennysmalleissa, joissa **Salli aallon kysynnän käyttää varaamattomia määriä** -valintaruutu on valittuna.

**Täydennysyksikkö** on täydennyksen vähimmäisyksikkö. Tämän on oltava kokonaisluku, joka on yksikön kerrannainen. Järjestelmä pyöristää ylöspäin suurimpaan mahdolliseen yksikköön työtä luotaessa.

Kysynnän täydennystä tuetaan myyntitilauksissa, siirtotilauksissa, tuotantotilauksissa ja kanbaneissa. 

## <a name="minmax-replenishment"></a>Vähimmäis- tai enimmäistäydennys
Vähimmäis- tai enimmäistäydennyksessä varastoa täydennetään niin, että on määritettyjen vähimmäis- ja enimmäisrajojen välillä. Yleensä tämä prosessi tapahtuu kerran päivässä, mikä auttaa varmistamaan, että kaikki keräilysijainnit on täytetty enimmäistasolle ennen keräilyn aloittamista. 

Vähimmäis- ja enimmäissummat määritetään täydennysmallissa. Monet muut mallin asetukset muistuttavat aallon kysynnän täydennyksessä käytettäviä malleja. Mallissa on oltava yksi rivi kullekin nimikkeelle ja sijainnille. Kun suoritat täydennyksen käyttämällä erätyötä, järjestelmä tarkistaa täydennyksen tarpeen siinä järjestyksessä, johon rivit on järjestetty. 

Huomaa, vähimmäis- ja enimmäistäydennysstrategia ei voi täydentää tyhjää sijaintia, ellei sijaintia ole määritetty nimikkeen kiinteästi sijainniksi. Jos täydennettävä sijainti ei ole kiinteä sijainti, järjestelmä ei voi määrittää täydennettävää nimikettä. Niinpä ennen täydennystä tarvitaan ainakin varastosaldo.

## <a name="load-demand-replenishment"></a>Kuorman kysynnän täydennys
Kuorman kysynnän täydennys summaa useiden kuormien kysynnän ja luo täydennystyön, jota tarvitaan varaston täyttämiseen liittyvissä keräilysijainneissa. Kuorman kysynnän täydennys muistuttaa monin tavoin aallon kysynnän täydennystä. Suurin on siinä, miten ja milloin kuorman kysynnän täydennys ja aallon kysynnän täydennys suoritetaan. Vähimmäis- tai enimmäistäydennyksen tavoin kuorman kysynnän täydennys suoritetaan käyttämällä erätyötä. Voit määrittää erätyön valitsemalla **Kuorman kysynnän täydennys** -sivulla käytettävän täydennysmallin ja määrittämällä suodatinkyselyn, joka määrittää kysynnän määrittämisessä käytettävät kuormat. Sijaintikysely määrittää sijainnit, joista käytettävissä olevat määrät vähennetään kuormien koottuun kysyntään vastaamiseksi.

## <a name="immediate-replenishment"></a>Välitön täydennys
Sen sijaan, että kysyntä laskettaisiin yhteen kohdistusprosessin lopussa ja täydennys tehtäisiin yhteenlasketun määrän perusteella, voit käyttää välitöntä täydennysstrategiaa. Tätä strategiaa käytettäessä varaston voi täydentää heti, kun sijaintidirektiivin rivi epäonnistuu. Näin voit määrittää täydennyksen siten, että se on rajoitettu tiettyihin yksiköihin ja että se käyttää tiettyjä sijainteja koskevia määriä.

## <a name="replenishment-prerequisites"></a>Täydennyksen edellytykset

|      Edellytys       |                                                                                                                                kuvaus                                                                                                                                 |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|          Nimike           |                                                                                                        Nimike on otettava käyttöön varastonhallintaprosesseille.                                                                                                        |
|        Varasto        | Varastossa on oltava käytössä varastonhallintaprosessit. Valitse <strong>Varastot</strong>-sivulta varasto ja sitten <strong>Käytä varastonhallintaprosesseja</strong> -vaihtoehto, jos haluat aktivoida varaston varastonhallintaprosesseja varten. |
| Täydennysmallit |                                                                   Vähimmäis- tai enimmäistäydennykselle, aallon kysynnän täydennykselle tai kuorman kysynnän täydennykselle on määritettävä vähintään yksi täydennysmalli.                                                                   |
|        Sijainnit        |                                                                                                       Sijainnit on luotava ja liitettävä sijaintiprofiiliin.                                                                                                       |
|    Sijaintiprofiilit    |                                                                                                        Sijaintiprofiilit tarvitaan sijaintien luontiin.                                                                                                        |
|   Sijaintidirektiivit   |                                                       Sijaintidirektiivejä tarvitaan ohjaamaan työ sijainteihin, joissa täydennystä tarvitaan, ja sijainteihin, jotka ovat varaston lähteenä.                                                        |
|     Työmallit      |                                                   <strong>Täydennys</strong> tyyppisiä työmalleja tarvitaan luomaan täydennystyö, jolla varasto voidaan siirtää haluttuun sijaintiin.                                                    |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]