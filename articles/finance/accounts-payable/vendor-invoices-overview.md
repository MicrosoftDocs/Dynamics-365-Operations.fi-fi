---
title: Toimittajan laskujen yleiskatsaus
description: Tässä aiheessa on yleistietoja toimittajan laskuista.
author: abruer
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3fac6a0232f7e51e859fcc5b23244be092ce8d76123ec42f586063a02abab603
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722788"
---
# <a name="vendor-invoices-overview"></a>Toimittajan laskujen yleiskatsaus

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Tässä aiheessa on yleistietoja toimittajan laskuista. Toimittajan laskut ovat tuotteiden ja palveluiden maksupyyntöjä. Toimittajan laskut voivat koskea juoksevia palveluita tai ne voivat perustua tiettyjen nimikkeiden ja palveluiden ostotilauksiin.

## <a name="vendor-invoices"></a>Toimittajan laskut

Ostotilauksesta peräisin oleva toimittajan lasku luodaan, kun tuotteet tai palvelut on vastaanotettu toimittajalle tehdyn ostotilauksen mukaisesti. Toimittajan lasku sisältää otsikon ja yhden tai useamman rivin nimikkeille tai palveluille. Toimittajan lasku päättää ketjun, joka kulkee ostotilauksesta tuotteen vastaanoton kautta toimittajan laskuun.

Vaikka toimittajan laskut liittyvät ostotilauksiin, toimittajan laskussa voi olla rivejä, jotka eivät vastaa ostotilauksen rivejä. Voit myös luoda toimittajan laskuja, joita ei ole liitetty mihinkään ostotilaukseen. Nämä toimittajan laskut voivat edustaa jatkuvia palveluita, kuten sähkölaskua. Kun lisäät jatkuvan palvelun, sinun ei tarvitse viitata ostotilaukseen.

Toimittajan laskun voi kirjata monella tavalla:

- Voit kirjata toimittajan laskurekisterissä nopeasti laskut, joista ei ole viittausta ostotilaukseen, jotta voit jaksottaa kulun. Toimittajalaskujen hyväksynnän kirjauskansiossa voit puolestaan valita kyseiset laskut ja kirjata ne toimittajan saldoon palauttamaan jaksotus.
- Voit kirjata toimittajan laskukirjauskansiossa laskut, joissa ei ole viittausta ostotilaukseen, yhdellä vaiheella.
- Toimittajalaskupooli yhdessä toimittajan laskurekisterin kanssa käytettynä mahdollistaa laskujen nopean kirjaaminen kulun jaksottamiseksi. Voit kirjata laskun kulutilille avaamalla liittyvät ostotilaukset myöhemmin.
- Voit luoda **Avoimet toimittajan laskut**- ja **Odottavat toimittajan laskut** -sivuilla toimittajan laskut vahvistetuista ostotilauksista.

Seuraavissa osissa on lisätietoja tavoista, joilla voit luoda **Avoimet toimittajan laskut**- tai **Odottavat toimittajan laskut**-sivulla toimittajan laskun ostotilauksesta.

## <a name="understanding-invoice-line-quantities"></a>Laskurivin määrien merkitys

Kun avaat toimittajan laskun liittyvästä ostotilauksesta, järjestelmä luo laskurivit ostotilauksesta. Järjestelmä noutaa määrät oletusarvoisesti tuotteen vastaanotosta. Voit kuitenkin mitä tahansa seuraavista oletustoiminnoista:

- **Vastaanottomäärä nyt** – Käytä tätä vaihtoehtoa osatoimituksissa. Järjestelmä määrittää oletusarvon **Määrä**-kentässä ostotilauksen **Ota vastaan nyt** -kentässä määritetystä määrästä.
- **Tilattu määrä** – Käytä täydellisissä toimituksissa tätä vaihtoehtoa. Järjestelmä määrittää oletusarvon **Määrä**-kentässä ostotilauksen **Tilattu** -kentässä määritetystä määrästä.
- **Rekisteröity määrä** – Käytä tätä vaihtoehtoa, jos nimike on rekisteröitävä **Ota vastaan nyt**-sivun määritysten mukaisesti. **Määrä**-kentän oletusarvo on fyysinen päivitetty määrä, joka on rekisteröity.
- **Tuotteen vastaanottomäärä** – Käytä tätä vaihtoehtoa, jos tilaukseen on jo vastaanotettu tuotteen vastaanotto. Järjestelmä ottaa oletusarvon **Määrä**-kentästä käytettävissä olevien tuotteen vastaanottojen kokonaismäärästä.
- **Rekisteröity määrä ja rekisteröidyt palvelut** – Käytä tätä vaihtoehtoa, jos määrä on rekisteröity varastoitavien nimikkeiden tai ei-varastoitavien nimikkeiden saapumisen kirjauskansioihin. Tämä vaihtoehto sisältää myös palveluja, riippumatta siitä, onko niitä rekisteröity.

