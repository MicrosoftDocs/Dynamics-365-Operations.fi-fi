---
title: Käyttäjäkokemuksen mukauttaminen
description: Tässä artikkelissa kerrotaan, miten voit mukauttaa sovellusta.
author: jasongre
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserSetup, DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c326e51dc127d8b82ccef28146ec223ca5169c5e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845439"
---
# <a name="personalize-the-user-experience"></a>Käyttäjäkokemuksen mukauttaminen

[!include [banner](../includes/banner.md)]

[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Tässä artikkelissa kerrotaan, miten voit mukauttaa sovellusta. Ohjeaihe sisältää seuraavat aiheet: 

- **Järjestelmänlaajuiset valinnat** – Nämä mukautusvalinnat tehdään asetussivulla. Ne ovat kaikkien käyttäjien käytettävissä. Väriteema ja aikavyöhyke ovat niistä esimerkkejä. 
- **Rajoitettu mukautuksen käyttöoikeus** – Tällä tasolla käyttäjän toiminnot, jotka liitetään tyypilliseen sivun käyttöön, tallennetaan automaattisesti sovellukseen ja palautetaan seuraavalla sivunkäyttökerralla. Sovellus tallentaa esimerkiksi ruudukoiden sarakeleveyksiä, jos muutat niitä, sekä pikavälilehtien laajennus- tai tiivistystiloja. 
- **Täysi mukautusoikeus** – Tällä käyttöoikeustasolla käyttäjillä on kaikkien mukautusominaisuuksien käyttöoikeus sovelluksessa. He voivat käyttää **Mukautus**-työkaluriviä. 
- **Mukautusten jakaminen** – Käyttäjät, joilla on täysi mukautusoikeus, voivat viedä sivun mukautuksia ja jakaa niitä muiden käyttäjien kanssa.
- **Mukautusten hallinta** – Käyttöoikeuden omaavat käyttäjät voivat käyttää **mukautuksen** hallintasivua ja hallinnoida kaikkia mukautuksia organisaation tasolla. 

## <a name="system-wide-options-for-the-current-user"></a>Nykyisen käyttäjän järjestelmänlaajuiset vaihtoehdot

**Käyttäjän asetukset** -sivulla on useita nykyisen käyttäjän koko järjestelmää koskevia asetuksia. Nämä vaihtoehdot ovat kaikkien käyttäjien käytettävissä, myös niiden, joille ei ole myönnetty mukautusoikeuksia. Avaa **Käyttäjän asetukset** -sivu valitsemalla **Asetukset**-painike siirtymispalkissa. Valitse sitten **Käyttäjän asetukset**. **Käyttäjän asetukset** -sivulla on neljä välilehteä, joissa erilaisia käyttäjäasetuksia:

- **Visuaalinen** – valitse sivun elementtien väriteema ja oletuskoko.
- **Asetukset** – Valitse oletusarvot, joita käytetään aina, kun avaat järjestelmän. Näitä arvoja ovat esimerkiksi oletusyritys, ensimmäinen sivu sekä näkymän tai muokkauksen oletustila. (Näkymä- tai muokkaustila määrittää, lukitaanko sivu näyttämistä varten vai avataanko se muokattavaksi aina, kun avaat sen.) Tässä välilehdessä on kieli- ja aikavyöhykeasetukset sekä päivämäärä-, kellonaika- ja numeromuotoilun asetukset. Tässä välilehdessä on lisäksi sekalaisia asetuksia,, jotka vaihtelevat julkaisuversiosta toiseen.
- **Tili** – Katso tai muokkaa käyttäjänimeä ja muita tiliin liittyviä asetuksia.
- **Työnkulku** – työnkulkuun liittyvien asetusten valitseminen.

Asetuksien muuttamisen lisäksi voit myös tarkastella ja poistaa käyttötiedot ja mukautukset käyttämällä **Käyttäjän asetukset** -sivua. Jos haluat nähdä käyttötiedot, valitse **Käyttötiedot** toimintoruudussa. **Mukauttaminen**-välilehdessä voit tarkastella ja hallita henkilökohtaisia muutoksia, jotka olet tehnyt sivuihin järjestelmässä. Tässä välilehdessä voit myös nollata kuvatekstitoiminnot (eli ponnahdusikkunat, joissa esitellään järjestelmän uudet ominaisuudet). Tämän jälkeen sinulle ilmoitetaan jälleen aiemmin käytetyistä ominaisuuksista.

> [!NOTE]
> Jos [Tallennetut näkymät](saved-views.md) -toiminto on käytössä, voit tarkastella ja hallita omia mukautuksiasi valitsemalla **Mukauttaminen** toimintoruudun **Käyttäjän asetukset** -sivulla.

## <a name="restricted-personalization-access-formerly-implicit-personalizations"></a>Rajoitettu mukautusoikeus (aiemmin implisiittiset mukautukset)

**Rajoitettu mukautuksen käyttöoikeus** -tasolla käyttäjän toiminnot, jotka liitetään tyypilliseen sivun käyttöön, tallennetaan automaattisesti sovellukseen ja palautetaan seuraavalla sivunkäyttökerralla. Eksplisiittistä tallennustoimintoa ei tarvita. 

Alla on luettelo toiminnoista, jotka kuuluvat tyypilliseen sivun käyttöön ja joita koskee rajoitettu mukautusoikeus: 

- **Ruudukon sarakkeenleveydet** – Ruudukon sarakkeen leveyttä voidaan säätää valitsemalla koon muuttamiseen tarkoitettu palkki sarakkeen otsikon vasemmalla tai oikealla puolella ja vetämällä sitä vasemmalle tai oikealle, kunnes sarake on halutun levyinen. Sovellus tallentaa sarakkeelle määritetyn leveyden. Kun seuraavan kerran avaat sivun, sarakkeen koko muutetaan vastaamaan kyseistä leveyttä.
- **Ruudukon alatunniste ja sarake yhteensä** – *(Käytettävissä vain, kun uuden ruudukon ohjausobjekti on päällä)* Voit päättää, näkyykö kokonaissumma minkä tahansa numeerisen sarakkeen alaosassa ruudukossa ja onko ruudukon alatunnisteen oltava näkyvissä. Sovellus tallentaa nämä määritykset ja käyttää niitä, kun seuraavan kerran avaat sivun. Lisätietoja on aiheessa [Ruudukon ominaisuudet](grid-capabilities.md). 
- **Pikavälilehdet** – Joillain sivuilla on laajennettavia *pikavälilehtinä* tunnettuja osia. Sovellus tallentaa tietoja laajennetuista ja tiivistetyistä pikavälilehdistä. Kun avaat sivun seuraavan kerran, pikavälilehdet näkyvät joko laajennettuina tai tiivistettyinä sen mukaan, mitä olet valinnut sivulla edellisellä kerralla. Joissain tapauksissa voit parantaa järjestelmän suorituskykyä tiivistämällä pikavälilehden, koska sovellus ei tarvitse noutaa tietoja pikavälilehtiä varten, ennen kuin ne laajennetaan. Jäljempänä tässä artikkelissa kerrotaan, miten voit myös muuttaa sivulla olevien pikavälilehtien järjestystä.
- **Tietoruudut** – Osalla sivuista on **Aiheeseen liittyviä tietoja** -ruutu, jossa näkyy vain luku -tietoja, jotka liittyvät sivun kulloiseenkin aiheeseen. Kukin **Aiheeseen liittyviä tietoja** -ruudun osio on nimeltään *Tietoruutu*. Voit laajentaa tai kutistaa **Aiheeseen liittyviä tietoja**-ruudun. Voit myös laajentaa tai kutistaa yksittäisiä tietoruutuja. Sovellus tallentaa nämä asetukset. Kun seuraavan kerran avaat sivun **Aiheeseen liittyviä tietoja** -ruutu ja yksittäiset tietoruudut ovat joko laajennettuna tai kutistettuna sen mukaan, mitä olet valinnut edellisellä kerralla. Joissain tapauksissa voit parantaa järjestelmän suorituskykyä kutistamalla **Liittyvät tiedot** -ruudun tai tietoruudun, koska sovelluksen ei tarvitse noutaa tietoja tietoruutuja varten, ennen kuin ne laajennetaan.
- **Toimintoruudut** – *Toimintoruutu* näkyy useimmilla sivuilla yläreunan lähellä. Toimintoruudussa on painikkeita, joilla voi tehdä monia valitulla sivulla tehtäviä toimintoja. Nämä painikkeet on usein järjestetty välilehtiin. Voit *kiinnittää* koko toimintoruudun avoimeksi. Vaihtoehtoisesti se voi olla oletusarvoisesti kutistettuna. Kun tämän jälkeen avaat sivun, toimintoruutu on joko auki tai kutistettuna sen mukaan, mitä olet valinnut edellisellä kerralla. Jos olet kiinnittänyt toimintoruudun avoimeksi, näkyvissä on viimeisin käyttämäsi välilehti.
- **Pikasuodattimet** – *Pikasuodatin* näkyy monien ruudukoiden yläpuolella. Pikasuodattimia voi käyttää ruudukon suodattamiseen valitun yhden sarakkeen perusteella. Sovellus tallentaa sarakkeen, johon suodatus perustuu. Kun avaat seuraavan kerran sivun, ruudukossa käytetään samaa saraketta suodatuksessa oletusarvoisesti. Voit kuitenkin suodattaa ruudukon tämän jälkeen toisen sarakkeen perusteella.
- **Sarakeotsikon suodattimet** – Kun ruudukkoa suodatetaan *sarakeotsikon suodattimilla*, suodatinoperaattori voidaan tarvittaessa vaihtaa etsittävien tietojen mukaan. Voit esimerkiksi vaihtaa operaattorin **alkaa** operaattoriksi **on täsmälleen**. Aina kun käytät sarakeotsikon suodatinta ja muutat suodatinoperaattoria, sovellus tallentaa muutoksen. Kun sitten seuraavan kerran suodatat kyseistä saraketta, suodatinoperaattori palautetaan.
- **Siirtymisruutu** – Voit avata *navigointiruudun* valitsemalla **Laajenna siirtymisruutu**-painikkeen minkä tahansa sivun vasemmassa yläkulmassa. (Tätä painiketta kutsutaan myös _**Valikko**-painikkeeksi_, *hampurilaiseksi*, *hampurilaismenuksi* tai *hampurilaispainikkeeksi*.) Voit kiinnittää siirtymisruudun avoimeksi tai pitää sen oletusarvoisesti kutistettuna. Kun olet kiinnittänyt siirtymisruudun avoimeksi, sovellus pitää sen avoimena siihen asti, että kutistat sen.

## <a name="full-personalization-access-formerly-explicit-personalizations"></a>Täysi mukautusoikeus (aiemmin eksplisiittiset mukautukset)

**Täysi mukautusoikeus** -tasolla käyttäjillä on kaikkien mukautusominaisuuksien käyttöoikeus sovelluksessa. Eri henkilöillä ja yrityksillä on erilaiset sovelluksen käyttöön liittyvät tarpeet, erityisesti käytettyjen kenttien osalta. Mukautus mahdollistaa sellaisten työkalujen käyttämisen, joiden avulla käyttäjät ja organisaatiot voivat räätälöidä tietojen järjestelyn ja sovelluksen käyttötavan. Nämä ominaisuudet ovat avainasemassa, kun halutaan tarjota yksinkertainen ja optimoitu käyttökokemus sovelluksessa, joka on räätälöity organisaatiolle ja käyttäjälle. 

Jos [Tallennetut näkymät](saved-views.md) -ominaisuus on käytössä., eksplisiittinen tallennus on pakollinen, jotta nämä muutokset säilyvät tietyn näkymän käyttökokemuksessa. Kun **Tallennetut näkymät** -toiminto on pois päältä, nämä muutokset tallennetaan automaattisesti.

Seuraavissa osissa käsitellään niiden mukautusominaisuuksien laajuutta, jotka ovat **Täysi käyttöoikeus** -tason omaavien käyttäjien käytettävissä. Tässä on esimerkkejä kyseisistä ominaisuuksista:

- Pikavalikkovaihtoehdot
- **Mukauttamisen** työkalurivi
- Ruutujen, luetteloiden ja linkkien lisääminen työtiloihin
- Yhteenvedon lisääminen työtilasta koontinäyttöön
- Koontinäytön mukauttaminen

### <a name="shortcut-menu-options"></a>Pikavalikkovaihtoehdot

Pikavalikkojen avulla sivun käyttöliittymää voi eksplisiittisesti muuttaa muutamalla tavalla siten, että se vastaa paremmin omia tai organisaation vaatimuksia. (Pikavalikkoa kutsutaan myös *hiiren kakkospainikkeella avattavaksi valikoksi* ja *tilannevalikoksi*.)

Tietyt tavallisimmat ja tärkeimmät sivulle tehtävät muutokset ovat käytettävissä suoraan pikavalikon vaihtoehtoina. Ruudukon sarakkeita voi esimerkiksi lisätä tai piilottaa kätevästi napsauttamalla sarakeotsikkoa hiiren kakkospainikkeella ja valitsemalla sitten **Lisää sarakkeita** tai **Piilota tämä sarake**.

Lisäksi mukauttamisen yleisimmät tyypit saa käyttöön napsauttamalla elementtiä hiiren kakkospainikkeella ja valitsemalla **Mukauta**. (Huomaa, että kaikkia sivun elementtejä ei voida mukauttaa.). Kun valitset tämän mukauttamistavan, elementin *ominaisuusikkuna* tulee näkyviin.

![Elementin ominaisuuksien mukauttaminen.](./media/cli-element-property-window.png)

Voit mukauttaa elementtiä ominaisuusikkunassa seuraavilla tavoilla:

- Elementin otsikon muuttaminen.
- Elementin piilottaminen niin, ettei se näy sivulla. Kentän tietoja ei poisteta eikä muokata. Tiedot eivät vain enää näy sivulla.
- Pikavälilehden yhteenveto-osan tietojen sisällyttäminen (jos elementti on pikavälilehdessä).
- Ohita kenttä, jotta siihen ei koskaan kohdisteta, kun siirryt sivun läpi sarkaimella.
- Estä kentän tietojen muokkaaminen (mikä tahansa tietue).
- Määritä kenttä, joka vaaditaan tietojen syöttämistä varten. Jos tähän kenttään ei ole syötetty arvoa, siinä näkyy punainen reunus ja tähti, jotka ilmaisevat tämän tilan. Tämä vaihtoehto on käytettävissä vain versiosta 10.0.11 alkaen, kun [Tallennetut näkymät](saved-views.md) ja **Määritä kentät tarpeen mukaan mukautuksen avulla** -ominaisuudet on otettu käyttöön.

Ominaisuusikkunassa voi olla elementin mukaan myös muita mukauttamisominaisuuksia. Ruudun ominaisuusikkunassa voi esimerkiksi olla mahdollista viedä kyseisen ruutu ylös koontinäyttöön, kun taas oletuskoontinäytön elementtien ominaisuusikkunoissa voi luoda uuden mukautetun työtilan.

### <a name="personalization-toolbar"></a>Mukauttamisen työkalurivi

Jos haluat tehdä useita muutoksia sivulle tai muutoksia, jotka eivät ole käytettävissä muiden mekanismien kautta (jos esimerkiksi haluat muuttaa elementtien järjestystä), voit käyttää **Mukauttaminen**-työkaluriviä. Voit avata **Mukauttaminen**-työkalurivin seuraavilla tavoilla:

- Valitse **Ctrl+Vaihto+P** sivun missä tahansa elementissä.
- Valitse **Mukauta tämä sivu** elementin ominaisuusikkunassa.
- Valitse **Mukauta tätä sivua** minkä tahansa sivun toimintoikkunan **Asetukset**-välilehden **Mukauttaminen**-ryhmässä.
- Valitse **Asetukset**-painike siirtymispalkissa ja valitse sitten **Mukauta**.

[![Mukauttamisen työkalurivi.](./media/restyledPersonalizationToolbar.png)](./media/restyledPersonalizationToolbar.png)

#### <a name="navigating-the-page"></a>Siirtyminen sivulla

Kun **Mukautus**-työkalurivi on auki, taustalla oleva sivu on vain luku -muodossa (tietoja ei siis voi muuttaa) mutta on edelleen vuorovaikutteinen. Voit laajentaa tai kutistaa **Aiheeseen liittyviä tietoja** -ruudun, vaihtaa välilehtiä ja laajentaa tai kutistaa osia tavanomaiseen tapaan. Voit ottaa kutistettavaan osaan tai välilehteen kohdistuvan mukautuksen (esimerkiksi pikavälilehden piilottamisen) käyttöön valitsemalla painikkeen, joka tulee näkyviin kyseisen osan tai välilehden viereen, kun kohdistat siihen näppäimistöllä tai liikutat hiirtä sen yläpuolella.

#### <a name="personalization-tools"></a>Mukauttamisen työkalut

**Mukauttamisen** työkalurivillä on seuraavat työkalut:

- Valitse elementin ominaisuuksia ja muuta niitä **Valitse**-työkalulla. Voit käyttää tätä työkalua valitsemalla työkalurivin **Valitse**-painikkeen ja valitsemalla sitten haluamasi elementin. Elementin ominaisuusikkuna avautuu. Voit muuttaa elementin kaikkia ominaisuuksia. Voit toistaa prosessin muille kyseisen sivun mukautettaville elementeille. Ota huomioon, että kaikki mukautusominaisuudet eivät välttämättä ole käytettävissä kaikissa tilanteissa. Et esimerkiksi voi lukita pakollista kenttää.
- Voit piilottaa elementin sivulla **Piilota**-työkalulla. Voit käyttää tätä työkalua valitsemalla työkalurivin **Piilota**-painikkeen ja valitsemalla piilotettavan elementin. Kun käytät **Piilota**-työkalua, kaikki tällä hetkellä piilotettuna olevat elementit tulevat näkyviin varjostetussa säilössä. Voit tehdä elementistä näkyvän valitsemalla sen. Valitsemalla toisen mukautustyökalun tai sulkemalla mukautuksen työkalurivin näet, miltä sivu näyttää, kun elementit piilotetaan.
- Voit lisätä sivullesi kenttiä **Lisää kentät** -työkalun avulla. Tällä työkalulla voidaan lisätä vain sivumääritykseen sisältyviä kenttiä. Lisätietoja nykyisen sivumääritelmän ulkopuolisten uusien kenttien luomisesta on kohdassa [Mukautettujen kenttien luominen ja käyttäminen](user-defined-fields.md). Sinun on valittava työkalurivin **Lisää kentät** -painikkeen valitsemisen jälkeen ensin ruudukko tai osa, johon haluat lisätä kentän. Valintaikkunassa näkyy luettelo valittuun ruudukkoon tai osaan liittyvistä kentistä. Valitse valintaikkunassa ainakin yksi kenttä, joka lisätään joko **Suositellut kentät**- tai **Kaikki kentät** -luetteloon. Valitse kenttien valitseminen jälkeen **Päivitä**. Voit poistaa aiemmin lisätyn kentän toistamalla edellä mainitut vaiheet mutta poistamalla valintaikkunassa kentän valinnan.

    **Suositellut kentät** -luettelossa näkyvät kentät, jotka organisaation muut käyttäjät ovat aiemmin lisänneet. Tämä kenttäluettelo päivitetään **Suosituksen erätyö** -kohdan toistovälin perusteella. Kokemus on vastaavanlainen kuin lisättäessä uusia suodatinkenttiä sivun Suodatin-ruudussa.

- Voit siirtää elementin **Siirrä**-työkalulla toiseen sijaintiin nykyisen elementtiryhmän sisällä. Ota huomioon, ettet voi siirtää elementtiä sen pääryhmän ulkopuolelle. Voit käyttää tätä työkalua valitsemalla työkalurivin **Siirrä**-painikkeen ja valitsemalla siirrettävän elementin. Kun valitset elementin, sovellus määrittää sijainnit, joihin elementti voidaan siirtää. Näitä sijainteja kutsutaan *pudotusalueiksi*. Kun vedät elementtiä valitussa ryhmässa, värillinen lihavoitu viiva osoittaa pudotusalueen, johon elementti voidaan pudottaa.
- Voit poistaa elementin nykyisen sivun näppäimistön sarkaimella tehtävistä valinnoista **Ohita**-työkalulla. Kun valitset työkalurivin **Ohita**-painikkeen, kaikki tällä hetkellä ohitettavat elementit näkyvät varjostetussa säilössä. Voit lisätä kenttiä sarkainjärjestykseen ja poistaa niitä vuorovaikutteisesti.
- Voit lisätä kentän pikavälilehtien yhteenveto-osaan käyttämällä **Näytä otsikossa**-työkalua. Kun valitset työkalurivin **Näytä otsikossa**-painikkeen, kaikki yhteenvetokentiksi valitut kentät näkyvät varjostetussa säilössä. Voit lisätä kenttiä vuorovaikutteisesti pikavälilehden yhteenvetoon ja poistaa kenttiä niistä valitsemalla kenttiä.
- Määritä **Vaadi**-työkalulla elementti, joka tarvitaan tietojen syöttämiseen. Kun valitset työkalurivin **Vaadi**-painikkeen, kaikki tarvittavat elementit, jotka on räätälöity niiden tekemiseksi tarvittaviksi näkyvät varjostetussa säilössä. Voit sitten määrittää ne takaisin ei vaadittaviksi. Tämä vaihtoehto on käytettävissä versiossa 10.0.12 ja myöhemmin, kun **Määritä kentät tarpeen mukaan mukautuksen avulla** -ominaisuus on otettu käyttöön.
- **Lukitse**-työkalulla voit merkitä, onko elementti muokattavaissa vai ei. Kun valitset työkalurivin **Lukitse**-painikkeen, kaikki elementit, jotka eivät tällä hetkellä ole muokattavissa, näkyvät varjostetussa säilössä. Voit sitten määrittää ne takaisin muokattaviksi. Huomaa, että jotkut kentät ovat pakollisia, eikä niiden muokkausta voi estää. Näiden kenttien vieressä on lukkokuvake.
- Käytä **Lisää sovellus Power Appsista** -työkalulla upottaaksesi sivulle sovelluksen, joka on luotu Microsoft Power Appsilla. Lisätietoja Power Apps -sovelluksen upottamisesta sivulle on kohdassa [Power Apps -sovellusten upottaminen](embed-power-apps.md). Tämä vaihtoehto on käytettävissä vain, kun [Tallennetut näkymät](saved-views.md) -toiminto on poistettu käytöstä.
- Käytä **Lisää sovellus** -painiketta upottaaksesi sivulle sovelluksen, joka on joko Microsoft Power Appsin tai kolmannen osapuolen luoma. Tämä vaihtoehto on käytettävissä vain, kun [Tallennetut näkymät](saved-views.md) -toiminto on otettu käyttöön. 
- Voit palauttaa sivun oletusasennustilaan **Tyhjennä**-työkalulla. Kaikki senhetkisen sivun mukautukset tyhjennetään. Tätä toimintoa ei voi kumota. Käytä tätä työkalua tämän vuoksi vain silloin, kun olet varma, että haluat palauttaa sivun alkuperäiset asetukset. Kun **Tallennetut näkymät** -ominaisuus on käytössä, tämä työkalu tyhjentää nykyisen näkymän mukautukset.
- Voit ladata mukautuksen aiemmin luodusta tiedostosta käyttämällä **Tuo**-työkalua. 

    - Kun **Tallennetut näkymät** -ominaisuus ei ole käytössä, voit määrittää, lisätäänkö olemassa olevat mukautukset sivulle tuotaviin mukautuksiin vai korvataanko ne. Tätä toimintoa ei voi kumota. Siksi sinun on manuaalisesti tyhjennettävä tai kumottava ei-toivotut muutokset, kun olet tuonut mukautuksia.
    - Kun **Tallennetut näkymät** -ominaisuus on käytössä, tuodut mukautukset ovat osa sivun näkymää. Jos näkymä on jo olemassa, voit halutessasi ohittaa tuonnin, korvata nykyisen näkymän, jolla on sama nimi, tai nimetä tuodun näkymän uudelleen.

- Voit tallentaa sivun mukautukset tiedostoon käyttämällä **Vie**-työkalua. Sitten voit jakaa mukautuksesi muiden käyttäjien kanssa. Kyseisten käyttäjien tarvitsee vain tuoda sivun mukautukset sisältävä tiedosto. Kun **Tallennetut näkymät** -ominaisuus on käytössä, tämä työkalu tallentaa nykyisen näkymän tiedostoksi jakamista varten.
- Sulje **mukauttamisen** työkalurivi valitsemalla **Sulje**-painike. Sivu palautuu nyt alkuperäiseen vuorovaikutteiseen tilaan.

Yleensä **Mukautus**-työkaluriviä käytettäessä mukautukset tulevat voimaan heti, kun ne on tehty. Jos [Tallennetut näkymät](saved-views.md) -ominaisuus kuitenkin on käytössä, sinun on erikseen tallennettava mukautukset valitsemaasi näkymään.

Joissain tapauksissa työkalua valittaessa elementin vieressä näkyy lukkokuvake. Tämä kuvake ilmaisee, että valittuun työkaluun liittyviä elementin ominaisuuksia ei voi muokata, koska kyseisten ominaisuuksien muutokset estävät sivun odotetun toiminnan.

### <a name="adding-tiles-lists-and-links-to-a-workspace"></a>Ruutujen, luetteloiden ja linkkien lisääminen työtilaan

Joillakin luetteloja sisältävillä sivuilla on käytettävissä **Lisää työtilaan** -mukautusominaisuus toimintoruudun **Asetukset**-välilehden **Mukauta**-ryhmässä. Tällä ominaisuudella voit siirtää tarvittavia tietoja kulloisestakin luettelosta tiettyyn työtilaan. Työtilassa näkyviin tulevat tiedot voivat perustua joko koko luetteloon tai suodatettuun ja lajiteltuun luettelon versioon. Voit myös määrittää, näkyvätkö tiedot työtilassa luettelona, luettelon nimikkeiden määrän näyttävänä yhteenvetoruutuna vai linkkinä.

> [!NOTE]
> Jos [Tallennetut näkymät](saved-views.md) -toiminto on käytössä, työtilaan siirrettävä sisältö on linkitetty suoraan näkymään. Näkymän kyselyä käytetään tietojen noutamiseen työtilassa ja vastaavaa työtilan ruutu tai linkki avaa kyseisen näkymän sivun, jolloin näkymän kyselyä ja mukautuksia sovelletaan siihen. Jos näkymä päivitetään, vastaavat työtilan elementit mukautetaan uuteen näkymän määritykseen.

[![Lisää työtilaan.](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png)

- Voit lisätä luettelon työtilaan lajittelemalla tai suodattamalla luettelon ensin sivulla niin, että tiedot näkyvät siinä muodossa kuin haluat niiden näkyvän työtilassa. (Jos **Tallennetut näkymät** -toiminto on käytössä, et voi jatkaa, ennen kuin olet tallentanut näkymän näillä ehdoilla.) Valitse sitten **Lisää työtilaan**. Valitse ensin työtila ja sitten **Esittely**-kentässä **Luettelo**. **Konfiguroi**-asetuksen valinnan jälkeen avautuu valintaikkuna, jossa voit valita työtilan luettelossa näytettävät sarakkeet. Voit myös määrittää työtilan luettelossa käytettävän otsikon.
- Voit lisätä ruudun työtilaan suodattamalla ensin sivun luettelon niin, että se näyttää vain tiedot, joista tehdään yhteenveto tai joita haluat käyttää nopeasti. (Jos **Tallennetut näkymät** -toiminto on käytössä, et voi jatkaa, ennen kuin olet tallentanut näkymän näillä ehdoilla.) Valitse sitten **Lisää työtilaan**. Valitse ensin työtila ja sitten **Esittely**-kentässä **Ruutu**. **Konfiguroi**-asetuksen valinnan jälkeen avautuu valintaikkuna, jossa voit määrittää työtilan ruudussa käytettävän otsikon. Voit myös määrittää, näytetäänkö määrä ruudussa. Kun ruutu on lisätty työtilaan voit valita, että se avaa kulloisenkin sivun työtilasta. Sen jälkeen voit tarkastella ruutuun liittyvää suodatettua luetteloa.
    - Alkaen versiosta 10.0.26, jos **Salli käyttäjien valita ja muuttaa ruutukokoja** -ominaisuus on otettu käyttöön,voit valita uudelle ruudulle yhden neljästä käytettävissä olevan **ruudun koosta** **Konfiguroi ruutu** -valintaikkunassa. Tämän ominaisuuden avulla voit myös säätää ruudun kokoa sen jälkeen, kun se on luotu suoraan työtilasta.   
- Voit lisätä linkin työtilaan suodattamalla ensin sivun luettelon näyttämään vain ne tiedot, joista olet kiinnostunut. (Jos **Tallennetut näkymät** -toiminto on käytössä, et voi jatkaa, ennen kuin olet tallentanut näkymän näillä ehdoilla.) Valitse sitten **Lisää työtilaan**. Valitse ensin työtila ja sitten **Esittely**-kentässä **Linkki**. **Konfiguroi**-asetuksen valinnan jälkeen avautuu valintaikkuna, jossa voit määrittää linkin yhteydessä käytettävän otsikon. Voit myös halutessasi määrittää sen osan otsikon, johon linkki voidaan sijoittaa. Jos osaa ei ole, uusi osa luodaan.

> [!NOTE]
> Versiosta 10.0.25 lähtien luettelon, ruudun tai linkin määrityksen jälkeen on ehkä valittava työtilanäkymät, johon haluat lisätä elementin , jos **(Esiversio) Tallennettujen näkymien tuki työtiloille** -toiminto on otettu käyttöön. Käytettävissä olevat työtilanäkymät näkyvät kunkin **Konfiguroi**-valintaikkunan **Työtilan vaihtoehdot** -osassa. 

Kun olet lisännyt luettelon, ruudun tai linkin työtilaan, voit avata kyseisen työtilan ja muuttaa sen elementtien järjestystä tarpeen mukaan.

### <a name="adding-a-summary-from-a-workspace-to-a-dashboard"></a>Yhteenvedon lisääminen työtilasta koontinäyttöön

Joissakin työtiloissa on lukumääräruutuja (ruutuja, joissa on numeroita). On mahdollista, että haluat nähdä kyseiset ruudut myös koontinäytössä. Napsauta työtilassa hiiren kakkospainikkeella **Mukauta** ja valitse ruudun ominaisuusikkunassa **Kiinnitä koontinäyttöön**. Kun seuraavan kerran avaat ja päivität valitun koontinäytön, lukumäärä näkyy kyseisen työtilan siirtymisruudun alapuolella. Voit valita, että tämä lukumäärä, siirtyy suoraan tietoihin, joihin se viittaa.

### <a name="changing-the-size-of-a-tile"></a>Ruudun koon muuttaminen
Versiosta 10.0.26 alkaen **Salli käyttäjien valita ja muuttaa ruutukokoja** -ominaisuuden avulla käyttäjät voivat muokata muiden kuin KPI-ruutujen kokoa personoinnin avulla. Napsauta työtilassa ruutua hiiren kakkospainikkeella ja valitse sitten **Mukauta**. Valitse ruudun ominaisuusikkunassa haluamasi koko **Ruudun koko** -asetuksista. Ruudun koko muutetaan välittömästi. Jos **(Esiversio) Tallennettujen näkymien tuki työtiloille** -toiminto on käytössä , voit tallentaa tämän mukauttaminsen työtilanäkymään.  

### <a name="personalizing-your-dashboard"></a>Koontinäytön mukauttaminen

Koontinäyttö on usein ensimmäinen sivu, jonka näet, kun avaat sovelluksen. Se voidaan mukauttaa kuten mikä tahansa muu järjestelmän sivu käyttämällä samoja mekanismeja, jotka on kuvattu aiemmin tässä artikkelissa. 

> [!WARNING]
> Kun nyt piilotat sisältöä koontinäytössä, on tärkeää kohdistaa ruutu suoraan, ei sen ympärillä olevaa tilaa. Jos piilotat ryhmän ruudun ympärillä, tulokset voivat olla odottamattomia, jos lisää ruutuja lisätään myöhemmin tai jos järjestelmä vaihdetaan eri kielelle.

Yksi ainutlaatuinen mukautusominaisuus, joka on käytettävissä koontinäytössä, on mahdollisuus lisätä ruutuja. 

- Jos **Koko sivun sovellukset** -ominaisuus on pois käytöstä, voit lisätä uuden ruudun valitsemalla elementin hiiren oikeanpuoleisella painikkeella koontinäytössä ja valitsemalla sitten **Lisää työtila**. Uusi työtilan ruutu luodaan koontinäytön alareunaan. Voit nimetä tämän uuden työtilan ruudun haluamallasi tavalla. Voit myös lisätä luetteloita, ruutuja ja linkkejä työtilaa aiemmin tämän artikkelin kohdassa [Ruutujen, luetteloiden ja linkkien lisääminen työtilaan](personalize-user-experience.md#adding-tiles-lists-and-links-to-a-workspace) kuvatulla tavalla.
- Jos **Koko sivun sovellukset** -ominaisuus on pois käytöstä, voit lisätä uuden ruudun valitsemalla elementin hiiren oikeanpuoleisella painikkeella koontinäytössä ja valitsemalla sitten **Lisää sovellus**. Määritä valintaikkunassa, haluatko lisätä ruudun uuteen työtilaan tai ruutuun, jolla on sisältöä Power Appsista tai verkkosivulta. Määritä sitten valitsemasi vaihtoehto ohjeiden mukaan. Uusi ruutu luodaan koontinäytön alareunaan. Lisätietoja näiden upotettujen sovellusten lisäämisestä, muokkaamisesta, poistamisesta ja jakamisesta on kohdissa [Pohjaan perustuvien sovellusten upottaminen Power Appsista](embed-power-apps.md) ja [Kolmannen osapuolen sovellusten upottaminen](embed-website.md).

## <a name="sharing-personalizations"></a>Mukauttamisen jakaminen

Kun olet mukauttanut sivun, voit jakaa mukautukset muiden käyttäjien kanssa muutamalla tavalla. Seuraavassa luettelossa menetelmät järjestetään suositeltavimmista vähiten suositeltavimpiin.

1. Julkaise näkymiä käyttäjille.
2. Kopioi näkymiä tai mukautuksia käyttäjille.
3. Vie ja tuo näkymiä tai mukautuksia.

### <a name="publish-views-to-users"></a>Julkaise näkymiä käyttäjille

Jos [Tallennetut näkymät](saved-views.md) -toiminto on käytössä ja jos sivu tukee näkymiä, paras tapa jakaa mukautuksia muiden käyttäjien kanssa on julkaista näkymä käyttäjille, joilla on vähintään yksi käyttöoikeusrooli. Lisätietoja on kohdassa [Julkaisunäkymät](saved-views.md#publishing-views).

### <a name="copy-views-or-personalizations-to-users"></a>Kopioi näkymiä tai mukautuksia käyttäjille

Jos [Tallennetut näkymät](saved-views.md) -toiminto on poistettu käytöstä tai jos sivu ei tue näkymiä, suositeltu tapa jakaa mukautuksia on kopioida ne käyttäjien välillä. Tämä menetelmä on vain käyttöoikeuden omaavien käyttäjien (esimerkiksi järjestelmänvalvojien) käytettävissä. Järjestelmänvalvojat voivat kuitenkin etsiä tietyn käyttäjän mukautuksen järjestelmästä (mukaan lukien käyttäjän oman näkymän, jos tallennetut näkymät ovat käytössä) ja kopioida konfiguraation muille käyttäjille.

Jos tallennetut näkymät ovat käytössä, kopioi mukautukset noudattamalla näitä ohjeita.

1. Valitse **Järjestelmänvalvonta \> Asetukset \> Mukauttaminen**.
2. Kopioi henkilökohtaiset näkymät noudattamalla seuraavia vaiheita:

    1. Valitse **Henkilökohtaiset näkymät**.
    2. Valitse luettelosta haluamasi näkymät.
    3. Valitse **Kopioi käyttäjille**.
    4. Valitse käyttäjät, joille näkymät jaetaan.

    Seuraavien vaiheiden avulla voit kopioida mukautuksia sivuille, jotka eivät tue näkymiä:

    1. Valitse **Käyttäjäasetukset**.
    2. Valitse käyttäjä, jolla on jaettava mukautus.
    3. Valitse **Hallitse kaikkia mukautuksia**.
    4. Valitse luettelosta haluamasi mukautukset.
    5. Valitse **Kopioi käyttäjille**.
    6. Valitse käyttäjät, joille mukautukset jaetaan.

Jos tallennetut näkymät eivät ole käytössä, kopioi mukautus noudattamalla näitä ohjeita.

1. Valitse **Järjestelmänvalvonta \> Asetukset \> Mukauttaminen**.
2. Valitse **Käytä**.
3. Valitse käyttäjät, joille mukautus jaetaan.
4. Valitse **Valitse aiemmin luotu mukautus**.
5. Etsi ja valitse haluamasi (yksittäinen) mukautus.
6. Valitse **OK**.

### <a name="export-and-import-views-or-personalizations"></a>Vie ja tuo näkymiä tai mukautuksia

Mukautuksia voidaan jakaa myös viennin ja tuonnin kautta. Yksittäiset käyttäjät tai järjestelmänvalvoja, joka toimii heidän puolestaan, voivat viedä mukautuksen tai näkymiä tämän menetelmän avulla ja antaa viedyn tiedoston sitten toisille käyttäjille tuontia varten. Vaihtoehtoisesti käyttäjät voivat antaa viedyt mukautukset käyttäjälle, jolla on järjestelmänvalvojan käyttöoikeudet. Tällöin käyttäjä voi käyttää mukautustiedostoa samalla kertaa useille käyttäjille **Mukauttaminen**-hallintasivulla.

> [!IMPORTANT]
> Koska mukautukset säilyvät päivityksestä toiseen, kaikkien mukautusten uudelleentuonti palvelupäivityksen jälkeen tai joskus muulloin on tarpeetonta eikä sitä missään nimessä suositella.

#### <a name="export"></a>Vie

Yleensä voit viedä oman näkymäsi tai mukautuksesi avaamalla haluamasi sivun, avaamalla **Mukauttaminen**-työkalurivin ja valitsemalla sitten **Vie**. Lisätietoja työkalurivistä on tämän artikkelin aiemmassa kohdassa [Mukauttamisen työkalurivi](#personalization-toolbar). Jos [tallennetut näkymät](saved-views.md) ovat käytettävissä, voit tarkastella luetteloa kaikista järjestelmän mukautuksista valitsemalla **Asetukset \> Käyttäjän asetukset \> Mukauttaminen**. Sieltä voit valita vietävien näkymien tai mukautusten tiedot ja valita sitten **Vie**.

Järjestelmänvalvojat voivat lisäksi viedä muiden käyttäjien mukautuksia noudattamalla seuraavia vaiheita.

1. Valitse **Järjestelmänvalvonta \> Asetukset \> Mukauttaminen**.
2. Valitse haluttu käyttäjä **Käyttäjät**-välilehdessä.
3. Etsi ja valitse haluamasi näkymä tai mukautus.
4. Valitse **Vie**.

#### <a name="import"></a>Tuo

Voit tuoda näkymän tai mukautuksen avaamalla **Mukauttaminen**-työkalurivin ja valitsemalla **Tuo**. Lisäksi järjestelmänvalvojat voivat tuoda tiedoston ja antaa sen välittömästi vähintään yhdelle käyttäjälle.

Jos tallennetut näkymät ovat käytössä, noudata näitä ohjeita.

1. Valitse **Järjestelmänvalvonta \> Asetukset \> Mukauttaminen**.
2. Valitse toimintoruudussa **Tuo näkymiä \> Käyttäjän näkymät**.
3. Valitse tuontitila:

    - **Valitse tietyt käyttäjät** – Anna näkymä tai mukauttaminen valituille käyttäjille.
    - **Tuo sellaisenaan** - Tuo näkymä tai mukautus samalle käyttäjälle, joka on vienyt sen.

4. Valitse **Selaa** ja etsi ja valitse tuotava mukautus.
5. Valitse **Seuraava**.
6. Jos valitsit vaiheessa 3 **Valitse tietyt käyttäjät**, valitse käyttäjät, joille mukautus tuodaan.
7. Valitse **Tuo**.
8. Ratkaise ristiriitoja tarpeen mukaan.

Jos tallennetut näkymät eivät ole käytössä, noudata näitä ohjeita.

1. Valitse **Järjestelmänvalvonta \> Asetukset \> Mukauttaminen**.
2. Valitse **Käytä**.
3. Valitse käyttäjät, joille mukautus jaetaan.
4. Valitse **Tuo mukautuksia tiedostosta**.
5. Valitse **Selaa** ja etsi ja valitse tuotava mukautus.
6. Valitse **OK**.

## <a name="administration-of-personalizations"></a>Mukautusten hallinta

**Mukautus**-sivu on keskitetty keskus, jolla hallitaan räätälöintejä organisaatiotasolla. Tämän sivun sisältö ja ominaisuudet määräytyvät sen mukaan, onko **Tallennetut näkymät** -toiminto otettu käyttöön.

Jos asiakas on ottanut käyttöön **Tallennetut näkymät** -toiminnon, lue Näkymien hallinta yleisesti -osa [Tallennetut näkymät](saved-views.md) -artikkelista.

Niillä asiakkaila, jotka eivät ole vielä ottaneet käyttöön [Tallennetut näkymät](saved-views.md) -ominaisuutta, tällä sivulla on neljä välilehteä:

- **Käytä** – Voit tuoda tai valita yhden tai usean käyttäjän mukautuksen. Jos mukautus otetaan käyttöön yhdelle tai usealle käyttäjälle, ensiksi valitaan rooli ja käyttäjät, joilla tämä rooli on. Valitse sitten joko aiemmin luotu mukautus, jota haluat käyttää valituille käyttäjille, tai tuo mukautustiedosto. Mukautuksen oikeellisuus tarkistetaan ja sitä käytetään kaikille käyttäjille, kun he seuraavan kerran avaavat valitun sivun.
- **Tyhjennä** – Voit tyhjentää yhden tai usean käyttäjän sivun tai työtilan kaikki mukautukset. Valitse ensin sivu tai työtila. Näet nyt luettelon käyttäjistä, jotka ovat mukauttaneet sitä. Valitse sitten käyttäjät, joiden sivun tai mukautukset on tyhjennettävä. Valitse lopuksi **Tyhjennä**. Kaikki mukautukset, joita valitut käyttäjät ovat käyttäneet valitulla sivulla tai valitussa työtilassa, poistetaan. Tätä toimintoa ei voi kumota. Jos sivulla tai työtilassa on kuitenkin tallennettuja mukautuksia, nämä mukautukset voidaan tuoda uudelleen.
- **Käyttäjät** – Valitse käyttäjä, kun haluat tarkastella käyttäjän mukauttamien sivujen luetteloa. Voit sitten sallia käyttäjän käyttävän mukautuksia tietyillä sivuilla tai koko järjestelmässä tai estää sen. Voit myös tuoda, viedä tai tyhjentää käyttäjän mukautuksen. Lisäksi voit palauttaa käyttäjän kuvatekstitoiminnot. Jos käyttäjä tällöin on aiemmin hylännyt uusia ominaisuuksia esitteleviä ponnahdusikkunoita, ne tulevat näkyviin uudelleen, kun kyseinen käyttäjä kohtaa kyseiset ominaisuudet.
- **Järjestelmä** – Voit poistaa kaikkien järjestelmän käyttäjien mukautukset käytöstä väliaikaisesti. Tällöin kaikkien käyttäjien mukautukset poistetaan ja kaikki sivut palautetaan oletustiloihinsa. Jos otat mukautukset myöhemmin jälleen käyttöön, kaikkia mukautuksia sovelletaan uudelleen. Voit poistaa tässä välilehdessä kaikkien järjestelmän käyttäjien mukautukset myös pysyvästi. Poistettuja mukautuksia ei voi palauttaa. Varmista tämän vuoksi ennen tämän tehtävän suorittamista, että olet vienyt kaikki ne mukautukset, jotka ehkä tarvitset myöhemmin.

### <a name="service-updates-and-personalization"></a>Palvelupäivitykset ja mukauttaminen
Mukautustietoja ei tarvitse tyhjentää tai nollata, kun siirrytään tuotteen uuteen versioon. Mukautukset ja tallennettujen näkymien tiedot toimivat päivitysten välillä. Poikkeuksia tähän ovat muutokset itse lomakkeeseen silloin, kun mukautus mitätöidään (kuten poistettu ohjausobjekti) tai muutokset lomakkeen peruskyselyyn. Se muuttaa lomakkeen tietolähteen alipuuta niin, että se ei enää vastaa näkymäkyselyyn liittyvän tietolähteen alipuuta.

## <a name="personalizing-inventory-dimensions"></a>Varastodimensioiden mukauttaminen

Kun mukautat varastodimension asetuksia sivulla, pidä mielessä **Näytä dimensio** -asetuksen avulla luodut asetukset. Voit esimerkiksi piilottaa eränumeron varastodimension sarakkeen mukautuksen avulla. Sarake kuitenkin näkyy, kun sivu avataan seuraavan kerran. Tämä on mahdollista, koska **dimension näyttöasetukset** määrittävät varastodimension näytettävät sarakkeet. **Dimension näyttöasetuksia** käytetään kaikilla sivulla, ja ne korvaavat kaikki yksittäisten sivujen mukautetut varastodimension kenttien asetukset.

Jos et siis halua edellisessä esimerkissä, että varastodimension eränumero näkyy sivulla, kyseisen dimension valinta on poistettava kyseisen sivun taulukon **Näytä dimensiot** -vaihtoehdon osana.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
