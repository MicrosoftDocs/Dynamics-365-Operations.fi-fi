---
title: Varastonhallinnan kuormitusten pilvi- ja reunapalvelujen scale unitit
description: Tässä aiheessa on tietoja toiminnossa, jonka avulla scale unitit voivat suorittaa valittuja prosesseja varastonhallinnan kuormituksesta.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, SysSecRolesEditUsers, SysWorkloadDuplicateRecord
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 7541688e8428dbc17a3c53d696913365580c3db8
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343761"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Varaston hallinnan kuormitukset pilven ja reunan asteikon yksiköitä varten

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Kaikkia varastonhallinnan liiketoimintatoimintoja ei tueta täysin varastoissa, joissa on käytössä scale unitin työkuorma. Varmista, että käytät vain niitä prosesseja, joiden tuesta nimenomaisesti ilmoitetaan tässä aiheessa.

## <a name="warehouse-execution-on-scale-units"></a>Scale unitien varastonohjaus

Tämän toiminnon avulla scale unitit voivat suorittaa valittuja prosesseja varastonhallinnan ominaisuuksista.

Tässä aiheessa varastonhallinnan ohjausta varastossa, joka on määritetty scale unitiksi, kutsutaan *varastonohjausjärjestelmäksi* (*WES*).

## <a name="prerequisites"></a>Edellytykset

Käytössä on oltava Dynamics 365 Supply Chain Managementin keskus ja scale unit, jonka käyttöönottoon sisältyy varastonhallinnan kuormitus. Lisätietoja on arkkitehtuurista ja käyttöönottoprosessista on kohdassa [Käytä scale uniteja Supply chain managementin työkuormien joustavuutta](cloud-edge-landing-page.md).

## <a name="how-the-wes-workload-works-on-scale-units"></a>WES-kuormituksen käyttäminen scale uniteissa

Varastonhallinnan kuormitusprosesseissa tiedot synkronoidaan keskuksen ja scale unitien välillä.

Scale unit voi ylläpitää vain omistamiaan tietoja. Scale unitien tietojen omistuksen käsite auttaa estämään moni-isäntäristiriidat. Tämän on tärkeää tietää, mitkä prosessit ovat keskuksen ja mitkä scale unitien omistamia.

Scale unitit omistavat seuraavat tiedot:

- **Lähetysaallon käsittelyn tiedot** – valitut aallon käsittelymenetelmät käsitellään scale unitin aallon käsittelyn osana.
- **Työn käsittelyn tiedot** – Tämä tietty scale unit omistaa scale unitille luodun varastotyön. Seuraavia työtilausten käsittelytyyppejä tuetaan:

  - **Varastosiirrot** (manuaalinen siirto ja mallityön mukainen siirto)
  - **Inventointi**- ja hyväksymis-/hylkäysprosessi osana inventointitoimintoja
  - **Ostotilaukset** (hyllytystyö varastotilauksen kautta, kun ostotilauksia ei liitetä kuormiin)
  - **Myyntitilaukset** (yksinkertainen keräily- ja lastaustyö)
  - **Siirtotilaukset** (vain lähtevät, jossa yksinkertainen keräily- ja lastaustyö)

- **Varastotilauksen vastaanoton tiedot** – näitä tietoja käytetään vain ostotilauksissa, jotka on vapautettu varastoon.
- **Rekisterikilven tiedot** – Rekisterikilpiä voidaan luoda sekä keskuksessa että scale uniteissa. Erillinen ristiriitojen käsittely on mahdollista. 

    > [!IMPORTANT]
    > Rekisterikilpien tiedot eivät ole varastokohtaisia. Jos saman rekisterinumeron saa luoda sekä keskuksessa että scale unitissa saman synkronointisyklin aikana, seuraava synkronointi epäonnistuu. Jos näin tapahtuu, valitse **Järjestelmänhallinta > Kyselyt > Kuormituskyselyt > Tietueiden kaksoiskappaleet**, jossa voit tarkastella ja yhdistää tietoja.

## <a name="outbound-process-flow"></a>Lähtevien käsittelyn työnkulku

Keskus omistaa seuraavat tiedot:

- Kaikki lähdeasiakirjat, kuten myyntitilaukset ja siirtotilaukset
- Tilausten kohdistus ja lähtevän kuorman käsittely
- Vapautus varastoon, lähetyksen luonti-, aallon luonti- ja aallon viimeistelyprosessit

