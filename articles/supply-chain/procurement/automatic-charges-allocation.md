---
title: Kulujen automaattinen kohdistaminen
description: Microsoft Dynamics 365 Supply Chain Managementin kulutoiminnolla voi automaattisesti kohdistaa kuluja osto- tai myyntitilauksiin.
author: dasani-madipalli
manager: tfehr
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-10-01
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: eddcf275c14565dfe77fbe7efa676be4a34da686
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244156"
---
# <a name="automatic-allocation-of-charges"></a>Kulujen automaattinen kohdistaminen

[!include [banner](../includes/banner.md)]

Asiakkaan tai myytävän nimikkeen perusteella halutaan ehkä käyttää tiettyjä lisämaksuja. Microsoft Dynamics 365 Supply Chain Managementin *kulutoiminnolla* voi automaattisesti kohdistaa kuluja osto- tai myyntitilauksiin.

Automaattisia kuluja käytetään automaattisesti, kun luot myynti- tai ostotilauksen. Voit määrittää automaattiset kulut tietyille toimittajille, asiakkaille, toimittajien ryhmille tai nimikkeille. Voit määrittää automaattisesti kuluja, joita käytetään kaikille toimittajille, asiakkaille tai nimikkeille.

## <a name="set-up-charges-codes"></a>Kulujen koodien määrittäminen

Kulujen kohdistamista varten on ensin määritettävä kulujen koodit.

1. Noudata seuraavia ohjeita:

    - Ostotilaukset: valitse **Ostoreskontra \> Kulujen määritys \> Kulujen koodit**.
    - Myyntitilaukset: valitse **Myyntireskontra \> Kulujen määritys \> Kulujen koodit**.

1. Luo kulujen koodi valitsemalla toimintoruudussa **Uusi**.
1. Määritä uuden tietueen ylätunnisteessa seuraavat kentät:

    - **Kulujen koodi** – anna kulujen koodi.
    - **Kuvaus** – anna kulujen kuvaus.
    - **Nimikkeen arvonlisäveroryhmä** – valitse tarvittaessa nimikkeen arvonlisäveroryhmä.
    - **Jaa suhteellisesti** – Määritä asetukseksi *Kyllä*, jos haluat jakaa kulut suhteellisesti. Tämä vaihtoehto on käytettävissä vain myyntitilauksissa.
    - **Enimmäissumma** – Anna suurin kulujen koodille sallittu summa. Tämän kentän avulla vahvistetaan toimittajan laskujen kulut. Se on käytettävissä vain ostotilauksissa.

        > [!NOTE]
        > Ostotilausten kulujen vahvistamistoiminto otetaan käyttöön valitsemalla **Ostoreskontra \> Määritykset \> Ostoreskontran parametrit**. Määritä **Laskun oikeellisuustarkistus** -pikavälilehden **Laskun oikeellisuustarkistus** -osan **Ota käyttöön laskujen täsmäytyksen vahvistus** -vaihtoehdoksi *Kyllä*.

1. **Kirjaus**-pikavälilehdessä on **Debet**- ja **Kredit**-osat. Määritä seuraavat kentät sen perusteella, mihin kirjanpitoon kulut halutaan kirjata:

    - **Tyyppi** – valitse sen tilin tyyppi, johon kirjaus tehdään (*Kirjanpito*, *Asiakas* tai *Nimike*).
    - **Kirjaus** – valitse luotavan kirjauksen tyyppi (kuten *Välittäjän maksu* tai *Asiakastilitys*).
    - **Tili** – valitse tili, johon kulu kirjataan.

1. Valitse toimintoruudussa **Tallenna**.

## <a name="create-charge-groups"></a>Kuluryhmien luominen

Kuluryhmät kohdistavat tietyt kulut automaattisesti asiakas- tai toimittajaryhmään. Seuraavissa alaosissa käsitellään näiden kuluryhmien luomista ja määrittämistä.

