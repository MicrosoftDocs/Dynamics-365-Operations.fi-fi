---
title: Tuottokirjaus myyntitilauksiin
description: Tässä aiheessa kuvataan tuottojen myyntitilauksiin ja laskuihin kirjaamisen perustoiminto. Tuottokirjaus on käytettävissä myyntitilauksessa ja laskussa, joka luodaan myyntitilauksen perusteella.
author: kweekley
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 7aaa5e7c3b568400c72a1a84b5f29082579aeeae
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725481"
---
# <a name="revenue-recognition-on-sales-orders"></a>Tuottokirjaus myyntitilauksiin

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Tuoton kirjaustoimintoa ei voi ottaa käyttöön ominaisuuksien hallinnan avulla. Tällä hetkellä se on otettava käyttöön konfigurointiavainten avulla.

Tässä aiheessa kuvataan tuottojen myyntitilauksiin ja laskuihin kirjaamisen perustoiminto. Tuottokirjaus on käytettävissä myyntitilauksessa ja laskussa, joka luodaan myyntitilauksen perusteella. Myyntitilaus voidaan luoda myös aika- ja materiaaliprojektilla.

> [!NOTE]
> Tämän ohjeaiheen kuvissa, sarakkeita on piilotettu tai lisätty ruudukoihin, jotta konseptit näkyvät selkeämmin. Siten kuvien sivut ja tiedot voivat poiketa siitä, mitä tuotteessa näkyy.

## <a name="enter-a-sales-order"></a>Myyntitilauksen syöttäminen

Seuraava myyntitilaus syötetään. Se sisältää kolme nimikettä, jotka määritetään tuottokirjausta varten.

[![Myyntitilauksen syöttäminen.](./media/revenue-recognition-so-basic-sales-order-header.png)](./media/revenue-recognition-so-basic-sales-order-header.png)

Tuottokirjaukselle on kaksi konseptia:

- **Tuottohinnan määritys.** Tuottohinta lasketaan vapautettujen tuotteiden määritysten perusteella. Tuottohinta ei koskaan näy asiakkaalle, vaan sitä käytetään vain myyntitilauksen laskun kirjanpidossa. Myyntitilausrivit ja osana myyntiä tulostetuissa asiakirjoissa näkyy edelleen yksikkö-/luettelohinta.
- **Määritä, milloin tuottokirjauksen pitäisi tapahtua.** Tuoton kirjaamisajankohdan määrityksessä käytetään tuottoaikataulua.

    Tässä esimerkissä ensimmäinen nimike, S0001, kohdistetaan **1O** (yhden esiintymän) -tuottoaikatauluun. Tämä rivi edustaa välitavoiteskenaariota, jossa tuotto kirjataan sen jälkeen, kun asennus on toteutunut tulevaisuudessa. Sen vuoksi tuottoa siirretään siihen asti, että asennus on suoritettu.

    Toinen nimike, S0008, on palvelunimike, joka on määritetty sopimuksenjälkeisen tuen (PCS:n) nimikkeeksi. Jatkuvat kehityspalvelut tuotetaan asiakkaalle 12 kuukauden ajan. Siten tuotteelle kohdistetaan oletusarvoisesti **12M**-tuottoaikataulu. Koska kyseessä on PCS-nimike, sopimuksen alkamis- ja päättymispäivät on määritettävä. Oletusarvoisesti sopimuksen alkamis- ja päättymispäivät löytyvät nimiketietojen Määritys-välilehdeltä. Tuottoaikataulussa asetuksen arvoksi määritetään **12M**, jolloin sopimusehdot täytetään automaattisesti seuraavan kuvan mukaisesti.

    [![Tuottoaikataulut.](./media/revenue-recognition-so-basic-revenue-schedules.png)](./media/revenue-recognition-so-basic-revenue-schedules.png)

    Kolmas nimike, S0012, on laitteistoa, eikä sille kohdisteta oletusarvoisesti tuottoaikataulua. Laitteistosta saatu tuotto kirjataan heti kun nimike laskutetaan.