Jos yritys käyttää laskujen täsmäytystä, voit tarkastella määrän täsmäytyksen tuloksia **Tuotteen vastaanoton määrän vastaavuus** -sarakkeessa. Voit tarkastella määrän täsmäytyksen tuloksia myös käyttämällä toimintoruudun **Tarkista**-välilehden **Täsmäytyksen tiedot** -painiketta.

## <a name="adding-a-line-that-wasnt-on-the-purchase-order"></a>Ostotilauksesta puuttuvan rivin lisääminen

Voit lisätä toimittajan laskuun sellaisen rivin, jota ei ole ostotilauksessa. Valitse nimiketunnus tai hankintaluokka. Voit sitten lisätä riville määrät, hinnat ja summat. Rivi sisällytetään vain laskusummien täsmäytyskäytäntöihin.

## <a name="submitting-a-vendor-invoice-for-review"></a>Toimittajan laskun lähettäminen tarkistettavaksi

Organisaatiosi saattaa hallita toimittajan laskujen tarkistusprosessia työnkulkujen avulla. Työnkulun tarkistusta voidaan edellyttää laskun ylätunnisteeseen, laskuriviin tai molempiin. Työnkulun ohjausobjekteja käytetään otsikkoon tai riviin sen perusteella, missä kohdistus on, kun valitset ohjausobjektin. **Kirjaa**-painikkeen sijaan näkyvissä on **Lähetä**-painike, jolla voit lähettää toimittajan laskun tarkistusprosessiin.

### <a name="preventing-invoice-from-being-submitted-to-workflow"></a>Estetään laskua lähtemästä työnkulkuun 

Seuraavilla tavoilla voi estää laskua lähtemästä työnkulkuun.

- **Laskun kokonaissumma ja rekisteröity kokonaissumma eivät ole samat.** Laskun lähettänyt henkilö saa hälytyksen, jonka mukaan yhteissummat eivät ole yhtä suuret. Hälytyksen kautta voit korjata saldot, ennen kuin lasku lähetetään uudelleen työnkulkuun. Tämä toiminto on käytettävissä, jos **Estä lähetys työnkulkuun, jos laskun kokonaissumma ja rekisteröidyn laskun kokonaissumma eivät ole samat** -parametri **Toimintojen hallinta** -sivulla on otettu käyttöön. 

- **Lasku sisältää kohdistamattomia kuluja.** Laskun lähettänyt henkilö saa hälytyksen, jonka mukaan laskulla on kohdistamattomia kuluja. Tämän jälkeen lasku voidaan korjata ennen sen lähettämistä työnkulkuun. Tämä toiminto on käytettävissä, jos **Estä lähetys työnkulkuun, jos toimittajan laskussa on kohdistamattomia kuluja** -parametri **Toimintojen hallinta** -sivulla on otettu käyttöön.

- **Lasku sisältää saman laskunumeron kuin toinen kirjattu lasku.** Laskun lähettänyt henkilö saa sanoman, jossa ilmoitetaan, että lasku, jonka numero on kaksoiskappale, löydettiin. Numeron kaksoiskappaleen voi korjata, ennen kuin lasku lähetetään uudelleen työnkulkuun. Tämä hälytys näytetään, kun Ostoreskontra-parametrin **Tarkista käytetty laskunumero** arvoksi on määritetty **Hylkää kaksoiskappale**. Tämä toiminto on käytettävissä, jos **Estä lähetys työnkulkuun, jos laskunumero on jo olemassa kirjatussa laskussa ja järjestelmää ei ole määritetty hyväksymään laskunumeroiden kaksoiskappaleita** -parametri **Toimintojen hallinta** -sivulla on otettu käyttöön.

- **Lasku sisältää rivin, jonka laskun määrä on pienempi kuin täsmäytetty tuotteen vastaanottomäärä.** Henkilö, joka lähettää laskun tai yrittää kirjata sen, saa sanoman, jonka mukaan määrät eivät täsmää. Sanoman kautta voit korjata arvot, ennen kuin lasku lähetetään uudelleen työnkulkuun. Tämä ominaisuus on käytettävissä, jos **Estä toimittajan laskujen kirjaaminen ja lähettäminen työnkulkuun** -parametriin on otettu käyttöön **ominaisuuden hallinta** -sivulla ja **Ostoreskontran parametrit** -sivun **Estä kirjaus ja lähetys työnkulkuparametriin** -toiminto on käytössä.  

## <a name="matching-vendor-invoices-to-product-receipts"></a>Toimittajan laskujen täsmäytys tuotteen vastaanottoihin

Voit syöttää ja tallentaa toimittajalaskujen tietoja, ja voit täsmäyttää laskurivit tuotteen vastaanottoriveihin. Voit täsmäyttää riville myös osan määristä.

