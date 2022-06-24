---
title: Varaston hallinnan kuormitukset pilven ja reunan asteikon yksiköitä varten
description: Tässä artikkelissa on tietoja toiminnossa, jonka avulla scale unitit voivat suorittaa valittuja prosesseja varastonhallinnan kuormituksesta.
author: perlynne
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, InventTransferOrders, SalesTable, SysSecRolesEditUsers, SysWorkloadDuplicateRecord
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: f9839ad9a18eb543734c2ba43a56b568460a64c3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893494"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Varaston hallinnan kuormitukset pilven ja reunan asteikon yksiköitä varten

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Kaikkia varastonhallinnan liiketoimintatoimintoja ei tueta täysin varastoissa, joissa on käytössä scale unitin työkuorma. Varmista, että käytät vain niitä prosesseja, joiden tuesta nimenomaisesti ilmoitetaan tässä artikkelissa.

## <a name="warehouse-execution-on-scale-units"></a>Scale unitien varastonohjaus

Varastonhallinnan kuormitukset mahdollistavat pilven ja reunan scale uniteille valittujen varastonhallinnan ominaisuuksien prosessien suorittamisen.

## <a name="prerequisites"></a>Edellytykset

Ennen varastonhallinnan työkuormaa järjestelmä on valmisteltava tässä osassa kuvatulla tavalla.

### <a name="deploy-a-scale-unit-with-the-warehouse-management-workload"></a>Ota scale unit käyttöön varastonhallinnan työkuorman avulla

Käytössä on oltava Dynamics 365 Supply Chain Managementin keskus ja scale unit, jonka käyttöönottoon sisältyy varastonhallinnan kuormitus. Lisätietoja arkkitehtuurista ja käyttöönottoprosessista: [Scale unitit jaetussa hybriditopologiassa](cloud-edge-landing-page.md).

### <a name="turn-on-required-features-in-feature-management"></a>Vaadittujen ominaisuuksien ottaminen käyttöön ominaisuuksien hallinnassa