Scale unitit omistavat varsinaisen aalloin käsittelyn (kuten työn kohdistamisen, täydennystyön ja kysynnän työn luonnin) aallon vapautuksen jälkeen. Niinpä varastotyöntekijät voivat käsitellä lähtevän työn käyttämällä Scale Unitiin yhdistettyä varastonhallinnan mobiilisovellusta.

![Aallon käsittelyn työnkulku.](./media/wes-wave-processing-ga.png "Aallon käsittelyn työnkulku")

### <a name="process-work-and-ship"></a>Työn käsittely ja lähetys

Kun lopullinen työprosessi laittaa varaston lopulliseen toimitussijaintiin (lastausovi), scale unit antaa merkin keskukselle päivittää lähdeasiakirjan varastotapahtumat tilaan *Kerätty*. Siihen asti kunnes prosessi suoritetaan ja synkronoidaan takaisin, scale unitin kuormituksen käytettävissä oleva varasto varataan fyysisesti varastotasolla.

Kun keskus on päivittänyt tapahtumat *Kerätty*-tilaan, se voi käsitellä lähtevän lähetyksen vahvistuksen ja siihen liittyvän myynnin pakkausluettelon tai siirtotilauksen lähetyksen kuormaa varten.

![Lähtevien käsittelyn työnkulku.](./media/WES-outbound-processing-19.png "Lähtevien käsittelyn työnkulku")

## <a name="inbound-process-flow"></a>Saapuvien käsittelyn työnkulku

Keskus omistaa seuraavat tiedot:

- Kaikki lähdeasiakirjat, kuten ostotilaukset ja myynnin palautustilaukset
- Saapuvan kuorman käsittely
- Kaikki kustannusten ja kirjanpidolliset päivitykset

> [!NOTE]
> Saapuva ostotilaustyönkulku poikkeaa käsitteellisesti lähtevästä työnkulusta. Samaa varastoa voi käyttää joko scale unitin tai keskuksen kautta sen mukaan, onko ostotilaus vapautettu varastoon vai ei. Kun tilaus on vapautettu varastoon, tilausta voi käsitellä vain scale unitiin kirjautuneena.
>
> Jos käytät *Vapauta varastoon* -prosessia, [*varastotilaukset*](cloud-edge-warehouse-order.md) luodaan ja asiaankuuluvan vastaanottokulun omistus kohdistetaan scale unitille. Keskus ei voi rekisteröidä saapuvaa vastaanottoa.

Sinun täytyy kirjautua keskukseen käyttääksesi *Vapauta varastoon* -prosessia. Voit suorittaa tai ajoittaa sen seuraavilta sivuilta:

- **Hankinta > Ostotilaukset > Kaikki ostotilaukset > Varasto > Toiminnot > Vapauta varastoon**
- **Varastonhallinta > Vapauta varastoon > Ostotilausten automaattinen vapautus**

Kun käytät **Ostotilausten automaattinen vapautus** -prosessia, voit valita haluamasi ostotilausrivit kyselyn perusteella. Tyypillinen tilanne on määrittää toistuva erätyö, joka vapauttaa kaikki vahvistetut ostotilausrivit, joiden odotetaan saapuvan seuraavana päivänä.

Työntekijä voi suorittaa vastaanottoprosessin käyttämällä Scale Unitiin yhdistettyä varastonhallinnan mobiilisovellusta. Tiedot kirjataan sitten scale unitin mukaan ja raportoidaan saapuvan varastotilauksen perusteella. Scale unit käsittelee myös myöhemmin tehtävän hyllytyksen luonnin ja käsittelyn.

Jos *varastoon vapauttamisen* prosessi ei ole käytössä, jolloin myöskään *varastotilaukset* eivät ole käytössä, keskus voi käsitellä varaston vastaanoton ja työn käsittelyn erillään scale uniteista.

![Saapuvien käsittelyn työnkulku.](./media/wes-inbound-ga.png "Saapuvien käsittelyn työnkulku")

Kun suoritat saapuvan rekisteröinnin varastosovelluksen vastaanottoprosessin avulla scale unitin varastotilauksen perusteella, scale unitin kuormitus antaa merkin keskukselle päivittää asiaan liittyvät ostotilausrivin tapahtumat tilaan *Rekisteröity*. Kun tämä on valmis, voit suorittaa sen jälkeen ostotilausten tuotevastaanoton.

