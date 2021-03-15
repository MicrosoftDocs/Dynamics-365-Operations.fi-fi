---
title: Järjestelmäohjattu klusterikeräily
description: Tämä ohjeaihe sisältää järjestelmän ohjaaman klusterin keräilyn yleiskatsauksen Microsoft Dynamics 365 Supply Chain Managementissa.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkCluster, WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: fa737f61bfd5bd71ba6d76e75e57c8e2d682cda3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965674"
---
# <a name="system-directed-cluster-picking"></a>Järjestelmäohjattu klusterikeräily

[!include [banner](../includes/banner.md)]

Klusterin poiminta on poimintaprosessi, jonka avulla voit poimia nimikkeitä useille tilauksille samanaikaisesti klusteroimalla ne poimintaklustereihin. Sinun tarvitsee vierailla poimintasijainnissa vain kerran. Yleensä tätä toimintoa käytetään pienten tilausten keräilyn tai sellaisten määrien kanssa, jotka ovat pienempiä kuin tapausmäärät.

Kun järjestelmän ohjaama klusterin poiminta on määritetty, voit klusteroimalla valita työn otsikot järjestelmän luoman klusterin perusteella. Järjestelmäklusteri poimii tilaukset jopa niiden toimien määrään, jotka on määritetty klusteriprofiilissa. Siksi voit valita useita tilauksia samanaikaisesti ilman, että klusteria on luotava manuaalisesti.

Järjestelmäohjattu klusteripoiminta tarjoaa vaihtoehdon manuaaliseen klusterirakennukseen, jossa klusterin luomiseen käytetään klusteriprofiilia. Klusteriprofiilissa on määritettävä useita asennukseen liittyviä rivejä, ennen kuin niitä käytetään:

- **Toimien määrä** vastaa klusteriin asetettavien tilausten määrää. Siksi se vastaa yhteenlaskujen määrää.
- **Hajota klusteri** määrittää, milloin klusteri on rikki.
- **Luo klusterin tunnus** määrittää, luodaanko klusterin tunnus järjestelmässä vai tuleeko käyttäjän syöttää se.
- **Lajittelu tarkistustyyppi** määrittää, tarvitaanko toimen vahvistusta.

Uutta mobiililaitteen valikkokohdetta käytetään järjestelmäohjatun klusterin poimintaan. Valitussa **Kohdistettava**-vaihtoehdossa on määritettävä **Klusteriprofiilin tunnus**. Lisäksi järjestelmän ohjaamat työjärjestyskyselyt voivat ryhmitellä tilauksia yrityskohtaisten kriteerien perusteella. Tämän vuoksi voit edelleen optimoida työtilausten määrityksen määrittämällä mukautetut lajittelukriteerit, jotka käyttävät järjestelmäohjattua työjärjestyskyselyä.

Kun järjestelmäohjattu klusterin poiminta on otettu käyttöön, varastotyöntekijöille esitetään klusteri, jossa keräilytilaukset on ennalta määritetty klusteripositioihin. Tämän vuoksi työntekijät voivat aloittaa kohteen poiminnan useille työtilauksille valitsemalla keräilysijainnissa vain yhden kerran. Järjestelmän ohjaama klusterin keräilyprosessi on sama kuin käyttäjän ohjaama klusterikeräilyprosessi.

## <a name="enable-the-system-directed-cluster-picking-feature"></a>Järjestelmäohjautuvan klusterin keräilyn ottaminen käyttöön

Ennen kuin käytät tätä toimintoa, se on otettava käyttöön järjestelmässä. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sivua ja tarkistaa toiminnon tilan sekä ottaa sen käyttöön tarvittaessa. Toiminto näkyy seuraavasti:

- **Moduuli** - Varastonhallinta
- **Ominaisuuden nimi** - Järjestelmäohjautuva klusterin keräily

Tämä ominaisuus edellyttää myös riippuvaisen ominaisuuden käyttöönottoa. Riippuvainen ominaisuus on:

- **Moduuli** - Varastonhallinta
- **Toiminnon nimi** - Organisaation laajuinen järjestelmäsuunnattu työn sekvensointi

## <a name="set-up-system-directed-cluster-picking"></a>Määritä järjestelmäohjattu klusterikeräily

### <a name="create-cluster-profiles"></a>Luo klusteriprofiilit

Klusteriprofiilit ohjaavat sitä, miten järjestelmä luo kunkin klusterin. Jos tarvitaan eri klustereita, kullekin mobiililaitteen valikkonimikkeelle tulisi luoda eri klusteriprofiili.