### <a name="charge-groups-for-purchase-orders"></a>Ostotilausten kuluryhmät

Ostotilausten kuluryhmiä luodaan seuraavasti:

1. Valitse **Ostoreskontra \> Kulujen määritys \> Toimittajan kuluryhmä**.
1. Lisää rivi ruudukkoon valitsemalla toimintoruudussa **Uusi** ja määritä sitten seuraavat kentät:

    - **Kuluryhmä** – anna kuluryhmän nimi.
    - **Kuvaus** – anna kuluryhmän kuvaus.

1. Valitse toimintoruudussa **Tallenna**.
1. Valitse **Ostoreskontra \> Toimittajat \> Kaikki toimittajat** ja avaa joko aiemmin luotu toimittaja tai luo uusi toimittaja.
1. Valitse **Oletusostotilaukset**-pikavälilehden **Ostotilaukset**-osan **Kuluryhmä**-kenttään juuri luotu kuluryhmä.

### <a name="charge-groups-for-sales-orders"></a>Myyntitilausten kuluryhmät

Myyntitilausten kuluryhmiä luodaan seuraavasti:

1. Valitse **Myyntireskontra \> Kulujen määritys \> Asiakkaan kuluryhmät**.
1. Lisää rivi ruudukkoon valitsemalla toimintoruudussa **Uusi** ja määritä sitten seuraavat kentät:

    - **Kuluryhmä** – anna kuluryhmän nimi.
    - **Kuvaus** – anna kuluryhmän kuvaus.

1. Valitse toimintoruudussa **Tallenna**.
1. Valitse **Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat** ja avaa joko aiemmin luotu asiakas tai luo uusi asiakas.
1. Valitse **Oletusostotilaukset**-pikavälilehden **Myyntitilaus**-osan **Kuluryhmä**-kenttään juuri luotu kuluryhmä.

## <a name="define-auto-charges"></a>Automaattisten kulujen määrittäminen

Kun kulujen koodit on määritetty, määritä automaattiset kulut seuraavien ohjeiden mukaisesti.

1. Noudata seuraavia ohjeita:

    - Ostotilaukset: Valitse **Hankinta \> Määritys \> Kulut \> Automaattiset kulut**.
    - Myyntitilaukset: valitse **Myyntireskontra** \> Määritys \> Kulujen määritys \> Automaattiset kulut.

1. Valitse luetteloruudun **Taso**-kentässä taso, jossa automaattista kulua käytetään:

    - *Pää* – lisää kulut tilauksen otsikkoon.
    - *Rivi* – lisää kuluja tilausriveille.

1. Valitse aiemmin luotu automaattinen kulu muokattavaksi tai määritä uusi automaattinen kulu valitsemalla **Uusi**.
1. Määritä tilialue, joita asetus koskee, valitsemalla **Tilikoodi**-luettelossa jokin seuraavista arvoista.

    - *Taulu* – määritä kulut tietylle asiakkaalle tai toimittajalle.
    - *Ryhmä* – määritä kulut muiden kulujen ryhmään.
    - *Kaikki* – määritä kulut kaikille asiakkaille tai toimittajille.

1. Valitse tietty asiakas tai toimittaja **Asiakassuhde**- tai **Toimittajasuhde**-kentässä, jos **Tilikoodi**-kentässä määritetään asetukseksi *Taulu*. Jos **Tilikoodi**-kentän asetukseksi määritetään *Ryhmä*, valitse asiakkaan tai toimittajan kuluryhmä.
1. Määritä nimikkeet, joita asetus koskee, valitsemalla **Nimikekoodi**-kentässä jokin seuraavista arvoista. Voit valita nimikekoodin vain, jos automaattiset kulut määritetään rivitasolla.

    - *Taulu* – määritä kulut tietylle nimikkeelle.
    - *Ryhmä* – määritä kulut nimikkeen kuluryhmään.
    - *Kaikki* – määritä kulut kaikille nimikkeille.

