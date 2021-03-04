---
title: Varastonhallinnan kuormitusten pilvi- ja reunapalvelujen scale unitit
description: Tässä aiheessa on tietoja toiminnossa, jonka avulla scale unitit voivat suorittaa valittuja prosesseja varastonhallinnan kuormituksesta.
author: perlynne
manager: tfeyr
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, SysSecRolesEditUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4ac76ad5cd88c35ac312b8e73d942a692f35c8aa
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516774"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Varastonhallinnan kuormitusten pilvi- ja reunapalvelujen scale unitit

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> Kaikkia liiketoimintatoimintoja ei tueta kokonaisuudessaan julkisessa esiversiossa, kun kuormituksen scale uniteja käytetään. Varmista, että käytät vain niitä prosesseja, joiden tuesta nimenomaisesti ilmoitetaan tässä aiheessa.

## <a name="warehouse-execution-on-scale-units"></a>Scale unitien varastonohjaus

Tämän toiminnon avulla scale unitit voivat suorittaa valittuja prosesseja varastonhallinnan ominaisuuksista. Pilvipalvelujen scale unitit suorittavat kuormitukset pilvessä käyttämällä erillisistä käsittelykapasiteettia valitulla Microsoft Azure -alueella. Reunapalvelujen scale uniteissa voidaan suorittaa joitakin kuormituksia erikseen paikallisesti, vaikka scale unitien yhteys pilvipalveluihin olisi tilapäisesti katkennut.

Tässä aiheessa varastonhallinnan ohjausta varastossa, joka on määritetty scale unitiksi, kutsutaan *varastonohjausjärjestelmäksi* (*WES*).

## <a name="prerequisites"></a>Edellytykset

Käytössä on oltava Dynamics 365 Supply Chain Managementin keskus ja scale unit, jonka käyttöönottoon sisältyy varastonhallinnan kuormitus. Lisätietoja on arkkitehtuurista ja käyttöönottoprosessista on kohdassa [Valmistuksen ja varastoinnin hallinnan kuormitusten pilvi- ja reunapalvelujen Scale Unitit](cloud-edge-landing-page.md).

## <a name="how-the-wes-workload-works-on-scale-units"></a>WES-kuormituksen käyttäminen scale uniteissa

Varastonhallinnan kuormitusprosesseissa tiedot synkronoidaan keskuksen ja scale unitien välillä.

Scale unit voi ylläpitää vain omistamiaan tietoja. Scale unitien tietojen omistuksen käsite auttaa estämään moni-isäntäristiriidat. Tämän on tärkeää tietää, mitkä prosessit ovat keskuksen ja mitkä scale unitien omistamia.

Scale unitit omistavat seuraavat tiedot:

- **Aallon käsittelyn tiedot** – valitut aallon käsittelymenetelmät käsitellään scale unitin aallon käsittelyn osana.
- **Työn käsittelyn tiedot** – Seuraavanlaisia työtilausten käsittelyjä tuetaan:

    - Varastosiirrot (manuaalinen siirto ja mallityön mukainen siirto)
    - Ostotilaukset (hyllytystyö varastotilauksen perusteella)
    - Myyntitilaukset (yksinkertainen keräily- ja lastaustyö)

- **Varastotilauksen vastaanoton tiedot** – näitä tietoja käytetään vain ostotilauksissa, jotka vapautetaan manuaalisesti varastoon.
- **Rekisterikilven tiedot** – Rekisterikilpiä voidaan luoda keskuksessa ja scale unitissa. Erillinen ristiriitojen käsittely on mahdollista. Huomaa, että nämä tiedot eivät ole varastokohtaisia.

## <a name="outbound-process-flow"></a>Lähtevien käsittelyn työnkulku

Keskus omistaa seuraavat tiedot:

- Kaikki lähdeasiakirjat, kuten myyntitilaukset ja siirtotilaukset
- Tilausten kohdistus ja lähtevän kuorman käsittely
- Vapautus varastoon, lähetyksen luonti ja aallon luontiprosessit

