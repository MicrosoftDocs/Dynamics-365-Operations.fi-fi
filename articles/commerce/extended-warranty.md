---
title: Laajennettujen takuiden luominen ja määrittäminen
description: Tässä artikkelissa on tietoja laajennetuista takuista sekä niiden luomisesta ja määrittämisestä Microsoft Dynamics 365 Commercessa.
author: josaw1
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 3754de54763be52c9090596fac0e170b0c5fc520
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268365"
---
# <a name="create-and-configure-extended-warranties"></a>Laajennettujen takuiden luominen ja määrittäminen

[!include [banner](includes/banner.md)]

Tässä artikkelissa on tietoja laajennetuista takuista sekä niiden luomisesta ja määrittämisestä Microsoft Dynamics 365 Commercessa.

## <a name="overview"></a>Yleiskuvaus

Asiakkaat valitsevat tuotteita ostaessaan enenevässä määrin laajennetun tuen ja laajennetut palvelut etenkin, jos on kyse kuluttajatuotteiden, kuten puhelimien ja tietokoneiden, premiun-hintaluokan tuotteista. Tarjoamalla oston yhteyden laajennettuja takuita, jälleenmyyjät voivat luoda asiakasuskollisuutta. Laajennetun takuun ansiosta asiakkaat tietävät, mistä he saavat huoltoa ja tukea. Tämän vuoksi he luottavat siihen, että ongelmat käsitellään tehokkaasti.

Laajennettuja takuita voidaan myydä asiakkaille vähittäismyyntikanavassa tuotteen oston yhteydessä. Niitä voidaan myydä myös rajoitetun ajan oston jälkeen.

### <a name="warranty-item-setup"></a>Takuunimikkeen määrittäminen

Dynamics 365 Commercessa toimintoja, joilla voi luoda takuunimikkeen ja lisätä siihen määritteitä. Nämä määrittävät sisältävät tuotteen ja takuunimikkeen välisen liitoksen, takuun hinnan ja takuun keston. Kun takuunimike on määritetty ja vapautettu organisaatioyksikköön, jälleenmyyjä voi myydä takuita Modern Point of Salen (MPOS), verkkokaupan ja muiden vähittäismyyntikanavien kautta.

### <a name="warranty-item-sales"></a>Takuunimikkeen myynti

Laajennettuja takuita myydään vähittäismyyntikanavassa tuotteen oston yhteydessä. Niitä voidaan myydä myös rajoitetun ajan oston jälkeen.

Myyntipisteessä myyjää kehotetaan lisäämään laajennettu takuu, kun liittyvä tuote lisätään asiakkaan ostoskoriin. Tällä tavoin myyjä saa lisä- tai ristiinmyyntimahdollisuus myyntityönkulun osana.

Asiakkaat voivat myös palata myöhemmin ostamaan laajennetun takuun tuotteelle, jonka he ovat ostaneet aiemmin. Näissä tapauksissa myyjä voi hakea alkuperäisen tapahtuman ja myyjä asiakkaalle liittyvän laajennetun takuunimikkeen.

### <a name="warranty-terminology"></a>Takuusanastoa

Seuraavassa taulukossa on joidenkin takuuaiheisten termien määritelmät.

