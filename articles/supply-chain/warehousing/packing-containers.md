---
title: Lähetettävien konttien pakkaaminen
description: Tässä artikkelissa kuvataan pakkausprosessi, jonka avulla voit vahvistaa varastonimikkeitä ja pakata ne kontteihin.
author: perlynne
ms.date: 7/13/2022
ms.topic: business-process
ms.search.form: WHSLocationType, WHSLocationProfile, WHSParameters, WHSContainerType, WHSPackProfile, WHSCloseContainerProfile, InventLocationIdLookup, UnitOfMeasureLookup, WHSPack, WHSContainerTable,
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 118b1c79d23cd1b5044ede9aa9c469409cd22166
ms.sourcegitcommit: 9e6a9d644a34158390c6e209e80053ccbdb7d974
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/20/2022
ms.locfileid: "9708780"
---
# <a name="pack-containers-for-shipment"></a>Lähetettävien konttien pakkaaminen

[!include [banner](../../includes/banner.md)]

Konttien pakkausprosessi sallii sinun vahvistaa varastonimikkeitä ja pakata ne kontteihin. Tavallisesti varastotyöntekijät keräävät varastonimikkeet tukkuvarastoista ja siirtävät ne pakkausalueelle tämän prosessin aikana. Siellä useat varastotyöntekijät tarkastavat nimikkeiden määrät ja tyypit ja kohdistavat ne asianmukaisiin konttikokoihin. Kun kontti on pakattu täyteen, se suljetaan, siirretään lähtölaiturille ja valmistellaan kuljetusta varten.

Kontit edustavat fyysisiä rakenteita, joihin nimikkeet pakataan. Voit seurata konttitietoja järjestelmässä. Nämä tiedot voivat olla hyödyllisiä kuljetusten suunnittelussa, varsinkin jos lasket kuljetusmaksut konttien perusteella. Ennen lähetystä voit tarkastaa toimituksessa käytettyjen konttien määrän, käytetyt konttityypit ja kunkin kontin fyysiset mitat (kuten kontin kokonaistilavuus ja -paino).

Konttien kanssa voidaan käyttää useita lähtövaraston ominaisuuksia. Lisätietoja on seuraavissa artikkeleissa:

- [Aaltokontitus](wave-containerization.md)
- [Lähtevä lajittelu](outbound-sorting.md)
- [Pienten pakettien lähettäminen](small-parcel-shipping.md)
- [Vahvistus ja siirtäminen](confirm-and-transfer.md)
- [Eri dimensioiden määrittäminen pakkausta ja varastointia varten](packing-vs-storage-dimensions.md)
- [Lähtevien konttien pakkaaminen ja toimitusten käsittely](packing-work.md)
- [Konttien pakkaaminen Warehouse Management ‑mobiilisovelluksen avulla](warehouse-app-packing-containers.md)
- [Esimerkkiskenaario – Konttien pakkaaminen Warehouse Management ‑mobiilisovelluksen avulla](warehouse-app-pack-containers-scenario.md)
- [Tulosta kontin etiketit](print-container-labels.md)

## <a name="set-up-your-warehouse-to-use-manual-packing-operations"></a>Varastosi määrittäminen manuaalisille pakkaustoiminnoille

Lähetystoimintosi voidaan järjestää kahdella perustavalla:

- **Aaltojen luominen ja käsittely** – Työntekijät poimivat nimikkeet lähtövaraston töiden perusteella. Tämän jälkeen he asettavat nimikkeet suoraan lähtösijaintiin, josta ne ovat heti valmiita lähetettäviksi. Lisätietoja tämän prosessin määrittämisestä ja käytöstä on kohdassa [Aaltojen luominen ja käsittely](wave-processing.md).
- **Manuaalinen pakkaaminen pakkausasemilla** – Tällä prosessilla on ylimääräinen työvaihe keräys- ja lähetysvaiheiden välillä. Sen sijaan, että työntekijät asettaisivat varaston *lastausoven toimitussijaintiin*, he asettavat sen *pakkaussijaintiin*. Tämän jälkeen he voivat hallita pakkausprosessia pakkausasemalla käyttämällä WWW-asiakasohjelman **Pakkaus**-sivua. Sinun täytyy määrittää järjestelmäsi tässä osiossa kuvatulla tavalla ottaaksesi tämän prosessin käyttöön.

### <a name="set-up-warehouse-locations-for-packing"></a>Varastosijaintien määrittäminen pakkaamista varten