1. Valitse **Varastonhallinta \> Asetukset \> Mobiililaite \> Klusteriprofiilit**.
2. Valitse **Uusi**.
3. Syötä **Klusteriprofiilin tunnus** -kenttään **2-sijainti**.
4. Kirjoita **Nimi**-kenttään **Sijainti 2**.
5. Kirjoita **Yleinen**-pikavälilehdelle seuraavat tiedot:

    - **Luo klusteritunnus** - Valitse **Kyllä**. Tämä asetus määrittää, luodaanko klusterin tunnus automaattisesti järjestelmässä vai onko käyttäjä luonut sen keräilyn alussa. 
    - **Aktivoi toimet** - Valitse **Kyllä**. Tämä asetus määrittää, luodaanko toimen nimet automaattisesti toimen nimi -asetusten perusteella. Jos tämän vaihtoehdon arvoksi on asetettu **Ei**, käytetään rekisterikilven tunnusta.
    - **Toimien enimmäismäärä** - Valitse **2**. Tämä kenttä määrittää klusterin toimien enimmäismäärän (eli ruutujen enimmäismäärän, yhteenlaskut, jne.).
    - **Toimen nimi** - Valitse **numeerinen**, jotta sijainnit on nimetty jatkuvien numeroiden avulla. Jos valitset **aakkosjärjestyksessä**, sijainnit on nimetty aakkosjärjestykseen.
    - **Hajota klusteri** - Valitse **Määritä**. Tämä kenttä määrittää, milloin klusteri on rikki. 
    - **Lajittelutarkistustyyppi** - Valitse **sijainnin tarkistus**. Tämä kenttä määrittää, onko hyllytyksen vaihe vahvistettu.
        
6. Voit määrittää lajitteluehdot **klusterin lajittelu** -pikavälilehdessä luomalla uuden rivin ja syöttämällä seuraavat tiedot:

    - **Numerosarja** - Valitse **1**. Tämä kenttä määrittää järjestyksen, jonka mukaan järjestelmä lajittelee. Arvo syötetään automaattisesti, mutta voit muuttaa jos on tarpeen.
    - **Kentän nimi** - Syötä **WMSLocationId**. Tämä kenttä määrittää kentän, jota rivi käyttää lajitteluehdoille.
    - **Lajittelu** - Valitse **nouseva**. Tässä kentässä määritetään, onko lajittelu tehty nousevassa vai laskevassa järjestyksessä.

### <a name="create-a-mobile-device-menu-item"></a>Luo mobiililaitteen valikkovaihtoehto

Jos haluat luoda uuden mobiililaitteen valikkovaihtoehdon järjestelmän ohjaukselle klusterikeräilyyn ja linkittää klusteriprofiilin tunnuksen mobiililaitteen valikkokohteeseen, toimi seuraavasti.

1. Valitse **Varastonhallinta > Asetukset > Mobiililaite > Mobiililaitteen valikkovaihtoehdot**.
1. Valitse **Uusi**.
1. Määritä seuraavat tiedot -otsikko-osiossa:
    - **Valikkokohteen nimi** - SD-klusteri
    - **Otsikko** - SD-klusteri
    - **Tila** - Työ
    - **Käytä aiemmin luotua työtä** - Kyllä

1. Kirjoita **Yleinen**-pikavälilehdelle seuraavat tiedot:
    - **Ohjattu** - Järjestelmäohjattu klusterikeräily
    - **Luo rekisterikilpi** - Kyllä
    - **Klusteriprofiilin tunnus** - 2-sijainti.

1. Määritä **työluokat**-pikavälilehdessä tämän mobiililaitteen valikkovaihtoehdon kelvollinen työluokka määrittämällä seuraavat kentät:
    - **Työluokan tunnus** - Myynti
    - **Työtilauksen tyyppi** - myyntitilaukset

1. Valitse **matkaviestimen valikkovaihtoehdot** -toimintoruudusta **järjestelmän ohjaamat työsarjakyselyt** ja määritä uusi järjestelmäohjattu työsarjakysely noudattamalla seuraavia ohjeita:
    - Valitse toimintoruudussa **Uusi**.
    - **Järjestysnumero** - 1
    - **Kuvaus** - Työn prioriteetti – työtunnus

1. Valitse toimintoruudussa **Muokkaa kyselyä**
1. Valitse **Lajittelu**-välilehti
1. Lisää uusi rivi valitsemalla **Lisää** ja syötä sitten seuraavat:
    - **Taulu** - työ
    - **Johdettu taulu** - Työ
    - **Kenttä** - Työn prioriteetti
    - **Hakusuunta** - Laskeva