| Kausi | kuvaus |
|------------------------------|--------------|
| Laajennettu takuu / takuu | *Laajennettu takuu* viittaa huoltosopimukseen tai sopimukseen, joka tarjoaa asiakkaille pidennetyn takuun. Laajennettu takuu sisältää lisäpalvelun, jonka mukaan tuotteet vaihdetaan tai korjataan laajennetun takuun voimassaolon aikana. |
| Valmistajan takuu | *Valmistajan takuu* (jota kutsutaan usein *rajoitetuksi takuuksi*) on takuu, jonka asiakkaat saavat ostaessaan tuotteen. Valmistajan takuun ominaisuuksia:<ul><li>Takuukustannukset sisältyvät tuotteen hintaan. Asiakkaiden ei tarvitse maksaa erikseen valmistajan takuusta.</li><li>Tuoteluokan perusteella valmistajan takuun kesto on yleensä 30 päivää, kuusi kuukautta tai yksi vuosi. (Kuluttajaelektroniikan takuun kesto on useimmissa tapauksissa yksi vuosi.)</li><li>Takuu kattaa kaikki viat, joiden syy on mekaaninen vika tai sähkövika. Kattavuus on rajallinen eikä se sisällä mitään ostetulle tuotteelle vahingoissa aiheutunutta vahinkoa. Asiakkaat, jotka haluavat suojata ostamansa tuotteen tavanomaisilta vaurioilta, kannattaa hankkia laajennettu takuu. Laajennetun takuun kesto on tuoteluokan mukaan kahdesta kymmeneen vuoteen. Lisäksi niiden kattavuus on laajempi, ja ne kattavat tavanomaiset vahingot, kuten putoamisesta, nesteiden roiskumisesta ja tahriintumisesta johtuvat vauriot.</li></ul> |
| Takuunimike | *Takuunimike* on laajennettu takuunimike, joka myydään takuunalaiselle nimikkeelle. Sellainen on esimerkiksi kannettavien tietokoneiden kahden vuoden vahinkosuoja. |
| Takuunalainen nimike | *Takuunalainen nimike* on sarjoitettu tuote, jolle takuu myydään. Esimerkiksi kannettava tietokone takuunalainen nimike, jolle myydään kahden ja kolmen vuoden laajennettuja takuita. |
| Takuuryhmä | *Takuuryhmä* on takuunimikkeiden ja takuunalaisten nimikkeiden välinen suhde. Myyntipiste määrittää takuuryhmien avulla, mitä takuunimikkeitä myyjiä kehotetaan lisäämään, kun takuunalainen nimike lisätään asiakkaan ostoskoriin. |
| Takuukäytäntö | *Takuukäytäntö* on entiteetti, joka luodaan Commercessa, kun takuukäytäntö myydään. Takuukäytäntö sisältää tietoja, kuten ostetun takuunimikkeen alkamis- ja päättymispäivät, käyttöehdot ja sen tuotteen sarjanumeron, jota takuu koskee. Takuukäytännön numerot voidaan jakaa asiakkaiden kanssa, jotta heillä on viittaus ostamaansa laajennettuun takuunimikkeeseen. |

## <a name="create-a-warranty-item"></a>Takuunimikkeen luominen

Takuunimike luodaan Commercessa seuraavasti:

1. Valitse **Retail ja Commerce \> Tuotteet ja luokat \> Tuotteet**.
1. Luo takuunimike valitsemalla **Uusi**.
1. Valitse **Uusi tuote** -valintaikkunan **Tuotetyyppi**-kentässä **Palvelu**.
1. Valitse **Tuotteen alatyyppi** -kentässä **Tuote**.
1. Valitse **Tuotteen palvelutyyppi**-kentässä **Palvelu**.
1. Anna **Tuotenimi**-kentässä tuotteen nimi.
1. Valitse **Vähittäismyyntiluokka**-kentässä avattavassa luettelossa arvo ja valitse sitten **OK**.
1. Anna **Tuotenumero**-kentässä tuotteen numero.
1. Valitse **OK**.
1. Määritä **Tuotteen tiedot** -sivun **Takuu**-pikavälilehdessä **Ajan yksikkö**- ja **Kesto**-kentät.

    | Kentän nimi | Arvo | kuvaus |
    |------------|-------|-------------|
    | Ajan yksikkö | **Päivää**, **Viikkoa**, **Kuukautta** tai **Vuotta** | Tämä kenttä määrittää takuussa käytetyn ajan yksikön. |
    | Ajan pituus | Positiivinen kokonaisluku | Tämä kenttää määrittää takuun keston valittuna ajan yksikkönä. |

    Esimerkiksi kahden vuoden takuussa **Ajan yksikkö** -kentän arvoksi määritetään **Vuotta** ja **Kesto**-kentän arvoksi **2**. Vaihtoehtoisesti **Ajan yksikkö** -kentän arvoksi voi määrittää **Kuukautta** ja **Kesto**-kentän arvoksi **24**, kuten seuraavassa kuvassa.

    ![Takuunimikkeen Tuotteen tiedot -sivu.](./media/ew-time-properties.png)