Sinulla täytyy olla vähintään yksi pakkaussijainti, johon työntekijät asettavat varastonimikkeitä kontteihin pakattaviksi. Lisätietoja varastosijaintien luomisesta on kohdassa [Sijaintien määrittäminen varastonhallintajärjestelmää käyttävässä varastossa](tasks\configure-locations-wms-enabled-warehouse.md). Seuraavat alaosiot kuvaavat, miten pakkaussijainnit luodaan ja määritetään.

#### <a name="set-up-location-types-for-packing"></a>Sijaintityyppien määrittäminen pakkaamista varten

Sinun täytyy määrittää pakkaussijainneille *sijaintityyppi*. Sijainnin tyyppejä voidaan käyttää suodatusasetuksina, joilla voi ohjata erilaisia varastonhallintaprosesseja. Kunkin sijaintityypin nimi kuvaa tavallisesti, miten sijaintityyppiä tulisi käyttää. Tässä määrittämäsi sijaintityyppi täytyy liittää kuhunkin pakkaustoimissa käytettävään sijaintiin.

Määritä sijaintityyppi noudattamalla seuraavia ohjeita.

1. Valitse **Varastonhallinta \> Asetukset \> Varasto \> Sijaintityypit**.
1. Lisää sijaintityyppi ruudukkoon valitsemalla toimintoruudusta **Uusi**.
1. Määritä uudelle sijaintityypille seuraavat kentät:

    - **Sijainnin tyyppi** – Syötä sijaintityypin nimi. Kaikkien nimien täytyy olla yksilöllisiä ja niiden täytyy kuvata, miten sijaintityyppiä tulisi käyttää.
    - **Kuvaus** – Syötä sijaintityypille lyhyt kuvaus.

#### <a name="inform-the-system-about-the-packing-location-type"></a>Pakkaussijainnin tyypin ilmoittaminen järjestelmälle

Kun olet luonut sijaintityypin, sinun täytyy määrittää järjestelmäsi tunnistamaan se pakkaustoiminnoissa käytettäväksi sijaintityypiksi.

Määritä pakkaustoimissa käytetty sijaintityyppi noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Varastonhallinnan parametrit**
2. Valitse **Yleiset**-välilehden **Sijaintityypit**-pikavälilehden **Pakkaussijainnin tyyppi** -kentästä sijaintityyppi, jota käytät pakkausasemien tunnistamiseen.

> [!NOTE]
> Jos olet päivittämässä Microsoft Dynamics AX -versiosta, *Pakataan*-tila on poistettu toimituksista ja kuormista, koska se ei toiminut yhdenmukaisesti ja aiheutti tarpeettomia tietoja. Tästä syystä **Toimituksissa**- ja **Kuormat pakkauksessa** -luettelosivut on poistettu tarpeettomina. Pakattavia kontteja seurataan sijainnin tasolla.
>
> Aiemmissa versioissa määritit pakkaussijainnin käyttämällä **Varastonhallinnan parametrit** -sivun **Pakkaus**-välilehden **Pakkauksen sijainnin profiilitunnus** -kenttää *sijaintiprofiilin* määrittämiseen. Nykyisessä versiossa käytät **Varastonhallinnan parametrit** -sivun **Yleiset**-välilehden **Pakkaussijainnin tyyppi** -kenttää määrittääksesi *sijaintityypin* tässä artikkelissa kuvatulla tavalla. Tämä uusi kenttä soveltuu paremmin prosessille, jolla valmistelusijainnit ja lopulliset lähetyssijainnit tunnistetaan.
>
> Voit edelleen käyttää vanhaa **Pakkauksen sijainnin profiilitunnus** -kenttää, mutta suosittelemme käyttämään uutta **Pakkaussijainnin tyyppi** -kenttää sen sijaan, koska vanha kenttä poistetaan aikanaan.
>
> Jos tyhjennät vanhan **Pakkauksen sijainnin profiilitunnus**-kentän asetuksen ja tallennat sitten sivun, kenttä poistetaan pysyvästi käytöstä. Jos **Pakkauksen sijainnin profiilitunnus** -kenttää ei ole käytetty asennuksessa koskaan, se on aina pois käytöstä. Kun olet tyhjentänyt **Pakkauksen sijainnin profiilitunnus** -kentän asetuksen, käytä tässä artikkelissa kuvattuja asetuksia määrittääksesi ja tunnistaaksesi pakkaussijaintisi.

#### <a name="set-up-location-profiles-for-packing-locations"></a>Sijaintiprofiilien määrittäminen pakkaussijainneille

*Sijaintiprofiilit* määrittävät kutakin sijaintia koskevat tiedot ja säännöt. Tarvitset vähintään yhden sijainnin pakkaustoimintoja varten, joten sinun täytyy luoda sille sijaintityypin lisäksi sijaintiprofiili. Jokaista profiilia voidaan käyttää rajattomalle määrälle sijainteja. Pakkausta varten käytettävät sijainnit täytyy määrittää seuramaan rekisterikilpiä.

