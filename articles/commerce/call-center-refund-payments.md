---
title: Hyvitysmaksujen käsittely puhelinkeskuksissa
description: Tässä artikkelissa kerrotaan, miten maksun hyvitykset luodaan puhelinkeskuksen kautta, kun palautukset luodaan tai kun tilaukset tai tilausrivit peruutetaan.
author: hhainesms
ms.date: 01/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: b1f3462529d501d9a5c279fd15dec69cb447cd51
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276916"
---
# <a name="refund-payment-processing-in-call-centers"></a>Hyvitysmaksujen käsittely puhelinkeskuksissa

Tässä artikkelissa kerrotaan, miten maksun hyvitykset luodaan puhelinkeskuksen kautta, kun palautukset luodaan tai kun tilaukset tai tilausrivit peruutetaan.

Käyttäjä, joka luo asiakkaalle palautustilauksen puhelukeskuksen käyttäjänä Microsoft Dynamics 365 Commerce headquarters -sovelluksessa, luo palautuksen valtuutuksen (RMA) **Palautustilaus** -sivulla. RMA määrittää tuotteet, jotka asiakas haluaa palauttaa tai vaihtaa, ja se luo linkitetyn palautusmyyntitilauksen, jonka tilaustyyppi on **Palautettu tilaus**. Tätä linkitettyä palautettua tilausta käytetään seuraamaan palautetun varaston kirjaamista sekä kirjattuja hyvityslaskuja tai maksun palautuksia.

Jos **Ota käyttöön tilausten viimeistely** -asetus on **Kyllä** puhelinkeskuskanavalle, RMA:n luovan soittokeskuksen käyttäjän on suoritettava tilauksen valmistumiskäsittely valitsemalla **Palautustilaus**-sivulla **Valmis**. **Valmis**-toiminto sisältää lasketun palautusyhteenvedon, joka sisältää erääntyvan hyvityssumman. Kun se on määritetty oikein, järjestelmä luo järjestelmällisesti palautusmaksurivin palautetulle tilaukselle.

Puhelinkeskuksen logiikka määrittää maksurivin maksutavan alkuperäisessä tilauksessa käytetyn maksutavan mukaan. Jos luotua palautustilausta ei ole linkitetty alkuperäiseen tilaukseen, järjestelmäparametrista otettua oletusmaksutapaa käytetään.

## <a name="how-a-call-center-determines-which-payment-method-to-apply-to-a-return-order"></a>Miten puhelukeskus määrittää, mitä maksutapaa palautustilauksessa käytetään?

Soittokeskus määrittää palautustilauksessa käytettävän maksutavan alkuperäisen tilauksen maksutavan avulla. Tämän prosessin toimintatavat ovat seuraaville alkuperäisille maksutavoille:

- **Normaali** (käteinen) tai **Sekki** – Kun luotu palautustilaus viittaa alkuperäiseen tilaukseen, joka on maksettu normaalin (käteis-) tai sekkimaksutyypin avulla, soittokeskuksen sovellus viittaa **Puhelinkeskuksen palautusmenetelmät** -sivun konfiguraatioihin. Tällä sivulla organisaatiot voivat määrittää tilausvaluutan mukaan, miten asiakkaille myönnetään palautusten hyvitykset tilauksista, jotka on alun perin maksettu normaalin tai sekin maksutavan mukaan. **Puhelinkeskuksen hyvitysmenetelmät** -sivulla organisaatiot voivat myös valita, lähetetäänkö asiakkaalle järjestelmän luoma hyvityssekki. Näissä tilanteissa soittokeskuksen logiikka viittaa palautustilauksen valuuttaan ja luo sitten **Vähittäismyynnin maksutapa** -arvon avulla palautusmyyntitilaukseen palautusmaksurivin kyseisenä valuuttana. Valuuttaan linkitetään myöhemmin myyntireskontran asiakkaan maksukirjauskansio, joka käyttää määritettyä myyntireskontran maksutapaa.

    Seuraavassa kuvassa esitetään skenaarion konfiguraatio, jossa asiakas palauttaa tuotteet USD-valuuttaan linkitetystä myyntitilauksesta, joka on alunperin maksettu normaali- tai sekkimaksulajin mukaan. Tässä skenaariossa asiakkaalle hyvitetään järjestelmän luoma palautussekki. **REF-CHK** -myyntireskontramaksutapa on määritetty hyvityssekin maksutyypiksi.

    ![Soittokeskuksen palautustapojen konfiguroiminen alkuperäisille tavallisille ja sekkimaksuille.](media/callcenterrefundmethods.png)

    > [!NOTE]
    > Asiakastiliä ei tueta käteis- tai sekkimaksujen hyvitysmenetelmänä.

