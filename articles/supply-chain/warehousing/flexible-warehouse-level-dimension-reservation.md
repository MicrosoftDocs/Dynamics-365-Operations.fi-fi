---
title: Joustava varastotason dimensionvarauskäytäntö
description: Tässä ohjeaiheessa kuvataan varaston varauskäytäntö, joka mahdollistaa eräseurattuja tuotteita myyville ja niiden logistiikan varastonhallintajärjestelmän toiminnoilla toteuttaville yrityksille tiettyjen erien varaamisen asiakkaiden myyntitilauksille, vaikka tuotteiden varaushierarkia ei salli tiettyjen erien varausta.
author: omulvad
manager: AnnBe
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: c0baf96315dd9fe6bc1984d337fd1c50ae47016a
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/07/2020
ms.locfileid: "3031040"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a>Joustava varastotason dimensionvarauskäytäntö

[!include [banner](../includes/banner.md)]

Kun Erä alla\[sijainti\]-tyyppinen varastonvaraushierarkia yhdistetään tuotteisiin, eräseurattuja tuotteita myyvät ja niiden logistiikan Microsoft Dynamics 365 -varastonhallintajärjestelmävalmiilla (WMS) toiminnoilla toteuttavat yritykset eivät voi varata tiettyjä kyseisten tuotteiden eriä asiakkaiden myyntitilauksille. Tässä ohjeaiheessa kuvataan varastonvarauskäytäntö, jonka avulla nämä yritykset varaavat tiettyjä eriä, vaikka tuotteet on yhdistetty Erä alla\[sijainti\]-varaushierarkiaan.

## <a name="inventory-reservation-hierarchy"></a>Varastovaraushierarkia

Tässä osassa on yhteenveto olemassa olevasta varastonvaraushierarkiasta. Se keskittyy tapaan, jolla erä- ja sarjaseurattuja kohteita käsitellään.

Varastonvaraushierarkia määrää, että varastodimensioiden osalta kysyntätilaus sisältää pakolliset dimensiot toimipaikka, varasto ja varastotila. Varastologiikka taas vastaa sijainnin osoittamisesta pyydetyille määrille ja kyseisen sijainnin varaamisesta. Toisin sanoen kysyntätilauksen ja varastotoimintojen välisissä vuorovaikutuksissa kysyntätilauksen oletetaan ilmaisevan, mistä tilaus on lähetettävä (eli mistä toimipaikasta ja varastosta). Tämän jälkeen varasto tukeutuu logiikkaan löytääkseen vaaditun määrän varastotilasta.

Yrityksen toimintamallin heijastamista varten seurantadimensiot (erä- ja sarjanumerot) ovat joustavampia. Varastonvaraushierarkia voi mukautua seuraavankaltaisiin tilanteisiin:

- Yritys käyttää varastotoimintojaan hallitsemaan sellaisten määrien keräilemiseen, joilla on erä- tai sarjanumerot, sen jälkeen, kun määrät on löydetty varaston säilytystilasta. Tätä mallia kutsutaan usein nimellä *Erä alla\[sijainti\]*. Sitä käytetään yleensä silloin, kun tuotteen erä- tai sarjanumeron tunnistus ei ole tärkeä asiakkaille, jotka tekevät pyynnön myyjäyritykselle.
- Jos erä- tai sarjanumerot ovat osa asiakkaan tilausmääritystä ja ne tallennetaan kysyntätilaukseen, varastotoiminnot, jotka etsivät määrät varastosta, rajoitetaan tiettyihin pyydettyihin numeroihin, joita ei voi muuttaa. Tätä mallia kutsutaan nimellä *Erä yllä\[sijainti\]*.

Näissä skenaarioissa haasteena on, että kullekin vapautetulle tuotteelle voidaan määrittää vain yksi varastonvaraushierarkia. Siksi, jotta varastonhallintajärjestelmä määrittäisi hierarkian määrittämisen jälkeen, milloin erä- tai sarjanumero pitäisi varata (joko kun kysyntätilaus saadaan tai varaston keräilytyön aikana), kyseistä ajoitusta ei voi muuttaa tilannekohtaisesti.

## <a name="flexible-reservation-for-batch-tracked-items"></a>Eräseurattujen nimikkeiden joustava varaus

### <a name="business-scenario"></a>Liiketoimintaskenaario

Tässä skenaariossa yritys käyttää varastostrategiaa, jossa valmiita tavaroita seurataan eränumeroiden avulla. Yritys käyttää myös varastonhallinnan työkuormitusta. Koska tässä työkuormituksessa on hyvin toimiva logiikka varaston keräily- ja lähetystoimintojen suunnittelulle ja suorittamiselle erämääräisiä nimikkeitä varten, useimmille valmiille nimikkeille määritetään Erä alla\[sijainti\] -varastonvaraushierarkia. Tällaisen operatiivisen määrityksen etuna on, että päätöksiä (jotka ovat käytännössä varauspäätöksiä) siitä, mitkä erät kerätään ja mihin ne laitetaan varastossa, lykätään siihen asti, että varastoin keräilytoiminnot alkavat. Niitä ei tehdä, kun asiakkaan tilaus saadaan.

Vaikka Erä alla\[sijainti\] -varaushierarkia palvelee yrityksen liiketoimintatavoitteita hyvin, monet yrityksen vakiintuneista asiakkaista tarvitsevat aikaisemmin ostamansa erää, kun ne tilaavat tuotteita uudelleen. Siksi yritys etsii joustavuutta erävaraussääntöjen käsittelyyn, jotta asiakkaan samaa nimikettä koskevasta kysynnästä riippuen, tapahtuu seuraavaa:

- Eränumero voidaan kirjata ja varata, kun myynninkäsittelijä vastaanottaa tarjouksen, eikä sitä voi muuttaa varastotoimintojen aikana ja/tai osoittaa muille kysynnöille. Tämä auttaa takaamaan, että tilattu eränumero toimitetaan asiakkaalle.
- Jos eränumerolla ei ole merkitystä asiakkaalle, varastotoiminnot voivat määrittää eränumeron keräilyn aikana, kun myyntitilauksen kirjaus ja varaus on tehty.

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a>Tietyn erän myyntilaukselle varaamisen mahdollistaminen

Jotta haluttu erävarauksen joustavuus mahdollistetaan nimikkeille, joilla on Erä alla\[sijainti\] -varastonvaraushierarkia, varastopäällikköjen on valittava **Salli varaus kysyntätilauksessa** -valintaruutu **Eränumero** -tasolla sivulla **Varastonvaraushierarkiat**.