Scale unitit omistavat varsinaisen aalloin käsittelyn (kuten työn kohdistamisen, täydennystyön ja kysynnän työn luonnin) aallon vapautuksen jälkeen. Niinpä varastotyöntekijät voivat käsitellä lähtevän työn käyttämällä scale unitiin yhdistettyä varastosovellusta.

![Aallon käsittelyn työnkulku](./media/wes_wave_processing_flow.png "Aallon käsittelyn työnkulku")

## <a name="inbound-process-flow"></a>Saapuvien käsittelyn työnkulku

Keskus omistaa seuraavat tiedot:

- Kaikki lähdeasiakirjat, kuten ostotilaukset ja myynnin palautustilaukset
- Saapuvan kuorman käsittely

> [!NOTE]
> Saapuvan ostotilauksen työnkulku poikkeaa käsitteellisesti lähtevien työnkulusta, ja käsittelyn suorittava scale unit määräytyy sen mukaan, onko tilaus vapautettu varastoon.

Jos käytössä on *varastoon vapautuksen* prosessi, varastotilaukset luodaan ja liittyvän vastaanoton työnkulun omistus määritetään scale unitille. Keskus ei voi rekisteröidä saapuvaa vastaanottoa.

Työntekijä voi suorittaa vastaanottoprosessin käyttämällä scale unitiin yhdistettyä varastosovellusta. Tiedot kirjataan sitten scale unitin mukaan ja raportoidaan saapuvan varastotilauksen perusteella. Scale unit käsittelee myös myöhemmin tehtävän hyllytyksen luonnin ja käsittelyn.

Jos *varastoon vapauttamisen* prosessi ei ole käytössä, jolloin myöskään *varastotilaukset* eivät ole käytössä, keskus voi käsitellä varaston vastaanoton ja työn käsittelyn erillään scale uniteista.

![Saapuvien käsittelyn työnkulku](./media/wes_Inbound_flow.png "Saapuvien käsittelyn työnkulku")

## <a name="supported-processes-and-roles"></a>Tuetut prosessit ja roolit

Scale unitin WES-kuormitus ei tue kaikkia varastonhallintaprosesseja. Tämän vuoksi kannattaa määrittää roolit, jotka vastaavan kunkin käyttäjän käytettävissä olevia toimintoja.

Tämä prosessia helpottamaan on luotu *Kuormituksen varastopäällikkö* -niminen mallirooli, joka sisältyy esittelytietoihin. Nämä tiedot saa käyttöön valitsemalla **Järjestelmänhallinta \> Suojaus \> Suojausmääritys**. Tämän roolin tarkoitus on antaa varastopäälliköille mahdollisuus käyttää scale unitin WES-järjestelmää. Rooli antaa niiden sivujen käyttöoikeuden, joita tarvitaan scale unitin isännöimän kuormituksen yhteydessä.

Scale unitin käyttäjäroolit määritetään osana tietojen ensimmäistä synkronointia keskuksesta scale unitiin.

Käyttäjälle määritettyjä rooleja voi muokata valitsemalla scale unitissa **Järjestelmänhallinta \> Suojaus \> Määritä käyttäjät rooleihin**. Käyttäjille, jotka toimivat varastopäällikköinä vain scale uniteissa, on määritettävä ainoastaan *Kuormituksen varastopäällikkö* -rooli. Tämä menettely varmistaa, että kyseisillä käyttäjillä on vain tuettujen toimintojen käyttöoikeus. Poista kaikki muut kyseisille käyttäjille määritetyt roolit.

Käyttäjille, jotka toimivat varastopäällikköinä sekä keskuksessa että scale uniteissa, on määritettävä nykyinen *Varastopäällikkö*-rooli. Ota huomioon, että tämä rooli antaa varastotyöntekijöille mahdollisuuden käyttää toimintoja (kuten siirtotilauksen käsittelyä), jotka näkyvät käyttöliittymässä mutta joita ei tällä hetkellä tueta scale uniteissa.

## <a name="supported-wes-processes"></a>Tuetut WES-prosessit

Seuraavat varastonohjausprosessit voidaan ottaa käyttöön scale unitin WES-kuormituksessa:

- Myyntitilausten ja kysynnän täydennyksen valitut aaltomenetelmät
- Työtilausten suorittaminen myyntitilauksista ja kysynnän täydennyksestä varastosovelluksella
- Käytettävissä olevan varaston kysely varastosovelluksella
- Varastosiirtojen luominen ja suorittaminen varastosovelluksella
- Ostotilausten rekisteröinti ja hyllytystöiden tekeminen varastosovelluksella.

Seuraavia työtilaustyyppejä tuetaan tällä hetkellä scale unit -käyttöönottojen WES-kuormituksissa:

- Myyntitilaukset
- Täydennys
- Varaston siirtotapahtuma
- Varastotilauksiin linkitetyt ostotilaukset

Scale uniteissa ei tueta tällä hetkellä muuta lähdeasiakirjojen käsittelyä. Scale unit WES-kuormituksessa ei voi suorittaa esimerkiksi seuraavia toimintoja:

- Siirtotilauksen vapauttaminen
- Lähtevien varaston keräily- ja lähetystoimintojen käsitteleminen

> [!IMPORTANT]
> Jos käytössä scale unitin kuormitus, prosesseja, joita ei tueta, ei voi suorittaa tietyn varaston osalta keskuksessa.

Seuraavia varastonhallintatoimintoja ei tueta tällä hetkellä scale uniteissa:

- Sellaisten nimikkeiden saapuvien ja lähtevien käsittely, joissa on aktiivisia seurantadimensiota (kuten erä- tai sarjanumerodimensioita)
- Varastotilan muutosten käsittely
- Sellaisen varaston käsittely, jonka tilan-arvona on esto
- Laadunvalvonnan sisältävä integrointi
- Tuotannon integrointi
- Todellisen painon nimikkeiden käsittely
- Ylitoimituksen ja alitoimituksen käsittely
- Negatiivisen käytettävissä olevan varaston käsittely

### <a name="outbound-supported-only-for-sales-orders-and-demand-replenishment"></a>Lähtevät (tuetaan vain myyntitilauksissa ja kysynnän täydennyksessä)

Seuraava taulukko sisältää tuetut lähtevät toiminnot ja missä näitä toimintoja tuetaan, kun varastonhallinnan kuormituksia käytetään pilvi- ja reunapalvelujen scale uniteissa.

> [!WARNING]
> Koska vain myyntitilauksia tuetaan, lähtevien varastonhallinnan käsittelyä ei voi käyttää siirtotilauksissa.
>
> Jotkin varastotoiminnot eivät ole käytettävissä varastoissa, joissa suoritetaan varastonhallinnan kuormituksia scale unitissa.

| Prosessoi                                                      | Keskus | WES-kuormitus scale unitissa |
|--------------------------------------------------------------|-----|------------------------------|
| Lähdeasiakirjan käsittely                                   | Kyllä | Nro |
| Lastauksen ja kuljetusten hallinnan käsittely                | Kyllä | Nro |
| Vapauta varastoon                                         | Kyllä | Nro |
| Lähetyksen konsolidointi                                       | Nro  | Nro |
| Cross docking (keräilytyö)                                 | Nro  | Nro |
| Lähetysaallon käsittely                                     | Ei, mutta aallon tilan viimeistely käsitellään keskuksessa. |<p>Kyllä, mutta seuraavia ominaisuuksia ei tueta:</p><ul><li>Rinnakkainen työn luonti</li><li>Kuorman luonti ja lajittelu</li><li>Konttiinpakkaus</li><li>Aallon etiketin tulostus</li></li></ul><p><b>Huomautus:</b> aallon tilan viimeistelyyn aallon käsittelyn osana tarvitaan keskuksen käyttöoikeus.</p> |
| Varastotyön käsittely (mukaan lukien rekisterikilven tulostus)     | Nro  | <p>Kyllä, mutta vain seuraavissa ominaisuuksissa:</p><ul><li>Myynnin keräily (ilman aktiivisten seurantadimensioiden käyttöä)</li><li>Myynnin lastaus (ilman aktiivisten seurantadimensioiden käyttöä)</li></ul> |
| Klusterin keräily                                              | Nro  | Nro |
| Pakkaamisen käsittely                                           | Nro  | Nro |
| Lähtevien lajittelun käsittely                                  | Nro  | Nro |
| Lastaukseen liittyvien asiakirjojen tulostaminen                           | Kyllä | Nro |
| Rahtikirjan ja ASN-ilmoituksen luonti                            | Kyllä | Nro |
| Lähetyksen vahvistuksen ja pakkausluettelon käsittely                | Kyllä | Nro |
| Lyhyt keräily (myyntitilaukset)                                 | Nro  | Nro |
| Työn peruutus                                            | Nro  | Nro |
| Työsijaintien muuttaminen (myyntitilaukset)                      | Nro  | Nro |
| Työn viimeistely (myyntitilaukset)                                 | Nro  | Nro |
| Työn esto ja eston poisto                                       | Nro  | Nro |
| Vaihda käyttäjä                                                  | Nro  | Nro |
| Työraportin tulostus                                            | Nro  | Nro |
| Aallon otsikko                                                   | Nro  | Nro |
| Palauta työ                                                 | Nro  | Nro |