![Saapuvien käsittelyn työnkulku.](./media/WES-inbound-processing-19.png "Saapuvien käsittelyn työnkulku")

## <a name="supported-processes-and-roles"></a>Tuetut prosessit ja roolit

Scale unitin WES-kuormitus ei tue kaikkia varastonhallintaprosesseja. Tämän vuoksi kannattaa määrittää roolit, jotka vastaavan kunkin käyttäjän käytettävissä olevia toimintoja.

Tämä prosessia helpottamaan on luotu *Kuormituksen varastopäällikkö* -niminen mallirooli, joka sisältyy esittelytietoihin. Nämä tiedot saa käyttöön valitsemalla **Järjestelmänhallinta \> Suojaus \> Suojausmääritys**. Tämän roolin tarkoitus on antaa varastopäälliköille mahdollisuus käyttää scale unitin WES-järjestelmää. Rooli antaa niiden sivujen käyttöoikeuden, joita tarvitaan scale unitin isännöimän kuormituksen yhteydessä.

Scale unitin käyttäjäroolit määritetään osana tietojen ensimmäistä synkronointia keskuksesta scale unitiin.

Käyttäjälle määritettyjä rooleja voi muokata valitsemalla **Järjestelmänhallinta \> Suojaus \> Määritä käyttäjät rooleihin**. Käyttäjille, jotka toimivat varastopäällikköinä vain scale uniteissa, on määritettävä ainoastaan *Kuormituksen varastopäällikkö* -rooli. Tämä menettely varmistaa, että kyseisillä käyttäjillä on vain tuettujen toimintojen käyttöoikeus. Poista kaikki muut kyseisille käyttäjille määritetyt roolit.

Käyttäjille, jotka toimivat varastopäällikköinä sekä keskuksessa että scale uniteissa, on määritettävä nykyinen *Varastopäällikkö*-rooli. Ota huomioon, että tämä rooli antaa varastotyöntekijöille mahdollisuuden käyttää toimintoja (kuten siirtotilauksen vastaanoton käsittelyä), jotka näkyvät käyttöliittymässä mutta joita ei tällä hetkellä tueta scale uniteissa.

## <a name="supported-wes-processes"></a>Tuetut WES-prosessit

Seuraavat varastonohjausprosessit voidaan ottaa käyttöön scale unitin WES-kuormituksessa:

- Myynti- ja siirtotilausten valitut aaltomenetelmät (kohdistus, kysynnän täydennys, konttiinpakkaus, työn luonti ja aallon etikettitulostus)

- Myynti- ja siirtotilausten varastotyön käsittely varastosovelluksella (mukaan lukien täydennystyö)
- Käytettävissä olevan varaston kysely varastosovelluksella
- Varastosiirtojen luominen ja suorittaminen varastosovelluksella
- Inventointityön luominen ja käsitteleminen varastosovelluksen avulla
- Varaston oikaisun tekeminen varastosovelluksella
- Ostotilausten rekisteröinti ja hyllytystöiden tekeminen varastosovelluksella.

Seuraavia työtilaustyyppejä tuetaan tällä hetkellä scale unit -käyttöönottojen WES-kuormituksissa:

- Myyntitilaukset
- Siirtovarasto-otto
- Täydennys (ei sisällä tuotannon raaka-aineita)
- Varaston siirtotapahtuma
- Inventointi
- Varastotilaukset (linkitetyt ostotilaukset)

Scale uniteissa ei tueta tällä hetkellä minkään muun tyyppistä lähdeasiakirjojen käsittelyä tai varastotyötä. Esimerkiksi scale unitin WES-työkuormassa ei voi suorittaa siirtotilauksen vastaanottoprosessia (siirron vastaanottoa) vaan sen sijaan keskusesiintymän pitää käsitellä se.

> [!NOTE]
> Niiden toimintojen, joita ei tueta, mobiililaitteen valikkovaihtoehtoja ja painikkeita ei näytetä _varastonhallinnan mobiilisovelluksessa_, kun se on yhdistetty Scale Unitin käyttöönottoon.

