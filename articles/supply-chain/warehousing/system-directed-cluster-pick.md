---
title: Järjestelmäohjattu klusterikeräily
description: Tämä ohjeaihe sisältää järjestelmän ohjaaman klusterin keräilyn yleiskatsauksen Microsoft Dynamics 365 Supply Chain Managementissa.
author: Mirzaab
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 390e0a3379a6482e99a13f4f7835b5264e3747ac
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3217238"
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

Uutta mobiililaitteen valikkokohdetta käytetään järjestelmäohjatun klusterin poimintaan. **Kohdistettava**-vaihtoehdossa on määritettävä klusteriprofiilin tunnus. Lisäksi järjestelmän ohjaama kyselyjärjestys voi ryhmitellä tilauksia yrityskohtaisten kriteerien perusteella. Tämän vuoksi voit edelleen optimoida työtilausten määrityksen määrittämällä mukautetut lajittelukriteerit järjestelmäohjatussa kyselyjärjestyksessä.

Kun järjestelmäohjattu klusterin poiminta on tehty, varastotyöntekijöille esitetään klusteri, jossa keräilytilaukset on ennalta määritetty klusteripositioihin. Tämän vuoksi työntekijät voivat aloittaa kohteen poiminnan useille työtilauksille valitsemalla keräilysijainnissa vain yhden kerran. Järjestelmän ohjaama klusterin keräilyprosessi on sama kuin käyttäjän ohjaama klusterikeräilyprosessi.

## <a name="set-up-system-directed-cluster-picking"></a>Määritä järjestelmäohjattu klusterikeräily

### <a name="create-cluster-profiles"></a>Luo klusteriprofiilit

Klusteriprofiilit ohjaavat sitä, miten järjestelmä luo kunkin klusterin. Jos tarvitaan eri klustereita, kullekin mobiililaitteen valikkonimikkeelle tulisi luoda eri klusteriprofiili.

1. Valitse **Varastonhallinta \> Asetukset \> Mobiililaite \> Klusteriprofiilit**.
2. Valitse **Uusi**.
3. Syötä **Klusteriprofiilin tunnus** -kenttään **2-sijainti**.
4. Kirjoita **Nimi**-kenttään **Sijainti 2**.
5. Valitse **Yleiset**-pikavälilehdellä seuraavat lisäkentät:

    - **Luo klusterin tunnus:** Määritä asetukseksi **Kyllä**. Tämä asetus määrittää, luodaanko klusterin tunnus automaattisesti järjestelmässä vai onko käyttäjä luonut sen keräilyn alussa.
    - **Aktivoi toimet:** Määritä tämän asetuksen arvoksi **Kyllä**. Tämä asetus määrittää, luodaanko toimen nimet automaattisesti toimen nimi -asetusten perusteella. Jos tämän vaihtoehdon arvoksi on asetettu **Ei**, käytetään rekisterikilven tunnusta.
    - **Toimien enimmäismäärä:** Syötä **2**. Tämä kenttä määrittää klusterin toimien enimmäismäärän (eli ruutujen enimmäismäärän, yhteenlaskut, jne.).
    - **Toimen nimi:** Valitse **numeerinen**, jotta sijainnit on nimetty jatkuvien numeroiden avulla. Jos valitset **aakkosjärjestyksessä**, sijainnit on nimetty aakkosjärjestykseen.
    - **Hajota klusteri:** Valitse **Määritä**. Tämä kenttä määrittää, milloin klusteri on rikki.
    - **Lajittelutarkistustyyppi:** Valitse **sijainnin tarkistus**. Tämä kenttä määrittää, onko hyllytyksen vaihe vahvistettu.

6. Voit määrittää lajitteluehdot **klusterin lajittelu** -pikavälilehdessä luomalla uuden rivin ja määrittämällä seuraavat kentät:

    - **Järjestysnumero:** Tämä kenttä määrittää järjestyksen, jonka mukaan järjestelmä lajittelee. Arvo syötetään automaattisesti, mutta voit muuttaa sitä tarpeen mukaan.
    - **Kentän nimi:** Valitse **WMSLocationId**. Tämä kenttä määrittää kentän, jota rivi käyttää lajitteluehdoille.
    - **Lajittelu:** Valitse **nouseva**. Tässä kentässä määritetään, onko lajittelu tehty nousevassa vai laskevassa järjestyksessä.

### <a name="create-a-mobile-device-menu-item"></a>Luo mobiililaitteen valikkovaihtoehto

Jos haluat luoda uuden mobiililaitteen valikkovaihtoehdon järjestelmän ohjaukselle klusterikeräilyyn ja linkittää klusteriprofiilin tunnuksen mobiililaitteen valikkokohteeseen, toimi seuraavasti.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.
2. Valitse **Uusi**.
3. Kirjoita **valikkovaihtoehdon nimi** -kenttään **SD-klusteri**.
4. Kirjoita **otsikko**-kenttään **SD-klusteri**.
5. Valitse **Tila**-kentässä **Työ**.
6. Valitse **Käytä nykyistä työtä** -asetukseksi **Kyllä**.
7. Valitse **Yleiset**-pikavälilehdellä seuraavat lisäkentät:

    - **Ohjaaja-kentässä:** Valitse **Järjestelmäohjattu**.
    - **Luo rekisterikilpi:** Määritä asetukseksi **Kyllä**.
    - **Klusteriprofiilin tunnus:** Valitse **2-sijainti**.