1. Tallenna takuunimike valitsemalla **Tallenna**.
1. Vapauta takuutuote yritykseen, jotta sitä voidaan myydä. Lisätietoja on kohdassa [Vähittäismyyntituotteiden määrittäminen](set-up-retail-products.md).
1. Määritä **Vapautetun tuotteen tiedot** -sivun **Takuu**-pikavälilehdessä **Perushinta-alue**-, **Alaraja**- ja **Yläraja**-kentät.

    | Kentän nimi | Arvo | kuvaus |
    |------------|-------|-------------|
    | Perushinta-alue | **Ei mitään**, **Perushinta** tai **Myyntihinta** | <ul><li>**Ei mitään** – hinta-alueen **Alaraja**- ja **Yläraja**-arvoja ei käytetä.</li><li>**Perushinta** – annettua takuuta käytetään, jos takuunalaisen tuotteen perushinta (eli hinta ilman alennuksia) sijoittuu tässä määritettyjen **Alaraja**- ja **Yläraja**-arvojen väliin, kun perusteena on takuunalaisen nimikkeen hinta.</li><li>**Myyntihinta** – tämä arvo varataan tulevaa käyttöä varten.</li></ul> |
    | Alaraja, yläraja | Positiivinen kokonaisluku | Nämä kentät määrittävät takuunalaisen nimikkeen hinnan ylä- ja alarajat sekä sen, miten nykyistä takuunimikettä käytetään takuunalaisessa nimikkeessä. Nämä rajat voivat perustua takuunalaisen nimikkeen perushintaan (joka tunnetaan valmistajan ehdotettuna vähittäismyyntihintana \[MSRP\]). Jos **Perushinta-alue**-kentässä on valittu **Perushinta**, vain sellainen takuunalainen nimike (tuote), jonka perushinta on **Alaraja**- ja **Yläraja**-arvojen välissä käynnistää myyntipisteessä kehotteen takuunimikkeen lisäämisestä. |

    Seuraavassa kuvassa on esimerkiksi **Perushinta-alue**-kenttä, jossa on valittu **Perushinta** ja jossa **Alaraja** -kentän arvona 500 $ ja **Yläraja**-kentän arvona 1 000 $.
    
    ![Takuunimikkeen Vapautetun tuotteen tiedot -sivu.](./media/ew-release-product-details.png)

1. Lisää takuunimike sen kanavan valikoimaan, jossa sitä myydään. Lisätietoja on kohdassa [Valikoimien määrittäminen](set-up-assortments.md).

### <a name="example"></a>Esimerkki

Kannettava tietokone on takuunalainen nimike (tuote), jonka perushinta on 999 $. Kannettavalla tietokoneella on kaksi takuunimikettä:

- Takuun \_1 alaraja on 500 $ ja yläraja 1 000 $ ja sen **Perushinta-alue**-kentässä on valittu **Perushinta**.
- Takuun \_2 alaraja on 1 001 $ ja yläraja 2 000 $ ja sen **Perushinta-alue**-kentässä on valittu **Perushinta**.

Kun tässä tapauksessa kannettava tietokone takuunalaisena nimikkeenä lisätään asiakkaan ostoskoriin, kehote lisää takuun\_1 näytettäväksi myyntipisteessä, koska kannettavan hinta sijoittuu takuun\_1 ylä- ja alarajojen väliin.