Määritä pakkaussijainnille sijaintiprofiili noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Varasto \> Sijaintiprofiilit**.
1. Valitse aiemmin luotu profiili luetteloruudusta tai luo uusi valitsemalla toimintoruudusta **Uusi**.
1. Määritä uuden tai valitun profiilin otsikossa seuraavat kentät:

    - **Sijainnin profiilitunnus** – Syötä profiilille yksilöllinen tunnus.
    - **Nimi** – Syötä profiilille kuvaava nimi.

1. Valitse **Yleiset**-pikavälilehdellä seuraavat lisäkentät:

    - **Sijainnin muoto** – Valitse nykyiselle sijainnille käytettävä sijainnin muoto. Sijaintien muodot ovat nimeämisjärjestelmä, jota käytetään yksilöllisten ja yhtenäisten nimien luomiseen varastossa käytettäville eri sijaintien lokeropaikoille. Jos sinulla ei vielä ole tarvitsemaasi muotoa, voit luoda sellaisen kohdasta **Varastonhallinta \> Asetukset \> Varasto \> Sijainnin muodot**. Lisätietoja on kohdassa [Sijaintien määrittäminen VHJ-yhteensopivassa varastossa](tasks/configure-locations-wms-enabled-warehouse.md).
    - **Sijainnin tyyppi** – Valitse sijaintityyppi, joka on määritetty pakkaussijainnin tyypiksi **Varastonhallinnan parametrit** -sivulla tässä artikkelissa aiemmin kuvatulla tavalla.
    - **Käytä rekisterikilven seurantaa** – Määritä pakkaussijainneille tämän asetuksen arvoksi *Kyllä*. Järjestelmän täytyy voida seurata rekisterikilpien tunnuksia pakkaussijainneissa, jotta se voi hallita pakkausprosessia.
    - **Salli negatiivinen varasto** – Määritä pakkaussijainneille tämän asetuksen arvoksi *Ei*.
    - **Salli yhdistetyt nimikkeet** – Määritä pakkaussijainneille tämän asetuksen arvoksi *Kyllä*. Tämä asetus on pakollinen, koska pakkaussijainteihin tuodaan tavallisesti monia erilaisia nimiketunnuksia samanaikaisesti.
    - **Salli yhdistetyt varastotilat** – Määritä pakkaussijainneille tämän asetuksen arvoksi *Kyllä*. Tämä asetus on pakollinen, koska pakkaussijainteihin tuodaan tavallisesti samanaikaisesti nimikkeitä, joilla on erilaiset varastotilat.
    - **Salli yhdistetyt varastoerät** – Määritä pakkaussijainneille tämän asetuksen arvoksi *Kyllä*. Tämän asetuksen arvoksi määritetään automaattisesti *Kyllä*, kun **Salli yhdistetyt nimikkeet** -asetuksen arvoksi määritetään *Kyllä*.

#### <a name="set-up-packing-locations"></a>Pakkaussijaintien määrittäminen

Sinulla täytyy olla vähintään yksi *sijainti*, johon työntekijät asettavat varastonimikkeitä kontteihin pakattaviksi.

Lisää pakkaussijainti noudattamalla seuraavia ohjeita.

1. Valitse **Varastonhallinta \> Asetukset \> Varasto \> Sijainnit**.
1. Lisää sijainti valitsemalla toimintoruudusta **Uusi**.
1. Määritä uudelle sijainnille seuraavat kentät:

    - **Varasto** – Määritä varasto, jossa pakkaussijainnin täytyy olla.
    - **Sijainti** – Syötä uudelle sijainnille nimi.
    - **Sijainnin profiilitunnus** – Muista määrittää edellisessä osiossa luomasi tunnus.

## <a name="set-up-the-packing-process"></a>Pakkausprosessin määrittäminen

Tässä osiossa kuvataan, kuinka määrittää asetukset, jotka mahdollistavat pakkausprosessin ja sallivat työntekijöiden pakata varastoa kontteihin.

### <a name="set-up-container-packing-policies"></a><a name="packing-policy"></a>Kontin pakkauskäytäntöjen määrittäminen

Jokainen *kontin pakkauskäytäntö* määrittää, miten kontti tulisi käsitellä. Joka kerta, kun luot uuden kontin, valitset sille myös pakkauskäytännön.

Kontin pakkauskäytäntö määritetään seuraavasti:

1. Valitse **Varastonhallinta \> Asetukset \> Kontit \> Kontin pakkauskäytännöt**.
1. Valitse aiemmin luotu käytäntö luetteloruudusta tai luo uusi valitsemalla toimintoruudusta **Uusi**.
1. Määritä uuden tai valitun käytännön otsikossa seuraavat kentät:

    - **Kontin pakkauskäytäntö** – Syötä käytännölle yksilöllinen nimi.
    - **Kuvaus** – Syötä käytännölle kuvaava nimi.

1. Määritä **Yleiskuvaus**-välilehdessä seuraavat kentät. Näiden kenttien avulla voit määrittää, mitä toimenpiteitä tulisi tehdä kontin ollessa suljettuna, käytetäänkö työn luontia vai ei, sekä milloin kontti tulisi vapauttaa pakkausasemasta.

    - **Varasto** – Valitse varasto, jossa pakkauskäytäntö on voimassa.
    - **Lopullisen lähetyksen oletussijainti** – Määritä kontille toivottu sijainti sen jälkeen, kun kontti on suljettu. Tämä kenttä on käytettävissä vain, kun **Kontin vapautuskäytäntö** -kentän arvoksi on määritetty *Tee saatavaksi lopullisessa lähetyssijainnissa*.
    - **Lajittelun oletussijainti** – Tätä kenttää käytetään [lähtevän lajittelun](outbound-sorting.md) ominaisuuden kanssa.
    - **Painoyksikkö** – Valitse oletusarvoinen mittayksikkö, jota käytetään, kun kontti suljetaan ja luetteloidaan. Tavallisesti tämä mittayksikkö on pakkausaseman vaa'an käyttämä mittayksikkö. Tämä kenttä koskee käytäntöjä työn luonnilla tai ilman.
    - **Kontin sulkemiskäytäntö** – Valitse jokin seuraavista vaihtoehdoista määrittääksesi, mitä kontin sulkemisen yhteydessä tulisi tapahtua:

        - *Automaattinen vapautus* – Kontti katsotaan vapautetuksi pakkausasemalta ja **Kontin vapautuskäytäntö** -kentässä määritetty toiminto käynnistyy.
        - *Viivästynyt vapautus* – Konttia ei vapauteta heti pakkausasemalta. Varastotyöntekijän on vapautettava se myöhemmin manuaalisesti.
        - *Valinnainen* – Kun työntekijä on sulkemassa konttia, hän voi valita, tulisiko kontti vapauttaa.

        Jos pakkausasema käsittelee pääasiallisesti yksittäisiä kontteja, jotka lähetetään suoraan asiakkaille, kaikkein luontaisin tapa on vapauttaa kontit välittömästi. Jos pakkausasema käsittelee lähetyksiä, jotka koostuvat useista konteista tai jopa kuormalavoista, on todennäköisesti parasta viivyttää vapautusta, kunnes koko lähetys tai kuormalava on pakattu ja valmiina noutoa varten.

    - **Kontin vapautuskäytäntö** – Valitse jokin seuraavista vaihtoehdoista määrittääksesi, mitä tulisi tapahtua, kun kontti vapautetaan pakkausasemalta:

        - *Tee saatavaksi lopullisessa lähetyssijainnissa* – Päivitä kontti lopulliseen lähetyssijaintiin. Jos valitset tämän vaihtoehdon, käytä **Lopullisen lähetyksen oletussijainti** -kenttää määrittääksesi kontille toivotun sijainnin, kun kontti on suljettu.
        - *Luo työ kontin siirtämiseksi pakkausasemalta* – Luo työ, jolla kontti siirretään pakkausasemalta valmistelualueelle tai suoraan lastausovelle. Käytä **Työmalli**-kenttää määrittääksesi työmallin, jota tulisi käyttää, kun kontille luodaan työ.
        - *Määritä kontti lähtevälle lajittelumääritykselle* – Tätä valintaa käytetään [lähtevän lajittelun](outbound-sorting.md) ominaisuudessa.

        Useimmissa tapauksissa suosittelemme, että luot työn konttien siirtoa varten, sillä tämä lähestymistapa edustaa varaston todellisia manuaalisia prosesseja paremmin. Yksinkertaisissa skenaarioissa tai tilanteissa, joissa pakkausasema sijaitsee suoraan lastausoven alueella, voi kuitenkin olla parempi, että kontti on heti käytettävissä lopullisessa lähetyssijainnissa.

    - **Työmalli** – Valitse työmalli, jota tulisi käyttää, kun kontille luodaan työ. Tämä kenttä on käytettävissä vain, kun **Kontin vapautuskäytäntö** -kentän arvoksi on määritetty *Luo työ kontin siirtämiseksi pakkausasemalta* ja se on liitetty työtilaustyyppiin, jonka nimi on *Pakatun kontin keräily*. Lisätietoja on kohdassa [Työmallit ja sijaintidirektiivit](control-warehouse-location-directives.md).

    Lopuissa vaiheissa määrität *luettelointiin* liittyvät asetukset. Luettelointi on prosessi, jossa kontin, konttiryhmän tai lähetyksen paino määritetään yhdessä kuljetuspalvelun tarjoajalta saadun seurantatunnuksen kanssa. Dynamics 365 Supply Chain Managementia ei voi integroida ulkoisiin kuljetuspalveluiden tarjoajien järjestelmiin. Sen sijaan varastotyöntekijöiden täytyy tulostaa kuljetuspalvelun tarjoajalta saadut etiketit ja skannata sitten seurantanumero luetteloinnin aikana.

    Luetteloinnin vaatimukset vaihtelevat asiakkaasta ja jopa lähetyksestä toiseen, joten pakkauskäytännöt tekevät työnkulusta merkittävästi joustavampaa. Voit määrittää luettelointeja konteille, konttiryhmille ja lähetyksille missä tahansa yhdistelmässä.

    Jos käytät monitasoista luettelointiprosessia, työntekijöiden täytyy luetteloida kaikki kontit ennen niihin liittyvän konttiryhmän luettelointia ja kaikki konttiryhmät ennen niihin liittyvän lähetyksen luettelointia.

