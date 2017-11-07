---
title: "Cross docking tuotantotilauksista lähtevien laituriin"
description: "Tässä ohjeaiheessa kerrotaan, miten valmiiksi ilmoitetun materiaalin cross docking -prosessia hallitaan tuotantolinjasta lähtevien laituriin."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a3f193b5b16406aa6ac3ed6a96f909318d100439
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="cross-docking-from-production-orders-to-outbound-docks"></a>Cross docking tuotantotilauksista lähtevien laituriin

Tässä ohjeaiheessa kerrotaan, miten valmiiksi ilmoitetun materiaalin cross docking -prosessia hallitaan tuotantolinjasta lähtevien laituriin.

<a name="introduction"></a>Johdanto
------------

Cross docking tuotannosta lähtevien sijaintiin on hyödyllinen valmistajille, joiden tuotantomäärät ovat suuria ja jotka haluavat lähettää valmiit tuotteet heti, kun tuotantolinja on ilmoittanut ne valmiiksi. Tuotteet on tarkoitus lähettää jakelukeskuksiin, jotka sijaitsevat asiakaskysynnän läheisyydessä, sen sijaan että varastoa koottaisiin valmistustoimipaikkaan.

Jos tuotteelle ei ole välitöntä kysyntää, sitä on säilytettävä valmistustoimipaikan varastosijainneissa. Tämä prosessi tunnetaan myös nimellä *opportunistinen cross docking*. Se ilmaisee, että jos tuotteen lähettämiselle ei ole kysyntää, mahdollisuus on käytettävä hyväksi sen sijaan, että tuote sijoitettaisiin sisäiseen varastoon.

Seuraavassa esimerkissä kolme on erilaista työnkulkua, jotka alkavat tuotantolinja päättyessä (2).

Tuote ilmoitetaan valmiiksi tuotannon tuotossijaintiin (3) ja trukin kuljettaja noutaa kuormalavan tästä sijainnista (3).

-   Jos tuotteen siirtämiseen valmistuksesta (1), jakelukeskuksen (7) on suunniteltu tehtävä (6), järjestelmä ohjeistaa trukin kuljettajan viemään kuormalavan lastausovelle (4).
-   Jos perävaunu on jo määritetty lastausovelle, kuorma-auton kuljettaja ohjataan lataamaan tuote suoraan perävaunuun.
-   Jos tuotteen siirrolle ei ole suunniteltua tehtävää, trukin kuljettaja ohjataan viemään tuote sisäiseen varastosijaintiin (5).

[![opportunistinen cross-docking](./media/scenario1.png)](./media/scenario1.png)

## <a name="configure-cross-docking"></a>Cross docking -määritys
Voit määrittää cross docking -prosessin **työkäytännöissä**. Työkäytäntö sisältää työtilaustyypin, paikan ja tuotteen. Seuraavassa esimerkissä cross docking määritetään tuotteelle X ja sijaintiin Y.

#### <a name="work-order-types"></a>Työtilaustyypit

-   Työtilaustyyppi: valmiiden tuotteiden poispano
-   Työn luontimentelmä: cross docking
-   Cross docking -käytännön nimi: siirtotilaukset

#### <a name="inventory-locations"></a>Varastosijainnit

-   Varasto: 51
-   Paikka: Y

#### <a name="products"></a>Tuotteet

-   Nimiketunnus: X

Tällä hetkellä cross docking voidaan määrittää vain kahdelle työtilaustyypille:

-   Valmiiden tuotteiden poispano
-   Rinnakkaistuotteen ja sivutuotteen poispano

**Cross docking -käytännössä** määritetään, mitä asiakirjatyyppejä cross docking koskee. Tällä hetkellä ainoa tuettu asiakirjatyyppi on **siirtotilaus**. Seuraavassa esimerkissä määritetään cross docking -käytäntö.

### <a name="cross-docking-policy-name-transfer-order"></a>Cross docking -käytännön nimi: siirtotilaus

-   Järjestysnumero: 10
-   Työtilaustyyppi: siirtovarasto-otto
-   Cross docking -tarve vaatii sijainnin: epätosi
-   Cross docking -strategia: päivämäärä ja aika

### <a name="sequence-number"></a>Järjestysnumero

**Järjestysnumero** ilmaisee asiakirjatyypin prioriteetin. Tällä hetkellä ainoa tuettu tyyppi on **siirtovarasto-otto**. Järjestysnumerolla onkin merkitystä vasta sitten, kun tuettavia tilaustyyppiä on useita.