> [!NOTE]
> Jos haluat, että tässä esimerkissä näytetään sekä takuun\_1 että takuun\_2 kehitteet takuunalaisen nimikkeen hinnasta riippumatta, valitse **Perushinta-alue**-kentässä **Ei mitään**.

## <a name="configure-channel-specific-settings"></a>Kanavakohtaisten asetusten määrittäminen

Kanavakohtaisilla asetuksilla voi määrittää, näytetäänkö takuunimikkeen lisäämiskehote myyntipisteessä, kun takuunalainen nimike lisätään asiakkaan ostoskoriin.

Kanavakohtainen asetus määritetään Commercessa seuraavasti:

1. Valitse **Retail ja Commerce \> Tuotteet ja luokat \> Takuu \> Takuuasetukset**.
1. Tee **Kanavakohtainen**-välilehden kanavan **Takuukehote**-sarakkeessa jokin seuraavista:

    - Valitse valintaruutu, jos takuunimikkeen kehote näytetään myyntipisteessä, kun takuunalainen nimike lisätään ostoskoriin.
    - Poista valintaruudun valinta, jos takuunimikkeen kehotetta ei näytetä myyntipisteessä, kun takuunalainen nimike lisätään ostoskoriin.

1. Synkronoi tiedot kanavaa suorittamalla **1070**-työ.

## <a name="configure-a-number-sequence-for-warranty-policies"></a>Takuukäytäntöjen numerosarjojen määrittäminen

Jokaisella takuukäytännöllä on yksilöivästi tunnistettava takuukäytäntönumero, joka luodaan numerosarjana. Lisätietoja numerosarjoista on kohdassa [Numerosarjojen yleiskatsaus](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).

Takuukäytäntöjen numerosarjat määritetään Commercessa seuraavasti:

1. Valitse **Retail ja Commerce \> Tuotteet ja luokat \> Takuu \> Takuuasetukset**.
1. Anna tai valitse **Numerosarjat**-välilehden **Takuukäytäntö**-viitteen rivillä arvo **Numerosarjan koodi** -kentässä.

## <a name="set-up-a-warranty-group"></a>Takuuryhmän määrittäminen

Takuuryhmä on takuunimikkeiden ja takuunalaisten nimikkeiden välinen suhde. Myyntipiste määrittää takuuryhmien avulla, mitä takuunimikkeitä myyjiä kehotetaan lisäämään, kun takuunalainen nimike lisätään asiakkaan ostoskoriin.

Takuuryhmä määritetään Commercessa seuraavasti:

1. Valitse **Retail ja Commerce \> Tuotteet ja luokat \> Takuu \> Takuuryhmät**.
1. Luo takuuryhmä valitsemalla **Uusi**.
1. Kirjoita uuden ryhmä nimi **Nimi**-kenttään.
1. Kirjoita **Yleiset**-pikavälilehden **Kuvaus**-kenttään ryhmän kuvaus.
1. Lisää takuunimike valitsemalla **Takuutuotteet**-pikavälilehdessä **Lisää rivi**.
1. Anna **Näyttöjärjestys**-kentässä numero, jolla takuuryhmän sijoitus määritetään myyntipisteessä. Myyntipiste näyttää takuunimikkeet takuukehotteessa sijoituksen mukaan nousevassa järjestyksessä.
1. Lisää takuunlaiset tuotteet valitsemalla **Takuunalaiset tuotteet**-pikavälilehdessä **Lisää rivi**.
1. Jos takuunimike koskee koko takuunalaisten nimikkeiden (tuotteiden) luokkaa, valitse luokka **Luokka**-kentässä. Jos takuunimike koskee tiettyä takuunalaista nimikettä (tuotetta), valitse tuote **Tuote**-kentässä.
1. Lisää kanava, jossa haluat myydä takuunimikettä, valitsemalla **Käytettävät kanavat** -pikavälilehdessä **Lisää rivi**.
1. Tallenna määritys valitsemalla **Tallenna**.
1. Julkaise takuuryhmä valitsemalla **Julkaise**.
1. Synkronoi tiedot kanavaa suorittamalla **1040**-työ.

