---
title: Toimittajan laskuautomaatio
description: "Tässä ohjeaiheessa kerrotaan ominaisuuksista, joita voidaan käyttää toimittajalaskujen päästä päähän -automatisointiin. Tämä koskee myös laskuja, jotka sisältävät liitteitä."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendEditInvoiceHeaderStagingListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 551f3d5fc52fac725fcc9fedc37dc1c85fac5a26
ms.contentlocale: fi-fi
ms.lasthandoff: 03/26/2018

---
# <a name="vendor-invoice-automation"></a>Toimittajan laskuautomaatio

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan ominaisuuksista, joita voidaan käyttää toimittajalaskujen päästä päähän -automatisointiin. Tämä koskee myös laskuja, jotka sisältävät liitteitä.

Organisaatiot, jotka haluavat helpottaa ostoreskontran prosessejaan, määrittelevät usein laskutusprosessin yhdeksi tärkeimmäksi tehostettavaksi prosessialueeksi. Usein nämä organisaatiot siirtävät paperilaskujen käsittelyn ulkoiselle optisten merkkien tunnistuksen (OCR) palveluntarjoajalle. Ne saavat koneellisesti luettavat laskun metatiedot ja jokaisen laskun skannatun kuvan. Automaation avuksi luodaan "viimeisen osuuden" ratkaisu, joka mahdollistaa näiden artefaktien käytön laskutusjärjestelmissä. Microsoft Dynamics 365 for Finance and Operations mahdollistaa nyt tämän "viimeisen osuuden" valmiin automaatioratkaisun käyttöönoton laskuautomaatioratkaisun avulla.

## <a name="solution-context"></a>Ratkaisukonteksti

Laskuautomaatioratkaisu tuo käyttöön vakiokäyttöliittymän, joka sisällyttää laskun metatiedot laskun otsikkoon ja laskutusriveille sekä mahdolliset laskuliitteet. Mikä tahansa ulkoinen järjestelmä, joka voi luoda tämän käyttöliittymän kanssa yhteensopivia artefakteja, voi lähettää syötteen Finance and Operations -palveluun laskujen ja liitteiden automaattista käsittelyä varten.

Seuraavassa kuvassa on esimerkkitilanne integroinnista, jossa Contoso on tehnyt yhteistyötä OCR-palveluntarjoajan kanssa toimittajan laskun käsittelyä varten. Contoson palveluntarjoajat lähettävät laskuja palveluntarjoajalle sähköpostitse. Palveluntarjoajan luo OCR-käsittelyn avulla laskun metatiedot (otsikon ja/tai rivit) ja skannatun kuvan laskusta. Integrointitaso muuntaa sitten nämä artefaktit Finance and Operations -yhteensopivaan muotoon.

![Esimerkkiskenaario integroinnista](media/vendor_invoice_automation_01.png)

Edellisestä skenaariosta on useita mahdollisia versioita, jos laskun integrointi on pakollinen. Toinen käyttöliittymän käyttötapaus on tietojen siirtäminen laskujen ja liitteiden luomiseksi Finance and Operations -palvelussa.

### <a name="solution-components"></a>Ratkaisukomponentit

Seuraavat komponentit sisältyvät kattavaan ratkaisuun:

+ Laskuotsikon, laskurivien ja laskun liitteiden tietoyksiköt
+ Laskujen poikkeusten käsittely
+ Laskujen liitteiden rinnakkainen tarkastelu

Tämä aiheohje sisältää myös näiden ratkaisukomponenttien yksityiskohtaiset kuvaukset.

## <a name="data-entities"></a>Tietoyksiköt

Datapaketti on työyksikkö, joka on lähetettävä Finance and Operations -palveluun, jotta laskun otsikko, laskurivit ja laskun liitteet voidaan luoda. Seuraavia tietoyksiköitä käytetään datapaketin muodostavien artefaktien luomiseen:

+ Toimittajan laskun otsikko
+ Toimittajan laskurivi
+ Toimittajan laskun asiakirjaliite

Toimittajan laskun asiakirjaliite on uusi toiminnon osana esiteltävä tietoyksikkö. Toimittajan laskun otsikkoa on muokattu siten, että se tukee liitteitä. Toimittajan laskuriviyksikköä ei ole muutettu tämän toiminnon osalta.

Tässä ohjeaiheessa ei anneta tarkkaa datapaketin määritystä. Tässä ei myöskään selitetä, miten datapaketit luodaan. Lisätietoja on ohjeaiheessa [Tietoyksikköjen ja -pakettien kehikko](../../dev-itpro/data-entities/data-entities-data-packages.md).

Noudata näitä vaiheita, kun haluat luoda nopeasti testitietoja, jotka sisältävät laskuja ja -liitteitä.

1. Kirjaudu omaan Finance and Operations -esiintymään.
1. Valitse **Ostoreskontra** > **Laskut** > **Avoimet toimittajan laskut**.
1. Luo laskuja, joissa on rivejä ja liitteitä.

    > [!NOTE]
    > Liitteiden on oltava otsikon liitteitä. Toimittajan laskun asiakirjaliiteyksiköt eivät tue tällä hetkellä riviliitteitä.

1. Avaa **Tietojen hallinta** -työtila.
1. Luo vientityö, joka sisältää toimittajan laskun otsikko-, toimittajan laskun rivi- ja toimittajan laskun asiakirjaliite -yksiköt.
1. Vie tiedot.
1. Lataa viedyt tiedot pakettina. Voit käyttää pakettia tietojen tuontiin kohde-esiintymiin testausta varten.

### <a name="determining-the-legal-entity-for-an-invoice"></a>Yritys määrittäminen laskua varten

Tietopakettien kautta tuodut laskut voidaan liittää ne omistaviin yrityksiin kahdella tavalla:

+ Laskuja käsittelevä tuontityö tuo sen samaan yritykseen, jossa työ oli ajoitettu **Tietojen hallinta** -työtilassa. Toisin sanoen työn yritys määrittää yrityksen, jolle lasku kuuluu.
+ Jos laskuja sisältävä tietopaketti lähetetään Finance and Operations -palveluun, kutsuja (toisin sanoen integrointisovellus, joka suoritetaan Finance and Operations -palvelun ulkopuolella) voi erikseen mainita yritystunnuksen HTTP-pyynnössä. Tässä tapauksessa yrityskonteksti, jossa käsittelytyö suoritetaan Finance and Operations -palvelussa, sekä laskut tuodaan yritykseen, joka siirrettiin HTTP-pyynnön kautta.

> [!NOTE]
> Tämä on vakiotyyppinen tietojen hallintatoiminto. Tämä on selitetty laskujen yhteydessä vain kattavuuden vuoksi.

## <a name="exception-processing"></a>Poikkeuksen käsittely

Skenaarioissa, joissa toimittajalaskut tulevat Finance and Operations -palveluun integroinnin kautta, ostoreskontratiimin jäsenellä on oltava helppo tapa käsitellä poikkeuksia tai epäonnistuneita laskuja ja keino luoda odottavia laskuja epäonnistuneista laskuista. Toimittajan laskujen poikkeusten käsittely on nyt osa Finance and Operations -palvelua.

### <a name="exceptions-list-page"></a>Poikkeusluettelo-sivu

Uusi laskun poikkeusten luettelosivu on kohdassa **Ostoreskontra** > **Laskut** > **Epäonnistuneet tuonnit** > **Toimittajan laskut, joiden tuonti epäonnistui**. Tällä sivulla näkyvät kaikki toimittajalaskujen otsikkotietueet Toimittajan laskun otsikko ‑tietoyksikön väliaikaisesta taulukosta. Huomaa, että samaa tietueita voidaan tarkastella **Tietojen hallinta** -työtilasta, jossa voit myös suorittaa samat toiminnot, jotka ovat käytössä poikkeusten käsittelytoiminnossa. Poikkeuksien käsittelytoiminnon käyttöliittymä on kuitenkin optimoitu toimintokäyttäjää varten.