![Varastovarausten hierarkian joustavoittaminen](media/Flexible-inventory-reservation-hierarchy.png)

Kun hierarkian **Eränumero**-taso on valittuna, kaikki kyseisen tason yläpuolella olevat dimensiot aina **Sijainti**-tasolle valitaan automaattisesti. (Oletusarvoisesti kaikki **Sijainti**-tason yläpuolella olevat dimensiot on esivalittu.) Tämä toiminta perustuu logiikkaan, jossa myös kaikki eränumeron ja sijainnin välisen alueen dimensiot varataan automaattisesti, kun varaat tietyn eränumeron tilausrivillä.

> [!NOTE]
> **Salli varaus kysyntätilauksessa** -valintaruutu pätee vain varaushierarkiatasoille, jotka ovat varastosijainnin dimension alapuolella.
>
> **Eränumero** on hierarkian ainoa taso, johon joustavaa varauskäytäntöä voi soveltaa. Toisin sanoen et voi valita **Salli varaus kysyntätilauksessa** -valintaruutua tasoille **Sijainti**, **Rekisterikilpi** tai **Sarjanumero**.
>
> Jos varaushierarkia sisältää sarjanumerodimension (jonka on aina oltava **Eränumero**-tason alapuolella) ja jos olet ottanut eräkohtaisen varauksen käyttöön eränumerolle, järjestelmä jatkaa sarjanumeroiden varaus- ja keräilytoimintojen käsittelyä niiden sääntöjen perusteella, jotka pätevät Sarja alla\[sijainti\] -varauskäytäntöön.

Voit missä tahansa vaiheessa ottaa eräkohtaisenvarauksen käyttöön olemassa olevalle Erä alla\[sijainti\] -varaushierarkialle ympäristössäsi. Tämä muutos ei vaikuta varauksiin ja avoimiin varastotöihin, jotka on luotu ennen muutosta. **Salli varaus kysyntätilauksessa** -valintaruutua ei kuitenkaan voi tyhjentää, jos varasto-ottotyypin **Varattu tilattu**, **Varattu fyysinen** tai **Tilattu** varastotapahtumia on olemassa vähintään yhteen kyseessä olevaan varaushierarkiaan liittyvän nimikkeen osalta.

> [!NOTE]
> Jos nimikkeen käytössä oleva varaushierarkia ei salli erän määritystä tilauksessa, voit siirtää sen varaushierarkiaan, joka sallii erän määrityksen, kunhan hierarkiatasorakenne on sama molemmissa hierarkioissa. Tee siirto toiminnolla **Muuta nimikkeiden varaushierarkiaa**. Tästä muutoksesta voi olla hyötyä, kun haluat estää eräseurattujen nimikkeiden alijoukon joustavan erävarauksen, mutta sallia sen muun tuoteportfolion osalta.

Riippumatta siitä, oletko valinnut **Salli varaus kysyntätilauksessa** -valintaruudun, jos et halua varata nimikkeelle tiettyä eränumeroa tilausrivillä, oletusarvoinen varastotoimintologiikka, jota sovelletaan Erä alla\[sijainti\] -varaushierarkiaan, pätee edelleen.

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a>Tietyn eränumeron varaaminen asiakastilausta varten

Kun eräseuratun nimikkeen Erä alla\[sijainti\] -varastonvaraushierarkia on määritetty sallimaan tiettyjen eränumeroiden varaaminen myyntitilauksissa, myyntitilausten käsittelijät voivat ottaa saman nimikkeen asiakastilauksia vastaan jollakin seuraavista tavoista asiakkaan pyynnöstä riippuen:

- **Anna tilaustiedot ilman eränumeron määritystä** – Tätä menetelmää kannattaa käyttää, kun tuotteen erämääritys ei ole tärkeä asiakkaalle. Kaikki aiemmin luodut prosessit, jotka liittyvät tällaisen tilauksen käsittelyyn, eivät muutu. Käyttäjiltä ei vaadita lisätoimia.
- **Anna tilaustiedot ja varaa tietty eränumero** – Tätä menetelmää kannattaa käyttää, kun asiakas pyytää tiettyä erää. Yleensä asiakkaat pyytävät tiettyä erää, kun he tilaavat uudelleen aiemmin ostamaansa tuotetta. Tällaista eräkohtaisia varausta kutsutaan nimellä *eräsidonnainen varaus*.

Seuraavat säännöt ovat voimassa, kun käsitellään määriä ja tietylle tilaukselle on määritetty eränumero:

- Jotta tietyn eränumeron varaaminen nimikkeelle olisi mahdollista Erä alla\[sijainti\] -varauskäytännössä, järjestelmän on varattava kaikki dimensiot aina sijaintiin asti. Tähän väliin kuuluu yleensä myös rekisterikilpidimensio.
- Sijaintidirektiivejä ei käytetä, kun keräilytyö luodaan myyntiriville, jossa käytetään tilaussidonnaista eränvarausta.
- Tilaussidonnaisiin eriin kohdistuvan työn varastokäsittelyn aikana käyttäjä tai järjestelmä ei voi muuttaa eränumeroa. (Tämä käsittely sisältää poikkeuksen käsittelyn.)

Seuraavassa esimerkissä työnkulku näkyy kokonaisuudessaan.

## <a name="example-scenario"></a>Esimerkkiskenaario

Esittelytietojen on oltava asennettuna tätä esimerkkiä varten, ja sinun on käytettävä esittelytietojen **USMF**-yritystä.

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a>Varastonvaraushierarkian määrittäminen sallimaan eräkohtainen varaus

1. Siirry kohtaan **Varastonhallinta** \> **Määritys** \> **Varasto \> Varaushierarkia**.
2. Valitse **Uusi**.
3. Anna nimi **Nimi**-kentässä (esim. **EräFlex**).
4. Anna kuvaus **Kuvaus**-kentässä (esim. **Erä joustavan alla**).
5. Valitse **Valittu**-kentässä **Sarjanumero** ja **Omistaja** ja siirrä ne sitten **Käytettävissä**-kenttään vasemman nuolipainikkeen avulla.
6. Valitse **OK**.
7. Valitse **Eränumero** -dimension tasolla valintaruutu **Salli varaus kysyntätilauksessa**. Tasot **Rekisterikilpi** ja **Sijainti** valitaan automaattisesti eikä niiden valintaruutuja voi tyhjentää.
8. Valitse **Tallenna**.

### <a name="create-a-new-released-product"></a>Uuden julkaistun tuotteen luominen