- **Luottokortti** – Kun luotu palautustilaus viittaa luottokortilla maksettuun alkuperäiseen tilaukseen, soittokeskuksen palautusmaksujen logiikka käyttää samaa alkuperäistä luottokorttia palautustilauksessa.
- **Kanta-asiakaskortti** – Kun luotu palautustilaus viittaa kanta-asiakaskortilla maksettuun alkuperäiseen tilaukseen, soittokeskuksen palautusmaksujen logiikka kohdistaa hyvityksen samaan kanta-asiakaskorttiin.
- **Lahjakortti** (sisäinen) – Kun luotu palautustilaus viittaa alkuperäiseen tilaukseen, joka on maksettu käyttämällä lahjakorttia, joka on myönnetty Dynamics 365 Commercesta (sisäinen lahjakorttitoiminto), puhelinkeskuksen palautusmaksun logiikka käyttää samaa alkuperäistä lahjakortin numeroa.
- **Lahjakortti** (ulkoinen) – Kun luotu palautustilaus viittaa alkuperäiseen tilaukseen, joka on maksettu ulkoisen kolmannen osapuolen lahjakortin avulla, puhelinkeskuksen palautusmaksujen logiikka käyttää palautusmaksun oletusmaksutapaa, joka on määritetty **Puhelinkeskuksen parametrit** -sivun **RMA/palautus**-välilehdessä.

Jos alkuperäisen tilauksen maksutyyppi on mistä tahansa syystä tuntematon tai alkuperäisen tilauksen maksamiseen on käytetty useita maksutapoja, soittokeskuksen logiikka käyttää palautusten oletusmaksumenetelmää, joka on määritetty **Puhelinkeskuksen parametrit** -sivun **RMA/Palautus**-välilehdessä.

Seuraavassa kuvassa näkyy **Maksutapa**-kenttä **RMA/Palautus**-välilehdessä **Puhelinkeskuksen parametrit** -sivulla.

![Maksutapa-kenttä RMA/Palautus-välilehdessä Puhelinkeskuksen parametrit -sivulla.](media/callcenterrefundparameters.png)

> [!NOTE]
> Aiemmin kuvatut palautusten käsittelysäännöt koskevat myös tilauksia tai tilausrivejä, jotka puhelinkeskuksen käyttäjä peruuttaa Commerce Headquarters -sovelluksessa. Jos tilauksen tai tiettyjen tilausrivien peruuttaminen aiheuttaa liikamaksun, samoja sääntöjä käytetään hyvitysmaksurivien luomiseksi.

Tavallisesti palautustilaus käy läpi vakioprosessin, jossa varasto vastaanotetaan (tai siirtyy hävikiksi), pakkausluettelo kirjataan palautustilausta vasten ja palautusmyyntitilaukselle suoritetaan laskun kirjausprosessi. Palautusmyyntitilaus linkitetään ja järjestelmällisesti luodaan osana palautustilauksen luontiprosessia. Tavallisissa tilanteissa maksuhyvitystä ei makseta asiakkaille ennen palautusmyyntitilauksen laskun kirjaamista.

### <a name="what-happens-when-an-invoice-is-posted-on-a-return-sales-order"></a>Mitä tapahtuu, kun lasku kirjataan palautusmyyntitilaukseen?

Seuraavat skenaariot selittävät, mitä tapahtuu, kun lasku kirjataan palautusmyyntitilaukseen:

- Jos palautustilauksen hyvitysmaksu on määritetty luottokortille, ohjelma aktivoi lisälogiikan, kun lasku kirjataan. Tämä logiikka kutsuu maksun käsittelijää hyvitysmaksun maksamiseksi asiakkaan luottokortille. Myös asiakkaan hyvitysmaksun tosite luodaan ja kirjataan järjestelmällisesti asiakkaan tilille. Tämä maksukirjauskansio täsmäytetään palautustilauksen hyvityslaskutosittetta vasten.
- Jos maksettava hyvitysmaksu on sekkimaksutyypille, luodaan myyntireskontran maksutapaa käyttävä asiakkaan maksutosite, joka on kirjattava tai tulostettava manuaalisesti, ennen kuin maksutosite voidaan kirjata asiakastilille. Hyvityssekin käsittelemiseksi käyttäjät voivat käyttää myyntireskontran **Asiakkaan maksukirjauskansio** -sivua tai Retailin ja Commercen **Palautussekin käsittely** -sivua.
- Jos myönnettävä hyvitysmaksu on määritetty sisäiselle lahjakortille tai kanta-asiakaskortin maksutyypille, palautustilauksen laskutuksen yhteydessä hyvitysmaksutosite luodaan ja kirjataan asiakastilille. Tämä laskutusvaihe myös lisää hyvityssumman takaisin asiakkaan sisäisesti seuratun lahjakortin saldoon tai kanta-asiakkuuspisteiden saldoon.
- Jos **Asiakas**-toimintoa (esimerkiksi asiakastiliä) käyttävä maksutapa on linkitetty palautusmyyntitilaukseen, luottorajatarkistukset ohitetaan maksun käsittelemisen yhteydessä. Tässä yhteydessä ei luoda tai kirjata maksutosittetta. Kun asiakkaan maksutyyppiä käytetään palautustilauksen yhteydessä, laskun kirjausprosessin luoma hyvityslaskutosite toimii asiakkaan hyvitystositteena ja osoittaa hyvityksen asiakkaan myyntireskontrasaldolle.