## <a name="sell-warranty-items-at-the-pos"></a>Takuunimikkeiden myynti myyntipisteessä

Myyjät voivat käyttää kahta myyntipistetoimintoa takuunimikkeiden myyntiin asiakasostojen työnkulun aikana:

- **Lisää takuu** – tämä toiminto käynnistää kehotteen, joka näyttää ostokorissa valittuna olevaa takuunalaista nimikettä koskevat takuut.
- **Lisää takuu aiemmin luotuun tapahtumaan** – Myyjä voi myydä tällä toiminnolla takuita aiemmin myydyille takuunalaisille tuotteille. Myyjä voi etsiä takuunalaisen nimikkeen alkuperäisen tehtävän antamalla tapahtuman kuitin numeron.

Seuraavassa kuvassa on esimerkki kassapäätesivusta, jossa on kehote lisätä takuunimike nykyiseen takuunalaisen nimikkeen ostoon.

![Esimerkki kehotteesta lisätä takuunimike nykyiseen ostoon.](./media/ew-sell-warranty.png)

Seuraavassa kuvassa on esimerkki toiminnosta, jolla lisätään takuunimike aiemmin myytyyn takuunalaiseen nimikkeeseen.

![Esimerkki toiminnosta, jolla lisätään takuunimike aiemmin myytyyn takuunalaiseen nimikkeeseen.](./media/ew-add-warranty-existing.png)

## <a name="process-warranty-transactions"></a>Käsittele takuutapahtumat

Kun takuita myydään itsepalvelutukkutapahtumille, Commerce-käyttäjät voivat suorittaa **Käsittele takuutapahtumat** -työn sen jälkeen, kun tapahtumat on kirjattu Commercen pääkonttoriversiossa. Tämä työ käsittelee takuutapahtumat ja luo takuukäytännöt.

Takuutapahtumia käsitellään Commercen pääkonttoriversiossa seuraavasti:

1. Valitse **Retail ja Commerce \> Tuotteet ja luokat \> Takuu \> Käsittele takuutapahtumat**.
1. Valitse **Valitse organisaatiosolmut** -valintaikkunan **Organisaatiohierarkia**-kentässä arvo.
1. Valitse **Käytettävissä olevat organisaatiosolmut** -luettelossa joko yksittäinen myymälä tai solmu, jos haluat luoda myymäläryhmän erätyön.
1. Lisää valinta oikealla nuolipainikkeella **Valitut organisaatiosolmut** -luetteloon.
1. Valitse **Suorita taustalla** -välilehti.
1. Määritä **Eräkäsittely**-vaihtoehdoksi **Kyllä** ja valitse sitten **Toistuminen**.
1. Valitse tai anna **Määritä toistuvuus** -valintaikkunan **Alkamispäivä**-kentässä toistuvuuden alkamispäivä.
1. Valitse tai anna toistuvuuden alkamispäivä **Alkamispäivä**-kentässä.
1. Noudata seuraavia ohjeita:

    - Valitse **Päättymispäivä puuttuu** -vaihtoehto, jos toistuvuuden ei ole tarkoitus päättyä.
    - Valitse **Päättyy jälkeen** -vaihtoehto, jos toistuvuuden on päätyttävä, kun tietty määrä ajoja on tehty. Jos valitset tämän vaihtoehdon, anna ajojen määrä.
    - Valitse **Päättyy mennessä** -vaihtoehto, jos toistuvuuden on päätyttävä tiettyyn päivämäärään mennessä. Jos valitset tämän vaihtoehdon, valitse tai anna päivämäärä.

1. Valitse **OK**.
1. Valitse **OK**.

## <a name="warranty-policies"></a>Takuukäytännöt