> [!WARNING]
> Jos työkuorma suoritetaan scale unitissa, prosesseja, joita ei tueta, ei voi suorittaa kyseisen varaston osalta keskuksessa. Tässä aiheessa on jäljempänä taulukoita, joissa on luettelo tuetuista ominaisuuksista.
>
> Valitut varastotyötyypit voidaan luoda sekä keskuksessa että scale uniteissa, mutta vain omistava keskus tai scale unit voi ylläpitää niitä (tiedot luonut käyttöönotto).
>
> On muistettava, että vaikka scale unit tukisi tiettyä prosessia, kaikkia tarvittavia tietoja ei ehkä synkronoida keskuksesta scale unitiin tai scale unitista keskukseen, mikä voi aiheuttaa odottamattoman järjestelmäkäsittelyn. Esimerkkejä:
> 
> - Jos käytössä on sijaintidirektiivin kysely, joka liittää vain keskuskäyttöönotossa olevan tietotaulukkotietueen.
> - Jos käytössä on sijainnin tila ja/tai sijainnin tilavuustietojen kuormaustoiminnot. Näitä tietoja ei synkronoida käyttöönottojen välillä, minkä vuoksi ne toimivat vain päivitettäessä jonkin käyttöönoton sijainnin käytettävissä olevaa varastoa.

Seuraavia varastonhallintatoimintoja ei tueta tällä hetkellä scale unitin työkuormissa:

- Kuormaan määritetyn ostotilausrivien saapuvien käsittely
- Projektin ostotilausten saapuvien käsittely
- Sellaisten nimikkeiden saapuvien ja lähtevien käsittely, joissa on aktiiviset **Omistaja**- ja/tai **Eränumero**-seurantadimensiot
- Sellaisen varaston käsittely, jonka tilan-arvona on esto
- Varaston tilan muuttaminen minkä tahansa siirtoprosessin aikana
- Tilaussidonnainen joustava varastotason dimensioiden varaukset
- *Varastosijainnin tila* -toiminnon käyttö (tietoja ei synkronoida käyttöönottojen välillä)
- *Toimipaikan rekisterikilpien paikannus* -toiminnon käyttö
- *Tuotesuodattimet*- ja *Tuotesuodatinryhmät*-asetusten, mukaan lukien **Päiviä erien yhdistämiseen** -asetuksen, käyttö
- Laadunvalvonnan sisältävä integrointi
- Todellisen painon nimikkeiden käsittely
- Nimikkeiden käsittely, jossa vain kuljetustenhallinta on otettu käyttöön
- Negatiivisen käytettävissä olevan varaston käsittely
- Mukautettuja työtyyppejä sisältävän varastotyön käsittely
- Kuormakirjoja sisältävän varastotyön käsittely
- Materiaalikäsittelyä tai varastoautomaatiota sisältävän varastotyön käsittely
- Tuotteen päätietojen kuvan käyttö (esimerkiksi varastonhallinnan mobiilisovelluksessa)

> [!WARNING]
> Jotkin varastotoiminnot eivät ole käytettävissä varastoissa, joissa varastonhallinnan työkuormia suoritetaan scale unitissa eikä sitä myöskään tueta keskuksessa tai scale unitin työkuormassa.
> 
> Muut ominaisuudet voidaan käsitellä molemmissa, mutta niiden käytössä on oltava varovainen joissa skenaarioissa, kuten silloin kun saman varaston käytettävissä oleva varasto päivitetään sekä keskuksessa että scale unitissa asynkronisen tietojen päivitysprosessin vuoksi.
> 
> Tiettyjä toimintoja (kuten *työn esto*), joita tuetaan sekä keskuksessa että scale uniteissa, voidaan tukea vain tietojen omistajan osalta.

### <a name="outbound-supported-only-for-sales-and-transfer-orders"></a>Lähtevät (tuetaan vain myyntitilauksissa ja siirtotilauksissa)

Seuraava taulukko sisältää tuetut lähtevät toiminnot ja missä näitä toimintoja tuetaan, kun varastonhallinnan kuormituksia käytetään pilvi- ja reunapalvelujen scale uniteissa.

