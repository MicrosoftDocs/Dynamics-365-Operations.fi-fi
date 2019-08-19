---
title: Toimittajan laskujen yleiskatsaus
description: Tässä aiheessa on yleistietoja toimittajan laskuista. Toimittajan laskut ovat vastaanotettujen tuotteiden ja palveluiden maksupyyntöjä. Toimittajan laskut voivat koskea juoksevia palveluita tai ne voivat perustua tiettyjen nimikkeiden ja palveluiden ostotilauksiin.
author: abruer
manager: AnnBe
ms.date: 07/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13971
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c69291214796847af7169cf261865860998f0d27
ms.sourcegitcommit: 299e20b59ebefa584ed46a13da3f1a7ff709e43c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2019
ms.locfileid: "1863320"
---
# <a name="vendor-invoices-overview"></a>Toimittajan laskujen yleiskatsaus

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Tässä aiheessa on yleistietoja toimittajan laskuista. Toimittajan laskut ovat vastaanotettujen tuotteiden ja palveluiden maksupyyntöjä. Toimittajan laskut voivat koskea juoksevia palveluita tai ne voivat perustua tiettyjen nimikkeiden ja palveluiden ostotilauksiin.

## <a name="vendor-invoices"></a>Toimittajan laskut

Ostotilauksesta peräisin oleva toimittajan lasku on lasku, joka luodaan, kun tuotteet tai palvelut on vastaanotettu toimittajalle tehdyn ostotilauksen mukaisesti. Toimittajan lasku sisältää otsikon ja yhden tai useamman rivin nimikkeille tai palveluille. Toimittajan lasku päättää ketjun, joka kulkee ostotilauksesta tuotteen vastaanoton kautta toimittajan laskuun.

Vaikka toimittajan laskuista liittyy ostotilauksiin, toimittajan laskussa voi olla rivejä, jotka eivät vastaa ostotilauksen rivejä. Voit myös luoda toimittajan laskuja, joita ei ole liitetty mihinkään ostotilaukseen. Nämä toimittajan laskut voivat koskea juoksevia palveluja, kuten sähkölasku, eikä niistä tarvitse olla viittausta ostotilaukseen, kun lisäät ne.

Toimittajan laskun voi kirjata monella tavalla:

- Voit kirjata toimittajan laskurekisterissä nopeasti laskut, joista ei ole viittausta ostotilaukseen, jotta voit jaksottaa kulun. Toimittajalaskujen hyväksynnän kirjauskansiossa voit puolestaan valita kyseiset laskut ja kirjata ne toimittajan saldoon palauttamaan jaksotus.
- Voit kirjata toimittajan laskukirjauskansiossa laskut, joissa ei ole viittausta ostotilaukseen, yhdellä vaiheella.
- Toimittajalaskupooli yhdessä toimittajan laskurekisterin kanssa käytettynä mahdollistaa laskujen nopean kirjaaminen kulun jaksottamiseksi. Voit kirjata laskun kulutilille avaamalla liittyvät ostotilaukset myöhemmin.
- Voit luoda **Avoimet toimittajan laskut**- ja **Odottavat toimittajan laskut** -sivuilla toimittajan laskut vahvistetuista ostotilauksista.

Seuraavissa osissa on lisätietoja tavoista, joilla voit luoda **Avoimet toimittajan laskut**- tai **Odottavat toimittajan laskut**-sivulla toimittajan laskun ostotilauksesta.

## <a name="understanding-invoice-line-quantities"></a>Laskurivin määrien merkitys

Kun avaat toimittajan laskun liittyvästä ostotilauksesta, laskurivit luodaan ostotilauksesta. Määrät haetaan oletusarvoisesti tuotteen vastaanottomäärästä. Voit kuitenkin mitä tahansa seuraavista oletustoiminnoista:

