---
title: Ajoita työtilauksia
description: Tässä ohjeaiheessa selitetään, miten työtilaukset ajoitetaan käyttöomaisuuden hallinnassa.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a594bacb1fcf53ae4a278dbb26f1de174e22288c
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275599"
---
# <a name="schedule-work-orders"></a>Ajoita työtilauksia

[!include [banner](../../includes/banner.md)]

 

Tässä ohjeaiheessa selitetään, miten työtilaukset ajoitetaan käyttöomaisuuden hallinnassa. 

Työtilauksen vaadittu tuntimäärä määritetään ennustettujen tuntien summana vähennettynä kirjattujen tuntien määrällä. Jos aikaa tarvitaan enemmän, ennustetta on muutettava vastaavasti. Kohdassa **Resurssien hallinta** > **yhteiset** > **Työtilaukset** > **Kaikki työtilaukset** tai **Aktiiviset työtilaukset** voit tarkastella tai muokata työtilauksen ennusteita valitsemalla työtilauksen ja valitsemalla **Ennuste** **Työtilaus**-välilehdessä. Kun työtilaukset on luotu ja arvioitu, seuraavaksi on kohdistettava tarvittavat kunnossapitotyöntekijät ja työkalut työtilausten suorittamista varten.

Voidaan ajoittaa vain työtilaukset, joissa on työtilauksen elinkaaritila, joka sallii ajoituksen. Ajoitus sallitaan kohdan **Resurssien hallinta** > **Asetukset** > **Työtilaukset** > **Elinkaaren tilat** > **Yleiset** -pikavälilehti > **Salli ajoitus** -valitsin.

1. Valitse **Resurssien hallinta** > **yhteiset** > **työtilaukset** > **kaikki työtilaukset**.

2. Valitse luettelosta työtilaukset, jotka haluat ajoittaa. Voit esimerkiksi lajitella luettelon **Nykyinen elinkaaren tila** -kentän mukaan.

3. Valitse **Yleiset**-välilehdestä **Ajoita**.

4. **Ajoita työtilaukset** -valintaikkunassa voit tarvittaessa lisätä odotettuun alkamispäivämäärään ja palvelutasoon liittyviä valintoja. Jos ajoitusprosessissa on huomioitava muiden töiden jo ajoitettujen resurssien kapasiteettirajoitukset, varmista, että **Resurssi**, **Työkalu** ja **Työntekijä**-vaihtopainikkeiksi on määritetty "Kyllä".

    [!NOTE]
    Jos määrität **Resurssi**-, **Työkalu**- ja **Työntekijä**-vaihtopainikkeiksi Ei, aiemmin luodut varaukset ohitetaan. Infolokissa näkyy luettelo päällekkäisistä työtilausaikatauluista, ja voit avata työtilauksen ja ajoittaa sen tarvittaessa uudelleen valitsemalla viestit.

5. Jos haluat lisätietoja aikataulutuksesta, valitse "Kyllä" **Yksityiskohtainen**-vaihtopainikkeessa. Tämä tarkoittaa, että työtilausten ja kunnossapitotyöntekijöiden laskettujen tulosten tiedot näkyvät infolokissa.

6. Valitse **OK** käynnistääksesi ajoitusprosessin.

7. Kun ajoitus on tehty, infolokissa näkyy ajoitettujen työtilausten määrä ja tarkempia tietoja, jos **Yksityiskohtainen**-vaihtopainikkeen tilaksi on määritetty Kyllä.

>[!NOTE]
>Työtilaukset ajoitetaan yhtä työtilausta kohden, ei yhtä työtilauksen työtä kohden. Voit myös avata **Ajoita työtilauksia** -valintaikkunan suoraan kohdassa **Resurssien hallinta** > **Kausittainen** > **työtilaukset** > **Ajoita työtilauksia**. Tee valinnat ja aloita työtilausten ajoittaminen valitsemalla **OK**. Voit määrittää työtilausten ajoituksen erätyönä **Ajoita työtilaukset** -valintaikkunan **Suorita taustalla** -pikavälilehdessä.

*Esimerkki:* Alla olevassa kuvassa **Odotettu alku** -kenttään lisätty kaava luo työtilausten aikataulutuksen kaikille työtilauksille, joiden odotettu alkamispäivä on viikko tästä lähtien ja myöhemmin. Tämä kaava voi olla hyödyllinen, kun suoritat työtilausten ajoitusta jatkuvasti, mutta haluat varmistaa, että seuraaville 5-6 päivälle ajoitettuja työtilauksia ei ajoiteta uudelleen.

![Kuva 1](media/03-work-order-scheduling.png)