| Prosessoi                                                      | Keskus | WES-kuormitus scale unitissa |
|--------------------------------------------------------------|-----|------------------------------|
| Lähdeasiakirjan käsittely                                   | Kyllä | Nro |
| Lastauksen ja kuljetusten hallinnan käsittely                | Kyllä | Nro |
| Vapauta varastoon                                         | Kyllä | Nro |
| Suunniteltu cross-docking                                        | Nro  | Nro |
| Lähetyksen konsolidointi                                       | Kyllä | Nro |
| Lähetysaallon käsittely                                     | Kyllä, mutta vain aallon alustus ja viimeistely käsitellään keskuksessa. Niinpä vain scale unit voi käsitellä lähtevän siirto- ja myyntitilauksen käsittelyn.|<p>Ei, keskus käsittelee alustuksen ja viimeistelyn eikä **kuorman luontia ja lajittelua** tueta<p><b>Huomautus:</b> aallon tilan viimeistelyyn aallon käsittelyn osana tarvitaan keskuksen käyttöoikeus.</p> |
| Aallon lähetysten ylläpito                                  | Kyllä | Nro |
| Varastotyön käsittely (mukaan lukien rekisterikilven tulostus)        | Nro  | <p>Kyllä, mutta vain edellä mainittujen tuettujen ominaisuuksien osalta. |
| Klusterin keräily                                              | Nro  | Kyllä|
| Manuaalinen pakkaamisen käsittely, mukaan lukien Pakatun kontin keräily -työn käsittely | Nro <P>Osa käsittelystä voidaan tehdä scale unitin käsittelemän ensimmäisen keräilyn käsittelyn jälkeen, mutta sitä ei suositella seuraavien estettyjen toimintojen vuoksi.</p>  | Nro |
| Poista kontti ryhmästä                                  | Nro  | Nro |
| Lähtevien lajittelun käsittely                                  | Nro  | Nro |
| Lastaukseen liittyvien asiakirjojen tulostaminen                           | Kyllä | Nro |
| Rahtikirjan ja ASN-ilmoituksen luonti                            | Kyllä | Nro |
| Lähetyksen vahvistus                                             | Kyllä | Nro |
| Lähetyksen vahvistus sekä Vahvista ja siirrä            | Nro  | Nro |
| Pakkausluettelon ja laskutuksen käsittely                        | Kyllä | Nro |
| Lyhyt keräily (myynti- ja siirtotilaukset)                    | Nro  | Nro |
| Ylikeräily (myynti- ja siirtotilaukset)                     | Nro  | Nro |
| Työsijaintien muuttaminen (myynti- ja siirtotilaukset)         | Nro  | Kyllä|
| Työn viimeistely (myynti- ja siirtotilaukset)                    | Nro  | Kyllä|
| Työraportin tulostus                                            | Kyllä | Nro |
| Aallon otsikko                                                   | Nro  | Kyllä|
| Työn jako                                                   | Nro  | Kyllä|
| Työn käsittely – Kuljetuksen kuormaus -ohjattu            | Nro  | Nro |
| Vähennä kerättyä määrää                                       | Nro  | Nro |
| Palauta työ                                                 | Nro  | Nro |
| Käännä lähetyksen vahvistus                                | Kyllä | Nro |

### <a name="inbound"></a>Saapuva

Seuraava taulukko sisältää tuetut saapuvien toiminnot ja missä näitä toimintoja tuetaan, kun varastonhallinnan kuormituksia käytetään pilvi- ja reunapalvelujen scale uniteissa.