8. Määritä **työluokat**-pikavälilehdessä tämän mobiililaitteen valikkovaihtoehdon kelvollinen työluokka määrittämällä seuraavat kentät:

    - **Työluokan tunnus:** Varmista, että **myynti** on syötetty.
    - **Työtilauksen tyyppi:** Varmista, että **myyntitilaus** on syötetty.

9. Määritä uusi järjestelmäohjattu työjärjestyskysely noudattamalla seuraavia ohjeita:

    1. Valitse **Uusi**.
    2. Syötä **Järjestysnumero**-kenttään arvo **1**.
    3. Valitse **kuvaus**-kentässä **työprioriteetti – työn tunnus**.

10. Valitse valikosta **Muokkaa kyselyä**.
11. Aseta **Lajittelu**-välilehdellä seuraavat kentät:

    - **Taulu:** Valitse **Työ**.
    - **Johdettu taulu:** Valitse **Työ**.
    - **Kenttä:** Valitse **työn prioriteetti**.
    - **Hakusuunta:** Valitse **Laskeva**.
    - **Taulu:** Valitse **Työ**.
    - **Johdettu taulu:** Valitse **Työ**.
    - **Kenttä:** Valitse **työn tunnus**.
    - **Hakusuunta:** Valitse **Laskeva**.

Järjestelmä lajittelee nyt työtunnukset klusterissa, ensin työn prioriteetin ja sitten työtunnuksen mukaan.

### <a name="set-up-a-mobile-device-menu"></a>Määritä varaston mobiililaitteen valikko

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikko**.
2. Lisää juuri luomasi valikkokohde haluamaasi valikkoon.

## <a name="example"></a>Esimerkki

### <a name="create-picking-work"></a>Luo keräystyö

Ennen kuin voit määrittää järjestelmäohjatun klusterikeräilyn, sinun on luotava joitakin tukikelpoisia lähteviä töitä. Aiemmin luomasi klusteriprofiili määrittää kaksi klusteripositiota. Siksi sinun on luotava vähintään kaksi työtunnusta.

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
2. Luo uusi myyntitilaus valitsemalla **Uusi**.
3. Valitse **Asiakastili**-kentässä mikä tahansa asiakas.
4. Valitse **Yleinen**-pikavälilehden **Varasto**-kentässä varasto **62**.
5. Valitse **OK**.
6. Valitse **Myyntitilausrivit**-pikavälilehdessä **Lisää rivi**.
7. Valitse **Nimikkeen numero** -kentässä **A0001**.
8. Kirjoita **Määrä**-kenttään **1**.
9. Lisää toinen rivi valitsemalla **Lisää rivi**.
10. Valitse **Nimikkeen numero** -kentässä **A0002**.
11. Kirjoita **Määrä**-kenttään **3**.
12. Toista vaiheet 2 – 6.
13. Valitse **Nimikkeen numero** -kentässä **A0001**.
14. Kirjoita **Määrä**-kenttään **4**.
15. Lisää toinen rivi valitsemalla **Lisää rivi**.
16. Valitse **Nimikkeen numero** -kentässä **A0002**.
17. Kirjoita **Määrä**-kenttään **2**.

Varaa varasto ja vapauta se varastoon. Luodaan kaksi erilaista työtunnusta. Jokaisella työtunnuksella on kaksi poimintariviä.

### <a name="run-the-mobile-device-flow"></a>Suorita mobiililaitteen virtaus

1. Valitse mobiililaitteessa valikko, joka sisältää uuden mobiililaitteen valikkovaihtoehdon.
2. Valitse **SD-klusteri**-valikkokohde ja aloita poiminta. Klusteri luodaan, ja siihen on liitetty kaksi aiemmin luomaasi työtunnusta. Jos olet luonut useamman kuin kaksi työtunnusta, vain kaksi ensimmäistä lisätään klusteriin. Huomaa, että työtunnukset lisätään klusteriin nousevassa järjestyksessä, kuten kyselyasetuksissa on määritetty.

    > [!NOTE]
    > Uusi klusteri luodaan automaattisesti vain, jos aiemmin on luotu riittävästi ylimääräisiä työtunnuksia. Muussa tapauksessa näyttöön tulee seuraava sanoma: "Klusterille ei löydy tarpeeksi työtä."

    Kun olet valinnut valikon, ensimmäinen poimintanäyttö tulee näkyviin. Järjestelmä kokoaa kaikki vastaavat poimintarivit kahdesta työtunnuksesta ja ohjaa sinut käymään keräilysijainnissa kerran, jotta voit tyydyttää molemmat tilaukset yhdellä poiminnalla. Tämä prosessi tehdään samalla tavalla kuin käyttäjän ohjaama klusterin poimintaprosessi.

3. Vahvista ensimmäinen poiminta. Kirjoita sitten toimen nimi varmistaaksesi, että nimikkeet on asetettu oikeaan asentoon.
4. Toista tämä prosessi, kunnes kaikki nimikkeet on kerätty ja asetettu oikeaan asentoon.
5. Viimeinen vaihe mobiililaitteessa on sijoittaa klusterin lopulliseen sijaintiin. Kun tämä sijoitustoiminto on vahvistettu, klusteri suljetaan ja hajotetaan sen mukaan, mikä arvo on klusteriprofiilin **Hajota klusteri** -kentässä. Myös työtunnukset suljetaan.
6. Mobiililaitteessa näkyy Klusteri valmis -sanoma.
