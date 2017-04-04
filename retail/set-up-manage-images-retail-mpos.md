---
title: "Määritä ja hallitse kuvia varten Retail POS-Sovelluksen Moderni"
description: "Tässä artikkelissa kuvataan toimet, jotka osallistuvat määrittäminen ja hallinta kuvia, jotka näkyvät-Retail Moderni POS (MPOS) eri kohteisiin."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 52851
ms.assetid: 5c21385e-64e0-4091-98fa-6a662eb33010
ms.search.region: global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: dbcf6d2ca3a6009c1631636309ff55cebb0551e6
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-and-manage-images-for-retail-modern-pos"></a>Määritä ja hallitse kuvia varten Retail POS-Sovelluksen Moderni

Tässä artikkelissa kuvataan toimet, jotka osallistuvat määrittäminen ja hallinta kuvia, jotka näkyvät-Retail Moderni POS (MPOS) eri kohteisiin.

<a name="setting-up-the-media-base-url-and-defining-media-templates-to-configure-the-format-for-image-urls"></a>Median URL-perusosoitteen ja mediamallien määrittäminen kuvien URL-osoitteiden konfiguraatiota varten
-------------------------------------------------------------------------------------------------

-Vähittäiskaupan Moderni POS (MPOS) näkyvät kuvat on isännöity ulkoisesti, ulkopuolella Microsoft Dynamics-365 työvaiheiden - Retail. Niitä isännöi yleensä sisällönhallintajärjestelmä, sisältöverkko (CDN) tai mediapalvelin. MPOS noutaa ja näyttää kuvat soveltuville yksiköille kuten tuotteille ja luetteloille, käyttämällä kohde-URL-osoitetta. Näiden ulkoisesti isännöityjen kuvien noutamista varten MPOS tarvitsee oikean URL-muodon kuville. Voit määrittää kuville vaaditun URL-muodon määrittämällä **Median URL-perusosoite **-arvon kanavaprofiilissa ja käyttämällä **Määritä mediamallit **-toimintoa kullekin yksikölle. Voit myös korvata perusmuotoisen URL:n yksikköjen osajoukolla käyttämällä **Muokkaa Excelissä** -toimintoa. **Tärkeä huomautus:** Dynamics 365 työvaiheiden nykyisessä versiossa ei enää määritetään URL-muotoa käyttämällä **kuvan** XML-määrite, MPOS **oletus** entiteettien määriteryhmän. Jos osaat Microsoft Dynamics AX 2012: n R3 ja ovat nyt työvaiheiden Dynamics 365 nykyisen version avulla, varmista, että käytät aina uuden **määrittäminen media-mallin** toimintoja kuvien määrittäminen. Älä käytä tai muokkaa **Kuva**-määritettä **Oletus**määriteryhmässä millekään yksikölle, mukaan lukien tuotteet. Suoraan **Oletus** kuvien määritysjoukossa tekemiäsi muutoksia ei oteta huomioon. Tämä vaihtoehto poistetaan käytöstä tulevissa versioissa. Seuraavissa menettelyissä on esimerkki kuvien määrittämisestä luetteloyksikölle. Näiden menettelyjen avulla voit taata, että oikea kuvan kohdepolku on implisiittisesti määritetty kaikille yhteistä polkua käyttäville luettelokuville. Jos olet esimerkiksi tehnyt mediapalvelimen tai CDN:n asetukset ulkoisesti ja haluat, että kuvat näkyvät tietyn myymälän MPOS:ssa, **Määritä mediamallit** -toiminto auttaa sinua määrittämään polun, josta MPOS voi etsiä ja noutaa kuvat. **Huomautus:** Tässä esittelytietoesimerkissä mediapalvelin on otettu käyttöön vähittäismyynnin palvelimella. Kuitenkin voi olla se missä tahansa Dynamics 365 toimintojen ulkopuolelle.

### <a name="set-up-the-media-base-url-for-a-channel"></a>Median URL-perusosoitteen määrittäminen kanavalle

1.  Avaa toimintojen Esikunnan portaalin Dynamics-365.
2.  Valitse **jälleenmyynti- ja commerce**&gt;**kanava-asetukset**&gt;**kanava profiilit**. [![kanava-profile1](./media/channel-profile1.png)](./media/channel-profile1.png)
3.  Päivitä myymäläsi MPOS:lle käyttämässä kanavaprofiilissa mediapalvelimesi tai CDN:si URL-perusosoite **Median URL-perusosoite** -kenttään. On base URL-osoite on URL-osoite, joka on jaettu eri yksiköiden kaikki kuva-kansioiden mukaan ensimmäinen osa. [![kanava-profile2](./media/channel-profile2.png)](./media/channel-profile2.png)

