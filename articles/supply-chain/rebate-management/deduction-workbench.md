---
title: Hallitse vähennyksiä käyttämällä vähennyksen työtilaa
description: Tässä artikkelissa kuvataan vähennyksen työtilan käyttö, jonka avulla voit käsitellä asiakkaan maksuja, jotka sisältävät vähennyksiä.
author: sherry-zheng
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 607ad528b56d1f0c9a78e113f67c920cdae6e620
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873605"
---
# <a name="manage-deductions-using-the-deduction-workbench"></a>Hallitse vähennyksiä käyttämällä vähennyksen työtilaa

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan vähennyksen työtilan käyttö, jonka avulla voit käsitellä asiakkaan maksuja, jotka sisältävät vähennyksiä.

Asiakas, joka on oikeutettu ostohyvitykseen, voi lunastaa ostohyvityksen heti. Sen sijaan asiakas voi lähettää maksun, joka sisältää ostohyvityksen suuruisen vähennyksen. Jos haluat käsitellä tämän tyyppistä tapahtumaa, voit käyttää vähennyksen työtilaa vähennysten täsmäyttämiseen avointen luottotapahtumien kanssa, vähennysten jakamiseen ja vähennysten pois kirjaamiseen.

> [!NOTE]
> Vähennyksen työtila on ollut osa Microsoft Dynamics 365 Supply Chain Managementin myynti- ja markkinointitoimintoja jo kauan aikaa. Sitä on nyt parannettu siten, että se toimii myös uuden **ostohyvityksen hallinta** -moduulin kanssa. Tässä artikkelissa kuvataan, miten vähennyksen työtilan sekä vanhempia ominaisuuksia että ostohyvitysten hallintatoimintoja käytetään. Jos [järjestelmän **ostohyvitysten hallinta** -moduulia ei ole otettu käyttöön](rebate-management-enable.md), osa tässä kuvatuista toiminnoista ei kuitenkaan ole käytettävissä.

## <a name="prerequisites"></a>Edellytykset

### <a name="set-up-the-old-deduction-management-system"></a>Vanhan vähennystenhallintajärjestelmän määritäminen

Voit käyttää vähennystyökorvauksia yhdessä Supply Chain Managementin vanhojen vähennysten hallintaominaisuuksien kanssa, vaikka et käyttäisikään **ostohyvityksen hallinta** -moduulia. Järjestelmä on kuitenkin ensin valmisteltava tässä osassa kuvatulla tavalla.

Ennen kuin voit käyttää vähennyksen työtilaa, sinun on suoritettava määritystehtävät, jotka on kuvattu kohdassa [Vähennyksen hallinnan määrittäminen](/dynamicsax-2012/appuser-itpro/set-up-deduction-management). Sinulla tulisi myös määrittää asiakkaalle jonkinlainen ostohyvityssopimus. Joko asiakkaan ostohyvitys, kuten kohdassa [Asiakashyvitysten määrittäminen ja ylläpito](/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-customer-rebates) on kuvattu tai myynninedistämispalkkion hyvitys.

Jos kohdistat vähennyksen asiakkaan ostohyvitykseen, sinun on suoritettava seuraavat tehtävät:

- [Määritä asiakkaan ostohyvitykset](/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-customer-rebates).
- Hyväksy ja käsittele ostohyvitys, jotta voit käyttää vähennyksen työtilaa.

Jos käytät vähennystä ostohyvitysalennukseen, sinun on suoritettava seuraavat tehtävät:

- Määritä takaisinmaksualennukset.
- Ota käyttöön takaisinmaksualennukset.

### <a name="configure-accounts-receivable-and-deductions"></a><a name="accounts-receivable-deductions"></a>Myyntireskontran ja vähennysten määrittäminen

Järjestelmä tallentaa kaikki vähennystapahtumat vaatimuskirjauskansioon. Siksi järjestelmään on sisällytettävä kirjauskansio, jota voidaan käyttää tähän tarkoitukseen. Jos sinulla ei ole vielä vaatimuskirjauskansiota, määritä se nyt. Tämä kirjauskansio on pakollinen, jotta vähennykset luodaan suoraan vähennyksen työtila-, asiakastilitys- tai asiakassivulla.

Määritä uusi vaatimuskirjauskansio vähennyksille seuraavien ohjeiden avulla.

1. Siirry kohtaan **Kirjanpito \> Kirjauskansion asetukset \> Kirjauskansioiden nimet**.
1. Valitse **Uusi** ja määritä uudelle kirjauskansion nimelle seuraavat kentät:

    - **Nimi** – Anna vaatimuskirjauskansiolle yksilöivä nimi.
    - **Kuvaus** – Syötä uuden kirjauskansion kuvaus.
    - **Kirjauskansion tyyppi** – Valitse *Päivittäinen*.
    - **Tositesarja** – Määritä aiemmin luotu numerosarja. Vaihtoehtoisesti voit luoda uuden numerosarjan, jolla on yrityksen käyttöalue, ja määrittää sen uudelle kirjauskansion nimelle.

1. Valitse **Myyntireskontra \> Asetukset \> Myyntireskontran parametrit**.
1. Määritä **Vähennykset**-välilehden **Yleiset**-pikavälilehdessä **Vaatimuskirjauskansion nimi** -kenttään luomasi kirjauskansion nimi.
1. Määritä **Palautustilaus**-pikavälilehdellä seuraavat kentät:

    - **Luo palautustilaus**– Valitsemalla tämän vaihtoehdon voit määrittää, mitä järjestelmän pitää tehdä, kun määräpohjainen vaatimus hyväksytään:

        - *Kyllä* – Palautustilauksen luominen.
        - *Ei* – Luo negatiivinen myyntitilaus.

    - **Luominen ilman liitettyä laskua** – Valitse arvo, joka määrittää, mitä järjestelmä tekee, kun määräperusteinen vaatimus hyväksytään, mutta laskua ei ole liitetty:

        - *Hyväkayminen* – Ostopalautustilauksen luominen.
        - *Varoitus* – Luo palautustilaus, mutta näyttöön tulee seuraava varoitussanoma: "Vaatimusta ei ole liitetty laskuun."
        - *Virhe* – Älä luo palautustilausta ja näyttöön tulee seuraava virhesanoma: "Vaatimusta ei ole liitetty laskuun. Päivitys on keskeytetty.

    - **Luo palautustilaus ennen vähennyksen hyväksyntää** – Määritä tämän asetuksen arvoksi *Kyllä*, jos palautustilaukset voidaan luoda ennen vaatimuksen hyväksymistä. Tämä asetus koskee vain määräpohjaisia vaatimuksia, joissa **Luo palautustilaus** -asetus on *Kyllä*.

### <a name="configure-general-ledger-parameters"></a>Konfiguroi yleisen kirjanpidon parametrit

Kun järjestelmä luo uudelle vähennykselle vaatimuskirjauskansion, järjestelmä luo myös kaksi uutta asiakastapahtumaa, jotka vastakirjaavat vaatimuksen summan alkuperäistä laskua vastaan, ja toisen, joka rekisteröi asiakkaan velan vaatimuksen summaan (koska vaatimusta ei ole vielä hyväksytty). Järjestelmä on näin ollen määritettävä niin, että yhdellä tositteella voi olla useita asiakasrivejä.

Jos haluat ottaa käyttöön yhden tositteen, jossa on useita asiakasrivejä, noudata seuraavia ohjeita.

1. Siirry kohtaan **Kirjanpito \> Kirjanpidon asetukset \> Kirjanpitoparametrit**.
1. Määritä **Kirjanpito**-välilehden **Yleiset**-pikavälilehdessä **Salli useita tapahtumia yhdessä tositteessa** -asetuksen arvoksi *Kyllä*.
1. Jos näyttöön tulee varoitussanoma, hyväksy muutos valitsemalla **Sulje**.

### <a name="create-deduction-reasons"></a><a name="deduction-reasons"></a>Vähennyksen syiden luominen

Järjestelmä edellyttää, että käyttäjät määrittävät kunkin vähennyksen syyn suoraan vähennyksen työ- tai asiakastilityssivulle. Syy määrittää, miten vähennystä käsitellään, kun se hyväksytään.