![Poikkeusluettelo-sivu](media/vendor_invoice_automation_02.png)

Tämä luettelosivulta sisältää seuraavat kentät, jotka saadaan syötteen kautta:

+ **Yritys** – Yritys, joka omistaa laskun
+ **Virhesanoma** – Virhesanoma, jonka tiedonhallinta-sovelluskehys muodostaa selitykseksi, miksi laskua ei voitu luoda
+ **Numero** – Laskunumero
+ **Laskutusasiakasnumero**
+ **Nimi** – Toimittajan nimi
+ **Toimittajanro**
+ **Ostotilauksen numero** – Ostotilauksen numero laskuun
+ **Kirjauspäivä**
+ **Laskun päivämäärä**
+ **Laskun kuvaus**
+ **Valuutta**
+ **Loki**
+ **Riviviite** – Tunnus, joka saadaan ulkoisesta järjestelmästä

    > [!NOTE]
    > Riviviite ei ole laskun tunnus.

Tällä luettelosivulta on myös esikatseluruutu, jota voit käyttää seuraavilla tavoilla:

+ Tarkastele koko virhesanomaa laajentamatta taulukon **Virhesanoma**-saraketta.
+ Tarkastele laskun koko liiteluetteloa, jos laskussa on liitteitä.

Luettelosivun tukee seuraavia toimia:

+ **Muokkaa** – Avaa poikkeustietue muokkaustilassa siten, että voit korjata ongelmia.
+ **Asetukset** – Luettelosivuilla käytettävissä olevien vakiovaihtoehtojen tarkastelu. Voit käyttää **Lisää työtilaan** -asetusta ja kiinnittää työtilaasi poikkeusluettelosivun luettelona tai ruutuna.

### <a name="exception-details-page"></a>Poikkeustiedot-sivu

Käynnistäessäsi muokkaustilan näyttöön tulee poikkeustiedot-sivu laskuista, joissa on ongelmia. Jos liitteitä on paljon, lasku ja oletusliite näkyvät rinnakkain Poikkeustiedot-sivulla.

![Poikkeustiedot-sivu](media/vendor_invoice_automation_03.png)

Edellisessä kuvassa ei toimittajan laskun otsikkoon tullut yhtään riviä. Tämän vuoksi riviosa on tyhjä.

Poikkeustiedot-sivu tukee seuraava toimintoa:

+ **Luo odottava lasku** – Kun laskun ongelmat on korjattu poikkeuskäsittelyn yhteydessä, voit luoda laskun valitsemalla tämän painikkeen. Odottavien laskujen luominen tapahtuu taustalla (asynkronisena työvaiheena).

### <a name="shared-service-vs-organization-based-exception-processing"></a>Jaettu palvelu vs. organisaatioperusteinen poikkeusten käsittely

Poikkeusluettelo-sivu tukee vakiotyyppisiä suojausrakenteita, joita **Tietojen hallinta** -työtila tukee väliaikaisten tiedostojen käsittelyssä. Laskun tuontityö voidaan suojata seuraavilla tavoilla:

+ Käyttäjäroolikohtainen
+ Käyttäjäkohtainen
+ Yrityskohtainen

![Tuontityö, joka on suojattu käyttäjärooli- ja yrityskohtaisesti](media/vendor_invoice_automation_04.png)

Jos suojaus on konfiguroitu laskun tuontityötä varten, poikkeusluettelosivu noudattaa kyseisiä asetuksia. Käyttäjät näkevät ainoastaan ne laskun poikkeustietueet, jotka tämä asetus sallii.