## <a name="confirm-the-sales-order"></a>Myyntitilauksen vahvistaminen

Lisätietoja tuottohinnasta ja tuottoaikataulusta saa käyttämällä myyntitilauksen toimintoruudun **Hallinta**-välilehden **Tuottokirjaus**-ryhmän painikkeita. Koska myyntitilausta ei ole vahvistettu tässä vaiheessa, tuottokirjausta varten käytettävät painikkeet eivät ole käytettävissä. Nämä painikkeet ovat käytettävissä tai käyttämättömissä sen mukaan, missä vaiheessa täyttämistä myyntitilaus on.

[![Myyntitilauksen ylätunniste.](./media/revenue-recognition-so-basic-sales-order-header-02.png)](./media/revenue-recognition-so-basic-sales-order-header-02.png)

Kolmella ensimmäisellä painikkeella saa tietoja tuottokirjausta varten määritetyn myyntitilauksen nimikkeiden tuottohinnasta.

- **Tuottohinnan kohdistus** – Tämä painike on käytettävissä, kun myyntitilaus on vahvistettu tai lasku on kirjattu. Sekä myyntitilauksen vahvistamisessa että laskun kirjaamisessa tuotto lasketaan sen hinnan kirjaamiseksi, joka kirjataan tai jota siirretään kirjanpitomerkinnällä. Määrityksestä riippuen laskettava tuottohinta voi poiketa asiakkaalle näytettävästä yksikköhinnasta.
- **Kohdista hinta uudelleen uusille tilausriveille** – Tämä painike on käytettävissä, kun myyntitilaus on vahvistettu tai lasku on kirjattu. Uudelleenkohdistusprosessia käytetään sen tuoton uudelleen laskemiseen, joka on kirjattava sen jälkeen, kun uusi rivi lisätään nykyiseen myyntitilaukseen laskutuksen jälkeen tai uuteen myyntitilauksen. Molemmissa tapauksissa uuden nimikkeen lisäys muuttaa sopimusta. Tämän vuoksi tuottohinta on kohdistettava uudelleen.
- **Päivitä tuottohinnan kohdistus** – Tämä painike tulee käyttöön, kun myyntitilaus on vahvistettu, mutta poistuu käytöstä, kun myyntitilaus on laskutettu. Päivitystä käytettään tuottohinnan kohdistuksen uudelleensuorittamiseen ilman tarvetta myyntitilauksen vahvistamiseen. Kun myyntitilaus on laskutettu, tuottohintaa ei voi laskea uudelleen.

Kahta viimeistä painiketta antaa tietoja niiden myyntitilauksen nimikkeiden tuottoaikataulusta, joilla on tuottoaikataulu.

- **Odotettu tuoton kirjausaikataulu** – Tämä painike tulee käyttöön, kun myyntitilaus on vahvistettu, mutta poistuu käytöstä, kun myyntitilaus on laskutettu. Se avaa sivun, jolla näkyy odotettu tuottoaikataulu. Lopullinen aikataulu voi muuttua, koska odotetussa aikataulussa käytetään pyydettyä lähetyspäivämäärää, kun taas lopullisessa aikataulussa käytetään todellista lähetyspäivämäärää.
- **Tuottokirjauksen aikataulu** – Tämä painike on käytettävissä, kun myyntitilaus on laskutettu. Lopullista tuottokirjauksen aikataulua ei luoda vahvistuksen tai pakkausluettelon luomisen yhteydessä. Se luodaan vain, kun myyntitilaus laskutetaan.

Seuraavassa esimerkissä tuottohinta kohdistettiin myyntitilauksen vahvistamisen yhteydessä. Huomaa, että vaikka tuottohinnat kohdistetaan eri tavoin, **Kirjattava tuotto** -kentän kokonaissumman on vastattava niiden myyntitilausrivien summaa, jotka laskutetaan asiakkaalta. Esimerkiksi myyntitilausrivien summa ilman veroja on 1 499 $. Siten myös **Kirjattavan tuoton** arvojen kokonaissumman on oltava 1 499 $.