1. Siirry kohtaan **Myynti ja markkinointi \> Kauppakorvaukset \> Vähennykset \> Vähennysten syyt**.
1. Lisää rivi ruudukkoon valitsemalla **Uusi** ja määritä sitten seuraavat kentät:

    - **Vaatimuksen syy** – Anna syylle yksilöivä nimi.
    - **Kuvaus** – Syötä syyn kuvaus, joka sisältää lisätietoja ryhmän käytöstä.
    - **Vaatimusperuste** – Valitse vaatimusperuste vaatimuksen syylle:

        - *Hintaperusteinen* – Voit luoda vapaatekstihyvityksen hyväksynnän yhteydessä.
        - *Määräperuste* – Negatiivisen myyntitilauksen tai palautustilauksen luominen hyväksynnän yhteydessä.

    - **Palautuksen syykoodi** – Valitse palautuksen syykoodi, joita käytetään palautustilauksen **palautuksen syykoodin** arvona.
    - **Tyyppi** – Valitse vähennyksen tyyppi. Valitun tyypin **Vähennyksen vastatili**-arvoa käytetään **Vähennyksen vastatili** -kentän vähennyksen tai vaatimuksen luomisen yhteydessä. Vähennystyypit määritetään **Vähennystyypit**-sivulla (**Myynti ja markkinointi \> Myynninedistämispalkkiot \> Vähennykset \> Vähennystyypit**).
    - **Vaatimuskirjaustili** – Tämä kenttä on käytettävissä vain, kun **Vaatimusperuste** -kentän arvoksi on määritetty *Hintaperuste*. Kun hintaan perustuva vaatimus hyväksytään, järjestelmä määrittää tässä valitsemasi kirjanpidon tilin **päätili**-arvoksi vapaan tekstin hyvityslaskun luonnokselle.

### <a name="set-up-the-settle-approved-deductions-periodic-task"></a>Selvitä hyväksyttyjen vähennysten kausittaisen tehtävän määritäminen

Voit määrittää *Selvitä hyväksytyt vähennykset* -kausittaisen tehtävän niin, että vähennykset ja hyvitykset täsmäytetään automaattisesti niiden vähennysten ja hyvitysten täsmäytystä varten, jotka vastaavat **vähennystunnus**-arvoja ja -summia, kun vähennykset luodaan käyttämällä **Uusi vähennys** -komentoa vähennyksen työ- tai asiakassivulla.

Voit ajoittaa tämän tehtävän menemällä kohtaan **Myyntimarkkinointi \> Kausittaiset tehtävät \> Selvitä hyväksytyt vähennykset** ja määritä asetukset, suodattimet ja aikataulu sekä muut kausittaiset tehtävät.

> [!NOTE]
> Jos **Automaattinen tilitys** -asetus on *Kyllä* **Myyntireskontran parametrit** -sivun **Tilitys**-välilehdessä (**Myyntireskontra \> Asetukset \> Myyntireskontran parametrit**), *Selvitä hyväksytyt vähennykset* -kausittainen tehtävä ei tee mitään, koska hyvitys tilitetään automaattisesti.

## <a name="create-a-deduction"></a>Vähennyksen luominen

### <a name="create-a-deduction-journal-entry-by-using-the-customer-payment-journal"></a>Vähennyksen kirjauskansiomerkinnän luominen asiakkaan maksukirjauskansion avulla

Luo vähennyskirjauskansioviesti noudattamalla seuraavia ohjeita.

1. Valitse **Myyntireskontra \> Maksut \> Asiakkaan maksukirjauskansio**.
1. Valitse **Uusi** lisätäksesi rivin ruudukkoon.
1. Valitse uuden rivin **Nimi**-kentästä kirjauskansion nimi.
1. Valitse toimintoruudussa **Rivit**.
1. Kirjoita päivämäärä, yritystili ja asiakkaan tilinumero.
1. **Lasku**-kentässä valitse lasku, johon vähennys on liitetty.
1. Kirjoita **Saldo**-kenttään asiakkaan maksama summa.
1. Valitse **OK** vahvistaaksesi, että summa on pienempi kuin merkityn tapahtuman kokonaissumma.
1. Valitse vastatilin tilityyppi vastatili.
1. Valitse ruudukon yllä olevasta työkalurivistä **Vähennykset**.
1. Valitse **Vähennykset**-sivulla toimintoruudussa **Uusi** lisätäksesi rivin ruudukkoon. Uuden rivin **Vähennystunnus**-kenttä määritetään automaattisesti.
1. Valitse **Tyyppi**-kentässä vähennystyyppi.
1. Syötä **Summa**-kenttään summa, joka näkyy vähennysluettelon alapuolella olevassa **Saldo**-kentässä. Tämä summa vastaa summaa, jonka asiakas vähensi maksusta.
1. Sulje **Vähennys**-sivu. Palaat **Asiakasmaksu**-sivulle, jolla on nyt uusi vähennysrivi.
1. Valitse toimintoruudussa **Vahvista \> Vahvista**. Sinun tulisi saada seuraava sanoma: "Kirjauskansio on OK".
1. Valitse toimintoruudussa **Kirjaa**.

### <a name="create-a-deduction-by-using-the-deduction-workbench"></a>Vähennyksen luominen vähennyksen työtilan avulla

Luo uusi vähennys vähennystyötilassa seuraavien ohjeiden avulla.

1. Siirry kohtaan **Myynti ja markkinointi \> Kauppakorvaukset \> Vähennykset \> Vähennysten työtila**.
1. Valitse toimintoruudussa **Ylläpidä \> Uusi vähennys**.

    **Uusi vähennys** -valintaikkunassa **Vähennystunnus**-kenttä määritetään **Kauppavähennyksiä koskevat parametrit** -sivulla määritetyn **vähennyksen tunnuksen** numerosarjan perusteella (**Myynti ja markkinointi \> Asetukset \> Kauppakorvaukset \> Myynninedistämispalkkioiden hallintaparametrit**).