| Käsittele                                                          | Keskus | WES-kuormitus scale unitissa<BR>*(Nimikkeet, joissa on Kyllä-merkintä, koskevat vain varastotilauksia)*</p> |
|------------------------------------------------------------------|-----|----------------------------------------------------------------------------------|
| Lähdeasiakirjan&nbsp;käsittely                             | Kyllä | Nro |
| Lastauksen ja kuljetusten hallinnan käsittely                    | Kyllä | Nro |
| Saapuvan lähetyksen vahvistus                                    | Kyllä | Nro |
| Ostotilauksen vapautus varastoon (varastotilausten käsittely) | Kyllä | Nro |
| Varastotilausrivien peruuttaminen<p>Huomaa, että tätä tuetaan vain silloin, kun riviin ei kohdistu rekisteröintiä</p> | Kyllä | Nro |
| Ostotilausnimikkeen vastaanotto ja poispano                       | <p>Kyllä,&nbsp;kun &nbsp;varastotilausta ei&nbsp;ole</p><p>Ei, kun varastotilaus on</p> | <p>Kyllä, jos ostotilaus ei ole <i>kuorman</i> osa</p> |
| Ostotilausrivin vastaanotto ja poispano                       | <p>Kyllä, kun varastotilausta ei ole</p><p>Ei, kun varastotilaus on</p> | <p>Kyllä, jos ostotilaus ei ole <i>kuorman</i> osa</p></p> |
| Palautustilauksen vastaanotto ja poispano                              | Kyllä | Nro |
| Yhdistetyn rekisterikilven vastaanotto ja poispano                       | <p>Kyllä, kun varastotilausta ei ole</p><p>Ei, kun varastotilaus on</p> | Nro |
| Kuorman nimikkeen vastaanotto                                              | <p>Kyllä, kun varastotilausta ei ole</p><p>Ei, kun varastotilaus on</p> | Nro |
| Rekisterikilven vastaanotto ja poispano                             | <p>Kyllä, kun varastotilausta ei ole</p><p>Ei, kun varastotilaus on</p> | Nro |
| Siirtotilausnimikkeen vastaanotto ja poispano                       | Kyllä | Nro |
| Siirtotilausrivin vastaanotto ja poispano                       | Kyllä | Nro |
| Työn peruuttaminen (saapuva)                                            | <p>Kyllä, kun varastotilausta ei ole</p><p>Ei, kun varastotilaus on</p> | <p>Kyllä, mutta vain silloin kun <b>Poista vastaanoton rekisteröinti, kun työ peruutetaan</b> -asetuksen (<b>Varastonhallinnan parametrit</b> -sivulla) valinta on tyhjennetty</p> |
| Ostotilauksen tuotteen vastaanoton käsittely                        | Kyllä | Nro |
| Alitoimituksen sisältävän ostotilauksen vastaanotto                      | <p>Kyllä, kun varastotilausta ei ole</p><p>Ei, kun varastotilaus on</p> | Kyllä, mutta vain tekemällä peruutuspyyntö keskuksesta |
| Ylitoimituksen sisältävän ostotilauksen vastaanotto                       | <p>Kyllä, kun varastotilausta ei ole</p><p>Ei, kun varastotilaus on</p> | Kyllä  |
| *Cross docking* -työn luonnin sisältävä vastaanotto                 | <p>Kyllä, kun varastotilausta ei ole</p><p>Ei, kun varastotilaus on</p> | Nro |
| *Laatutilaus*-työn luonnin sisältävä vastaanotto                  | <p>Kyllä, kun varastotilausta ei ole</p><p>Ei, kun varastotilaus on</p> | Nro |
| *Laatunimikkeen otanta* -työn luonnin sisältävä vastaanotto          | <p>Kyllä, kun varastotilausta ei ole</p><p>Ei, kun varastotilaus on</p> | Nro |
| *Laatu laaduntarkistuksessa* -työn luonnin sisältävä vastaanotto       | <p>Kyllä, kun varastotilausta ei ole</p><p>Ei, kun varastotilaus on</p> | Nro |
| Laatutilauksen luonnin sisältävä vastaanotto                            | <p>Kyllä, kun varastotilausta ei ole</p><p>Ei, kun varastotilaus on</p> | Nro |
| Työnkäsittely – *Klusterihyllytys*-ohjattu                 | Kyllä | Nro |
| *Lyhyt keräilyn* sisältävän työn käsittely                               | Kyllä | Nro |
| Rekisterikilven lataus                                           | Kyllä | Kyllä |

### <a name="warehouse-operations-and-exception-handing"></a>Varastotoiminnot ja poikkeuksien käsittely

Seuraava taulukko sisältää tuetut varastotoimintojen ja poikkeuksien käsittelyn toiminnot ja missä näitä toimintoja tuetaan, kun varastonhallinnan kuormituksia käytetään pilvi- ja reunapalvelujen scale uniteissa.