## <a name="advance-credit"></a>Ennakkohyvitys

Kun käyttäjä käsittelee palautustilauksia käyttäjänä soittokeskuksessa, jossa **Ota käyttöön tilausten viimeistely** asetus on **Kyllä**, aiemmin kuvatusta palautusmaksun kirjausprosessistaa voi poiketa, jos palautustilauksen luovan soittokeskuksen käyttäjä määrittää **Ennakkoluotto** -arvoksi **Kyllä** **Puhelinkeskuksen parametrit** -sivun **RMA/Palautus**-kentässä. Tässä tapauksessa maksun palautus tapahtuu heti palautustilauksen lähettämisen jälkeen käyttämällä **Palautuksen yhteenveto** -sivun **Lähetä**-toimintoa. Järjestelmä luo välittömästi ennakkomaksun asiakasmaksutositteen palautusarvolle, vaikka itse palautusmyyntitilausta ei ole vielä laskutettu. Tätä menetelmää voidaan käyttää tilanteissa, joissa organisaation pitää maksaa palautuksia ennakkoon asiakaspalveluongelman vuoksi, eikä se halua vaatia palautetun varaston vastaanottoa ennen palautusten hyvittämistä.

## <a name="replacement-orders"></a>Korvaavat tilaukset

Kun palautustilaus on myönnetty, **Korvaava tilaus** -toimintoa voidaan käyttää uuden myyntitilauksen luomiseksi asiakkaalle. Tätä menetelmää voidaan käyttää vaihtoskenaarioissa. **Korvaava tilaus** -toiminto luo uuden myyntitilauksen uusille lähetettäville nimikkeille, mutta **Puhelinkeskuksen parametrit** -sivun **RMA/Palautus**-välilehden ristiviittauslinkki linkittää korvaavan tilauksen, RMA:n ja palautetun myyntitilauksen.

Kun korvaavan tilauksen maksut käsitellään, organisaatioilla on kaksi vaihtoehtoa:

- Hyvitä palautustilauksen asiakkaalle alkuperäisen maksutavan mukaan ja kerää sitten erillinen maksu korvaavasta tilauksesta. Tämän vaihtoehdon käyttö ei vaadi lisäkonfiguraatiota.
- Määritä **Käytä hyvitystä** -asetukseksi **Kyllä** **RMA/Palautus**-välilehdessä **Puhelinkeskuksen parametrit** -sivulla. Tällöin asiakkaan maksutapaa sovelletaan järjestelmällisesti sekä palautustilaukseen että korvaavaan tilaukseen. Tämän vaihtoehdon avulla voit estää ulkoisen hyvityksen maksamisen. Se auttaa myös estämään tapahtuman maksukäsittelyn. Tämä voi olla hyödyllistä tilanteissa, joissa tasan menevää vaihtorahaa käsitellään, ja organisaatio haluaa käyttää palautustilauksen laskutuksen yhteydessä luotua hyvitystositetta korvaavan tilauksen luoman laskun maksamiseen. Kun **Käytä hyvitystä** -asetuksen arvoksi on määritetty **Kyllä**, organisaation on täsmäytettävä hyvityslasku manuaalisesti korvaavan tilauksen laskun kanssa, kun molemmat asiakirjat on luotu.

**Käytä hyvitystä** -asetuksen **Kyllä** -arvoa käytetään vain, kun palautustilaus linkitetään korvaavaan tilaukseen. Tässä tapauksessa asiakkaan maksutapa, jota käytetään järjestelmällisesti palautuksen ja vaihtotilauksen maksamiseen, määritetään **Puhelinkeskuksen parametrit** -sivun **RMA/Palautus**-välilehden **Käytä hyvitysmaksutapaa** -kentässä. Tässä kentässä voi valita vain **Asiakas**-toiminnon maksutyypin.

> [!NOTE]
> Jos palautustilauksen korvaavaa tilausta ei ole linkitetty, **Käytä hyvitystä** -asetuksen **Kyllä**-asetuksella ei ole vaikutusta palautustilauksen maksulogiikkaan, koska tämä asetus koskee vain korvaustilauksia.