Kun laajennettu takuu myydään, takuukäytäntöentiteetti luodaan automaattisesti. Takuukäytännön numerot voidaan jakaa asiakkaiden kanssa, jotta heillä on viittaus ostettuun takuunimikkeeseen. Takuukäytäntöjen ominaisuudet sisältävät takuun alkamis- ja vanhentumispäivän, käyttöedot ja sen takuunalaisen tuotteen sarjanumeron, jolle takuu myytiin.

> [!NOTE]
> Takuukäytännön ominaisuudet luodaan automaattisesti, kun takuukäytäntöentiteetit luodaan. Tällä hetkellä niitä ei voi määrittää eikä muokata manuaalisesti.

Seuraavassa taulukossa käsitellään takuukäytännön ominaisuuksia ja niiden arvoja. Commercen pääkonttoriversiossa tietokantataulukon nimi on TAKUUKÄYTÄNTÖ.

| Ominaisuuden nimi | Arvo | kuvaus |
|---------------|-------|-------------|
| PolicyNumber | Merkkijono (enintään 20 merkkiä) | Takuukäytännön numero |
| WarrantiedItemId | Merkkijono (enintään 20 merkkiä) | Takuunalaisen nimikkeen tunnus |
| WarrantiedInventoryLotId | Merkkijono (enintään 20 merkkiä) | Takuunalaisen nimikkeen varastoerän tunnus |
| WarrantiedSerialNumber | Merkkijono (enintään 20 merkkiä) | Takuunalaisen nimikkeen sarjanumero |
| WarrantiedFulfilledDate | Päivämäärä | Takuunalaisen nimikkeen täyttämispäivä |
| WarrantyItemId | Merkkijono (enintään 20 merkkiä) | Takuunimikkeen tunnus |
| WarrantyInventoryLotId | Merkkijono (enintään 20 merkkiä) | Takuunimikkeen varastoerän tunnus |
| WarrantySalesDate | Päivämäärä | Takuunimikkeen myyntipäivä |
| WarrantyEffectiveDate | Päivämäärä | Takuukäytännön voimaantulopäivä |
| WarrantyExpirationDate | Päivämäärä | Takuukäytännön vanhentumispäivä |
| CustAccount | Merkkijono (enintään 20 merkkiä) | Asiakkaan tilinumero |
| Tila | **Luotu**, **mitätöity**, **voimassa** tai **vanhentunut** | Takuukäytännön tila |
| Muistiinpanot | Merkkijono (enintään 255 merkkiä) | Takuukäytäntöä koskevia huomautuksia, kuten käyttöehdot |

## <a name="frequently-asked-questions-faq"></a>Usein kysytyt kysymykset

**Miksi takuukehote ei näy myyntipisteessä?**

Varmista, että takuunimike on lisätty kanavan valikoimaan. Varmista myös, että takuuryhmä on määritetty sisältämään kyseinen kanava.

**Miksi tapahtumarivinimikkeitä ei näy, kun yritän lisätä takuun aiemmin luotuun tapahtumaan ja antaa asiakkaan tilauksen kuitin numeron?**

Kuitit löytyvät vain, jos kuitit ladataan Commercen pääkonttoriversioon suorittamalla noutotyö (P-työ). Suorita P-työ valitsemalla ensin **Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu**, sitten **P-0001**-työ ja lopuksi **Suorita nyt**.

**Miksi takuutoiminto koskee vain sarjoitettuja tuotteita?**

Takuu on palvelu, joka koskee tiettyä yksilöityä tuotetta. Dynamics 365:n tuote voidaan tunnistaa yksilöivästi vain sarjanumeron avulla.

## <a name="additional-resources"></a>Lisäresurssit

[Vähittäismyyntituotteiden määrittäminen](set-up-retail-products.md)

[Valikoimien määrittäminen](set-up-assortments.md)

[Numerosarjojen yleiskatsaus](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