1. Määritä tuotteen kolme päätietoparametria käyttämällä seuraavia arvoja:

    - Valitse **Varastodimensioryhmä**-kentässä **Tavara**.
    - Valitse **Seurantadimensioryhmä**-kentässä **Erä-fyy**.
    - Valitse **Varaushierarkia** -kentässä **EräFlex**.

2. Luo kaksi eränumeroa, kuten**B11** ja **B22**.
3. Lisää nimekemääriä käytettävissä olevaan varastoon seuraavien arvojen avulla.

    | Varasto | Eränumero | Toimipaikka | Rekisterikilpi | Määrä |
    |-----------|--------------|----------|---------------|----------|
    | 24        | B11          | BULK-001 | Ei ole          | 10       |
    | 24        | B11          | FL-001   | LP11          | 10       |
    | 24        | B22          | FL-002   | LP22          | 10       |

### <a name="enter-sales-order-details"></a>Syötä myyntitilaustiedot

1. Siirry kohtaan **Myynti ja markkinointi** \> **Myyntitilaukset** \> **Kaikki myyntitilaukset**.
2. Valitse **Uusi**.
3. Syötä myyntitilausotsikon **Asiakastili**-kenttään **US-003**.
4. Lisää rivi uutta nimikettä varten ja syötä määräksi **10**. Varmista, että **Varasto**-kentän arvo on **24**.
5. Valitse **Myyntitilausrivit** -pikavälilehdessä **Varasto** ja sitten **Ylläpidä**-ryhmässä **Erävaraus**. **Erävaraus**-sivulla näkyy luettelo eristä, jotka voidaan varata tilausrivillä. Tässä esimerkissä määränä on **20** eränumerolle **B11** ja **10** eränumerolle **B22**. Huomaa, että **Erävaraus**-sivua ei voi käyttää riviltä, jos rivin nimikkeelle on määritetty Erä alla\[sijainti\] -varaushierarkia, ellei sitä ole määritetty sallimaan eräkohtaista varausta.

    > [!NOTE]
    > Varataksesi ostotilaukselle tietyn erän sinun on käytettävä **Erävaraus** -sivua.
    >
    > Jos syötät eränumeron suoraan myyntitilausriville, järjestelmä toimii siten kuin olisit syöttänyt tietyn eräarvon nimikkeelle, johon sovelletaan Erä alla\[sijainti\] -varauskäytäntöä. Kun tallennat rivin, näyttöön tulee varoitussanoma. Jos vahvistat, että eränumero on määritettävä suoraan tilausrivillä, tavanomainen varastonhallintalogiikka ei käsittele kyseistä riviä.
    >
    > Jos varaat määrän **Varaus**-sivulta, tiettyä erää ei varata ja rivin osalta sovelletaan varastotoimintojen suorittamiseen niitä sääntöjä, joita sovelletaan Erä alla\[sijainti\] -varastokäytännön mukaan.

    Yleensä tämä sivu toimii ja siihen sovelletaan samaa vuorovaikutusta kuin silloin, kun asianomaisille nimikkeille on määritetty Erä yllä\[sijainti\] -tyyppinen varaushierarkia. Seuraavat poikkeukset kuitenkin pätevät:

    - **Lähderiville sidotut eränumerot** -pikavälilehdessä näkyvät tilausriville varatut eränumerot. Ruudukon eräarvot näkyvät koko tilausrivin toteutusjakson aikana, varaston käsittelyvaiheet mukaan luettuna. **Yhteenveto**-pikavälilehdessä ruudukossa sen sijaan näkyy tavanomainen tilausrivin varaus (eli **Sijainti**-tason yläpuoleisille dimensioille tehtävä varaus) aina siihen asti, kun varastotyö luodaan. Tämän jälkeen rivinvaraus siirtyy työyksikölle, eikä rivinvaraus enää ole näkyvissä sivulla. **Lähderiviin sidotut eränumerot** -pikavälilehti auttaa sen varmistamisessa, että myyntitilausten käsittelijä näkee asiakkaan tilaukseen missä tahansa sen elinkaaren aikana aina laskutukseen asti sidotut eränumerot.
    - Tietyn erän varauksen lisäksi käyttäjä voi valita erän sijainnin ja rekisterikilven manuaalisesti sen sijaan, että se antaisi järjestelmän valita ne automaattisesti. Tämä ominaisuus liittyy tilaussidonnaisen erävarausmekanismin rakenteeseen. Kuten aiemmin mainittiin, kun nimikkeelle varataan eränumero Erä alla\[sijainti\] -varauskäytännössä, järjestelmän on varattava kaikki dimensiot aina sijaintiin asti. Tämän vuoksi varastotyössä käytetään tilauksia käsitelleiden käyttäjien varaamia varastodimensioita, eivätkä ne aina välttämättä vastaa nimikkeen kätevää tai edes mahdollista varastointipaikkaa keräilytoimintoja varten. Jos tilausten käsittelijät ovat tietoisia varaston rajoituksista, heidän saattaa kannattaa valita sijainnit ja rekisterikilvet manuaalisesti, kun he varaavat erää. Tällöin käyttäjän on käytettävä **Näytä dimensiot** -toimintoa sivun otsikossa ja lisättävä sijainti ja rekisterikilpi **Yhteenveto**-pikavälilehden ruudukkoon.

