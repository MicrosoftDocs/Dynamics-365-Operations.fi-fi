---
title: Laadunhallinnan testiryhmät
description: Tässä aiheessa kuvataan, kuinka testiryhmiä luodaan, jotta laatutilauksissa voidaan käyttää useita testejä Microsoft Dynamics 365 Supply Chain Managementissa.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fdd7c2eb452d7d34e05d9e067e61d6587e1fd4b67b22723ecef2832501be1eaf
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6774123"
---
# <a name="quality-management-test-groups"></a>Laadunhallinnan testiryhmät

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, kuinka testiryhmiä luodaan, jotta laatutilauksissa voidaan käyttää useita testejä Microsoft Dynamics 365 Supply Chain Managementissa.

Voit määrittää, muokata ja tarkastella testiryhmiä ja testiryhmälle määritettyjä yksittäisiä testejä **Testiryhmä**-sivulla. Sivun yläosassa näkyvät testiryhmät, ja alaosassa näkyvät valitulle testiryhmälle määritetyt testit.

Voit määrittää testiryhmälle useita käytäntöjä, kuten otantasuunnitelman, hyväksytyn laatutason ja destruktiivisen testin tarpeen. Kun määrität testiryhmään yksittäisen testin, määrität samalla lisätietoja, kuten järjestyksen, asiakirjat ja voimassaolopäivät. Määrällisessä testissä määritetään myös hyväksyttävät mitta-arvot. Laadullisessa testissä tietoja ovat testimuuttuja ja oletustulos.

Laatutilaukseen määritetty testiryhmä määrittää oletustestit, jotka tietylle nimikkeelle on suoritettava. Voit kuitenkin lisätä, muuttaa ja poistaa laatutilauksen testejä. Laatutilauksen jokaisen testin tulokset raportoidaan.

Kun määrität testiryhmän, voit halutessasi määrittää nimikeotantamenetelmän. Nimikeotantoja käytetään testattavan tuotteen määrän määrittämiseen. Lisätietoja on kohdassa [Laadunhallinnan nimikeotanta](quality-item-sampling.md). Voit myös määrittää, ovatko testiryhmän testit destruktiivisia. Destruktiivisessa testissä nimikeotanta tuhotaan ja määrä poistetaan käytettävissä olevasta varastosta.

## <a name="example-of-a-test-group"></a>Esimerkki testiryhmästä

Tuotantoyritys määrittää testiryhmän kutakin laatuvaatimusversiotaan varten. Eri testiryhmät edustavat eroja otantasuunnitelmissa, yhdessä suoritettavissa testeissä, hyväksytyissä mitta-arvoissa ja muissa seikoissa. Määrällisissä testeissä eroja on hyväksyttävissä mitta-arvoissa. Laatuohjeidensa noudattamista varten yritys liittää testiryhmän kuhunkin sääntöön, jota käytetään laatutilausten tuottamiseen automaattisesti **Laatuliitokset**-sivulla. Se liittää myös testiryhmän manuaalisesti luotuihin laatutilauksiin.

## <a name="create-a-test-group"></a>Testiryhmän luominen

Voit luoda testiryhmän seuraavasti.

1. Valitse **Varastonhallinta \> Asetukset \> Laadunvalvonta \> Testiryhmät**.
1. Valitse toimintoruudussa **Uusi** lisätäksesi rivin ruudukkoon sivun yläosassa. Määritä sitten uudelle rivillä seuraavat kentät:

    - **Testiryhmä** – Määritä testiryhmän yksilöivä tunnus tai nimi.
    - **Kuvaus** – Anna testiryhmän yksityiskohtainen kuvaus.
    - **Hyväksyttävän laadun taso** – Määritä testitulosten kokonaisprosentti, joka on hyväksyttävä, jotta testiryhmä voidaan katsoa hyväksytyksi.
    - **Nimikeotanta** – Valitse nimikeotanta. Lisätietoja on kohdassa [Laadunhallinnan nimikeotanta](quality-item-sampling.md).
    - **Destruktiivinen** – Valitsemalla tämän valintaruudun voit määrittää, että testiryhmä tuhoaa testatut nimikkeet.