1. Valitse **Nimikesuhde**-kentässä tietty nimike, jos määrität **Nimikekoodi**-kentässä asetukseksi *Taulu*. Jos määrität **Nimikekoodi**-kentän asetukseksi *Ryhmä*, valitse nimikkeen kuluryhmä.
1. **Vain myyntitilaukset:** määritä toimitustavat, joita asetus koskee, valitsemalla **Toimitustapakoodi**-kentässä jokin seuraavista arvoista:

    - *Taulu* – määritä kulut tietylle toimitustavalle.
    - *Ryhmä* – määritä kulut tietylle toimitustaparyhmälle.
    - *Kaikki* – määritä kulut kaikille toimitustavoille.

1. **Vain myyntitilaukset:** Vallitse **Toimitustapasuhde**-kentässä tietty toimitustapa, jos **Toimitustapakoodi**-kentässä määritettiin asetukseksi *Taulu*. Jos määritit **Toimitustapakoodi**-kentän asetukseksi *Ryhmä*, valitse toimitustaparyhmä.
1. Määritä **Rivit**-pikavälilehdessä kulut ja kulujen prosentit, joita käytetään nykyistä automaattista kulua käytettäessä. Voit lisätä tarvittavan määrän rivejä käyttämällä tämän pikavälilehden työkaluriviä. Määritä kullekin riville seuraavat kentät:

    - **Valuutta** – valitse kulujen laskemiseen käytettävä valuutta.
    - **Kulujen koodi** – valitse kulun koodi.
    - **Luokka** – valitse jokin seuraavista arvoista:

        - *Kiinteä* – Kulu kirjataan kiinteänä määränä riville. Sekä tilauksen otsikon että tilausrivien kuluissa voidaan käyttää kiinteitä kuluja.
        - *Kpl* – Kulu perustuu yksikköön. Näitä kuluja voidaan käyttää vain tilausriveillä. Ne tulevat näkyviin, kun tilauksen kokonaissumma lasketaan.
        - *Prosentti* – Kulu kirjataan prosenttiosuutena riville. Sekä tilauksen otsikon että tilausrivien kuluissa voidaan käyttää prosenttimuotoisia kuluja.
        - *Konsernin sisäinen prosentti* – Kulu kirjataan prosenttia konsernin sisäisten tilausten riville. Konsernin sisäisiä prosenttikuluja voidaan käyttää vain tilausriveillä.
        - *Ulkoinen* – kulu lasketaan vähintään yhteen rahdinkuljettajaan liitetyn kolmannen osapuolen palvelun mukaan.

    - **Kulujen arvo** – anna kulun arvo valitun luokan perusteella.
    - **Kulujen valuuttakoodi** – Määritä kulun valuutta, jos haluat käyttää jotain muuta kuin **Valuutta**-kentässä määritettyä valuuttaa. Voit käyttää eri valuttaa vain, jos valitun kulujen koodin **Debet-tyyppi**- tai **Kredit-tyyppi**-kentän asetuksena on *Kirjanpitotili* tai *Nimike*.
    - **Summasta** – Määritä aloitussumma, johon automaattinen kulu kohdistetaan. Tässä yhteydessä summa viittaa tilauksen kokonaissummaan.
    - **Summaan** – Määritä lopetussumma, johon automaattinen kulu kohdistetaan. Tässä yhteydessä summa viittaa tilauksen kokonaissummaan.
    - **Arvonlisäveroryhmä** – määritä arvolisäveroryhmä.
    - **Toimipaikka** ja **Varasto** – määritä toimipaikka ja varasto, jos kulut kohdistetaan vain tiettyyn toimipaikkaan ja varastoon.
    - **Säilytä** – valitse tämä valintaruutu, jos haluat säilyttää kulutapahtumat laskutuksen valmistumisen jälkeen siten, että kulua käytetään aina, kun luot uuden laskun valitulle asiakastilille.