### <a name="inbound"></a>Saapuva

Seuraava taulukko sisältää tuetut saapuvien toiminnot ja missä näitä toimintoja tuetaan, kun varastonhallinnan kuormituksia käytetään pilvi- ja reunapalvelujen scale uniteissa.

| Prosessoi                                                          | Keskus | WES-kuormitus scale unitissa |
|------------------------------------------------------------------|-----|------------------------------|
| Lähdeasiakirjan&nbsp;käsittely                                       | Kyllä | Nro |
| Lastauksen ja kuljetusten hallinnan käsittely                    | Kyllä | Nro |
| Lähetyksen vahvistus                                            | Kyllä | Nro |
| Ostotilauksen vapautus varastoon (varastotilausten käsittely) | Kyllä | Nro |
| Ostotilausnimikkeen vastaanotto ja poispano                        | <p>Kyllä,&nbsp;kun &nbsp;varastotilausta ei&nbsp;ole</p><p>Ei, kun varastotilaus on</p> | <p>Kyllä, kun varastotilaus on ja kun ostotilaus ei ole <i>kuorman</i> osa. On kuitenkin käytettävä kahta mobiililaitteen valikkovaihtoehtoa: toista vastaanottoon (<i>Ostotilausnimikkeen vastaanotto</i>) ja toista hyllytyksen käsittelyyn <b>Käytä aiemmin luotua työtä</b> -asetus käyttöönotettuna.</p><p>Ei, kun varastotilausta ei ole.</p> |
| Ostotilausrivin vastaanotto ja poispano                        | <p>Kyllä, kun varastotilausta ei ole</p><p>Ei, kun varastotilaus on</p> | Nro |
| Palautustilauksen vastaanotto ja poispano                               | Kyllä | Nro |
| Yhdistetyn rekisterikilven vastaanotto ja poispano                        | <p>Kyllä, kun varastotilausta ei ole</p><p>Ei, kun varastotilaus on</p> | Nro |
| Kuorman nimikkeen vastaanotto                                              | <p>Kyllä, kun varastotilausta ei ole</p><p>Ei, kun varastotilaus on</p> | Nro |
| Rekisterikilven vastaanotto ja poispano                              | <p>Kyllä, kun varastotilausta ei ole</p><p>Ei, kun varastotilaus on</p> | Nro |
| Siirtotilausnimikkeen vastaanotto ja poispano                        | Kyllä | Nro |
| Siirtotilausrivin vastaanotto ja poispano                        | Kyllä | Nro |
| Työn peruutus                                                | <p>Kyllä, kun varastotilausta ei ole</p><p>Ei, kun varastotilaus on</p> | <p>Kyllä, mutta <b>Poista vastaanoton rekisteröinti, kun työ peruutetaan</b> -asetusta (<b>Varastonhallinnan parametrit</b> -sivulla) ei tueta.</p> |
| Ostotilauksen tuotteen vastaanoton käsittely                        | Kyllä | Nro |
| Cross docking -työn luonti vastaanoton osana                 | <p>Kyllä, kun varastotilausta ei ole</p><p>Ei, kun varastotilaus on</p> | Nro |