| Prosessoi                                            | Keskus | WES-kuormitus scale unitissa |
|----------------------------------------------------|-----|------------------------------|
| Rekisterikilpikysely                              | Kyllä | Kyllä                          |
| Nimikekysely                                       | Kyllä | Kyllä                          |
| Sijaintikysely                                   | Kyllä | Kyllä                          |
| Vaihda varastoa                                   | Kyllä | Kyllä                          |
| Siirto                                           | Kyllä | Kyllä                          |
| Siirto mallin mukaan                               | Kyllä | Kyllä                          |
| Varastosiirto                                 | Kyllä | Nro                           |
| Siirtotilauksen luominen varastosovelluksesta           | Kyllä | Nro                           |
| Oikaisu (sisään/ulos)                                | Kyllä | Kyllä, mutta ei oikaisu ulos -skenaariota varten, jossa varastovaraus on poistettava käyttämällä varasto-oikaisutyyppien **Poista varaukset** -asetusta.</p>                           |
| Varaston tilamuutos                            | Kyllä | Nro                           |
| Inventointi ja poikkeamien käsittely | Kyllä | Kyllä                           |
| Etiketin uudelleentulostus (rekisterikilven tulostus)             | Kyllä | Kyllä                          |
| Rekisterikilpikoonti                                | Kyllä | Nro                           |
| Rekisterikilven tauko                                | Kyllä | Nro                           |
| Pakkaa sisäkkäisiin rekisterikilpiin                                | Kyllä | Nro                           |
| Kuljettajan sisäänkuittaus                                    | Kyllä | Nro                           |
| Kuljettajan uloskuittaus                                   | Kyllä | Nro                           |
| Eräkäsittelykoodin muuttaminen                      | Kyllä | Kyllä                          |
| Näytä avoin työluettelo                             | Kyllä | Kyllä                          |
| Konsolidoi rekisterikilvet                         | Kyllä | Nro                           |
| Vähimmäis- ja enimmäistäydennyksen sekä vyöhykkeen rajatäydennyksen käsittely| Kyllä <p>Suosituksena on, että samaa sijaintia ei sisällytetä kyselyjen osana</p>| Kyllä                          |
| Paikoitustäydennyksen käsittely                  | Kyllä  | Kyllä<p>Huomaa, että määritys on tehtävä scale unitissa</p>                           |
| Työn esto ja eston poisto                             | Kyllä | Kyllä                          |
| Vaihda käyttäjä                                        | Kyllä | Kyllä                          |
| Työpoolin vaihtaminen työssä                           | Kyllä | Kyllä                          |
| Peruuta työ                                        | Kyllä | Kyllä                          |

### <a name="production"></a>Tuotantoympäristö

Seuraavassa taulukossa esitellään, mitä varastonhallinnan tuotantoskenaarioita tuetaan (ja ei tueta) tällä hetkellä Scale Unitin työkuormissa.

| Käsittele | Keskus | WES-kuormitus scale unitissa |
|---------|-----|------------------------------|
| Ilmoita valmiiksi ja valmiiden tuotteiden hyllytys | Kyllä | Kyllä |
| Rinnakkaistuotteen ja sivutuotteen poispano | Kyllä | Kyllä |
| <p>Kaikki muut tuotantoon liittyvät varastonhallintaprosessit, esim:</p><li>Vapauta varastoon</li><li>Tuotannon aallon käsittely</li><li>Raaka-aineiden keräily</li><li>Kanban-poispano</li><li>Kanban-keräily</li><li>Käynnistä tuotantotilaus</li><li>Tuotannon hävikki</li><li>Tuotannon viimeinen kuormalava</li><li>Rekisteröi materiaalikulutus</li><li>Tyhjennä kanban</li></ul> | Kyllä | Nro |
| Raaka-aineiden täydennys | Nro | Nro |

## <a name="maintaining-scale-units-for-wes"></a>WES-järjestelmän scale unitien ylläpito

Useita erätöitä suoritetaan sekä keskuksessa että scale uniteissa

Erätöitä voidaan ylläpitää manuaalisesti keskuskäyttöönotossa. Seuraavia erätyötä voi hallita valitsemalla **Varastonhallinta \> Kausittaiset tehtävät \> Taustatoimintojen kuormituksen hallinta**:

- Scale Unitin ja keskuksen välinen sanoman käsittelijä
- Rekisteröi lähdetilauksen vastaanotot
- Viimeistele varastotilaukset

Scale unitien kuormituksissa voi hallita seuraavia erätöitä valitsemalla **Varastonhallinta \> Kausittaiset tehtävät \> Kuormituksen hallinta**:

- Aaltotaulukon tietueiden käsittely
- Varastokeskuksen yksikkösanoman käsittelijä
- Käsittele varastotilausrivien määräpäivityspyynnöt

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