### <a name="cross-docking-policy"></a>Cross docking -käytäntö

Cross docking -käytäntö määrittää myös siirtotilauksen kysynnän priorisointikäytännön. Jos esimerkiksi samalle tuotteelle on useita siirtotilauksia, kuormassa määritetty ja siirtotilaukseen liitetty ajoitettu päivämäärä ja aika määrittävät tilausten priorisointijärjestyksen. Ajoitettu päivämäärä ja aika voidaan määrittää suoraan kuormassa. Vaihtoehtoisesti ne voidaan määrittää kuormaan liitetyssä **ajoitetusta tapaamisesta**. Cross docking -strategia määrittää priorisoinnin. Tällä hetkellä on vain yksi strategia: **päivämäärä ja kellonaika**.

### <a name="cross-docking-demand-requires-location"></a>Cross docking -tarve vaatii sijainnin

Voit määrittää cross docking -käytännössä ehdon, jonka mukaan siirtotilauksiin on määritettävä sijainti, jota ilman sitä ei voi ottaa mukaan cross docking -prosessiin. Tämä ehto määritetään **Cross docking -tarve vaatii sijainnin** -kentässä. Kuormaan liitettyä ajoitetun tapaamisen sijaintia käytetään niiden tavaroiden lopullisena sijaintia, joissa käytetään cross dockingia. **Määritä**-työtilaustyypin **siirtovarasto-oton** sijaintidirektiivi määrittää niiden tavaroiden lopulllisen sijainnin, joissa käytetään cross dockingia. **Cross docking -tarve vaatii sijainnin** -kentän määrittäminen voi olla hyödyllistä skenaariossa, jossa valmiissa tavaroissa käytetään cross dockingia vain, jossa perävaunu on määritetty lastausovelle. Tässä skenaariossa tavarat siirretään suoraan tuotantolinjalta perävaunuun. Kun perävaunu on määritetty lastausovelle, käyttäjä määrittää sijainnin ajoitettuun tapaamiseen, jolloin sijainti tulee myös käytettäväksi cross dockingissa. Seuraavissa osissa käsitellään kaksi esimerkkiä.

#### <a name="scenario-1--cross-docking-from-production-to-transfer-orders"></a>Skenaario 1 – Cross docking tuotannosta siirtotilauksiin

Kun tuote on ilmoitettu valmiiksi tuotantolinjalla, se siirretään lastausovisijaintiin, jossa se lastataan kuorma-autoon ja siirretään jakelukeskukseen. Käytä yrityksen USMF:ää.

1.  Ota käyttöön uusi cross docking -numerosarja. Siirry **Numerosarjat**-sivulle ja valitse **Luo**-painike. Ohjattu toiminto opastaa prosessin vaiheissa.
2.  Luo cross docking -käytäntö. Siirry **Cross docking -käytäntö** -sivulle ja luo uusi **Cross docking siirtotilaukseen** -niminen käytäntö. Huomaa, että ainoa valittava työtilaustyyppi on **Siirtovarasto-otto** ja että ainoa käytettävissä oleva cross docking -strategia on **Päivämäärä ja kellonaika**.
3.  Luo työkäytäntö. Siirry **Työkäytännöt**-sivulle ja luo uusi **Cross dock L0101** -niminen työkäytäntö.
4.  Määritä kuormat siten, että ne luodaan siirtotilauksille automaattisesti. Määritä varastoparametreissa kuormat siten, että ne luodaan automaattisesti siirtotilauksia luotaessa. Kuorma on välttämätön, jotta cross dockingia voidan käyttää siirtotilauksessa.
5.  Määritä nimikkeiden kuormamääritys. Siirry **Nimikkeiden kuormamääritys** -sivulle ja määritä **CarAudio**-nimikeryhmälle vakiokuormamalli. Tämä yhdistämismääritys lisätään automaattisesti kuorman kuormamalliin siirtotilausta luotaessa.
6.  Luo siirtotilaus. Luo nimiketunnuksen L0101 siirtotilaus. Määrä = 20.
7.  Vapauta siirtotilaus kuormasuunnittelun työtilassa. Valitse **Lähetys**-välilehdessä kuormasuunnittelun työtilan valikkovaihtoehto. Valitse sitten kuormarivin **Vapauta**-valikossa **Vapauta varastoon**. Siirtotilauksessa on nyt tyypin **Siirtovarasto-otto** avoin aaltorivi.
8.  Luo tuotantotilaus. Siirry **Tuotantotilaus**-luettelosivulle ja luo tuotteen L0101 tuotantotilaus. Määrä = 20. Arvioi ja aloita tuotantotilaus. Huomaa, että **Kirjaa keräysluettelo nyt** -kentän arvo on edelleen **Ei**.
9.  Ilmoita valmiiksi mobiililaitteessa. Siirry mobiililaiteportaaliin ja valitse valikossa **Ilmoita valmiiksi ja pane pois**. Ilmoita nyt L0101 valmiiksi kämmenlaitteessa. Huomaa, että laittosijainti on **LASTAUSOVI**. Tämä sijainti löytyy **Määritä**-työtilaustyypin **Siirtovarasto-otto**-sijaintidirektiivistä. Huomaa myös, että **Siirtovarasto-otto**-tyypin työ on luotu ja valmis. Tarkista työ siirtymällä siirtotilaustyön tietoihin.
10. Yritä nyt aloittaa vielä 20 kappaletta tuotantotilauksessa ja yritä sitten raportoida 20 kappaletta valmiiksi kämmenlaitteessa. Tällä kertaa sijaintia **LP-001** ehdotetaan poispanosijainniksi. Tämä sijainti löytyy **Valmiiden tuotteiden poispano** -sijaintidirektiivistä. Tätä sijaintidirektiiviä käytetään, koska cross docking -mahdollisuutta ei ole. Ensimmäinen cross docking -tehtävä toteutti LP-001-siirtotilauksen kokonaisuudessaan.