Esimerkiksi Contoso on päättänyt käsitellä laskun poikkeuksia yrityskohtaisesti. Siksi suojaus on määritetty laskun tuontityölle siten, että yrityksen A käyttäjä näkee ainoastaan laskun poikkeukset yrityksessä A ja yrityksen B käyttäjä näkee ainoastaan laskun poikkeukset yrityksessä B. Tämä asetus mahdollistaa tehtävien eriyttämisen laskun poikkeusten hallinnassa.

Contoso voi myös päättää ettei se pakota mitään suojausta, jotta samat käyttäjät voivat prosessoida laskun poikkeuksia kaikissa yrityksissä. Tämä asetus mahdollistaa jaetut palvelut -skenaarion laskun poikkeusten hallintaa varten.

## <a name="side-by-side-attachment-viewer"></a>Liitteiden rinnakkainen tarkastelu

Seuraavilla sivuilla, joita käytetään laskutusprosessiin, on nyt liitteiden tarkastelutoiminto toimittajan laskujen helppoa tarkastelua varten:

+ **Poikkeusten käsittely**
+ **Odottavat toimittajan laskut** -sivu (käytettävissä myös laskun tarkistusprosessissa)
+ **Laskukirjauskansio** -kyselysivu (kirjatuille laskuille)

Liitteen tarkastelutoiminnon päätoiminto:

+ Kaikkien liitetiedostotyyppien tarkastelu joita tiedostojen hallinta tukee (tiedostot, kuvat, URL-osoitteet ja huomautukset).
+ Monisivuisten TIFF-tiedojen tarkastelu.
+ Suorita seuraavat toiminnot kuvatiedostoille:
  + Korosta kuvan osia.
  + Estä kuvan osia.
  + Lisää huomautuksia kuvaan.
  + Suurenna ja pienennä kuvaa.
  + Panoroi kuvaa.
  + Peruuta toiminto ja tee se uudelleen.
  + Sovita kuvan koko.

> [!NOTE]
> Nämä toiminnot ovat käytettävissä vain kuvatiedostoille (JPEG TIFF, PNG jne.). Näillä toiminnoilla kuvaan tekemäsi muutokset tallennetaan kuvatiedostoon. Tällä hetkellä liitteen tarkastelutoiminto ei sisällä versionhallinta- tai tarkistusominaisuuksia.

### <a name="default-attachment"></a>Oletusliite

Jos toimittajalaskussa on useampia kuin yksi liite , voit määrittää yhden asiakirjan oletusliitteeksi **Liitteet**-sivulla. **On oletusliite** -asetus on tämän toiminnon osaksi lisätty uusi asetus. Tämä asetus on käytettävissä myös toimittajan laskujen asiakirjaliite -tietoyksikössä. Näin oletusliite voidaan määrittää integrointien avulla.

Ainoastaan yksi tiedosto voidaan määrittää oletusliitteeksi. Määritettyäsi asiakirjan oletusliitteeksi se näytetään automaattisesti liitteen katseluohjelmassa laskun avaamisen yhteydessä. Jos et määritä mitään asiakirjaa oletusliitteeksi, liitteen katseluohjelma ei näytetä automaattisesti mitään liitettä laskun avaamisen yhteydessä.

### <a name="showhide-invoice-attachments"></a>Näytä/piilota laskun liitteet

Uudella painikkeella, joka on käytettävissä **Poikkeuksen käsittely**, **Odottava lasku** ja **Laskukirjauskansio** -kyselysivuilla, voit näyttää tai piilottaa liitteiden tarkastelutoiminnon.

### <a name="security"></a>Suojaus

Seuraavia liitteen katseluohjelman toimintoja ohjataan roolipohjaisen suojauksen kautta:

+ Korostus
+ Esto
+ Huomautus

### <a name="pending-vendor-invoices-page"></a>Odottavat toimittajan laskut -sivu