- **Vastaanottomäärä nyt** – Käytä tätä vaihtoehtoa osatoimituksissa. **Määrä**-kentän oletusarvo haetaan ostotilauksen **Ota vastaan nyt** -kentässä määritetystä määrästä.
- **Tilattu määrä** – Käytä täydellisissä toimituksissa tätä vaihtoehtoa. **Määrä**-kentän oletusarvo haetaan ostotilauksen **Tilattu**-kentässä määritetystä määrästä.
- **Rekisteröity määrä** – Käytä tätä vaihtoehtoa, jos nimike on rekisteröitävä **Ota vastaan nyt**-sivun määritysten mukaisesti. **Määrä**-kentän oletusarvo on fyysinen päivitetty määrä, joka on rekisteröity.
- **Tuotteen vastaanottomäärä** – Käytä tätä vaihtoehtoa, jos tilaukseen on jo vastaanotettu tuotteen vastaanotto. **Määrä**-kentän oletusarvo haetaan käytettävissä olevien tuotteen vastaanottojen kokonaismäärästä.
- **Rekisteröity määrä ja rekisteröidyt palvelut** – Käytä tätä vaihtoehtoa, jos määrä on rekisteröity varastoitavien nimikkeiden tai ei-varastoitavien nimikkeiden saapumisen kirjauskansioihin. Tämä vaihtoehto sisältää myös palveluja, riippumatta siitä, onko niitä rekisteröity.

Jos yritys käyttää laskujen täsmäytystä, voit tarkastella määrän täsmäytyksen tuloksia **Tuotteen vastaanoton määrän vastaavuus** -sarakkeessa. Voit tarkastella määrän täsmäytyksen tuloksia myös käyttämällä toimintoruudun **Tarkista**-välilehden **Täsmäytyksen tiedot** -painiketta.

## <a name="adding-a-line-that-wasnt-on-the-purchase-order"></a>Ostotilauksesta puuttuvan rivin lisääminen

Voit lisätä toimittajan laskuun sellaisen rivin, jota ei ole ostotilauksessa. Valitse nimiketunnus tai hankintaluokka. Voit sitten lisätä riville määrät, hinnat ja summat. Rivi sisällytetään vain laskusummien täsmäytyskäytäntöihin.

## <a name="submitting-a-vendor-invoice-for-review"></a>Toimittajan laskun lähettäminen tarkistettavaksi

Organisaatiosi saattaa hallita toimittajan laskujen tarkistusprosessia työnkulkujen avulla. Työnkulun tarkistusta voidaan edellyttää laskun ylätunnisteeseen, laskuriviin tai molempiin. Työnkulun ohjausobjekteja käytetään otsikkoon tai riviin sen perusteella, missä kohdistus on, kun valitset ohjausobjektin. **Kirjaa**-painikkeen sijaan näkyvissä on **Lähetä**-painike, jolla voit lähettää toimittajan laskun tarkistusprosessiin.

## <a name="matching-vendor-invoices-to-product-receipts"></a>Toimittajan laskujen täsmäytys tuotteen vastaanottoihin

Voit syöttää ja tallentaa toimittajalaskujen tietoja, ja voit täsmäyttää laskurivit tuotteen vastaanottoriveihin. Voit täsmäyttää riville myös osan määristä.

Voit luoda toimittajan laskun, joka perustuu tuotteen vastaanoton rivinimikkeisiin, jotka on tähän päivään mennessä vastaanotettu, vaikka kaikkia tietyn ostotilauksen nimikkeitä ei olisikaan vielä vastaanotettu. Voit esimerkiksi käyttää tätä vaihtoehtoa, jos toimittaja lähettää kuukaudessa yhden laskun, joka sisältää kaikki sen kuukauden aikana lähettämät toimitukset. Jokainen tuotteen vastaanotto edustaa ostotilauksen nimikkeiden osatoimitusta tai täydellistä toimitusta.

Kun kirjaat laskun, jokaisen nimikkeen **Laskuttamatta**-määrä päivitetään valittujen tuotteen vastaanottojen kokonaismäärän mukaiseksi. Jos ostotilauksen kaikkien nimikkeiden **Laskuttamatta**-määrä ja **Jäljellä oleva määrä** on 0 (nolla), ostotilauksen tilaksi muutetaan **Laskutettu**. Jos **Laskuttamatta**-määrä ei ole 0, ostotilauksen tilaa ei muuteta ja siihen voi lisätä laskuja.

Tässä vaihtoehdossa oletetaan, että vähintään yksi tuotteen vastaanotto on kirjattu ostotilaukseen. Toimittajalasku perustuu näiden tuotteiden vastaanottoihin ja vastaa niiden määriä. Laskun kirjanpitotiedot perustuvat tietoihin, jotka syötettiin laskujen kirjauksen yhteydessä.

Lisätietoja on ohjeaiheessa [Toimittajan laskun kirjaaminen ja täsmäyttäminen vastaanotettuihin määriin](../accounts-receivable/tasks/record-vendor-invoice-match-against-received-quantity.md)