Työtilauksiin liittyvä työtilaustyyppi voi määrittää yhden kunnossapitotyöntekijän ajoituksen (**Resurssien hallinta** > **Asetukset** > **Työtilaukset** > **Työtilaustyypit** > **Yksi ylläpitotyöntekijä** -valintanäppäimeksi määritetty "Kyllä"). Tämä tarkoittaa, että jos työtilaustyyppiä käytetään työtilauksessa, **Yksi ylläpitotyöntekijä** -vaihtopainikkeen arvoksi tulee automaattisesti "Kyllä" **Kaikki työtilaukset** -tietosivun **Otsikko**-näkymän **Ajoita**-pikavälilehdessä. Työtilauksen ajoituksen aikana kaikki työtilaukseen luodut työtilaustyöt ajoitetaan myöhemmin samalle kunnossapitotyöntekijälle. Voit tarvittaessa muokata **Yksi ylläpitotyöntekijä** -valintaa**Kaikki työtilaukset** -kohdassa, jolloin useiden työntekijöiden tai yhden työntekijän työtilaustöiden ajoittaminen sallitaan.

Käyttöomaisuuden hallinnan ajoittaminen sisältää useita tekijöitä aikataulutuksen laskennassa:

- Laskee sekä työtilausten että kunnossapitotyöntekijöiden tulokset. Työtilausten ja kunnossapitotyöntekijöiden tulokset määritetään **Resurssienhallinnan parametrit** -kohdassa. 
- Työn suorittamiseen tarvittavien osaamisalueiden, taitojen ja sertifikaattien tarkistaminen. Osaamiaslaueet ja sertifikaatit ylläpitotyöntekijöille määritettän kohdassa **Henkilöstöhallinto** -moduuli (**Henkilöstöhallinto** > **Työntekijät** > **Työntekijät**, valitse työntekijä listasta, **Työntekijä**-välilehti > **Osaamistiedot**-osa > **Osaamisalueet** ja **Sertifikaatit** -painikkeet). Myös osaamisalueet ja sertifikaatit voidaan lisätä ylläpitotöiden tyyppeihin ja ylläpitotöiden toimialoihin. Luo lisätietoja kohdassa [Ylläpitotöiden tyyppiluokat ja ylläpitotöiden tyypit, ylläpitotöiden tyyppien variantit, ylläpitotöiden toimialat ja ylläpidon tarkistuslistat](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).  

## <a name="scores-used-in-work-order-scheduling"></a>Työtilausten suunnittelussa käytettävät pisteet

Työtilaustyön tulosten laskemisen perusteena käytetään odotettua aloituspäivää ja työtilauksen palvelutasoa.

**Aloituspäivä**-laskenta: jokaisesta tulevasta päivästä, joka lasketaan odotetun alkamispäivän perusteella, aloituspäivämäärän pistemäärä vähennetään ja kerrotaan tuloksella, joka on alla olevissa esimerkeissä 10.

**Kriittisyys**-laskeminen: kriittisyyspisteet kerrottuna työtilauksen kriittisyydellä.

**Palvelutaso**-laskeminen: palvelutason pisteet jaetaan työtilauksen palvelutason mukaan.

Alla olevissa esimerkeissä kriittisyyspisteet ovat "2" ja palvelutason tulokset ovat "5" ja "100".

**Esimerkki 1:**

| Työtilauksen tunnus | Odotettu alkamispäivämäärä | Työtilauksen kriittisyys | Työtilauksen palvelutaso | Laskelma               | Pistemäärä      |
|---------------|---------------------|------------------------|--------------------------|---------------------------|------------|
| WO-00010816   | Huomenna            | 2                      | 20              | (-1 \* 10) + (2 \* 2) + 5 / 20     | \- 5.75    |
| WO-00010817   | Kaksi päivää tästä eteenpäin   | 2                      | 20              | (-2 \* 10) + (2 \* 2) + 5 / 20     | \- 15.75   |
| WO-00010818   | Kaksi päivää tästä eteenpäin   | 3                      | 5               | (-2 \* 10) + (2 \* 3) + 5 / 5      | \- 13      |

Työtilaukset ajoitetaan seuraavassa järjestyksessä: WO-000108**16**, WO-000108**18**, WO-000108**17**.

**Esimerkki 2:**

| Työtilauksen tunnus | Odotettu alkamispäivämäärä | Työtilauksen kriittisyys | Työtilauksen palvelutaso | Laskelma                 | Pistemäärä    |
|---------------|---------------------|------------------------|---------------------|----------------------------------|----------|
| WO-00010816   | Huomenna            | 2                      | 20                  | (-1 \* 10) + (2 \* 2) + 100 / 20 | \- 1     |
| WO-00010817   | Kaksi päivää tästä eteenpäin   | 2                      | 20                  | (-2 \* 10) + (2 \* 2) + 100 / 20 | \- 11    |
| WO-00010818   | Kaksi päivää tästä eteenpäin   | 3                      | 5                   | (-2 \* 10) + (2 \* 3) + 100 / 5  | 6        |

Jos palvelutason pisteet nostetaan lukuun 100 5:n sijasta, ajoitusjärjestys on: WO-000108**18**, WO-000108**16**, WO-000108**17**.

Työtilausten työntekijöiden laskennassa käytettävät luokituspisteet määritetään luvuiksi, jotka lisätään kuhunkin huoltotyön tekijän laskentaan työtilauksen ajoituksessa. Työtilauksessa valitaan huoltotyöntekijä, jolla on korkein pistemäärä. Seuraavassa on lyhyt kuvaus kunnossapitotyöntekijän tuloksista:

| Ylläpitotyöntekijän pistemäärä| Kuvaus |
|---|---|
| Vastaava työntekijä | Jos kunnossapitotyöntekijä on valittu työtilauksen vastuulliseksi työntekijäksi, tulos lisätään. |
| Vastuullinen ylläpitotyöntekijöiden ryhmä | Jos kunnossapitotyöntekijä on valittu osaksi työtilauksen vastuullista työntekijäryhmää, tulos lisätään. |
| Ensisijainen ylläpitotyöntekijä         | Jos työntekijä on valittu resurssin ensisijaiseksi työntekijäksi, tulos lisätään. |
| Ensisijainen ylläpitotyöntekijöiden ryhmä   | Jos työntekijä on valittu osaksi resurssin ensisijaista työntekijäryhmää, tulos lisätään.  |
| Toimipaikka  | Jos yrityksessä käytetään toiminnallisia sijainteja, ylläpitotyöntekijät saavat täydet pisteet, jos ne sijaitsevat resurssiin liittyvässä toiminnallisessa sijainnissa. Jos resurssin toiminnallisella sijainnilla on pääsijainti, kyseisen toimintasijainnin ylläpitotyöntekijät saavat puolet pisteistä. Jos kyseisessä sijainnissa on myös ylätaso, kyseisessä sijainnissa olevat ylläpitotyöntekijät saavat 1/3 pisteistä. Jos kyseisessä sijainnissa on myös ylätaso, kyseisessä sijainnissa olevat ylläpitotyöntekijät saavat 1/4 pisteistä jne. Jos yrityksessä käytetään resurssin sijaintia, jota ei suositella, sijaisntipisteet lasketaan sijainnin, alueen ja vyöhykkeen mukaan. Työntekijät saavat täydet pisteet, jos ne sijaitsevat resurssiin liittyvässä sijainnissa ja alueella sekä vyöhykkeellä. Jos työntekijän sijainti vastaa vain sijaintia ja aluetta, ylläpitotyöntekijän luokituspisteet ovat 2/3 täysistä pisteistä. Jos ylläpitotyöntekijän sijainti vastaa vain sijaintia, ylläpitotyöntekijän luokituspisteet ovat 1/3 täysistä pisteistä. |
| Työntekijän aloituspäivämäärä  | Jokaiselle päivälle, jonka suunniteltu alkamispäivämäärä on myöhempi kuin odotettu alkamispäivämäärä, tulos vähennetään.  |

>[!NOTE]
>Jos tulokseksi määrityetään 0, tätä pistettä ei lasketa. Tästä on hyötyä esimerkiksi silloin, kun et halua sisällyttää aikataulutukseen vastaavaa työntekijää.

## <a name="competencies-used-in-work-order-scheduling"></a>Työtilausten suunnittelussa käytettävät osaamistiedot

Osaamisalueiden ja sertifikaattien vaatimukset voidaan määrittää ylläpitotyötyypeille (**Resurssien hallinta** > **Asetukset** > **Työt** > **ylläpitotöiden tyypit**) jaylläpitotöiden toimialoille (**Resurssien hallinta** > **Asetukset** > **Työt** > **Ylläpitotyön toimiala**). 

Kunnossapitotöiden tyypit ja kunnossapitotöiden toimialat valitaan työtilaustöille. Jos osaamislaueet tai sertifikaatit on valittu kunnossapitotöiden tyypille tai kunnossapitotöiden toimialalle ja jos kyseistä kunnossapitotyön tyyppiä tai kunnossapitotyön toimialaa on käytetty työtilaustyössä, vain osaamisalueissa ja sertifikaateissa vastaavat huoltotyö tekijät on ajoitetaan työskentelemään työtilaukselle.

<a name="gantt"></a>

## <a name="work-with-scheduled-work-orders-using-a-gantt-chart"></a>Ajoitettujen työtilausten käsitteleminen Gantt-kaavion avulla

**Ajoitetut työtilaukset Gantt-kaaviossa** tarjoaa graafisen käyttöliittymän, jossa voit tarkastella ja ajoittaa työtilauksia uudelleen.

Gantt-kaavion tarkasteleminen ja käsitteleminen:

1. Siirry kohtaan **Käyttöomaisuuden hallinta > työtilaukset > ajoitettujen työtilausten Gantt-kaavio**.

1. **Asetukset**-osan avattavien luetteloiden ja kenttien avulla voit määrittää Gantt-kaaviossa näytettävän toimintosijainnin, aikavälin ja aika-asteikon.

1. Valitse **Käytä**.

    - Gantt-kaavio päivittyy siten, että se näyttää asetuksia vastaavat ajoitetut työtilaukset. Kutakin työtilausta edustaa sininen suorakulmio.
    - Jos haluat ajoittaa näytössä olevan työtilauksen uudelleen, valitse ja vedä se sitten sopivaan uuteen päivämäärään ja kellonaikaan.

1. Jos teit muutoksia, tallenna ne valitsemalla toimintoruudussa **Tallenna**.