### <a name="define-the-media-template-for-an-entity"></a>Määritä yksikön mediamalli

1.  Valitse **jälleenmyynti- ja commerce**&gt;**luettelon hallinta**&gt;**luettelon kuvia**.
2.  Valitse **Luettelokuvat**-sivun Toimintoruudussa **Määritä mediamallit**. **Määritä mediamallit** -valintaikkunan **Yksikkö**-kentässä pitäisi oletusvalintana olla **Luettelo**.
3.  Syötä **Mediapolku**-pikavälilehdessä kuvan sijainnin polun loppuosa. Mediapolku tukee **LanguageID:tä** muuttujana. Voit esimerkiksi luoda demotiedoille **Luettelot**-kansion kaikille mediapalvelimesi median URL-perusosoitteessa sijaitseville luettelokuville (https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer). Sinulla voi sitten olla kansio kullekin kielelle, kuten en-US tai fi-FI, ja kopioida kuhunkin kansioon asiaankuuluvat kuvat. Jos sinulla ei ole eri kuvia eri kielille, voit ohittaa **LanguageID**-muuttujan kansiorakenteestasi ja osoittaa suoraan luettelokuvat sisältävää Luettelot-kansioon. **Huomautus:** Nykyinen Dynamics AX:n versio tukee **{LanguageId}**-tunnusta Luettelo-, Tuote- ja Luokka-yksiköihin. **{LanguageID}**-tunnusta ei tueta Asiakas- ja Työntekijä-yksiköille nykyisen, Microsoft Dynamics AX 6.x.:stä lähtien voimassa olleen standardin mukaisesti.
4.  Kuvien tiedostonimen muoto on pysyväiskoodattu luettelon nimeen eikä sitä voi muuttaa. Nimeä siksi kuvasi uudelleen niin, että niillä on soveltuvat luettelon nimet sen varmistamiseksi, että MPOS käsittelee niitä oikein.
5.  Valitse **Tiedostotunniste**-kentässä odotettu tiedostonimen tunniste riippuen sinulla olevista kuvatyypeistä. Esimerkiksi demotiedoissa luettelokuvien asetukseksi on määritetty .jpg-tunniste. (Kuvatiedot nimetään myös uudelleen niin, että niillä on luetteloiden nimet.)
6.  Click **OK**.
7.  Tarkista, että kuvien mediamalli on tallennettu oikein, valitsemalla **Luettelokuvat**-sivulla uudelleen **Määritä mediamallit**. Jos haluat tarkistaa mallin sulkematta **Määritä mediamallit** -valintaikkunaa, voit käyttää **Luo kuvien URL-osoitteet Exceliin** -pikavälilehteä. Tarkista kuvan URL-osoitteen ulkonäkö ja varmista, että URL-osoite on aiemmin mainitun mallistandardin mukainen. **Määritä mediamallit** -valintaikkuna on nyt määrittänyt kuvan polun implisiittisesti kaikille tätä yhteistä URL-polkua käyttäville luettelokuville. Tätä URL-polkua käytetään kaikille luettelokuville, ellei niitä ole korvattu. Ensimmäinen osa kuvan polkua otetaan median URL-perusosoitteesta, jonka määritit kanavaprofiilissa. Polun loppuosa otetaan polusta, jonka määritit mediamallissa. Nämä kaksi osaa liitetään yhteen ja näin muodostetaan kuvan sijainnin täydellinen URL-osoite. Esimerkiksi demotiedoissa olevan luettelon nimi on Fabrikam Base Catalog. Näin ollen kuvan nimen on oltava Fabrikam Base Catalog.jpg, jotta se käyttää luettelon nimeä ja .jpg-tiedostonimen tunnistetta, joka määritettiin mallissa. Tässä tapauksessa, yhteen liittämisen jälkeen URL-osoite on https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer/Catalogs/en-US/Fabrikam Base Catalog.jpg.
8.  Suorita synkronointityöt uuden mallin siirtämiseen kanavan tietokantaan niin, että MPOS voi käyttää näitä kuvia mallia avulla.
9.  Päivitä media malli luettelo kuvia kanavan puolella, muista suorittaa **luettelon työn 1150** - **vähittäismyynnin IT**&gt;**aikataulun jakelu**. [![catalog1](./media/catalog1.png)](./media/catalog1.png)