## <a name="working-with-multiple-invoices"></a>Useita laskujen käsittely

Voit käsitellä useita laskuja samaan aikaan ja kirjata ne kaikki samaan aikaan. Jos sinun on luotava useita laskuja, käytä **Odottavat toimittajan laskut** -sivua. Jos sinun on kirjattava ja tulostettava useita toimittaja laskuja, käytä laskujen hyväksymiskirjauskansiota. Jos käytät laskun hyväksynnän kirjauskansiota, ostotilaukselle on oltava kirjattuna ainakin yksi tuotteen vastaanotto ja että ostotilauksen laskun on oltava kirjattuna laskurekisteriin. Laskun kirjanpitotiedot ovat peräisin laskusta, joka on kirjattu rekisteriin.

## <a name="recovering-vendor-invoices-that-are-being-used"></a>Palauta toimittajalaskut, joita käytetään

Toimittajalaskua käytettäessä sitä ei voi muokata toiselle käyttäjälle. Laskun tila voi toisinaan tarkoittaa, että lasku on käytössä, vaikka sitä ei ole aktiivisesti muokattu. Sovellus on esimerkiksi saattanut lakata vastaamasta laskun muokkaamisen aikana, tai käyttäjä on saattanut jättää tahattomasti laskun auki sovelluksessa.

Voit käyttää **Palauta toimittajalaskut** -sivua palauttaaksesi tai vapauttaaksesi toimittajalaskut, jotka ovat olleet käytössä yli 4 tuntia, jotta niitä voidaan muokata. Voit avata sivun **Kausittainen tehtävä** -valikosta tai -ruudusta **Laskun toimittajatapahtuma**-työtilassa. Kun lasku on palautettu, se on käytettävissä muokkaamista varten **Toimittajalasku**-sivulla.

Saat käyttöösi **Palauttaa toimittajalaskut** -sivun vain, jos **Palauta käytössä olevat toimittajalaskut** -suojausvelvollisuudet ja oikeudet on määritetty itsellesi. Lisäksi **Salli toimittajalaskun palautus** -parametri **Ostoreskontran parametrit** -sivulla on otettu käyttöön.

## <a name="resetting-the-workflow-status-for-vendor-invoices-from-unrecoverable-to-draft"></a>Työn kulun tilan nollaaminen toimittajan laskuja varten laskusta, jota ei voi palauttaa luonnokseksi

Peruuttamattoman virheen vuoksi pysäytetyn työnkulun esiintymän työnkulun tila on **peruuttamaton**. Kun toimittajan laskun työnkulun tila on **Peruuttamaton**, voit palauttaa sen **Luonnos**-tilaan valitsemalla **Peruuta**. Voit sitten muokata toimittajan laskua. Tämä toiminto on käytettävissä, jos **ominaisuuden hallinta** -sivun **toimittajan laskun työnkulun parametrin palautusluonnos** on päällä.

Voit palauttaa työnkulun tilaksi **Luonnos** käyttämällä **Työnkulkuhistoria**-sivua. Voit avata tämän sivun **Toimittajan lasku** -kohdasta tai kohdasta **Yhteiset > Kyselee** > Työnkulku. Voit nollata työn kulun tilaksi **Luonnos**valitsemalla **Peruuta**. Voit myös nollata työn kulun tilaksi Luonnos valitsemalla **Peruuta**-toiminnon **Toimittajan lasku**- tai **Odottavat toimittajan laskut** -sivulla. Kun työnkulun tila palautetaan **luonnos**-tilaan, se on muokattavissa **toimittajan lasku** -sivulla.



## <a name="additional-resources"></a>Lisäresurssit

- [Määritä toimittajan laskutuskäytännöt](../accounts-receivable/tasks/set-up-vendor-invoice-policies.md)
- [Laskun keskeiset tiedot ostoreskontraan toimittajalaskun avulla](tasks/key-invoice-data-ap-system-vendor-invoice.md)
- [Laskun keskeiset tiedot ostoreskontraan hyväksymiskirjauskansion avulla](tasks/key-invoice-data-into-ap-system-approval-journal.md)
- [Laskun keskeiset tiedot ostoreskontrajärjestelmään laskupoolin avulla](tasks/key-invoice-data-into-ap-system-invoice-pool.md)
- [Toimittajan laskun tallentaminen laskukirjauskansioon](tasks/record-vendor-invoice-invoice-journal.md)