1. Kun uusi rivi on vielä valittuna, valitse sivun yläosasta **Yleiset**-välilehti. Osa **Yhteenveto**-välilehdessä valitun testiryhmän asetuksista toistetaan tässä. Voit määrittää ryhmälle myös seuraavat kentät:

    - **Päivitä varaston erämäärite** – Kun määrität tämän asetuksen arvoksi *Kyllä* tässä, arvoksi määritetään automaattisesti *Kyllä* kaikille uusille testeille, jotka lisätään sivun alaosan testiryhmään.
    - **Päivitä eräkäsittely** – Kun määrität tämän asetuksen arvoksi *Kyllä*, jos testattavaa nimikettä ohjataan eräkäsittelyllä, eräkäsittely päivittyy automaattisesti arvolla, joka on valittu **Epäonnistuneen laatutilauserän käsittely**- tai **Onnistuneen laatutilauserän käsittely** -kentässä.
    - **Epäonnistuneen laatutilauserän käsittely** – Valitse erän käsittelykoodi, joka on pitäisi määrittää, kun tämän testiryhmän sisältävä laatutilaus epäonnistuu, koska se ei täytä hyväksyttävän laadun tasoa.
    - **Onnistuneen laatutilauserän käsittely** – Valitse erän käsittelykoodi, joka on pitäisi määrittää, kun tämän testiryhmän sisältävä laatutilaus onnistuu, koska se täyttää hyväksyttävän laadun tason.
    - **Päivitä varaston tila** – Kun määrität tämän asetuksen arvoksi *Kyllä*, jos testattavan nimikkeen varastodimensioryhmän **Varastotila** on otettu käyttöön, tilaksi päivitetään automaattisesti tila, joka on valittuna **Epäonnistuneen laatutilauksen tila**- tai **Onnistuneen laatutilauksen tila** -kentässä.
    - **Epäonnistuneen laatutilauksen tila** – Valitse varastotila, joka on pitäisi määrittää nimikkeelle, kun tämän testiryhmän sisältävä laatutilaus epäonnistuu, koska se ei täytä hyväksyttävän laadun tasoa.
    - **Onnistuneen laatutilauksen tila** – Valitse varastotila, joka on pitäisi määrittää nimikkeelle, kun tämän testiryhmän sisältävä laatutilaus onnistuu, koska se täyttää hyväksyttävän laadun tason.

## <a name="add-a-qualitative-test-to-a-test-group"></a>Laadullisen testin lisääminen testiryhmään

Voit lisätä laadullisen testin testiryhmään noudattamalla seuraavia vaiheita.

1. Valitse **Varastonhallinta \> Asetukset \> Laadunvalvonta \> Testiryhmät**.
1. Valitse **Yhteenveto**-välilehdestä sivun yläosassa testiryhmä, johon haluat lisätä testin.
1. Lisää rivi ruudukkoon valitsemalla sivun alaosan **Yhteenveto**-välilehdestä **Lisää**. Määritä sitten uudelle rivillä seuraavat kentät:

    - **Järjestysnumero** – Kirjoita kokonaisluku, joka määrittää järjestyksen, jossa testit on suoritettava. Pienemmällä järjestysnumerolla olevat testit suoritetaan ennen kuin testejä, joilla on suuremmat järjestysnumerot.

        > [!NOTE]
        > Suosittelemme, että jätät järjestysnumeroiden väliin välin. Määritä esimerkiksi ensimmäisen testin **Järjestysnumero**-kentän arvoksi *10* ja lisää sitten kunkin lisätestin arvoa 10:llä. Näin voit lisätä uusia testejä myöhemmin ilman, että rivejä tarvitsee poistaa ja luoda uudelleen, jotta testit voidaan asettaa haluttuun järjestykseen.

    - **Testt** – Valitse suoritettava testi. Valitse laadullista testiä varten testi, jossa **Tyyppi**-kentän arvoksi on määritetty *Asetus*.
    - **Voimassa** – Valitse ensimmäinen päivämäärä, jolloin testi on voimassa. Jos jätät kentän tyhjäksi, rajaa ei ole.
    - **Vanhentumisaika** – Valitse viimeinen päivämäärä, jolloin testi on voimassa. Jos jätät tämän kentän tyhjäksi tai määrität sen arvoksi *Ei koskaan*, rajaa ei ole.
    - **Testiarvon määritys** – Valitse, miten hyväksyttävän laadun taso määritetään, kun samalle testille kirjataan useita tuloksia. Laadullista testiä varten voidaan valita vain *Manuaalinen*. Jos valitset toisen arvoista (*Keskimääräinen*, *Minimi* tai *Maksimi*), näyttöön tulee virhesanoma, kun tallennat testiryhmän.
    - **Määrite** – Jos haluat tallentaa testitulokset erämääritteeseen, valitse määrite tästä ja valitse **Päivitä varaston erämäärite** -valintaruutu.
    - **Päivitä varaston erämäärite** – Valitse tämä valintaruutu, jos haluat tallentaa testituloksia erämääritteelle, joka on valittuna **Määrite**-kentässä.