1. Lisää toinen rivi valitsemalla **Lisää** ja syötä sitten seuraavat:
    - **Taulu** - työ
    - **Johdettu taulu** - Työ
    - **Kenttä** - Työn tunnus
    - **Hakusuunta** - Laskeva

1. Järjestelmä lajittelee nyt työtunnukset klusterissa, ensin työn prioriteetin ja sitten työtunnuksen mukaan.

### <a name="set-up-a-mobile-device-menu"></a>Määritä varaston mobiililaitteen valikko

1. Valitse **Varastonhallinta > Asetukset > Mobiililaite > Mobiililaitteen valikko**.
1. Lisää **SD-klusteri**-valikkovaihtoehto, jonka juuri loit mobiililaitteen valikkoon.
1. Valitse **Lähtevä**-valikko.
1. Valitse toimintoruudussa **Muokkaa**.
1. Vieritä, kunnes löydät **SD-klusterin**.
1. Valitse **SD-klusteri**, **valikkorakenne** -luetteloon osoittava nuoli otetaan käyttöön.
1. Siirrä **SD-klusterin** valikkokohde **Lähtevän** valikon rakenteeseen valitsemalla **nuoli**-painike.
1. Valitse **Valikkorakenne**-luettelosta **SD-klusteri** ja siirrä valikkokohde haluamaasi kohtaan mobiililaitteen valikossa valitsemalla **ylös** tai **alas** osoittavia nuolia.

## <a name="scenario"></a>Skenaario

### <a name="create-picking-work"></a>Luo keräystyö

Ennen kuin voit määrittää järjestelmäohjatun klusterikeräilyn, sinun on luotava tukikelpoisia lähteviä töitä. Aiemmin luomasi klusteriprofiili määrittää kaksi klusteripositiota. Siksi sinun on luotava vähintään kaksi työtunnusta. Tässä skenaariossa voit luoda kaksi myyntitilausta, varata varaston, vapauttaa myyntitilaukset varastoon ja käsitellä sitten aallon manuaalisesti.

1. Siirry kohtaan **Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset**.
1. Valitse **Uusi** toimintoruudussa, luodaksesi ensimmäisen myyntitilauksen.
    - **Luo myyntitilaus** -valikko avautuu, lisää seuraavat tiedot:
        - Määritä **asiakas**-pikavälilehdessä **Asiakastili** - **US-004**.
        - Kirjoita **Yleinen**-pikavälilehdelle **Varasto** - **62**.
        - Valitse **OK** sulkeaksesi valikon ja luodaksesi myyntitilauksen.
    - **Valitse myyntitilausrivit** -pikavälilehdessä **Lisää rivi**, jos uutta riviä ei lisätä automaattisesti, ja kirjoita seuraavat kohdat:
        - **Nimiketunnus** - A0001
        - **Määrä** - 1
        - Lisää toinen rivi valitsemalla **Lisää rivi**.
        - **Nimiketunnus** - A0002
        - **Määrä** - 3
    - Varaa varasto molempia juuri luomiasi rivejä varten.
        - Valitse **Rivi 1**.
        - Valitse **myyntitilauksen rivien** toimintaruudusta **Varasto** ja valitse sitten luettelosta **Varaus**.
        - Valitse **Varaus**-lomakkeessa **Varaa erä** voidaksesi tehdä varauksia varastosta.
        - Kun **Varaus** on tehty, suljetaan varauslomake.
        - Toista nämä vaiheet, kun varaat **rivin 2** varaston.
1. Valitse **Uusi** toimintoruudussa, luodaksesi toisen myyntitilauksen
    - **Luo myyntitilaus** -valikko avautuu, lisää seuraavat tiedot:
        - Määritä **asiakas**-pikavälilehdessä **Asiakastili** - **US-005**.
        - Kirjoita **Yleinen**-pikavälilehdelle **Varasto** - **62**.
        - Valitse **OK** sulkeaksesi valikon ja luodaksesi myyntitilauksen
    - **Valitse myyntitilausrivit** -pikavälilehdessä **Lisää rivi**, jos uutta riviä ei lisätä automaattisesti, ja kirjoita seuraavat tiedot:
        - **Nimiketunnus** - A0001
        - **Määrä** - 4
        - Lisää toinen rivi valitsemalla **Lisää rivi**.
        - **Nimiketunnus** - A0002
        - **Määrä** - 2
    - Varaa varasto molempia juuri luomiasi rivejä varten.
        - Valitse **Rivi 1**.
        - Valitse **myyntitilauksen rivien** toimintaruudusta **Varasto** ja valitse sitten luettelosta **Varaus**.
        - Valitse **Varaus**-lomakkeessa **Varaa erä** voidaksesi tehdä varauksia varastosta.
        - Kun **Varaus** on tehty, suljetaan varauslomake.
        - Toista nämä vaiheet, kun varaat **rivin 2** varaston.
    - Sulje myyntitilaus ja palaa **Kaikki myyntitilaukset** -luettelosivulle.