Ota [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilassa käyttöön seuraavat ominaisuudet. (Molemmat toiminnot on lueteltu *Varastonhallinta*-moduulissa.)

- Erota hyllytys lähetysilmoituksista (ASN)
- (Esiversio) Saapuvien ja lähtevien varastotilausten skaalausyksikön tuki

## <a name="how-the-warehouse-execution-workload-works-on-scale-units"></a>Varastonohjauksen kuormituksen toiminta scale uniteissa

Varastonhallinnan kuormitusprosesseissa tiedot synkronoidaan keskuksen ja scale unitien välillä.

Scale unit voi ylläpitää vain omistamiaan tietoja. Scale unitien tietojen omistuksen käsite auttaa estämään moni-isäntäristiriidat. Tämän on tärkeää tietää, mitkä prosessitiedot ovat keskuksen ja mitkä scale unitien omistamia.

Liiketoimintaprosesseista riippuen saman tietueen omistus voi vaihdella keskuksen ja scale unitien välillä. Seuraavassa osassa on esimerkki tästä skenaariosta.

> [!IMPORTANT]
> Joitakin tietoja voidaan luoda sekä keskuksessa että scale unitissa. Esimerkkejä ovat **Rekisterikilvet** ja **Eränumerot.** Erillistä ristiriitojen käsittelyä voidaan käyttää tilanteissa, joissa sama yksilöllinen tietue luodaan sekä keskuksessa että scale unitissa saman synkronointisyklin aikana. Jos näin tapahtuu, seuraava synkronointi epäonnistuu ja sinun on siirryttävä kohtaan **Järjestelmänhallinta > Kyselyt > Kuormituskyselyt > Tietueiden kaksoiskappaleet**, jossa voit tarkastella ja yhdistellä tietoja.

## <a name="outbound-process-flow"></a>Lähtevien käsittelyn työnkulku

Ennen kuin otat varastonhallinnan kuormituksen käyttöön pilvipalvelussa tai reunan skaalausyksikössä, varmista, että yritykselläsi on *skaalausyksikön tuki lähtevien tilausten varaston vapautusta* varten. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä ottaa sen käyttöön, jos sitä vaaditaan. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Ominaisuuden nimi:** *Lähtevien tilausten varastoon vapauttamisen asteikon yksikön tuki*

Lähtevien tietojen omistusprosessi määräytyy sen mukaan, käytätkö kuormansuunnitteluprosessia. Kaikissa tapauksissa keskus omistaa *lähdeasiakirjat*, kuten myynti- ja siirtotilaukset, sekä tilausten kohdistusprosessin ja siihen liittyvät tilaustapahtumatiedot. Kun käytät kuormansuunnitteluprosessia, kuormat luodaan keskuksessa, minkä vuoksi keskus myös omistaa ne aluksi. Osana *varastoon vapauttamisen* prosessia kuormatietojen omistus siirretään erilliselle scale unitin esiintymälle, josta tulee tästä seuraavan *lähetysaallon käsittelyn* (esim. töiden kohdistuksen, täyttötöiden ja kysyntätyön luonnin) omistaja. Tämän vuoksi varastotyöntekijät voivat käsitellä lähtevien myynti- ja siirtotilausten töitä vain käyttämällä Warehouse Management -mobiilisovellusta, joka on yhteydessä siihen esiintymään, joka suorittaa kulloistakin scale unitin työkuormaa.

Kun lopullinen työprosessi laittaa varaston lopulliseen toimitussijaintiin (lastausovi), scale unit antaa merkin keskukselle päivittää lähdeasiakirjan varastotapahtumat tilaan *Kerätty*. Kunnes prosessi suoritetaan ja synkronoidaan takaisin, scale unitin työkuormassa käytettävissä oleva varasto varataan fyysisesti varastotasolla ja voit välittömästi käsitellä lähtevän lähetyksen vahvistuksen odottamatta tämän synkronoinnin valmistumista. Tästä seuraava kuorman myynnin pakkausluettelo ja laskutus tai siirtotilauslähetys käsitellään keskuksessa.

Seuraavassa kaaviossa näkyy lähtevä työnkulku ja se, missä yksittäiset liiketoimintaprosessit tapahtuvat. (Suurenna kaaviota valitsemalla se.)

[![Lähtevien käsittelyn työnkulku.](media/wes_outbound_warehouse_processes-small.png "Lähtevien käsittelyn työnkulku")](media/wes_outbound_warehouse_processes.png)

### <a name="outbound-processing-with-load-planning"></a>Lähtevä käsittely, jossa käytetään kuormansuunnittelua

Kun käytät kuormansuunnitteluprosessia, kuormat ja lähetykset luodaan keskuksessa ja tietojen omistus siirretään scale uniteille osana *varastoon vapauttamisen* prosessia, kuten seuraavassa kuvassa näkyy.

![Lähtevä käsittely, jossa käytetään kuormansuunnittelua.](./media/wes_outbound_processing_with_load_planning.png "Lähtevä käsittely, jossa käytetään kuormansuunnittelua")

### <a name="outbound-processing-without-load-planning"></a>Lähtevä käsittely ilman kuormansuunnittelua

Kun et käytä kuormansuunnitteluprosessia, lähetykset luodaan scale uniteissa. Kuormia luodaan scale uniteissa myös osana aaltoprosessia.

![Lähtevä käsittely ilman kuormansuunnittelua.](./media/wes_outbound_processing_without_load_planning.png "Lähtevä käsittely ilman kuormansuunnittelua")

## <a name="inbound-process-flow"></a>Saapuvien käsittelyn työnkulku

Keskus omistaa seuraavat tiedot:

- Kaikki lähdeasiakirjat, kuten osto- ja tuotantotilaukset
- Saapuvan kuorman käsittely
- Kaikki kustannusten ja kirjanpidolliset päivitykset

> [!NOTE]
> Saapuva ostotilaustyönkulku poikkeaa käsitteellisesti lähtevästä työnkulusta. Samaa varastoa voi käyttää joko scale unitin tai keskuksen kautta sen mukaan, onko ostotilaus vapautettu varastoon. Kun tilaus on vapautettu varastoon, tilausta voi käsitellä vain scale unitiin kirjautuneena.
>
> Jos käytät *Vapauta varastoon* -prosessia, [*varastotilaukset*](cloud-edge-warehouse-order.md) luodaan ja asiaankuuluvan vastaanottokulun omistus kohdistetaan scale unitille. Keskus ei voi rekisteröidä saapuvaa vastaanottoa.

Sinun täytyy kirjautua keskukseen käyttääksesi *Vapauta varastoon* -prosessia. Ostotilaus suoritetaan tai ajoitetaan jollakin seuraavista sivuista:

- **Hankinta > Ostotilaukset > Kaikki ostotilaukset > Varasto > Toiminnot > Vapauta varastoon**
- **Varastonhallinta > Vapauta varastoon > Ostotilausten automaattinen vapautus**

Kun käytät **Ostotilausten automaattinen vapautus** -prosessia, voit valita haluamasi ostotilausrivit kyselyn perusteella. Tyypillinen tilanne on määrittää toistuva erätyö, joka vapauttaa kaikki vahvistetut ostotilausrivit, joiden odotetaan saapuvan seuraavana päivänä.

Työntekijä voi suorittaa vastaanottoprosessin käyttämällä Scale Unitiin yhdistettyä varastonhallinnan mobiilisovellusta. Tiedot kirjataan sitten scale unitin mukaan ja raportoidaan saapuvan varastotilauksen perusteella. Scale unit käsittelee myös myöhemmin tehtävän hyllytyksen luonnin ja käsittelyn.

Jos *varastoon vapauttamisen* prosessi ei ole käytössä, jolloin myöskään *varastotilaukset* eivät ole käytössä, keskus voi käsitellä varaston vastaanoton ja työn käsittelyn erillään scale uniteista.

![Saapuvien käsittelyn työnkulku.](./media/wes-inbound-ga.png "Saapuvien käsittelyn työnkulku")

Kun työntekijä suorittaa saapuvan rekisteröinnin käyttäen Warehouse Managementin mobiilisovelluksen vastaanottoprosessia scale unitista, vastaanotto kirjataan siihen liittyvän varastotilauksen perusteella. Se vuorostaan tallennetaan scale unitiin. tämän jälkeen scale unitin työkuorma antaa keskukselle signaalin asiaan liittyvän ostotilauksen rivitapahtumien tilan päivittämiseksi muotoon *Rekisteröity*. Kun tämä on valmis, voit suorittaa sen jälkeen ostotilausten tuotevastaanoton.

Seuraavassa kaaviossa näkyy saapuva työnkulku ja se, missä yksittäiset liiketoimintaprosessit tapahtuvat. (Suurenna kaaviota valitsemalla se.)

[![Saapuvien käsittelyn työnkulku](media/wes_inbound_warehouse_processes-small.png "Saapuvien käsittelyn työnkulku")](media/wes_inbound_warehouse_processes.png)

## <a name="production-control"></a>Tuotannonhallinta

Varastonhallinnan työkuorma tukee seuraavia kolmea tuotannon työnkulkua Warehouse Management -sovelluksessa:

- Ilmoita valmiiksi ja pane pois
- Käynnistä tuotantotilaus
- Rekisteröi materiaalikulutus

### <a name="report-as-finished-and-put-away"></a>Ilmoita valmiiksi ja pane pois

Työntekijät voivat ilmoittaa tuotantotilauksen tai erätilauksen valmiiksi käyttämällä **Ilmoita valmiiksi ja pane pois** -työnkulkua Warehouse Management -sovelluksessa. He voivat myös raportoida erätilauksen osatuotteita ja sivutuotteita valmiiksi. Kun työ ilmoitetaan valmiiksi, järjestelmä luo yleensä myös hyllytyksen varastotyön skaalausyksikölle. Jos et vaadi hyllytystyötä, voit jättää sen pois määrittämällä työkäytännöt.

### <a name="start-production-order"></a>Käynnistä tuotantotilaus

Työntekijät voivat rekisteröidä tuotantotilauksen tai erätilauksen alkamisen Warehouse Management -sovelluksen **Aloita tuotantotilaus** -työnkulun avulla.

### <a name="register-material-consumption"></a>Rekisteröi materiaalikulutus

Työntekijät voivat ilmoittaa tuotantotilauksen tai erätilauksen materiaalikulutuksen Warehouse Management -sovelluksen **Rekisteröi materiaalikulutus** -työnkulun avulla. Keräysluettelon kirjauskansio luodaan tämän jälkeen tuotanto- tai erätilauksen raportoidulle materiaalille skaalausyksikössä. Kirjauskansion rivit tekevät fyysisen varauksen kulutettavasta varastosta. Kun tiedot synkronoidaan vaakayksikön ja keskuksen välillä, keräysluettelon kirjauskansio luodaan ja kirjataan keskuksen instanssiin.

## <a name="supported-processes-and-roles"></a>Tuetut prosessit ja roolit

Scale unitin varaston ohjauksen työkuorma ei tue kaikkia varastonhallintaprosesseja. Tämän vuoksi kannattaa määrittää roolit, jotka vastaavan kunkin käyttäjän käytettävissä olevia toimintoja.

Tämä prosessia helpottamaan on luotu *Kuormituksen varastopäällikkö* -niminen mallirooli, joka sisältyy esittelytietoihin. Nämä tiedot saa käyttöön valitsemalla **Järjestelmänhallinta \> Suojaus \> Suojausmääritys**. Tämän roolin tarkoitus on antaa varastopäälliköille mahdollisuus käyttää scale unitin varaston ohjauksen työkuormaa. Rooli antaa niiden sivujen käyttöoikeuden, joita tarvitaan scale unitin isännöimän kuormituksen yhteydessä.

Scale unitin käyttäjäroolit määritetään osana tietojen ensimmäistä synkronointia keskuksesta scale unitiin.

Käyttäjälle määritettyjä rooleja voi muokata valitsemalla **Järjestelmänhallinta \> Suojaus \> Määritä käyttäjät rooleihin**. Käyttäjille, jotka toimivat varastopäällikköinä vain scale uniteissa, on määritettävä ainoastaan *Kuormituksen varastopäällikkö* -rooli. Tämä menettely varmistaa, että kyseisillä käyttäjillä on vain tuettujen toimintojen käyttöoikeus. Poista kaikki muut kyseisille käyttäjille määritetyt roolit.

Käyttäjille, jotka toimivat varastopäällikköinä sekä keskuksessa että scale uniteissa, on määritettävä nykyinen *Varastopäällikkö*-rooli. Ota huomioon, että tämä rooli antaa varastotyöntekijöille mahdollisuuden käyttää toimintoja (kuten siirtotilauksen vastaanoton käsittelyä), jotka näkyvät käyttöliittymässä mutta joita ei tällä hetkellä tueta scale uniteissa.

### <a name="supported-warehouse-execution-processes"></a>Tuetut varaston ohjauksen prosessit

Seuraavat varastonohjausprosessit voidaan ottaa käyttöön scale unitin varaston ohjauksen työkuormassa:

- Myynti- ja siirtotilausten valitut aaltomenetelmät (vahvistus, kuorman luonti, kohdistus, kysynnän täydennys, konttiinpakkaus, työn luonti ja aallon etikettitulostus)

- Myynti- ja siirtotilausten varastotyön käsittely varastosovelluksella (mukaan lukien täydennystyö)
- Käytettävissä olevan varaston kysely varastosovelluksella
- Varastosiirtojen luominen ja suorittaminen varastosovelluksella
- Inventointityön luominen ja käsitteleminen varastosovelluksen avulla
- Varaston oikaisun tekeminen varastosovelluksella
- Ostotilausten rekisteröinti ja hyllytystöiden tekeminen varastosovelluksella.

Seuraavia työtyyppejä voidaan luoda scale uniteissa ja siten käsitellä osana varaston ohjauksen työkuormaa:

- **Varastosiirrot** – Manuaalinen siirto ja mallityön mukainen siirto.
- **Inventointi** – Tähän kuuluu eroavaisuuksien hyväksymis-/hylkäysprosessi osana inventointitoimintoja.
- **Ostotilaukset** – Hyllytystyö varastotilauksen kautta, kun ostotilauksia ei liitetä kuormiin.
- **Myyntitilaukset** – Yksinkertainen keräily- ja lastaustyö.
- **Siirron vastaanotto** – Rekisterikilven vastaanottokäsittelyn kautta.
- **Siirtoasia** – Yksinkertainen poiminta ja kuormaus.
- **Täydennys** – Ei sisällä tuotannon raaka-aineita.
- **Valmiiden tuotteiden hyllytys** – Tapahtuu valmiiksi ilmoittamisen tuotantoprosessin jälkeen.
- **Oheis- ja sivutuotteiden hyllytys** – Tapahtuu valmiiksi ilmoittamisen tuotantoprosessin jälkeen.
<!-- - **Packed container picking** - After manual packing station processing. -->

Scale uniteissa ei tueta tällä hetkellä minkään muun tyyppistä lähdeasiakirjojen käsittelyä tai varastotyötä. Kun esimerkiksi suoritetaan varaston suorituksen työkuormaa skaalausyksikössä, palautustilausten käsittelemiseen ei voi käyttää myynnin palautustilauksen vastaanottoprosessia. Sen sijaan käsittely pitää tehdä keskuksen esiintymässä.

> [!NOTE]
> Niiden toimintojen, joita ei tueta, mobiililaitteen valikkovaihtoehtoja ja painikkeita ei näytetä _varastonhallinnan mobiilisovelluksessa_, kun se on yhdistetty Scale Unitin käyttöönottoon.
>
> Warehouse Management -mobiilisovelluksen määrittäminen pilvipalvelun tai reunan skaalausyksikölle edellyttää joitakin lisävaiheita. Lisätietoja on kohdassa [Määritä Warehouse Management -mobiilisovellus pilvi- ja reunapalvelujen Scale Uniteille](cloud-edge-workload-setup-warehouse-app.md).
>
> Jos työkuorma suoritetaan scale unitissa, prosesseja, joita ei tueta, ei voi suorittaa kyseisen varaston osalta keskuksessa. Tässä artikkelissa on jäljempänä taulukoita, joissa on luettelo tuetuista ominaisuuksista.
>
> Valitut varastotyötyypit voidaan luoda sekä keskuksessa että scale uniteissa, mutta vain omistava keskus tai scale unit voi ylläpitää niitä (tiedot luonut käyttöönotto).
>
> On muistettava, että vaikka scale unit tukisi tiettyä prosessia, kaikkia tarvittavia tietoja ei ehkä synkronoida keskuksesta scale unitiin tai scale unitista keskukseen, mikä voi aiheuttaa odottamattoman järjestelmäkäsittelyn. Esimerkkejä tästä skenaariosta:
>
> - Jos käytössä on sijaintidirektiivin kysely, joka liittää vain keskuskäyttöönotossa olevan tietotaulukkotietueen.
> - Jos käytössä on sijainnin tila ja/tai sijainnin tilavuustietojen kuormaustoiminnot. Näitä tietoja ei synkronoida käyttöönottojen välillä, minkä vuoksi ne toimivat vain päivitettäessä jonkin käyttöönoton sijainnin käytettävissä olevaa varastoa.

Seuraavia varastonhallintatoimintoja ei tueta tällä hetkellä scale unitin työkuormissa:

- Kuormaan määritetyn ostotilausrivien saapuvien käsittely.
- Projektin ostotilausten saapuvien käsittely.
- Aiheutuneen kustannuksen hallinta, matkojen käyttäminen ja kuljetuksessa olevien tuotteiden seuraaminen.
- Sellaisten nimikkeiden saapuvien ja lähtevien käsittely, joissa on aktiiviset **Omistaja**- ja/tai **Eränumero**-seurantadimensiot.
- Sellaisen varaston käsittely, jonka tilan-arvona on esto.
- Varaston tilan muuttaminen minkä tahansa siirtoprosessin aikana.
- Tilaussidonnainen joustava varastotason dimensioiden varaukset.
- *Varastosijainnin tila* -toiminnon käyttö (tietoja ei synkronoida käyttöönottojen välillä).
- *Toimipaikan rekisterikilpien paikannus* -toiminnon käyttö.
- *Tuotesuodattimet*- ja *Tuotesuodatinryhmät*-asetusten, mukaan lukien **Päiviä erien yhdistämiseen** -asetuksen, käyttö.
- Laadunvalvonnan sisältävä integrointi.
- Todellisen painon nimikkeiden käsittely.
- Nimikkeiden käsittely, jossa vain kuljetustenhallinta on otettu käyttöön.
- Negatiivisen käytettävissä olevan varaston käsittely.
- Yritysten välisten tietojen jakaminen tuotteita varten. <!-- Planned -->
- Kuormakirjoja sisältävän varastotyön käsittely (esimerkiksi pakkausluettelot pakkausasemalla).
- Tuotteen päätietojen kuvat (esimerkiksi Warehouse Management -mobiilisovelluksessa).
- Materiaalikäsittelyä tai varastoautomaatiota sisältävän varastotyön käsittely.

> [!WARNING]
> Jotkin varastotoiminnot eivät ole käytettävissä varastoissa, joissa varastonhallinnan työkuormia suoritetaan scale unitissa eikä sitä myöskään tueta keskuksessa tai scale unitin työkuormassa.
>
> Muut ominaisuudet voidaan käsitellä molemmissa, mutta niiden käytössä on oltava varovainen joissa skenaarioissa, kuten silloin kun saman varaston käytettävissä oleva varasto päivitetään sekä keskuksessa että scale unitissa asynkronisen tietojen päivitysprosessin vuoksi.
>
> Tiettyjä toimintoja (kuten *työn esto*), joita tuetaan sekä keskuksessa että scale uniteissa, voidaan tukea vain tietojen omistajan osalta.

### <a name="outbound-supported-only-for-sales-and-transfer-orders"></a>Lähtevät (tuetaan vain myyntitilauksissa ja siirtotilauksissa)

Seuraava taulukko sisältää tuetut lähtevät toiminnot ja missä näitä toimintoja tuetaan, kun varastonhallinnan kuormituksia käytetään pilvi- ja reunapalvelujen scale uniteissa.

| Käsittele                                                      | Keskus | Varaston ohjauksen työkuorma scale unitissa |
|--------------------------------------------------------------|-----|------------------------------|
| Lähdeasiakirjan käsittely                                   | Kyllä | Ei |
| Lastauksen ja kuljetusten hallinnan käsittely                | Kyllä, mutta vain kuormansuunnitteluprosessit. Kuljetuksen hallinnan käsittely ei tueta  | Ei |
| Vapauta varastoon                                         | Kyllä | Ei |
| Suunniteltu cross-docking                                        | Ei  | Ei |
| Lähetyksen konsolidointi                                       | Kyllä, käytettäessä kuormansuunnittelua | Kyllä |
| Lähetysaallon käsittely                                     | Ei  |Kyllä, paitsi **Kuorman kokoaminen ja lajittelu** |
| Aallon lähetysten ylläpito                                  | Ei  | Kyllä|
| Varastotyön käsittely (mukaan lukien rekisterikilven tulostus)        | Ei  | Kyllä, mutta vain edellä mainittujen tuettujen ominaisuuksien osalta |
| Klusterin keräily                                              | Ei  | Kyllä|
| Manuaalinen pakkausaseman käsittely  | Ei  | Ei |
| Lähtevien lajittelun käsittely                                  | Ei  | Ei |
| Lastaukseen liittyvien asiakirjojen tulostaminen                           | Kyllä | Kyllä|
| Rahtikirjan ja ASN-ilmoituksen luonti                            | Ei  | Kyllä|
| Lähetyksen vahvistus                                             | Ei  | Kyllä|
| Lähetyksen vahvistus sekä Vahvista ja siirrä            | Ei  | Kyllä|
| Pakkausluettelon ja laskutuksen käsittely                        | Kyllä | Ei |
| Lyhyt keräily (myynti- ja siirtotilaukset)                    | Ei  | Kyllä, poistamatta lähdeasiakirjojen varauksia|
| Ylikeräily (myynti- ja siirtotilaukset)                     | Ei  | Kyllä|
| Konsolidoi rekisterikilvet                                   | Ei  | Kyllä|
| Työsijaintien muuttaminen (myynti- ja siirtotilaukset)         | Ei  | Kyllä|
| Työn viimeistely (myynti- ja siirtotilaukset)                    | Ei  | Kyllä|
| Työraportin tulostus                                            | Kyllä | Kyllä|
| Aallon otsikko                                                   | Ei  | Kyllä|
| Työn jako                                                   | Ei  | Kyllä|
| Työn käsittely – Kuljetuksen kuormaus -ohjattu            | Ei  | Ei |
| Vähennä kerättyä määrää                                       | Ei  | Kyllä|
| Palauta työ                                                 | Ei  | Kyllä|
| Käännä lähetyksen vahvistus                                | Ei  | Kyllä|
| Varastotilausrivien peruuttamispyyntö                      | Kyllä | Ei, mutta pyyntö hyväksytään tai hylätään. |
| <p>Julkaise siirtotilaukset vastaanottoa varten</p><p>Tämä prosessi tapahtuu automaattisesti osana siirtotilauksen lähetysprosessia. Sen avulla voi kuitenkin ottaa käyttöön vaakayksikössä vastaanottava rekisterikilpi, jos saapuvat varastotilausrivit on peruutettu tai osana uutta työkuorman käyttöönottoprosessia.</p> | Kyllä | Ei|
<!--| Manuaalinen pakkausaseman käsittely, mukaan lukien Pakatun kontin keräily -työ  | Ei  | Kyllä, mutta ilman TMS-lähetystä, jossa on luettelotiedostoja ja myyntipakkausluettelojen kirjaus ja ilman pakkausmerkintöjä ja tuotekuvia |-->

### <a name="inbound"></a>Saapuva

Seuraava taulukko sisältää tuetut saapuvien toiminnot ja missä näitä toimintoja tuetaan, kun varastonhallinnan kuormituksia käytetään pilvi- ja reunapalvelujen scale uniteissa.

| Käsittele                                                          | Keskus | Varaston ohjauksen työkuorma scale unitissa<BR>*(Nimikkeet, joissa on Kyllä-merkintä, koskevat vain varastotilauksia)* |
|------------------------------------------------------------------|-----|----------------------------------------------------------------------------------|
| Lähdeasiakirjan&nbsp;käsittely                             | Kyllä | Ei |
| Lastauksen ja kuljetusten hallinnan käsittely                    | Kyllä | Ei |
| Aiheutunut kustannus ja kuljetettavien tuotteiden vastaanottaminen                       | Kyllä | Ei |
| Saapuvan lähetyksen vahvistus                                    | Kyllä | Ei |
| Ostotilauksen vapautus varastoon (varastotilausten käsittely) | Kyllä | Ei |
| Varastotilausrivien peruuttamispyyntö                            | Kyllä | Ei, mutta pyyntö hyväksytään tai hylätään. |
| Ostotilauksen lähdeasiakirjan tuotteen vastaanoton käsittely                        | Kyllä | Ei |
| Ostotilausnimikkeen vastaanotto ja poispano                       | <p>Kyllä,&nbsp;kun &nbsp;varastotilausta ei&nbsp;ole</p><p>Ei, kun varastotilaus on</p> | <p>Kyllä, jos ostotilaus ei ole <i>kuorman</i> osa</p> |
| Ostotilausrivin vastaanotto ja poispano                       | <p>Kyllä, kun varastotilausta ei ole</p><p>Ei, kun varastotilaus on</p> | <p>Kyllä, jos ostotilaus ei ole <i>kuorman</i> osa</p></p> |
| Palautustilauksen vastaanotto ja poispano                              | Kyllä | Ei |
| Yhdistetyn rekisterikilven vastaanotto ja poispano                       | <p>Kyllä, kun varastotilausta ei ole</p><p>Ei, kun varastotilaus on</p> | Kyllä |
| Kuorman nimikkeen vastaanotto                                              | <p>Kyllä, kun varastotilausta ei ole</p><p>Ei, kun varastotilaus on</p> | Ei |
| Ostotilauksen rekisterikilven vastaanotto ja poispano              | <p>Kyllä, kun varastotilausta ei ole</p><p>Ei, kun varastotilaus on</p> | Ei |
| Siirtotilauksen rekisterikilven vastaanotto ja poispano             | Ei | Kyllä |
| Siirtotilausnimikkeen vastaanotto ja poispano                       | Kyllä | Ei |
| Siirtotilausrivin vastaanotto ja poispano                       | Kyllä | Ei |
| Alitoimituksen sisältävän ostotilauksen vastaanotto                      | <p>Kyllä, kun varastotilausta ei ole</p><p>Ei, kun varastotilaus on</p> | Kyllä, mutta vain tekemällä peruutuspyyntö keskuksesta |
| Ylitoimituksen sisältävän ostotilauksen vastaanotto                       | <p>Kyllä, kun varastotilausta ei ole</p><p>Ei, kun varastotilaus on</p> | Kyllä  |
| *Cross docking* -työn luonnin sisältävä vastaanotto                 | <p>Kyllä, kun varastotilausta ei ole</p><p>Ei, kun varastotilaus on</p> | Ei |
| *Laatutilaus*-työn luonnin sisältävä vastaanotto                  | <p>Kyllä, kun varastotilausta ei ole</p><p>Ei, kun varastotilaus on</p> | Ei |
| *Laatunimikkeen otanta* -työn luonnin sisältävä vastaanotto          | <p>Kyllä, kun varastotilausta ei ole</p><p>Ei, kun varastotilaus on</p> | Ei |
| *Laatu laaduntarkistuksessa* -työn luonnin sisältävä vastaanotto       | <p>Kyllä, kun varastotilausta ei ole</p><p>Ei, kun varastotilaus on</p> | Ei |
| Laatutilauksen luonnin sisältävä vastaanotto                            | <p>Kyllä, kun varastotilausta ei ole</p><p>Ei, kun varastotilaus on</p> | Ei |
| Työnkäsittely – *Klusterihyllytys*-ohjattu                 | Kyllä | Ei |
| *Lyhyt keräilyn* sisältävän työn käsittely                               | Kyllä | Ei |
| Työn peruuttaminen (saapuva)                                            | <p>Kyllä, kun varastotilausta ei ole</p><p>Ei, kun varastotilaus on</p> | <p>Kyllä, mutta vain silloin kun <b>Poista vastaanoton rekisteröinti, kun työ peruutetaan</b> -asetuksen valinta on tyhjennetty <b>Varastonhallinnan parametrit</b> -sivulla</p> |
| Rekisterikilven lataus                                           | Kyllä | Kyllä |

### <a name="warehouse-operations-and-exception-handing"></a>Varastotoiminnot ja poikkeuksien käsittely

Seuraava taulukko sisältää tuetut varastotoimintojen ja poikkeuksien käsittelyn toiminnot ja missä näitä toimintoja tuetaan, kun varastonhallinnan kuormituksia käytetään pilvi- ja reunapalvelujen scale uniteissa.

| Käsittele                                            | Keskus | Varaston ohjauksen työkuorma scale unitissa |
|----------------------------------------------------|-----|------------------------------|
| Rekisterikilpikysely                              | Kyllä | Kyllä                          |
| Nimikekysely                                       | Kyllä | Kyllä                          |
| Sijaintikysely                                   | Kyllä | Kyllä                          |
| Vaihda varastoa                                   | Kyllä | Kyllä                          |
| Siirto                                           | Kyllä | Kyllä                          |
| Siirto mallin mukaan                               | Kyllä | Kyllä                          |
| Varastosiirto                                 | Kyllä | Ei                           |
| Siirtotilauksen luominen varastosovelluksesta           | Kyllä | Ei                           |
| Oikaisu (sisään/ulos)                                | Kyllä | Kyllä, mutta ei oikaisu ulos -skenaariota varten, jossa varastovaraus on poistettava käyttämällä varasto-oikaisutyyppien **Poista varaukset** -asetusta.</p>                           |
| Varaston tilamuutos                            | Kyllä | Ei                           |
| Inventointi ja poikkeamien käsittely | Kyllä | Kyllä                           |
| Etiketin uudelleentulostus (rekisterikilven tulostus)             | Kyllä | Kyllä                          |
| Rekisterikilpikoonti                                | Kyllä | Ei                           |
| Rekisterikilven tauko                                | Kyllä | Ei                           |
| Pakkaa sisäkkäisiin rekisterikilpiin                      | Kyllä | Ei                           |
| Kuljettajan sisäänkuittaus                                    | Kyllä | Ei                           |
| Kuljettajan uloskuittaus                                   | Kyllä | Ei                           |
| Eräkäsittelykoodin muuttaminen                      | Kyllä | Kyllä                          |
| Näytä avoin työluettelo                             | Kyllä | Kyllä                          |
| Vähimmäis- ja enimmäistäydennyksen sekä vyöhykkeen rajatäydennyksen käsittely| Kyllä <p>Suosituksena on, että samaa sijaintia ei sisällytetä kyselyjen osana</p>| Kyllä                          |
| Paikoitustäydennyksen käsittely                  | Kyllä  | Kyllä<p>Huomaa, että määritys on tehtävä scale unitissa</p>                           |
| Työn esto ja eston poisto                             | Kyllä | Kyllä                          |
| Vaihda käyttäjä                                        | Kyllä | Kyllä                          |
| Työpoolin vaihtaminen työssä                           | Kyllä | Kyllä                          |
| Peruuta työ                                        | Kyllä | Kyllä                          |

### <a name="production"></a>Tuotantoympäristö

Seuraavassa taulukossa esitellään, mitä varastonhallinnan tuotantoskenaarioita tuetaan tällä hetkellä scale unitin työkuormissa.

| Käsittele | Keskus | Varaston ohjauksen työkuorma scale unitissa |
|---------|-----|----------------------------------------------|
| Tuotantotilauksen lähdetiedostojen käsittely    | Kyllä | Ei |
| Vapauta varastoon                           | Kyllä | Ei |
| Käynnistä tuotantotilaus                         | Kyllä | Kyllä|
| Varastotilausten luominen                        | Kyllä | Ei |
| Varastotilausrivien peruuttamispyyntö        | Kyllä | Ei, mutta pyyntö hyväksytään tai hylätään. |
| Ilmoita valmiiksi ja valmiiden tuotteiden hyllytys | <p>Kyllä, kun varastotilausta ei ole</p><p>Ei, kun varastotilaus on</p> | Kyllä|
| Rinnakkaistuotteen ja sivutuotteen poispano             | <p>Kyllä, kun varastotilausta ei ole</p><p>Ei, kun varastotilaus on</p> | Kyllä|
| Rekisteröi materiaalikulutus                  | Kyllä | Kyllä|
| Tuotannon aallon käsittely                     | Kyllä | Ei |
| Raaka-aineiden keräily                           | Kyllä | Ei |
| Kanban-poispano                                | Kyllä | Ei |
| Kanban-keräily                                 | Kyllä | Ei |
| Tyhjennä kanban                                   | Kyllä | Ei |
| Tuotannon hävikki                               | Kyllä | Ei |
| Tuotannon viimeinen kuormalava                         | Kyllä | Ei |
| Raaka-aineiden täydennys                     | Ei  | Ei |

## <a name="maintaining-scale-units-for-warehouse-execution"></a>Scale unitien ylläpito varaston ohjausta varten

Useita erätöitä suoritetaan sekä keskuksessa että scale uniteissa

Seuraavia erätöitä voidaan ylläpitää manuaalisesti keskuskäyttöönotossa:

- Seuraavia erätyötä voi hallita valitsemalla **Varastonhallinta \> Kausittaiset tehtävät \> Taustatoimintojen kuormituksen hallinta**:

    - Scale Unitin ja keskuksen välinen sanoman käsittelijä
    - Rekisteröi lähdetilauksen vastaanotot
    - Viimeistele varastotilaukset
    - Luo puuttuvat lähtevät varastotilaukset

- Seuraavia erätyötä voi hallita valitsemalla **Varastonhallinta \> Kausittaiset tehtävät \> Työkuormien hallinta**:

    - Varastokeskuksen yksikkösanoman käsittelijä
    - Käsittele varastotilausrivien vastaanotot varaston vastaanoton kirjausta varten

Scale unitien käyttöönotossa voi hallita seuraavia erätöitä valitsemalla **Varastonhallinta \> Kausittaiset tehtävät \> Kuormituksen hallinta**:

- Käsittele aaltotaulukon tietueet
- Varastokeskuksen yksikkösanoman käsittelijä
- Käsittele varastotilausrivien vastaanotot varaston vastaanoton kirjausta varten

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