[![Tuottohinnan kohdistus.](./media/revenue-recognition-so-basic-revenue-price-allocation.png)](./media/revenue-recognition-so-basic-revenue-price-allocation.png)

Myös odotettu tuoton kirjausaikataulu luodaan. Tuottoaikataulussa siirrettävänä summana käytetään **Kirjattava tuotto** -arvoa. Nimike S0001 siirtää 321,21 dollaria 300 dollarin sijaan ja S0008 siirtää 160,61 dollaria 100 dollarin sijaan. Nimikettä S0012 ei näytetä odotetussa aikataulussa, koska tuottoa ei siirretä. Kun kirjaus tapahtuu, nimikkeellä S0012 kirjataan 1 017,18 $ suoraan tuottokirjanpitotilille.

[![Odotettu tuoton kirjausaikataulu.](./media/revenue-recognition-so-basic-expected-rev-rec-schedule.png)](./media/revenue-recognition-so-basic-expected-rev-rec-schedule.png)

## <a name="create-the-packing-slip"></a>Pakkausluettelon luominen

Seuraavaksi voidaan luoda myyntitilauksen pakkausluettelo. Pakkausluettelon kirjauksen yhteydessä ei kirjata tuottoa. Jos myyntitilausta ei ole vahvistettu, pakkausluettelon kirjaaminen ei käynnistä tuottohinnan laskemista. Se ei myöskään käynnistä odotetun tai lopullisen tuoton kirjausaikataulun luontia. Jos nimikkeen malliryhmä määritetään siirtämään tuottoa pakkausluettelolle, sen kirjaaminen jatkuu kulloisenkin kirjausprofiilin kirjanpitotilejä. Tällöin ei siis käytetä uusia siirretyn tuoton tilejä, joita käytetään laskun kirjaamiseen.

## <a name="create-the-invoice"></a>Laskun luominen

Viimeinen vaihe on myyntitilauksen laskuttaminen. Laskun tositteesta käy ilmi, että nimikkeiden S0001 ja S0008 tuotto siirrettiin (321,21 + 160,61 $ = 481,82 $) ja että jäljellä oleva nimikkeen S0012 summa (1 017,18) kirjattiin tuotoksi. Näiden arvojen kokonaissumma on 1 499 $, joka vastaa myyntitilausrivien summaa.

[![Tositetapahtumat.](./media/revenue-recognition-so-voucher-transactions.png)](./media/revenue-recognition-so-voucher-transactions.png)

Kun lasku on luotu, tuottokirjauksen painikkeet **Tuottohinnan kohdistus**, **Kohdista hinta uudelleen uusille tilausriveille** ja **Tuottokirjauksen aikataulu** tulevat käyttöön, mutta **Päivitä tuottohinnan kohdistus** ja **Odotettu tuoton kirjausaikataulu** eivät ole käytössä.

[![Käytettävissä olevat tuottokirjauksen painikkeet.](./media/revenue-recognition-so-basic-after-invoice-buttons.png)](./media/revenue-recognition-so-basic-after-invoice-buttons.png)

**Tuottohinnan kohdistus**-painike on edelleen käytettävissä, jotta tuottohinnan laskemista voidaan tarkastella. Jos vahvistuksen jälkeen mikään ei ole muuttunut myyntitilauksessa, laskun kirjaus ei muuta **Kirjattava tuotto** -kentän laskettua summaa.

Odotettu tuoton kirjausaikataulu poistetaan ja korvataan lopullisella tuottokirjausaikataululla. Tuottoaikataulun tietoja ylläpidetään kunkin myyntitilausrivin osalta, ja niitä käytetään siirretyn tuoton vapauttamiseen todelliseksi tuotoksi, kun sopimusvelvoitteet on täytetty.

[![Lopullinen tuoton kirjausaikataulu.](./media/revenue-recognition-so-revenue-recognition-schedule.png)](./media/revenue-recognition-so-revenue-recognition-schedule.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