## <a name="previewing-an-image-from-the-entity-level"></a>Kuvan esikatselu yksikkötasolla
1.  Yksikkönimikkeen pääkonttorissa olevalta sivulta voit esikatsella kuvia, jotka käyttävät mediamallista johdettua kuvan URL-osoitetta. Esimerkiksi, siirry haluamasi luettelon ja valitse sitten toiminto-ruudussa **Media**&gt;**kuvia**. Valitse avattavasta luettelosta eri myymälät, joilla saattaa olla erilaisia kanavaprofiileita.
2.  Jos haluat muokata tai poistaa implisiittisen mediamallin, sinun on palattava **Määritä mediamallit** -valintaikkunaan **Luettelokuvat**-sivulle.
3.  Voit käyttää **Lisää** ja **Poista**-painikkeita muuttaaksesi manuaalisesti polun, joka perustuu implisiittiseen malliin ja jota käytetään määrätylle kuvalle. Lisätietoja jäljempänä tämän aiheen osiossa “Yksikkönimikkeiden mediamallien korvaaminen".
4.  Sen jälkeen, kun olet lisännyt kuvan esikatselun ja tekemällä muutokset edellyttävät, Käynnistä myymälöiden MPOS esiintymän ja nähdä luettelon kuvat näytetään. [![catalog4](./media/catalog4.png)](./media/catalog4.png)

**Huomautus:** Voit käyttää samaa menettelyä kaikille viidelle tuetulle yksikölle: Työntekijä, Asiakas, Luettelo, Luokka, ja Tuotteet. "Luettelotuotteet" (tuotteet, jotka määritetään luettelotasolla) ja "Kanavatuotteet" (tuotteet, jotka määritetään kanavatasolla) käyttävät Tuotteet-yksikölle määritettyä mediamallia. Tuotteet-mediamallissa voit valita näytettävien tuotekuvien määrän tuotekohtaisesti. Voit myös määrittää tuotteen oletuskuvan. Näin voit estää tyhjät kuvat MPOS:ssa ja hallita, mitä kuvia käytetään tuotenimikkeen oletuskuvana. Seuraavassa esimerkissä kullakin tuotteella on viisi kuvaa, ja ensimmäinen kuva määritetään oletuskuvaksi. Tuotevariantteja käsitellään samalla tavoin kuin päätuotteita. Kuvatiedostojen tiedostonimien tulee perustua tuotenumeroihin. Joitain merkkejä myös ohitetaan tiedostonimeä luotaessa. Tiedostonimi tulisi siksi tarkistaa käyttämällä **Luo kuvien URL-osoitteet Exceliin** -osiota. [![keppejä](./media/prods.png)](./media/prods.png)  

## <a name="synchronization-jobs-to-send-a-media-template-to-the-channel-side"></a>Synkronointityöt mediamallin lähettämiseksi kanavapuolelle
Kaikki viisi tuetun entiteettien (työntekijä, asiakas, luettelo, luokka ja tuotteet), aina, kun päivität **määrittäminen media malli** valintaikkunan kuvan asetukset, varmista, että voit suorittaa luettelon työ (1150) **vähittäismyynnin IT**&gt;**aikataulun jakelu**. Tämä työ ottaa käyttöön päivitetyn mediamallin synkronoitavaksi kanavaan ja MPOS:n käyttöön. Suorita Luettelotyö (1150), kun olet tehnyt jonkin seuraavista muutoksista:

-   Voit päivittää luettelon kuvan media mallin **luettelon kuvia**&gt;**mallin määrittäminen media**.
-   Työntekijän kuvan media mallin päivittäminen **työntekijän kuvia**&gt;**mallin määrittäminen media**.
-   Voit päivittää kuvan media asiakasmallin- **asiakkaan Kuva**&gt;**mallin määrittäminen media**.
-   Voit päivittää tuotteen kuva media mallin **tuotekuvat**&gt;**mallin määrittäminen media**.
-   Luokan kuvan media mallin päivittäminen **luokan kuvia**&gt;**mallin määrittäminen media**. Sinun täytyy myös julkaista kanava.