**Valmiiden tuotteiden poispano** -tyyppinen työ luotiin ja käsiteltiin.

#### <a name="scenario-2---cross-docking-from-production-to-transfer-orders-with-an-appointment-schedule"></a>Skenaario 2 – Cross docking tuotannosta siirtotuotantotilaukseen sekä ajoitettu tapaaminen

Kun tuote on ilmoitettu valmiiksi tuotantolinjalla, se siirretään lastausovisijaintiin, joka saadaan lastausovisijaintien ajoitetusta tapaamisesta. Käytä yrityksen USMF:ää.

1.  Muuta cross docking -käytäntöä. Muuta skenaariossa 1 luomaasi cross docking -käytäntöä valitsemalla **Cross docking -tarve vaatii sijainnin** -valintaruudun.
2.  Uuden uusi siirtotilaus.
3.  Avaa **Kuormasuunnittelun työtila**.
4.  Siirry kuormasuunnittelun työtilassa **Kuormat**-osioon ja luo uusi ajoitettu tapaaminen valitsemalla **Kuljetus**-valikossa **Ajoita tapaaminen**. Huomaa, että ajoitettu tapaaminen viittaa **Tilausnumero**-kentän siirtotilaukseen. Voit määrittää tapaamisen päivämäärän ja ajan **Suunniteltu aloituspäivä- ja aika sijainnissa** -kentässä. Päivämäärää ja aikaa käytetään, kun cross docking -tarve priorisoidaan cross docking -prosessissa. Tässä kentässä määritetty päivämäärä ja aika päivittää vastaavan kuorman **Kuorman ajoitettu lähetyspäivä ja -aika** -kentän. **Lähetyksen erittely**-pikavälilehdellä oleva sijainti määrittää sijainnin, johon siirtotilaus lähetetään.
5.  Tee vapautus varastoon **Kuormasuunnittelun työtila** -kohdassa.
6.  Luo tuotantotilaus nimiketunnukselle **L0101**. Määritä sen tilaksi **Aloitettu** ja määräksi 20.
7.  Ilmoita valmiiksi mobiililaitteessa.
8.  Siirry mobiililaiteportaaliin ja valitse valikossa **Ilmoita valmiiksi ja pane pois**.
9.  Ilmoita nimiketunnus **L0101** valmiiksi kämmenlaitteessa. Huomaa, että poispanosijainti on nyt **LASTAUSOVI 2**. Tämä sijainti löytyy ajoitetusta tapaamisesta eikä **Siirron vastaanotto** -sijaintidirektiivistä.

### <a name="additional-information"></a>Lisätiedot

-   Cross docking -skenaariota tuetaan erä- ja sarjanumero-ohjatuissa nimikkeissä sekä erä- että sarjanumerodimensioissa, joille on määritetty varaushierarkiassa sijainti ylä- tai alapuolella.