Seuraavat oikeudet mahdollistavat vain luku -tyyppiset käyttöoikeudet tai luku-/kirjoitus-oikeudet liitteen katseluohjelmassa korostamis-, esto- ja huomautustoiminnoille:

+ **Ylläpidä toimittajan laskun kuvan** – Tämä oikeus antaa luku-/kirjoitusoikeudet.
+ **Näytä toimittajan laskun kuva** – Tämä oikeus antaa vain luku -oikeudet.

Seuraavat tehtävät antavat vain luku -oikeudet tai luku-/kirjoitusoikeudet liitteen katseluohjelmalle näissä toiminnoissa:

+ **Toimittajan laskujen ylläpito** : Toimittajan laskujen kuvan ylläpito-oikeus on annettu tälle tehtävälle.
+ **Kohdista kyselyjä toimittajan laskujen tilaan** : Toimittajan laskujen kuvan tarkasteluoikeus on annettu tälle tehtävälle.

Seuraavat roolit antavat vain luku -oikeudet tai luku-/kirjoitusoikeudet liitteen katseluohjelmalle näissä toiminnoissa:

+ **Ostoreskontra-assistentti** ja **Ostoreskontrapäällikkö**: Toimittajan laskujen ylläpito -tehtävä on annettu näille rooleille.
+ **Ostoreskontra-assistentti**, **Ostoreskontrapäällikkö**, **Ostoreskontran keskitetty maksuliikenneassistentti** ja **Ostoreskontran maksuliikenneassistentti**: Kohdista kyselyjä toimittajan laskujen tilaan -velvollisuus on liitetty näihin rooleihin.

### <a name="invoice-exception-details-page"></a>Laskun poikkeustiedot -sivu

Seuraavat oikeudet mahdollistavat vain luku -tyyppiset käyttöoikeudet tai luku-/kirjoitus-oikeudet liitteen katseluohjelmassa korostamis-, esto- ja huomautustoiminnoille.

> [!NOTE]
> Valmiiksi määritetyillä rooleilla, jotka mainitaan tässä osassa, on vain luku -oikeudet laskun kuviin liitteen katseluohjelmassa. Jos roolilla pitää olla myös kirjoitusoikeus kuviin, jos annat kirjoitusoikeudet kyseiselle roolille käyttämällä oikeuksia ja velvollisuuksia, jotka on kuvattu tässä.

+ **Ylläpidä toimittajan laskun otsikon yksikön kuvaa**: Oikeus sisältää luku-/kirjoitusoikeudet laskun kuviin liitteen katseluohjelmassa.
+ **Tarkastele toimittajan laskun otsikon yksikön kuvaa**: Oikeus sisältää vain luku -oikeudet laskun kuvaan liitteen katseluohjelmassa.

Seuraavat tehtävät antavat vain luku -oikeudet liitteen katseluohjelmalle näissä toiminnoissa:

+ **Toimittajan laskujen ylläpito** : Toimittajan laskujen otsikko -yksikön kuvan ylläpito-oikeus on annettu tälle tehtävälle.

Seuraavat roolit antavat vain luku -oikeudet liitteen katseluohjelmalle näissä toiminnoissa:

+ **Ostoreskontra-assistentti** ja **Ostoreskontrapäällikkö**: Toimittajan laskujen ylläpito -tehtävä on annettu näille rooleille.

Oletusarvoisesti jos käyttäjärooli antaa muokkausoikeudet mille tahansa sivulle, käyttäjällä on myös muokkausoikeudet liitteen katseluohjelmassa korostus-, esto- ja huomautustoimintojen osalta. Jos kuitenkin esiintyy skenaarioita, joissa tietyllä roolilla on oltava muokkausoikeudet sivulla mutta ei liitteen katseluohjelmassa, voidaan käyttää edellä olevassa luettelossa esitettyjä ja käyttötapaukseen soveltuvia oikeuksia.