## <a name="overwriting-the-media-template-for-entity-items"></a>Yksikkönimikkeen mediamallin korvaaminen
Kuten opit edellisessä kohdassa, tietyn yksikön mediamalli tukee vain yhtä yhteistä polkua. Tämä polku perustuu määritettyyn median URL-perusosoitteeseen ja mediapolkuun. Useissa tapauksissa jälleenmyyjä haluaa pystyä käyttämään eri lähteistä tulevia kuvia yksikön nimikkeiden osajoukolle. Myymälä voi esimerkiksi käyttää itseisännöityä mediapalvelinta yhdelle luettelokuvien joukolle, mutta käyttää CDN URL-osoitteita toiselle joukolle. Jos haluat korvata yksiköiden kuvien mediamalliin perustuvia kuvan URL-osoitteita yksikkötasolla, voit käyttää Muokkaa Excelissä- ja Manuaalinen muokkaus -toimintoja **Esikatselu**-sivulla.

### <a name="overwrite-by-using-edit-in-excel"></a>Korvaa käyttämällä Muokkaa Excelissä-toimintoa

1.  Valitse **jälleenmyynti- ja commerce**&gt;**luettelon hallinta**&gt;**luettelon kuvia**.
2.  Valitse **Luettelokuvat**-sivulla **Määritä mediamallit**. **Määritä mediamallit** -valintaikkunan **Yksikkö**-kentässä pitäisi olla valittuna **Luettelo**.
3.  Huomioi **Mediapolku**-pikavälilehdessä kuvan sijainti.
4.  Valitse **Luo kuvien URL-osoitteet Exceliin** -pikavälilehdellä **Luo**. **Tärkeää:** Aina, kun mediamallia muutetaan, sinun on valittava **Luo** ennen kuin voit käyttää Muokkaa Excelissä-toimintoa. [![excel1](./media/excel1.jpg)](./media/excel1.jpg) voit nyt esikatsella kuvan URL-osoitteet, jotka luotiin viimeksi tallennettu media mallin perusteella. [![excel2](./media/excel2.png)](./media/excel2.png)**Huomautus:** URL-osoitteet, jotka on luotu Excel käyttää polku ja käytäntöjä media-mallin, joka on määritetty. Näihin käytäntöihin sisältyy tiedostonimiä koskevat käytännöt. Odotus on, että olet määrittänyt fyysiset kuvat Dynamics AX:n ulkopuolella ja kuvat voidaan noutaa URL-osoitteista, jotka on johdettu aiemmin määrittämästäsi mediamallista. Voit korvata nämä johdetut URL-osoitteet Muokkaa Excelissä -toiminnon avulla.
5.  Valitse **Muokkaa Excelissä**.
6.  Kun Microsoft Excel -laskentataulukko avautuu, napsauta **Ota muokkaus käyttöön**, kun saat kehotuksen.
7.  Kun saat tätä koskevan kehotuksen, napsauta **Luota tähän lisäosaan** oikeanpuoleisessa ruudussa ja odota lisäosan latautumisen valmistumista. [![Tämä apuohjelma on luotettava](./media/excel4.jpg)](./media/excel4.jpg)
8.  Jos saat kehotuksen kirjautua sisään, syötä tunnistetiedot, joita käytit kirjautuessasi pääkonttoriin. [![Kirjaudu sisään kehote](./media/excel5.png)](./media/excel5.png)
9.  Kun olet kirjautunut sisään, sinun pitäisi pystyä näkemään eri luettelonimikkeiden kuvien URL-osoitteiden luettelon.
10. Voit muokata, lisätä tai poistaa eri yksikkönimikkeiden kuvien URL-osoitteita.
11. Voit korvata kaikkien muiden yksiköiden kuvien URL-osoitteet paitsi Tuotteiden. Muokkaa olemassa olevaa kuvan URL-osoitetta niin, että se käyttää uutta kuvan kohde-URL:ää ja päivitä kuvatiedoston tiedostonimeksi uusi tiedostonimi. Tiedostonimien on oltava yksilöivä sen varmistamiseksi, että tietue on yksilöllinen. [![Korvaa Excelissä kuva URL-osoitteet](./media/excel6.jpg)](./media/excel6.jpg)**Huomautus:** tuotteiden entiteettien kuvan URL-osoitteet korvata käyttämällä Muokkaa Excel-toimintoja tai yksikön Nimike-sivu, kun MPOS näkyvät aina kaikki media mallin kuvan URL ja korvata kuvan URL-osoitteet.
12. Kun olet tehnyt kaikki muutokset, luo uusi eksplisiittinen liitosmerkintä valitsemalla **Julkaise Excelissä**.
13. Palaa Pääkonttoriin ja napsauta **OK**.
14. Suorita kyseisen yksikön soveltuvat synkronointityöt ja tarkista esikatselu yksikkösivulla tai MPOS:ssa.