1. Määritä seuraavat kentät **Kontin lastiluettelo** -pikavälilehdessä:

    - **Automaattinen lastiluettelo konttia suljettaessa** – Määritä tämän asetuksen arvoksi *Kyllä*, jos haluat käyttää luettelointitietoja osana kontin sulkemisprosessia. Jos et käytä kuljetuksen integraatiota, tiedot täytyy kirjata manuaalisesti.
    - **Kontin lastiluettelon vaatimukset** – Valitse jokin seuraavista vaihtoehdoista:

        - *Ei mitään* – Mitään luettelointiprosessia ei käytetä.
        - *Manuaalinen* – Pakkaustyönkulku edellyttää luettelointia. Järjestelmä ei salli kontin sulkemista tai vapauttamista ennen kuin luettelointi on suoritettu.
        - *Kuljetustenhallinta* – Luettelointi tehdään kuljetustenhallinnan (TMS) hinnan laskentojen avulla. Tämä vaihtoehto edellyttää mukautettua kehitystyötä moduulin toteuttamiseksi kuljetuspalvelun tarjoajalle, joten se ei toimi käyttövalmiina nykyisessä versiossa.

    - **Tulosta kontin sisältö** – Määritä asetuksen arvoksi *Kyllä*, jos haluat tulostaa kontin sisältöraportin automaattisesti, kun kontti rekisteröidään suljetuksi. Raportti voidaan myös tulostaa tarvittaessa.

1. Valitse **Konttiryhmän lastiluettelo** -pikavälilehden **Konttiryhmän lastiluettelon vaatimukset** -kentästä jokin seuraavista vaihtoehdoista:

    - *Ei mitään* – Konttiryhmän luettelointia ei sisällytetä vaatimukseksi pakkaustyönkulkuun.
    - *Manuaalinen* – Konttiryhmän luettelointi sisällytetään vaatimukseksi pakkaustyönkulkuun. Kaikki ryhmään sisältyvät kontit on luetteloitava ja suljettava ennen kuin ryhmä voidaan luetteloida. Valitse tämä vaihtoehto, jos sinun täytyy suorittaa luettelointi jokaiselle pakkausasemalla pakatulle pakkausryhmälle. Valitset tämän vaihtoehdon tavallisesti, jos kontit pakataan kuormalavaan ja koko kuormalava luetteloidaan.

    > [!NOTE]
    > Nykyinen versio ei tue konttiryhmien luettelointiraportteja, eikä TMS-moduulia tueta konttiryhmille.

1. Määritä seuraavat kentät **Lähetysluettelo**-pikavälilehdessä:

    - **Lähetyksen lastiluettelon vaatimukset** – Valitse jokin seuraavista vaihtoehdoista:

        - *Ei mitään* – Lähetyksen luettelointia ei sisällytetä vaatimukseksi pakkaustyönkulkuun.
        - *Manuaalinen* – Lähetyksen luettelointi sisällytetään vaatimukseksi pakkaustyönkulkuun. Lähetyksen kontteja ei voi vapauttaa ennen kuin luettelointi on suoritettu.
        - *Kuljetustenhallinta* – Luettelointi tehdään kuljetustenhallinnan TMS-hintalaskentojen avulla. Tämä vaihtoehto edellyttää mukautettua kehitystyötä moduulin toteuttamiseksi kuljetuspalvelun tarjoajalle, joten se ei toimi käyttövalmiina nykyisessä versiossa.

        Lähetyksen luetteloinnin tulisi olla käytössä, jos sinun täytyy suorittaa luettelointi koko pakkausasemalla pakatulle lähetykselle. Sitä käytetään tavallisesti silloin, kun tarvitaan yksi yhdistetty luettelointi, vaikka lähetys koostuisi useista konteista tai konttiryhmistä.

    - **Tulosta pakkausluettelo** – Määritä tämän asetuksen arvoksi *Kyllä*, jos haluat tulostaa pakkausluettelon automaattisesti osana lähetyksen luettelointia. Pakkausluettelo voidaan myös tulostaa tarvittaessa.