Voit luoda toimittajan laskun, joka perustuu tuotteen vastaanoton rivinimikkeisiin, jotka on tähän päivään mennessä vastaanotettu, vaikka kaikkia tietyn ostotilauksen nimikkeitä ei olisikaan vielä vastaanotettu. Voit esimerkiksi käyttää tätä vaihtoehtoa, jos toimittaja lähettää kuukaudessa yhden laskun, joka sisältää kaikki sen kuukauden aikana lähettämät toimitukset. Jokainen tuotteen vastaanotto edustaa ostotilauksen nimikkeiden osatoimitusta tai täydellistä toimitusta.

Kun lasku on työnkulussa, hyväksyjä voi päivittää laskujen määrät niin, että ne vastaavat **Kohdistettava tuotteen vastaanoton määrä** -kentän arvoa. Voit tehdä tämän valitsemalla **Päivitä laskun määrät vastaamaan tuotteiden vastaanottomääriä työnkulussa** -toiminnon **Ominaisuuden hallinta** -työtilassa ja valitsemalla **Ota käyttöön**. Jos työnkulkuprosessin hyväksyjä on poistanut kaikki vastaavuudet laskuriviltä kaikista tuotevastaanottoista, laskurivi poistetaan. Kun tämä toiminto ei ole käytössä, työnkulun laskujen määriä ei päivitetä.

Kun kirjaat laskun, jokaisen nimikkeen **Laskuttamatta**-määrä päivitetään valittujen tuotteen vastaanottojen kokonaismäärän mukaiseksi. Jos ostotilauksen kaikkien nimikkeiden **Laskuttamatta**-määrä ja **Jäljellä oleva määrä** on 0 (nolla), ostotilauksen tilaksi muutetaan **Laskutettu**. Jos **Laskuttamatta**-määrä ei ole 0, ostotilauksen tilaa ei muuteta ja siihen voi lisätä laskuja.

Tässä vaihtoehdossa oletetaan, että vähintään yksi tuotteen vastaanotto on kirjattu ostotilaukseen. Toimittajalasku perustuu näiden tuotteiden vastaanottoihin ja vastaa niiden määriä. Laskun kirjanpitotiedot perustuvat tietoihin, jotka syötettiin laskujen kirjauksen yhteydessä.

Lisätietoja on ohjeaiheessa [Toimittajan laskun kirjaaminen ja täsmäyttäminen vastaanotettuihin määriin](../accounts-payable/tasks/record-vendor-invoice-match-against-received-quantity.md)

## <a name="configure-an-automated-task-for-vendor-invoice-workflow-to-post-the-vendor-invoice-using-a-batch-job"></a>Toimittajan laskun työnkulun automaattisen tehtävän määrittäminen toimittajan laskun kirjaamiseksi erätyön avulla

Voit lisätä automaattisen kirjaustehtävän toimittajan laskun työnkulkuun niin, että laskut käsitellään eränä. Kun laskut kirjataan eränä, työnkulkuprosessi jatkaa. Se ei odota, että kirjaaminen on tehty. Tämä parantaa kaikkien työnkulkuun lähetettävien tehtävien yleistä suorituskykyä.

Jos haluat kirjata toimittajan laskun eränä, ota käyttöön **Toimintojen hallinta** -sivulla **Toimittajan laskun erän kirjaus** -parametri. Toimittajan laskun työnkulut määritetään siirtymällä kohtaan **Ostoreskontra > Asetukset > Ostoreskontran työnkulut**.

Voit nähdä **Kirjaa toimittajan lasku erän avulla** -tehtävän työnkulun editorissa siitä huolimatta, onko toiminnon **Toimittajan laskun erän kirjaus** -parametri käytössä vai ei. Kun toiminnon parametria ei ole otettu käyttöön, **Kirjaa toimittajan lasku käyttämällä erätehtävää** -parametrin sisältävää laskua ei käsitellä työnkulussa, jos parametri ei ole käytössä. **Kirjaa toimittajan lasku erän avulla** -tehtävää ei voi käyttää samassa työnkulussa kuin automaattista **Kirjaa toimittajan laskut** -tehtävää. Lisäksi **Kirjaa toimittajan lasku erän avulla** -tehtävän tulisi olla työnkulun kokoonpanon viimeinen elementti.

Voit määrittää erään sisällytettävien laskujen määrän ja odotusajan tunteina. Tämän jälkeen erä ajoitetaan uudelleen siirtymällä kohtaan **Ostoreskontra > Asetukset > Ostoreskontran parametrit > Lasku > Laskun työnkulku**. 

## <a name="working-with-multiple-invoices"></a>Useita laskujen käsittely