1. **Vain myyntitilaukset:** jos haluat laskea kulut tasoittain, lisätietoja on kohdassa [Myyntitilausten tasoittaiset kulut](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/about-tiered-charges-on-sales-orders).

## <a name="allocate-charges-from-the-header-to-a-line"></a>Kulujen kohdistaminen otsikosta riville

Seuraava menettely näyttää, miten otsikkotason kulut kohdistetaan riville. Ennen tämän menettelyn aloittamista sinulla on oltava *kiinteä summa* -tyyppinen otsikkotason kulu ja tilaus, johon kulu kohdistetaan. Lisäksi tilauksessa on oltava ainakin yksi rivinimike.

1. Avaa ostotilaus tai kulutilaus.
1. Toimi toimintoruudussa jollakin seuraavista tavoista:

    - Ostotilaukset: valitse **Ostot**-välilehden **Kulut**-ryhmässä **Kohdista kulut**.
    - Myyntitilaukset: valitse **Myynti**-välilehden **Kulut**-ryhmässä **Kohdista kulut**.

1. Määritä **Kohdista kulut tilausriveille** -valintaikkunassa seuraavat kentät:

    - **Kulujen kohdistus** – määritä kulujen kohdistaminen valitsemalla jokin seuraavista kentistä:

        - *Nettosumma* – kohdista kulut sen mukaan, mikä on kunkin rivisumman suhde kokonaisnettosummaan.
        - *Määrä* – kohdista kulut sen mukaan, mikä kunkin rivin yksiköiden määrä suhteessa yksiköiden kokonaismäärään.
        - *Riveittäin* – kohdista kulut tasan rivien kokonaismäärään.

    - **Kohdista kulut riveille** – valitse arvot määrittämään, onko kulut kohdistettava kaikille riveille, vain positiivisille riveillä vai vain negatiivisille riveille.
    - **Kohdista kaikki** – valitse tämä valintaruutu, jos haluat kohdistaa kulut ostotilauksen riveille myös silloin, kulujen koodin debet-tyyppi on muu kuin *Nimike*.
    - **Vastaanotettu** – valitse tämä valintaruutu, jos haluat kohdistaa kulut vain vastaanotetuille tilausriveille.
    - **Varastoitava** – valitse tämä valintaruutu, jos haluat kohdistaa kulut vain varastoiduille tilausriveille.
    - **Näytä valinnat ja tyhjennä määritetyt rivit** – Valitse tämä valintaruutu, jos haluat jättää tiettyjä rivejä pois tästä kohdistuksesta. Jos valitset tämän valintaruudun, **Valitse rivit, joita ei sisällytetä kohdistukseen** -ruudukko avautuu. Tässä ruudukossa on vain **Kohdista kulut riveille**- ja **Varastoitava**-kenttien määrittäviä ehtoja vastaavat rivit. Jos esimerkiksi määrität **Kohdista kulut riveille** -kentän asetukseksi *Positiiviset rivit* ja valitset **Varastoitava**-valintaruudun, ruudukossa näytetään vain rivit, jotka ovat sekä positiivisia että varastoitavia. Lisäksi ruudukko suodattaa automaattisesti pois kaikki rivit, joiden koko määrä on jo vastaanotettu. Poista avatussa ruudukossa **Sisällytä**-valintaruudun valinta niiltä riveiltä, joita ei sisällytetä kohdistukseen. 

        > [!IMPORTANT]
        > Varmista **Valitse rivit, joita ei sisällytetä kohdistukseen** -ruudukkoa käytettäessä, että ruudukko on avoinna siihen saakka, että valitset **Kohdista**. Jos suljet ruudukon ennen **Kohdista**-vaihtoehdon valintaa, ruudukossa tehdyt asetukset menetetään. Siinä tapauksessa kulut kohdistetaan aiemmin määritettyjen ehtojen perusteella.

1. Ota asetukset käyttöön valitsemalla **Kohdista** ja sulje kyselyn valintaikkuna.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]