---
title: Toimittajan laskujen yleiskatsaus
description: "Tässä artikkelissa on yleistietoja toimittajan laskuista. Toimittajan laskut ovat vastaanotettujen tuotteiden ja palveluiden maksupyyntöjä. Toimittajan laskut voivat koskea juoksevia palveluita tai ne voivat perustua tiettyjen nimikkeiden ja palveluiden ostotilauksiin."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13971
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: de536be7b0d25a1b0f662f64a31be26dbcd10c28
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="vendor-invoices-overview"></a>Toimittajan laskujen yleiskatsaus

[!include[banner](../includes/banner.md)]


Tässä artikkelissa on yleistietoja toimittajan laskuista. Toimittajan laskut ovat vastaanotettujen tuotteiden ja palveluiden maksupyyntöjä. Toimittajan laskut voivat koskea juoksevia palveluita tai ne voivat perustua tiettyjen nimikkeiden ja palveluiden ostotilauksiin. 

<a name="vendor-invoices"></a>Toimittajan laskut
---------------

Ostotilauksesta peräisin oleva toimittajan lasku on lasku, joka luodaan, kun tuotteet tai palvelut on vastaanotettu toimittajalle tehdyn ostotilauksen mukaisesti. Toimittajan lasku sisältää otsikon ja yhden tai useamman rivin nimikkeille tai palveluille. Toimittajan lasku päättää ketjun, joka kulkee ostotilauksesta tuotteen vastaanoton kautta toimittajan laskuun. 

Vaikka toimittajan laskuista liittyy ostotilauksiin, toimittajan laskussa voi olla rivejä, jotka eivät vastaa ostotilauksen rivejä. Voit myös luoda toimittajan laskuja, joita ei ole liitetty mihinkään ostotilaukseen. Nämä toimittajan laskut voivat koskea juoksevia palveluja, kuten sähkölasku, eikä niistä tarvitse olla viittausta ostotilaukseen, kun lisäät ne. 

Toimittajan laskun voi kirjata monella tavalla:

-   Voit kirjata toimittajan laskurekisterissä nopeasti laskut, joista ei ole viittausta ostotilaukseen, jotta voit jaksottaa kulun. Toimittajalaskujen hyväksynnän kirjauskansiossa voit puolestaan valita kyseiset laskut ja kirjata ne toimittajan saldoon palauttamaan jaksotus.
-   Voit kirjata toimittajan laskukirjauskansiossa laskut, joissa ei ole viittausta ostotilaukseen, yhdellä vaiheella.
-   Toimittajalaskupooli yhdessä toimittajan laskurekisterin kanssa käytettynä mahdollistaa laskujen nopean kirjaaminen kulun jaksottamiseksi. Voit kirjata laskun kulutilille avaamalla liittyvät ostotilaukset myöhemmin.
-   Voit luoda **Avoimet toimittajan laskut**- ja **Odottavat toimittajan laskut** -sivuilla toimittajan laskut vahvistetuista ostotilauksista.

Seuraavissa osissa on lisätietoja tavoista, joilla voit luoda **Avoimet toimittajan laskut**- tai **Odottavat toimittajan laskut**-sivulla toimittajan laskun ostotilauksesta.

## <a name="understanding-invoice-line-quantities"></a>Laskurivin määrien merkitys
Kun avaat toimittajan laskun liittyvästä ostotilauksesta, laskurivit luodaan ostotilauksesta. Määrät haetaan oletusarvoisesti tuotteen vastaanottomäärästä. Voit kuitenkin mitä tahansa seuraavista oletustoiminnoista:

-   **Vastaanottomäärä nyt** – Käytä tätä vaihtoehtoa osatoimituksissa. **Määrä**-kentän oletusarvo haetaan ostotilauksen **Ota vastaan nyt** -määräkentästä.
-   **Tilattu määrä** – Käytä täydellisissä toimituksissa tätä vaihtoehtoa. **Määrä**-kentän oletusarvo haetaan ostotilauksen **Tilattu**-määräkentästä.
-   **Rekisteröity määrä** – Käytä tätä vaihtoehtoa, jos nimike on rekisteröitävä **Ota vastaan nyt**-sivun määritysten mukaisesti. **Määrä**-kentän oletusarvo on fyysinen päivitetty määrä, joka on rekisteröity.
-   **Tuotteen vastaanottomäärä** – Käytä tätä vaihtoehtoa, jos tilaukseen on jo vastaanotettu tuotteen vastaanotto. **Määrä**-kentän oletusarvo haetaan käytettävissä olevien tuotteen vastaanottojen kokonaismäärästä.
-   **Rekisteröity määrä ja rekisteröidyt palvelut** – Käytä tätä vaihtoehtoa, jos määrä on rekisteröity varastoitavien nimikkeiden tai ei-varastoitavien nimikkeiden saapumisen kirjauskansioihin. Tämä vaihtoehto sisältää myös palveluja, riippumatta siitä, onko niitä rekisteröity.