Voit käsitellä useita laskuja samaan aikaan ja kirjata ne kaikki samaan aikaan. Jos sinun on luotava useita laskuja, käytä **Odottavat toimittajan laskut** -sivua. Jos sinun on kirjattava ja tulostettava useita toimittaja laskuja, käytä laskujen hyväksymiskirjauskansiota. Jos käytät laskun hyväksynnän kirjauskansiota, ostotilaukselle on oltava kirjattuna ainakin yksi tuotteen vastaanotto ja että ostotilauksen laskun on oltava kirjattuna laskurekisteriin. Laskun kirjanpitotiedot ovat peräisin laskusta, joka on kirjattu rekisteriin.

## <a name="recovering-vendor-invoices-that-are-being-used"></a>Palauta toimittajalaskut, joita käytetään

Toimittajalaskua käytettäessä sitä ei voi muokata toiselle käyttäjälle. Laskun tila voi toisinaan tarkoittaa, että lasku on käytössä, vaikka sitä ei ole aktiivisesti muokattu. Sovellus on esimerkiksi saattanut lakata vastaamasta laskun muokkaamisen aikana, tai käyttäjä on saattanut jättää tahattomasti laskun auki sovelluksessa.

Voit käyttää **Palauta toimittajalaskut** -sivua palauttaaksesi tai vapauttaaksesi toimittajalaskut, jotka ovat olleet käytössä yli 4 tuntia, jotta niitä voidaan muokata. Voit avata sivun **Kausittainen tehtävä** -valikosta tai -ruudusta **Laskun toimittajatapahtuma**-työtilassa. Kun lasku on palautettu, se on käytettävissä muokkaamista varten **Toimittajalasku**-sivulla.

Saat käyttöösi **Palauttaa toimittajalaskut** -sivun vain, jos **Palauta käytössä olevat toimittajalaskut** -suojausvelvollisuudet ja oikeudet on määritetty itsellesi. Lisäksi **Salli toimittajalaskun palautus** -parametri **Ostoreskontran parametrit** -sivulla on otettu käyttöön.

## <a name="resetting-the-workflow-status-for-vendor-invoices-from-unrecoverable-to-draft"></a>Työn kulun tilan nollaaminen toimittajan laskuja varten laskusta, jota ei voi palauttaa luonnokseksi

Peruuttamattoman virheen vuoksi pysäytetyn työnkulun esiintymän työnkulun tila on **peruuttamaton**. Kun toimittajan laskun työnkulun tila on **Peruuttamaton**, voit palauttaa sen **Luonnos**-tilaan valitsemalla **Peruuta**. Voit sitten muokata toimittajan laskua. Tämä toiminto on käytettävissä, jos **Työnkulun tilan nollaaminen toimittajan laskuja varten laskusta, jota ei voi palauttaa luonnokseksi** -parametri **Toimintojen hallinta** -sivulla on käytössä.

Voit palauttaa työnkulun tilaksi **Luonnos** käyttämällä **Työnkulkuhistoria**-sivua. Voit avata tämän sivun **Toimittajan lasku** -kohdasta tai kohdasta **Yhteiset > Kyselee** > Työnkulku. Voit nollata työn kulun tilaksi **Luonnos** valitsemalla **Peruuta**. Voit myös nollata työn kulun tilaksi Luonnos valitsemalla **Peruuta**-toiminnon **Toimittajan lasku**- tai **Odottavat toimittajan laskut** -sivulla. Kun työnkulun tila palautetaan **luonnos**-tilaan, se on muokattavissa **toimittajan lasku** -sivulla.

## <a name="viewing-the-invoice-total-on-the-pending-vendor-invoices-page"></a>Odottavat toimittajan laskut -sivun laskun kokonaissumman tarkasteleminen
Voit tarkastella laskujen kokonaismäärää **Odottavat toimittajan laskut** -sivulla ottamalla käyttöön **Näytä laskun loppusumma odottavien toimittajalaskujen luettelossa** -parametrin **Ostoreskontran parametrit** -sivulla. 



## <a name="additional-resources"></a>Lisäresurssit

- [Määritä toimittajan laskutuskäytännöt](../accounts-receivable/tasks/set-up-vendor-invoice-policies.md)
- [Ostoreskontrajärjestelmän avaintiedot toimittajan laskua käyttämällä](tasks/key-invoice-data-ap-system-vendor-invoice.md)
- [Laskun keskeiset tiedot ostoreskontraan hyväksymiskirjauskansion avulla](tasks/key-invoice-data-into-ap-system-approval-journal.md)
- [Laskun keskeiset tiedot ostoreskontrajärjestelmään laskupoolin avulla](tasks/key-invoice-data-into-ap-system-invoice-pool.md)
- [Toimittajan laskun tallentaminen laskukirjauskansioon](tasks/record-vendor-invoice-invoice-journal.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