### <a name="set-up-container-types"></a>Määritä konttityypit

Manuaalisen pakkausprosessin aikana kontit täytyy luoda ennen kuin niihin voi pakata nimikkeitä. Jokaisen kontin täytyy perustua *konttityyppiin*, joka määrittää kontin fyysisen enimmäistilavuuden ja painokapasiteetin.

Luo konttityyppi noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Kontit \> Konttityypit**.
1. Lisää konttityyppi valitsemalla toimintoruudusta **Uusi**.
1. Määritä konttityypille seuraavat kentät:

    - **Kontin tyyppikoodi** – Syötä konttityypille yksilöllinen tunnus.
    - **Kuvaus** – Syötä uudelle konttityypille kuvaus.
    - **Taaran paino** – Syötä kontin todellinen tai arvioitu paino.
    - **Enimmäisnettopaino** – Syötä konttiin sijoitettava enimmäispaino.

1. Syötä itse kontin fyysiset mitat **Kontin dimensiot** -osion **Pituus**-, **Leveys**-, **Korkeus**- ja **Tilavuus**-kenttiin.
1. Syötä kontin sallimat fyysiset enimmäismitat **Maksimit**-osion **Pituus**-, **Leveys**-, **Korkeus**- ja **Tilavuus**-kenttiin.
1. Voit määrittää lisämääritteitä konttityypeille, jotka liittyvät muihin kontteja käyttäviin työvaiheisiin. Lisätietoja on kohdassa [Konttiinpakkaus](wave-containerization.md).

> [!NOTE]
> Järjestelmä käyttää manuaalisessa pakkausprosessissa vain **Enimmäisnettopaino**-kentän arvoa ja **Maksimit**-osion **Tilavuus**-kentän arvoa.

### <a name="set-up-packing-profiles"></a>Määritä pakkausprofiilit

*Pakkausprofiilit* ovat pakollisia pakkausprosessille. Ne voidaan valita tai määrittää oletusarvoisesti, kun aloitat pakkaustoiminnon **Pakkaus**-sivulta.

Määritä pakkausprofiili seuraavasti:

1. Valitse **Varastonhallinta \> Asetukset \> Pakkaus \> Pakkausprofiilit**.
1. Valitse aiemmin luotu profiili luetteloruudusta tai luo uusi valitsemalla toimintoruudusta **Uusi**.
1. Määritä uuden tai valitun profiilin otsikossa seuraavat kentät:

    - **Pakkausprofiilin tunnus** – Syötä profiilille lyhyt tunnus.
    - **Kuvaus** – Syötä pakkausprofiilille kuvaus.
    - **Kontin pakkauskäytäntö** – Valitse profiilia koskeva pakkauskäytäntö. Lisätietoja on tämän artikkelin [Kontin pakkauskäytäntöjen määrittäminen](#packing-policy) -osiossa.
    - **Kontin tunnuksen tila** – Valitse, tulisiko kontin tunnus luoda automaattisesti kontin luomisen yhteydessä vai täytyykö se luoda manuaalisesti.
    - **Konttityyppi** – Valitse konttityyppi, jota käytetään oletusarvoisesti, kun uusi kontti luodaan.
    - **Luo kontti automaattisesti kontin sulkemisessa** – Valitse tämä valintaruutu, jos haluat luoda uuden kontin automaattisesti, jos edellinen kontti on suljettu ja vähintään yksi rivi säilyy nykyisessä lähetyksessä.

### <a name="set-up-warehouse-workers"></a>Varastotyöntekijöiden määrittäminen

Kaikilla käyttäjillä, jotka pakkaavat kontteja käyttämällä WWW-asiakasohjelman **Pakkaus**-sivua tai Warehouse Management -mobiilisovelluksen *Pakkaus*- tehtäväkoodia, täytyy olla käyttäjätili, joka on liitetty *työntekijän/henkilön* tietueeseen, jolle vaaditut käyttöoikeudet kohdistetaan. (Lisätietoja käyttäjien määrittämisestä on kohdassa [Uusien käyttäjien luominen](../../fin-ops-core/dev-itpro/sysadmin/tasks/create-new-users.md)).

Määritä *työntekijän/henkilön* tietue pakkausprosessia varten noudattamalla seuraavia ohjeita.

1. Valitse **Varastonhallinta \> Asetukset \> Työntekijä**.
1. Lisää työn käyttäjä valitsemalla toimintoruudussa **Uusi**.
1. Määritä **Työntekijä**-kentän arvoksi työntekijätietue, joka on määritetty pakkausprosessin suorittavan käyttäjän **Henkilöstöhallinto**-moduulissa.
1. Valitse **Profiili**-pikavälilehdellä seuraavat lisäkentät:

    - **Kontin pakkauskäytäntö** – Valitse kontin pakkauskäytäntö, jolla määritellään, miten kontit käsitellään pakkausasemalla. Tässä valitsemasi kontin pakkauskäytäntö valitaan työntekijälle ennalta, kun hän avaa pakkausaseman. Lisätietoja on seuraavassa blogikirjoituksessa: [Parannettu pakkaustoiminto](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/12/01/improved-packing-functionality-dynamics-365-for-operations-1611).
    - **Pakkausprofiilin tunnus** – Valitse pakkausprofiilin tunnus, jolla määritetään pakkauskäytäntö ja käytettävät konttiasetukset. Jos valittu pakkausprofiilin tunnus on liitetty kontin pakkauskäytäntöön, et voi muuttaa **Kontin pakkauskäytäntö** -kentän asetusta tältä sivulta.

1. Valitse **Oletuspakkausasema**-pikavälilehdestä työntekijän oletustoimipaikka, varasto ja sijainti.
1. Jos työntekijä käyttää konttien pakkaustöidensä hallintaan ja rekisteröimiseen Warehouse Management -mobiilisovellusta, määritä **Käyttäjät**-pikavälilehdestä yksi tai useampi tili, joilla työntekijä voi kirjautua sovellukseen. Lisätietoja on kohdassa [Mobiililaitteen käyttäjätilit](mobile-device-work-users.md).

## <a name="example-scenario"></a><a name="scenario"></a>Esimerkkiskenaario

Tämän osion esimerkkiskenaariossa kuvataan, miten tilaus luodaan ja nimikkeet pakataan.

### <a name="make-sample-data-available"></a>Ota mallitiedot käyttöön

Tämän skenaarion käyttäminen tässä määritettyjen mallitietojen ja -arvojen avulla edellyttää, että käytössä on järjestelmä, johon vakio-[demotiedot](../../fin-ops-core/fin-ops/get-started/demo-data.md) on asennettu. Sinun on myös valittava **USMF**-yritys ennen kuin aloitat.

Voit käyttää tätä skenaariota ohjeena ominaisuuden käyttämiseen tuotantojärjestelmässä. Siinä tapauksessa tässä kuvatut arvot on kuitenkin korvattava omilla arvoilla.

### <a name="sign-in-as-a-user-that-can-do-packing-work"></a>Kirjaudu sisään käyttäjänä, joka voi tehdä pakkaustöitä

Kirjaudu sisään Supply Chain Managementiin käyttäjätilillä, jolla on konttien pakkaamiseen tarvittavat käyttöoikeudet. Demotiedot sisältävät käyttäjän *Julia Funderburk*, jolla on tarvittavat käyttöoikeudet. Tämän käyttäjän käyttäjätunnus on *Admin*.

### <a name="create-a-sales-order-and-complete-the-work"></a>Myyntitilauksen luominen ja työn merkitseminen valmiiksi

Luo myyntitilaus ja merkitse tilattujen nimikkeiden siirtäminen pakkausasemalle suoritetuksi noudattamalla seuraavia ohjeita.

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Valitse toimintoruudussa **Uusi**.
1. Valitse **Luo myyntitilaus** -valintaikkunan **Asiakastili**-kentässä *US-005*.
1. Sulje valintaikkuna valitsemalla **OK**.
1. Uusi myyntitilaus avataan, ja se sisältää yhden tyhjän rivin **Myyntitilausrivit**-pikavälilehdessä. Määritä uudelle tilausriville seuraavat arvot:

    - **Nimiketunnus:** *A0001*
    - **Määrä** *2*
    - **Toimipaikka:** *6*
    - **Varasto**: *62*

1. Kun uusi tilausrivi on edelleen valittuna, valitse **Myyntitilausrivit**-pikavälilehden työkaluriviltä **Varasto \> Varaus**.
1. Valitse **Varaus**-sivun toimintoruudusta **Varaa erä**, jos haluat varata koko valitun rivin määrän varastosta.
1. Palaa myyntitilaukseen sulkemalla **Varaus**-sivun.
1. Valitse toimintoruudussa **Varasto**-välilehdellä **Vapauta varastoon**.

    Tilauksen lähetyksen ja aallon tunnukset näytetään viestissä.

1. Kun uusi tilausrivi on edelleen valittuna, valitse **Myyntitilausrivit**-pikavälilehden työkaluriviltä **Varasto** \> **Työn tiedot**. Jos käytät aaltojen suorittamiseen eräkäsittelyä, työn luominen voi kestää hetken.
1. Valitse toimintoruudun **Työ**-sivun **Työ**-välilehdestä **Valmistunut työ**.
1. Määritä **Työn valmistuminen** -sivun **Käyttäjätunnus**-kentän arvoksi *62*.
1. Valitse toimintoruudusta **Tarkista työ**.
1. Kun näet viestin, joka ilmaisee, että työsi läpäisi tarkistuksen, valitse **Valmistunut työ** merkitäksesi varastonimikkeiden keräysprosessin ja niiden asettamisen *Pakkaus*-sijaintiin valmiiksi.
1. Kirjoita työn ylemmässä ruudukossa näytetty **Lähetyksen tunnus** -arvo muistiin.

### <a name="pack-the-ordered-items-into-a-container"></a>Tilattujen nimikkeiden pakkaaminen konttiin

Varastonimikkeet on nyt tuotu pakkausalueelle, ja ne ovat valmiita pakattavaksi kontteihin. Luo järjestelmään uusi kontti ja pakkaa se noudattamalla seuraavia ohjeita.

1. Valitse **Varastoinhallinta \> Pakkaus ja konttiinpakkaus \> Pakkaus**.
1. Määritä seuraavat arvot **Valitse pakkausasema** -valintaikkunassa:

    - **Toimipaikka:** *6*
    - **Varasto**: *62*
    - **Sijainti:** *Pakkaus*
    - **Pakkausprofiilin tunnus:** *WH62*

1. Valitse **OK**.
1. Syötä **Pakkaus**-sivun **Rekisterikilpi tai lähetys** -kenttään lähetyksen tunnus, jonka kirjoitit aiemmin muistiin. Sinun tulisi nyt nähdä **Avoimet rivit** -pikavälilehdessä nimikkeet, joita ei ole vielä pakattu.
1. Luo järjestelmään uusi kontti valitsemalla toimintoruudusta **Uusi kontti**.
1. Määritä **Uuden kontin tunnus** -valintaikkunassa **Konttityyppi** -kentän arvoksi *Pieni laatikko*.
1. Luo kontti valitsemalla **OK**.
1. Valitse **OK** palataksesi **Pakkaus**-sivulle. Luomasi kontin **Kontin tunnus** -arvo näytetään nyt **Avoimet kontit** -pikavälilehdessä.
1. Tässä skenaariossa pakkaat vain yhden tilatuista nimikkeistä tältä erää. Määritä siis **Nimikepakkaus**-pikavälilehdessä seuraavat arvot:

    - **Määrä** *1.00*
    - **Tunniste:** *A0001*

    Kun valitset **Tunniste**-arvon, sivu päivittää **Avoimet rivit**- ja **Kaikki rivit**-pikavälilehdet välittömästi osoittamaan, että yksi nimike on pakattu. Nyt nimikkeen *A0001* toisen osan tulisi olla pakattuna.

1. Valitse toimintoruudussa **Sulje kontti**.
1. Valitse **Sulje kontti** -valintaikkunassa **Hae järjestelmän paino** korvataksesi **Bruttopaino**-kentän oletusarvon.
1. Sulje kontti valitsemalla **OK**.

> [!TIP]
> Kontteja voi tarkastella monin eri tavoin kontekstin perusteella. Kun esimerkiksi pakkaat lähetyksen, on usein hyödyllistä tarkastaa lähetykseen sisältyvät tai kaikki pakkausasemalla fyysisesti sijaitsevat kontit. **Pakkausasema**-sivulla on painikkeet, joita voit käyttää pakkausaseman kaikkien avointen ja suljettujen konttien tarkastelemiseen. Näitä näkymiä ei ole rajoitettu tiettyyn lähetykseen. Ne voivat olla erittäin hyödyllisiä tilanteissa, joissa yksi työntekijä pakkaa kontin ja toinen työntekijä luetteloi ja vapauttaa sen.
>
> Myös kaikkien konttien yhdistetty näkymä on saatavilla. Tämä näkymä on hyödyllinen tavallisesti käyttäjille, joiden työ kattaa useita pakkausasemia. Näet sen avaamalla **Varastonhallinta \> Pakkaaminen ja konttiinpakkaus \> Kontit**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