### <a name="warehouse-operations-and-exception-handing"></a>Varastotoiminnot ja poikkeuksien käsittely

Seuraava taulukko sisältää tuetut varastotoimintojen ja poikkeuksien käsittelyn toiminnot ja missä näitä toimintoja tuetaan, kun varastonhallinnan kuormituksia käytetään pilvi- ja reunapalvelujen scale uniteissa.

| Prosessoi                                            | Keskus | WES-kuormitus scale unitissa |
|----------------------------------------------------|-----|------------------------------|
| Rekisterikilpikysely                              | Kyllä | Kyllä                          |
| Nimikekysely                                       | Kyllä | Kyllä                          |
| Sijaintikysely                                   | Kyllä | Kyllä                          |
| Vaihda varastoa                                   | Kyllä | Kyllä                          |
| Siirto                                           | Nro  | Kyllä                          |
| Siirto mallin mukaan                               | Nro  | Kyllä                          |
| Oikaisu (sisään/ulos)                                | Kyllä | Nro                           |
| Inventointi ja poikkeamien käsittely | Kyllä | Nro                           |
| Etiketin uudelleentulostus (rekisterikilven tulostus)             | Kyllä | Nro                           |
| Rekisterikilpikoonti                                | Kyllä | Nro                           |
| Rekisterikilven tauko                                | Kyllä | Nro                           |
| Kuljettajan sisäänkuittaus                                    | Kyllä | Nro                           |
| Kuljettajan uloskuittaus                                   | Kyllä | Nro                           |
| Eräkäsittelykoodin muuttaminen                      | Kyllä | Nro                           |
| Näytä avoin työluettelo                             | Kyllä | Nro                           |
| Konsolidoi rekisterikilvet                         | Nro  | Nro                           |
| Poista kontti ryhmästä                        | Nro  | Nro                           |
| Peruuta työ                                        | Nro  | Nro                           |
| Vähimmäis- ja enimmäistäydennyksen käsittely                   | Nro  | Nro                           |
| Paikoitustäydennyksen käsittely                  | Nro  | Nro                           |

### <a name="production"></a>Tuotantoympäristö

Tuotantoskenaarioiden varastonhallinnan integrointia ei tueta tällä hetkellä, kuten seuraava taulukko osoittaa.

| Prosessoi | Keskus | WES-kuormitus scale unitissa |
|---------|-----|------------------------------|
| <p>Kaikki tuotantoon liittyvät varastonhallintaprosessit Seuraavassa on muutamia esimerkkejä:</p><li>Vapauta varastoon</li><li>Tuotannon aallon käsittely</li><li>Raaka-aineiden keräily</li><li>Valmiiden tuotteiden poispano</li><li>Rinnakkaistuotteen ja sivutuotteen poispano</li><li>Kanban-poispano</li><li>Kanban-keräily</li><li>Käynnistä tuotantotilaus</li><li>Tuotannon hävikki</li><li>Tuotannon viimeinen kuormalava</li><li>Rekisteröi materiaalikulutus</li><li>Tyhjennä kanban</li></ul> | Nro | Nro |

## <a name="maintaining-scale-units-for-wes"></a>WES-järjestelmän scale unitien ylläpito

Useita erätöitä suoritetaan sekä keskuksessa että scale uniteissa

Erätöitä voidaan ylläpitää manuaalisesti keskuskäyttöönotossa. Seuraavia kolmea työtä voi hallita valitsemalla **Varastonhallinta \> Kausittaiset tehtävät \> Taustatoimintojen kuormituksen hallinta**:

- Käsittele työn tilan päivitystapahtumat
- Käsittele aallon suorituksenhallinnan siirtotapahtumat
- Rekisteröi lähdetilauksen vastaanotot

Scale unitien kuormituksissa voi hallita kahta seuraavaa erätyötä valitsemalla **Varastonhallinta \> Kausittaiset tehtävät \> Kuormituksen hallinta**:

- Aaltotaulukon tietueiden käsittely
- Käsittele aallon suorituksenhallinnan siirtotapahtumat


[!INCLUDE[footer-include](../../includes/footer-banner.md)]