1. Etsi juuri luomasi kaksi myyntitilausta (sivu on ehkä päivitettävä). Valitse taulusta molemmat myyntitilaukset käyttämällä osan valintamerkkiä.
    - Valitse **Kaikki myyntitilaukset** -toimintoruudusta **Varasto**-välilehti.
    - Vapauta molemmat myyntitilaukset varastoon valitsemalla **toimenpiteet**-ryhmästä **vapauta varastoon**.
1. Kun vapautus varastoon -prosessi on päättynyt, näkyviin tulee tiedottava sanoma.
    - Kullekin myyntitilaukselle luodaan lähetykset.
    - Aalto luodaan ja molemmat lähetykset liitetään aaltokohteeseen. Kirjoita **aallon tunnus** muistiin.
1. Valitse **Varastonhallinta > Lähtevät aallot > Lähetysaallot > Kaikki aallot**.
    - Valitse **Kaikki aallot** -luettelosta edellisessä vaiheessa luomasi **aallon tunnus**.
    - Valitse Toimintoruudun **Aalto**-välilehdellä,
    - Valitse **Aalto**-ryhmästä **prosessi**, jossa käsitellään ja luodaan **Työ**.
    - Tiedottavat sanomat luodaan, kun käsittely on suoritettu, mikä ilmaisee, että työ on luotu ja aalto kirjattu.
1. **Valinnainen**: voit tarkastella luotua työtä valitsemalla **varaston hallinta > työ > työn tiedot**. Luodaan kaksi erilaista työtunnusta. Jokaisella työtunnuksella on kaksi poimintariviä.

### <a name="run-the-mobile-device-flow"></a>Suorita mobiililaitteen virtaus

1. Kirjaudu kannettavaan laitteeseen käyttäjälle varastossa **62**.
1. Valitse **päävalikosta** **Lähtevä**.
1. Valitse **Lähtevä**-valikossa **SD-klusteri**-valikkokohde aloittaaksesi poiminnan.
    - Klusteri luodaan, ja siihen on liitetty kaksi aiemmin luomaasi työtunnusta. Jos olet luonut useamman kuin kaksi työtunnusta, vain kaksi ensimmäistä lisätään klusteriin. Huomaa, että työtunnukset lisätään klusteriin nousevassa järjestyksessä, kuten kyselyasetuksissa on määritetty.

    > [!NOTE]
    > Uusi klusteri luodaan automaattisesti vain, jos aiemmin on luotu riittävästi ylimääräisiä työtunnuksia. Muussa tapauksessa näyttöön tulee seuraava sanoma: "Klusterille ei löydy tarpeeksi työtä."

    - Kun olet valinnut valikon, ensimmäinen poimintanäyttö tulee näkyviin. Järjestelmä kokoaa kaikki vastaavat poimintarivit kahdesta työtunnuksesta ja ohjaa sinut käymään keräilysijainnissa kerran, jotta voit tyydyttää molemmat tilaukset yhdellä poiminnalla. Tämä prosessi tehdään samalla tavalla kuin käyttäjän ohjaama klusterin poimintaprosessi.

1. Vahvista ensimmäinen keräyksen sijainti ja nimike valitsemalla **OK**.
    - Poiminnan määrä on sen nimikkeen kokonaissumma, joka näkyy klusterin myyntitilauksissa.
1. Kirjoita toimen nimi (numeerinen tai aakkosellinen) vahvistaaksesi, että toimeen kerätty nimikkeen määrä on otettu oikeaan kohtaan.
1. Toista tämä prosessi, kunnes kaikki nimikemäärät on kerätty ja asetettu oikeaan asentoon.
1. Viimeinen vaihe mobiililaitteessa on **sijoittaa** klusteri lopulliseen sijaintiin. Valitse **OK**
    - Kun sijoitustoiminto on vahvistettu, klusteri suljetaan ja hajotetaan sen mukaan, mikä arvo on klusteriprofiilin **Hajota klusteri** -kentässä. Myös työtunnukset suljetaan.
1. Mobiililaitteessa näkyy Klusteri valmis -sanoma.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]