Jos yritys käyttää laskujen täsmäytystä, voit tarkastella määrän täsmäytyksen tuloksia **Tuotteen vastaanoton määrän vastaavuus** -sarakkeessa. Voit tarkastella määrän täsmäytyksen tuloksia myös käyttämällä **Tarkista**-välilehden **Täsmäytyksen tiedot** -valikkokomentoa.

## <a name="adding-a-line-that-wasnt-on-the-purchase-order"></a>Ostotilauksesta puuttuvan rivin lisääminen
Voit lisätä toimittajan laskuun sellaisen uuden rivin, jota ei ole ostotilauksessa. Valitse nimiketunnus tai hankintaluokka. Voit sitten lisätä riville määrät, hinnat ja summat. Rivi sisällytetään vain laskusummien täsmäytyskäytäntöihin.

## <a name="submitting-a-vendor-invoice-for-review"></a>Toimittajan laskun lähettäminen tarkistettavaksi
Organisaatiosi saattaa hallita toimittajan laskujen tarkistusprosessia työnkulkujen avulla. Työnkulun tarkistusta voidaan edellyttää laskun ylätunnisteeseen, laskuriviin tai molempiin. Työnkulun ohjausobjekteja käytetään otsikkoon tai riviin sen perusteella, missä kohdistus on, kun napsautat ohjausobjektia. **Kirjaa**-painikkeen sijaan näkyvissä on **Lähetä**-painike, jolla voit lähettää toimittajan laskun tarkistusprosessiin.

## <a name="matching-vendor-invoices-to-product-receipts"></a>Toimittajan laskujen täsmäytys tuotteen vastaanottoihin
Voit syöttää ja tallentaa toimittajalaskujen tietoja, ja voit täsmäyttää laskurivit tuotteen vastaanottoriveihin. Voit täsmäyttää riville myös osan määristä. 

Voit luoda toimittajan laskun, joka perustuu tuotteen vastaanoton rivinimikkeisiin, jotka on tähän päivään mennessä vastaanotettu, vaikka kaikkia tietyn ostotilauksen nimikkeitä ei olisikaan vielä vastaanotettu. Voit esimerkiksi käyttää tätä vaihtoehtoa, jos toimittaja lähettää kuukaudessa yhden laskun, joka sisältää kaikki toimittajan kuukauden aikana lähettämät toimitukset. Jokainen tuotteen vastaanotto edustaa ostotilauksen nimikkeiden osatoimitusta tai täydellistä toimitusta. 

Kun kirjaat laskun, jokaisen nimikkeen **Laskuttamatta**-määrä päivitetään valittujen tuotteen vastaanottojen kokonaismäärän mukaiseksi. Jos ostotilauksen kaikkien nimikkeiden **Laskuttamatta**-määrä ja **Jäljellä oleva määrä** on 0 (nolla), ostotilauksen tilaksi muutetaan **Laskutettu**. Jos **Laskuttamatta**-määrä ei ole 0, ostotilauksen tilaa ei muuteta ja siihen voi lisätä laskuja.

Tässä vaihtoehdossa oletetaan, että vähintään yksi tuotteen vastaanotto on kirjattu ostotilaukseen. Toimittajalasku perustuu näiden tuotteiden vastaanottoihin ja vastaa niiden määriä. Laskun kirjanpitotiedot perustuvat tietoihin, jotka syötettiin laskujen kirjauksen yhteydessä.

Lisätietoja on ohjeaiheessa [Toimittajan laskun kirjaaminen ja täsmäyttäminen vastaanotettuihin määriin](../accounts-receivable/tasks/record-vendor-invoice-match-against-received-quantity.md)

## <a name="working-with-multiple-invoices"></a>Useita laskujen käsittely

Voit käsitellä useita laskuja samaan aikaan ja kirjata ne kaikki samaan aikaan. Jos sinun on luotava useita laskuja, käytä **Odottavat toimittajan laskut** -sivua. Jos sinun on kirjattava ja tulostettava useita toimittaja laskuja, käytä laskujen hyväksymiskirjauskansion sivua. Jos käytät laskun hyväksynnän kirjauskansiota, ostotilaukselle on oltava kirjattuna ainakin yksi tuotteen vastaanotto ja että ostotilauksen laskun on oltava kirjattuna laskurekisteriin. Laskun kirjanpitotiedot ovat peräisin laskusta, joka on kirjattu rekisteriin.


Lisätietoja on kohdassa 

 - [Määritä toimittajan laskutuskäytännöt](../accounts-receivable/tasks/set-up-vendor-invoice-policies.md) 

 - [Laskun keskeiset tiedot ostoreskontraan toimittajalaskun avulla](tasks/key-invoice-data-ap-system-vendor-invoice.md)
 
 - [Laskun keskeiset tiedot ostoreskontraan hyväksymiskirjauskansion avulla](tasks/key-invoice-data-into-ap-system-approval-journal.md)
  
 - [Laskun keskeiset tiedot ostoreskontrajärjestelmään laskupoolin avulla](tasks/key-invoice-data-into-ap-system-invoice-pool.md)
 
 - [Toimittajan laskun tallentaminen laskukirjauskansioon](tasks/record-vendor-invoice-invoice-journal.md)