![Käytä hyvitysmaksutapaa -kenttä RMA/Palautus-välilehdessä Puhelinkeskuksen parametrit -sivulla.](media/callcenterrefundparameters1.png)

> [!IMPORTANT]
> Jos käyttäjät, jotka luovat korvaavat tilaukset ja käyttävät **Käytä hyvitystä** -asetusta, he eivät saa suorittaa palautustilaukselle **Valmis**-toimintoa ennen kuin **Käytä hyvitystä** -vaihtoehdon arvona on **Kyllä**. Kun **Valmis**-toiminto on suoritettu, hyvitysmaksu lasketaan ja kohdistetaan palautusmyyntitilaukseen. Jos **Käytä hyvitystä** -asetuksen arvoksi yritetään määrittää **Kyllä**, kun hyvitysmaksu on jo laskettu ja kohdistettu, hyvitysmaksun uudelleenlaskenta käynnisty, eikä **Käytä hyvitysmaksutapaa** -kentässä valittua maksutapaa käytetä. Jos tässä yhteydessä on käytettävä **Käytä hyvitystä** -asetusta, käyttäjän on poistettava korvaava tilaus ja RMA ja aloitettava sen jälkeen alusta ja luoda uusi RMA. Tällöin käyttäjän on varmistettava, että **Käytä hyvitystä** -asetuksen arvo on **Kyllä**, ennen kuin **Valmis**-toiminto suoritetaan.

## <a name="payment-overrides-for-call-center-returns"></a>Puhelukeskuksen palautusten maksun ohitukset

Vaikka puhelukeskuksen logiikka systemaattisesti määrittää hyvitysmaksutavan aiemmin tässä artikkelissa kuvatulla tavalla, käyttäjät voivat joskus haluta ohittaa nämä maksut. Käyttäjä voi esimerkiksi muokata tai poistaa aiemmin luotuja hyvitysmaksurivejä ja ottaa käyttöön uusia maksurivejä. Järjestelmän laskemia hyvitysmaksuja voivat muuttaa vain käyttäjät, joilla on oikeat ohitusoikeudet. Nämä käyttöoikeudet voidaan konfiguroida Retailin ja Commercen **Ohitusoikeudet** -sivulla. Jos haluat käyttää hyvitysmaksun ohitusta, käyttäjä on linkitettävä suojausrooliin, jossa **Salli vaihtoehtoinen maksu** -asetuksen arvo on **Kyllä** **Ohitusoikeudet**-sivulla.

![Salli vaihtoehtoinen maksu -vaihtoehto Ohitusoikeudet-sivulla.](media/overridepermissions.png)

Vaihtoehtoisesti organisaatio voi määrittää **Puhelinkeskuksen parametri** -sivun **RMA/Palautus**-välilehdessä **Salli maksun ohitus** -asetuksen arvoksi **Kyllä**. Tässä tapauksessa **Suojauksen ohituskoodi** -kentässä on valittava suojauksen ohituskoodi. Suojauksen ohituskoodi on aakkosnumeerinen koodi, jota on hallittava ulkoisesti, koska käyttäjät eivät voi tarkastella koodia Commerce Headquartersissa sen määrittämisen jälkeen. Vain muutaman organisaation luotettavan henkilön tulisi tietää suojauksen ohituskoodi. Jos **Salli maksun ohitus** -asetus on **Kyllä** ja kaikki käyttäjät, joilla ei ole oikeita roolin käyttöoikeuksia, yrittävät muuttaa palautustilauksen maksutapaa, he voivat määrittää suojauksen ohjauskoodin. Jos he eivät tiedä sitä tai esimies tai valvoja ei voi syöttää sitä sivulle, he eivät voi ohittaa palautuksen maksumenetelmää.

> [!NOTE]
> Jos suojauksen ohituskoodi häviää tai unohtuu, organisaation on palautettava koodi määrittämällä uusi suojauksen ohituskoodi **Puhelinkeskuksen parametri** -sivun **RMA/palautus**-välilehden **Suojauksen ohituskoodi** -kentässä.

![Maksun ohituksen parametrit RMA/Palautus-välilehdessä Puhelinkeskuksen parametrit -sivulla.](media/overridepaymentparameter.png)

> [!IMPORTANT]
> Ennen kuin organisaatiot yrittävät ohittaa luottokorttimaksulajeja käyttävät hyvitysmaksut, niiden on tarkistettava, että luottokorttien käsittelijä sallii linkittämättömät palautukset. Monet käsittelijät edellyttävät, että palautukset kirjataan takaisin alkuperäiseen korttiin. Jos yrität myöntää hyvityksen kortille, jolla ei ole aiempia tapahtumia, tämä voi aiheuttaa kirjausvirheitä käsittelijässä.

## <a name="additional-resources"></a>Lisäresurssit

[Puhelinkeskusten maksutavat](work-with-payments.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