#### <a name="creating-new-records"></a>Uusien tietueiden luonti

Voit luoda uusia tietueita Excelissä. Varmista kuitenkin, että annat oikeat tiedot. Esimerkiksi, luodaksesi uuden luettelomerkinnän, varmista, että luettelon tunnus ja luettelon nimi ovat oikein. Anna myös yksilöivä tiedostonimi. Yksilöivä tiedostonimi on erittäin tärkeä, koska Excelin tietueiden yksilöllisyys tarkistetaan julkaisun aikana. Kopioi ensin tiedot siitä luettelosta, johon haluat luoda uuden tietueen ja kopioi sitten kyseinen tietue. Sinun tarvitsee vain päivittää tiedostonimi ja URL-osoite, koska muut tiedot ovat samat. Käytät samaa perusmenettelyä uusien tietueiden luomiseen Tuoteyksikkönimikkeille. Kopioi Excel-laskentataulukosta olemassa oleva tietue sille tuotteelle, jolle haluat luoda uuden tietueen ja korvaa kuvan URL-osoite ja tiedostonimi. Varmista, että tiedostonimi on yksilöivä.

#### <a name="deleting-an-existing-record"></a>Olemassa olevan tietueen poistaminen

Vain korvatut kuvien URL-tietueet voidaan poistaa. Kun kuva on poistettu ja synkronisointi valmistunut, kuvaa ei enää näytetä **Esikatselu**-sivulla tai MPOS:ssa. Mediamallista johdettuja kuvien URL-tietueita ei voida poistaa, koska nämä tietueet johdetaan aina mediamallista jokaisella kerralla.

### <a name="overwrite-from-the-entity-level-preview-page"></a>Korvaaminen yksikkötason Esikatselu-sivulta

Lukuun ottamatta Tuote-yksiköitä, voit korvata tietyn yksikkönimikkeen kuvan URL-osoitteen yksikkönimiketasolla **Esikatselu**-sivulla. Tuotteille voit käyttää "Luettelotuotteet"-yksikkösivua. Tässä esimerkissä havainnollistetaan, kuinka luettelokuva korvataan.

1.  Valitse **luettelot**&gt;**Media**&gt;**kuvia**, ja valitse Päivitä luettelon-kuva.
2.  Valitse **Lisää** ja syötä sen kuvan URL-osoite, joka korvaa mediamallin URL-osoitteen.
3.  Jos haluat, että tämä kuva näytetään luettelolle MPOS:ssa, voit määrittää sen oletuskuvaksi.
4.  Napsauta **OK**. Kuvan URL-osoite päivitetään tämän luettelokuvan osalta ja näytetään kuvan esikatselu. [![preview3](./media/preview3.png)](./media/preview3.png)
5.  Voit myös esikatsella kaikkien korvattujen kuvien URL-osoitteiden kuvat**Luettelokuvat**-galleriasivulla.

**[![Esikatselu-4](./media/preview-4.png)](./media/preview-4.png)Huomautus:** tällä hetkellä valikoimassa ei Näytä Media Esikatselukuvat mallin kuvan URL-osoitteita. Luettelo-, Työntekijä-, Asiakas-, ja Luokka- yksiköiden ollessa kyseessä, jos käyttäjä antaa eksplisiittisesti URL-osoitteen tällä sivulla, suosittelemme, että ilmaiset, mikä kuva on oletuskuva, koska Retail Serverin työasemat näyttävät vain yhden kuvan kullekin Luettelolle, Asiakkaalle, Työntekijälle ja Luokalle. Jos käyttäjä ei määritä oletuskuvaa, järjestelmä määrittää oletuskuvan ja lähettää sen vähittäismyynnin palvelinkutsujalle (MPOS tai Ecommerce).

### <a name="overwrite-the-image-url-for-catalog-product-images-from-the-preview-page"></a>Kuvan URL-osoitteen korvaaminen tuotekuville Esikatselu-sivulta