1. Valitse sivun alaosasta **Yleiset**-välilehti. Osa **Yhteenveto**-välilehdessä valitun testin asetuksista toistetaan tässä. Voit määrittää testille myös seuraavat kentät:

    - **Analyysitodistusraportti** – Määritä tämän asetuksen arvoksi *Kyllä*, kun haluat, että testitulokset tulostetaan analyysitodistukseen (CoA). Tämän raportin voi luoda laatutilauksesta.
    - **Virheen yhteydessä tehtävä toiminto** – Valitse joko *Hyväksy* tai *Epäonnistuminen* ilmaistaksesi, hyväksytäänkö vai hylätäänkö testi, jos sen hyväksyttävän laadun taso ei täyty.
    - **Hyväksyttävän laadun taso** – Määritä testitulosten kokonaisprosentti, joka on hyväksyttävä, jotta testi voidaan katsoa hyväksytyksi.

1. Määritä sivun alaosan **Testi**-välilehdessä seuraavat kentät:

    - **Muuttuja** – Valitse testimuuttuja laadullisen testin tulosten tallentamista varten.
    - **Oletustulos** – Valitse oletustulos, joka pitäisi tallentaa testituloksille.
    - **Testin mittaväline** – Valitse laite, jota testissä on käytettävä. Jos testille on määritetty mittaväline, se syötetään testiryhmän testille automaattisesti.

1. Sulje sivu.

## <a name="add-a-quantitative-test-to-a-test-group"></a>Määrällisen testin lisääminen testiryhmään

Voit lisätä määrällisen testin testiryhmään noudattamalla seuraavia vaiheita.