1. Määritä seuraavat kentät:

    - **Asiakastili** – Valitse asiakastili, jota vähennys koskee.
    - **Ulkoinen vaatimusnumero** – Kirjoita asiakkaan vaatimusviite.
    - **Vaatimussumma** – Määritä verollinen saatavan summa. Arvon on oltava positiivinen.
    - **Valuutta** – Valitse vähennyksen valuutta. Oletusarvo on valitulle asiakastilille määritetty valuutta.
    - **Vaatimusperuste** – Valitse vaatimusperuste. Vaatimusperuste määrittää hyvitystapahtuman tyypin, joka luodaan, kun vähennys tai vaatimus on hyväksytty.

        - *Hintaperusteinen* – Vapaatekstin luonnoslasku luodaan.
        - *Määräperuste* – Negatiivisen myyntitilauksen tai palautustilauksen luominen.

    - **Vaatimuspäivä** – Valitse vaatimuksen päivämäärä. Oletusarvo on nykyinen päivämäärä.
    - **Vaatimuksen syy** – Valitse nykyiseen vähennykseen sisältyvä syykoodi. Valitsemasi vaatimusperuste vaikuttaa valittuihin asetuksiin. Lisätietoja tässä kohdassa valittavissa olevien vähennysten syiden luo ja konfiguroinnista on tämän artikkelin aiemmassa [Luo vähennyksen syyt](#deduction-reasons) -osassa.
    - **Huomautukset** – Lisää mahdolliset huomautukset. Kun vaatimus hyväksytään, hyväksyjä voi muokata tai lisätä vaatimuksen huomautuksia.
    - **Luo vaatimuskirjauskansio** – Valitsemalla tämän vaihtoehdon voit määrittää, luodaanko vaatimuskirjauskansio, kun vaatimus tai vähennys luodaan:

        - *Kyllä* – Järjestelmä luo ja kirjaa yleisen kirjauskansion käyttämällä **Myyntireskontran parametrit** -sivulla määritettyä vaatimuskirjauskansiota. (Lisätietoja on kohdassa [Määritä myyntireskontran ja vähennysten](#accounts-receivable-deductions) osa aiemmin tässä artikkelissa.) Kun lasku on liitetty vaatimukseen, vaatimuskirjauskansion avulla vähennetään sovellettavaa laskua. Jos vaatimus hylätään myöhemmin, hakemuskirjauskansio ja tilitys (jos lasku on liitetty) peruutetaan.
        - *Ei* – Tällä hetkellä ei luoda vaatimuskirjauskansiota. Se luodaan, kun vaatimus hyväksytään. Lasku voidaan vielä liittää uuteen vaatimukseen, vaikka vaatimuskirjauskansiota ei luoda. Selvitystä ei kuitenkaan voi tehdä ilman vaatimuskirjauskansiota.

1. Valitse **OK**.

    Uusi vähennys luodaan. Jos määrität **Luo vaatimuskirjauskansio** -asetuksen arvoksi *Kyllä*, seuraavat tapahtumat kirjataan:

    - **Kaksi uutta asiakastapahtumaa** – Yksi tapahtuma vastakirjaa vaatimuksen summan alkuperäistä laskua vastaan. Muut tapahtumat rekisteröivät asiakkaan velan vaatimuksen summaan, koska vaatimusta ei ole vielä hyväksytty. Alkuperäinen laskutapahtuma ja vastakirjausvaatimustapahtuma merkitään automaattisesti tilitykseen, kun liität laskun valitsemalla toimintoruudusta **Ylläpidä \> liitä lasku**.
    - **Kaksi vastatapahtumaa** – Nämä tapahtumat kirjataan **vähennyksen vastakirjanpito** -tilille.
    - **Vaatimuskirjauskansio** – Voit tarkastella kunkin vähennyksen työtilassa näkyvän vähennyksen kirjauskansiota valitsemalla **Viitteet**-välilehden. Vaatimuskirjauskansio näkyy **Kirjauskansion eränumero** -kentässä. Voit tarkastella vaatimuskirjauskansiota myös **Vähennystapahtumat**-välilehdessä. Siinä sen **päivitystyypin** arvo on *Täsmäytä*.

### <a name="create-a-deduction-from-a-customer-settlement"></a>Vähennyksen luominen asiakastilitysten avulla

Prosessi, jossa vähennys luodaan asiakastilityksistä, muistuttaa vähennysten luomista vähennyksen avulla. Asiakas- ja laskutusvaluutta määritetään kuitenkin automaattisesti ja lasku liitetään. Kun luot vaatimuksen tai vähennyksen asiakkaan tilityssivulla, sinun ei tarvitse valita toimintoruudusta **Ylläpidä \> Liitä lasku**.

1. Siirry kohtaan **Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat**.
1. Valitse asiakas, jolle vähennys luodaan.
1. Valitse toimintoruudun **Kerää**-välilehden **Selvitä**-ryhmässä **Selvitä tapahtumat**.
1. Valitse **Tapahtumien määrittäminen** -valintaikkunan **Yhteenveto**-välilehdestä lasku, johon vähennys luodaan.
1. Valitse työkaluriviltä **Vähennykset \> Uusi vähennys**.

    **Uusi vähennys** -valintaikkunassa **Vähennystunnus**-kenttä määritetään **Kauppavähennyksiä koskevat parametrit** -sivulla määritetyn **vähennyksen tunnuksen** numerosarjan perusteella (**Myynti ja markkinointi \> Asetukset \> Kauppakorvaukset \> Myynninedistämispalkkioiden hallintaparametrit**). **Asiakastili**-kenttä on määritetty asiakastilille, jota vähennys koskee.

1. Määritä seuraavat kentät:

    - **Ulkoinen vaatimusnumero** – Kirjoita asiakkaan vaatimusviite.
    - **Vaatimussumma** – Määritä verollinen saatavan summa. Arvon on oltava positiivinen.
    - **Valuutta** – Valitse vähennyksen valuutta. Oletusarvo on valitulle asiakastilille määritetty valuutta.
    - **Vaatimusperuste** – Valitse vaatimusperuste. Vaatimusperuste määrittää hyvitystapahtuman tyypin, joka luodaan, kun vähennys tai vaatimus on hyväksytty.

        - *Hintaperusteinen* – Vapaatekstin luonnoslasku luodaan.
        - *Määräperuste* – Negatiivisen myyntitilauksen tai palautustilauksen luominen.

    - **Vaatimuspäivä** – Valitse vaatimuksen päivämäärä. Oletusarvo on nykyinen päivämäärä.
    - **Vaatimuksen syy** – Valitse nykyiseen vähennykseen sisältyvä syykoodi. Valitsemasi vaatimusperuste vaikuttaa valittuihin asetuksiin. Lisätietoja tässä kohdassa valittavissa olevien vähennysten syiden luo ja konfiguroinnista on tämän artikkelin aiemmassa [Luo vähennyksen syyt](#deduction-reasons) -osassa.
    - **Huomautukset** – Lisää mahdolliset huomautukset. Kun vaatimus hyväksytään, hyväksyjä voi muokata tai lisätä vaatimuksen huomautuksia.
    - **Luo vaatimuskirjauskansio** – Valitsemalla tämän vaihtoehdon voit määrittää, luodaanko vaatimuskirjauskansio, kun vaatimus tai vähennys luodaan:

        - *Kyllä* – Järjestelmä luo ja kirjaa yleisen kirjauskansion käyttämällä **Myyntireskontran parametrit** -sivulla määritettyä vaatimuskirjauskansiota. (Lisätietoja on kohdassa [Määritä myyntireskontran ja vähennysten](#accounts-receivable-deductions) osa aiemmin tässä artikkelissa.) Kun lasku on liitetty vaatimukseen, vaatimuskirjauskansion avulla vähennetään sovellettavaa laskua. Jos vaatimus hylätään myöhemmin, hakemuskirjauskansio ja tilitys (jos lasku on liitetty) peruutetaan.
        - *Ei* – Tällä hetkellä ei luoda vaatimuskirjauskansiota. Se luodaan, kun vaatimus hyväksytään. Lasku voidaan vielä liittää uuteen vaatimukseen, vaikka vaatimuskirjauskansiota ei luoda. Selvitystä ei kuitenkaan voi tehdä ilman vaatimuskirjauskansiota.

1. Valitse **OK**.

    Uusi vähennys luodaan. Jos määrität **Luo vaatimuskirjauskansio** -asetuksen arvoksi *Kyllä*, seuraavat tapahtumat kirjataan:

    - **Kaksi uutta asiakastapahtumaa** – Yksi tapahtuma vastakirjaa vaatimuksen summan alkuperäistä laskua vastaan. Muut tapahtumat rekisteröivät asiakkaan velan vaatimuksen summaan, koska vaatimusta ei ole vielä hyväksytty. Alkuperäinen laskutapahtuma ja vastakirjausvaatimustapahtuma merkitään automaattisesti tilitykseen, kun liität laskun valitsemalla toimintoruudusta **Ylläpidä \> liitä lasku**.
    - **Kaksi vastatapahtumaa** – Nämä tapahtumat kirjataan **vähennyksen vastakirjanpito** -tilille.
    - **Vaatimuskirjauskansio** – Voit tarkastella kunkin vähennyksen työtilassa näkyvän vähennyksen kirjauskansiota valitsemalla **Viitteet**-välilehden. Vaatimuskirjauskansio näkyy **Kirjauskansion eränumero** -kentässä. Voit tarkastella vaatimuskirjauskansiota myös **Vähennystapahtumat**-välilehdessä. Siinä sen **päivitystyypin** arvo on *Täsmäytä*.

    Olet palannut **Palautetut tapahtumat** -sivulle, jossa valittu lasku näkyy merkittynä. **Kirjaa**-painike on käytettävissä vain, jos määrität **Luo vaatimuskirjauskansio** -asetuksen arvoksi *Kyllä*. Jos se on käytettävissä, pienennä laskun saldoa **vaatimussumman** arvolla valitsemalla **Kirjaa**.

### <a name="create-a-deduction-from-a-customer-page"></a>Vähennyksen luominen asiakassivun avulla

Prosessi, jossa vähennys luodaan asiakassivulta, muistuttaa vähennysten luomista vähennyksen avulla. Asiakas kuitenkin määritetään automaattisesti.

1. Siirry kohtaan **Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat**.
1. Valitse asiakas, jolle vähennys luodaan.
1. Valitse **Kerää**-välilehden **Vähennykset**-ryhmän toimintoruudussa **Luo vähennykset**.

    **Uusi vähennys** -valintaikkunassa **Vähennystunnus**-kenttä määritetään **Kauppavähennyksiä koskevat parametrit** -sivulla määritetyn **vähennyksen tunnuksen** numerosarjan perusteella (**Myynti ja markkinointi \> Asetukset \> Kauppakorvaukset \> Myynninedistämispalkkioiden hallintaparametrit**). **Asiakastili**-kenttä on määritetty asiakastilille, jota vähennys koskee.

1. Määritä seuraavat kentät:

    - **Ulkoinen vaatimusnumero** – Kirjoita asiakkaan vaatimusviite.
    - **Vaatimussumma** – Määritä verollinen saatavan summa. Arvon on oltava positiivinen.
    - **Valuutta** – Valitse vähennyksen valuutta. Oletusarvo on valitulle asiakastilille määritetty valuutta.
    - **Vaatimusperuste** – Valitse vaatimusperuste. Vaatimusperuste määrittää hyvitystapahtuman tyypin, joka luodaan, kun vähennys tai vaatimus on hyväksytty.

        - *Hintaperusteinen* – Vapaatekstin luonnoslasku luodaan.
        - *Määräperuste* – Negatiivisen myyntitilauksen tai palautustilauksen luominen.

    - **Vaatimuspäivä** – Valitse vaatimuksen päivämäärä. Oletusarvo on nykyinen päivämäärä.
    - **Vaatimuksen syy** – Valitse nykyiseen vähennykseen sisältyvä syykoodi. Valitsemasi vaatimusperuste vaikuttaa valittuihin asetuksiin. Lisätietoja tässä kohdassa valittavissa olevien vähennysten syiden luo ja konfiguroinnista on tämän artikkelin aiemmassa [Luo vähennyksen syyt](#deduction-reasons) -osassa.
    - **Huomautukset** – Lisää mahdolliset huomautukset. Kun vaatimus hyväksytään, hyväksyjä voi muokata tai lisätä vaatimuksen huomautuksia.
    - **Luo vaatimuskirjauskansio** – Valitsemalla tämän vaihtoehdon voit määrittää, luodaanko vaatimuskirjauskansio, kun vaatimus tai vähennys luodaan:

        - *Kyllä* – Järjestelmä luo ja kirjaa yleisen kirjauskansion käyttämällä **Myyntireskontran parametrit** -sivulla määritettyä vaatimuskirjauskansiota. (Lisätietoja on kohdassa [Määritä myyntireskontran ja vähennysten](#accounts-receivable-deductions) osa aiemmin tässä artikkelissa.) Kun lasku on liitetty vaatimukseen, vaatimuskirjauskansion avulla vähennetään sovellettavaa laskua. Jos vaatimus hylätään myöhemmin, hakemuskirjauskansio ja tilitys (jos lasku on liitetty) peruutetaan.
        - *Ei* – Tällä hetkellä ei luoda vaatimuskirjauskansiota. Se luodaan, kun vaatimus hyväksytään. Lasku voidaan vielä liittää uuteen vaatimukseen, vaikka vaatimuskirjauskansiota ei luoda. Selvitystä ei kuitenkaan voi tehdä ilman vaatimuskirjauskansiota.

1. Valitse **OK**.

    Uusi vähennys luodaan. Jos määrität **Luo vaatimuskirjauskansio** -asetuksen arvoksi *Kyllä*, seuraavat tapahtumat kirjataan:

    - **Kaksi uutta asiakastapahtumaa** – Yksi tapahtuma vastakirjaa vaatimuksen summan alkuperäistä laskua vastaan. Muut tapahtumat rekisteröivät asiakkaan velan vaatimuksen summaan, koska vaatimusta ei ole vielä hyväksytty. Alkuperäinen laskutapahtuma ja vastakirjausvaatimustapahtuma merkitään automaattisesti tilitykseen, kun liität laskun valitsemalla toimintoruudusta **Ylläpidä \> liitä lasku**.
    - **Kaksi vastatapahtumaa** – Nämä tapahtumat kirjataan **vähennyksen vastakirjanpito** -tilille.
    - **Vaatimuskirjauskansio** – Voit tarkastella kunkin vähennyksen työtilassa näkyvän vähennyksen kirjauskansiota valitsemalla **Viitteet**-välilehden. Vaatimuskirjauskansio näkyy **Kirjauskansion eränumero** -kentässä. Voit tarkastella vaatimuskirjauskansiota myös **Vähennystapahtumat**-välilehdessä. Siinä sen **päivitystyypin** arvo on *Täsmäytä*.

## <a name="create-a-credit-note-for-a-customer"></a>Luo asiakkaalle hyvityslasku

Kun asiakkaalle on myönnetty hyväksytty hyvitys, voit luoda hyvitysilmoituksen asiakkaan tilille hyvityksen esittämiseksi tarpeen mukaan. Kredit näkyy tämän jälkeen vähennyksen työtilassa, jossa se voidaan kohdistaa vähennykseen.

Voit luoda hyvityslaskun seuraavien ohjeiden avulla.

1. Valitse **Myynti ja markkinointi \> Asiakkaat \> Kaikki asiakkaat**.
1. Valitse asiakas.
1. Valitse toimintoruudun **Kerää**-välilehden **Selvitä**-ryhmässä **Selvitä tapahtumat**.
1. Valitse **Täsmäytä tapahtumat** -valintaikkunasta tapahtuma, johon ostohyvitys on kohdistettu.
1. Valitse Työkalurivin **Toiminnot**-valikosta ostohyvitysohjelman tyyppi.
1. Valitse **Ostohyvitys**-sivun **Yhteenveto**-välilehdestä ostohyvityksen tunnuksen vieressä oleva **Merkitse** valintaruutu.
1. Valitse toimintoruudusta **Toiminnot \> Luo hyvityslasku**.

## <a name="process-a-deduction-on-the-deduction-workbench"></a>Käsittele vähennys vähennyksen työtilassa

Vähennyksen työtilassa voit täsmäyttää vähennykset avoimien luottotapahtumien kanssa, jakaa vähennyksiä, kieltää vähennyksiä ja kirjata pois vähennyksiä.

Suorita yksi tai useampi seuraavien osioiden toimenpiteistä riippuen siitä, miten haluat käsitellä vähennyksen. Voit yhdistää toimenpiteet tarpeen mukaan. Voit esimerkiksi jakaa vähennyksen kahteen osaan ja täsmäyttää sitten yhden osan kreditiin mutta jättää jäljelle jäävän osan työpöydälle ja täsmäyttää sen myöhemmin toiseen kreditiin. Voit myös verrata vähennystä luottoon, joka on pienempi kuin vähennyksen summa, ja estää tai kirjata pois vähennyksen jäljellä olevan saldon.

### <a name="match-a-deduction-to-a-credit"></a>Täsmäytä vähennys hyvitykseen

Voit täsmäyttää vähennyksen saldoon noudattamalla seuraavia vaiheita.

1. Siirry kohtaan **Myynti ja markkinointi \> Kauppakorvaukset \> Vähennykset \> Vähennysten työtila**.
1. Valitse **Merkitse**-valintaruutu jokaisen käsiteltävän vähennyksen vierestä.
1. Valitse **Avoimet tapahtumat** -osassa vähennykseen täsmäytyksen hyvityksen **Merkitse**-valintaruutu. Jos luettelossa on useita hyvityksiä, voit valita niistä useita vastaamaan hyvitystä. Jos haluat, että järjestelmä valitsee automaattisesti vähennyksen summaa vastaavat hyvitykset, valitse sopiva vaihtoehto **Valitse vähennyssumma** -valikosta.
1. Valitse toimintoruudussa **Ylläpidä \> Täsmäytä**. Järjestelmä täsmäyttää vähennyksen kredit-arvoon. Jos saldo jää vähennykseen, se näkyy **Vähennykset**-välilehden **Jäljellä oleva summa** -kentässä.

    > [!NOTE]
    > Vähennyksille, jotka on luotu käyttämällä **Uusi vähennys** -komentoa vähennyksen työpöydällä, asiakkaan selvityksessä tai asiakassivulla, **Ylläpidä \> Täsmäytä** -komento on käytettävissä vain, jos **Vaatimuksen tila** -kentän arvoksi on asetettu *Hyväksytty*. Tämän komennon avulla voit täsmätä hinta- tai määräpohjaisen tapahtuman manuaalisesti siihen liittyvään hyvitykseen **Avoimet tapahtumat** -osassa. Tämä hyvitys luodaan joko vähennyksen hyväksymisen yhteydessä (käyttämällä **Ylläpidä \> Hyväksy vähennys** -komentoa) tai kun se on liitetty olemassa olevaan hyvitykseen, kuten on kuvattu tässä artikkelissa myöhemmin kohdassa [Hyväksytyn vähennysprosessin ulkopuolella luodut saldot](#credits-outside-approval). *Selvitä hyväksytyt vähennykset* -kausittainen tehtävä (**Myynnin markkinointi \> Kausittaiset tehtävät \> Selvitä hyväksytyt vähennykset**) -tehtävää voidaan käyttää myös niiden vähennysten ja hyvitysten automaattiseen täsmäyttämiseen, joissa on täsmäytyksen **Vähennystunnus**-arvot ja -summat.

### <a name="split-a-deduction"></a>Vähennyksen jakaminen

Jaa vähennys noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Myynti ja markkinointi \> Kauppakorvaukset \> Vähennykset \> Vähennysten työtila**.
1. Valitse **Merkitse**-valintaruutu jokaisen käsiteltävän vähennyksen vierestä.
1. Valitse toimintoruudussa **Ylläpidä \> Jaa**.
1. Kirjoita **Jaa**-valintaikkunan **Jaa summa** -kenttään päävähennyksestä jaettava summa. Valitse sitten **OK**.
1. Valitse **Vähennykset**-välilehdellä ilmoitus, jossa jaetun summan uusi tietue näkyy. Alkuperäinen vähennystietue sisältää muistutuksen vähennyksen saldosta. Voit nyt hallita alkuperäisen ostohyvityksen kahta osaa erikseen.
1. Valitse alkuperäinen vähennystietue ja valitse sitten **Viitteet**-välilehti. **Jakosumma**-kentässä näkyy summa, joka on jaettu alkuperäisestä summasta.

### <a name="attach-an-invoice-to-a-deduction"></a>Laskun liittäminen vähennykseen

Voit liittää laskun vähennykseen, jos vähennys on luotu **Uusi vähennys** -komennolla vähennyksen työtilassa, asiakastiliselvityksessä tai asiakassivulla ja jos siihen ei ole liitetty laskua (**lasku**-sarake on tyhjä).

Voit liittää laskun vähennykseen noudattamalla seuraavia vaiheita.

1. Siirry kohtaan **Myynti ja markkinointi \> Kauppakorvaukset \> Vähennykset \> Vähennysten työtila**.
1. Valitse **Merkitse**-valintaruutu jokaisen käsiteltävän vähennyksen vierestä.
1. Valitse toimintoruudussa **Ylläpidä \> Liitä lasku**.
1. Valitse **Laskun liittäminen** -valintaikkunasta lasku ja valitse **OK**.
1. Suorita **Tapahtumien selvittäminen** -valintaikkunassa jokin seuraavista vaiheista sen mukaan, kirjattiinko vaatimuskirjauskansio vähennyksen luomisen yhteydessä:

    - Jos vaatimuskirjauskansio on kirjattu, valitsemassasi laskussa ja vaatimuskirjauskansion asiakkaan hyvitystapahtumassa on valintamerkki **Merkitse**-sarakkeessa. Valitse **Kirjaa**. Liitetyn laskun jäljelle jäävästä saldosta vähennetään saatava summa.
    - Jos lunastamiskirjauskansiota ei ole kirjattu, **Merkitse**-sarakkeessa ei ole valintamerkkiä. Koska et voi vastakirjata vaatimuskirjauskansiota vastaan, ennen kuin vähennys on hyväksytty, valitse **Peruuta**.

### <a name="detach-an-invoice-from-a-deduction"></a>Laskun poistaminen vähennyksestä

Voit poistaa laskun vähennyksestä, jos vähennys on luotu **Uusi vähennys** -komennolla vähennyksen työtilassa, asiakastiliselvityksessä tai asiakassivulla ja jos siihen ei ole liitetty laskua (eli **Lasku**-sarakkeessa näkyy laskun numero) ja jos **Vaatimuksen tila** -kentän arvoksi on asetettu *Auki*. Saatat tehdä tämän tehtävän, koska siihen on liitetty väärä lasku. Lasku poistetaan vähennyksestä ja sen jäljellä oleva saldo päivitetään, jos sitä pienennettiin laskun ollessa liitettynä.

Poista lasku seuraavia ohjeita noudattamalla.

1. Siirry kohtaan **Myynti ja markkinointi \> Kauppakorvaukset \> Vähennykset \> Vähennysten työtila**.
1. Valitse **Merkitse**-valintaruutu jokaisen käsiteltävän vähennyksen vierestä.
1. Valitse toimintoruudussa **Ylläpidä \> Poista lasku**.

### <a name="approve-a-deduction"></a>Vähennyksen hyväksyminen

Voit hyväksyä vähennykset, jotka on luotu käyttämällä **Uusi vähennys** -komentoa vähennystyötilassa, asiakastilityksessä tai asiakassivulla. Voit kuitenkin hyväksyä vain vähennykset, joiden **Vaatimustila**-kentän arvoksi on määritetty *Avoin*.

Hyväksy vähennys noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Myynti ja markkinointi \> Kauppakorvaukset \> Vähennykset \> Vähennysten työtila**.
1. Valitse **Merkitse**-valintaruutu jokaisen käsiteltävän vähennyksen vierestä.
1. Valitse toimintoruudussa **Ylläpidä \> Hyväksy vähennys**.
1. Muokkaa tai lisää tarvittaessa tietoja **huomautuksen** arvoon **vähennyksen hyväksyminen** -valintaikkunassa.
1. Jos vähennys on hintapohjainen eikä siihen ole liitetty laskua, valitse nimikkeen arvonlisäveroryhmä. Tavallisesti veronimikeryhmä on määritetty laskussa. Veronimikekoodi on määritettävä, kun sitä ei ole liitetty laskuun.
1. Valitse **OK**.

    Tässä vaiheessa vähennystä ei voi enää muuttaa. Jos **Luo vaatimuskirjauskansio** -asetuksen arvoksi on asetettu *Ei*, kun vähennys luotiin, vaatimuskirjauskansio luodaan ja kirjataan, kun vähennys hyväksytään. Kun vähennys on hyväksytty, luotto luodaan ja avataan automaattisesti. Tyyppi määräytyy vähennyksen **vaatimusperusteen** arvon mukaan:

    - *Hintaperusteinen* – Jos vähennys perustuu hintaan, asiakastilille luodaan vapaatekstilasku. Voit lisätä kuvauksen ja kirjata hyvityksen. Vähennykset täytetään seuraavien kenttien perusteella, kun viestiluonnos luodaan:

        - **Vähennyksen tunnus** – Tämä kenttä lisätään ylätunnisteeseen, jotta vähennys voidaan ottaa uudelleen käyttöön.
        - **Päätili** – Arvo määräytyy vähennykseen liitetylle vähennyksen syylle määritetyn **vaatimuskirjaustilin** arvon mukaan.
        - **Nimikkeen arvonlisäveroryhmä** – Arvo määräytyy liitetyn laskun tai vähennyksen hyväksyessä valitsemasi arvon mukaan.
        - **Yksikköhinta** – Arvo on vähennyksen vaatimussumman hyvitys.
        - **Laskun teksti** – Oletusarvon mukaan tämän kentän arvoksi on määritetty vähennyksen **Huomautukset**-arvo.

    - *Määrä perustuu* – Jos vähennys perustuu määrään, luodaan avoin myyntitilaus tai palautustilaus. **[Myyntireskontran parametrit](#accounts-receivable-deductions)** -sivun **Luo palautustilaus** -asetus määrittää, luodaanko myyntitilaus vai palautustilaus, kun vähennys hyväksytään. Näkyviin tulee **Kopioi tilaukset** -sivu, joka suodatetaan näyttämään rivit, joilla **Laskutustili**-kentän arvoksi on määritetty vähennyksen asiakastili. Noudata näitä ohjeita:

        1. **Laskut**-pikavälilehden **Otsikot**-osassa näkyvät myyntilaskut, joissa **laskutustilin** arvo vastaa vähennyksen asiakastiliä. Valitse soveltuva myyntilasku.
        1. **Rivit**-osassa näkyvät valitun myyntilaskun rivit. Valitse jokaiselle kopioitavalle riville **Valitse**-valintaruutu. Vaihtoehtoisesti voit valita **Otsikot**-osasta kaikki sen rivit valitsemalla myyntitilauksen **Valitse kaikki** -valintaruudun.
        1. Oikaise yhden tai useamman rivin **Määrä**-arvo tarpeen mukaan.

            Kaikki tähän mennessä valitsemasi rivit näkyvät **Kopioitavat valitut rivit tai otsikot** -pikavälilehdellä.

        1. Toista tarvittaessa edelliset kaksi vaihetta, kunnes kaikki tarvittavat rivit näkyvät **Kopioitavat valitut rivit tai otsikot** -pikavälilehdellä.
        1. Valitse **OK**.

            Uusi palautustilaus avataan, ja seuraavat kentät määritetään automaattisesti:

            - **Vähennyksen tunnus** – Tämä kenttä lisätään ylätunnisteeseen, jotta vähennys voidaan ottaa uudelleen käyttöön.
            - **Palautuksen syykoodi** – Oletusarvon mukaan tässä kentässä on **palautuksen syykoodin** arvo, joka on määritetty vähennykselle määritetylle vähennyksen syylle.

Kun hyvitys on laskutettu, se näkyy vähennyksen työn **avointen tapahtumien** osassa suhteessa sovellettavaan **vähennystunnuksen** arvoon ja sen **vaatimustyyppi**-kenttään on määritetty *Muut hyvitykset*. Luotto on käytettävissä, kunnes se selvitetään vähennyksellä jo jollain seuraavista tavoista:

- Voit selvittää sen manuaalisesti valitsemalla toimintoruudusta **Ylläpidä \> täsmäytä**.
- Se selvitetään automaattisesti *Selvitä hyväksytyt vaatimukset* -kausityö (**Myynti ja markkinointi \> Kausittaiset tehtävät \> Selvitä hyväksytyt vaatimukset**).
- Tilitys selvitetään automaattisesti, koska **Myyntireskontran parametrit** -sivun **Tilitys**-välilehden **Automaattinen tilitys** -asetus on *Kyllä*.

Kun vähennys hyväksytään, luotua luottoa voi tarkastella myös vähennystyötilan **Avoimet tapahtumat** -osan **Avoin kredit** -painikkeella.

### <a name="create-a-return-order"></a>Palautustilauksen luominen

Voit luoda vähennyksiä varten palautustapahtuman, jotka on luotu käyttämällä **Uusi vähennys** -komentoa vähennystyötilassa, asiakastilityksessä tai asiakassivulla. Kaikkien seuraavien ehtojen on kuitenkin täytyttävä:

- **Vaatimusperuste**-kentän arvoksi määritetään *Määrään perustuva*.
- **Vaatimuksen tila** -kentän arvoksi määritetään *Avoin*.
- **[Myyntireskontran parametrit](#accounts-receivable-deductions)** -sivun **Vähennykset**-välilehden **Luo palautustilaus** -asetuksen arvona on *Kyllä*.
- **[Myyntireskontran parametrit](#accounts-receivable-deductions)** -sivun **Vähennykset**-välilehden **Luo palautustilaus ennen vähennyksen hyväksymistä** -asetuksen arvona on *Kyllä*.

Luo palautustilaus seuraamalla näitä ohjeita.

1. Siirry kohtaan **Myynti ja markkinointi \> Kauppakorvaukset \> Vähennykset \> Vähennysten työtila**.
1. Valitse **Merkitse**-valintaruutu jokaisen käsiteltävän vähennyksen vierestä.
1. Valitse toimintoruudussa **Ylläpidä \> Luo palautustilaus**.
1. Muokkaa **Vähennyksen hyväksyminen** -valintaikkunassa muokkaa tai lisää tietoja olemassa olevaan **Huomautukset**-arvoon tarpeen mukaan ja valitse sitten **OK**.
1. **Kopioi tilaukset** -valikkoruudussa, **Laskut**-pikavälilehden **Otsikot**-osassa näkyvät myyntilaskut, joissa **laskutustilin** arvo vastaa vähennyksen asiakastiliä. Valitse soveltuva myyntilasku.
1. **Rivit**-osassa näkyvät valitun myyntilaskun rivit. Valitse jokaiselle kopioitavalle riville **Valitse**-valintaruutu. Vaihtoehtoisesti voit valita **Otsikot**-osasta kaikki sen rivit valitsemalla myyntitilauksen **Valitse kaikki** -valintaruudun.
1. Oikaise yhden tai useamman rivin **Määrä**-arvo tarpeen mukaan.

    Kaikki tähän mennessä valitsemasi rivit näkyvät **Kopioitavat valitut rivit tai otsikot** -pikavälilehdellä.

1. Toista tarvittaessa edelliset kaksi vaihetta, kunnes kaikki tarvittavat rivit näkyvät **Kopioitavat valitut rivit tai otsikot** -pikavälilehdellä.
1. Valitse **OK**.

    Uusi palautustilaus avataan, ja seuraavat kentät määritetään automaattisesti:

    - **Vähennyksen tunnus** – Tämä kenttä lisätään ylätunnisteeseen, jotta vähennys voidaan ottaa uudelleen käyttöön.
    - **Palautuksen syykoodi** – Oletusarvon mukaan tässä kentässä on **palautuksen syykoodin** arvo, joka on määritetty vähennykselle määritetylle vähennyksen syylle.

### <a name="deny-a-deduction"></a>Vähennyksen hylkääminen

Hylkää vähennys noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Myynti ja markkinointi \> Kauppakorvaukset \> Vähennykset \> Vähennysten työtila**.
1. Valitse **Merkitse**-valintaruutu jokaisen käsiteltävän vähennyksen vierestä.
1. Valitse toimintoruudussa **Ylläpidä \> Hylkää**.
1. Valitse **Hylkää**-valintaikkunassa hylkäyksen syykoodi ja valitse sitten **OK**.
1. Valitse **Näytä**-kentästä toimintoruudun alapuolelta *Suljettu*.

    **Vähennykset**-välilehti näyttää vähennetyn vähennyksen ja **Vähennyksen jäljellä oleva määrä** -kentän vähennyksen arvoksi on asetettu *0,00*.

    Vähennyksille, jotka on luotu käyttämällä **Uusi vähennys** -komentoa vähennyksen työtilassa, asiakkaan selvityksessä tai asiakassivulla, tapahtuu seuraavat tapahtumat:

    - **Hylkäys**-osan kentät päivitetään **Viitteet**-välilehdessä.
    - Jos valitsit, että hakemuskirjauskansio luodaan vähennyksen luomisen yhteydessä ja jos laskun saldoa pienentävään vähennykseen on liitetty lasku, laskua lisätään ja aiemmin liitetyn laskun jäljellä oleva saldo kasvaa hylätyn laskun summalla.
    - Vähennyksen **Tila**-kentän arvoksi määritetään *Suljettu*.
    - Vähennyksen **Vaatimuksen tila**-kentän arvoksi määritetään *Hylätty*.

Peruuta hylkäys noudattamalla seuraavia ohjeita.

1. Valitse **Vähennykset**-välilehdessä hylätty vähennys.
1. Valitse toimintoruudussa **Peruuta hylkäys**.

    Vähennyksille, jotka on luotu käyttämällä **Uusi vähennys** -komentoa vähennyksen työtilassa, asiakkaan selvityksessä tai asiakassivulla, tapahtuu seuraavat tapahtumat:

    - **Hylkäys**-osan kentät päivitetään **Viitteet**-välilehdessä.
    - Vähennyksen **Tila**-kentän arvoksi määritetään *Avoin*.
    - Vähennyksen **Vaatimuksen tila**-kentän arvoksi määritetään *Avoin*.

### <a name="write-off-a-deduction"></a>Vähennyksen poiskirjaaminen

Kirjaa vähennys pois noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Myynti ja markkinointi \> Kauppakorvaukset \> Vähennykset \> Vähennysten työtila**.
1. Valitse **Merkitse**-valintaruutu jokaisen käsiteltävän vähennyksen vierestä.
1. Valitse toimintoruudussa **Ylläpidä \> poiskirjaa**.
1. Valitse **Poiskirjaa**-valintaikkunassa poiskirjauksen syykoodi ja valitse sitten **OK**.
1. Valitse **Näytä**-kentässä *Suljettu*.

    **Vähennykset**-välilehti näyttää poiskirjatun vähennyksen ja **Vähennyksen jäljellä oleva määrä** -kentän vähennyksen arvoksi on asetettu *0,00*.

    Vähennyksille, jotka on luotu käyttämällä **Uusi vähennys** -komentoa vähennyksen työtilassa, asiakkaan selvityksessä tai asiakassivulla, tapahtuu seuraavat tapahtumat:

    - **Poiskirjaus**-osan kentät päivitetään **Viitteet**-välilehdessä.
    - Jos olet luonut vaatimuskirjauskansion vähennyksen luomisen yhteydessä, vähennyksen poiston syykoodiin kirjataan vaatimuskirjauskansio. Voit tarkastella tätä merkintää **Vähennystapahtumat**-välilehdessä, jossa sen **Päivitystyypin** arvo on *Poiskirjaus*.
    - Vähennyksen **Tila**-kentän arvoksi määritetään *Suljettu*
    - Vähennyksen **Vaatimuksen tila**-kentän arvoksi määritetään *Poiskirjaus*.

Peruuta poiskirjaus noudattamalla seuraavia ohjeita.

1. Valitse **Vähennykset**-välilehdessä hylätty vähennys.
1. Valitse toimintoruudussa **Peruuta poiskirjaus**.

    Vähennyksille, jotka on luotu käyttämällä **Uusi vähennys** -komentoa vähennyksen työtilassa, asiakkaan selvityksessä tai asiakassivulla, tapahtuu seuraavat tapahtumat:

    - **Poiskirjaus**-osan kentät päivitetään **Viitteet**-välilehdessä.
    - Jos olet luonut vaatimuskirjauskansion vähennyksen luomisen yhteydessä, vähennyksen poiston syykoodiin kirjataan vaatimuskirjauskansio. Voit tarkastella tätä merkintää **Vähennystapahtumat**-välilehdessä, jossa sen **Päivitystyypin** arvo on *Peruuta poiskirjaus*.
    - Vähennyksen **Tila**-kentän arvoksi määritetään *Avoin*.
    - Vähennyksen **Vaatimuksen tila**-kentän arvoksi määritetään *Avoin*.

## <a name="credits-created-outside-the-approve-deduction-process"></a><a name="credits-outside-approval"></a>Vähennysprosessin ulkopuolella luodut hyvitykset

Tämä osa koskee vain vähennyksiin, jotka on luotu käyttämällä **Uusi vähennys** -komentoa vähennystyötilassa, asiakastilityksessä tai asiakassivulla.

Eri käyttäjät ovat jo luoneet vapaatekstilaskun, palautustilauksen tai negatiivisen myyntitilauksen asiakkaan vaatimusta varten **Hyväksy vähennys** -prosessin ulkopuolella. Kun vähennys hyväksytään vähennyksen työjärjestyksessä, järjestelmä luo automaattisesti toisen vapaatekstilaskun, palautustilauksen tai negatiivisen myyntitilauksen. Tässä osassa kuvaillaan, miten aiemmin luotuja saldoja hyvitetään hyvitykseen ennen vähennyksen hyväksymistä. Näin estät päällekkäiset hyvitykset.

### <a name="attach-a-credit-to-deduction"></a>Liitä hyvitettävä vähennys

Tässä osassa kuvataan, kuinka voit liittää hyvityksen vähennykseen luotosta.

Kun saldo on liitetty vähennykseen, luotua luottoa voi tarkastella myös vähennystyötilan **Avoimet tapahtumat** -osan **Avoin saldo** -painikkeella.

Kun hyvitys on laskutettu ja vähennys hyväksytty, saldo näkyy vähennyksen työn **avointen tapahtumien** osassa suhteessa sovellettavaan **vähennystunnuksen** arvoon ja sen **vaatimustyyppi**-kenttään on määritetty *Muut hyvitykset*.

#### <a name="attach-a-free-text-invoice-to-a-deduction"></a>Vapaatekstilaskun liittäminen vähennykseen

Voit liittää vapaatekstilaskun vähennykseen noudattamalla seuraavia vaiheita.

1. Siirry kohtaan **Myyntireskontra \> Laskut \> Kaikki vapaatekstilaskut**.
1. Valitse soveltuva lasku.
1. Valitse toimintoruudun **Lasku**-välilehdessä **Liitä saldo vähennykseen**. Tämä painike on saatavilla vain, jos vapaatekstimuotoisen laskun **Vähennystunnus** -kenttä on tyhjä. Tyhjä kenttä ilmaisee, että vapaatekstilaskua ei ole vielä liitetty vähennykseen.
1. **Liitä saldo vähennykseen** -sivulla voit valita *yhden* vähennyksen. Valittavissa ovat vain avoimet *hintaan perustuvat* vähennykset.
1. Valitse **OK**. **Vähennystunnus**-kenttä määritetään vapaatekstilaskun otsikossa.

#### <a name="attach-a-return-order-to-a-deduction"></a>Palautustilauksen liittäminen vähennykseen

Voit liittää palautustilauksen vähennykseen noudattamalla seuraavia vaiheita.

1. Valitse **Myyntireskontra \> Tilaukset \> Kaikki palautustilaukset**.
1. Valitse sovellettava vastaanotetun tai avoimen palautuskauppatavaran (RMA) numero.
1. Valitse toimintoruudun **Palautustilaus**-välilehdessä **Liitä saldo vähennykseen**. Tämä painike on saatavilla vain, jos palautustilauksen **Vähennystunnus** -kenttä on tyhjä. Tyhjä kenttä ilmaisee, että palautustilausta ei ole vielä liitetty vähennykseen.
1. **Liitä saldo vähennykseen** -sivulla voit valita *yhden* vähennyksen. Valittavissa ovat vain avoimet *määrään perustuvat* vähennykset.
1. Valitse **OK**. **Vähennystunnus**-kenttä määritetään palautustilauksen otsikossa.

#### <a name="attach-a-sales-order-to-a-deduction"></a>Myyntitilauksen liittäminen vähennykseen

Voit liittää myyntitilauksen vähennykseen noudattamalla seuraavia vaiheita.

1. Valitse **Myyntireskontra \> Tilaukset \> Kaikki myyntitilaukset**.
1. Valitse avoin, toimitettu tai laskutettu myyntitilaus.
1. Valitse toimintoruudun **Lasku**-välilehdessä **Liitä saldo vähennykseen**. Tämä painike on saatavilla vain, jos myyntitilauksen **Vähennystunnus** -kenttä on tyhjä. Tyhjä kenttä ilmaisee, että myyntitilausta ei ole vielä liitetty vähennykseen.
1. **Liitä vähennys** -sivulla voit valita *yhden* vähennyksen. Valittavissa ovat vain avoimet *määrään perustuvat* vähennykset.
1. Valitse **OK**. **Vähennystunnus**-kenttä määritetään myyntitilauksen otsikossa.

#### <a name="detach-a-deduction-from-a-credit"></a>Irrota vähennys saldosta

Jos vähennys on tehty virheellisesti, voit irrottaa sen saldosta. Kaikkien seuraavien ehtojen on kuitenkin täytyttävä:

- Vähennykseen liittyy hyvitys.
- **Vaatimuksen tila** -kentän arvoksi määritetään *Avoin*.

Jos haluat vähennyksen saldosta, valitse jokin seuraavista vaiheista hyvitystyypin mukaan:

- **Vapaatekstilaskut:** Valitse **Kaikki vapaatekstilaskut** -sivulla lasku. Valitse sitten toimintoruudun **Lasku**-välilehdessä **Poista saldo vähennyksestä**.
- **Palautustilaukset:** Valitse **Kaikki palautustilaukset** -sivulla tilaus. Valitse sitten toimintoruudun **Palautustilaus**-välilehdessä **Poista saldo vähennyksestä**.
- **Myyntitilaukset:** Valitse **Kaikki myyntitilaukset** -sivulla tilaus. Valitse sitten toimintoruudun **Lasku**-välilehdessä **Poista saldo vähennyksestä**.

### <a name="attach-a-deduction-to-a-credit"></a>Liitä vähennys hyvitykseen

Tässä osassa kuvataan, kuinka voit liittää vähennyksen hyvitykseen vähennyksestä.

#### <a name="attach-a-deduction-to-a-free-text-return-order-or-sales-order-credit"></a>Vähennyksen liittäminen vapaatekstiin, palautustilauksen tai myyntitilauksen hyvitykseen

Voit liittää vähennyksen vapaatekstiin, palautustilaukseen tai myyntitilauksen hyvitykseen seuraavalla tavalla.

1. Siirry kohtaan **Myynti ja markkinointi \> Kauppakorvaukset \> Vähennykset \> Vähennysten työtila**.
1. Valitse sovellettava avoin vähennys.
1. Valitse toimintoruudussa **Ylläpidä \> Liitä vähennys saldoon**. Tämä painike on käytettävissä vain, jos **Vaatimus-tila** -kentän arvoksi on määritetty *Avoin*.
1. **Liitä saldo** -sivulla voit valita *yhden* saldon. Näytettä olevien hyvitysten tyyppi määräytyy vähennyksen **Vaatimusperuste** -arvon mukaan:

    - *Hintaperusteinen* – Sivulla näkyvät sen asiakastilin vapaatekstilaskut, jonka **vähennystunnus**-kenttä on tyhjä. Asiakkaan ehdotukset näkyvät myös, koska vapaatekstilasku voi olla kirjaamaton. Sen vuoksi sillä ei välttämättä ole numeroa, joksi siinä viitataan.
    - *Määräperuste* – Näkyvissä olevan hyvityksen tyyppi määräytyy **[Myyntireskontran parametrit](#accounts-receivable-deductions)** -sivulla olevan **Luo palautustilaus** -asetuksen asetusten mukaan:

        - *Kyllä* – Sivulla näkyvät sen asiakastilin palautustilaukset, jonka **vähennystunnus**-kenttä on tyhjä.
        - *Ei* – Sivulla näkyvät sen asiakastilin myyntitilaukset, jonka **vähennystunnus**-kenttä on tyhjä.

1. Valitse **OK**. **Vähennystunnus**-kenttä määritetään saldon otsikossa.

Kun saldo on liitetty vähennykseen, luotua luottoa voi tarkastella myös vähennystyötilan **Avoimet tapahtumat** -osan **Avoin saldo** -painikkeella.

Kun hyvitys on laskutettu ja vähennys hyväksytty, saldo näkyy vähennyksen työn **avointen tapahtumien** osassa suhteessa sovellettavaan **vähennystunnuksen** arvoon ja sen **vaatimustyyppi**-kenttään on määritetty *Muut hyvitykset*.

#### <a name="detach-a-credit-from-the-deduction"></a>Irrota saldo vähennyksestä

Jos saldoon tehty virheellisesti, voit irrottaa sen vähennyksestä. Valitse sitten toimintoruudun **ylläpidä**-ryhmässä **Poista vähennys saldosta**. **Vähennystunnuksen** arvo poistetaan saldohyvityksestä.

**Poista hyvitys saldosta** -painike on käytössä vain, jos seuraavat ehdot täyttyvät:

- Vähennykseen liittyy hyvitys.
- **Vaatimuksen tila** -kentän arvoksi määritetään *Avoin*.

## <a name="create-a-one-time-promotion"></a>Kertaluonteisen korotuksen luominen

Joskus sinulla ei ehkä ole hyväksyttyä ostohyvitystä, jonka voisit täsmäyttää vähennyksen kanssa. Tässä tapauksessa voit käyttää *kertaluonteinen korotus* -ominaisuutta vähennyksen täsmäyttämiseksi asiakkaaseen liitetyn myynninedistämispalkkion kanssa. *Kertaluonteinen korotus* -toiminto luo uuden myynninedistämispalkkiosopimuksen ja kokonaissumman myynninedistämistapahtumalle. Se täsmäyttää kokonaissumman tämän jälkeen vähennykseen ja suorittaa kirjaukset, jotka vaaditaan vähennyksen sulkemiseen.

Tämä ominaisuus on hyödyllinen, jos käytät myynninedistämispalkkioita. Lisätietoja myynninedistämispalkkiosta on kohdassa [myynninedistämispalkkion hallinta](../sales-marketing/trade-allowance.md).

Ensin on asetettava malli, jota voidaan käyttää uuden myynninedistämispalkkiosopimuksen luomiseen. Määritä malli noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Myynti ja markkinointi \> Myynninedistämispalkkiot \> Mallit**.
1. Valitse toimintoruudussa **Uusi**.
1. Syötä kenttiin tiedot, joiden tulee näkyä mallista luoduissa sopimuksissa.
1. Valitse **Asiakkaat**-pikavälilehden **Hierarkia**-kentästä hierarkiataso.
1. Valitse hierarkialuettelosta asiakas, jolla ei ole vähennystä, ja valitse sitten oikea nuolipainike (**\>**). Asiakas lisätään **Myynninedistämispalkkiosopimuksen asiakkaat**-luetteloon.
1. Määritä muut kentät tarpeen mukaan ja sulje sitten sivu.
1. Siirry kohtaan **Myynti ja markkinointi \> Asetuksiin \> Myynninedistämispalkkio \> Myynninedistämispalkkioiden hallintaparametrit**.
1. Valitse **Yhteenveto**-välilehden **Kertaluonteinen tarjousmalli** -kentästä kerta-alennusten luomiseen käytettävä mallin nimi.

Seuraavaksi voit luoda kertaluonteisen kampanjan vähennyksen työtilassa. Luo kertaluonteisen kampanjan seuraavien ohjeiden avulla.

1. Siirry kohtaan **Myynti ja markkinointi \> Kauppakorvaukset \> Vähennykset \> Vähennysten työtila**.
1. Valitse **Merkitse**-valintaruutu käsiteltävän vähennyksen vierestä.
1. Valitse toimintoruudusta **Ylläpidä \> Selvitä vähennys kertaluonteisena tarjouksena**.
1. Liitä vähennys yhteen tai useampiin varoihin **kertaluontoisen myynninedistämisen** valintaikkunassa seuraavasti:

    1. Valitse **Uusi**, ja sitten **Rahoitustunnus**-kentässä valitse rahoitustunnus. Toista tämä vaihe lisätäksesi niin monta rahastoa kuin on tarpeen.
    1. Valitse **Prosentti**-kentässä kunkin rahaston tunnuksen vieressä kirjoita rahastoon kohdistettava vähennyksen prosenttiosuus. **Prosentti**-kenttiin kirjoittamiesi summien tulee olla yhteensä 100 prosenttia.

1. Valitse **OK**. Järjestelmä luo uuden myynninedistämispalkkiosopimuksen, jossa markkinointitapahtuman kokonaissumma ja täsmäyttää kokonaissumman vähennykseen.

## <a name="do-a-mass-update-of-deductions"></a>Suorita vähennysten laajamittainen päivitys

Jos sinun täytyy tehdä sama muutos useisiin vähennyksiin, voit valita ne vähennykset ja tehdä joukkopäivityksen kentissä.

Tee joukkopäivitys seuraavia ohjeita noudattamalla.

1. Siirry kohtaan **Myynti ja markkinointi \> Kauppakorvaukset \> Vähennykset \> Vähennysten työtila**.
1. Valitse **Näytä**-kentässä toimintoruudun alapuolelta voit tarkastella vähennyksien tyyppiä.
1. Valitse valintaruutu jokaisen päivitettävän vähennyksen vierestä. Valitse sitten toimintoruudussa **Ylläpidä \> Päivitä joukkona**.
1. **Joukkopäivitys**-valintaikkunassa näkyvät valitut vähennykset. Päivitä kentät tarpeen mukaan ja hyväksy muutokset valitsemalla **OK**.