Jos haluat korvata kuvien URL-osoitteet luetteloiden tuotekuville, sinun on käytettävä **Esikatselu**-sivua. Et voi käyttää Muokkaa Excelissä -toimintoa.

1.  Korvaa tuotekuvat luettelotasolla valitsemalla luettelo ja valitsemalla sitten tuote, jonka tuotekuvan haluat korvata.
2.  Valitse **Määritteet**.
3.  Valitse seuraavalla sivulla **Kuva** ja napsauta sitten **Muokkaa**. **Esikatselu**-sivu avautuu liukuvana valintaikkunana.
4.  Valitse **Lisää** ja korvaa kuvan URL-osoite uudella URL-osoitteella.
5.  Napsauta **OK**. Näet nyt uuden kuvan esikatselun ja voit määrittää sen oletuskuvaksi.

**[![cat3](./media/cat3.png)](./media/cat3.png)Huomautus:** luokan kuvan kytkennän jälkeen julkaista kanava ja kanava netto auttavat takaamaan, että kanava tietokantaan julkaistaan muutoksia.

## <a name="setting-up-images-to-appear-in-offline-mode-for-mpos"></a>Kuvien määrittäminen näkymään MPOS:n offline-tilassa
MPOS voi toimia online-tilassa (kun MPOS:lla on yhteys Retail Serveriin) tai offline-tilassa (kun ei ole yhteyttä Retail Serveriin tai verkkoyhteyttä, ja tapahtumat tallennetaan paikalliseen offline-tietokantaan). Kun MPOS toimii offline-tilassa, se ei voi hakea kuvia ulkoiselta kuvapalvelimelta näyttääkseen ne Retail Serverillä, koska yhteys Retail Serveriin on menetetty. Voit kuitenkin määrittää kuvat niin, että ne näytetään, kun MPOS on offline-tilassa.

### <a name="set-up-product-images-to-appear-in-offline-mode-for-mpos"></a>Tuotekuvien määrittäminen näkymään MPOS:n offline-tilassa

Tuotekuvat, joita on käytettävä offline-tilassa, voidaan määrittää lataamalla tarvittava fyysinen kuva perustuotteen kuvaan.

1.  Valitse **tuotetietojen hallinta**&gt;**tuotteita**&gt;**tuotteita**.
2.  Valitse tuote, jolle määritetään offline-kuva.
3.  Valitse **Muokkaa**, ja napsauta sitten oikeassa kulmassa olevaa nuolta niin, että oikeanpuoleinen ruutu tuodaan näkyviin.
4.  Napsauta **Tuotekuva**-pikavälilehdellä **Muuta kuva**, ja lataa fyysinen kuva, joka näytetään valitulle tuotteelle offline-tilassa.
5.  Tallenna ja sulje sivu.
6.  Kun MPOS on online-tilassa, suorita Luettelo-työ pääkonttorissa varmistaaksesi, että tiedot lähetetään ainakin kerran offline-tietokantaan.
7.  Aseta MPOS offline-tilaan. Sinun pitäisi nähdä tietylle tuotteelle lataamasi kuva pääkonttorissa. [![offline1](./media/offline1.png)](./media/offline1.png)

 

### <a name="set-up-catalog-category-employee-and-customer-images-to-appear-in-offline-mode-for-mpos"></a>Luettelo-, luokka-, työntekijä- ja asiakaskuvien määrittäminen näkymään MPOS:n offline-tilassa

Luettelo-, luokka-, työntekijä- ja asiakaskuvat, joita on käytettävä offline-tilassa, voidaan määrittää lisäämällä tarvittavan kuvan kohdelinkki galleriaan ja määrittämällä kuva valitun yksikön oletuskuvaksi.

1.  Siirry luetteloon ja valitse sitten toimintoruudusta **Media**&gt;**kuvia**.
2.  Seuraa kohdan "**Korvaaminen yksikkötason Esikatselu-sivulta**" vaiheita lisätäksesi ulkoisen kuvan URL-osoitteen.
3.  Merkitse tämä kuva luettelon oletuskuvaksi valitsemalla Kuva-kohdan vieressä oleva valintaruutu ruudukon luettelosta.
4.  Suorita Luettelo-työ. Tätä kuvaa käytetään nyt kyseisen luettelon offline-kuvana MPOS:ssa.
5.  Noudata samaa prosessia muille yksiköille, kuten Luokka, Työntekijä ja Asiakas.

[![offline2](./media/offline2.png)](./media/offline2.png)    