1. Valitse **Varastonhallinta \> Asetukset \> Laadunvalvonta \> Testiryhmät**.
1. Valitse **Yhteenveto**-välilehdestä sivun yläosassa testiryhmä, johon haluat lisätä testin.
1. Lisää rivi ruudukkoon valitsemalla sivun alaosan **Yhteenveto**-välilehdestä **Lisää**. Määritä sitten uudelle rivillä seuraavat kentät:

    - **Järjestysnumero** – Kirjoita kokonaisluku, joka määrittää järjestyksen, jossa testit on suoritettava. Pienemmällä järjestysnumerolla olevat testit suoritetaan ennen kuin testejä, joilla on suuremmat järjestysnumerot.

        > [!NOTE]
        > Suosittelemme, että jätät järjestysnumeroiden väliin välin. Määritä esimerkiksi ensimmäisen testin **Järjestysnumero**-kentän arvoksi *10* ja lisää sitten kunkin lisätestin arvoa 10:llä. Näin voit lisätä uusia testejä myöhemmin ilman, että rivejä tarvitsee poistaa ja luoda uudelleen, jotta testit voidaan asettaa haluttuun järjestykseen.

    - **Testt** – Valitse suoritettava testi. Valitse määrällistä testiä varten testi, jossa **Tyyppi**-kentän arvoksi on määritetty *Murtoluku* tai *Kokonaisluku*.
    - **Voimassa** – Valitse ensimmäinen päivämäärä, jolloin testi on voimassa. Jos jätät kentän tyhjäksi, rajaa ei ole.
    - **Vanhentumisaika** – Valitse viimeinen päivämäärä, jolloin testi on voimassa. Jos jätät tämän kentän tyhjäksi tai määrität sen arvoksi *Ei koskaan*, rajaa ei ole.
    - **Testiarvon määritys** – Valitse, miten hyväksyttävän laadun taso määritetään, kun samalle testille kirjataan useita tuloksia. Käytettävissä olevat asetukset ovat *Keskimääräinen*, *Minimi*, *Maksimi* ja *Manuaalinen*.
    - **Määrite** – Jos haluat tallentaa testitulokset erämääritteeseen, valitse määrite tästä ja valitse **Päivitä varaston erämäärite** -valintaruutu.
    - **Päivitä varaston erämäärite** – Valitse tämä valintaruutu, jos haluat tallentaa testituloksia erämääritteelle, joka on valittuna **Määrite**-kentässä.

1. Valitse sivun alaosasta **Yleiset**-välilehti. Osa **Yhteenveto**-välilehdessä valitun testin asetuksista toistetaan tässä. Voit määrittää testille myös seuraavat kentät:

    - **Analyysitodistusraportti** – Määritä tämän asetuksen arvoksi *Kyllä*, kun haluat, että testitulokset tulostetaan analyysitodistukseen (CoA). Tämän raportin voi luoda laatutilauksesta.
    - **Virheen yhteydessä tehtävä toiminto** – Valitse joko *Hyväksy* tai *Epäonnistuminen* ilmaistaksesi, hyväksytäänkö vai hylätäänkö testi, jos sen hyväksyttävän laadun taso ei täyty.
    - **Hyväksyttävän laadun taso** – Määritä testitulosten kokonaisprosentti, joka on hyväksyttävä, jotta testi voidaan katsoa hyväksytyksi.

1. Määritä sivun alaosan **Testi**-välilehdessä seuraavat kentät:

    - **Vakio** – Määritä testitulosten odotettu summa (kokonaisluku tai murtoluku). Syötetty arvo syötetään oletusarvon mukaan testituloksiin. Lisäksi se syötetään automaattisesti oletusarvoksi **Minimi**- ja **Maksimi**-kenttiin.
    - **Minimi** – Määritä testitulosten pienin sallittu arvo. Kirjoitettavan arvon on oltava pienempi kuin **Vakio**-kentässä määritetty summa. Kun päivität **Minimi**-kentän, **Vähimmäistoleranssi (%)** -kenttä päivitetään automaattisesti. Samoin kun päivität **Vähimmäistoleranssi (%)** -kentän, **Minimi**-kenttä päivitetään automaattisesti.
    - **Maksimi** – Määritä testitulosten suurin sallittu arvo. Kirjoitettavan arvon on oltava suurempi kuin **Vakio**-kentässä määritetty summa. Kun päivität **Maksimi**-kentän, **Enimmäistoleranssi (%)** -kenttä päivitetään automaattisesti. Samoin kun päivität **Enimmäistoleranssi (%)** -kentän, **Maksimi**-kenttä päivitetään automaattisesti.
    - **Testin mittaväline** – Valitse laite, jota testissä on käytettävä. Jos testille on määritetty mittaväline, se syötetään testiryhmän testille automaattisesti.

1. Sulje sivu.

## <a name="additional-resources"></a>Lisäresurssit

- [Laadunhallinnan testin mittavälineet](quality-management-processes.md)
- [Laadunhallinnan testit](quality-management-processes.md)
- [Laadunhallinnan testimuuttujat](quality-management-processes.md)
- [Laatuliitokset](quality-management-processes.md)
- [Erämääritteet](/supply-chain/production-control/batch-attributes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