6. Valitse **Erävaraus**-sivulla erän **B11** rivi ja sitten **Varaa rivi**. Sijaintien ja rekisterikilpien määritykselle ei ole omaa logiikkaansa automaattisen varauksen aikana. Voit syöttää määrän manuaalisesti **Varaus**-kenttään. Huomaa, että **Lähderiviin sidotut eränumerot**-pikavälilehdessä erän **B11** arvona on **Sidottu**.

    ![Tietyn eränumeron sitominen myyntitilausriviin erävaraussivulla](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > Myyntitilausrivin määrä voidaan varata eri eristä. Myös samaa erää voidaan varata useiden sijaintien ja rekisterikilpien perusteella (jos rekisterikilvet on sallittu sijainneille).
    >
    > Tietyn erän varaaminen myyntitilausrivin määrälle voi olla myös osittaista. Esimerkiksi 100 yksikön kokonaismäärä voidaan varata siten, että tietty erä on sidottu 20 yksikköön, kun taas 80 yksikköä varataan toimipaikka- ja varastotasolla mistä tahansa käytettävissä olevasta erästä. Tässä tapauksessa varastonhallintajärjestelmä käsittelee keräilytoiminnot käyttäen kahta erillistä työriviä.

7. Siirry kohtaan **Tuotetietojen hallinta** \> **Tuotteet** \> **Vapautetut tuotteet**. Valitse nimikkeesi ja sitten **Hallitse varastoa** \> **Näytä** \> **Tapahtumat**.

    ![Tilaussidonnainen varaus varastotapahtumatyyppinä](media/Inventory-transactions-for-order-committed-reservation.png)

8. Tarkista nimikkeen varastotapahtumat, jotka liittyvät myyntitilausrivin varaukseen.

    - Tapahtuma, jossa **Viite**-kentän arvona on **Myyntitilaus** ja **Varasto-otto**-kentän arvona **Varattu fyysinen**, edustaa varausrivin varausta **Sijainti**-tason yläpuolella olevien dimension osalta. Nimikkeen varastonvaraushierarkian mukaan nämä dimensiot ovat toimipaikka, varasto ja varastotila.
    - Tapahtuma, jossa **Viite**-kentän arvona on **Tilaussidonnainen varaus** ja **Varasto-otto**-kentän arvona **Varattu fyysinen**, edustaa varausrivin varausta määritetyn erän ja kaikkien sen yläpuolella olevien dimensioiden osalta. Nimikkeen varastonvaraushierarkian mukaan nämä dimensiot ovat eränumero ja sijainti. Tässä esimerkissä sijainti on **Bulk-001**.

9. Valitse myyntitilauksen otsikossa **Varasto** \> **Toiminnot** \> **Vapauta varastoon**. Tilausrivi on nyt aallotettu, ja kuormitus ja työ luodaan.

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a>Niiden varastotöiden tarkistus ja käsittely, joilla on tilaussidonnaisia eränumeroita

1. Valitse **Myyntitilausrivit**-pikavälilehdessä **Varasto** \> **Työn tiedot**.

    Työllä, joka käsittelee myyntitilausriviin sidottujen erämäärien keräilytoiminnon, on seuraavat ominaisuudet:

    - Järjestelmä käyttää työn luomisessa työmalleja, mutten sijaintidirektiivejä. Kaikkia työmalleille määritettyjä vakioasetuksia, kuten keräilyrivien tai tietyn mittayksikön enimmäismäärää, käytetään sen määrittämisessä, milloin uusi työ luodaan. Keräilysijaintien tunnistamisen sijaintidirektiiveihin liittyviä sääntöjä ei kuitenkaan oteta huomioon, koska tilaussidonnaisessa varauksessa määritetään jo kaikki varastodimensiot. Nämä varastodimensiot sisältävät varastosäilytystason dimensiot. Siten työ perii kyseiset dimensiot ilman sijaintidirektiivien käyttöä.
    - Eränumeroa ei näytetä keräilyrivillä (kuten työrivillä, joka luodaan nimikkeelle, johon liittyy Erä yllä\[sijainti\]-varaushierarkia). Sen sijaan kohteesta-eränumero ja kaikki muut varastodimensiot näkyvät työrivin työvarastotapahtumassa, joka perustuu tähän liittyviin varastotapahtumiin.

        ![Varaston varastotapahtuma töille, jotka perustuvat tilaussidonnaiseen varaukseen](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - Kun työ on luotu, nimikkeen varastotapahtuma, jossa **Viite**-kentän arvona on **Tilaussidonnainen varaus**, poistetaan. Varastotapahtuma, jossa **Viite**-kentän arvona on **Työ**, sisältää nyt kaikkien määrän varastodimensioiden fyysisen varauksen.

        Varastotoiminnot voivat seuraavaksi suorittaa työt tavanomaiseen tapaan. Mobiililaitteen ohjeet kuitenkin ohjeistavat työntekijää keräilemään tiettyä eränumeroa. Varastoympäristöissä, joissa sijainteja hallitaan rekisterikilvillä, työntekijä voi keräillä mistä tahansa vielä varaamattomasta rekisterikilvestä (jota ei siis ole varattu toiselle tilaussidonnaiselle varaukselle tai työlle, joka perustuu tällaiselle varaukselle), kun hän saapuu sijainnille, jossa säilytetään samaa erää useissa rekisterikilvissä.

        Jos on epäkäytännöllistä keräillä työrivillä määritetystä sijainnista, varasto-operaattorit voivat käyttää jotakin seuraavista toiminnoista tietyn erän keräilyn siirtämiseen kätevämpään sijaintiin:

        - Vakiomuotoinen mobiililaitteen **Ohita toiminto** (jos varastotyöntekijän **Salli keräilysijainnin ohitus** -asetus on käytössä)
        - **Muuta sijaintia** -toiminto **Työluettelon tiedot** -sivulla. 

2. Lopeta työn keräily ja hyllytys mobiililaitteella.

    Eränumeroa **B11** on nyt kerätty määrä **10** myyntitilausriviä varten ja siirretty sijaintiin **Lastauspaikan ovi**. Tässä vaiheessa se on valmis lastattavaksi kuorma-autoon ja lähetettäväksi asiakkaan osoitteeseen.

## <a name="exception-handling-of-warehouse-work-thas-has-order-committed-batch-numbers"></a>Niiden varastotöiden poikkeustenkäsittely, joilla on tilaussidonnaiset eränumerot

Tilaussidonnaisten eränumeroiden keräilyn varastotyöhön sovelletaan samoja varaston poikkeustenkäsittelyä ja -toimintoja kuin tavanomaiseen työhön. Yleisesi ottaen avoin työ tai työrivi voidaan peruuttaa, se voidaan keskeyttää, koska käyttäjän sijainti on täynnä, siihen voidaan soveltaa lyhyttä keräilyä ja sitä voidaan päivittää siirron vuoksi. Samoin jo valmiiksi saatua keräiltyä työmäärää voidaan vähentää tai työ voidaan palauttaa.

Kaikkiin näihin poikkeusten käsittelyn toimintoihin sovelletaan seuraavaa keskeistä sääntöä: asiakkaalle varattua eränumeroa ei voi koskaan korvata toisella eränumerolla, mutta sen varastodimensioita (sijainti ja rekisterikilpi) voi muuttaa joko käyttäjän manuaalisella päivityksellä tai järjestelmän automaattisella päivityksellä. Automaattinen päivitys perustuu samaan varastodimensioiden satunnaiseen määrittämiseen, jota käytetään, kun tietty erä varataan automaattisesti mutta varastodimensioita ei määritetä.

### <a name="example-scenario"></a>Esimerkkiskenaario

Esimerkki tästä skenaariosta on tilanne, jossa aiemmin valmistuneiden töiden keräily perutaan **Vähennä keräiltyä määrää** -toimintoa. Tämä esimerkki jatkaa tämän aiheen edellistä esimerkkiä.

1. Siirry kohtaan **Varastonhallinta** \> **Kuormat** \> **Aktiiviset kuormat**.
2. Valitse kuorma, joka on luotu myyntitilauksen lähetyksen yhteydessä.
3. Valitse **Kuormatilauksen rivit** -pikavälilehdestä **Vähennä keräiltyä määrää**.
4. Valitse **Vähennä keräiltyä määrää** -sivun **Siirrä sijaintiin** -kentässä **FL-001**.
5. Valitse **Siirrä rekisterikilvelle**-kentässä **LP33**.
6. Syötä **Peruttava keräilty varastomäärä** -kenttään arvo **10**.
7. Valitse **OK**.

Tässä ovat keräilyn perumisen tulokset:

- Aiemmin suljetun työn tilaksi määritetään **Peruttu**.
- Uusi **Varastonsiirto**-tyypin työ luodaan varastomäärälle **10** eränumerossa **B11**. Tämä työ edustaa siirtoa sijainnista **Lastauspaikan ovi** rekisterikilvelle **LP33** sijainnissa **FL-001**. Tilaksi määritetään **Suljettu**.
- Järjestelmä varaa uudelleen alun perin tilatun eränumeron ja määrittää sijainnin ja rekisterikilpitunnukset. (Tämä prosessi vastaa **Vara rivi** -toiminnon suorittamista tietyn eränumeron tilausriville). Tämän tuloksena erä **B11** näkyy sidottuna **Lähderiville sidotut eränumerot** -pikavälilehdessä sivulla **Erävaraus** ja **Varaus**-kentässä on määrä **10** eränumeron **B11** osalta. Lisäksi **Sijainti**-kentän arvona on **FL-001** ja **Rekisterikilpi**-kentän arvona on **LP11**. (Voit lisätä nämä kentät ruudukkoon, jos ne eivät ole näkyvissä.)

Seuraavissa taulukoissa on yhteenveto siitä, miten järjestelmä käsittelee tiettyjen varastotoimintojen tilaussidonnaisen erävarauksen. Taulukkojen sisältöä tulkitaan olettamalla, että kukin varastotoiminnon suorittamiseen liittyy olemassa oleva tilaussidonnaiseen erävaraukseen perustuvaa työ tai että kunkin varastotoiminnon suorittaminen vaikuttaa kyseisentyyppiseen työhön.

> [!NOTE]
> Näissä taulukoissa Erämäärä on käytettävissä -sarake ilmaisee, onko varastomäärää käytettävissä sen määrän lisäksi, joka on jo varattu kulloisillekin tilaussidonnaisille varauksille tai joka on varattu kyseisentyyppisiin varauksiin perustuvassa varastotyössä.

#### <a name="override-the-pick-location-on-the-open-work"></a>Avoimen työn keräilysijainnin ohitus

<table>
<thead>
<tr>
<th>Keskeiset määritysparametrit</th>
<th>Erämäärä on käytettävissä</th>
<th>Keskeiset käyttäjän vaiheet</th>
<th>Varastotyö</th>
<th>Tilaussidonnainen erävaraus</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><strong>Salli keräilysijainnin ohitus</strong> -asetus on käytössä työntekijällä.</td>
<td>Kyllä</td>
<td>
<ol>
<li>Valitse valikkovaihtoehto <strong>Ohita sijainti</strong> varaston mobiilisovelluksessa (WMA), kun aloitat keräilytyön.</li>
<li>Valitse <strong>Ehdota</strong>.</li>
<li>Vahvista uusi sijainti, jota ehdotetaan erämäärän käytettävyyden perusteella.</li>
</ol>
</td>
<td>Seuraavat toiminnot tapahtuvat kulloisessakin työssä:
<ul>
<li>Keräilyrivin sijainniksi päivittyy uusi sijainti. (Jos sijainti on rekisterikilpihallittu, työvarastotapahtumalle määritetään satunnainen rekisterikilpi ja työntekijä voi keräillä mistä tahansa rekisterikilvestä, jossa määrää on käytettävissä.)</li>
<li>Jos määrää on uuden sijainnin useassa rekisterikilvessä, alkuperäinen keräilyrivi jaetaan useaan riviin, jotka vastaavat kutakin rekisterikilpeä.</li>
</ul>
</td>
<td>Ei käytettävissä</td>
</tr>
<tr>
<td>Ei</td>
<td>
<ol>
<li>Valitse valikkovaihtoehto <strong>Ohita sijainti</strong> varaston WMA:ssa, kun aloitat keräilytyön.</li>
<li>Määritä sijainti manuaalisesti.</li>
</ol>
</td>
<td><strong>Ohita sijainti</strong> -toiminto ei ole mahdollinen. Se epäonnistuu, ja ilmenee virhe.</td>
<td>Ei käytettävissä</td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a>Täysi-painike – Työrivin jakaminen käyttäjän sijainnin ylivuodon vuoksi

<table>
<thead>
<tr>
<th>Keskeiset määritysparametrit</th>
<th>Erämäärä on käytettävissä</th>
<th>Keskeiset käyttäjän vaiheet</th>
<th>Varastotyö</th>
<th>Tilaussidonnainen erävaraus</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Salli työn jakaminen</strong> -asetus on käytössä mobiililaitteen valikkovaihtoehdossa.</td>
<td>Ei käytettävissä</td>
<td>
<ol>
<li>Valitse valikkovaihtoehto <strong>Täysi</strong> varaston WMA:ssa, kun käsittelet keräilytyötä.</li>
<li>Syötä <strong>Keräilymäärä</strong>-kenttään tarvittavan keräilyn osamäärä ilmaisemaan täyttä kapasiteettia.</li>
</ol>
</td>
<td>
<ul>
<li>Kulloisessakin työssä määrä päivitetään vastaamaan jäljellä olevaa keräiltävää määrää.</li>
<li>Keräillylle määrälle luodaan uusi työ ja se suljetaan.</li>
</ul></td>
<td>Ei käytettävissä</td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a>Valmiin työn keräillyn määrän vähentäminen (kuormasta)

<table>
<thead>
<tr>
<th>Keskeiset määritysparametrit</th>
<th>Erämäärä on käytettävissä</th>
<th>Keskeiset käyttäjän vaiheet</th>
<th>Varastotyö</th>
<th>Tilaussidonnainen erävaraus</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Ei käytettävissä</td>
<td>Kyllä</td>
<td>
<ol>
<li>Avaa <strong>Vähennä keräiltyä määrää</strong> -sivu kuormariviltä.</li>
<li>Syötä sen määrän kokonaisarvo, jonka keräily perutaan.</li>
<li>Valitse "siirto kohteeseen" sijainti/rekisterikilpi.</li>
</ol>
</td>
<td>
<ul> 
<li>Kuormariviin liittyvä työ perutaan.</li>
<li>Varastosiirrolle luodaan uusi työ ja se suljetaan.</li>
</ul>
</td>
<td>Määrä varataan uudelleen samalle erälle. Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</td>
</tr>
<tr>
<td>Ei</td>
<td>Katso edellinen rivi.</td>
<td>Katso edellinen rivi.</td>
<td>Määrä varataan uudelleen samalle erälle ja samalle sijainnille ja rekisterikilvelle (jos sijainti on rekisterikilpihallittu), jotka on syötetty keräilyn perumisen yhteydessä.</td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a>Nimikkeen siirtäminen varastossa

> [!NOTE]
> Tätä varastotoimintoa voidaan soveltaa vain **Työnluontiprosessi**-tyypin siirtoihin, ei mallin mukaiseen siirtoon.

<table>
<thead>
<tr>
<th>Keskeiset määritysparametrit</th>
<th>Erämäärä on käytettävissä</th>
<th>Keskeiset käyttäjän vaiheet</th>
<th>Varastotyö</th>
<th>Tilaussidonnainen erävaraus</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><strong>Salli työhön liitetyn varaston siirto</strong> -asetus on käytössä työntekijällä.</td>
<td>Kyllä</td>
<td>
<ol>
<li>Aloita siirto WMA:lla.</li>
<li>Anna kohteesta- ja kohteeseen-sijainnit.</li>
</ol></td>
<td>
<ul>
<li>Kaikissa olemassa olevissa töissä, joihin siirto vaikuttaa, keräilysijainniksi päivitetään uusi kohteeseen-sijainti.</li>
<li>Varastosiirrolle luodaan uusi työ ja se suljetaan.</li>
</ul>
</td>
<td>Kaikki aiemmin luodut varaukset, joihin kyseisestä sijainnista suoritettava määränsiirto vaikuttaa, varataan uudelleen samalle erälle. Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</td>
</tr>
<tr>
<td>Ei</td>
<td>Katso edellinen rivi.</td>
<td>Katso edellinen rivi.</td>
<td>Kaikki aiemmin luodut varaukset, joihin kyseisestä sijainnista suoritettava määränsiirto vaikuttaa, varataan uudelleen samalle erälle ja uudelle kohteeseen-sijainnille ja rekisterikilvelle (jos sijainti on rekisterikilpihallittu).</td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a>Valmiin työn keräillyn määrän palauttaminen (kuormasta tai aallosta)

<table>
<thead>
<tr>
<th>Keskeiset määritysparametrit</th>
<th>Erämäärä on käytettävissä</th>
<th>Keskeiset käyttäjän vaiheet</th>
<th>Varastotyö</th>
<th>Tilaussidonnainen erävaraus</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'>Ei käytettävissä</td>
<td>Kyllä</td>
<td>
<ol>
<li>Avaa <strong>Työn palautus</strong> -sivu.</li>
<li>Valitse pyyntösivulla vaihtoehto <strong>Jätä nimikkeet nykyiseen sijaintiin</strong>.</li>
</ol>
</td>
<td>Kaikki tähän Kuormariviin liittyvät työt perutaan.</td>
<td>Määrä varataan uudelleen samalle erälle. Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</td>
</tr>
<tr>
<td>Ei</td>
<td>Katso edellinen rivi.</td>
<td>Katso edellinen rivi.</td>
<td>Määrä varataan uudelleen samalle erälle sekä sijainnille ja rekisterikilvelle, joihin määrä jätettiin palautuksen yhteydessä.</td>
</tr>
<tr>
<td>Kyllä</td>
<td>
<ol>
<li>Avaa <strong>Työn palautus</strong> -sivu.</li>
<li>Valitse pyyntösivulla vaihtoehto <strong>Osoita nimikkeet tähän sijaintiin</strong>.</li>
</ol>
</td>
<td>
<ul>
<li>Nykyinen työ perutaan.</li>
<li>Varastosiirrolle luodaan uusi työ ja se suljetaan.</li>
</ul>
</td>
<td>Määrä varataan uudelleen samalle erälle. Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</td>
</tr>
<tr>
<td>Ei</td>
<td>Katso edellinen rivi.</td>
<td>Katso edellinen rivi.</td>
<td>Määrä varataan uudelleen samalle erälle sekä sijainnille ja rekisterikilvelle, joihin määrä osoitettiin palautuksen yhteydessä.</td>
</tr>
<tr>
<td>Kyllä/ei</td>
<td>
<ol>
<li>Avaa <strong>Työn palautus</strong> -sivu.</li>
<li>Valitse pyyntösivulla vaihtoehto <strong>Siirrä nimikkeet tähän sijaintiin</strong>.</li>
</ol>
</td>
<td>Palautusta ei tueta.</td>
<td>Ei käytettävissä</td>
</tr>
<tr>
<td>Kyllä/ei</td>
<td>
<ol>
<li>Avaa <strong>Työn palautus</strong> -sivu.</li>
<li>Valitse pyyntösivulla vaihtoehto <strong>Siirrä nimikkeet sijaintidirektiivien perusteella</strong>.</li>
</ol>
</td>
<td>Palautusta ei tueta. </td>
<td>Ei käytettävissä</td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a>Määrän lyhytkeräily – Rekisteröi määrä fyysisesti löytymättömäksi sijainnista/rekisterikilvestä, kun keräilytyötä suoritetaan

<table>
<thead>
<tr>
<th>Keskeiset määritysparametrit</th>
<th>Erämäärä on käytettävissä</th>
<th>Keskeiset käyttäjän vaiheet</th>
<th>Varastotyö</th>
<th>Tilaussidonnainen erävaraus</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Määritetään <strong>Lyhyt keräily</strong> -tyypin poikkeus, jossa <strong>Nimikkeen uudelleenosoitus</strong> = <strong>Ei mitään</strong>, <strong>Varaston oikaisu</strong> = <strong>Kyllä</strong> ja <strong>Poista varaukset</strong> = <strong>Ei</strong>.</td>
<td>Kyllä</td>
<td>
<ol>
<li>Valitse valikkovaihtoehto <strong>Lyhyt keräily</strong> varaston WMA:ssa, kun suoritat keräilytyötä.</li>
<li>Kirjoita <strong>Keräilymäärä</strong>-kenttään <strong>0</strong> (nolla).</li>
<li>Kirjoita <strong>Syy</strong>-kenttään <strong>Ei uudelleenosoitusta</strong>.</li>
</ol>
</td>
<td>
<ul>
<li>Olemassa oleva työ suljetaan ja keräiltävä määrä on 0 (nolla).</li>
<li><strong>Inventointi</strong>-tyypin ja <strong>Myyty</strong>-tyypin varasto-ottotyyppi luodaan edustamaan oikaisua.</li>
</ul>
</td>
<td>Määrä varataan uudelleen samalle erälle. Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</td>
</tr>
<tr>
<td>Ei</td>
<td>Katso edellinen rivi.</td>
<td>
<ul>
<li>Lyhyt keräilytoiminto epäonnistuu ja ilmenee virhe.</li>
<li>Olemassa oleva työ pysyy avoimena.</li>
</ul>
</td>
<td>Ei käytettävissä</td>
</tr>
<tr>
<td rowspan='2'>Määritetään <strong>Lyhyt keräily</strong> -tyypin poikkeus, jossa <strong>Nimikkeen uudelleenosoitus</strong> = <strong>Ei mitään</strong>, <strong>Varaston oikaisu</strong> = <strong>Kyllä</strong> ja <strong>Poista varaukset</strong> = <strong>Kyllä</strong>.</td>
<td>Kyllä</td>
<td>
<ol>
<li>Valitse valikkovaihtoehto <strong>Lyhyt keräily</strong> varaston WMA:ssa, kun suoritat keräilytyötä.</li>
<li>Kirjoita <strong>Keräilymäärä</strong>-kenttään <strong>0</strong> (nolla).</li>
<li>Kirjoita <strong>Syy</strong>-kenttään <strong>Ei uudelleenosoitusta</strong>.</li>
</ol>
</td>
<td>
<ul>
<li>Olemassa oleva työ suljetaan ja keräiltävä määrä on 0 (nolla).</li>
<li><strong>Inventointi</strong>-tyypin ja <strong>Myyty</strong>-tyypin varasto-ottotyyppi luodaan edustamaan oikaisua.</li>
</ul>
</td>
<td>Kaikki aiemmin luodut varaukset, joihin lyhytkeräilyn sijainnin määräoikaisu vaikuttaa, varataan uudelleen samalle erälle. Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</td>
</tr>
<tr>
<td>Ei</td>
<td>Katso edellinen rivi.</td>
<td>Katso edellinen rivi.</td>
<td>Kaikki aiemmin luodut varaukset, joihin lyhytkeräilyn sijainnin määräoikaisu vaikuttaa, poistetaan.</td>
</tr>
<tr>
<td>Määritetään <strong>Lyhyt keräily</strong> -tyypin poikkeus, jossa <strong>Nimikkeen uudelleenosoitus</strong> = <strong>Manuaalinen</strong>, <strong>Varaston oikaisu</strong> = <strong>Kyllä</strong> ja <strong>Poista varaukset</strong> = <strong>Ei/Kyllä</strong>. Lisäksi <strong>Salli manuaalinen nimikkeiden uudelleenkohdistus</strong> -asetus on käytössä työn tekijän kohdalla.</td>
<td>Kyllä</td>
<td>
<ol>
<li>Valitse valikkovaihtoehto <strong>Lyhyt keräily</strong> varaston WMA:ssa, kun suoritat keräilytyötä.</li>
<li>Kirjoita <strong>Lyhyesti keräiltävä määrä</strong>-kenttään <strong>0</strong> (nolla).</li>
<li>Valitse <strong>Syy</strong>-kentässä <strong>Lyhytkeräily ja manuaalinen uudelleenkohdistus</strong>.</li>
<li>Valitsee sijainti/rekisterikilpi luettelosta.</li>
</ol>
</td>
<td>
<ul>
<li>Seuraavat toiminnot tapahtuvat kulloisessakin työssä:
<ul>
<li>Keräilyrivi suljetaan ja keräiltävä määrä on 0 (nolla).</li>
<li>Hyllytysrivi perutaan.</li>
<li>Uusi keräilyrivi luodaan. Siinä käytetään käyttäjän valitsemaa sijaintia/rekisterikilpeä.</li>
<li>Uusi hyllytysrivi luodaan.</li>
</ul>
</li>
<li><strong>Inventointi</strong>-tyypin ja <strong>Myyty</strong>-tyypin varasto-ottotyyppi luodaan edustamaan oikaisua.</li>
</ul>
</td>
<td>Ei käytettävissä</td>
</tr>
<tr>
<td>Määritetään <strong>Lyhyt keräily</strong> -tyypin poikkeus, jossa <strong>Nimikkeen uudelleenosoitus</strong> = <strong>Manuaalinen</strong>, <strong>Varaston oikaisu</strong> = <strong>Kyllä</strong> ja <strong>Poista varaukset</strong> = <strong>Ei</strong>. Lisäksi <strong>Salli manuaalinen nimikkeiden uudelleenkohdistus</strong> -asetus on käytössä työn tekijän kohdalla.</td>
<td>Ei</td>
<td>
<ol>
<li>Valitse valikkovaihtoehto <strong>Lyhyt keräily</strong> varaston WMA:ssa, kun suoritat keräilytyötä.</li>
<li>Kirjoita <strong>Lyhyesti keräiltävä määrä</strong>-kenttään <strong>0</strong> (nolla).</li>
<li>Valitse <strong>Syy</strong>-kentässä <strong>Lyhytkeräily ja manuaalinen uudelleenkohdistus</strong>.</li>
</ol>
</td>
<td>Lyhyt keräilytoiminto epäonnistuu ja ilmenee virhe.</td>
<td>Ei käytettävissä</td>
</tr>
<tr>
<td>Määritetään <strong>Lyhyt keräily</strong> -tyypin poikkeus, jossa <strong>Nimikkeen uudelleenosoitus</strong> = <strong>Manuaalinen</strong>, <strong>Varaston oikaisu</strong> = <strong>Kyllä</strong> ja <strong>Poista varaukset</strong> = <strong>Kyllä</strong>. Lisäksi <strong>Salli manuaalinen nimikkeiden uudelleenkohdistus</strong> -asetus on käytössä työn tekijän kohdalla.</td>
<td>Ei</td>
<td>
<ol>
<li>Valitse valikkovaihtoehto <strong>Lyhyt keräily</strong> varaston WMA:ssa, kun suoritat keräilytyötä.</li>
<li>Kirjoita <strong>Lyhyesti keräiltävä määrä</strong>-kenttään <strong>0</strong> (nolla).</li>
<li>Valitse <strong>Syy</strong>-kentässä <strong>Lyhytkeräily ja manuaalinen uudelleenkohdistus</strong>.</li>
<li>Valitsee sijainti/rekisterikilpi luettelosta.</li>
</ol>
</td>
<td>
<ul>
<li>Seuraavat toiminnot tapahtuvat kulloisessakin työssä:
<ul>
<li>Keräilyrivi suljetaan ja keräiltävä määrä on 0 (nolla).</li>
<li>Hyllytysrivi perutaan.</li>
</ul>
</li>
<li><strong>Inventointi</strong>-tyypin ja <strong>Myyty</strong>-tyypin varasto-ottotyyppi luodaan edustamaan oikaisua.</li>
</ul>
</td>
<td>Kaikki aiemmin luodut varaukset, joihin lyhytkeräilyn sijainnin/rekisterikilven määräoikaisu vaikuttaa, poistetaan.</td>
</tr>
<tr>
<td>Määritetään <strong>Lyhyt keräily</strong> -tyypin poikkeus, jossa <strong>Nimikkeen uudelleenosoitus</strong> = <strong>Automaattinen</strong>, <strong>Varaston oikaisu</strong> = <strong>Kyllä/Ei</strong> ja <strong>Poista varaukset</strong> = <strong>Kyllä/Ei</strong>.</td>
<td>Ei käytettävissä</td>
<td>
<ol>
<li>Valitse valikkovaihtoehto <strong>Lyhyt keräily</strong> varaston WMA:ssa, kun suoritat keräilytyötä.</li>
<li>Kirjoita <strong>Lyhyesti keräiltävä määrä</strong>-kenttään <strong>0</strong> (nolla).</li>
<li>Valitse <strong>Syy</strong>-kentässä <strong>Lyhytkeräily ja automaattinen uudelleenkohdistus</strong>.</li>
</ol>
</td>
<td>Lyhtykeräilyä, johon liittyy automaattinen uudelleenkohdistus, ei tueta.</td>
<td>Lyhtykeräilyä, johon liittyy automaattinen uudelleenkohdistus, ei tueta.</td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a>Muuta varaston tilaa

> [!NOTE]
> Tämä varastotoiminto voidaan suorittaa useista aloituskohdista. Tässä näkyvässä esimerkissä käytetään **Varaston tilanmuutos** -toimintoa **Käytettävissä sijainnin mukaan** -sivulla.

<table>
<thead>
<tr>
<th>Keskeiset määritysparametrit</th>
<th>Erämäärä on käytettävissä</th>
<th>Keskeiset käyttäjän vaiheet</th>
<th>Varastotyö</th>
<th>Tilaussidonnainen erävaraus</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><strong>Varasto</strong>-tietueen <strong>Varasto</strong>-välilehden <strong>Poista varaukset ja merkinnät</strong> -kentän arvo muuttuu muotoon <strong>Varaukset</strong> tai <strong>Merkinnät ja varaukset</strong>.</td>
<td>Kyllä</td>
<td>
<ol>
<li>Valitse tietty sijainti.</li>
<li>Valitse rivi, jolla on tietty nimike, sijainti ja rekisterikilpi (jos sijainti on rekisterikilpihallittu).</li>
<li>Valitse <strong>Varaston tilanmuutos</strong>.</li>
<li>Määritä <strong>Varastotila</strong>-kentän arvoksi <strong>Esto</strong>.</li>
</ol>
</td>
<td>Varaston tilanmuutokset eivät ole sallittuja määrille, jotka on varattu työlle.</td>
<td>
<ul>
<li>Määrä varataan uudelleen samalle erälle. Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</li>
<li>Kaksi tyypin <strong>Varaston tilanmuutos</strong> varastotapahtumaa luodaan edustamaan muutosta varastotiladimensiossa.</li>
<li><strong>Varastoesto</strong>-tyypin varastotapahtuma ja varasto-ottotyyppi <strong>Varattu fyysinen</strong> luodaan edustamaan estetyn määrän varausta.</li>
</ul>
</td>
</tr>
<tr>
<td>Ei</td>
<td>Katso edellinen rivi.</td>
<td>Varaston tilanmuutokset eivät ole sallittuja määrille, jotka on varattu työlle.</td>
<td>
<ul>
<li>Varaus poistetaan.</li>
<li>Kaksi tyypin <strong>Varaston tilanmuutos</strong> varastotapahtumaa luodaan edustamaan muutosta varastotiladimensiossa.</li>
<li><strong>Varastoesto</strong>-tyypin varastotapahtuma ja varasto-ottotyyppi <strong>Varattu fyysinen</strong> luodaan edustamaan estetyn määrän varausta.</li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><strong>Varasto</strong>-tietueen <strong>Varasto</strong>-välilehden <strong>Poista varaukset ja merkinnät</strong> -kentän arvo muuttuu muotoon <strong>Ei mitään</strong>.</td>
<td>Kyllä</td>
<td>
<ol>
<li>Valitse tietty sijainti.</li>
<li>Valitse rivi, jolla on tietty nimike, sijainti ja rekisterikilpi (jos sijainti on rekisterikilpihallittu).</li>
<li>Valitse <strong>Varaston tilanmuutos</strong>.</li>
<li>Määritä <strong>Varastotila</strong>-kentän arvoksi <strong>Esto</strong>.</li>
</ol>
</td>
<td>Varaston tilanmuutokset eivät ole sallittuja määrille, jotka on varattu työlle.</td>
<td>Määrä varataan uudelleen samalle erälle. Järjestelmä määrittää satunnaisesti sijainnin ja rekisterikilven (jos sijainti on rekisterikilpihallittu), joissa määrä on käytettävissä.</td>
</tr>
<tr>
<td>Ei</td>
<td>Katso edellinen rivi.</td>
<td>Varaston tilanmuutokset eivät ole sallittuja määrille, jotka on varattu työlle.</td>
<td>Varastotilan muutokset eivät ole sallittuja.</td>
</tr>
</tbody>
</table>

## <a name="limitations"></a>Rajoitukset

- Joustava varastotason dimensionvaraustoiminto ei tue seuraavia ominaisuuksia:

    - Todellisen painon hallinta
    - Fyysinen negatiivinen varasto
    - Varaus tilatun tarjonnan perusteella
    - Siirtotilaukset ja raaka-aineiden keräily

- Kontin direktiiviyksiköittäin pakkaamisen konsolidointisäännöllä on rajoituksia. Tilaussidonnaisten varausten osalta suosittelemme välttämää sellaisten kontinrakennusmallien käyttöä, joissa **Pakkaa direktiiviyksiköittäin** -kenttä on käytössä. Nykyisessä ratkaisussa sijaintidirektiivejä ei käytetä varastotyön luonnin yhteydessä. Siksi vain yksikön sarjaryhmän alinta yksikköä (varastoyksikköä) käytetään konttiinpakkauksen aaltovaiheen aikana.
